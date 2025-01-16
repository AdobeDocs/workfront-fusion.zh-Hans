---
title: HubSpot CRM模块
description: 通过 [!DNL Adobe Workfront Fusion] HubSpot CRM模块，您可以监视 [!DNL HubSpot CRM] 帐户中的事件、记录、联系人、预约、文件和表单提交，或者创建、检索、更新和删除记录、联系人、预约、事件或文件。
author: Becky
feature: Workfront Fusion
exl-id: b8a1bbcd-337e-4c92-a1a6-d6d4bab1f440
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '5655'
ht-degree: 0%

---

# [!DNL HubSpot CRM]模块

通过[!DNL Adobe Workfront Fusion] [!DNL HubSpot CRM]模块，您可以监视事件、记录、联系人、预约、文件和表单提交，或者创建、检索、更新和删除您[!DNL HubSpot CRM]帐户中的记录、联系人、预约、事件或文件。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
  <td> <p>[!UICONTROL Pro] 或更高</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
   <td> <p>[!UICONTROL Plan]， [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前许可证要求：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Adobe Workfront]计划，则您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[!UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## 先决条件

要使用[!DNL HubSpot CRM]模块，您必须具有[!DNL HubSpot CRM]帐户。

## HubSpot CRM API信息

HubSpot CRM连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td>https://api.hubapi.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v2.0.14</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Adobe Workfront Fusion]连接到[!DNL HubSpot CRM]

有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅[创建与 [!DNL Adobe Workfront Fusion] 的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>配置连接时，请选择&#x200B;**HubSpot CRM**&#x200B;连接类型。 HubSpot CRM（已弃用）类型支持现有连接，但我们不建议使用它来创建新连接。

## [!DNL HubSpot CRM]模块及其字段

配置[!DNL Hubspot CRM]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Hubspot CRM]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [CRM对象](#crm-objects)
* [记录（交易、联系人和公司）](#records-deals-contacts-and-companies)
* [联系人](#contacts)
* [交易](#deals)
* [公司](#companies)
* [参与](#engagements)
* [事件和通知](#events-and-notifications)
* [文件](#files)
* [任务](#tasks)
* [用户](#users)
* [票证](#tickets)
* [表单](#forms)
* [社交媒体（广播）](#social-media-broadcast)
* [博客帖子](#blog-posts)
  <!--* [Workflows]-->
* [订阅](#subscriptions)
  <!--* [Associations](#associations)-->
* [其他](#other)

+++**CRM对象**

### CRM对象

* [搜索CRM对象](#search-for-crm-objects)
* [监视CRM对象](#watch-crm-objects)

#### [!UICONTROL Search for CRM Objects]

此搜索模块按自定义属性或查询搜索CRM对象。 要搜索产品或行项目，请使用具有所需自定义范围的特殊连接。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射模块在一个执行周期中返回的最大项数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type to Search]</td> 
   <td>选择要搜索的Hubspot CRM对象的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>选择要显示在模块输出中的属性。 可用字段取决于您选择的对象。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by] </td> 
   <td> <p>选择您希望如何筛选搜索</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>输入或映射查询</p> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>输入搜索的组或筛选器。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>如果要对结果进行排序，请单击。 如果选择对结果进行排序，则会显示以下字段。 </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Property name]</strong> </p> <p>选择要按其排序结果的属性</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>选择是否要以升序或降序方向对结果进行排序。</p> </li> 
    </ul> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">起始偏移</td> 
    <td>输入或映射要检索其详细信息的第一个项目的ID。 此模块一次最多只返回5000个结果。 设置起始偏移允许您检索前5000项以外的项目。 如果起始偏移为5000，则模块将返回项目5000-9999。</td> 
   </tr>
 </tbody> 
</table>

#### 监视CRM对象

此触发器模块会在创建或更新CRM对象时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射模块在一个执行周期中返回的最大项数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object type to search]</td> 
   <td> <p>选择要搜索的对象类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>选择要包含在此模块输出中的属性。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created/Updated]</td> 
   <td>选择要监视已创建（新）对象还是已更新（已修改）对象。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by]</td> 
   <td>您可以添加过滤器，以确保仅在满足某些条件时启动方案。<ul><li><b>查询</b><p>输入要作为筛选依据的查询。</li><li><b>属性</b><p>对于要用于筛选结果的每个属性，单击<b>添加项</b>并输入属性名称、运算符和属性值。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**记录（交易、联系人和公司）**

### 记录（交易、联系人和公司）

* [创建记录](#create-a-record)
* [[!UICONTROL Create a Record (Legacy)]](#create-a-record-legacy)
* [[!UICONTROL Delete a Record]](#delete-a-record)
* [[!UICONTROL Get a Record]](#get-a-record)
* [[!UICONTROL Get a Record Property]](#get-a-record-property)
* [列出记录](#list-records)
* [[!UICONTROL Update a Record]](#update-a-record)
* [[!UICONTROL Watch Records]](#watch-records)

#### 创建记录

此操作模块创建联系人、公司或交易。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要创建的记录类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>对于创建记录时要添加的每个属性，选择属性所在的组。 此时将打开资产组，随后您可以填写资产的值。 可用的属性组和属性取决于您要创建的记录类型。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Record (Legacy)]

此操作模块创建联系人、公司或交易。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要创建的记录类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>填写要为记录设置的任何属性。 可用字段取决于您要创建的记录类型。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Record]

此操作模块可删除联系人、公司或交易。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>选择要删除的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入要删除的联系人、公司或交易的ID。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Record]

此操作模块可获取联系人、公司或交易的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择记录类型。</p> 
    <ul> 
     <li>[!UICONTROL Contact]</li> 
     <li>[!UICONTROL Company] </li> 
     <li>[!UICONTROL Deal]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td>如果您正在获取联系人，请选择是要通过ID还是电子邮件地址来识别联系人。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入要检索的联系人、公司或交易的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>输入要检索其详细信息的联系人的电子邮件地址。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Record Property]

此操作模块通过特定记录属性的（内部）名称获取该属性的元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>选择具有您要为其检索元数据的属性的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property Name]</td> 
   <td>选择要为其检索元数据的属性。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Option ID]</td> 
   <td> <p> 某些属性具有一组可用选项，用户可以选择这些选项作为属性值。 输入表示要检索的属性值的选项的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 列出记录

此搜索模块返回联系人、公司或交易的列表。 产量限制为5000个联系人、12,500家公司或12,500项交易。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> <p>选择要返回的记录类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>选择要包含在此模块输出中的属性。</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr>

</tbody> 
</table>

#### [!UICONTROL Update a Record]

此操作模块可更新联系人、公司或交易。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>选择要更新的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search Type]</td> 
   <td> <p>如果您要获得联系人，请选择您希望如何识别记录：</p> 
    <ul> 
     <li> <p>[!UICONTROL ID]</p> </li> 
     <li> <p>[!UICONTROL Email]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入要更新的联系人、公司或交易的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>输入要更新其详细信息的联系人的电子邮件地址。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>填写要为记录设置的任何属性。 可用字段取决于您要创建的记录类型。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Records]

此触发器模块会在联系人、公司或交易在过去30天内被修改或创建时启动场景。 输出限制为10,000条记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>选择具有要监视的属性的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>选择您要监视最近修改的记录还是最近创建的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>选择要包含在模块输出中的属性。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**联系人**

### 联系人

* [[!UICONTROL Add Contacts to a List]](#add-contacts-to-a-list)
* [创建/更新联系人](#createupdate-a-contact)
* [[!UICONTROL Create/Update a Contact (Legacy)]](#createupdate-a-contact-legacy)
* [[!UICONTROL Create/Update a Group of Contacts]](#createupdate-a-group-of-contacts)
* [[!UICONTROL List Contacts]](#list-contacts)
* [[!UICONTROL List Contacts of a Company]](#list-contacts-of-a-company)
* [[!UICONTROL Merge contacts]](#merge-contacts)
* [[!UICONTROL Remove a Contact from a List]](#remove-a-contact-from-a-list)
* [[!UICONTROL Search for Contacts]](#search-for-contacts)
* [监视添加到列表中的联系人](#watch-contacts-added-to-a-list)

#### [!UICONTROL Add Contacts to a List]

此模块将系统中已创建的联系人记录添加到联系人列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>选择要向其添加联系人的列表的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IDs/Emails] </td> 
   <td> <p>选择您希望如何识别要添加到列表中的联系人：</p> 
    <ul> 
     <li> <p>[!UICONTROL IDs]</p> <p>添加要添加到列表中的联系人的ID。</p> </li> 
     <li> <p>[!UICONTROL Emails]</p> <p>添加要添加到列表中的联系人的电子邮件地址。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 创建/更新联系人

如果门户中不存在联系人，此操作模块将创建联系人。 如果门户中确实存在联系人，则此模块会使用提供的值更新该联系人。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Property groups]</td> 
   <td>对于创建联系人时要添加的每个属性，选择属性所在的组。 此时将打开资产组，随后您可以填写资产的值。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Contact (Legacy)]

如果门户中不存在联系人，则创建联系人；如果门户中不存在联系人，则使用最新属性值更新联系人。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Properties]</td> 
   <td>填写您要为联系人设置或更新的任何属性。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create/Update a Group of Contacts]

创建联系人组或更新他们（如果已经存在）。 当批次大小限制为100个或更少联系人时，性能最佳。 通过此端点进行的更改是异步处理的，因此可能需要几分钟才能将更改应用到联系人记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Batch of Contacts to Create/Update] </td> 
   <td> <p>添加联系人批次。</p> <p>单击<strong>[!UICONTROL Add item]</strong>以添加新联系人。 在出现的窗口中，输入或映射以下信息：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search Type]</strong> </p> <p>选择您希望如何识别联系人：</p> 
      <ul> 
       <li> <p>[!UICONTROL ID]</p> <p>输入要创建或更新的联系人的ID。 </p> </li> 
       <li> <p>[!UICONTROL Email]</p> <p>输入要创建或更新的联系人的电子邮件地址。 </p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Properties]</strong> </p> <p>填写您要为联系人设置或更新的任何属性。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Contacts]

返回在门户中创建的所有联系人。 输出限制为5000个联系人。 要列出上一个或下一个联系人，您可以使用[!UICONTROL advanced]参数偏移列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>在一个方案执行周期内应返回的最大联系人数[!DNL Workfront Fusion]。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>选择要显示在模块输出中的属性。 </td> 
  </tr> 
   <tr> 
    <td role="rowheader">联系人ID [起始偏移] </td> 
    <td>输入或映射要启动列表的用户的ID。 例如，将联系人ID设置为第101位联系人的ID将允许模块列出联系人101-5100，而不是1-5000。 </td> 
   </tr>
 </tbody> 
</table>

#### [!UICONTROL List Contacts of a Company]

检索公司中的联系人列表。 输出限制为5000个联系人。 要列出上一个或下一个联系人，您可以使用[!UICONTROL advanced]参数偏移列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入要列出其联系人的公司的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>在一个方案执行周期内应返回的最大联系人数[!DNL Workfront Fusion]。 </td> 
  </tr> 
   <tr> 
    <td role="rowheader">联系人ID [起始偏移] </td> 
    <td>输入或映射要启动列表的用户的ID。 例如，将联系人ID设置为第101位联系人的ID将允许模块列出联系人101-5100，而不是1-5000。 </td> 
   </tr>
 </tbody> 
</table>

#### [!UICONTROL Merge contacts]

此操作模块合并联系人

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 1] </td> 
   <td>输入要合并的联系人的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID 2] </td> 
   <td>输入要合并的其他联系人的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a Contact from a List]

从联系人列表中删除联系人。

>[!NOTE]
>
>您无法从动态列表中手动删除联系人。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID] </td> 
   <td>选择要从中删除联系人的列表的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID] </td> 
   <td>输入要从列表中删除的联系人的ID。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for Contacts]

使用搜索查询检索联系人列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>输入搜索查询。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>输入或映射在一个方案执行周期内应返回的最大联系人数[!DNL Workfront Fusion]。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch contacts added to a list]

此触发器模块会在向列表添加新联系人后启动方案。 这仅适用于拥有付费营销帐户的用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>输入或映射包含要监视的联系人的列表ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output Properties]</td> 
   <td>选择要包含在模块输出中的属性。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**交易**

### 交易

* [[!UICONTROL Get a Deal's CRM Pipeline]](#get-a-deals-crm-pipeline)
* [[!UICONTROL List Deal/Ticket Pipelines]](#list-dealticket-pipelines)

#### [!UICONTROL Get a Deal's CRM Pipeline]

返回特定的交易管道。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Pipeline ID] </td> 
   <td>输入或映射要检索其详细信息的管道ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stage ID] </td> 
   <td>输入或映射要检索其详细信息的阶段的ID。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Deal/Ticket Pipelines]

返回给定门户的所有交易和票证管道。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type] </td> 
   <td>选择您要列出交易还是票证。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**公司**

### 公司

#### [!UICONTROL Search for Companies by domain]

根据与域属性的完全匹配检索公司列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Domain] </td> 
   <td>输入要搜索公司的域，如<code>[!DNL hubspot].com</code>。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>在一个方案执行周期内应返回的最大公司数[!DNL Workfront Fusion]。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output properties]</td> 
   <td>选择要显示在模块输出中的属性。 </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**参与**

### 参与

* [将参与与CRM对象关联](#associate-an-engagement-with-a-crm-object)
* [创建参与](#create-an-engagement)
* [删除参与](#delete-an-engagement)
* [Watch参与](#watch-engagements)

#### 将参与与CRM对象关联

此操作模块将项目与联系人、公司或交易相关联。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>选择要与项目关联的CRM记录的类型。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Engagement ID]</td> 
  <td>输入或映射要与对象关联的预订的ID。</td> 
   </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
  <td>输入或映射要与预订关联的记录的ID。</td> 
   </tr> 
 </tbody> 
</table>

#### 创建参与

此操作模块在HubSpot中创建具有CRM对象的参与（如注释、任务或活动）。 预订是与应记录在CRM中的联系人的任何交互。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Is Active?]</td> 
   <td>如果新预订将在创建时处于活动状态，则启用此选项。 预订必须处于活动状态才能显示在时间线中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
  <td>选择要创建的参与度类型。
  <ul>
  <li><b>电子邮件</b><p></p>继续<a href="#email-metadata" class="MCXref xref" >电子邮件元数据</a>。</p></li>
  <li><b>调用</b><p>继续<a href="#call-metadata" class="MCXref xref" >调用元数据</a>。</p></li>
  <li><b>会议</b><p>继续<a href="#meeting-fields" class="MCXref xref" >会议字段</a>。</p></li>
  <li><b>任务</b><p>继续<a href="#task-fields" class="MCXref xref" >任务字段</a>。</p></li>
  <li><b>注释</b><p>在正文字段中，输入注释的文本。</p></li>
  </ul>
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">时间戳</td> 
   <td>输入或映射参与的时间戳。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">所有者 ID</td> 
   <td>输入或映射预订将分配到的人员的所有者ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UID</td> 
   <td>输入或映射项目的ID，该ID可用于各种对象类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">门户ID</td> 
   <td>输入或映射门户的ID。 如果您的组织有多个门户，则此功能非常有用。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">关联的联系人</td> 
   <td>对于要与此预订关联的每个联系人，单击<b>添加项目</b>并输入联系人ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">关联公司</td> 
   <td>对于要与此预订关联的每个公司，单击<b>添加项目</b>并输入公司ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">关联交易</td> 
   <td>对于要与此预订关联的每个交易，单击<b>添加项目</b>并输入交易ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">关联的票证</td> 
   <td>对于要与此预订关联的每个票证，单击<b>添加项目</b>并输入票证ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">附件</td> 
   <td>对于要与此预订关联的每个附件，单击<b>添加项目</b>，然后输入要附加的文件的文件ID。</td> 
  </tr> 
 </tbody> 
</table>

##### 电子邮件元数据

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL From > Email]</p> </td> 
   <td> <p>输入或映射发送电子邮件的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL First Name]</td> 
   <td>输入或映射发送电子邮件的人员的名字。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Last Name]</td> 
  <td>输入或映射发送电子邮件的人员的姓氏。
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">到</td> 
   <td>对于要向其发送电子邮件的每个电子邮件地址，单击<b>添加项</b>，然后输入或映射电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">抄送</td> 
   <td>对于要抄送电子邮件的每个电子邮件地址，单击<b>添加项</b>，然后输入或映射电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">密件抄送</td> 
   <td>对于要密件抄送电子邮件的每个电子邮件地址，单击<b>添加项</b>并输入或映射电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">主题</td> 
   <td>输入或映射电子邮件主题的文本</td> 
  </tr> 
  <tr> 
   <td role="rowheader">HTML</td> 
   <td>要发送HTML格式的电子邮件，请输入或映射电子邮件的正文，包括HTML标签。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">文本</td> 
   <td>要发送纯文本电子邮件，请输入或映射电子邮件正文的文本。</td> 
  </tr> 
 </tbody> 
</table>

##### 调用元数据

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL To Number]</p> </td> 
   <td> <p>输入或映射将向其进行呼叫的电话号码。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From Number]</td> 
   <td>输入或映射进行呼叫的电话号码。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
  <td>选择呼叫的状态。
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">正文</td> 
   <td>输入或映射呼叫的详细信息或备注。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">外部 ID</td> 
   <td>此字段表示在HubSpot中进行的调用的内部ID。 无需采取任何操作。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">持续时间</td> 
   <td>输入或映射调用的长度（以毫秒为单位）</td> 
  </tr> 
  <tr> 
   <td role="rowheader">外部帐户ID</td> 
   <td>此字段表示在HubSpot中进行的调用的内部帐户ID。 无需采取任何操作。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">录制URL</td> 
   <td>输入或映射录制文件的URL。</td> 
  </tr> 
 </tbody> 
</table>

##### 会议字段

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Title]</p> </td> 
   <td> <p>输入或映射会议的标题或主题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>输入或映射会议描述或详细信息的文本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Time]</td> 
  <td>输入或映射会议的开始时间作为UNIX时间戳。
  </td> 
   </tr> 
  <tr> 
   <td role="rowheader">结束时间</td> 
   <td>输入会议结束时间或将会议结束时间映射为UNIX时间戳。</td> 
  </tr> 
 </tbody> 
</table>

##### 任务字段

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Subject]</p> </td> 
   <td> <p>输入或映射任务的标题或主题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>输入或映射任务说明或详细信息的文本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">状态</td> 
   <td>选择任务的状态。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL For Object Type]</td> 
  <td>输入<code>CONTACT</code>或<code>COMPANY</code>。
  </td> 
   </tr> 
 </tbody> 
</table>

#### 删除参与

此操作模块按其ID删除参与。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>输入或映射要删除的参与的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### Watch参与

此触发器模块会在门户中创建新参与时启动方案。 此模块仅返回在过去30天内创建的记录，或最近创建的10,000条记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>在一个方案执行周期内应返回的最大公司数[!DNL Workfront Fusion]。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Since]</td> 
   <td>输入或映射要监视事件的最早日期。 使用格式<code>MM/DD/YYYY h:mm</code>。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**事件和通知**

### 事件和通知

* [创建/更新时间线事件](#create--update-a-timeline-event)
* [列出时间线事件类型](#list-timeline-event-types)
* [观看日历事件](#watch-calendar-events)
* [Watch通知](#watch-notifications)

#### 创建/更新时间线事件

此操作模块创建或更新时间线事件。 此模块只能与包括用户标识符、HubSpot API密钥、客户端ID和客户端密钥的开发人员连接一起使用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>输入或映射此事件所属的应用程序ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td>输入或映射此事件的ID。 事件ID不是由系统生成的。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Type ID]</td> 
   <td>输入或映射此事件事件类型的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>输入或映射要为其创建事件的联系人的电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object ID]</td> 
   <td>输入或映射要为其创建事件的联系人的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp]</td> 
   <td>输入或映射此事件的时间戳。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom data]</td> 
   <td>对于要添加到此事件的每个自定义数据项，单击<b>添加项</b>并输入该项的名称和值。</td> 
  </tr> 
 </tbody> 
</table>

#### 列出时间线事件类型

此搜索模块返回特定应用程序的所有时间线事件的列表。 此模块只能与包括用户标识符、HubSpot API密钥、客户端ID和客户端密钥的开发人员连接一起使用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>输入或映射此事件所属的应用程序ID。 </td> 
  </tr> 
 </tbody> 
</table>

#### 观看日历事件

此触发器模块会在向日历添加新事件时启动方案。 在开始日期和结束日期之间的时间间隔内，最多可包含500个任务。 此模块只能与包括用户标识符、HubSpot API密钥、客户端ID和客户端密钥的开发人员连接一起使用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Events Type]</td> 
   <td>选择您要观看社交活动、内容活动还是所有活动。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大文件数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>输入或映射开始日期。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>输入或映射结束日期。</td> 
  </tr> 
 </tbody> 
</table>

#### Watch通知

此触发器模块会在发送有关更改的新通知时启动方案。  在开始日期和结束日期之间的时间间隔内，最多可包含500个任务。 此模块只能与包括用户标识符、HubSpot API密钥、客户端ID和客户端密钥的开发人员连接一起使用。 在HubSpot中，每个开发人员应用程序只能有一个webhook URL。

要为此模块创建webhook，请单击webhook字段旁边的&#x200B;**添加**&#x200B;并填写以下字段：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application ID]</td> 
   <td>输入要用于此webhook的应用程序ID。 您可以在HubSpot开发人员门户中找到该ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscriptions]</td> 
   <td> <p>对于要监视的每种通知类型，单击<b>添加项目</b>并选择订阅类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Force to Remove Old Subscriptions]</td> 
   <td>启用此选项可分离或删除附加到此webhook的旧订阅。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**文件**

### 文件

* [[!UICONTROL Create a Folder]](#create-a-folder)
* [删除文件](#delete-a-file)
* [[!UICONTROL Delete a Folder]](#delete-a-folder)
* [列出文件](#list-files)
* [[!UICONTROL Move a File]](#move-a-file)
* [上传文件](#upload-a-file)
* [监视文件](#watch-files)

#### [!UICONTROL Create a Folder]

此模块创建一个文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder Name] </td> 
   <td>输入或映射新文件夹的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID] </td> 
   <td>为要创建的文件夹选择父文件夹的ID。 </td> 
  </tr> 
 </tbody> 
</table>

#### 删除文件

此操作模块会从文件管理器中永久删除文件以及所有相关数据和缩略图。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>输入或映射要删除的文件的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Folder]

将文件夹标记为已删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射要删除的文件夹的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 列出文件

此搜索模块返回存储在文件管理器中的文件列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大文件数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>输入或映射包含要列出文件的文件夹的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>要仅包含文件名中包含特定字符的文件，请输入或映射希望文件名包含的字符。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File]

将文件移动到其他文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID] </td> 
   <td>输入或映射要移动的文件的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>选择要将文件移动到的文件夹的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>输入已移动文件的名称。</td> 
  </tr> 
 </tbody> 
</table>

#### 上传文件

此操作模块会将文件上传到文件管理器。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Access type] </td> 
   <td>选择您希望文件是私有文件、公共文件但不可索引文件，还是公共文件且可索引文件。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID] </td> 
   <td>选择要上载文件的文件夹的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Overwrite]</td> 
   <td>启用此选项以覆盖文件夹中已存在的文件。</td> 
  </tr> 
 </tbody> 
</table>

### 监视文件

在将新文件保存到文件管理器时，此触发器模块会启动一个方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大文件数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>输入或映射包含要监视的文件的文件夹的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>要仅包含文件名中包含特定字符的文件，请输入或映射希望文件名包含的字符。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**任务**

### 任务

* [创建日历任务](#create-a-calendar-task)
* [删除日历任务](#create-a-calendar-task)
* [观看任务事件](#watch-task-events)

#### 创建日历任务

此操作模块为日历创建新任务。 此模块中使用的连接必须使用具有付费营销帐户的用户的凭据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>输入或映射新日历任务的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>输入或映射新日历任务的说明。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td>输入或映射分配给此任务的用户的所有者ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Date]</td> 
   <td>输入或映射此任务的日期。<p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Category]</td> 
   <td>选择事件类型。<ul><li><b>博客帖子</b><p>输入内容组ID。 这是博客页面的ID。</p></li><li><b>电子邮件</b><p>输入或映射要使用的电子邮件模板的路径。</li><li><b>登陆页面</b><p>输入或映射要使用的登陆页面模板的路径。</li><li><b>自定义</b></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td>输入事件处于“待办事项”还是“已完成”状态。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign GUID]</td> 
   <td>输入或映射此事件所属的营销活动的内部HubSpot ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 删除日历任务

此操作模块删除日历任务。 此模块中使用的连接必须使用具有付费营销帐户的用户的凭据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射要删除的任务的标识号。</td> 
  </tr> 
 </tbody> 
</table>

#### 观看任务事件

此触发器模块在日历中有新任务事件时启动方案。 此模块中使用的连接必须使用具有付费营销帐户的用户的凭据。 模块最多返回500个事件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大文件数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>输入或映射要监视事件的最早日期。 使用格式<code>MM/DD/YYYY h:mm</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>输入或映射您要观看活动的最新日期。 使用格式<code>MM/DD/YYYY h:mm</code>。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**用户**

### 用户

* [获取所有者](#get-an-owner)
* [列表所有者](#list-owners)

#### 获取所有者

此操作模块返回所有者的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Owner ID]</td> 
   <td> <p>输入或映射要为其返回详细信息的所有者的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 列表所有者

此搜索模块返回HubSpot帐户中所有所有者的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**票证**

### 票证

<!--* [Create a Ticket]-->
* [删除票证](#delete-a-ticket)
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->
  <!--* [Create a Ticket]-->

<!-- Create a Ticket Need to find a working connection-->

#### [!UICONTROL Delete a Ticket]

按票证ID删除现有票证。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入要删除的票证ID。 </td> 
  </tr> 
 </tbody> 
</table>

<!-- Get a Ticket  Need to find a working connection-->

<!-- List Tickets  Need to find a working connection-->

&lt;！ — 更新票证需要找到有效连接 — >

<!-- Watch Tickets Need to find a working connection-->

+++

+++**Forms**

### 表单

* [通过表单上传文件](#get-a-file-uploaded-via-form)
* [列出Forms](#list-forms)
  <!--* [Submit Data to a Form]-->
  <!--* [Watch Submissions for a Form]-->

#### 通过表单上传文件

此操作模块会返回通过表单上传的文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File URL]</td> 
   <td>输入或映射要检索的文件的URL。 这可以在表单元数据中找到。</td> 
  </tr> 
 </tbody> 
</table>

#### 列出Forms

此操作模块返回在与用于此模块的连接关联的帐户中创建的所有表单。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射模块在一个执行周期中返回的最大表单数。</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Submit Data to a Form Need to find a working connection-->



&lt;！—####观察表单提交情况 — 需要找到有效连接>—>

+++

+++**社交媒体（广播）**

### 社交媒体（广播）

* [取消广播消息](#cancel-a-broadcast-message)
* [创建广播消息](#create-a-broadcast-message)
* [观看广播消息](#watch-broadcast-messages)

#### 取消广播消息

此操作模块可取消计划的广播，例如推文或Facebook帖子。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>输入或映射要取消的广播的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 创建广播消息

此操作模块会在指定的社交媒体渠道上创建消息并立即发布消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel ID]</td> 
   <td>输入或映射要用于此广播的频道ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Title]</td> 
   <td>输入或映射此广播的标题。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>输入或映射广播的文本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Photo URL]</td> 
   <td>输入或映射要包含在广播中的照片的URL。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Thumbnail URL]</td> 
   <td>输入或映射要用于此广播的缩略图URL。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Trigger at]</td> 
   <td>输入或映射您希望发送广播的日期和时间。 如果将其留空，则会立即发送广播。<p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p></td> 
  </tr> 
 </tbody> 
</table>

#### 观看广播消息

当消息从HubSpot发布到指定的社交媒体渠道时，此触发器模块会启动一个方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射模块在一个执行周期中返回的最大项数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Status]</td> 
   <td>要仅在消息处于特定状态时启动方案，请选择状态。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by Channel]</td> 
   <td>要仅在消息位于特定渠道上时启动方案，请选择该渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Broadcast ID]</td> 
   <td>要仅在消息处于特定日期或特定日期之后启动方案，请以<code>MM/DD/YYYY</code>格式输入或映射日期。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++**博客帖子**

### 博客帖子

<!--* [Create a Blog Post]-->
* [删除博客帖子](#delete-a-blog-post)
  <!--* [List Blog Posts]-->
* [Publish/取消发布博客帖子](#publish--unpublish-a-blog-post)
  <!--* [Watch Blog Posts]-->

<!--
#### Create a Blog Post May need connection
-->


#### 删除博客帖子

此操作模块删除单个博客帖子。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射要删除的博客帖子的ID。</td> 
  </tr> 
 </tbody> 
</table>

<!--#### List Blog Posts May need connection

This search module retrieves posts from a HubSpot blog.-->

#### Publish /取消发布博客帖子

此操作模块可计划或取消博客帖子的发布。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射要计划或取消的博客帖子的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td>选择是要计划博客帖子，还是取消以前计划的博客帖子。</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Watch Blog PostsMay need connection-->

+++

<!--+++**Workflows**>

<!--### Workflows May need connection

#### Add a Contact to a Workflow


#### Remove a Contact from a Workflow

-->

<!--+++-->

+++**订阅**

### 订阅

* [更新电子邮件订阅](#update-email-subscription)
* [Watch门户的订阅时间表](#watch-subscriptions-timeline-for-a-portal)

#### 更新电子邮件订阅

此操作模块可更新HubSpot中的电子邮件订阅。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email]</td> 
   <td>输入或映射要更新的订阅的电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Statuses]</td> 
   <td>对于要更新订阅的每个状态，单击<b>添加项目</b>并输入该状态的ID以及电子邮件地址是否会订阅该状态。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Status]</td> 
   <td>要记录此订阅的GDPR法律依据，请选择此订阅的法律状态。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Portal Subscription Legal Basis Explanation]</td> 
   <td>要添加有关此订阅GDPR的法律基础的注释，请输入或映射注释的文本。</td> 
  </tr> 
 </tbody> 
</table>

#### Watch门户的订阅时间表

在将新的电子邮件时间线订阅添加到门户后，此触发器模块将启动一个方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射模块在一个执行周期中返回的最大项数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Timestamp]</td> 
   <td>要在特定日期或之后返回结果，请以格式输入日期 <code>MM/DD/YYYY.</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Timestamp]</td> 
   <td>要在特定日期或之前返回结果，请以格式输入日期 <code>MM/DD/YYYY.</code></td> 
  </tr> 
 </tbody> 
</table>

+++

<!--+++**Associations**-->

<!--### Associations-->

<!--#### Associate CRM Objects  May need connection

This action module associates two CRM objects.-->

<!--#### Associate Multiple CRM Objects  May need connection-->



<!--#### Delete an Association May need connection-->



<!--#### Delete Multiple Associations between CRM Objects May need connection-->



<!--#### List Associations for a CRM Object May need connection-->

<!--+++-->

+++**其他**

### 其他

#### [!UICONTROL Make an API Call]

允许您执行自定义API调用。

>[!NOTE]
>
>以下端点已于2023年8月31日在HubSpot API中弃用，并且在Fusion模块中无法再使用。
>
>* 列出内容事件
>* 列出社交事件
>* 列出日历任务事件
>* 列出所有日历事件
>* 创建日历任务
>* 按ID获取日历任务
>* 更新日历任务
>* 删除日历任务

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL HubSpot CRM]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>输入相对于https://api.hubapi.com/的路径。 例如， /contacts/v1/lists/all/contacts/all</p> <p>有关可用端点的列表，请参阅<a href="https://legacydocs.hubspot.com/docs/overview">[!DNL HubSpot] API文档</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>选择要使用的HTTP方法：</p> <p>[!UICONTROL GET]</p> <p>检索条目的信息。</p> <p>[!UICONTROL POST]</p> <p>以创建新条目。</p> <p>[!UICONTROL PUT]</p> <p>更新/替换现有条目。</p> <p>[!UICONTROL PATCH]</p> <p>更新部分条目。</p> <p>[!UICONTROL DELETE]</p> <p>以删除条目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p> 输入所需的请求标头。 您无需添加授权标头；我们已经为您添加了这些标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> 输入请求查询字符串。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。<img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**示例：**&#x200B;以下API调用返回您[!DNL HubSpot]帐户中的所有联系人：
>
>**URL**： `/contacts/v1/lists/all/contacts/all`
>
>**方法**： `GET`
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-config.png)
>
>在[!UICONTROL Bundle] > [!UICONTROL Body] > [!UICONTROL contacts]下的模块输出中可以找到搜索匹配项。
>
>在我们的示例中，返回了3个联系人：
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/hubspot-api-output.png)

+++

## 创建新应用程序

1. 登录到您的[!DNL HubSpot]开发人员帐户。
1. 选择&#x200B;**[!UICONTROL Create an App]**&#x200B;选项。
1. 输入应用程序名称并[!UICONTROL Save]对话框。
1. 选择webhook所需的范围。

   例如，添加联系人范围，以便在创建或删除新联系人时触发模块。

   [!UICONTROL contacts scope]是您接收联系人、交易和公司活动Webhook所需的一切。

   >[!IMPORTANT]
   >
   >请勿填写[!UICONTROL Redirect URL]字段。
