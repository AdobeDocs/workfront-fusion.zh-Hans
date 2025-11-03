---
title: Azure Active Directory模块
description: 在Adobe Workfront Fusion方案中，您可以自动使用 [!DNL Azure] Active Directory的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 96455ae4-ef68-46b5-a172-429cf9f982fb
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 1%

---

# [!DNL Azure Active Directory]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Azure Active Directory]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL Azure Active Directory]模块，您必须具有[!DNL Azure Active Directory]帐户。

## [!DNL Azure Active Directory] API信息

Azure Active Directory连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.4.5</td> 
  </tr>
 </tbody> 
</table>

## [!DNL Azure Active Directory]模块及其字段

在配置[!DNL Azure Active Directory]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Azure Active Directory]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[在Adobe Workfront Fusion中将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](../assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!UICONTROL 观看记录] （已计划）

此轮询（计划）触发器模块执行的情况是，选定对象中的记录自[!DNL Azure Active Directory]中上次计划运行以来已创建。 它还返回与一个或多个记录关联的所有标准字段，以及连接访问的任何自定义字段和值。您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure Active Directory]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL类型]</td> 
   <td>选择要监视用户记录还是组记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL最大记录数]</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 读取记录]](#read-record)
* [[!UICONTROL 创建记录]](#create-record)
* [[!UICONTROL 自定义API调用]](#custom-api-call)

#### [!UICONTROL 读取记录]

此操作模块从[!DNL Azure Active Directory]中的单个记录读取数据。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

您必须具有足够的权限才能访问[!DNL Azure Active Directory]中的记录以检索此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure Active Directory]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择您要读取[！UICONTROL User]记录还是[！UICONTROL Group]记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td>选择要包含在此模块的输出捆绑包中的信息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL ID]</td> 
   <td>输入或映射您希望模块读取的记录的唯一[!DNL Azure Active Directory] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建记录]

此操作模块创建新用户或组记录。

指定所需记录的类型。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure Active Directory]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择您要读取[！UICONTROL User]记录还是[！UICONTROL Group]记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL其他字段]</td> 
   <td>填写这些字段以设置新记录的值。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义API调用]

此操作模块允许您对[!DNL Azure Active Directory] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Azure Active Directory]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure Active Directory]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL URL]</td> 
   <td>输入或映射相对路径 <code>https://graph.microsoft.com/{version}/{resource}?{query-parameters}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="../assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [搜索用户](#search-users)
* [搜索用户/组增量](#search-usersgroups-delta)

#### [!UICONTROL 搜索用户]

此搜索模块在[!DNL Azure Active Directory]中查找与您指定的搜索查询匹配的对象中的记录。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure Active Directory]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL搜索条件]</td> 
   <td> <p>输入要在搜索中使用的标准。</p> <p>有关要使用的参数（如“[！UICONTROL $filter]”）的信息，请参阅<a href="https://docs.microsoft.com/en-us/graph/query-parameters"> API文档中的</a>使用查询参数自定义响应[!DNL Microsoft]。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td>选择要包含在此模块的输出捆绑包中的信息。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL最大记录数]</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索用户/组增量]

此搜索模块查找[!DNL Azure AD]中已创建、更新或删除的记录。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure Active Directory]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>
