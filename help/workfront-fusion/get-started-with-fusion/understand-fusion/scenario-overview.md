---
title: 场景概述
description: 使用 Adobe Workfront Fusion 需要在拥有 Adobe Workfront 许可的基础上另行购买 Workfront Fusion 许可。
author: Becky
feature: Workfront Fusion
exl-id: de81ad4c-27e5-4b6c-acf0-f01a8c85922e
source-git-commit: 34dad92019ca855f40698d3f3795788698c1cece
workflow-type: ht
source-wordcount: '704'
ht-degree: 100%

---

# 场景概述

Adobe Workfront Fusion 的作用是自动化您的业务流程，使用户无需将大量时间花在日常重复性任务上。它通过连接应用程序和服务内部或之间的操作，构建可自动传输并转换数据的场景。您创建的场景会监控某个应用程序或服务中的数据，并对这些数据进行处理，以生成您所需的结果。

场景由一系列模块组成，这些模块会指示数据在应用程序内部如何转换，或在应用程序与网络服务之间如何传输。

## 场景元素概述

场景由多个不同的元素组成。了解这些元素的术语有助于更轻松地使用相关文档。

* [场景](#scenario)
* [触发器](#trigger)
* [模块](#module)
* [路由](#route)
* [场景区段](#scenario-segment)
* [连接器](#connector)

### 场景

**场景**&#x200B;是一组由用户创建的自动化步骤，用于移动和处理数据。“场景”一词指的是整个相互连接的步骤集合。

![场景](assets/entire-scenario-scenario.png)

### 触发器

场景始于一个&#x200B;**触发器**。 触发器会监控新增或更新的数据，并在满足模块中配置的特定条件时启动场景。触发器可以配置为按计划（轮询）启动场景，或在数据发生更改时即时启动。

![触发器](assets/scenario-trigger.png)

### 模块

在触发器之后会执行一系列&#x200B;**模块**。模块代表场景中的单一步骤，用于执行特定操作。通过配置并串联模块，即可构建场景。

![模块](assets/scenario-module.png)

### 路由

一个场景可以划分为多个&#x200B;**路由**。 路由是场景中的一个部分，在处理特定数据捆绑包时可能会被使用，也可能不会。路由通过路由器模块和筛选条件进行配置。

![路由](assets/scenario-route.png)

### 场景区段

场景区段是场景中的一个部分，由一系列连续的模块组成，这些模块均连接到同一应用程序。场景区段通常表示应用程序中的一段短工作流程。

![场景区段](assets/scenario-segment.png)

### 连接器

连接器是一组为特定应用程序提供的模块集合。Workfront Fusion 提供适用于多种常用工作应用的连接器，例如 Workfront、Salesforce 和 Jira，也提供可用于任意 Web 服务的通用连接器。

![连接器](assets/scenario-connectors.png)

## 示例

展开以下章节即可查看示例场景及其说明。

+++**在 Adobe Workfront 中自动化流程**

Workfront Fusion 允许您在 Workfront 中自动化简单或复杂的工作流，从而节省时间，并确保流程一致执行。

在此示例中，当 Workfront 中任务或问题的指定字段发生变化时，即会触发场景。场景触发后，会获取相关项目中的信息，并为项目中被分配至特定角色的人员生成定制更新。

![模板示例](assets/fusion-template-example.png)

+++

+++**将 Workfront 连接到其他应用程序或 Web 服务**

>[!NOTE]
>
>如果您的组织仍在使用旧版授权模式，则必须拥有 Workfront Fusion for Work Automation and Integration 许可证，才能连接其他应用程序。

Workfront Fusion 可以连接到其他应用程序和 Web 服务。您可以访问、导入、处理或导出来自其他应用程序的数据，并将这些应用程序与 Workfront 或彼此进行集成。

许多应用程序都提供专用的 Workfront Fusion 连接器。如果要访问的应用程序没有专用连接器，您可以使用 Workfront Fusion 的 HTTP 或 SOAP 模块，通过其 API 连接到该应用程序。

在此示例中，当用户被添加到一份 [!DNL Excel] 电子表格时会触发场景。 场景会检查该用户是否已存在于 Workfront 中。如果不存在，场景会在 Workfront 中创建该用户，并将其 Workfront 用户 ID 回写到电子表格中。

![集成示例](assets/fusion-integration-example.png)

有关专用连接器的完整列表，请参阅 [Fusion 应用程序及其模块参考：文章索引](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)。


>[!IMPORTANT]
>
>Adobe Workfront Fusion 几乎可以连接到任何 Web 服务。如果您要使用的应用程序没有专用的 Workfront Fusion 连接器，您可以使用通用连接器连接该应用程序或服务。
>
>有关通用连接器的列表，请参阅[通用连接器](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)

+++

## 参考

* 有关 Workfront Fusion 中使用的术语表，请参阅 [Adobe Workfront Fusion 术语表](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md)。
* 若要开始构建练习场景，请参阅[创建基础场景](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)。
* 有关创建和管理场景的详细信息，请参阅以下内容中的文章：
   * [创建场景](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)
   * [管理场景](/help/workfront-fusion/manage-scenarios/manage-scenarios-toc.md)
