---
title: 运行场景评分专家
description: 场景评分专家可以帮助您确保按照最佳实践的方式配置场景。 它会检查您的方案并提供有关其结构和组织的建议。
author: Becky
feature: Workfront Fusion
exl-id: b668e7f6-dac5-4ac9-b3f3-109f70eaa2c4
TQID: https://experienceleague.adobe.com/g8v-odwnN-wtyzSh8wr6LSNL7xLIBs8Guw2zY-JW700
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 32%

---

# 运行场景评分专家

>[!IMPORTANT]
>
>场景得分专家已暂时禁用。

场景评分专家可以帮助您确保按照最佳实践的方式配置场景。 它会检查您的方案并提供有关其结构和组织的建议。

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
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 运行场景评分专家

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

  有关操作步骤，请参阅[计划场景](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。
* 方案Blueprint大小必须小于5 MB。

  有关详细信息，请参阅[Fusion性能护栏](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md#scenarios)。
* 如果使用Workfront instant trigger模块，则必须对其进行筛选。

  有关说明，请参阅Workfront > [!UICONTROL 观看活动]模块](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules)中的[活动订阅筛选器。
