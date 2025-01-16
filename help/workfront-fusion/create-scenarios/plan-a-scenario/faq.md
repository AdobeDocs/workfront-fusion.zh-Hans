---
title: 方案规划常见问题解答
description: 当您开始在Workfront Fusion中创建场景时，本文中的信息可能会很有用。
author: Becky
feature: Workfront Fusion
exl-id: 6a1d672d-0bd7-4a3a-b96d-6d8b4c97522d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 1%

---

# 方案规划常见问题解答

当您开始在Workfront Fusion中创建场景时，本文中的信息可能会很有用。

## 什么是场景？

### 答案

场景定义了Adobe Workfront Fusion要执行的一系列步骤。 对于每个方案，您可以指定数据源、要使用的数据以及如何处理数据。 通过Fusion，您可以创建简单或复杂的场景，以便符合组织的用例。

有关方案的详细信息，请参阅[方案概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md)。

## 在一个场景中可以使用多少个模块？

### 答案

您可以在场景中使用任意数量的模块。 您可以将模块划分为路由，还可以指定哪些数据应通过每个路由。 也可以使用一个模块的输出作为另一个模块的输入。

虽然对场景中的模块数没有限制，但超过150个模块会影响场景性能。

有关模块的更多信息，请参阅[模块概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md)。

## [!DNL Workfront Fusion]可以使用文件吗？

### 答案

可以。Workfront Fusion可以接收、保存、转换、转换和加密文件。 Fusion还提供了范围广泛的内置功能，旨在使用户能够有效、创造性地处理文件中包含的数据。

有关在Fusion中使用文件的详细信息，请参阅[在模块之间映射文件](/help/workfront-fusion/create-scenarios/map-data/map-files.md)。

## 某些触发器允许场景立即运行。 “即时”是什么意思？

### 答案

场景可以根据您指定的计划间隔运行，例如每小时或每5分钟运行一次。 有一些特殊的触发器，称为即时触发器(webhook)，可以在它们从给定服务收到数据后立即启动场景。 Fusion会立即处理接收的数据，而不等待下一次计划运行。

有关轮询触发器和即时触发器之间差异的更多信息，请参阅文章模块概述中的[触发器模块](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules)。

## 什么是操作？

### 答案

操作是由模块执行的任何任务。 例如，每次触发器运行以及每次操作执行任务时都会执行操作。

某些Fusion计划基于您的组织使用的操作数。

有关操作的详细信息，请参阅[操作](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md)。

## 什么是数据传输？

### 答案

数据传输是指通过您的方案传输的数据量。 例如，从Workfront中检索100KB的图像，然后将该图像上传到文档存储提供商的场景。 此方案中使用的数据量为200KB。

## 什么是连接？

### 答案

连接是指您的[!DNL Workfront Fusion]帐户与要使用的第三方服务之间的链接。 可在编辑场景时创建连接。

有关详细信息，请参阅[连接概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md)。

## 什么是聚合？

### 答案

[!UICONTROL Aggregator]将数据合并到一个集合中。 例如，将文件压缩为zip存档并作为电子邮件附件发送。

有关详细信息，请参阅[[!UICONTROL Aggregator]模块](/help/workfront-fusion/references/modules/aggregator-module.md)。

## 如果我允许[!DNL Workfront Fusion]处理包含多个附件的电子邮件，会发生什么情况？

### 答案

如果您使用[!UICONTROL Email]模块[!UICONTROL Retrieve attachments]，则每个附件都将通过场景中的其余模块单独发送。 类似的模块也可用于同时接收多个文件的其他应用程序。
