---
title: 数据存储在 [!DNL Adobe Workfront Fusion]中
description: 数据存储类似于数据库或简单表，可以存储场景中的数据，从而可以在单独的场景或场景运行之间传输数据。 在同步过程中，您可以使用数据存储来存储来自不同系统的新数据。
author: Becky
feature: Workfront Fusion
exl-id: 8bfa3201-45db-49d7-985d-9c324acd56b6
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 1%

---

# 创建和管理数据存储

数据存储类似于数据库或简单表，可以存储场景中的数据，从而可以在单独的场景或场景运行之间传输数据。 在同步过程中，您可以使用数据存储来存储来自不同系统的新数据。

数据存储模块允许您对[!DNL Adobe Workfront Fusion]数据存储中的记录执行以下操作：

* 添加
* 替换
* 更新
* Retrieve
* 删除
* 搜索
* 计数

有关使用数据存储模块的信息，请参阅[[!UICONTROL Data store]模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md)。

有关Workfront Fusion中数据存储的视频介绍，请参阅：

* [数据存储](https://video.tv.adobe.com/v/3427029/){target=_blank}

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证</td> 
   <td> <p>新增： [!UICONTROL Standard]</p><p>或</p><p>当前： [!UICONTROL Work]或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>[!UICONTROL Select] 或[!UICONTROL Prime] [!DNL Workfront]计划：您的组织必须购买[!DNL Adobe Workfront Fusion]。</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 计划： [!DNL Workfront Fusion]已包括在内。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买[!DNL Adobe Workfront Fusion]。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 可用数据空间

如果贵组织使用的是新的Workfront计划模型(Select、Prime和Ultimate包)，则贵组织的计划会影响Fusion实例可用的数据存储的大小和数量。

### Ultimate计划

Ultimate包上的Fusion实例将接收：

* 100 MB空间
* 50个数据存储

### 选择和Prime计划

Select或Prime包上的Fusion实例将接收：—>

* 第一个500K操作为100 MB。

* 每个额外的100,000操作为10 MB。

  例如，拥有600K操作的组织接收110 MB。

您的组织最多可以拥有50个数据存储。 这些数据存储的组合大小不能超过贵组织的数据存储总大小。

## 在[!DNL Workfront Fusion]中创建数据存储

* [设置数据存储](#set-up-the-data-store)
* [设置数据结构](#set-up-the-data-structure)

### 设置数据存储

在模块中使用数据存储之前，必须在[!DNL Workfront Fusion]中创建数据存储。

>[!NOTE]
>
>您的组织的可用数据存储数量有限。 如果尝试创建的数据存储区多于可用存储区，[!DNL Workfront]将返回[!UICONTROL Maximum stores reached]错误。
>
>有关详细信息，请参阅本文中的[最大存储达到错误](#maximum-stores-reached-error)。

1. 登录到您的[!DNL Workfront Fusion]帐户。
1. 在左侧导航面板中单击&#x200B;**[!UICONTROL Data stores]**。
1. 单击屏幕右上角的&#x200B;**[!UICONTROL Add data store]**。
1. 输入新数据存储的设置。

   [!DNL Workfront Fusion]模块中字段的粗体标题表示必需的设置。

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data store name] </td> 
      <td> <p>输入数据存储的名称。 </p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Data Structure]</p> </td> 
      <td> <p>数据结构是表的列的列表。 此列表指示列名和数据类型。</p> <p>执行下列操作之一：</p> 
       <ul> 
        <li><b>选择已创建的数据结构</b></li> 
        <li><b>添加新数据结构</b> <p>单击<strong>[!UICONTROL Add]</strong>以创建新的数据结构。</p> <p>有关详细信息，请参阅本文中的<a href="#set-up-the-data-structure" class="MCXref xref">设置数据结构</a>部分。</p> </li> 
        <li style="font-weight: bold;"> <p>将此字段留空</p> <p style="font-weight: normal;">如果不选择或添加数据结构，则数据库将仅包含主键。 如果您只想保存密钥，并且只想知道数据库中是否存在特定密钥，则此类数据库类型很有用。</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>数据存储大小(MB)</td> 
      <td> <p>从内部数据存储总量中分配数据存储的大小。</p> <p> 默认值为10 MB。 如果您未分配的数据存储空间少于10 MB（分配给95 MB的空间），则默认大小为未分配的存储量。  <p>注：保留金额可以随时更改。</p>  </td> 
     </tr> 
    </tbody> 
   </table>

### 设置数据结构

1. 创建或编辑数据存储时，单击&#x200B;**[!UICONTROL Add]**。
1. 在显示的&#x200B;**[!UICONTROL Add data structure]**&#x200B;框中，配置以下字段：

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data structure name]</td> 
      <td> <p> 输入新数据结构的名称。</p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Specification]</p> </td> 
      <td> <p>执行以下操作之一来设置数据存储列。</p> 
       <ul> 
        <li> <p>单击<strong>[!UICONTROL Add item]</strong>以手动指定一列的属性。</p> <p>输入数据存储列的<strong>[!UICONTROL Name]</strong>和<strong>[!UICONTROL Type]</strong>并定义相应的属性。</p> </li> 
        <li> <p>单击<strong>[!UICONTROL Generator]</strong>以根据您提供的示例数据确定列。</p> 
         <div class="example" data-mc-autonum="<b>Example: </b>">
          <span class="autonumber"><span><b>示例： </b></span></span> 
          <p>例如，以下JSON示例数据创建三列：姓名、年龄和电话号码。 电话号码是手机和固定电话号码的集合。</p> 
          <p><code>&lbrace;</code> </p> 
          <p><code>"name":"John",</code> </p> 
          <p><code>"age":30,</code> </p> 
          <p><code>"phone number": &lbrace;</code> </p> 
          <p><code>"mobile":"987654321",</code> </p> 
          <p><code>"landline":"123456789"</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p>数据存储视图中的空列：</p> 
          <p> <img src="assets/empty-columns-350x132.png" style="width: 350;height: 132;"> </p> 
          <p>您可以手动或使用[!DNL Workfront Fusion]数据存储模块向数据存储添加值。</p> 
         </div> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Strict] </td> 
      <td> <p>启用此选项以确保有效负载与数据结构匹配。 包含未在数据结构中指定的额外项的有效负载将被拒绝。</p> </td> 
     </tr> 
    </tbody> 
   </table>

## 编辑现有数据存储

您可以在[!DNL Workfront Fusion]的[!UICONTROL Data stores]区域中编辑现有数据存储的属性和内容。

* [编辑数据存储的属性](#edit-the-properties-of-a-data-store)
* [编辑数据存储的内容](#edit-the-contents-of-a-data-store)

### 编辑数据存储的属性

数据存储的属性包括数据存储使用的数据结构以及数据存储的大小。

1. 在左侧导航面板中单击&#x200B;**[!UICONTROL Data stores]** ![](assets/data-store-icon.png)以打开[!UICONTROL Data stores]区域。
1. 单击要编辑的数据存储旁边的&#x200B;**[!UICONTROL Edit]** ![](assets/data-store-edit.png)。
1. （可选）如果要将此数据存储使用的数据结构更改为其他现有数据结构，请从&#x200B;**[!UICONTROL Data structure]**&#x200B;下拉列表中选择它。

   或

   （可选）如果要将此数据存储使用的数据结构更改为全新的数据结构，请参阅本文中的[设置数据结构](#set-up-the-data-structure)。

1. （可选）通过在&#x200B;**[!UICONTROL Data storage size in MB]**&#x200B;字段中输入新大小来更改数据存储的大小。
1. 单击 **[!UICONTROL Save]**。

### 编辑数据存储的内容

1. 单击左侧导航面板中的&#x200B;**[!UICONTROL Data Store]**&#x200B;图标![](assets/data-store-icon.png)以打开[!UICONTROL Data Store]区域。
1. 单击要编辑的数据存储旁边的&#x200B;**[!UICONTROL Browse]**。
1. （可选）通过将列拖动到所需位置来重新排列列。
1. （可选）单击单个单元格中的&#x200B;**[!UICONTROL Edit]**&#x200B;图标，然后输入所需的值，从而对该单元格执行[!UICONTROL Edit]操作。
1. （可选）通过单击&#x200B;**[!UICONTROL Add]**&#x200B;向数据存储添加新项，然后输入新项的信息。
1. 单击 **[!UICONTROL Save]**。

## 故障排除

* [从数据存储中恢复丢失的数据](#restoring-lost-data-from-a-data-store)
* [空间不足错误](#out-of-space-error)
* [已达到最大存储数错误](#maximum-stores-reached-error)

### 从数据存储中恢复丢失的数据

目前没有可以自动恢复丢失数据的工具。

#### 解决方法

1. 检查将项目插入数据存储的所有方案的执行日志。

   有关检查执行日志的详细信息，请参阅[查看方案的执行历史记录](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md)。

1. 复制数据。
1. 再次将数据插入数据存储。

   有关将数据插入数据存储的信息，请参阅本文中的[编辑数据存储的内容](#edit-the-contents-of-a-data-store)。

### [!UICONTROL Out of space]错误

发生[!UICONTROL Out of Space]错误，因为先前创建的数据存储已分配给您分配的数据存储存储。

#### 解决方法

1. 编辑任何现有数据存储以使用更少的空间。 这样可释放空间给您的新数据存储。

   有关详细信息，请参阅本文中的[编辑数据存储的属性](#edit-the-properties-of-a-data-store)。

>[!NOTE]
>
>我们建议您不要将所有空间分配给单个数据存储，除非您确定不需要更多数据存储。

### [!UICONTROL Maximum stores reached]错误

发生[!UICONTROL Maximum stores reached]错误，因为您的组织已使用其所有可用数据存储。

#### 解决方法

要减少现有数据存储的数量，请考虑执行以下操作之一：

* 合并现有数据存储
* 删除未使用的数据存储
