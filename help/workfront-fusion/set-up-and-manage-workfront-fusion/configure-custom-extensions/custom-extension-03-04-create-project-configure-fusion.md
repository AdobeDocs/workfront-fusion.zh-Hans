---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 为用户界面可扩展性创建项目
description: 为用户界面可扩展性创建项目
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 1360
ht-degree: 0%

---

# 为用户界面可扩展性创建项目

>[!NOTE]
>
>本文假定您对软件开发工具有一定的了解。

要创建自定义UI扩展，您必须为其创建一个App Builder项目。

本页介绍如何使用`aio`命令行生成通用App Builder项目。 “通用”表示项目&#x200B;**不**&#x200B;是从产品特定的模板开始的。 使用通用应用程序启动可以使项目变得简单，并且允许项目与Workfront Fusion连接。

熟悉以下有关创建项目以用于Adobe Fusion AI扩展性的概念和术语可能会很有用。

* **Adobe Developer Console** (<https://developer.adobe.com/console>)是您的项目所在的Web仪表板。

* **术语**：

  | 术语 | 它的含义 |
  | ------ | --------------- |
  | **组织** | 您公司的Adobe组织。 与在Fusion中使用的组织相同。 |
  | **项目** | 一个应用程序/扩展的容器。 您将为扩展创建一个项目。 |
  | **工作区** | 工作阶段的项目配置副本。 每个项目都有一个&#x200B;**生产**&#x200B;工作区，并且您通常还使用&#x200B;**暂存**&#x200B;工作区进行测试。 想想像“环境”这样的工作区。 |
  | **凭据/服务** | 允许您的应用程序使用的权限。 为您创建的默认值足以启动。 |

* 创建项目的方法有两种：

  * **自动（推荐）：**&#x200B;命令`aio app init`在生成代码时为您创建项目和工作区。 本文介绍了此过程。
  * **手动：**&#x200B;您首先在Developer Console中自己创建项目，然后指向`aio`。 我们建议仅在您的组织要求集中创建项目时才执行此操作。

* 在决定使用哪个工作区时，请先开发并部署到&#x200B;**阶段**。 仅当用户在其Fusion配置文件（用户头像菜单>产品设置> Fusion配置文件>首选项>暂存扩展）中打开暂存测试时，Fusion才会加载暂存内部版本；否则，只显示已发布的生产扩展。 您还可以使用`aio app run`在本地预览，然后稍后升级到&#x200B;**生产**。

  有关提升至生产环境的详细信息，请参阅[发布您的扩展](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md)。


## 运行`aio app init`

1. 打开终端。
1. 在终端中，移至保留项目的文件夹。
1. 运行：

   ```sh
   aio app init my-fusion-extension --standalone-app
   ```

   * `my-fusion-extension`是文件夹/应用程序名称。 您可以选择此名称，但应使用小写字母、连字符且不能使用空格。
   * `--standalone-app`告知CLI创建&#x200B;**普通应用程序框架**，而不是要求您选择产品模板。 这是避免AEM（或任何其他）模板的关键。

1. 出现提示时，**选择您的组织**（如果您属于多个组织）。
1. 出现提示时，选择&#x200B;**创建新项目**&#x200B;并接受建议的名称，或选择现有的空项目。

   该命令会自动设置&#x200B;**暂存**&#x200B;和&#x200B;**生产**&#x200B;工作区。

   该命令还会将文件生成到`my-fusion-extension`文件夹并运行`npm install`。

1. 继续[确认项目创建](#confirm-project-creation)。

>[!NOTE]
>
> **如果您更喜欢交互式菜单：**&#x200B;请运行`aio app init my-fusion-extension` > （不带`--standalone-app`）。 当它询问&#x200B;**“您要搜索什么模板？”** 或显示模板核对清单，请勿选择AEM等产品模板。 选择选项以创建&#x200B;**独立应用程序** / **“所有扩展点→无”**。

## 检查项目创建

1. 在终端中，移到已创建的文件夹：

   ```sh
   cd my-fusion-extension
   ```

   您应该看到类似于下面的结构（省略了一些文件）：

   ```
   my-fusion-extension/
   |--- app.config.yaml   // main configuration (you will edit this)
   |---  package.json   //dependencies and scripts
   |---  src/    // your source code
   |---  web-src/  or  src/.../web-src/  // front-end files (HTML/JS)
   ```

   您最关心的两个文件是：

   * **`app.config.yaml`**：中央配置。 在此过程的后续步骤中，您将在此处添加一个`extensions:`部分，以将您的应用程序连接到Fusion扩展点。
   * **`package.json`**：列出您的应用程序使用的库。 您将在此处添加Adobe UI可扩展性来宾库。

1. 继续[添加所需的库](#add-required-libraries)。

>[!TIP]
>
> 如果生成的布局在CLI版本之间略有不同，请不要担心。 此过程可告知您确切要创建哪些文件以及要放置哪些文件，以便您可以匹配预期的结构，而不管起始点是什么。

## 添加所需的库

您的扩展需要两个库：

* **`@adobe/uix-guest`**：允许您的应用程序与Fusion（主机）通信。
* **`@adobe/react-spectrum`**： Adobe的React UI组件，因此您的屏幕与Adobe的外观相匹配。 （可选，但推荐；您可以改用纯HTML。）

要安装这些库，请执行以下操作：

1. 在终端中，运行：

   ```sh
   npm install @adobe/uix-guest @adobe/react-spectrum
   ```

1. （视情况而定）如果您生成的项目尚未包含React，请同时安装以下组件：

   ```sh
   npm install react react-dom react-router-dom
   ```

1. 继续[确认项目生成](#confirm-the-project-builds)。

## 确认项目生成

在更改任何内容之前，请确保生成空项目

1. 在终端中，运行：

   ```sh
   aio app build
   ```

   如果此操作完成且没有错误，则表示您的工具和项目已正确配置。 您已准备好将该项目连接到Fusion。

   >[!TIP]
   >
   > **如果生成失败，**&#x200B;最常见的原因是不支持的Node.js版本。 运行`node --version`并确保其为18或20。
   >
   >* 有关安装Node.js的信息，请参阅[设置工具](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)。
   >* 有关其他可能错误的信息，请参阅[疑难解答](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)。

1. 继续[为Fusion](#configure-the-project-for-fusion)配置项目。

## 为Fusion配置项目

设置自定义扩展的下一步是将通用项目连接到Workfront Fusion。

您将会：

1. [为扩展创建文件夹](#create-a-folder-for-your-extension)
1. 告知App Builder有关Fusion **扩展点** （在`app.config.yaml`中）的信息。
1. 描述扩展的片段（在`ext.config.yaml`中）。
1. **注册**&#x200B;您的小组件，以便Fusion知道其标题及其UI所在的位置。

我们全程使用`fusion/nav-organization/1`。 若要改为定位团队分区，请在所有位置交换`fusion/nav-team/1`。 要同时支持这两者，请为每个重复该模式。

## 为扩展创建文件夹

1. 创建文件，使项目如下所示：

   ```
   my-fusion-extension/
   |-- app.config.yaml
   |-- src/
          |-- fusion-nav-organization-1/          // one folder per extension point
             |-- ext.config.yaml
             |-- web-src/
                |-- src/
                   |-- components/
                      |-- App.js
                      |-- ExtensionRegistration.js
                      |-- DashboardWidget.js
                      |-- Constants.js
   ```

   我们建议在扩展点(`fusion-nav-organization-1`)之后命名文件夹。 确切名称由您决定，但必须与您在`app.config.yaml`中引用的名称匹配。

1. 继续[在`app.config.yaml`](#declare-the-extension-point-in-appconfigyaml)中声明扩展点。

## 在`app.config.yaml`中声明扩展点

1. 打开`app.config.yaml`并将其内容更新为：

   ```yaml
   extensions:
     fusion/nav-organization/1:
       $include: src/fusion-nav-organization-1/ext.config.yaml
   ```

   这些内容描述如下：

   * `extensions:`：此应用实现一个或多个扩展点。
   * `fusion/nav-organization/1`：您插入的Fusion插槽。 **名称必须完全匹配**，包括版本`1`。
   * `$include:`：这指向描述此扩展的内容的第二个配置文件（在下一步中创建）。 将其保留在单独的文件中可保持`app.config.yaml`整洁，并允许您稍后添加更多扩展点。

   >[!NOTE]
   >
   >如果要定位这两个扩展，请列出这两个扩展，每个扩展都有自己的文件夹：
   >
   > ```yaml
   > extensions:
   >     fusion/nav-organization/1:
   >         $include: src/fusion-nav-organization-1/ext.config.yaml
   >     fusion/nav-team/1:
   >         $include: src/fusion-nav-team-1/ext.config.yaml
   > ```

   1. 继续[在`ext.config.yaml`](#describe-the-extension-in-extconfigyaml)中描述扩展

## 描述`ext.config.yaml`中的扩展

1. 使用以下方式创建`src/fusion-nav-organization-1/ext.config.yaml`：

   ```yaml
   operations:
      view:
       - type: web
         impl: index.html
   web: web-src
   hooks:
     pre-app-build: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
      pre-app-run: node node_modules/@adobe/uix-guest/scripts/generate-metadata.js
   ```

   这些内容描述如下：

   * **`operations.view`**：声明您的扩展提供了从`index.html`提供的&#x200B;**视图** （可见UI）。 正因如此，扩展才会显示屏幕，而不是仅在后台运行。
   * **`web: web-src`**：保存前端文件的文件夹。 App Builder在此构建所有内容，并将其托管在Adobe的内容交付网络(CDN)上。
   * **`hooks`**：在生成/运行时自动运行的小型命令。 `generate-metadata.js`脚本随`@adobe/uix-guest`提供，并生成您的注册代码所需的`app-metadata.json`文件（请参阅步骤4）。 你不写这个脚本，你只是引用它。

   >[!NOTE]
   >
   > 如果您还需要服务器端逻辑，还可以添加无服务器`actions`（小型后端函数）。 操作是可选的，并且无需进行渲染UI，因此我们将其排除在外，以便本指南保持重点。 如果稍后添加它们，请在此处声明一个`actions:`文件夹，并在`app.config.yaml`中声明一个`runtimeManifest:`。 添加一个函数的最常见原因是调用Workfront/Fusion API而不点击浏览器CORS。
   > 有关调用API的信息，请参阅[调用Workfront和Fusion API](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md)。
1. 继续[设置稳定的扩展ID](#set-a-stable-extension-id)。

## 设置稳定的扩展ID

您的扩展需要两个框架共享的唯一ID。

有关与自定义扩展相关的框架的信息，请参阅UI扩展中包含的[框架](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md#frames-included-in-a-ui-extension)。

1. 创建`src/fusion-nav-organization-1/web-src/src/components/Constants.js`：

   ```js
   module.exports = {
     extensionId: 'my-fusion-extension'
   };
   ```

   在您的代码引用扩展ID的任何位置使用相同的值。
1. 继续[注册您的小组件](#register-your-widget)。


## 注册您的构件

“注册”是隐藏的背景框架告诉Fusion您的扩展所提供内容的方式。 您声明了一个`dashboard.getWidget()`方法，该方法返回您的小部件的标题及其可见UI的URL。

1. 创建`src/fusion-nav-organization-1/web-src/src/components/ExtensionRegistration.js`。
重要部分是`register(...)`调用：

   ```js
   import { register } from "@adobe/uix-guest";
   import metadata from "../../../../app-metadata.json";
   import { extensionId } from "./Constants";
   
   async function init() {
     await register({
       id: extensionId,
       metadata,
       methods: {
         dashboard: {
           getWidget() {
             return {
               id: extensionId,
               title: "My Fusion tool",        // shown on the Fusion nav button
               description: "What this tool does",
               url: "/index.html#/my-widget",  // route to your visible UI
               hideWidgetHeader: false          // false = Fusion shows the title
             };
           }
         }
       }
      });
   }
   
   init().catch(console.error);
   ```

   要点：

   * **`title`**&#x200B;是Fusion放置在导航按钮上的标签。 如果`hideWidgetHeader`是`false`，Fusion还会将标题显示为您UI上方的标题。
   * **`url`**&#x200B;是您在此同一应用程序中的&#x200B;*visible* UI的路由。 此处是您的前端路由器（在下一页设置）处理的哈希路由(`#/my-widget`)。 它必须解析为呈现屏幕的组件。
   * **`metadata`**&#x200B;来自`app-metadata.json`，`generate-metadata`挂接在生成时为您创建。 导入它，如下所示。
   * `dashboard.getWidget`方法名称是同意的合同Fusion调用，用于发现您的小组件。 保留`dashboard`命名空间和`getWidget`名称。

扩展的后端现已完成。 构建扩展UI的下一个步骤。

有关构建UI的说明，请参阅[构建自定义扩展UI](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md)。
