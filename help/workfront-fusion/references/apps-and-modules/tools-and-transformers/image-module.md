---
title: 图像模块
description: Adobe Workfront Fusion图像模块允许您获取有关特定图像的信息（尺寸、类型等），将图像转换为另一种文件格式，并直接更改图像的大小。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: a7696c9d-002d-4bb4-ae10-1f69dc5e66fe
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# 图像模块

Adobe Workfront Fusion [!UICONTROL 图像]模块允许您获取有关特定图像（尺寸、类型等）的信息，将图像转换为其他文件格式，并直接更改图像的大小。

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



## [!UICONTROL 图像]模块及其字段

配置此模块时，会显示以下字段。 模块中的粗体标题表示必填字段。

* [[!UICONTROL 转换格式]](#convert-a-format)
* [[!UICONTROL 提取元数据]](#extract-metadata)
* [[!UICONTROL 调整大小]](#resize)

### [!UICONTROL 转换格式]

此转换器模块更改图像文件的格式。 此模块兼容以下格式：

* PNG
* JPG
* GIF
* BMP

源文件和输出都必须采用以下格式之一。 例如，[!UICONTROL Image] >[!UICONTROL 转换格式]模块可以将PNG文件转换为BMP文件，或将BMP转换为JPG。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出格式]</td> 
   <td>选择您希望模块将源文件转换成的格式。 </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 提取元数据]

此转换器模块返回有关模块的基本信息。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 调整大小]

此转换器模块会根据您指定的条件更改图像的高度和宽度。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL我想]</td> 
   <td>选择是要保持高宽比还是将尺寸更改为指定的高度和宽度。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL根据]</td> 
   <td> <p>选择您希望模块如何确定图像的新大小。 如果您在“我想”字段中选择了保持高宽比，则会显示此字段。 根据在此字段中选择的内容，将显示其他字段。</p> 
    <ul> 
     <li> <p>[！UICONTROL最大宽度]</p> <p>将图像缩小到您指定的宽度。 高度会自动计算。</p> </li> 
     <li> <p>[！UICONTROL最大高度]</p> <p>将图像缩小到您指定的高度。 会自动计算宽度。</p> </li> 
     <li> <p>[！UICONTROL最大高度或宽度]</p> <p>以高度和宽度不超过指定值的方式缩小图像。 由于此选项会保持高宽比，因此其中一个尺寸可能小于指定的尺寸。 例如，如果高度和宽度都指定为40，则400x300图像将减少到40X30。</p> </li> 
     <li> <p>[！UICONTROL最小宽度]</p> <p>将图像放大到您指定的宽度。 高度会自动计算。</p> </li> 
     <li> <p>[！UICONTROL最小高度]</p> <p>将图像放大到您指定的高度。 会自动计算宽度。</p> </li> 
     <li> <p>[！UICONTROL最小高度或宽度]</p> <p>以不小于指定值的高度和宽度来放大图像。 由于此选项会保持高宽比，因此其中一个尺寸可能大于指定的尺寸。 例如，如果高度和宽度都指定为300，则40x30图像将放大为400X300。</p> </li> 
     <li> <p>[！UICONTROL百分比]</p> <p>根据您指定的值按百分比更改图像大小。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL宽度]</td> 
   <td>输入或映射调整大小的图像的所需宽度（以像素为单位）。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Height]</td> 
   <td>输入或映射调整大小后图像的所需高度（以像素为单位）。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL百分比变化]</td> 
   <td>如果您已选择按百分比更改图像，请输入或映射要更改图像的百分比。</td> 
  </tr> 
 </tbody> 
</table>

## 故障排除

### 操作因错误而终止

由于以下原因之一，操作可能会因错误而终止：

* 接收的数据不是JPG/GIF/PNG/BMP格式
* 更改图像尺寸时，超过了最大宽度/高度限制。 图像大小不得超过3840像素宽度和2160像素高度
* 更改图像的尺寸或格式时，超出了图像的最大允许大小。
