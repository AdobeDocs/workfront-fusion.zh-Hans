---
title: 查看组织的绩效仪表板
description: Fusion administrators can view a dashboard that shows execution metrics for an organization.
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
source-git-commit: 6762806f17a0fc55531b647a84901b8ca572a997
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 7%

---

# 查看组织的绩效仪表板

The Fusion Performance Dashboard allows you to quickly see which scenarios are running the most, where delays are occurring, and how effectively your worker pools are operating. This provides real-time visibility into execution volumes, queue depth, pool utilization, and scenario-level performance.

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

## Performance dashboard components

>[!NOTE]
>
>Metrics are shown by worker pool. To view a different worker pool, click the Pool field near the upper-left corner of the dashboard, then select the pool you want to view metrics for.

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

In the Fusion performance dashboard, you can see the following metrics.

* **Executions waiting to be processed**
This chart shows the number of executions waiting to be processed (also known as the execution backlog) at a given point in time.

  A high number of executions waiting to be processed may affect performance in your Fusion instance. You will receive a notification if your execution backlog reaches 5000 executions. We recommend identifying responsible scenarios and modifying or disabling them. If the high execution backlog persists, the Fusion team will protect the performance of your Fusion instance by disabling the responsible scenarios.
* **Pool Utilization**
This chart shows worker pool utilization over time. If this chart routinely shows worker pool utilization, you may want to assign some scenarios to another pool.

  If a pool is nearing 100% utilization, other resources that use the same pool may be delayed or disrupted. If this occurs, we recommend reassigning a high-usage scenario to another worker pool, or modifying existing scenarios to be less resource intensive.
* **Executions per scenario**
This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

  您可以使用此图表来确定哪些方案可能会导致执行积压或工作线程池利用率高。
* **执行持续时间**
此图表显示每个方案的执行次数。 不同的颜色代表不同的场景。 当您将鼠标悬停在图表上时，会出现一个窗口，显示哪种颜色是哪种方案。

  您可以使用此图表识别耗时超过正常时间的方案，包括受连接的应用程序或服务问题影响的方案。

## 查看Fusion性能仪表板

1. 在Fusion中，单击左侧导航栏中的&#x200B;**性能**。

   “操控板”打开。

1. 要查看特定时间点的数据，请将光标悬停在仪表板上，并将光标调整为位于要查看的时间点上。

   所有图形上在该时间点上都会出现一条直线，并且每个图形上都会出现一个显示该时间数据的窗口。
1. 要在每个方案的执行次数图表或执行持续时间图表中查看特定方案的数据，请单击要查看其数据的方案的颜色条。 要返回到显示所有情景的视图，请再次单击图形。
1. 要转到“每个方案的执行数”图表或“执行持续时间”图表中显示的特定方案，请右键单击方案的颜色条形，然后选择&#x200B;**在新选项卡中打开方案**。
1. 若要展开图表，请单击该图表右上角的&#x200B;**展开**&#x200B;图标![展开图标](assets/expand-icon.png)。
1. 要更改仪表板的时间范围，请在仪表板右上角的时间范围字段中，选择一个新的时间范围。 可用的最长时间段为24小时，最短时间段为15分钟。
1. 要刷新图表，请单击仪表板右上角附近的刷新图标。
1. 要查看其他Worker池，请单击仪表板左上角附近的“池”字段，然后选择要查看的池。
