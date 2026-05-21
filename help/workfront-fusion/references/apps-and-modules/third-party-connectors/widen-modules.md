---
title: Widen 模块
description: 在Adobe Workfront Fusion方案中，您可以自动使用[!UICONTROL Widen]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 11376e58-a44b-4766-85dc-e2421b0112de
TQID: https://experienceleague.adobe.com/joW38nxn0gj6qr1bd1RMS2RT2xOd2KgUsA-M8l57-ys
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1673
ht-degree: 30%

---

# [!DNL Widen] 模块

在Adobe Workfront Fusion方案中，您可以自动使用[!UICONTROL Widen]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!UICONTROL 加宽]模块，您必须具有[!UICONTROL 加宽]帐户。

## 扩展API信息

Widen连接器使用以下方法：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 版本</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.10.11</td> 
  </tr>
 </tbody> 
 </table>

## 将 [!DNL Widen] 连接到 Workfront Fusion  {#connect-widen-to-workfront-fusion}

您可以在[!DNL Widen]模块内直接创建与[!DNL Widen]帐户的连接。

1. 在任意[!DNL Widen]模块中，单击[!UICONTROL 连接]字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 选择要连接的环境和帐户类型。 这仅供参考，并显示在Fusion的“连接”区域中。
1. 选择要连接的[!DNL Widen]域。
1. 输入[!DNL Widen]帐户的令牌。 有关查找此令牌的说明，请参阅[[!DNL Widen] API常见问题解答](https://community.widen.com/collective/s/article/API-FAQs)。
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Widen] 模块及其字段

在您配置 [!DNL Widen] 模块时，Workfront Fusion 会显示以下字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Widen] 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器模块](#trigger-modules)
* [操作模块](#action-modules)
* [搜索模块](#search-modules)

### 触发器模块

#### [!UICONTROL 观看资源]

此触发器模块会在创建或更新资产时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
  <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 事件类型]</td> 
   <td> <p>选择您要监视新资源还是更新的资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 展开]</td> 
   <td> <p>除了资源字段之外，还选择要包含在模块输出中的属性。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要包含在模块输出中的字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块使用的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作模块

* [[!UICONTROL 将资源添加到收藏集]](#add-assets-to-collections)
* [[!UICONTROL 自定义 API 调用]](#custom-api-call)
* [[!UICONTROL 下载文件]](#download-file)
* [[!UICONTROL 读取资源信息]](#read-asset-info)
* [[!UICONTROL 从收藏集中删除资源]](#remove-assets-from-collection)
* [[!UICONTROL 更新资源元数据]](#update-asset-metadata)
* [[!UICONTROL 上载文件]](#upload-a-file)

#### [!UICONTROL 将资源添加到收藏集]

此操作模块向收藏集添加一个或多个资源。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
  <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 收藏集ID]</td> 
   <td>对于要将资产添加到的每个收藏集，单击<strong>[收藏集ID]</strong>并输入或映射[!UICONTROL 收藏集ID]。</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> 对于要添加到收藏集的每个资源，单击<strong>[!UICONTROL Assets ID]</strong>并输入或映射该资源ID。</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块使用的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义 API 调用]

此操作模块允许您向 [!DNL Widen] API 发起自定义的已经过身份认证的调用。 通过这种方式，您可以构建其他 [!DNL Widen] 模块无法实现的数据流自动化。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API版本]</td> 
   <td>选择您要使用最新版本的[!DNL Widen] API，还是版本1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入或映射API调用的URL。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。 有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] 会自动为您添加授权标头。</p> </td> 
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

#### [!UICONTROL 下载文件]

此操作模块从您的[!DNL Widen]帐户下载资产。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
  <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资源 ID]</td> 
   <td> <p>输入或映射要下载的资源的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取资源信息]

此操作模块通过资产的唯一ID检索单个资产。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
  <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资源 ID]</td> 
   <td> <p>输入或映射要为其读取信息的资源的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 展开]</td> 
   <td> <p>除了资源字段之外，还选择要包含在模块输出中的属性。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要包含在模块输出中的字段。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 从收藏集中删除资源]

此操作模块将从收藏集中删除一个或多个资源。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
  <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 收藏集ID]</td> 
   <td>对于要删除资产的每个收藏集，单击<strong>[收藏集ID]</strong>，然后输入或映射[!UICONTROL 收藏集ID]。</li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Assets ID]</td> 
   <td> 对于要从收藏集中删除的每个资源，单击<strong>[!UICONTROL Assets ID]</strong>并输入或映射该资源ID。</p> </li> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块使用的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新资源元数据]

此操作模块可更新资源的元数据字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
  <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资源 ID]</td> 
   <td> <p>输入或映射要更新元数据的资源的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 元数据类型]</td> 
   <td> <p>为要更新的元数据选择元数据类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 元数据]</td> 
   <td>选择要更新的元数据字段。 对于每个字段，输入该字段的新值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块使用的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上载文件]

此操作模块将文件上传到您的[!DNL Widen]帐户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
  <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 上传配置文件]</td> 
   <td> <p>选择您希望模块使用的上载配置文件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 上载方法]</td> 
   <td> <p>选择上载文件的方式。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL ，来自文件]</strong> </p> <p>从上一个模块中选择或映射源文件。</p> </li> 
     <li> <p><strong>[!UICONTROL ，按URL]</strong> </p> <p>输入或映射要上载的文件的URL。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件名]</td> 
   <td>输入或映射上传文件的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 元数据类型]</td> 
   <td>为要上载的文件选择元数据类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 元数据]</td> 
   <td>选择要包含在文件上载中的元数据字段。 对于每个字段，输入该字段的[!UICONTROL 值]。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索模块

* [[!UICONTROL 读取收藏集资源]](#read-collection-assets)
* [[!UICONTROL 搜索资源]](#search-assets)

#### [!UICONTROL 读取收藏集资源]

此操作模块可检索收藏集中的资产列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
  <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 收藏集ID]</td> 
   <td> <p>输入或映射包含要读取的资产的收藏集的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 开始]</td> 
   <td>输入或映射要列出的第一个项目的编号。 这是对记录进行分页的一种方式。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 排序方式]</td> 
   <td> <p>选择要对资源进行排序的属性。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 顺序]</td> 
   <td>选择您希望对资源进行升序排序还是降序排序。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要包含在模块输出中的字段。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索资源]

此搜索模块可检索与特定搜索条件匹配的资源列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
  <td> <p>有关将[!DNL Widen]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-widen-to-workfront-fusion" class="MCXref xref">将[!DNL Widen]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 搜索查询]</td> 
   <td> <p>输入搜索资产时所依据的标准。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 排序方式]</td> 
   <td> <p>选择您希望对资源排序的方式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 顺序]</td> 
   <td>选择您希望对资源进行升序排序还是降序排序。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include已删除]</td> 
   <td>启用此选项以在搜索中包含已删除的资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 包含已存档]</p> </td> 
   <td> <p>启用此选项以在搜索中包含已存档的资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 搜索文档文本]</td> 
   <td>启用此选项可在搜索中包含文档文本，或设置为false以仅包含标题与搜索条件匹配的资产。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 偏移]</td> 
   <td>输入或映射要检索其详细信息的第一个项目的编号。 这是对记录进行分页的一种方式。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scroll]</td> 
   <td>启用此选项以允许滚动。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 展开]</td> 
   <td> <p>除了资源字段之外，还选择要包含在模块输出中的属性。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要包含在模块输出中的字段。</td> 
  </tr> 
 </tbody> 
</table>
