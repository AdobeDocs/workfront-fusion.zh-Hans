---
title: 解释人工智能的场景错误
description: 当场景运行失败时，您可以单击错误旁边的解释以获取有关错误以及如何修复的简短简短语言描述。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 565302f1d994819607051014d18779ccfb2645cb
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 15%
---
# 解释人工智能的场景错误

当场景运行失败时，AI可以为您提供简短、简单的语言描述，说明哪里出了错误以及如何修复错误。 说明显示在原始错误旁边，因此您可以同时阅读这两个错误。

您可以在Workfront Fusion的以下区域中解释错误：

* 方案设计器中的模块错误详细信息
* 方案执行历史记录中的运行详细信息
* 分析页面上的[!UICONTROL 失败的执行日志]表

>[!NOTE]
>
>**[!UICONTROL Explain]**&#x200B;按钮仅在新的方案设计器中可用。 在旧版场景设计器中不可用。
>
>您的组织必须具有AI许可证才能使用此功能。

## 访问权限要求

+++ 展开可查看本文所述功能的访问权限要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 包</td> 
   <td> <p>任意 Adobe Workfront Workflow 包以及任意 Adobe Workfront 自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime 和 Select 包，且需额外购买 Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 许可证</td> 
   <td> <p>标准</p><p>工作版或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 解释模块输出详细信息中的错误

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要说明错误的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 按计划运行方案，或单击&#x200B;**运行一次**。
1. 当某个模块出现故障时，请打开该模块的错误详细信息。
1. 单击&#x200B;**[!UICONTROL 说明]**。

   按钮在错误下方。

   ![模块输出中有解释错误](assets/explain-in-module-output.png)

说明显示在错误下方。

>[!NOTE]
>
> * 当AI生成说明时，会出现加载状态。
> * 如果无法生成说明，请单击&#x200B;**[!UICONTROL 重试]**。
> * 如果贵组织达到其AI使用限制，则会显示使用限制消息，而不是说明。

## 解释场景执行历史记录中的错误

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡，然后单击方案。
1. 单击方案名称附近的&#x200B;**[!UICONTROL 历史记录]**。
1. 单击要查看的失败运行。

   运行详细信息中的每个错误都有一个&#x200B;**[!UICONTROL Explain]**&#x200B;按钮。

1. 在要说明的错误下单击&#x200B;**[!UICONTROL 说明]**。

   如果多个模块在运行时失败，您可以自行解释每个错误。

   ![在执行历史记录中说明](assets/explain-in-execution-details.png)

有关查看运行的详细信息，请参阅[查看方案的执行历史记录](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md)和[查看特定方案的执行](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md)。

>[!NOTE]
>
> * 当AI生成说明时，会出现加载状态。
> * 如果无法生成说明，请单击&#x200B;**[!UICONTROL 重试]**。
> * 如果贵组织达到其AI使用限制，则会显示使用限制消息，而不是说明。

## 解释分析页面上的错误

1. 在Fusion中，单击左侧导航栏中的&#x200B;**[!UICONTROL 分析]**。
1. 在[!UICONTROL 失败的执行]表中，将鼠标悬停在要查看的失败行上。

   出现&#x200B;**[!UICONTROL 解释]**&#x200B;按钮。

1. 单击&#x200B;**[!UICONTROL 说明]**。

   ![在见解页面中说明](assets/explain-failed-execution-log.png)

   此时将打开一个弹出窗口，其中显示错误和AI说明。

有关“分析”页面的详细信息，请参阅[查看组织的分析仪表板](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/view-insights-dashboard.md)。

>[!NOTE]
>
> * 当AI生成说明时，会出现加载状态。
> * 如果无法生成说明，请单击&#x200B;**[!UICONTROL 重试]**。
> * 如果贵组织达到其AI使用限制，则会显示使用限制消息，而不是说明。
