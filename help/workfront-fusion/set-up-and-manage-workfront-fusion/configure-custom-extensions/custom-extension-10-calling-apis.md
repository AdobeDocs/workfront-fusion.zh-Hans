---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 从扩展中调用Workfront和Fusion API
description: 从扩展中调用Workfront和Fusion API
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1083
ht-degree: 0%

---


# 从扩展中调用Workfront和Fusion API

>[!NOTE]
>
>本文假定您对软件开发工具有一定的了解。

Fusion上下文引用会为您提供登录用户的IMS令牌，因此自然而然的下一步是调用Workfront或Fusion API并显示实际数据。 由于CORS，这是不可能的。 本文介绍如何使用App Builder运行时操作作为服务器端代理来绕过此限制，并包含示例（事件订阅仪表板）。

## 为什么直接浏览器调用失败(CORS)

您的可见UI在从Adobe CDN (`https://<your-app>.adobeio-static.net`)提供的`<iframe>`中运行。 当该页面对&#x200B;**其他**&#x200B;源上的Workfront或Fusion API执行`fetch(...)`操作时，浏览器将实施跨源资源共享(CORS)。 除非API为您的CDN源明确返回`Access-Control-Allow-Origin`，否则浏览器将阻止响应。 这些API不会允许列表任意扩展源，因此来自访客的直接调用会失败。

有关CORS的信息，请参阅[CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS)。

## 在不使用CORS的情况下调用您自己的运行时操作

此问题的解决方法是在不使用CORS的情况下调用您自己的运行时操作。

App Builder应用程序可以包括运行时操作，这些操作是在Adobe I/O Runtime服务器端运行的小型无服务器函数。 服务器到服务器调用不受浏览器CORS限制。 由于该操作是应用程序的一部分，因此访客可以使用相对URL调用它，该URL是同域的，因此不会被阻止。

```
  Guest UI (browser, adobeio-static.net)
     │  fetch('/api/v1/web/<app>/wf-proxy?...')   ← relative = same-origin, no CORS
     ▼
  Your runtime action  (Adobe I/O Runtime, server-side)
     │  fetch('https://fusion.adobe.com/api/v3/...')  ← server-to-server, no CORS
     ▼
  Workfront / Fusion API
```

该操作从来宾接收用户的IMS令牌并将其转发到上游，因此仍代表用户使用其权限进行调用。

## 第1步：声明操作

运行时操作在扩展的`runtimeManifest`下的`app.config.yaml`中声明。 在扩展旁边添加`wf-proxy`操作：

```yaml
extensions:
  fusion/nav-organization/1:
    $include: src/fusion-nav-organization-1/ext.config.yaml
    runtimeManifest:
      packages:
        fusion-uix-guest:                # ← your package name; part of the action URL
          license: Apache-2.0
          actions:
            wf-proxy:
              function: src/fusion-nav-organization-1/actions/wf-proxy/index.js
              web: 'yes'                  # exposes it at /api/v1/web/<package>/wf-proxy
              runtime: nodejs:22
              inputs:
                LOG_LEVEL: debug
              annotations:
                require-adobe-auth: false # see note below
                final: true
```

该操作将在以下位置变为可访问：

```
/api/v1/web/<package>/<action>     e.g.  /api/v1/web/fusion-uix-guest/wf-proxy
```

### `require-adobe-auth`： true与false

此注释控制Adobe的网关在操作运行之前是否验证IMS令牌。

* **`true`：**&#x200B;安全默认值。  网关拒绝未经身份验证的调用。 但是，验证器会严格限制它预期的标头，并且可能会拒绝请求或丢弃上游调用所需的自定义标头。 如果发生这种情况，即使您的令牌有效，它也会显示为`401`。
* **`false`：**&#x200B;跳过网关检查。 您的操作随后可公开调用，因此您&#x200B;**必须**&#x200B;自己强制执行授权。 操作中需要`Authorization`持有者，如果缺少则拒绝，然后向上游转发该持有者，Workfront和Fusion将验证它。 与步骤2中描述的严格目标允许列表相结合，这是需要传递自定义标头的代理的可靠路径。

>[!TIP]
>
> 请先尝试`true`。 如果您看到无法解释的`401`，因为该令牌有效且在其他位置工作，请切换到`false` **和**，保留操作中的持有者检查并允许列表，以便上游仍强制实施安全性。

## 步骤2：为代理编写操作

创建`src/fusion-nav-organization-1/actions/wf-proxy/index.js`。 有两个规则可以确保此安全：上游目标的允许列表，以便该操作不能用作开放中继，以及上游转发的必需持有者令牌。

```js
const fetch = require('node-fetch')
const { Core } = require('@adobe/aio-sdk')
const { errorResponse, getBearerToken, checkMissingRequestInputs } = require('../utils')

// Page-through query params (see "Paginate list results" below).
const pageQuery = (p) => {
  const q = new URLSearchParams()
  if (p.start != null) q.set('start', p.start)
  if (p.limit != null) q.set('limit', p.limit)
  return q
}

// Only these upstreams may be reached. Never build the URL from arbitrary input.
const TARGETS = {
  subscriptions: {
    method: 'GET',
    url: () => 'https://<your-wf-host>/attask/eventsubscription/api/v1/subscriptions',
  },
  hooks: {
    method: 'GET',
    // Fusion hooks are team-scoped: teamId is a REQUIRED query param (see below).
    url: (p) => {
      const q = pageQuery(p)
      if (p.teamId) q.set('teamId', p.teamId)
      return `https://fusion.adobe.com/api/v3/hooks?${q.toString()}`
    },
  },
  scenarios: {
    method: 'GET',
    url: (p) => {
      const q = pageQuery(p)
      if (p.fusionOrgId) q.set('organizationId', p.fusionOrgId)
      return `https://fusion.adobe.com/api/v3/scenarios?${q.toString()}`
    },
  },
}

async function main (params) {
  const logger = Core.Logger('main', { level: params.LOG_LEVEL || 'info' })
  try {
    const missing = checkMissingRequestInputs(params, ['target'], ['Authorization'])
    if (missing) return errorResponse(400, missing, logger)

    const target = TARGETS[params.target]
    if (!target) return errorResponse(400, `unknown target '${params.target}'`, logger)

    const token = getBearerToken(params)              // reads params.__ow_headers.authorization
    const headers = { authorization: `Bearer ${token}`, 'content-type': 'application/json' }
    if (params.orgId) headers['x-gw-ims-org-id'] = params.orgId        // Adobe IMS org id
    if (params.fusionOrgId) headers['x-organization-id'] = params.fusionOrgId  // Fusion tenant id
    if (params.teamId) headers['x-team-id'] = params.teamId            // Fusion team id

    const res = await fetch(target.url(params), { method: target.method, headers })
    const text = await res.text()
    let body
    try { body = JSON.parse(text) } catch (e) { body = text }

    if (!res.ok) {
      return { statusCode: res.status, body: { error: `upstream ${res.status}`, target: params.target, details: body } }
    }
    return { statusCode: 200, body }
  } catch (error) {
    logger.error(error)
    return errorResponse(500, 'server error: ' + error.message, logger)
  }
}

exports.main = main
```

`getBearerToken`、`errorResponse`和`checkMissingRequestInputs`来自生成的`actions/utils.js`，模板将他们作为基架。 `getBearerToken`读取`params.__ow_headers.authorization`，网关将传入的`Authorization`标头放置在该位置。

## 步骤3：从来宾中调用操作

从您的UI中，`fetch`具有相对（同源） URL的操作，并将IMS令牌作为持有者发送。 将上游所需的组织和团队ID作为查询参数进行传递。

```js
const PROXY_URL = "/api/v1/web/fusion-uix-guest/wf-proxy";

async function callProxy(target, token, { imsOrgId, fusionOrgId, teamId, start, limit } = {}) {
  const params = new URLSearchParams({ target });
  if (imsOrgId) params.set("orgId", imsOrgId);          // → x-gw-ims-org-id
  if (fusionOrgId) params.set("fusionOrgId", fusionOrgId); // → x-organization-id
  if (teamId) params.set("teamId", teamId);             // → x-team-id
  if (start != null) params.set("start", start);        // pagination offset
  if (limit != null) params.set("limit", limit);        // pagination page size
  const res = await fetch(`${PROXY_URL}?${params.toString()}`, {
    headers: { authorization: `Bearer ${token}` },
  });
  if (!res.ok) throw new Error(`${target} request failed: ${res.status}`);
  return res.json();
}
```

从上下文获取`token`、`imsOrgId`、`fusionOrgId`和`teamId`：

```js
const token       = connection.sharedContext.get("imsToken");
const imsOrgId    = connection.sharedContext.get("imsOrgId");
const fusionOrgId = connection.sharedContext.get("organization")?.id; // Fusion tenant id
const teamId      = connection.sharedContext.get("team")?.id;
```

有关上下文的信息，请参阅[Fusion上下文引用](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)。

## Fusion v3 API详情

对于`https://fusion.adobe.com/api/v3`的仪表板适用的内容：

| 标题/参数 | 价值 | 注释 |
| ---------------- | ------- | ------- |
| `Authorization` | `Bearer <imsToken>` | 上下文中的用户的IMS令牌。 |
| `x-organization-id` | `organization.id` | Fusion自己的租户ID，而不是IMS组织ID。 Fusion通过它来标识租户。 |
| `x-team-id` | `team.id` | 当调用属于团队范围时发送。 |
| `x-gw-ims-org-id` | `imsOrgId` | 网关的Adobe IMS组织ID。 |

请注意以下注意事项：

* **`GET /api/v3/hooks`是团队范围：** `teamId`是&#x200B;**必需的查询参数** (`/api/v3/hooks?teamId=...`)。 没有它，您会获得`400`。 这意味着挂接仅针对&#x200B;*活动团队返回*；覆盖组织、循环团队和合并。
* **`GET /api/v3/scenarios`**&#x200B;与`organizationId` (`/api/v3/scenarios?organizationId=...`)配合使用。

>[!NOTE]
>
> 官方引用是Adobe的[Workfront Fusion API](https://developer.adobe.com/workfront-fusion-apis/)。 标头/身份验证要求因网关而异。 此表反映了演示的实际需求。 如果调用返回`401`/`400`，请先重新检查这些标头。

## 按页显示列表结果

Fusion v3列表端点（挂接、场景）一次返回一个&#x200B;**页面**，而不是整个集。 响应如下所示：

```json
{
  "items": [ /* ...this page of records... */ ],
  "_page": { "start": 0, "limit": 100, "total": 342 }
}
```

记录在&#x200B;**`items`**&#x200B;下，分页元数据在&#x200B;**`_page`**&#x200B;下。 您使用&#x200B;**`start`**（偏移量）和&#x200B;**`limit`**（页面大小）查询参数进行页面。 上述代理同时传递两者，因此在收集所有内容之前，通过循环在访客中翻页：

```js
const PAGE_LIMIT = 100;

async function fetchAllPages(target, token, opts = {}) {
  const all = [];
  let start = 0;
  // Stop when a page returns fewer than PAGE_LIMIT items, or when _page.total is reached.
  for (;;) {
    const res = await callProxy(target, token, { ...opts, start, limit: PAGE_LIMIT });
    const items = res.items ?? [];
    all.push(...items);

    const total = res._page?.total;
    const done = items.length < PAGE_LIMIT || (total != null && all.length >= total);
    if (done) break;
    start += PAGE_LIMIT;
  }
  return all;
}
```

如果您希望从浏览器中发出寻呼，请在运行时操作内执行相同的循环，并在一个响应中返回合并的`items`数组。 无论如何，请不要假定第一页是整个结果集。 否则，具有多页钩子的团队将看起来缺少场景。

## 安全核对清单

* **允许列表上游。** 切勿通过原始客户端输入构造目标URL。 将短的`target`键映射到固定URL，如步骤2中所示。 这样可防止您的操作成为开放式中继。
* **在操作中需要持有者令牌**，并将其向上游转发。 让Workfront和Fusion强制实施用户的权限。
* **从不记录令牌。** `imsToken`是凭据。 让`LOG_LEVEL`留意`stringParameters`打印的内容。
* **仅通过HTTPS**&#x200B;转发到受信任的Adobe和Workfront主机。

## 工作示例：事件订阅仪表板

演示仪表板将连接三个源，以根据Workfront事件订阅显示匹配的Fusion场景是否正常：

1. `fetchSubscriptions()`Workfront事件订阅（带有已接收/传递的计数器）。
1. 活动团队的`fetchHooks(teamId)`个→ Fusion挂接（通过`fetchAllPages`分页）。
1. `fetchScenarios(fusionOrgId)`组织→Fusion方案（通过`fetchAllPages`分页）。

**join**&#x200B;将它们链结，但有一个需要注意的问题：Workfront订阅和它的Fusion挂接指向&#x200B;**不同主机**&#x200B;上的实时位置，因此它们的URL字段并非完全相同。 稳定的是webhook URL **（最后一个路径段）末尾的**&#x200B;令牌。 匹配该尾随令牌，而不是完整URL。 然后，挂接的`scenarioId`与方案的`id`匹配：

```
subscription.targetUrl  ──(trailing token)──▶  hook.url
                                                hook.scenarioId  ──▶  scenario.id
```

```js
// Reduce a webhook URL to its trailing token so hosts/bases can differ.
function hookKey(url) {
  if (!url) return "";
  const path = String(url).trim().toLowerCase().split(/[?#]/)[0].replace(/\/+$/, "");
  const i = path.lastIndexOf("/");
  return i >= 0 ? path.slice(i + 1) : path;
}

// Index hooks by token, then look each subscription up by the same token.
const hooksByToken = new Map(hooks.map((h) => [hookKey(pick(h, ["url", "address", "targetUrl"], "")), h]));
const hook = hooksByToken.get(hookKey(pick(sub, ["url", "endpointUrl", "targetUrl", "target.url", "callbackUrl"], "")));
```

状态派生自连接：

* **已中断**：没有匹配的挂接，或者挂接是`gone`。
* **正在筛选**：已匹配，但`passed < received`（事件已到达，但在方案运行之前已筛选掉）。
* **正常**：匹配并传递。

由于实际有效负载形状不同，因此客户端会防御性地映射字段，在每个字段中尝试多个候选键，因此API的细微差异不会破坏表：

```js
function pick(obj, keys, fallback) {
  for (const key of keys) {
    const value = key.split(".").reduce((acc, part) => (acc == null ? acc : acc[part]), obj);
    if (value != null) return value;
  }
  return fallback;
}
```

这只是个例子。 相同的代理模式适用于您需要的任何Workfront或Fusion API。
