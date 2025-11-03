---
title: Bynder模块
description: 在Adobe Workfront Fusion方案中，您可以自动使用 [!DNL Bynder]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 0a45f8a7-12cc-41cc-9135-92f4779afac0
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1853'
ht-degree: 0%

---

# [!DNL Bynder]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Bynder]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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
   <td role="rowheader">Adobe Workfront Fusion许可证</td> 
   <td>
   <p>基于操作：不需要Workfront Fusion许可证</p>
   <p>基于连接器（旧版）：用于工作自动化和集成的Workfront Fusion </p>
   </td> 
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

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

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

>[!NOTE]
>
>Bynder使用授权代码/刷新令牌授予类型。 这是Fusion Bynder连接器使用的唯一授予类型。

* [从Workfront Fusion创建与 [!DNL Bynder] 的连接](#create-a-connection-to-bynder-from-workfront-fusion)
* [在[!UICONTROL 中生成]客户端ID[!UICONTROL 和]客户端密钥 [!DNL Bynder] （可选）](#generate-a-client-id-and-client-secret-in-bynder-optional)

### 从Workfront Fusion创建与[!DNL Bynder]的连接

您可以在[!DNL Bynder]模块内直接创建从Workfront Fusion到[!DNL Bynder]帐户的连接。

1. 在任意[!DNL Bynder]模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
1. 选择要连接的[!DNL Bynder]域。
1. （可选）单击&#x200B;**[!UICONTROL 高级设置]**，然后输入您的[!UICONTROL 客户端ID]和[!UICONTROL 客户端密钥]。

   有关生成客户端ID和客户端密钥的说明，请参阅本文中的[在 [!DNL Bynder] （可选）](#generate-a-client-id-and-client-secret-in-bynder-optional)中生成客户端ID和客户端密钥。

1. 在[!UICONTROL 登录]窗口中，输入用户名（电子邮件地址）和密码。
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

### 在[!UICONTROL 中生成]客户端ID[!UICONTROL 和]客户端密钥[!DNL Bynder]（可选）

如果要使用客户端ID和客户端密钥创建连接，则可以从[!DNL Bynder]帐户生成连接。 在[!DNL Bynder]中创建应用程序时生成客户端ID和客户端密钥。

有关在[!DNL Bynder]中创建应用程序的说明，请参阅[文档中的](https://developer-docs.bynder.com/api/authentication-oauth2-oauth-apps/)Oauth 2.0应用程序[!DNL Bynder]。

>[!NOTE]
>
>* 在[!DNL Bynder]中创建应用程序时，输入以下内容作为`redirect uri`：
>
>   * 美国群集： `https://app.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * 欧盟群集： `https://app-eu.workfrontfusion.com/oauth/cb/workfront-bynder`
>   * Azure群集： `https://app-az.workfrontfusion.com/oauth/cb/workfront-bynder`
>* Bynder使用授权代码/刷新令牌授予类型。 这是Fusion Bynder连接器使用的唯一授予类型。

## [!DNL Bynder]模块及其字段

在配置[!DNL Bynder]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Bynder]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)
* [搜索](#searches)
* [触发器](#triggers)

### 操作

* [[!UICONTROL 向资源添加标记]](#add-a-tag-to-assets)
* [[!UICONTROL 将资源添加到收藏集]](#add-assets-to-a-collection)
* [[!UICONTROL 自定义API调用]](#custom-api-call)
* [[!UICONTROL 下载资源]](#download-asset)
* [[!UICONTROL 读取资源元数据]](#read-asset-metadata)
* [[!UICONTROL 从资源中删除标记]](#remove-a-tag-from-assets)
* [[!UICONTROL 从收藏集中删除资源]](#remove-assets-from-collection)
* [[!UICONTROL 更新资源元数据]](#update-asset-metadata)
* [[!UICONTROL 上传资源]](#upload-asset)

#### [!UICONTROL 向资源添加标记]

此操作模块会将标记添加到一个或多个资源

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL标记ID]</td> 
   <td> <p>输入或映射要添加到资产的标记的ID。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资产ID]</td> 
   <td> <p>对于每个要标记的资产，单击<strong>[！UICONTROL添加项]</strong>，然后输入或映射该资产ID。</p> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL 将资源添加到收藏集]

此操作模块可向收藏集添加一个或多个资产。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL收藏集ID]</td> 
   <td> <p>输入或映射要添加资产的收藏集的ID。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资产ID]</td> 
   <td> <p>对于要添加到收藏集的每个资产，单击<strong>[！UICONTROL添加项]</strong>，然后输入或映射资产ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义API调用]

此操作模块允许您对[!DNL Bynder] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Bynder]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

模块返回状态代码，以及API调用的标头和正文。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>输入相对于<code>https://{your-bynder-domain}/api/{api-version}/</code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如： <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 下载资源]

此操作模块可下载单个资产。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资产ID]</td> 
   <td>输入或映射要下载的资源的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资产版本]</td> 
   <td> <p>输入或映射要下载的资源版本。 要下载最新版本的资源，请将字段留空。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取资源元数据]

此操作模块读取资源的元数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资产ID]</td> 
   <td>输入或映射要为其检索元数据的资源的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 从资源中删除标记]

此操作模块从一个或多个资产中删除标记

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL标记ID]</td> 
   <td> <p>输入或映射要从资产中删除的标记的ID。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资产ID]</td> 
   <td> <p>对于要从中删除标记的每个资源，单击<strong>[！UICONTROL添加项]</strong>，然后输入或映射该资源ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 从收藏集中删除资源]

此操作模块会从收藏集中删除一个或多个资产。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL收藏集ID]</td> 
   <td> <p>输入或映射要删除资产的收藏集的ID。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资产ID]</td> 
   <td> <p>对于要从收藏集中删除的每个资源，单击<strong>[！UICONTROL添加项]</strong>，然后输入或映射该资源ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新资源元数据]

此操作模块可更新现有资源的元数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资产ID]</td> 
   <td>输入或映射要为其更新元数据的资源的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL字段]</td> 
   <td> <p>选择要为其输入信息的字段，然后输入要更新元数据的信息或将其映射到这些字段中。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Metaproperties]</p> </td> 
   <td>选择要更新的选项，然后输入信息或将信息映射到这些属性。 元属性是指有关资产的信息，并不表示资产中的特定字段。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上传资源]

此操作模块上传单个资源。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL另存为]</td> 
   <td> <p>选择要如何保存要上传的文件。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL新资产]</strong> </p> <p>选择要为其输入信息的字段和元属性，然后在这些字段中输入信息。</p> <p>输入或映射要用于上传资源的品牌的ID。</p> </li> 
     <li> <p><strong>[！UICONTROL新资产版本]</strong> </p> <p>输入要为其上传新版本的资产的ID。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td>从上一个模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL异步文件上传]</td> 
   <td>在上传大文件时启用此选项。 这样可以防止大型文件阻止场景执行。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL 列出记录]](#list-record)
* [[!UICONTROL 搜索Assets]](#search-assets)

#### [!UICONTROL 列出记录]

此搜索模块可检索特定类型的所有项目。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td> <p>选择要列出的记录类型。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL读取所有收藏集]</strong> </p> </li> 
     <li> <p><strong>[！UICONTROL读取有关所有标记的信息]</strong> </p> </li> 
     <li> <p><strong>[！UICONTROL读取收藏集的所有资产]</strong> </p> <p>输入或映射要为其列出资产的收藏集的ID。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td> <p>选择要包含在模块输出中的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索Assets]

此搜索模块会根据您提供的条件搜索资产。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL搜索条件]</td> 
   <td> <p>输入搜索条件。 </p> 
    <ul> 
     <li> <p><strong>[！UICONTROL字段]</strong> </p> <p>选择要在搜索中使用的字段</p> </li> 
     <li> <p><strong>[！UICONTROL逻辑运算符]</strong> </p> <p>选择要在搜索中使用的运算符。</p> </li> 
     <li> <p><strong>[！UICONTROL值]</strong> </p> <p>在选定字段中输入或映射要查找的值。 值类型应与所选字段的数据类型相同。 </p> <p>有关数据类型的详细信息，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">项数据类型</a>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL结果集]</td> 
   <td>选择您要返回第一个匹配的资产还是所有匹配的资产。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL排序方式]</td> 
   <td> <p>选择要作为排序依据的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL排序方向]</td> 
   <td> <p>选择是要升序排序还是降序排序。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td> <p>选择要包含在模块输出中的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 触发器

#### [!UICONTROL 观看资源]

此触发器模块会在创建或更新资产时启动方案。

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">事件类型</td>
    <td>选择您是否希望在创建新资产或更新现有资产时启动方案。</td>
  </tr> 
  <tr>
     <td role="rowheader">[！UICONTROL收藏集]</td>
   <td> <p>选择要监视新资产的收藏集。 若要观看所有收藏集，请将此字段留空。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">输出</td>
    <td>选择要包含在输出中的字段。</td>
  </tr> 
  <tr> 
    <td role="rowheader">[！UICONTROL限制]</td>

<td> <p>输入您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>
