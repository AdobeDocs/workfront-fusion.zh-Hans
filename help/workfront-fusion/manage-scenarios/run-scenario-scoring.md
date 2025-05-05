---
title: 运行方案得分专家
description: 场景评分专家可以帮助您确保按照最佳实践的方式配置场景。 它会检查您的方案并提供有关其结构和组织的建议。
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 1ac1c4358901ef81bb7375c24fcdf1a44119af13
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 1%

---

# 运行方案得分专家

>[!IMPORTANT]
>
>场景得分专家已暂时禁用。

场景评分专家可以帮助您确保按照最佳实践的方式配置场景。 它会检查您的方案并提供有关其结构和组织的建议。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证</td> 
   <td> <p>新增： [!UICONTROL Standard]</p><p>或</p><p>当前： [!UICONTROL Work]或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>[!UICONTROL Select] 或[!UICONTROL Prime] [!DNL Workfront]计划：您的组织必须购买[!DNL Adobe Workfront Fusion]。</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 计划： [!DNL Workfront Fusion]已包括在内。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买[!DNL Adobe Workfront Fusion]。</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">访问级别配置*</td> 
   <td> 
     <p>您必须是组织的[!DNL Workfront Fusion]管理员。</p>
     <p>您必须是团队的[!DNL Workfront Fusion]管理员。</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 运行方案得分专家

1. 单击左侧面板中的&#x200B;**[!UICONTROL Scenarios]**&#x200B;选项卡。
1. 选择要运行方案评分专家的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击屏幕底部附近的“场景评分专家”图标![场景评分专家](assets/scoring-expert-icon.png)。

   此时将打开“场景评分专家”面板。
1. 单击&#x200B;**评估**。

场景评分专家返回10分，并显示哪些检查通过或失败。 如果检查失败，场景评分专家会就如何确保场景满足这些检查提出建议。

![方案得分](assets/scenario-score.png)

## 场景评分检查

方案得分专家使用以下检查：

* 必须命名方案。
* 必须为所有模块设置标签。
* 方案必须按设定的计划运行。

  有关说明，请参阅[计划方案](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。
* 方案Blueprint大小必须小于5 MB。

  有关详细信息，请参阅[Fusion性能护栏](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#scenarios)。
* 如果使用Workfront instant trigger模块，则必须对其进行筛选。

  有关说明，请参阅 [!DNL Workfront] > [!UICONTROL Watch Events]模块[&#128279;](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules)中的事件订阅筛选器。
