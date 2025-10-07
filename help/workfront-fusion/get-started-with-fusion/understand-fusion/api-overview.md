---
title: API概述
description: 应用程序编程接口(API)是应用程序和服务相互通信的一种方式。 Fusion使用API与您连接的应用程序进行通信。 每个应用程序都有一个单独的API。
author: Becky
feature: Workfront Fusion
source-git-commit: 1ee32ad1faa8c105142f85e83f1b522548fc7f93
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Fusion中的API概述

<!--Add me to TOCs-->

应用程序编程接口(API)是应用程序和服务相互通信的一种方式。 Fusion使用API与您连接的应用程序进行通信。

API由应用程序的所有者创建并控制。 例如，Workfront API归Adobe的Workfront团队所有，而Microsoft Graph API归Microsoft所有。 API的所有者定义可通过API执行的操作。

## 注意事项

API由其所有者而非Fusion定义这一事实引出了一些重要的注意事项：

* **您可以使用Fusion连接到任何具有公共API的应用或服务**，无论Fusion是否提供到该应用或服务的专用连接器。 您可以使用Fusion的通用连接器将这些应用程序或服务引入您的方案中。

  有关通用连接器的列表，请参阅[通用连接器](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)

* **所有者对应用程序API所做的更改可能会影响Fusion功能。**&#x200B;如果更改足够严重，Fusion可能需要更新模块或连接类型，或者在极端情况下可能为应用程序创建新的连接器。

  有关这些称为“重大更改”的极端情况的详细信息，请参阅本文中的[重大更改](#breaking-changes)。


## 重大更改

在API所有者从可用性中删除部分或全部API时，发生重大更改的常见原因是弃用。 发生这种情况时，Fusion团队会尽一切努力快速将Fusion功能与应用程序的API的新版本重新调整。 这通常采用新模块、连接类型或连接器的形式。

由于您的Fusion方案是使用特定数据配置的，因此您可能需要更新方案。

* 如果更改与身份验证或授权相关，则可能需要更新该应用程序的连接。
* 如果更改与API中的特定操作（端点）相关，您可能需要将与该操作相关的模块更新为模块的新版本。
* 如果弃用Fusion使用的整个API版本，则可能需要将该连接器的所有模块更新为新版本的连接器。

在许多情况下，您可以升级到模块的新版本，而无需重新配置该模块。

有关升级模块的信息和说明，请参阅[将模块升级到新版本](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md)。
