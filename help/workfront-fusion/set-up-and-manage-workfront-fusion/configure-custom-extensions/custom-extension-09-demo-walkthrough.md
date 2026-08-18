---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 自定义扩展的演示演练
description: 自定义扩展的演示演练
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
source-wordcount: 964
ht-degree: 0%

---


# 在Fusion中创建自定义扩展的演示演练

>[!NOTE]
>
>本文假定您对软件开发工具有一定的了解。

此演示将介绍如何创建自定义扩展、如何部署以及在Fusion中运行该扩展。

其包括：

* 通过通用App Builder Shell模板为Experience Cloud应用程序搭建基架。
* 将应用程序重新定位到Fusion扩展点。
* 将应用程序部署到暂存工作区。
* 在Fusion中打开暂存测试并显示应用程序正在运行。

从模板而不是空的`--standalone-app`开始表示已为您生成SPA引导：`index.js`、`exc-runtime.js`、`App.js`（路由选择和`ErrorBoundary`）以及示例`ExtensionRegistration`。 演示中的实时步骤是重新定位配置并编辑两个文件，这恰恰是生成实际`fusion-uix-guest`的方式。

>[!NOTE]
>
> **时间：**&#x200B;在工具设置后，实时演示大约需要10分钟。 在&#x200B;**演示之前，您必须执行一次性设置(Node 18/20， `aio` CLI， `aio login`)**。 有关说明，请参阅[设置用户界面扩展工具和帐户](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)。


## 开始之前

此操作只需执行一次，并且可在演示之前在摄像头外完成。

```sh
node --version          # must be 18 or 20
aio --version           # @adobe/aio-cli installed
aio login               # signs you into your Adobe org
aio console org select  # pick the org you'll demo in (same org as Fusion)
```

在演示组织中，必须做到以下两点：

* 已为组织载入`fusion/nav-organization/1`扩展点。 如果未载入，则部署将失败，并出现错误1060。 有关详细信息，请参阅[自定义扩展疑难解答](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)。
* 自定义扩展功能会在Fusion主机中启用。 （默认情况下，此功能处于打开状态）。 由于您将演示Stage内部版本而不是已发布的内部版本，因此还将打开Fusion配置文件中的&#x200B;**Stage扩展**&#x200B;开关。 （此开关如步骤7中所示。） Fusion将仅显示已发布的扩展，直到您执行该操作为止。

## 步骤1：从通用模板生成应用程序

```sh
aio app init my-fusion-extension --template @adobe/generator-app-excshell
cd my-fusion-extension
```

* 出现提示时，选择&#x200B;**新建项目**，然后接受建议的名称。
* `@adobe/generator-app-excshell`是通用的&#x200B;**Experience Cloud Shell** UI扩展模板，不是产品特定的。 它为`src/dx-excshell-1/`下的完整、有效的SPA提供基架。

>[!NOTE]
>
>如果您更喜欢此菜单，请运行`aio app init my-fusion-extension`，选择&#x200B;**添加扩展或独立应用程序** > **模板**，然后选择&#x200B;**“适用于Experience Cloud Shell的App Builder UIX扩展”**。

您将获得一组文件，其中包括以下内容：

```
my-fusion-extension/
|-- app.config.yaml
|-- src/dx-excshell-1/
    |-- ext.config.yaml
    |-- web-src/src/
        |-- index.js          // SPA bootstrap (exc-app Runtime + React render)
        |-- exc-runtime.js    // Experience Cloud Shell runtime glue
        |-- components/
            |-- App.js                    // Router + ErrorBoundary (generated)
            |-- ExtensionRegistration.js  // sample registration (generated)
```

## 步骤2：添加Fusion来宾库

模板已包括React、React Spectrum和exc-app。 添加与Fusion主机对话的库：

```sh
npm install @adobe/uix-guest
```

## 步骤3：将配置重新定位到Fusion

打开&#x200B;**`app.config.yaml`**&#x200B;并仅将&#x200B;**扩展点键**&#x200B;从Experience Cloud Shell点更改为Fusion点（保留`$include`路径）：

```yaml
extensions:
  fusion/nav-organization/1:                 # was: dx/excshell/1
    $include: src/dx-excshell-1/ext.config.yaml
```

您无需更改配置中的任何其他内容。 文件夹名称`dx-excshell-1`是内部名称，不会影响Fusion，因此您可以离开它。 重命名还意味着更新任何操作路径。 在演示中跳过该步骤。

>[!NOTE]
>
>如果您正在定位&#x200B;**团队**&#x200B;分区，请改用`fusion/nav-team/1`。 若要在生产环境中同时发运&#x200B;**组织**&#x200B;和团队，请使用&#x200B;**两个不同的项目**。 每个注册表名称一个扩展点捆绑包可避免共享应用程序冲突。

## 步骤4：编辑注册和Widget文件

所有路径都在`src/dx-excshell-1/web-src/src/components/`下。

### **`ExtensionRegistration.js`**

生成的文件注册一个Experience Cloud Shell示例。 将其`methods`替换为Fusion **`dashboard.getWidget`**&#x200B;合同，以便Fusion知道您的标题和UI所在的位置：

```js
import { Text } from "@adobe/react-spectrum";
import { register } from "@adobe/uix-guest";
import metadata from "../../../../app-metadata.json";
import { extensionId } from "./Constants";

function ExtensionRegistration() {
  const init = async () => {
    await register({
      id: extensionId,
      metadata,
      methods: {
        dashboard: {
          getWidget() {
            return {
              id: extensionId,
              title: "My Fusion tool",          // label on the Fusion nav button
              description: "Hello from App Builder",
              url: "/index.html#/widget",       // route to the visible UI (4b)
              widgetSize: { defaultWidth: 6, defaultHeight: 6 },
              hideWidgetHeader: false,
            };
          },
        },
      },
    });
  };
  init().catch(console.error);

  return <Text>Registering with Fusion...</Text>;
}

export default ExtensionRegistration;
```

如果`Constants.js`旁边不存在，请创建它：

```js
module.exports = { extensionId: "my-fusion-extension" };
```

### `DashboardWidget.js`

创建此文件。 它完成握手并显示实时Fusion上下文：

```js
import { useEffect, useState } from "react";
import { Flex, Heading, Text, View } from "@adobe/react-spectrum";
import { attach } from "@adobe/uix-guest";
import { extensionId } from "./Constants";

const KEYS = ["imsOrgId", "imsUserId", "organization", "team", "user"];

export default function DashboardWidget() {
  const [ctx, setCtx] = useState(null);

  useEffect(() => {
    attach({ id: extensionId })
      .then((guest) => {
        const read = () =>
          KEYS.reduce((acc, k) => ({ ...acc, [k]: guest.sharedContext.get(k) }), {});
        setCtx(read());
        guest.addEventListener("contextchange", () => setCtx(read()));
      })
      .catch((e) => console.error("attach failed", e));
  }, []);

  return (
    <View padding="size-300">
      <Heading level={2}>Hello from App Builder</Heading>
      {!ctx ? (
        <Text>Connecting to Fusion...</Text>
      ) : (
        <Flex direction="column" gap="size-100" marginTop="size-200">
          <Text>User: {ctx.user?.name ?? ctx.imsUserId}</Text>
          <Text>Organization: {ctx.organization?.name} (id {ctx.organization?.id})</Text>
          <Text>Team: {ctx.team?.name ?? "-"}</Text>
        </Flex>
      )}
    </View>
  );
}
```

### `App.js`

生成的路由器已将`index` / `index.html`发送到`ExtensionRegistration`。 为构件添加路由并将其导入：

```js
import DashboardWidget from "./DashboardWidget";
// ...inside <Routes>, alongside the existing ExtensionRegistration routes:
<Route exact path="widget" element={<DashboardWidget />} />
```

> 路由路径(`widget`)必须匹配`getWidget().url` (`/index.html#/widget`)中的哈希。 将生成的`index.js` / `exc-runtime.js`和`App.js`的其余部分完全保持为基架结构，因为这是您希望模板提供的引导。

## 步骤5：构建

```sh
aio app build
```

这将编译前端并运行生成`app-metadata.json`的元数据挂接。 请在继续之前修复所有错误。

## 步骤6：部署到暂存环境

```sh
aio console workspace select     # choose Stage
aio app deploy
```

`deploy`在Adobe的CDN上托管您的UI，并在Stage工作区中注册扩展端点，这允许Fusion发现它。 CLI打印终结点URL，如`https://<project>-stage.adobeio-static.net`。

## 步骤7：打开暂存测试并在Fusion中显示扩展

1. Experience Cloud上的Open Fusion，已登录到您部署到的相同组织。
1. 打开用户头像菜单，然后转到&#x200B;**产品设置** > **Fusion配置文件** > **首选项**。
1. 打开&#x200B;**暂存扩展**&#x200B;开关并确认重新加载。

   Fusion现在从暂存工作区加载扩展并将它们标记为&#x200B;**（暂存）**。
1. 转到左侧导航的&#x200B;**组织**&#x200B;区域。

   出现&#x200B;**“我的融合工具（舞台）”**&#x200B;按钮。
1. 单击&#x200B;**“My Fusion tool (Stage)”**&#x200B;按钮。
您的UI将加载到主面板中，并显示实时用户、组织和团队。
1. **在Fusion中切换活动组织或团队**。

   面板更新，用于演示实时上下文(`contextchange`)。

>[!TIP]
>
>如果未显示该按钮，请重新加载一次，因为每个会话都会缓存发现。 然后，请参阅[自定义扩展疑难解答](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)。


## 在演示过程中迭代

进行更改，然后重建并重新部署。  用户下次打开时将会看到更新的扩展。

```sh
aio app build && aio app deploy
```

## 演示后转至生产

Stage足以演示。 要在整个组织范围内发布应用程序，请切换到生产工作区，部署并提交审批请求。 必须使用系统管理员角色提交请求。 有关完整流程，请参阅[发布生产](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md#release-on-production)。

## 演示对话跟踪（可选）

在实时演示过程中，您可能需要提出以下几点：

* **“我从通用Experience Cloud Shell模板启动。”** 它支撑着整个SPA Shell，因此我仅重新定位了扩展点并编辑了两个文件。
* **“Fusion是主机，我的应用程序是来宾。”** 它们在不同的框架中运行，并讨论Adobe的UI可扩展性SDK，而无需自定义联网。
* **“注册与查看”** 隐藏帧&#x200B;*注册*&#x200B;我提供的内容(`dashboard.getWidget`)，可见帧&#x200B;*附加*&#x200B;并读取上下文。
* **“暂存测试是每个用户的切换。”** 默认情况下，Fusion仅显示已发布的扩展。 我在Fusion配置文件中翻转Stage扩展，加载我的Stage版本，而不发布生产版本。
* **“实时上下文”。** 切换组织或团队会重新发送上下文，然后访客会重新呈现。
