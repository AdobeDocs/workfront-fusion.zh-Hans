---
title: 将过滤器添加到方案
description: 在某些情况下，您只需要使用满足特定条件的包。 您可以使用过滤器选择这些包。
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# 将过滤器添加到方案

在某些情况下，您只需要使用满足特定条件的包。 您可以使用过滤器选择这些包。

例如，您可以为Workfront创建一个具有[!UICONTROL 监视记录]触发器的方案，以便仅捕获分配给特定用户的任务。

可以在两个模块之间添加过滤器，并检查从上述模块接收的捆绑包是否满足特定的过滤器条件：

* 如果是，则捆绑包将传递到场景中的下一个模块。
* 如果不存在，则终止对捆绑包的处理。

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

+++##先决条件

必须先将两个模块添加到方案中，然后才能在它们之间添加过滤器。

## 在两个模块之间添加过滤器：

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要添加过滤器的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 在要添加过滤器的模块之间单击扳手图标![扳手图标](assets/wrench-icon.png)，然后选择&#x200B;**设置过滤器**。
1. 在显示的框中，输入筛选器的&#x200B;**[!UICONTROL 标签]**。
1. 定义筛选器&#x200B;**[!UICONTROL 条件]**。

   在第一个字段中输入要作为筛选依据的字段、运算符，以及（如有必要）要与字段比较的值。

   >[!TIP]
   >
   >您可以从映射面板在筛选器字段中输入值
   >有关映射的详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

   例如，如果您希望过滤器在Adobe Workfront中传递以XML结尾的文件，则应在和的第一个框中输入&#x200B;**[!UICONTROL File name]**。第二个框中的&#x200B;**[!UICONTROL xml]**。 在它们之间的下拉菜单中，选择&#x200B;**[!UICONTROL 结尾为（不区分大小写）]**。 此过滤器将应用于来自第一个模块(Workfront)的传入包。 只有包含XML文件的包才会传递到下一个模块。

   ![设置筛选器](assets/set-up-filter-box.png)

1. 单击 **[!DNL OK]**。

## 复制筛选器

目前，场景编辑器不包括复制过滤器的功能。

>[!NOTE]
>
>如果复制过滤器两侧的模块，则也会复制过滤器。
>
>有关复制模块的详细信息，请参阅[在Adobe Workfront Fusion中复制模块或方案](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md)。

要复制筛选器而不复制模块，可以使用Fusion DevTool

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要添加过滤器的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击屏幕底部附近的DevTool图标![DevTool图标](assets/debugger-icon.png)以打开Fusion DevTool。

   如果您没有看到DevTool图标，请参阅[调试方案](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md)以获取有关打开DevTool的说明。

1. 单击左侧栏中的&#x200B;**[!UICONTROL 工具]**&#x200B;图标![DevTool工具](assets/devtools-tools-icon.png)。

1. 单击&#x200B;**[!UICONTROL 复制筛选器]**，然后在右侧面板中配置&#x200B;**[!UICONTROL 复制筛选器]**&#x200B;工具：

   1. 在要复制的筛选器之后直接将&#x200B;**[!UICONTROL Source模块]**&#x200B;设置为模块。
   1. 将&#x200B;**[!UICONTROL Target模块]**&#x200B;设置为要在其后直接放置过滤器的模块。

1. 单击&#x200B;**[!UICONTROL 运行]**。
