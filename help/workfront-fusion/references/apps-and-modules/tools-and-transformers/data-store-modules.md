---
title: 数据存储模块
description: Adobe Workfront Fusion数据存储与数据库或简单表类似，可以存储场景中的数据，从而可以在各个场景或场景运行之间传输数据。 在同步过程中，您可以使用数据存储来存储来自不同系统的新数据。
author: Becky
feature: Workfront Fusion
exl-id: 0338b822-b345-429e-850d-3978b692231d
TQID: https://experienceleague.adobe.com/xxcj73D3UZawazZrK92lAZTYaFTVj92o74zPRsnfFPA
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1139
ht-degree: 30%

---

# [!UICONTROL 数据存储]模块

Adobe Workfront Fusion数据存储与数据库或简单表类似，可以存储场景中的数据，从而可以在各个场景或场景运行之间传输数据。 在同步过程中，您可以使用数据存储来存储来自不同系统的新数据。

通过数据存储模块，您可以在Adobe Workfront Fusion数据存储中添加、替换、更新、检索、删除、搜索或计数记录。

<!--For information on creating, editing, and troubleshooting data stores, see [Data Stores in Adobe Workfront Fusion](/help/workfront-fusion/references/mapping-panel/data-types/)-->

有关Workfront Fusion中数据存储的视频介绍，请参阅：

* [数据存储](https://video.tv.adobe.com/v/3427029/){target=_blank}

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

要使用[!UICONTROL 数据存储]模块，您必须先创建数据存储。

有关创建数据存储的信息，请参阅[创建和管理数据存储](/help/workfront-fusion/create-scenarios/map-data/data-stores.md)。

## [!UICONTROL 数据存储]模块及其字段

配置数据存储模块时，Workfront Fusion会显示以下列出的字段。 除此之外，还可能会显示其他数据存储字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的加粗标题表示必填字段。

您无需创建连接即可使用数据存储。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

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

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

>[!NOTE]
>
>当您尝试添加以相同名称存在于数据存储中的记录时，模块会引发错误，并且[!UICONTROL 覆盖现有记录]选项被禁用。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 数据存储]</td> 
   <td> <p> 选择或添加要在其中创建记录的数据存储。 </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 键] </td> 
   <td> <p>输入您希望模块添加或替换的记录的唯一键。 该键以后可用于检索记录。 如果将此字段留空，则会自动生成键。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 覆盖现有记录] </td> 
   <td> <p>启用此选项以覆盖记录。 要覆盖的记录必须在上面的“键”字段中指定。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录] </td> 
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
   <td>[!UICONTROL 数据存储] </td> 
   <td> <p>选择要检查记录是否存在的数据存储。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 键] </td> 
   <td> <p>输入您希望模块检查是否存在记录的唯一键。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 记录数]

此操作模块对数据存储中的记录进行编号。

您指定数据存储。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 数据存储] </td> 
   <td> <p>选择包含要计数的记录的数据存储。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 删除记录]

此操作模块删除记录。

指定数据存储和记录的键。

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 数据存储] </td> 
   <td> <p>选择要检查记录是否存在的数据存储。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 键] </td> 
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
   <td>[!UICONTROL 数据存储] </td> 
   <td> <p>选择要从中删除所有记录的数据存储。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 获取记录]

此操作模块可检索记录。

指定数据存储和记录的键。

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 数据存储]</td> 
   <td> <p> 选择要从中检索记录的数据存储</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 键] </td> 
   <td> <p>输入您希望模块检索的记录的唯一键值。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 搜索记录]

此搜索模块在数据存储区中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 数据存储]</td> 
   <td> <p> 选择要搜索的数据存储。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 筛选条件]</p> </td> 
   <td> <p>为搜索设置过滤器。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 排序]</p> </td> 
   <td> <p style="font-weight: normal;">对于要作为排序依据的每个字段，请填写以下字段：</p> <p style="font-weight: bold;">[!UICONTROL 键]</p> <p>选择要作为结果排序依据的列名。</p> <p style="font-weight: bold;">[!UICONTROL 顺序]</p> <p>选择是否要以升序或降序对结果进行排序。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 限制]</td> 
   <td> <p> 设置Workfront Fusion在一个执行周期内返回的最大搜索结果数。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 即使模块未返回任何结果，仍继续执行路由]</td> 
   <td> <p> 如果启用，则此模块所属的路由将继续处理，即使此模块未返回任何结果。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 更新记录]

此操作模块更新记录。

指定数据存储和记录的键。

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 数据存储]</td> 
   <td> <p> 选择或添加要在其中创建记录的数据存储。 </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 键] </td> 
   <td> <p>输入您希望模块更新的记录的唯一键。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Insert missing record] </td> 
   <td> <p>启用此选项以在具有指定键的记录不存在时创建新记录。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录]</td> 
   <td> <p> 在要更新的记录字段中输入所需的值。</p> </td> 
  </tr> 
 </tbody> 
</table>
