---
title: Split.io模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用 [!DNL Split.io]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 7d738a96-5424-4c30-831f-82e1d4c6f9d2
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1492'
ht-degree: 0%

---

# [!DNL Split.io]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Split.io]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL Split.io]模块，您必须具有[!DNL Split.io]帐户。

## Split.io API信息

Split.io连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://api.split.io/internal/api</td>
   </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.34.1</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Split.io]连接到[!DNL Workfront Fusion] {#connect-split-io-to-workfront-fusion}

您可以在[!DNL Split.io]模块内直接创建与[!DNL Split.io]帐户的连接。

1. 在任意[!DNL Split.io]模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 输入连接的名称。
1. 输入您的[!DNL Split.io] API密钥。

   有关[!DNL Split.io] API密钥的更多信息，请参阅[!DNL Split.io]文档中的[API密钥](https://help.split.io/hc/en-us/articles/360019916211-API-keys)。

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。

## [!DNL Split.io]模块及其字段

配置[!DNL split.io]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL split.io]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)
* [搜索](#searches)

### 操作

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Get Split]](#get-split)
* [[!UICONTROL Get Split Definition in Environment]](#get-split-definition-in-environment)
* [[!UICONTROL Create Split]](#create-split)
* [[!UICONTROL Delete Split]](#delete-split)
* [[!UICONTROL Create Split Definition in Environment]](#create-split-definition-in-environment)
* [[!UICONTROL Remove Split Definition from Environment]](#remove-split-definition-from-environment)
* [[!UICONTROL Partial Update Split Definition in Environment]](#partial-update-split-definition-in-environment)
* [[!UICONTROL Associate Tags]](#associate-tags)

#### [!UICONTROL Custom API Call]

此操作模块允许您对[!DNL split.io] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL split.io]模块无法实现的数据流自动化。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code>https://api.split.io/internal/api/v2/</code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
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
   <td>输入或映射每个方案执行周期中您希望模块使用的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Split]

此操作模块将检索拆分。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要检索的分割的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>输入或映射要检索的分割的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Split Definition in Environment]

此操作模块从指定的环境中检索特定的拆分定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要检索的拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>选择或映射包含要检索的拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>输入或映射要检索其拆分定义的分割的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split]

在给定流量类型的情况下，此操作模块会在您的组织中创建新拆分。

>[!NOTE]
>
>该API不会在任何环境中配置拆分。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要在其中创建拆分的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Traffic Type ID or Name]</td> 
   <td>选择或映射要创建拆分的流量类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>输入或映射要创建的拆分的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Description]</td> 
   <td>为要创建的分割输入或映射[!UICONTROL split]描述。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Split]

此操作模块会从您的组织中删除拆分。 这会自动从所有环境中取消配置剥离定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要删除拆分的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>输入或映射要删除的分割的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create Split Definition in Environment]

此操作模块为特定环境配置拆分定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要在其中创建拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>选择或映射要创建拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>输入或映射要为其创建定义的分割的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>输入或映射要添加到拆分定义的任何注释。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Rules]</td> 
   <td> <p>对于要添加到定义的每个定位规则，单击<b>[!UICONTROL Add item]</b>，然后输入或映射该规则。</p> <p>有关定位规则的更多信息，请参阅[!DNL Split.io]文档中的<a href="https://docs.split.io/reference#create-split-definition-in-environment">在环境中创建拆分定义</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default rule]</td> 
   <td> <p>输入或映射希望拆分用于不符合其他规则规范的流量的规则。</p> <p>有关定位规则的更多信息，请参阅[!DNL Split.io]文档中的<a href="https://docs.split.io/reference#create-split-definition-in-environment">在环境中创建拆分定义</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Default treatment]</td> 
   <td> <p>输入或映射在拆分被终止或客户不包含在流量分配中的情况下希望拆分使用的处理方式。</p> <p>有关处理的详细信息，请参阅[!DNL Split.io]文档中的<a href="https://docs.split.io/reference#create-split-definition-in-environment">在环境中创建拆分定义</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Treatments]</td> 
   <td> <p>对于要添加到定义的每个处理，单击<b>[!UICONTROL Add item]</b>，然后输入或映射处理。</p> <p>有关处理的详细信息，请参阅[!DNL Split.io]文档中的<a href="https://docs.split.io/reference#create-split-definition-in-environment">在环境中创建拆分定义</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Split Definition from Environment]

此操作模块为特定环境取消配置拆分定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要删除拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>选择或映射要删除拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>输入或映射要删除其定义的分割的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>输入或映射要添加到拆分定义的任何注释。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Partial Update Split Definition in Environment]

此操作模块更新特定环境的拆分定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要更新拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>选择或映射要更新拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Split Name]</td> 
   <td> <p>输入或映射要更新其定义的分割的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update content]</td> 
   <td> <p>对于要更新的拆分的每个属性，单击<b>[!UICONTROL Add item]</b>并输入或映射所需的更改。</p> <p>有关详细信息，请参阅[!DNL Split.io]文档中的<a href="https://docs.split.io/reference#partial-update-split-definition-in-environment">环境</a>中的部分更新拆分定义。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>输入或映射要添加到拆分定义的任何注释。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Associate Tags]

此操作模块将标记添加到指定的对象。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要添加标记的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Name]</td> 
   <td>输入或映射要添加标记的对象的名称，</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Object Type]</td> 
   <td> <p>输入或映射要添加标记的对象的类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> <p>对于要添加的每个标记，单击<b>[!UICONTROL Add item]</b>并输入或映射该标记。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL Get Workspaces]](#get-workspaces)
* [[!UICONTROL Get Environments]](#get-environments)
* [[!UICONTROL Get Splits]](#get-splits)
* [[!UICONTROL List Split Definitions in an Environment]](#list-split-definitions-in-an-environment)
* [[!UICONTROL Get Traffic Types]](#get-traffic-types)

#### [!UICONTROL Get Workspaces]

此搜索模块检索组织的工作区。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射每个方案执行周期中您希望模块检索的最大工作区数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Environments]

此搜索模块可检索环境列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要列出的环境的工作区。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Splits]

此搜索模块检索拆分列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要列出的拆分的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射您希望模块在每个方案执行周期中检索的最大拆分数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Split Definitions in an Environment]

此搜索模块检索给定环境中的拆分定义列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要列出的拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Environment Name or ID]</td> 
   <td>选择或映射包含要列出的拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射每个方案执行周期中您希望模块检索的最大拆分定义数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Traffic Types]

此搜索模块可检索流量类型的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要列出的流量类型的工作区。</td> 
  </tr> 
 </tbody> 
</table>
