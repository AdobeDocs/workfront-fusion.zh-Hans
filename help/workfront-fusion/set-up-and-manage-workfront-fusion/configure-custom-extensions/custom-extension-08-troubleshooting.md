---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 自定义扩展疑难解答
description: 自定义扩展疑难解答
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1136
ht-degree: 0%

---


# 自定义扩展疑难解答

>[!NOTE]
>
>本文假定您对软件开发工具有一定的了解。

本文针对在创建自定义扩展时最可能遇到的问题，提供了一些解决方案，这些解决方案大致按照开发过程中遇到的顺序排列。

## 快速核对清单

如果某些功能无法正常工作，请先验证以下内容：

* Node.js的版本为18或20 (`node --version`)。
* 您已登录(`aio login`)并使用正确的组织/项目/工作区(`aio console where`)。
* 扩展点名称完全匹配，包括版本： `fusion/nav-organization/1`。
* `getWidget()`中的`url`与您的应用程序中的路由匹配。
* 您可见的UI调用`attach({ id })`。
* 您在Fusion中查看的扩展集是正确的：
  * 要查看Stage内部版本，请部署到Stage，然后在Fusion配置文件中打开舞台扩展开关（“产品设置”>“Fusion配置文件”>“首选项”）。
  * 要查看已发布的扩展，请部署到生产环境并获得批准。

## 错误1060：“扩展点不存在”

**完整消息：** `CoreConsoleAPISDK ... 1060: Extension point 'fusion/nav-organization/1' does not exist`在`aio app deploy`期间。

**含义：**&#x200B;您的Adobe组织尚未启用Fusion扩展点（“已载入”）。 Adobe会在部署时验证组织的目录中是否存在扩展点。 这是您的代码或YAML的&#x200B;**不是**&#x200B;问题。

**修复：**&#x200B;请求Fusion团队加入您的IMS组织的扩展点（`fusion/nav-organization/1`和/或`fusion/nav-team/1`）。 当您请求载入时，包括：

* 您的&#x200B;**IMS组织ID** (`XXXX@AdobeOrg`)，
* 您所需的&#x200B;**扩展点**，
* 您的&#x200B;**Developer Console项目和工作区**&#x200B;名称。

确认载入后，重新运行`aio app deploy`。


## “等待来自target iframe的初始消息”/面板永远旋转

**含义：** Fusion打开了您的可见UI，但未完成握手，因此Fusion超时。

**常见原因：**

* `attach`仅在注册组件中，不在可见的小部件中。
* `getWidget()`中的`url`指向渲染&#x200B;**注册**&#x200B;组件（或空白页面）而不是您的小组件的路由。
* 传递给`attach`的`id`与`register`中使用的`id`不同。 它们必须相同，因此请将它们保留在`Constants.js`中。

**修复：**&#x200B;确保您的&#x200B;**可见**&#x200B;组件调用`attach({ id })`：

```jsx
useEffect(() => {
  attach({ id: extensionId }).catch(console.error);
}, []);
```

有关详细信息，请参阅[生成自定义扩展UI](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md)。



## 导航按钮未出现在Fusion中

如果您的自定义扩展的导航按钮未在Fusion中显示，请依次检查以下各项：

1. **您是否查看了正确的扩展集？** 默认情况下，Fusion仅显示已部署到生产环境并批准的已发布扩展。 如果要测试Stage内部版本，请在Fusion配置文件（“产品设置”>“Fusion配置文件”>“首选项”）中打开Stage扩展开关，然后重新加载。 阶段项标记为&#x200B;**（阶段）**。
有关详细信息，请参阅[发布您的自定义扩展](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md)。
1. **是撤消还是撤回？** 已撤销或撤销的扩展停止出现在Fusion中，并且没有错误。 如果以前工作的按钮消失，请先确认该按钮在Adobe Exchange中仍处于活动状态，然后再查找代码问题。
1. **是否将其部署到正确的工作区？** 使用暂存测试开关时，将部署到您实际加载的工作区和暂存工作区。
1. **是否将其部署到正确的组织？** 使用您部署到的&#x200B;**相同** IMS组织中的帐户登录到Fusion。
1. **它是否位于正确部分？** `fusion/nav-organization/1`显示在&#x200B;**组织**&#x200B;下；`fusion/nav-team/1`显示在&#x200B;**团队**&#x200B;下（您必须先选择一个团队）。
1. **是否存在扩展点名称拼写错误？** 它必须完全读取`app.config.yaml`和文件夹的`ext.config.yaml`包含路径中的`fusion/nav-organization/1`。


## 按钮出现，但面板为空白

如果出现按钮但面板为空，请检查以下各项：

* **路由不匹配：**&#x200B;来自`getWidget()`的`url`（如`/index.html#/my-widget`）必须与`App.js`中的`<Route>`匹配。 不匹配加载不带组件的页面。
* **JavaScript错误：**&#x200B;打开浏览器的开发人员工具(F12) > **控制台**&#x200B;选项卡，并查找来自iframe的错误。 修复报告的错误并重新部署。
* **标题缺失/重复：`getWidget()`中的** `hideWidgetHeader`控制Fusion是否在UI上方显示标题。 如果您渲染自己的标头，请将其设置为`true`。

## iframe被阻止（内容安全策略/“拒绝帧”）

Fusion仅允许在Adobe的App Builder CDN (`*.adobeio-static.net`)上托管的扩展，默认情况下，`aio app deploy`会将您的文件放在该CDN上。 如果您将UI托管在其他位置，例如自定义域，则Fusion拒绝加载它。 按照文档说明通过App Builder部署，或询问Fusion团队您的域是否可以部署。

## 上下文为空或已过时

* **加载后立即为空：**&#x200B;解析后&#x200B;**`attach`读取上下文**，而不是之前。 在此之前，将显示“正在连接……”状态。
* **当用户切换组织或团队时未更新：**&#x200B;订阅`contextchange`事件并重新读取处理程序中的密钥。 有关详细信息，请参阅“生成自定义扩展UI”一文中的[阅读上下文Fusion共享](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md#read-the-context-fusion-shares)。
* **日期错误：**&#x200B;日期字段以ISO **字符串**&#x200B;形式到达，而不是`Date`对象。 将它们包装在`new Date(...)`中。 请参阅Fusion上下文引用的文章中的[日期](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md#dates)。

## 调用API失败，并出现CORS错误

**症状：**&#x200B;当您的UI直接调用Workfront/Fusion API时，浏览器控制台显示&#x200B;*“无‘Access-Control-Allow-Origin’标头”*（或请求被阻止）。

**修复：**&#x200B;不要从浏览器调用这些API。 通过您自己的App Builder **运行时操作**（服务器端，无CORS）路由调用，并让访客使用相对的同源URL调用该操作。 有关详细信息，请参阅[调用Workfront和Fusion API](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md)。


## 即使使用有效令牌，代理操作也会返回401

**含义：**&#x200B;对于`require-adobe-auth: true`，Adobe网关会在您的操作运行之前验证调用，可以拒绝它或丢弃您的上游需要的自定义标头，显示为`401`。

**修复：**&#x200B;在操作&#x200B;**上设置`require-adobe-auth: false`并**&#x200B;自己强制执行授权。 操作中需要`Authorization`持有者，将其转发到上游，并保持严格的目标。 请参阅[require-adobe-auth： true与false](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#require-adobe-auth-true-vs-false)。

## 融合`GET /api/v3/hooks`返回400

**含义：**&#x200B;挂接终结点为&#x200B;**团队范围**，因此`teamId`是必需的查询参数。

**修复：**&#x200B;调用`/api/v3/hooks?teamId=<team.id>`。 钩子只为活动团队返回。 要覆盖组织，请循环其团队并合并。 相反，方案接受`organizationId`。 查看[Fusion v3 API详细信息](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md#fusion-v3-api-specifics)。


## `aio`个错误

* **`aio: command not found`：** CLI未安装或未安装在您的路径上。 重新运行`npm install -g @adobe/aio-cli`，然后打开新终端。
* **在全新节点版本**&#x200B;上生成/部署失败。请使用节点&#x200B;**18或20 LTS**。 非常新的、非LTS版本有时会破坏工具链。
* **“您不是开发人员”/看不到您的组织：**&#x200B;您的Adobe组织管理员必须向您授予&#x200B;**开发人员**&#x200B;角色和App Builder访问权限。 有关详细信息，请参阅[设置用户界面扩展工具和帐户](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)。
* **401 /部署或发现期间的令牌无效：**&#x200B;您的会话已过期或您正在混合环境。 运行`aio logout`，然后运行`aio login`，确认`aio console where`，并部署到要加载的工作区。

## 收集支持信息

收集此信息以更快地作出诊断：

* 您运行的确切命令和&#x200B;**full**&#x200B;错误输出。
* 您的&#x200B;**IMS组织ID**、**项目**&#x200B;和&#x200B;**工作区**。
* 您定位的&#x200B;**扩展点**。
* `aio app deploy`是否成功，扩展是否为&#x200B;**已发布**（或者，对于暂存测试，暂存扩展开关是否打开）。
* 在Fusion中打开面板时，浏览器&#x200B;**控制台** (F12)中的任何错误。
