---
title: 数据存储模块
description: Adobe Workfront Fusion数据存储与数据库或简单表类似，可以存储场景中的数据，从而可以在各个场景或场景运行之间传输数据。 在同步过程中，您可以使用数据存储来存储来自不同系统的新数据。
author: Becky
feature: Workfront Fusion
exl-id: 0338b822-b345-429e-850d-3978b692231d
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '1139'
ht-degree: 0%

---

# [!UICONTROL 数据存储]模块

Adobe Workfront Fusion数据存储与数据库或简单表类似，可以存储场景中的数据，从而可以在各个场景或场景运行之间传输数据。 在同步过程中，您可以使用数据存储来存储来自不同系统的新数据。

通过数据存储模块，您可以在Adobe Workfront Fusion数据存储中添加、替换、更新、检索、删除、搜索或计数记录。

<!--For information on creating, editing, and troubleshooting data stores, see [Data Stores in Adobe Workfront Fusion](/help/workfront-fusion/references/mapping-panel/data-types/)-->

有关Workfront Fusion中数据存储的视频介绍，请参阅：

* [数据存储](https://video.tv.adobe.com/v/3427029/){target=_blank}

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

要使用[!UICONTROL 数据存储]模块，您必须先创建数据存储。

有关创建数据存储的信息，请参阅[创建和管理数据存储](/help/workfront-fusion/create-scenarios/map-data/data-stores.md)。

## [!UICONTROL 数据存储]模块及其字段

配置数据存储模块时，Workfront Fusion会显示以下列出的字段。 除此之外，还可能会显示其他数据存储字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

您无需创建连接即可使用数据存储。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [添加/替换记录](#addreplace-a-record)
* [检查记录是否存在](#check-the-existence-of-a-record)
* [对记录计数](#count-records)
* [删除记录](#delete-a-record)
* [删除所有记录](#delete-all-records)
* [获取记录](#get-a-record)
* [搜索记录](#search-records)
* [更新记录](#update-a-record)

### [!UICONTROL 添加/替换记录]

此操作模块添加或替换记录。

指定数据存储和记录的键。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

>[!NOTE]
>
>当您尝试添加以相同名称存在于数据存储中的记录时，模块会引发错误，并且[!UICONTROL 覆盖现有记录]选项被禁用。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL数据存储]</td> 
   <td> <p> 选择或添加要在其中创建记录的数据存储。 </p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Key] </td> 
   <td> <p>输入您希望模块添加或替换的记录的唯一键。 该键以后可用于检索记录。 如果将此字段留空，则会自动生成键。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL覆盖现有记录] </td> 
   <td> <p>启用此选项以覆盖记录。 要覆盖的记录必须在上面的“键”字段中指定。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL记录] </td> 
   <td> <p>在记录的字段中输入所需的值。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 检查记录是否存在]

此操作模块指定特定记录是否存在。

指定数据存储和记录的键。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL数据存储] </td> 
   <td> <p>选择要检查记录是否存在的数据存储。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Key] </td> 
   <td> <p>输入您希望模块检查是否存在记录的唯一键。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 记录数]

此操作模块对数据存储中的记录进行编号。

您指定数据存储。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL数据存储] </td> 
   <td> <p>选择包含要计数的记录的数据存储。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 删除记录]

此操作模块删除记录。

指定数据存储和记录的键。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL数据存储] </td> 
   <td> <p>选择要检查记录是否存在的数据存储。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Key] </td> 
   <td> <p>输入您希望模块删除的记录的唯一键值。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 删除所有记录]

此操作模块会从特定数据存储中删除所有记录。

您指定数据存储。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL数据存储] </td> 
   <td> <p>选择要从中删除所有记录的数据存储。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 获取记录]

此操作模块可检索记录。

指定数据存储和记录的键。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL数据存储]</td> 
   <td> <p> 选择要从中检索记录的数据存储</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Key] </td> 
   <td> <p>输入您希望模块检索的记录的唯一键值。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 搜索记录]

此搜索模块在数据存储区中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL数据存储]</td> 
   <td> <p> 选择要搜索的数据存储。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL筛选器]</p> </td> 
   <td> <p>为搜索设置过滤器。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL排序]</p> </td> 
   <td> <p style="font-weight: normal;">对于要作为排序依据的每个字段，请填写以下字段：</p> <p style="font-weight: bold;">[！UICONTROL Key]</p> <p>选择要作为结果排序依据的列名。</p> <p style="font-weight: bold;">[！UICONTROL顺序]</p> <p>选择是否要以升序或降序对结果进行排序。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL限制]</td> 
   <td> <p> 设置Workfront Fusion在一个执行周期内返回的最大搜索结果数。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL即使模块未返回任何结果，仍继续执行路由]</td> 
   <td> <p> 如果启用，则此模块所属的路由将继续处理，即使此模块未返回任何结果。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 更新记录]

此操作模块更新记录。

指定数据存储和记录的键。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL数据存储]</td> 
   <td> <p> 选择或添加要在其中创建记录的数据存储。 </p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Key] </td> 
   <td> <p>输入您希望模块更新的记录的唯一键。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Insert missing record] </td> 
   <td> <p>启用此选项以在具有指定键的记录不存在时创建新记录。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL记录]</td> 
   <td> <p> 在要更新的记录字段中输入所需的值。</p> </td> 
  </tr> 
 </tbody> 
</table>
