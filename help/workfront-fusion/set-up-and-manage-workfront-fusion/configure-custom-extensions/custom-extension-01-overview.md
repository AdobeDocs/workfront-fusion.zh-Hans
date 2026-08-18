---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: UI可扩展性概述
description: Workfront Fusion中的自定义扩展
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 835
ht-degree: 0%

---

# UI可扩展性概述

UI可扩展性允许您将自定义逻辑和UI（用户界面）引入Adobe Workfront Fusion。 通过使用Adobe App Builder，您可以修改组织的Workfront Fusion体验以更好地满足组织的需求，同时仍可依靠Fusion的核心功能。

本文概述了UI的可扩展性以及您的自定义扩展与Workfront Fusion的通信方式。

## 扩展结构

* [主持人和嘉宾](#hosts-and-guests)
* [下面的技术](#the-technology-underneath)

### 主持人和嘉宾

Fusion可以显示非Workfront Fusion团队创建的UI。 为确保这些UI更改不会影响Fusion的核心功能，UI在其自己的独立浏览器框架(`<iframe>`)中运行，与Fusion的代码完全不同。

* **主机**： *包含*&#x200B;扩展的应用程序。 此处是&#x200B;**Fusion**。 主机可决定扩展可以出现的位置以及它将与它们共享的数据。
* **来宾**： *您的*&#x200B;扩展。 它是主机加载到iframe中的小型Web应用程序。

创建UI扩展时，不会修改Fusion。 您可以生成并发布访客，在发布访客后，Fusion可以使用该访客。

### 下面的技术

您的来宾采用了两种Adobe技术：

* **Adobe App Builder**：适用于小型Web应用和无服务器操作的免费托管和工具平台。 您的扩展是一个App Builder应用程序。 App Builder为您提供了一个托管UI（在Adobe的`*.adobeio-static.net`内容交付网络上）的位置，以及一个名为`aio`的命令行工具来创建、构建和发布它。
* **Adobe UI可扩展性SDK (UIX)**：允许主持人和来宾通话的库。 您将使用您这边的一个包`@adobe/uix-guest`。 Fusion在其一侧使用匹配的`@adobe/uix-host`包。

<!--

```
   ┌────────── Browser ─────────────────────────────┐
   │                                                                   │
   │   Fusion (Host)                      Your extension (Guest)       │
   │   ────────────                       ─────────────────────        │
   │   @adobe/uix-host   ◀── messages ──▶  @adobe/uix-guest            │
   │        │                                    │                     │
   │   renders an iframe ───────────────▶  your React/HTML UI          │
   │                                                                   │
   └───────────────────────────────────────────────────────────────────┘

   Your UI files are hosted by Adobe App Builder at
   https://<your-app>.adobeio-static.net
```

-->

## 扩展点

扩展点是主机中允许出现来宾的名为“slot”。 Fusion定义其版块，您可以选择访客使用哪个版块。

扩展点名称由三部分组成： `service/name/version`。

Fusion提供了以下扩展点：

| 扩展点 | UI在Fusion中的显示位置 | 何时使用 |
| --- | --- | ---- |
| `fusion/nav-organization/1` | 在左侧导航的&#x200B;**组织**&#x200B;部分下。 | 你的工具关系到整个组织。 |
| `fusion/nav-team/1` | 在左侧导航的&#x200B;**团队**&#x200B;部分下（在选择团队时显示）。 | 您的工具与特定团队有关。 |

* `fusion`是&#x200B;**服务** （产品， Fusion）。
* `nav-organization` / `nav-team`是&#x200B;**名称**（特定插槽）。
* `1`是&#x200B;**版本**。

一个扩展可以实施一个扩展点，也可以同时实施两个扩展点。 大多数扩展只使用一点。

Fusion会根据选择的扩展点向匹配导航部分添加一个带有扩展标题的按钮。 单击该链接会在Fusion的主内容区域中打开一个专用页面，并在该处加载您的UI。

## UI扩展中包含的框架

>[!IMPORTANT]
>
>本节将讨论可能导致混淆的UI扩展的一个方面。 我们建议仔细阅读。

当Fusion加载来宾时，扩展将在&#x200B;**两个**&#x200B;帧中运行：

1. **注册帧（不可见）。** 首先在后台运行。 注册框架可告知Fusion您的扩展提供了哪些功能。 例如，它可能表示它具有一个仪表板小组件，并发送该小组件的标题及其UI的URL。 注册帧通过调用`register(...)`来执行此操作。 它不会呈现可见的UI。
1. **UI框架（可见）。** 这是Fusion向用户显示的页面。 它必须通过调用`attach(...)`向主机宣布自身。 如果它从未调用`attach`，则Fusion会等待并最终因错误而超时。

>[!BEGINSHADEBOX]

此示例显示了用户单击扩展按钮时的流程。

1. 已单击按钮。
1. Fusion将加载REGISTRATION框架（隐藏）。

   ```
   register({ methods: { dashboard: { getWidget() {...} } } })
   ```

   `getWidget()`返回您可见UI的URL
1. Fusion将在该URL处加载您的UI框架（可见）。

   ```
   attach({ id }) 
   ```

   此项为必需，否则Fusion将超时
1. Fusion发送上下文，您的UI呈现。

>[!ENDSHADEBOX]

构建UI时，将编写两个框架。 重要的是要记住，可见页面&#x200B;**必须**&#x200B;调用`attach`。

有关生成UI的详细信息，请参阅[生成自定义扩展UI](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md)。

## Fusion中的上下文

附加扩展后，Fusion将与您的来宾共享`context`对象。 主库文件包含：

* **用户**：登录用户的Fusion配置文件和Adobe IMS用户ID。
* **组织**：活动组织的完整Fusion组织记录和Adobe IMS组织ID。
* **团队**：活动团队（如果适用）。
* **Adobe IMS访问令牌**：如有必要，这将代表用户调用Adobe或Fusion API。

Fusion还会推送更新。 例如，如果用户在UI打开时切换组织或团队，则Fusion会发送新上下文，以便UI能够立即做出反应。

有关上下文字段的完整列表，请参阅[Fusion上下文引用](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)。

## 创建UI扩展

要创建UI扩展，请执行以下步骤：

1. [安装工具并创建Adobe项目](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)。
1. [生成一个空白的App Builder项目，将其指向Fusion扩展点并注册您的小组件](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md)。
1. [生成UI并连接到Fusion](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md)。
1. [使用Fusion发送的上下文](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)。
1. [发布，以便Fusion能够找到它](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md)。
1. （可选） [调用不具有CORS的实际数据的Workfront/Fusion API](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md)。

要开始此过程，请转到[设置您的工具和Adobe帐户](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)。


