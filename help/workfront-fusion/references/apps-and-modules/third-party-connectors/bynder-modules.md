---
title: Bynder模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用 [!DNL Bynder]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1426'
ht-degree: 0%

---

# [!DNL Bynder]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Bynder]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL Bynder]模块，您必须具有[!DNL Bynder]帐户。

## Bynder API信息

Bynder连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.25.21</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Bynder]连接到Workfront Fusion  {#connect-bynder-to-workfront-fusion}

* [创建从 [!DNL Workfront Fusion]到 [!DNL Bynder] 的连接](#create-a-connection-to-bynder-from-workfront-fusion)
* [在 [!DNL Bynder] 中生成[!UICONTROL Client ID]和[!UICONTROL Client Secret]（可选）](#generate-a-client-id-and-client-secret-in-bynder-optional)

### 从[!DNL Workfront Fusion]创建与[!DNL Bynder]的连接

您可以在[!DNL Bynder]模块内直接创建从[!DNL Workfront Fusion]到[!DNL Bynder]帐户的连接。

1. 在任意[!DNL Bynder]模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 选择要连接的[!DNL Bynder]域。
1. （可选）单击&#x200B;**[!UICONTROL Advanced settings]**，然后输入您的[!UICONTROL Client ID]和[!UICONTROL Client Secret]。

   有关生成客户端ID和客户端密钥的说明，请参阅本文中的[在 [!DNL Bynder] （可选）](#generate-a-client-id-and-client-secret-in-bynder-optional)中生成客户端ID和客户端密钥。

1. 在[!UICONTROL login]窗口中，输入用户名（电子邮件地址）和密码。
1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。

### 在[!DNL Bynder]中生成[!UICONTROL Client ID]和[!UICONTROL Client Secret]（可选）

如果要使用客户端ID和客户端密钥创建连接，则可以从[!DNL Bynder]帐户生成连接。 在[!DNL Bynder]中创建应用程序时生成客户端ID和客户端密钥。

有关在[!DNL Bynder]中创建应用程序的说明，请参阅[!DNL Bynder]文档中的[Oauth 2.0应用程序](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/)。

>[!NOTE]
>
>在[!DNL Bynder]中创建应用程序时，输入以下内容作为`redirect uri`：
>
>`https://app.workfrontfusion.com/oauth/cb/workfront-bynder`

## [!DNL Bynder]模块及其字段

配置[!DNL Bynder]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Bynder]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)
* [搜索](#searches)
* [触发器](#triggers)

### 操作

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Read asset metadata]](#read-asset-metadata)
* [[!UICONTROL Update asset metadata]](#update-asset-metadata)
* [[!UICONTROL Add assets to a collection]](#add-assets-to-a-collection)
* [[!UICONTROL Remove assets from collection]](#remove-assets-from-collection)
* [[!UICONTROL Add a tag to assets]](#add-a-tag-to-assets)
* [[!UICONTROL Remove a tag]来自资源](#remove-a-tag-from-assets)
* [[!UICONTROL Download asset]](#download-asset)
* [[!UICONTROL Upload asset]](#upload-asset)

#### [!UICONTROL Custom API Call]

此操作模块允许您对[!DNL Bynder] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Bynder]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

模块返回状态代码，以及API调用的标头和正文。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>输入相对于<code>https://{your-bynder-domain}/api/{api-version}/</code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如： <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
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

#### [!UICONTROL Read asset metadata]

此操作模块读取资源的元数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>输入或映射要为其检索元数据的资源的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update asset metadata]

此操作模块可更新现有资源的元数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>输入或映射要为其更新元数据的资源的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>选择要为其输入信息的字段，然后输入要更新元数据的信息或将其映射到这些字段中。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Metaproperties]</p> </td> 
   <td>选择要更新的选项，然后输入信息或将信息映射到这些属性。 元属性是指有关资产的信息，并不表示资产中的特定字段。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add assets to a collection]

此操作模块可向收藏集添加一个或多个资产。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>输入或映射要添加资产的收藏集的ID。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>对于要添加到收藏集的每个资源，单击<strong>[!UICONTROL Add item]</strong>，然后输入或映射该资源ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove assets from collection]

此操作模块会从收藏集中删除一个或多个资产。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Collection ID]</td> 
   <td> <p>输入或映射要删除资产的收藏集的ID。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>对于要从收藏集中移除的每个资源，单击<strong>[!UICONTROL Add item]</strong>，然后输入或映射该资源ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add a tag to assets]

向一个或多个资源添加标记

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>输入或映射要添加到资产的标记的ID。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>对于每个要标记的资源，单击<strong>[!UICONTROL Add item]</strong>，然后输入或映射该资源ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove a tag from assets]

从一个或多个资源中删除标记

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tag ID]</td> 
   <td> <p>输入或映射要从资产中删除的标记的ID。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset IDs]</td> 
   <td> <p>对于要从中删除标记的每个资源，单击<strong>[!UICONTROL Add item]</strong>，然后输入或映射该资源ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download asset]

此操作模块可下载单个资产。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td>输入或映射要下载的资源的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset version]</td> 
   <td> <p>输入或映射要下载的资源版本。 要下载最新版本的资源，请将字段留空。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload asset]

此操作模块上传单个资源。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save as]</td> 
   <td> <p>选择要如何保存要上传的文件。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL New asset]</strong> </p> <p>选择要为其输入信息的字段和元属性，然后在这些字段中输入信息。</p> <p>输入或映射要用于上传资源的品牌的ID。</p> </li> 
     <li> <p><strong>[!UICONTROL New asset version]</strong> </p> <p>输入要为其上传新版本的资产的ID。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>从上一个模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL List record]](#list-record)
* [[!UICONTROL Search for assets]](#search-for-assets)

#### [!UICONTROL List record]

此搜索模块可检索特定类型的所有项目。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要列出的记录类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Read all collections]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read information about all tags]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Read all assets of a collection]</strong> </p> <p>输入或映射要为其列出资产的收藏集的ID。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在模块输出中的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for assets]

此搜索模块会根据您提供的条件搜索资产。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Criteria]</td> 
   <td> <p>输入搜索条件。 </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Field]</strong> </p> <p>选择要在搜索中使用的字段</p> </li> 
     <li> <p><strong>[!UICONTROL Logical Operator]</strong> </p> <p>选择要在搜索中使用的运算符。</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>在选定字段中输入或映射要查找的值。 值类型应与所选字段的数据类型相同。 </p> <p>有关数据类型的详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">项数据类型。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>选择您要返回第一个匹配的资产还是所有匹配的资产。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td> <p>选择要作为排序依据的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort Direction]</td> 
   <td> <p>选择是要升序排序还是降序排序。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在模块输出中的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 触发器

#### [!UICONTROL Watch assets]

此触发器模块会在创建或更新资产时启动方案。

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到[!DNL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> <!--
    <td role="rowheader">Event type</td>
   --> <!--
    <td>Select whether you want to start the scenario when a new asset is created or when an existing asset is updated.</td>
   --> 
  </tr> 
  <tr>
     <td role="rowheader">[!UICONTROL Collections]</td>
   <td> <p>选择要监视新资产的收藏集。 若要观看所有收藏集，请将此字段留空。</p> </td> 
  </tr> 
  <tr> <!--
    <td role="rowheader">Outputs</td>
   --> <!--
    <td>Select the fields that you want to include in the output.</td>
   --> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Limit]</td>

<td> <p>输入您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>
