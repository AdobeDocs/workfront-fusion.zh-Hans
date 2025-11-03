---
title: 分配模块
description: 在Adobe Workfront Fusion场景中，您可以自动执行使用Allocadia的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 9a6fccd6-6eee-42dc-a678-c1f34280d139
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1463'
ht-degree: 0%

---

# [!DNL Allocadia]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Allocadia]的工作流，并将其连接到多个第三方应用程序和服务。

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

## 将[!DNL Allocadia]连接到Workfront Fusion

您可以直接从[!DNL Allocadia]模块内部创建与[!DNL Allocadia]帐户的连接。

1. 在任意[!DNL Allocadia]模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
1. 选择您要使用北美服务器还是欧洲服务器。
1. 输入您的用户名和密码。
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Allocadia]模块及其字段

在配置[!DNL Allocadia]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Allocadia]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!UICONTROL 观看记录]

此触发器模块执行特定类型的对象添加、更新或同时添加和更新的方案。 该模块返回与一个或多个记录关联的所有标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> <table style="table-layout:auto"> <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将Allocadia帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">[!UICONTROL Connect Allocadia]到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">筛选条件</td> 
   <td> <p>选择您希望方案仅观看“新记录”、[!UICONTROL 仅更新记录]还是“新记录和更新记录”。</p> </td> 
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

#### [!UICONTROL 自定义API调用]

此操作模块允许您对[!DNL Allocadia] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Allocadia]模块无法实现的数据流自动化。

该操作基于您指定的图元类型（Allocadia对象类型）。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Allocadia]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code>https://api-na.allocadia.com/{version}</code>或<code>https://api-eu.allocadia.com/{version}</code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

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
   <td> <p>有关将[!DNL Allocadia]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 实体类型]</td> 
   <td>选择您希望模块读取的[!DNL Allocadia]记录的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在模块输出中的字段。 可用字段取决于您选择的[!UICONTROL 实体类型]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射您希望模块读取的记录的唯一[!DNL Allocadia] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建记录]

此操作模块创建记录。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Allocadia]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 实体类型]</td> 
   <td>选择是要基于联机项目还是列选项创建新的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 预算]</td> 
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

#### [!UICONTROL 删除记录]

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
   <td> <p>有关将[!DNL Allocadia]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 实体类型]</td> 
   <td> <p>选择要删除的实体类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 行项]</strong> </p> <p>输入行项目标识</p> </li> 
     <li> <p><strong>[!UICONTROL 列选择]</strong> </p> <p>选择要从中删除记录的预算，然后输入列ID和选项ID。</p> </li> 
     <li> <p><strong>[!UICONTROL 预测标记]</strong> </p> <p>选择要从中删除记录的预算，然后输入标签ID。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新记录]

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
   <td> <p>有关将您的[!UICONTROL Allocadia]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 实体类型]</td> 
   <td>选择要更新模块的[!DNL Allocadia]记录的类型。 根据您选择的实体类型，将显示其他字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 预算]</td> 
   <td> <p>选择要更新记录的预算。 </p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL 搜索记录]

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
   <td> <p>有关将[!DNL Allocadia]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将[!DNL Allocadia]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 实体类型]</td> 
   <td>选择要模块搜索的[!DNL Allocadia]记录的类型。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 预算]</td> 
   <td> <p>选择要搜索的预算。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 结果集]</td> 
   <td>选择您希望模块返回所有匹配记录，还是仅返回第一个匹配记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 最大记录数]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 搜索条件]</td> 
   <td>选择要搜索的字段，选择操作，然后输入或映射要搜索的值。 您可以添加[!DNL AND]或[!DNL OR]规则以进一步筛选搜索。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在模块输出中的字段。 可用字段取决于您选择的实体类型。</p> </td> 
  </tr> 
 </tbody> 
</table>
