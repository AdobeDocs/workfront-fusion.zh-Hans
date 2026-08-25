---
title: 将模块移动到链
description: 您可以选择方案中的一组模块并将它们移动到新的链接方案中，而无需手动重新创建映射或数据结构。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: f1a80f64edc410ae76bfbba1280df7232e2d09c5
workflow-type: tm+mt
source-wordcount: 513
ht-degree: 17%

---

# 将模块移动到链

>[!IMPORTANT]
>
>此功能位于Beta中，不建议用于任务关键型生产工作流。 作为Beta功能，行为可能会发生更改，并且可能无法完全处理边缘情况。

您可以选择方案中的一组模块并将它们移动到新的链接方案中，而无需手动重新创建映射或数据结构。 这提供了一种将大型场景模块化的简单方法。

将一组模块移动到链中时，Workfront Fusion：

* 将选定模块移动到新创建的方案中。
* 在单独的浏览器窗口中打开新方案。
* 将原始方案中的选定模块替换为链>调用子方案模块。
* 自动创建新的子方案所需的输入和输出数据结构。
* 保留现有方案行为，因此方案将继续以移动模块之前的方式运行。
* 自动更新映射：
  * 移到子方案中的模块通过链>从父模块的输入接收数据，来接收数据。
  * 子方案的输出将自动显示回父方案。
  * Blueprint中的现有映射会被调整以匹配新结构。

有关计划链接方案的信息，请参阅[链接多个方案](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)。

有关配置链模块的说明，请参阅[链模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)。

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

## 先决条件

要移动到链中的模块必须已存在于方案中，并且必须选择多个模块。

## 限制

在以下情况中，不能将选定模块移入链：

* 所选模块不是单个不间断流的一部分。 例如，不能同时从两条不同的未连接路由中选择模块。
* 该选择包括webhook模块。
* 该选项包括另一个链模块。
* 该选项包括一个路由器模块，而您尚未选择该路由器的所有路由。
* 选定的模块具有错误处理程序路由，而您尚未选择该路由。

## 将模块移动到链中

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择包含要移动的模块的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 通过按住[!UICONTROL Shift]并单击要移动的模块，选择要移动到链中的模块。
1. 右键单击其中一个选定的模块。
1. 选择&#x200B;**[!UICONTROL 移动到链]**。
