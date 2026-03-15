---
title: 为场景添加筛选条件
description: 在某些情况下，您只需要使用满足特定条件的包。 您可以使用过滤器选择这些包。
author: Becky
feature: Workfront Fusion
exl-id: b507dca0-0e85-4ab7-8310-b6e6bcb7ae12
source-git-commit: bec838423e13c3efe4f3d002f824c203cad6ecf8
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 19%

---

# 为场景添加筛选条件

在某些情况下，您只需要使用满足特定条件的包。 您可以使用过滤器选择这些包。

例如，您可以为Workfront创建一个具有[!UICONTROL 监视记录]触发器的方案，以便仅捕获分配给特定用户的任务。

可以在两个模块之间添加过滤器，并检查从上述模块接收的捆绑包是否满足特定的过滤器条件：

* 如果是，则捆绑包将传递到场景中的下一个模块。
* 如果不存在，则终止对捆绑包的处理。

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

您可以复制现有筛选器并将其粘贴到场景中的其他位置。

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要添加过滤器的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 右键单击过滤器所在的模块之间的连接点。
1. 选择&#x200B;**复制筛选器**。
1. 右键单击要粘贴过滤器的模块之间的连接点。
1. 选择**粘贴筛选器
1. （可选）要调整筛选器，请单击筛选器图标或标签，然后输入值，如本文中的[在两个模块之间添加筛选器](#add-a-filter-between-two-modules)中所述。




<!--

Currently, the scenario editor does include a feature for copying a filter.

>[!NOTE]
>
>If you copy the modules on either side of the filter, the filter is also copied.
>
>For more information on copying modules, see [Copy modules or scenarios in Adobe Workfront Fusion](/help/workfront-fusion/create-scenarios/add-modules/copy-modules-or-scenarios.md).

To copy a filter without copying modules, you can use the Fusion DevTool

1. Click the **[!UICONTROL Scenarios]** tab in the left panel.
1. Select the scenario where you want to add a filter.
1. Click anywhere on the scenario to enter the Scenario editor.
1. Open the Fusion DevTool by clicking on the DevTool icon ![DevTool icon](assets/debugger-icon.png) near the bottom of the screen.
   
   If you do not see the DevTool icon, see [Debug a scenario](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md) for instructions on opening the DevTool.
   
1. Click the **[!UICONTROL Tools]** icon ![DevTool tools](assets/devtools-tools-icon.png) in the left side bar.

1. Click **[!UICONTROL Copy Filter]**, then configure the **[!UICONTROL Copy Filter]** tool in the right side panel:

   1. Set the **[!UICONTROL Source Module]** as the module directly after the filter you want to copy.
   1. Set the **[!UICONTROL Target Module]** as the module that you want to place the filter directly after.

1. Click **[!UICONTROL Run]**.

-->
