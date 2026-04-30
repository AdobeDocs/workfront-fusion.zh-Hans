---
title: 查看链接方案关系
description: 您可以映射父方案和子方案之间的关系。
author: Becky
feature: Workfront Fusion
exl-id: 0782c6b1-42a5-48de-bfa0-3ced6ed2bf7f
source-git-commit: aee2b35919e240cce5346df6d94a610c34b26e88
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 18%

---

# 查看和管理链接方案关系

您可以映射父方案和子方案之间的关系。 您还可以使用映射跳转到链中的不同方案。

有关链接方案的详细信息，请参阅[链接多个方案](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)。

有关配置链接方案的信息，请参阅[链接模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md)

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

## 查看链接关系的映射

您可以查看当前方案及其父方案或子方案的映射。 该图显示了链接方案中的数据流图表。

![链接方案关系](assets/chained-scenario-relationships-2.png)

<!--get a better picture-->

要查看链接方案的关系图，请执行以下操作：

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡，然后单击方案。

   或

   如果您在方案编辑器中处理方案，请单击窗口左上角附近的左箭头![退出编辑箭头](assets/exit-editing-arrow.png)。

1. 单击&#x200B;**关系**&#x200B;选项卡。

   ![关系选项卡](assets/relations-tab.png)

1. 有关每个链接方案的一般详细信息，请检查标记。

   每个方案都有一个或多个以下标记：

   * 根：方案是链的开始，没有父方案。
   * 父项：方案是父方案。
   * 子项：方案是子方案。 方案既可以是父项，也可以是子项。
   * 当前：这是用户当前正在查看的方案。 换句话说，这是用户打开关系映射的场景。

   关系图中的![方案标记](assets/chained-scenario-maps-tag.png)
1. （可选）要查看方案的小型图表，请将鼠标悬停在方案上。
1. （可选）要从映射直接转到另一个方案，请单击该方案。

   单击的场景将在另一个窗口中打开。
1. （可选）要在地图的水平视图和垂直视图之间切换，请单击“方案详细信息”页面右上角附近的&#x200B;**水平**&#x200B;或&#x200B;**垂直**。
1. （可选）要查看地图的简化视图，请检查页面的右下角。

   如果链图较大或复杂，这可能很方便。

   * 如果只查看地图的一部分，则该部分在简化图上较暗。
   * 在简化的地图上，当前方案以蓝色标记。
1. 要查看链的执行历史记录，请单击视图顶部附近的“历史记录”选项卡。

   您可以单击历史记录以查看链接方案之间传递的特定数据。
