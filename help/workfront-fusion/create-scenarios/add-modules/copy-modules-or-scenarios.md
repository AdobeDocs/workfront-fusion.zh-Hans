---
title: 复制模块或方案
description: 您可以在Adobe Workfront Fusion中复制模块、模块组或整个方案。 此功能允许您重复使用场景或部分场景，而无需再次构建它们。
author: Becky
feature: Workfront Fusion
exl-id: 5cece7d4-b2c7-4276-8a6f-f65bad799c7a
source-git-commit: c83070a7c2d1d048000a4eace4aaede73c7ec49d
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 0%

---

# 复制模块或方案

您可以在Adobe Workfront Fusion中复制模块、模块组或整个方案。 此功能允许您重复使用场景或部分场景，而无需再次构建它们。

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

## 先决条件

模块必须存在于场景中才能复制。

## 复制一个模块或一组模块

复制模块时，复制操作会保留原始模块的所有字段值和设置。

您可以将一个或多个模块粘贴到同一场景的另一个区域或另一个场景中。

将模块粘贴到其他方案时，请考虑以下事项：

* 从您未复制的其他模块中提取信息的任何字段值都将无法再访问该信息。 必须设置这些字段才能从新方案中提取信息。
* 如果将模块粘贴到另一个团队或组织所拥有的方案中，则必须将所有连接更新为拥有新方案的团队或组织所拥有的连接。

### 复制模块

复制一组模块与复制单个模块类似。

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要复制模块的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 右键单击要复制的模块。

   >[!NOTE]
   >
   >按住[!UICONTROL Shift]并单击要复制的模块，可选择多个模块。 复制一组模块时，还会复制它们之间的任何连接线、过滤器或路由逻辑。

1. 选择&#x200B;**[!UICONTROL 复制模块]**。
1. 将光标移动到您希望场景副本所在的场景区域。
1. 右键单击，然后选择&#x200B;**[!UICONTROL 粘贴]**。
1. 通过将粘贴的模块拖动到方案中的适当位置，将其连接到方案。

   您还可以使用键盘快捷键进行复制和粘贴。

## 通过克隆复制方案

克隆方案会创建方案的副本，然后可以对其进行编辑。

1. 打开方案详细信息页：

   1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡，然后单击要了解详细信息的方案。

      或

      如果您在方案编辑器中处理方案，请单击窗口左上角附近的左箭头![退出编辑箭头](assets/exit-editing-arrow.png)。

1. 右键单击页面右上角的&#x200B;**[!UICONTROL 选项]**。
1. 选择&#x200B;**[!UICONTROL 克隆]**。
1. （可选）输入新方案的名称。
1. （可选）启用&#x200B;**[!UICONTROL 使任何新模块的状态与正在复制的模块状态相同]**，以确保复制的方案也包含有关原始方案处理的最新记录的信息。
1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;以创建方案。

## 使用Blueprint复制方案

场景Blueprint表示给定场景在给定时间点的排列、映射和字段值。 您可以将方案Blueprint导出到计算机上的JSON文件中，然后在创建新方案时导入它。 可以编辑从方案Blueprint导入的方案。

方案Blueprint表示整个方案。 如果只想从场景中复制某些模块，请参阅本文中的[复制模块或模块组](#copy-a-module-or-a-group-of-modules)。

### 导出方案Blueprint

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要导出Blueprint的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 在方案中，单击方案设置区域中的&#x200B;**[!UICONTROL 更多]**&#x200B;菜单。
1. 单击&#x200B;**[!UICONTROL 导出Blueprint]**。

   将创建一个JSON文件并下载到您的计算机。 您可以在[!DNL Downloads]文件夹中找到此文件。

>[!NOTE]
>
>要导出方案的先前版本的Blueprint，请参阅[查看和管理方案版本](/help/workfront-fusion/manage-scenarios/restore-a-scenario-version.md)。

### 导入Blueprint

>[!IMPORTANT]
>
>如果将Blueprint导入现有方案，则方案Blueprint将替换现有方案。 不能将Blueprint附加到现有方案。

1. 开始创建新方案。
1. 在方案中，单击方案设置区域中的&#x200B;**[!UICONTROL 更多]**&#x200B;菜单。
1. 单击&#x200B;**[!UICONTROL 导入Blueprint]**。
1. 在出现的对话框中，单击&#x200B;**[!UICONTROL 浏览]**
1. 导航到要导入的Blueprint，然后单击&#x200B;**[!UICONTROL 打开]**。
1. 单击&#x200B;**[!UICONTROL 保存]**。

   将创建一个JSON文件并下载到您的计算机。 您可以在[!UICONTROL 下载]文件夹中找到此文件。

## 使用模板复制和重用方案

您可以创建模板作为Workfront Fusion方案的起点。 从模板创建方案时，无需修改模板即可修改方案。 字段值未保存在模板中。

有关使用模板创建方案的详细信息，请参阅[使用模板创建方案](/help/workfront-fusion/create-scenarios/add-modules/create-scenarios-with-fusion-templates.md)。

## 故障排除

如果要按照[复制模块或模块组](#copy-a-module-or-a-group-of-modules)中的说明复制并粘贴模块，粘贴时不会显示任何内容，请检查浏览器的网站设置，以确保允许从剪贴板进行粘贴。
