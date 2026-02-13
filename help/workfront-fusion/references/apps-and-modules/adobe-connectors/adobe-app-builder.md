---
title: Adobe App Builder模块
description: Adobe App Builder连接器允许您在场景中使用自定义函数。
author: Becky
feature: Workfront Fusion
source-git-commit: 8250d4fdad8ed7ffe63cd003f6e0cb325cbbfa8d
workflow-type: tm+mt
source-wordcount: '299'
ht-degree: 31%

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

当前唯一可用的Adobe App Builder模块是执行操作，该模块允许您使用之前配置的自定义JavaScript函数。

有关配置自定义函数的说明，请参阅[使用自定义函数映射数据](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md)。

### 执行操作

此模块执行以前配置的自定义函数。

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


