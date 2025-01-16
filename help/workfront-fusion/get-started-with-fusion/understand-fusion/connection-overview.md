---
title: 连接概述
description: 对于大多数应用，必须创建一个连接，通过该连接 [!DNL Adobe Workfront Fusion] 可以根据特定方案的设置与给定的第三方服务进行通信。
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 连接概述

对于大多数应用程序，Workfront Fusion都需要一个连接。  它使用此连接与给定的第三方服务进行通信。

例如，如果要创建一个从[!DNL Workfront]中检索信息的方案，则必须授予[!DNL Workfront Fusion]访问您的[!DNL Workfront]帐户的权限。

连接表示Fusion用于访问应用程序的授权和权限。 您可以为方案中使用的每个应用程序创建一个或多个连接，并可以在多个模块或方案中使用相同的连接。

大多数连接只用于单个应用程序。 例如，无法在[!UICONTROL Salesforce]模块中使用[!DNL Workfront]连接。 某些[!DNL Adobe]应用程序可以共享连接。 有关详细信息，请参阅[Fusion应用程序及其模块引用中列出的这些应用程序的文章：文章索引](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)。

连接由团队拥有。 团队的所有成员都可以访问团队的连接，而团队外部的用户无权访问团队的连接。

## 访问权限

对于每个连接，[!DNL Workfront Fusion]只需要成功完成给定方案所需的访问权限。 例如，如果您创建方案从[!DNL Workfront]下载文档，[!DNL Workfront Fusion]不要求创建新项目的权限。 之后，如果您发现需要创建项目，则可以更新连接或创建一个可以创建项目的新连接。

并非所有服务都允许您限制对特定任务的访问。 在这些情况下，[!DNL Workfront Fusion]必须要求完全访问权限。 有关如何限制[!DNL Workfront Fusion]访问注册到这些服务的帐户的详细信息，请参阅[Fusion应用程序及其模块引用中列出的应用程序特定文档：文章索引](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)。
