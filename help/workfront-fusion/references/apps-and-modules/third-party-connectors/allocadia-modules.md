---
title: 分配模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Allocadia的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 9a6fccd6-6eee-42dc-a678-c1f34280d139
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# [!DNL Allocadia]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Allocadia]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL Allocadia]模块，您必须具有[!DNL Allocadia]帐户。

## [!DNL Allocadia] API信息

Allocadia连接器使用以下对象：

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
   <td>v1.7.6</td> 
  </tr>
 </tbody> 
</table>

## 将[!DNL Allocadia]连接到[!DNL Workfront Fusion]

您可以直接从[!DNL Allocadia]模块内部创建与[!DNL Allocadia]帐户的连接。

1. 在任意[!DNL Allocadia]模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 选择您要使用北美服务器还是欧洲服务器。
1. 输入您的用户名和密码。
1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。

## [!DNL Allocadia]模块及其字段

配置[!DNL Allocadia]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Allocadia]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!UICONTROL Watch Record]

此触发器模块执行特定类型的对象添加、更新或同时添加和更新的方案。 该模块返回与一个或多个记录关联的所有标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> <table style="table-layout:auto"> <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将Allocadia帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect Allocadia]到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">筛选条件</td> 
   <td> <p>选择您希望方案仅观看“新记录”、[!UICONTROL Updated Records Only]还是“新记录和更新的记录”。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">实体类型</td> 
   <td>选择要模块监视的Allocadia记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出</td> 
   <td> <p>选择要包含在模块输出中的字段。 可用字段取决于您选择的实体类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">限制</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中监视的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [自定义API调用](#custom-api-call)
* [读取记录](#read-record)
* [创建记录](#create-record)
* [删除记录](#delete-record)
* [更新记录](#update-record)

#### [!UICONTROL Custom API Call]

此操作模块允许您对[!DNL Allocadia] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Allocadia]模块无法实现的数据流自动化。

该操作基于您指定的图元类型（Allocadia对象类型）。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Allocadia]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code>https://api-na.allocadia.com/{version}</code>或<code>https://api-eu.allocadia.com/{version}</code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 为您添加授权标头。</p> </td> 
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
 </tbody> 
</table>

#### [!UICONTROL Read Record]

此操作模块从[!DNL Allocadia]中的单个记录读取数据。

您指定记录的ID。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Allocadia]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>选择您希望模块读取的[!DNL Allocadia]记录的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在模块输出中的字段。 可用字段取决于您选择的[!UICONTROL Entity Type]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射您希望模块读取的记录的唯一[!DNL Allocadia] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Record]

此操作模块创建记录。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Allocadia]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>选择是要基于联机项目还是列选项创建新的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>选择要创建记录的预算。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Column choices]</td> 
   <td>选择要用于创建新记录的列。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Label]</td> 
   <td>输入或映射新记录的标签</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Record]

此操作模块删除特定记录。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Allocadia]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td> <p>选择要删除的实体类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Line item]</strong> </p> <p>输入行项目标识</p> </li> 
     <li> <p><strong>[!UICONTROL Column Choice]</strong> </p> <p>选择要从中删除记录的预算，然后输入列ID和选项ID。</p> </li> 
     <li> <p><strong>[!UICONTROL Forecast Tags]</strong> </p> <p>选择要从中删除记录的预算，然后输入标签ID。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update Record]

此操作模块更新记录，例如行项目、用户或列选项。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!UICONTROL Allocadia]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>选择要更新模块的[!DNL Allocadia]记录的类型。 根据您选择的实体类型，将显示其他字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>选择要更新记录的预算。 </p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL Search Record]

此搜索模块在[!DNL Allocadia]中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景的后续模块中映射此信息。

指定所需记录的类型。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Allocadia]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>选择要模块搜索的[!DNL Allocadia]记录的类型。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Budgets]</td> 
   <td> <p>选择要搜索的预算。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>选择您希望模块返回所有匹配记录，还是仅返回第一个匹配记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>选择要搜索的字段，选择操作，然后输入或映射要搜索的值。 您可以添加[!DNL AND]或[!DNL OR]规则以进一步筛选搜索。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在模块输出中的字段。 可用字段取决于您选择的实体类型。</p> </td> 
  </tr> 
 </tbody> 
</table>
