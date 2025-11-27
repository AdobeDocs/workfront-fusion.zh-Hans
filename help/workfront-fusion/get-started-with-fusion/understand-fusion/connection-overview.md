---
title: 连接概述
description: 对于大多数应用程序，您都需要创建一个连接，从而使 Adobe Workfront Fusion 能够根据特定场景的设置，与相关的第三方服务进行通信。
author: Becky
feature: Workfront Fusion
exl-id: 01132df7-4cc0-4ff3-b4d7-607a06558735
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: ht
source-wordcount: '315'
ht-degree: 100%

---

# 连接概述

Workfront Fusion 在大多数应用程序中都需要一个连接。Fusion 通过该连接与指定的第三方服务进行通信。

例如，如果您想创建一个从 Workfront 获取信息的场景，则必须授予 Workfront Fusion 访问您的 Workfront 帐户的权限。

连接表示 Fusion 用于访问应用程序的授权和权限。您可以为场景中使用的每个应用程序创建一个或多个连接，并且可以在多个模块或场景中重复使用同一个连接。

大多数连接仅用于一个应用程序。例如，Workfront 连接不能在 [!UICONTROL Salesforce] 模块中使用。 某些 [!DNL Adobe] 应用程序可以共享连接。有关详细信息，请参阅这些应用程序的文章，文章列表位于 [Fusion 应用程序及其模块参考：文章索引](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)。

连接由团队所有。 团队中的所有成员都可以访问团队的连接，团队外的用户则无法访问这些连接。

## 访问权限

对于每个连接，Workfront Fusion 只需要完成特定场景所需的最低访问权限。例如，如果您创建一个从 Workfront 下载文档的场景，Workfront Fusion 不会请求创建新项目的权限。如果之后您发现需要创建项目，可以更新现有连接，或创建一个具有项目创建权限的新连接。

并非所有服务都允许您将访问权限限制在特定任务范围内。在这种情况下，Workfront Fusion 必须要求具有完整访问权限。要了解如何限制 Workfront Fusion 对您在这些服务中注册的帐户的访问权限，请参阅列于 [Fusion 应用程序及其模块参考：文章索引](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)中的各应用程序专用文档。
