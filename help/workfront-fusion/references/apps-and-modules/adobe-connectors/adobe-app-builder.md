---
title: Adobe App Builder模块
description: Adobe App Builder连接器允许您在场景中使用自定义函数。
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
source-git-commit: 042f32f35e630ec76a7356fa750f5238f74a6f25
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 23%

---

# Adobe App Builder模块

您可以在Fusion的“函数”区域中创建自定义函数。 然后，以Adobe App Builder模块的形式将这些函数添加到场景中。

由于自定义函数可通过Adobe App Builder使用，因此您的组织必须具有Adobe App Builder许可证才能使用它们。

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
   <p><ul><li>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li><li>您必须拥有Adobe App Builder许可证才能使用自定义函数。</ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## Adobe App Builder模块

<!--

### Run a custom code block

This module allows you to run a code block. You configure the code block when you set up the module, and it is run when the module runs during a scenario execution.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>Select the connection that contains the custom function that you want to run. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Code block]</td> 
   <td>Enter the block of code that you want the module to run.<p>To format the code for easier reading, click the <b>Format code</b> icon.</td> 
  </tr> 
   </tbody> 
</table>

-->

### 从包运行自定义函数

此模块从包中运行函数。

<!--For information on packages, see []().-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>选择包含要运行的自定义函数的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL包]</td> 
   <td>选择包含要在场景中运行的函数的包。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量] </td> 
   <td>选择要在场景中运行的函数。</p></td> 
  </tr> 
   </tbody> 
</table>

### 使用包中的变量

此模块会将包中配置的变量引入场景。

<!--For information on packages, see []().-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>选择包含要运行的自定义函数的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL包]</td> 
   <td>选择包含要纳入场景的变量的资源包。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量] </td> 
   <td>选择要纳入场景的变量。</p></td> 
  </tr> 
   </tbody> 
</table>

### 运行自定义函数或代码块

通过此模块，您可以使用存储在函数区域中的之前配置的自定义JavaScript函数。

有关配置自定义函数的说明，请参阅[使用自定义函数映射数据](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md)。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>选择包含要运行的自定义函数的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 操作]</td> 
   <td>选择要运行的自定义函数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL参数] </td> 
   <td>输入函数参数的值。 可用参数基于创建函数时配置的参数。<p>如果某个参数具有默认值，则您将不会在字段中看到该默认值，但可以通过在字段中输入或映射值来覆盖该默认值。</p></td> 
  </tr> 
   </tbody> 
</table>
