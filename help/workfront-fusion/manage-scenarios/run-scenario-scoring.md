---
title: 运行方案得分专家
description: 场景评分专家可以帮助您确保按照最佳实践的方式配置场景。 它会检查您的方案并提供有关其结构和组织的建议。
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# 运行方案得分专家

>[!IMPORTANT]
>
>场景得分专家已暂时禁用。

场景评分专家可以帮助您确保按照最佳实践的方式配置场景。 它会检查您的方案并提供有关其结构和组织的建议。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何Adobe Workfront Workflow包和任何Adobe Workfront自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime和Select包，以及额外购买的Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>标准</p><p>工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果贵组织具有不包含Workfront Automation and Integration的Select或Prime Workfront包，则贵组织必须购买Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

+++

## 运行方案得分专家

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
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

  有关说明，请参阅Workfront > [观看活动[!UICONTROL 模块]中的](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules)活动订阅筛选器。
