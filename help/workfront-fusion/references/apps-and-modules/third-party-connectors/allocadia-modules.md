---
title: Allocadia 模块
description: 在Adobe Workfront Fusion场景中，您可以自动执行使用Allocadia的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 9a6fccd6-6eee-42dc-a678-c1f34280d139
TQID: https://experienceleague.adobe.com/bCfkq5fzw21hmZWLrWztL27g2RAlBbyk9vPEQ-v6bBU
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1467
ht-degree: 56%

---

# [!DNL Allocadia] 模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL Allocadia] 的工作流，并将其连接到多个第三方应用程序和服务。

有关创建场景的说明，请参阅[创建场景：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)中的相关文章。

有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的相关文章。

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
   <td role="rowheader">Adobe Workfront Fusion 许可证</td> 
   <td>
   <p>基于操作：不需要 Workfront Fusion 许可证</p>
   <p>基于连接器（旧版）：Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

有关 Adobe Workfront Fusion 许可证的详细信息，请参阅 [Adobe Workfront Fusion 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

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
   <td role="rowheader">API 版本</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.7.6</td> 
  </tr>
 </tbody> 
</table>

## 将 [!DNL Allocadia] 连接到 Workfront Fusion

您可以直接从[!DNL Allocadia]模块内部创建与[!DNL Allocadia]帐户的连接。

1. 在任意[!DNL Allocadia]模块中，单击[!UICONTROL 连接]字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 选择您要使用北美服务器还是欧洲服务器。
1. 输入您的用户名和密码。
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Allocadia] 模块及其字段

在您配置 [!DNL Allocadia] 模块时，Workfront Fusion 会显示以下字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Allocadia] 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!UICONTROL 监控记录]

当新增、更新某一类型的对象或同时发生这两种情况时，此触发器模块会执行场景。 该模块会返回与记录关联的所有标准字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> <table style="table-layout:auto"> <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 连接]</p> </td> 
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

#### [!UICONTROL 自定义 API 调用]

此操作模块允许您向 [!DNL Allocadia] API 发起自定义的已经过身份认证的调用。 通过这种方式，您可以构建其他 [!DNL Allocadia] 模块无法实现的数据流自动化。

该操作基于您指定的图元类型（Allocadia对象类型）。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Allocadia] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将 [!DNL Allocadia] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code>https://api-na.allocadia.com/{version}</code>或<code>https://api-eu.allocadia.com/{version}</code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。 有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 正文]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

此操作模块从[!DNL Allocadia]中的单个记录读取数据。

您需要指定记录的 ID。

该模块会返回与记录关联的所有标准字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Allocadia] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将 [!DNL Allocadia] 连接到 Workfront Fusion</a>。</p> </td> 
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

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Allocadia] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将 [!DNL Allocadia] 连接到 Workfront Fusion</a>。</p> </td> 
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

您需要指定记录的 ID。

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Allocadia] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将 [!DNL Allocadia] 连接到 Workfront Fusion</a>。</p> </td> 
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

您需要指定记录的 ID。

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
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

您可以在场景后续的模块中映射这些信息。

指定所需记录的类型。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   td role="rowheader"&gt; <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Allocadia] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-allocadia-to-workfront-fusion" class="MCXref xref">将 [!DNL Allocadia] 连接到 Workfront Fusion</a>。</p> </td> 
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
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
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
