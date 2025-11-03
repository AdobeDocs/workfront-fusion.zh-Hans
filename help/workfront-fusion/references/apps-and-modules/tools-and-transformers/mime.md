---
title: MIME模块
description: 您可以在Adobe Workfront Fusion中使用MIME类型。 多用途Internet邮件扩展(MIME)类型是允许软件识别在Internet上共享的不同类型数据的标签。 Web服务器和浏览器使用MIME类型来确定应该对文件执行的操作。 例如，具有MIME类型text/html的文件在浏览器中的处理方式与MIME类型image/jpeg的文件有所不同。 MIME类型独立于操作系统和硬件。
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# [!UICONTROL MIME]模块

您可以在Adobe Workfront Fusion中使用MIME类型。 多用途Internet邮件扩展(MIME)类型是允许软件识别在Internet上共享的不同类型数据的标签。 Web服务器和浏览器使用MIME类型来确定应该对文件执行的操作。 例如，在浏览器中处理MIME类型为`text/html`的文件的方式与MIME类型为`image/jpeg`的文件的方式不同。 MIME类型独立于操作系统和硬件。

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



## [!UICONTROL MIME]模块及其字段

* [获取文件扩展名](#get-a-file-extension)
* [获取MIME类型](#get-a-mime-type)

### [!UICONTROL 获取文件扩展名]

此转换器模块返回给定MIME类型的原始文件扩展名。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL MIME类型]</td> 
   <td> <p>输入或映射要确定其文件扩展名的MIME类型。 </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 获取MIME类型]

此转换器模块返回与给定文件名、路径或扩展名关联的MIME类型。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件]</td> 
   <td> <p>输入或映射要为其确定MIME类型的文件。 </p> <p>您可以使用以下方式输入文件：</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL文件路径]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>示例： </b></span></span>/file/image.jpeg</p> </li> 
     <li><strong>[！UICONTROL文件名]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>示例：</b></span></span>image.jpeg</p> </li> 
     <li><strong>[！UICONTROL文件扩展名]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>示例：</b></span></span>jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
