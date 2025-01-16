---
title: Marketo模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用 [!DNL Marketo]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1740'
ht-degree: 0%

---

# [!DNL Marketo]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Marketo]的工作流，并将其连接到多个第三方应用程序和服务。

有关Marketo连接器的视频介绍，请参阅：

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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

要使用[!DNL Marketo]模块，您必须具有[!DNL Marketo]帐户。

## Marketo API信息

Marketo连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Marketo]连接到Workfront Fusion {#connect-marketo-to-workfront-fusion}

您可以直接从[!DNL Marketo]模块内部创建与[!DNL Marketo]帐户的连接。

1. 在任意[!DNL Marketo]模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 输入您的[!DNL Marketo]帐户或[!DNL Marketo] [!UICONTROL Munchkin] ID。 这是分配给您帐户的基本URL或终结点的唯一部分，您使用它通过其[!UICONTROL REST] API访问[!DNL Marketo]。 有关查找此内容的说明，请参阅[!DNL Marketo]文档中的[基本URL](https://developers.marketo.com/rest-api/base-url/)。
1. 输入您的[!UICONTROL Client ID]和[!UICONTROL Client secret]。 有关查找这些对象的说明，请参阅[!DNL Marketo]文档中的[身份验证](https://developers.marketo.com/rest-api/authentication/)。
1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。

## [!DNL Marketo]模块及其字段

配置[!DNL Marketo]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Marketo]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

* [[!UICONTROL Watch events (Instant)]](#watch-events-instant)
* [[!UICONTROL Watch records]](#watch-records)

#### [!UICONTROL Watch events (Instant)]

此触发器模块会在创建或更新记录时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>输入您希望模块使用的webhook。</p> <p>有关Webhook的更多信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<!--<a href="For instructions, see [Instant triggers (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->" class="MCXref xref"&gt;即时触发器(Webhook)。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch records]

此触发器模块会在创建或更新记录时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要创建的记录类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Activity]</strong> </p> <p>选择要监视的活动类型。 </p> <p>模块仅监视新活动。<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>选择是否要监视新记录、更新的记录、新记录和更新的记录或特定字段更新。 如果选择监视特定字段更新，请选择要模块监视的字段。</p> </li> 
     <li> <p><strong>[!UICONTROL Program]</strong> </p> <p>选择是要监视新记录、更新的记录，还是同时监视新记录和更新的记录。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Add Leads to a List]](#add-leads-to-a-list)
* [[!UICONTROL Clone a Program]](#clone-a-program)
* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Custom API call]](#custom-api-call)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Remove Leads from a List]](#remove-leads-from-a-list)
* [[!UICONTROL Schedule a Campaign]](#schedule-a-campaign)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Upload a File]](#upload-a-file)

#### [!UICONTROL Add Leads to a List]

此操作模块通过使用潜在客户ID向列表添加一个或多个潜在客户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>输入或映射要添加潜在客户的列表的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>对于要添加到列表中的每个商机，单击<b>[!UICONTROL Add]</b>，然后输入或映射要添加的商机的ID。 您最多可以为模块添加300个潜在客户以添加到列表中。</p> <p>单击映射切换可映射要添加到列表中的现有潜在客户集合。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clone a Program]

此操作模块使用现有项目的ID制作项目副本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Existing Program ID]</td> 
   <td>输入或映射要复制的程序的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New Program Name]</p> </td> 
   <td> <p>输入或映射新项目的名称</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>输入或映射要放置新程序的文件夹的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a record]

此操作模块在[!DNL Marketo]中创建新记录

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要创建的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Folder]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>如果要创建公司或销售线索，请选择要在创建新记录时为其设置值的字段，然后输入这些字段的值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Type]</td> 
   <td>如果要创建程序，请选择要创建的程序类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Channel] </td> 
   <td>如果要创建项目，请选择要创建项目的项目频道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Program Name]</td> 
   <td>如果要创建文件夹或程序，请输入或映射新记录的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>如果要创建文件夹或程序，请输入或映射新记录的说明。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID]</td> 
   <td>如果要创建文件夹或程序，请输入或映射要创建新记录的父文件夹的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>如果要创建项目，请添加任何成本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>如果要创建项目，请添加任意标记</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API call]

此操作模块允许您对[!DNL Marketo] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Marketo]模块无法实现的数据流自动化。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code>https://{your-base-url}.mktorest.com/</code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] 为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块使用的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

此操作模块使用文件ID下载文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>映射要下载的文件的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

此操作模块使用记录的ID读取有关记录的信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要创建的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaign]</p> </li> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL List]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>选择要包含在此模块的输出捆绑包中的信息。 基于您选择的[!UICONTROL Record Type]字段可用。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL <Object> ID]</td> 
   <td>输入或映射要检索相关信息的对象的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Leads from a List]

此操作模块使用潜在客户ID从列表中删除一个或多个潜在客户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>输入或映射要删除潜在客户的列表的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>对于要从列表中删除的每个商机，单击<b>[!UICONTROL Add]</b>，然后输入或映射要删除的商机的ID。 您最多可以为模块添加300个要从列表中删除的销售机会。 </p> <p>单击映射切换可映射要从列表中删除的现有潜在客户集合。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Schedule a Campaign]

此操作模块可计划特定日期的现有营销活动。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>输入或映射要计划的营销活动的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Schedule for Date]</p> </td> 
   <td>选择要运行营销活动的日期。 如果此字段留空，则营销活动将在方案开始后5分钟运行。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

此操作模块使用现有记录的ID更新该记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要创建的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Company] / [!UICONTROL Lead] / [!UICONTROL Program ID]</td> 
   <td>输入或映射要更新的记录ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>如果要更新“公司”或“销售线索”，请选择要为其更新值的字段，然后输入这些字段的值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Name]</td> 
   <td>如果要更新程序，请输入或映射程序的新名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>如果要更新程序，请输入或映射程序的新说明。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>如果要更新程序，请输入或映射程序的新开始日期。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>如果要更新项目群，请输入或映射项目群的新结束日期。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>如果要更新项目，请添加任何成本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>如果要更新项目，请添加任意标记</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

此操作模块会将新文件上传到[!UICONTROL Marketo]。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>从上一个模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>输入或映射要放置新文件的文件夹的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>输入已上载文件的说明。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL List records]](#list-records)
* [[!UICONTROL Search Records]](#update-a-record)

#### [!UICONTROL List records]

此操作模块可检索特定类型的所有记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要列出的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL Read all campaigns]</p> </li> 
     <li> <p>[!UICONTROL Read all programs]</p> </li> 
     <li> <p>[!UICONTROL Read all leads] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field]</td> 
   <td>如果已选择检索潜在客户，请选择是要从列表还是从项目群检索潜在客户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>选择要包含在此模块的输出捆绑包中的信息。 基于您选择的[!UICONTROL Record Type]字段可用。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Records]

此搜索模块可检索符合特定搜索条件的记录列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Marketo]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将[!DNL Marketo]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>选择要搜索的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaigns]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programs]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Field]</p> </td> 
   <td> <p>选择您要按名称、项目名称或工作区名称搜索。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td>对于要搜索的每个值，单击<b>[!UICONTROL Add item]</b>并输入值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>
