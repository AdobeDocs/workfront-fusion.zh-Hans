---
title: 在场景中查找和替换变量、源和连接
description: 使用“查找并替换”可替换映射的变量、将引用从一个源模块重新映射到另一个源模块，或将连接复制到场景中的其他模块。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 15%
---

# 在场景中查找和替换变量、源和连接

>[!NOTE]
>
>此功能仅在新的方案编辑器体验中可用。 有关详细信息，请参阅文章场景编辑器中的[新体验和经典体验](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)。

通过“查找”和“替换”，可一次性对多个模块进行相同的更改。 您可以：

* 在整个场景中或在一个模块中替换映射的变量。
* 将引用从一个源模块重新映射到另一个源模块。
* 将连接从同一应用程序复制到一个或所有兼容的模块。

在进行更改之前，“查找和替换”会显示将受影响的模块的预览。

在经典Experience中，您可以使用DevTool中的“交换”变量、“重新映射源”和“交换”连接工具来执行这些任务。 有关详细信息，请参阅[调试方案](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md)。

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

## 打开“查找并替换”

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要进行更改的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 在控件区域单击&#x200B;**查找和替换**&#x200B;图标![查找和替换](assets/find-replace-icon.png)。

   您可能需要单击“控件”区域中的三个圆点图标来查看“查找并替换”图标。

查找和替换在画布右侧的面板中打开。

## 替换变量

使用&#x200B;**变量**&#x200B;选项卡替换映射的变量。

1. 打开“查找和替换”，然后单击“**变量**”选项卡。
1. 在要查找的变量字段中，粘贴要替换的变量。
1. 在替换为字段中，粘贴将替换上一个变量的变量。
1. 在“模块”字段中，选择将应用更改的模块，或选择&#x200B;**整个方案**&#x200B;将更改应用到方案中所有受影响的模块。
1. 单击&#x200B;**替换**
1. 查看将受影响的模块的预览。 要转到画布上的模块，请在预览中选择其行。
1. 单击&#x200B;**应用**。

## 重新映射源

使用&#x200B;**Source**&#x200B;选项卡更改其他模块中的映射引用的模块。

1. 打开“查找并替换”，然后单击&#x200B;**Source**&#x200B;选项卡。
1. 在Source模块字段中，选择映射当前引用的源模块。
1. 在Target模块字段中，选择他们应引用的模块。
1. 在“模块”字段中，选择将应用更改的模块，或选择&#x200B;**整个方案**&#x200B;将更改应用到方案中所有受影响的模块。
1. 单击&#x200B;**替换**
1. 查看将受影响的模块的预览。 要转到画布上的模块，请在预览中选择其行。
1. 单击&#x200B;**应用**。

## 将连接复制到其他模块

使用&#x200B;**连接**&#x200B;选项卡可在同一应用程序的多个模块中使用相同的连接。

1. 打开“查找并替换”，然后单击“**连接**”选项卡。
1. 在“连接自”字段中，选择当前具有要用于其他模块的连接的模块。
1. 在应用至字段中，选择要应用更改的模块，或者是否将更改应用到场景中的所有兼容模块。
1. 单击&#x200B;**应用**。
