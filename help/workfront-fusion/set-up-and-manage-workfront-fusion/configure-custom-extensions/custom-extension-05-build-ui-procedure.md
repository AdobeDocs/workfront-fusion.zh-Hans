---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 构建自定义扩展UI
description: 构建自定义扩展UI
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
source-wordcount: 440
ht-degree: 0%

---


# 构建自定义扩展UI

>[!NOTE]
>
>本文假定您对软件开发工具有一定的了解。

此过程描述如何生成用户实际看到的屏幕，以及如何使用Fusion完成&#x200B;**连接（“握手”）**。

在此过程中，请务必记住，扩展在两个框架中运行：隐藏的&#x200B;**注册**&#x200B;框架和可见的&#x200B;**UI**&#x200B;框架。

有关与自定义扩展相关的框架的信息，请参阅UI扩展中包含的[框架](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension)。

有关构建注册框架的说明，请参阅[创建用于UI扩展性的项目](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md)。

## 在两个帧之间布线

两帧加载相同的`index.html`；小型前端路由器根据URL决定要显示的组件。

1. 在`web-src/src/components/App.js`中设置路由。 关键部分是：

   ```jsx
   import { HashRouter as Router, Routes, Route } from "react-router-dom";
   import ExtensionRegistration from "./ExtensionRegistration";
   import DashboardWidget from "./DashboardWidget";
   
   export default function App() {
     return (
       <Router>
         <Routes>
           {/* Background frame: registers the extension with Fusion */}
           <Route index element={<ExtensionRegistration />} />
           <Route path="index.html" element={<ExtensionRegistration />} />
   
           {/* Visible frame: the URL you returned from getWidget() */}
           <Route path="my-widget" element={<DashboardWidget />} />
         </Routes>
       </Router>
     );
   }
   ```

   这些路由将映射到以前的配置，如下所示：

   * 默认路由(`index`)呈现&#x200B;**`ExtensionRegistration`**，即调用`register(...)`的隐藏帧。
   * `my-widget`路由呈现您可见的UI **`DashboardWidget`**。 这与您在[上一页](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md)中从`getWidget()`返回的`url: "/index.html#/my-widget"`匹配。

   >[!NOTE]
   >
   > **路由和`getWidget` URL必须一致。** 如果更改路由名称，请同时更改`url`，否则Fusion将加载空白页。

1. 继续[完成与`attach`](#complete-the-handshake-with-attach)的握手。

## 使用`attach`完成握手

这是可见UI中最重要的一行。 当Fusion打开您的UI框架时，将等待该框架“签入”。 您的代码通过调用`attach({ id })`签入。

**如果省略，Fusion将超时**，并出现错误，例如&#x200B;*“正在等待来自目标iframe的初始消息。”*

1. 将以下内容添加到`web-src/src/components/DashboardWidget.js`：

   ```jsx
   import { useEffect, useState } from "react";
   import { attach } from "@adobe/uix-guest";
   import { extensionId } from "./Constants";
   
   export default function DashboardWidget() {
     const [connection, setConnection] = useState(null);
   
     useEffect(() => {
       // Tell Fusion this UI frame is ready. Required.
       attach({ id: extensionId })
         .then(setConnection)
         .catch((e) => console.error("attach failed", e));
     }, []);
   
     if (!connection) {
       return <p>Connecting to Fusion...</p>;
     }
   
     return <h2>Hello from my Fusion extension!</h2>;
   }
   ```

   此代码执行以下操作：

   * Fusion响应后，`attach({ id })`将返回&#x200B;**连接对象**。 我们建议保存此内容，因为您将在下一步中使用它来读取Fusion发送的上下文。
   * 在连接解析之前，出现一个简短的“Connecting...”（连接……） 将显示消息。
   * 使用您在`Constants.js`中设置的&#x200B;**相同`extensionId`**。

   此时，您拥有一个有效的扩展：该扩展注册、附加和显示消息。 之后的所有工作都是关于使用数据融合的。

1. 继续[读取上下文Fusion共享](#read-the-context-fusion-shares)。

## 读取上下文Fusion共享

在附加该连接后，该连接会公开一个&#x200B;**共享上下文**，其中包含有关当前用户、组织和团队的信息。 您可以使用`connection.sharedContext.get("<key>")`读取单个值：

```jsx
const orgId = connection.sharedContext.get("imsOrgId");
const organization = connection.sharedContext.get("organization"); // full Fusion org
const user = connection.sharedContext.get("user");                 // full Fusion user
```

此示例显示了一个完整的被动示例，当用户切换组织或团队时，该示例也会更新：

```jsx
import { useEffect, useState } from "react";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

function readContext(source) {
  // sharedContext behaves like a Map (.get); the change event gives a plain object.
  const get =
    typeof source.get === "function" ? (k) => source.get(k) : (k) => source[k];
  return Object.fromEntries(KEYS.map((k) => [k, get(k)]));
}

export default function DashboardWidget() {
  const [context, setContext] = useState(null);

  useEffect(() => {
    let cleanup = () => {};
    attach({ id: extensionId })
      .then((connection) => {
        // 1) initial values
        setContext(readContext(connection.sharedContext));

        // 2) react to org/team/user changes pushed by Fusion
        const onChange = (event) =>
          setContext(readContext(event?.detail?.context ?? connection.sharedContext));
        connection.addEventListener("contextchange", onChange);
        cleanup = () => connection.removeEventListener?.("contextchange", onChange);
      })
      .catch((e) => console.error("attach failed", e));
    return () => cleanup();
  }, []);

  if (!context) return <p>Connecting to Fusion...</p>;

  return (
    <div>
      <h2>{context.organization?.name ?? "No organization"}</h2>
      <p>Signed in as {context.user?.name} ({context.user?.email})</p>
      <p>IMS org: {context.imsOrgId}</p>
    </div>
  );
}
```

请记住以下内容：

* **直接在`attach`之后从`connection.sharedContext.get(key)`中读取初始值**。
* **订阅`contextchange`**&#x200B;以保持同步。 每当活动的组织、团队或用户发生更改时，Fusion都会触发此事件。 新值在`event.detail.context`到达。

有关键的完整列表以及每个键所包含的内容，均包含在[Fusion上下文引用](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)中。

要继续配置自定义扩展的过程，请转到[Fusion上下文引用](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)。
