---
title: 查看组织的分析仪表板
description: Fusion管理员可以查看显示组织执行度量的功能板。
author: Becky
feature: Workfront Fusion
exl-id: 8f80f86a-69e5-48a1-9812-87322a4959a6
TQID: 'https://experienceleague.adobe.com/tBZCbpImQxY42gOE8e04aQwCJC8EKgrDTIAt6Sw1KaU'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 45c755a2f6152b6e230864e4c840d0334705bd22
workflow-type: tm+mt
source-wordcount: '1307'
ht-degree: 2%
---
# 查看组织的分析仪表板

Fusion Insights仪表板允许您快速查看哪些场景运行得最多、发生延迟的位置以及工作人员池的运行效率。 这提供了执行卷、队列深度、池利用率和方案级性能的实时可见性。

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

## 分析仪表板组件

>[!NOTE]
>
>指标按工作线程池显示。 要查看其他工作线程池，请单击仪表板左上角附近的池字段，然后选择要查看其指标的池。

<!--

>[!NOTE]
>
>Organizations can request provisioning for one additional worker pool (for a total of 2).

-->

在Fusion Insights仪表板中，您可以看到以下量度。

* **失败的执行日志**
此表列出了组织内执行的每个失败或警告场景，因此您可以在不离开仪表板的情况下查找并排除问题运行。
* **组织操作**
此图表允许您查看组织中使用的操作数。 您可以选择特定的团队或方案，并查看上周、月或年中的操作。
* **按操作排名最前的方案**
此图表允许您查看哪些方案使用最多的操作。 您可以选择特定团队，或查看过去1天、1周或1个月的数据。

<!--

* **Executions waiting to be processed**
   This chart shows the number of executions waiting to be processed (also known as the execution backlog) at a given point in time. 

   A high number of executions waiting to be processed may affect performance in your Fusion instance. You will receive a notification if your execution backlog reaches 5000 executions. We recommend identifying responsible scenarios and modifying or disabling them. If the high execution backlog persists, the Fusion team will protect the performance of your Fusion instance by disabling the responsible scenarios.
* **Pool Utilization**
   This chart shows worker pool utilization over time. If this chart routinely shows worker pool utilization, you may want to assign some scenarios to another pool.

   If a pool is nearing 100% utilization, other resources that use the same pool may be delayed or disrupted. If this occurs, we recommend reassigning a high-usage scenario to another worker pool, or modifying existing scenarios to be less resource intensive.
* **Executions per scenario**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify which scenarios may be causing an execution backlog or high worker pool utilization. 
* **Duration of executions**
   This chart displays executions per scenario. Different colors represent different scenarios. When you hover over the chart, a window appears that shows which color is which scenario.

   You can use this chart to identify scenarios that are taking longer than usual, including those affected by issues with a connected app or service.

-->

## 查看Fusion分析功能板

1. 在Fusion中，单击左侧导航栏中的&#x200B;**分析**。

   “操控板”打开。

1. 要查看特定时间点的数据，请将光标悬停在仪表板上，并将光标调整为位于要查看的时间点上。

   所有图形上在该时间点上都会出现一条直线，并且每个图形上都会出现一个显示该时间数据的窗口。
1. 要在每个方案的执行次数图表或执行持续时间图表中查看特定方案的数据，请单击要查看其数据的方案的颜色条。 要返回到显示所有情景的视图，请再次单击图形。
1. 要转到“每个方案的执行数”图表或“执行持续时间”图表中显示的特定方案，请右键单击方案的颜色条形，然后选择&#x200B;**在新选项卡中打开方案**。
1. 若要展开图表，请单击该图表右上角的&#x200B;**展开**&#x200B;图标![展开图标](assets/expand-icon.png)。
1. 要更改仪表板的时间范围，请在仪表板右上角的时间范围字段中，选择一个新的时间范围。 可用的最长时间段为24小时，最短时间段为15分钟。
1. 要刷新图表，请单击仪表板右上角附近的刷新图标。
1. 要查看其他Worker池，请单击仪表板左上角附近的“池”字段，然后选择要查看的池。

## 自定义分析仪表板

您可以选择哪些构件将以何种顺序显示在分析仪表板上。

### 添加、删除或重新排序小组件

1. 在左侧导航中，单击&#x200B;**分析** ![分析图标](assets/insights-icon.png)。
1. 在“分析”标题中单击&#x200B;**[!UICONTROL 自定义]**。

   此时将打开侧面板。 它会将每个构件列为一个卡片，显示预览、构件名称和描述。

1. 要显示或隐藏构件，请单击其卡片，或单击卡片上的&#x200B;**[!UICONTROL 添加构件]**&#x200B;或&#x200B;**[!UICONTROL 删除构件]**&#x200B;按钮。

   显示的构件带有复选标记。
1. 要重新排序构件，请将构件卡拖动到面板中的新位置。

   虚线占位符和拖放栏显示卡片将登陆的位置。

您的选择将按浏览器保存。 在以后版本中添加的小组件会自动显示在面板中。

如果删除所有构件，则页面会显示“此页面上无构件”消息。

## 刷新分析仪表板

要重新加载每个小组件的数据，请单击&#x200B;**[!UICONTROL 自定义]**&#x200B;旁边的&#x200B;**[!UICONTROL 刷新]**。

* 每个构件都保留其筛选器。
* 在所有小组件完成加载之前，**[!UICONTROL 刷新]**&#x200B;按钮会显示挂起状态。
* 图表将上一个图表放在加载旋转器下，执行日志在数据重新加载时将其表放在旋转器下变暗。
* 如果刷新失败，则小组件将保留其最后的良好数据。

## 观看分析教程

首次打开“见解”仪表板时，欢迎对话框为您提供开始导览或跳过导览的选项。

导览以保存顺序突出显示每个构件，以及标题栏中的&#x200B;**[!UICONTROL 自定义]**&#x200B;按钮和面板、**[!UICONTROL 刷新]**&#x200B;按钮和&#x200B;**[!UICONTROL 重播导览]**&#x200B;按钮。

要随时重新开始导览，请单击标题栏中的导览信息图标![信息图标](assets/insights-tour-information.png)。

当您从场景中的链接打开分析仪表板时，导览不会开始。 有关详细信息，请参阅本文中[从方案](#open-the-insights-dashboard-from-a-scenario)中打开分析仪表板。

## 按ID搜索方案和团队

在&#x200B;**[!UICONTROL 组织操作]**&#x200B;和&#x200B;**[!UICONTROL 按操作排名最前的方案]**&#x200B;小组件中，**[!UICONTROL 方案]**&#x200B;和&#x200B;**[!UICONTROL 团队]**&#x200B;字段在ID和名称上匹配。 每个选项都会在名称下显示其ID，例如“ID 123”。

* 这些列表加载前500个场景和前200个团队。 如果您输入的ID不在已加载列表中，则Fusion会在短暂延迟后自动查找该ID。
* 如果清除方案，则自动为该方案填写的团队也会被清除。

>[!NOTE]
>
>执行日志中的场景过滤器在ID上不匹配。

## 从场景打开分析仪表板

您可以使用过滤到特定方案和团队的&#x200B;**[!UICONTROL 组织运营]**&#x200B;构件打开分析仪表板。

要从场景转到分析页面，请执行以下操作：

1. 打开方案详细信息页：

   1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡，然后单击要了解详细信息的方案。

      或

      如果您在方案编辑器中处理方案，请单击窗口左上角附近的左箭头![退出编辑箭头](assets/exit-editing-arrow.png)。
      1. 单击页面顶部附近的&#x200B;**报表**&#x200B;选项卡。

* **[!UICONTROL 组织操作]**&#x200B;构件将打开并筛选为该方案和团队，页面将滚动到该构件。
* 如果您已从页面中删除小组件，则会显示带有&#x200B;**[!UICONTROL 添加小组件]**&#x200B;按钮的警告。

## 使用深色模式

分析功能板及其构件会自动遵循深色模式设置。 更改设置后，页面会立即更新而不重新加载，并保持当前状态。 光模式保持不变。

## 性能构件访问

仅向具有以下权限之一的用户显示&#x200B;**[!UICONTROL 性能]**&#x200B;构件：

* 在活动组织中编辑组织
* 管理页面上的“组织”视图

对于其他用户，该构件在页面和&#x200B;**[!UICONTROL 自定义]**&#x200B;面板中处于隐藏状态。 如果稍后授予用户访问权限，则小组件将返回其保存位置。 直接打开分析URL不会绕过此检查。

## 在执行日志中过滤和分类执行

使用执行日志查找在您的组织中失败或返回警告的场景执行，并重新激活在重复失败后自动停用的任何场景。

1. 在执行日志中，按以下任一条件筛选执行：

   * [!UICONTROL 团队]
   * [!UICONTROL 场景]
   * [!UICONTROL 运行类型]
   * [!UICONTROL 日期范围]
   * [!UICONTROL 停用状态]
   * [!UICONTROL 错误消息]

   对于大多数过滤器，您可以选择仅匹配您选择的值，或者除这些值之外的所有其他值。

1. 单击执行可查看有关其错误的更多详细信息。
1. 要重新激活在重复失败后自动取消激活的一个或多个方案，请选择执行，然后单击&#x200B;**激活**。

   >[!NOTE]
   >
   >在重新激活场景之前，调查失败的原因，如凭据过期或连接器问题，以使场景不会立即再次失败。
