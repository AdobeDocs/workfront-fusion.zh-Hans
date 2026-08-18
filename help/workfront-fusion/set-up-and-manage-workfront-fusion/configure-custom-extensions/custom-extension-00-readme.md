---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 自定义UI扩展：文章索引
description: Workfront Fusion中的自定义扩展
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
source-wordcount: 603
ht-degree: 3%

---


# 自定义UI扩展：文章索引

Fusion可以在界面中显示您自己的Web UI。 您可以构建一个名为扩展的小型Web应用程序，并将其发布到Adobe，然后在Fusion导航中显示为按钮。 当用户单击它时，您的UI将加载到Fusion的主区域，并自动接收有关登录者、用户所在的组织和团队等的信息。

Fusion文档的此部分将指导您完成整个过程，而不需要假设您之前已体验Adobe App Builder或前端框架。 它还包含必要的代码以及代码解释。

## 何时使用本指南

如果要向Fusion添加自定义屏幕或工具，请使用此指南。 您无需成为开发人员专家。 您确实需要习惯将命令复制到终端并编辑一些文本文件。

要创建自定义UI扩展，您需要Adobe ID和对Adobe组织的访问权限（与登录Fusion时所用的访问权限相同）。

## 您将构建的内容

在本指南结束时，您将拥有：

1. 免费的Adobe **App Builder**&#x200B;项目。 这是扩展所在的位置。
1. 一个小型Web应用程序，可呈现您的自定义UI。
1. 该Web应用程序连接到Fusion的某个扩展点，因此显示在Fusion导航中。
1. 您的UI会从Fusion中读取实时上下文（例如当前用户、组织和团队），并在用户切换组织或团队时做出反应。
1. 已发布的扩展，以便组织中的其他用户能够查看它。

<!--

## How it works, in one picture

```
  Fusion (the "Host")                         Your extension (the "Guest")
  ───────────────────────────────                         ──────────────────────────────
  Left navigation                             A web app hosted by Adobe
   └── Organization                            (App Builder + UI Extensibility)
       └── [Your extension button]  ── click ──▶ Fusion opens your UI in an iframe
                                              and sends it live context:
                                               * signed-in user
                                               * active organization
                                               * active team
                                               * Adobe IMS identifiers
```

Fusion is the **host**. Your extension is the **guest**. They run in separate browser frames and talk to each other through Adobe's **UI Extensibility SDK** (no custom networking required on your side).

-->

## 目录

首次按顺序阅读页面。 以后你可以直接跳到你需要的那边。

| # | 页面 | 涵盖的内容 |
| --- | ------ | ---------------- |
| 1 | [概述和关键概念](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-01-overview.md) | 词汇表、架构以及每个Fusion扩展点的用途。 |
| 2 | [设置您的工具和Adobe帐户](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md) | Node.js、Adobe I/O CLI、登录，并在Adobe Developer Console中创建项目。 |
| 3 | [创建项目并针对Fusion进行配置](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-03-04-create-project-configure-fusion.md) | 使用`aio`命令行生成通用App Builder项目（不是产品特定的模板）。 然后，将您的项目指向Fusion扩展点并注册您的小组件。 |
| 5 | [构建UI](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md) | 渲染您的自定义屏幕并与Fusion完成连接（“握手”）。 |
| 6 | [Fusion上下文引用](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md) | 每个字段Fusion都会发送您、其含义以及如何对更改做出反应。 |
| 7 | [发布扩展](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md) | 生成、部署您的扩展并使之在Fusion中可见。 |
| 8 | [故障排除](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md) | 修复了最常见的错误。 |
| 9 | [演示演练](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-09-demo-walkthrough.md) | 一个线性、复制并粘贴脚本：通用Experience Cloud Shell模板中的基架，→重新定位到Fusion →，然后部署到暂存→在Fusion中运行。 最适合实时演示。 |
| 10 | [调用Workfront和Fusion API](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md) | 使用运行时操作代理，从扩展调用后端API而不点击浏览器CORS。 涵盖`require-adobe-auth`、Fusion v3标头以及一个有效示例。 |

## 可用性说明

Fusion当前公开以下扩展点：

* `fusion/nav-organization/1` — 显示在&#x200B;**组织**&#x200B;部分下。
* `fusion/nav-team/1` — 显示在&#x200B;**团队**&#x200B;部分下。

在您可以发布这些扩展点中的某个扩展点之前，必须为您的Adobe组织载入扩展点。 如果发布步骤失败，指出扩展点“不存在”，请参阅[疑难解答](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)。

## Adobe官方文档

本指南特定于Fusion。 对于基础平台，规范引用包括：

* [UI可扩展性概述](https://developer.adobe.com/uix/docs/)
* [UI扩展开发流程](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [UI扩展管理（发布/批准/撤销）](https://developer.adobe.com/uix/docs/guides/publication/)
* [Adobe App Builder快速入门](https://developer.adobe.com/app-builder/docs/getting_started/)
