---
title: 查看组织的绩效仪表板
description: Fusion管理员可以查看显示组织执行度量的功能板。
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: b4c9cd075cc2bb7aa3d5c568bb91fb8ce5c6f31e
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 7%

---

# 查看组织的绩效仪表板

Fusion Performance Dashboard允许您快速查看哪些场景运行得最多、发生延迟以及工作人员池的运行效率。 这提供了执行卷、队列深度、池利用率和方案级性能的实时可见性。

## 访问权限要求

+++ 展开可查看本文所述功能的访问权限要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 包</td> 
   <td> <p>Adobe Workfront工作流程Ultimate和Adobe Workfront自动化与集成Ultimate</p><p>Workfront Ultimate</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 许可证</td> 
   <td> <p>标准</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">访问级别配置</td> 
   <td> 
     <p>您必须是组织的Workfront Fusion管理员。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 性能仪表板组件

>[!NOTE]
>
>指标按工作线程池显示。 要查看其他工作线程池，请单击仪表板左上角附近的池字段，然后选择要查看其指标的池。

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

在Fusion性能仪表板中，您可以看到以下量度。

* **正在等待处理的执行**
此图表显示在给定时间点等待处理的执行（也称为执行积压）的数量。

  等待处理的大量执行可能会影响Fusion实例中的性能。 如果您的执行积压达到5000次执行，您将收到通知。 我们建议确定负责任的方案，并修改或禁用它们。 如果高执行积压持续存在，Fusion团队将通过禁用负责的场景来保护Fusion实例的性能。
* **池利用率**
此图表显示一段时间内的工作线程池利用率。 如果此图表定期显示工作线程池的利用率，则您可能希望将某些方案分配给另一个池。

  如果池的利用率接近100%，则使用同一池的其他资源可能会延迟或中断。 如果出现这种情况，我们建议将高使用率方案重新分配给另一个工作线程池，或者修改现有方案以降低资源密集程度。
* 每个场景&#x200B;**执行次数**
此图表显示每个方案的执行次数。 不同的颜色代表不同的场景。 当您将鼠标悬停在图表上时，会出现一个窗口，显示哪种颜色是哪种方案。

  您可以使用此图表来确定哪些方案可能会导致执行积压或工作线程池利用率高。
* **执行持续时间**
此图表显示每个方案的执行次数。 不同的颜色代表不同的场景。 当您将鼠标悬停在图表上时，会出现一个窗口，显示哪种颜色是哪种方案。

  您可以使用此图表识别耗时超过正常时间的方案，包括受连接的应用程序或服务问题影响的方案。

## 查看Fusion性能仪表板

1. 在Fusion中，单击左侧导航中的性能。

   “操控板”打开。

1. 要查看特定时间点的数据，请将光标悬停在仪表板上，并将光标调整为位于要查看的时间点上。

   所有图形上在该时间点上都会出现一条直线，并且每个图形上都会出现一个显示该时间数据的窗口。
1. 要在每个方案的执行次数图表或执行持续时间图表中查看特定方案的数据，请单击要查看其数据的方案的颜色条。 要返回到显示所有情景的视图，请再次单击图形。
1. 要转到“每个方案的执行数”图表或“执行持续时间”图表中显示的特定方案，请右键单击方案的颜色条形，然后选择&#x200B;**在新选项卡中打开方案**。
1. 若要展开图表，请单击该图表右上角的&#x200B;**展开**&#x200B;图标![展开图标](assets/expand-icon.png)。
1. 要更改仪表板的时间范围，请在仪表板右上角的时间范围字段中，选择一个新的时间范围。 可用的最长时间段为24小时，最短时间段为15分钟。
1. 要刷新图表，请单击仪表板右上角附近的刷新图标。
1. 要查看其他Worker池，请单击仪表板左上角附近的“池”字段，然后选择要查看的池。



