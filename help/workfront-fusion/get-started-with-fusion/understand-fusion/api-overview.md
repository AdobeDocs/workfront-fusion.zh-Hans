---
title: API 概述
description: 应用程序编程接口（API）是一种使应用程序与服务之间能够相互通信的方式。Fusion 通过 API 与您要连接的应用程序进行通信。每个应用程序都有各自独立的 API。
author: Becky
feature: Workfront Fusion
source-git-commit: 74308a6a43418296b29739f03683f23357d545bc
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 87%

---

# Fusion 中的 API 概述

<!--Add me to TOCs-->

应用程序编程接口（API）是一种使应用程序与服务之间能够相互通信的方式。Fusion 依靠 API 与您所连接的应用程序进行交互。

API 由应用程序的所有者创建并维护。例如，Workfront API 由 Adobe 的 Workfront 团队维护，而 Microsoft Graph API 则由 Microsoft 负责。API 的所有者决定 API 可提供哪些操作。

>[!NOTE]
>
>Workfront Fusion具有自己的API，您可以使用它在Fusion中自动执行操作。
>这些API正在逐步发布，目前标记为试验性的。 Fusion团队正在积极开发和扩展API，并且随着新功能的推出，将发布更新。
>有关Workfront Fusion API的文档，请参阅[Workfront Fusion API](https://developer.adobe.com/workfront-fusion-apis/)。

## 注意事项

由于 API 由其所有者而非 Fusion 定义，因此需要注意以下重要事项：

* **只要某个应用程序或服务提供公共 API，您就可以使用 Fusion 将其连接起来**，无论 Fusion 是否为其提供专用连接器。您可以使用 Fusion 的通用连接器将这些应用程序或服务纳入您的场景中。

  有关通用连接器的列表，请参阅[通用连接器](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)。

* **应用程序所有者对其 API 所做的更改可能会影响 Fusion 的功能。**&#x200B;如果更改幅度较大，Fusion 可能需要更新模块或连接类型；在极端情况下，甚至可能需要为该应用程序创建新的连接器。

  有关这类极端情况（称为“重大变更”）的详细信息，请参阅本文中的[重大变更](#breaking-changes)。


## 重大变更

导致重大变更的常见原因是弃用，即 API 所有者停止提供 API 的部分或全部功能。发生这种情况时，Fusion 团队会尽力使 Fusion 的功能尽快与应用程序 API 的新版本保持一致。这通常会通过新增模块、更新连接类型或创建新的连接器来实现。

由于您的 Fusion 场景基于您的特定数据进行配置，因此您可能需要更新这些场景。

* 如果变更与身份验证或授权相关，您可能需要更新该应用程序的连接设置。
* 如果变更涉及 API 中的某个具体操作（端点），您可能需要将与该操作相关的模块更新为新版本。
* 如果 Fusion 所使用的整个 API 版本已弃用，您可能需要将该连接器的所有模块更新到新的连接器版本。

在许多情况下，您可以在无需重新配置模块的前提下，将其升级到新版本。

有关升级模块的详细信息和操作步骤，请参阅[将模块升级到新版本](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md)。
