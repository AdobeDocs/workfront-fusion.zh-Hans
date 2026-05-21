---
title: 将信息从一个模块映射到另一个模块
description: 映射是将模块输出（由项目构成）分配到另一个模块输入字段的过程。
author: Becky
feature: Workfront Fusion
exl-id: 1e3f7729-f48e-451e-a90b-d680c9e3bcbc
TQID: https://experienceleague.adobe.com/wKSHupk1Gx2g7ydAOilpbfRnqu-TMY5W8zKEyKd8Slk
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 777
ht-degree: 17%

---

# 将信息从一个模块映射到另一个模块

映射是将一个模块的输出分配到另一个模块的输入字段的过程。

单击某个字段时，将显示映射面板，您可以在该字段中插入从场景中的上一个模块输出的值。

您还可以使用映射面板中的函数和映射项的任意组合以及键入的静态文本来创建公式。 这些元素可以相互嵌套。

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

## 映射项目

通过链接两个或多个模块创建一系列模块后，每个模块可以处理其前面的模块输出的项目值。

要将输出项分配给模块的输入字段，请执行以下操作：

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要映射数据的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击应处理上述一个或多个模块输出的模块。
1. 在显示的模块设置面板中，单击要使用从前一模块输出的项目值的字段。

   将打开映射面板。

1. （可选）要在映射面板中搜索特定字段，请单击映射面板搜索栏，然后键入要搜索的搜索词。 当字段显示在列表中时，单击该字段。

   搜索结果包含搜索词且不区分大小写。
1. 要选择某个值，该值是某个收集的一个要素，请单击该收集旁边的箭头，然后在该要素出现时选择该要素。

   ![收藏集元素](assets/collection-dropdown.png)

1. 单击映射面板中的项以将其插入到字段中。

有关详细信息，请参阅[配置模块](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)。


## 故障排除

### 问题：映射面板中缺少项目

映射面板显示以前模块的输出项。 有时，此面板中可能缺少某些项目。 您可以在场景编辑器中运行缺少输出的模块，然后映射面板可以在后面的模块中包含这些项。 确切的过程因模块的类型而异。

* [即时触发](#instant-trigger)
* [轮询触发器](#polling-trigger)
* [其他模块](#other-modules)

#### 即时触发

1. 右键单击该模块，然后在显示的菜单中单击&#x200B;**[!UICONTROL 仅运行此模块]**。

   由于这是一个即时触发器，因此它会开始观察事件。

1. 创建模块正在监视的事件。

   例如，如果模块是监视任务分配的Workfront >监视事件模块，请登录Workfront（作为非Fusion连接正在使用的用户）并分配任务。

1. 当模块完成运行时，单击模块上方的气泡以浏览其完整输出。

   以后模块的映射面板现在包含模块输出中的所有项。

#### 轮询触发器

1. 右键单击该模块，然后在显示的菜单中单击&#x200B;**[!UICONTROL 仅运行此模块]**。
1. 如果没有输出，请单击&#x200B;**[!UICONTROL 选择开始位置]**&#x200B;并调整设置。
1. （视情况而定）如果没有要处理的事件，请创建模块要监视的事件，并重复步骤2。

   例如，如果模块是监视任务分配的Workfront >观察记录模块，请登录Workfront（作为非Fusion连接正在使用的用户）并分配任务，然后再次运行模块。

1. 当模块完成运行时，单击模块上方的气泡以浏览其完整输出。

   以后模块的映射面板现在包含模块输出中的所有项。

#### 其他模块

您可以选择执行：

* 整个场景（或仅包含模块的部分）
* 单个模块

要执行单个模块，请执行以下操作：

1. 右键单击该模块，然后在显示的菜单中单击&#x200B;**[!UICONTROL 仅运行此模块]**。
1. 提供输入项的示例值，然后单击&#x200B;**[!UICONTROL 确定]** 。
1. 当模块完成运行时，单击模块上方的气泡以浏览其完整输出。

   以后模块的映射面板现在包含模块输出中的所有项。
