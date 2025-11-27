---
title: Marketo 模块
description: 在 Adobe Workfront Fusion 场景中，您可以自动化使用  [!DNL Marketo] 的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '2237'
ht-degree: 100%

---

# [!DNL Marketo] 模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL Marketo] 的工作流，并将其连接到多个第三方应用程序和服务。

有关 Marketo 连接器的视频介绍，请参阅：

* [Marketo](https://video.tv.adobe.com/v/3427026/){target=_blank}

有关创建场景的说明，请参阅[创建场景：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)中的相关文章。

有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)中的相关文章。

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

要使用 [!DNL Marketo] 模块，您必须拥有一个 [!DNL Marketo] 帐户。

## Marketo API 信息

Marketo 连接器使用以下内容：

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
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## 将 [!DNL Marketo] 连接到 Workfront Fusion {#connect-marketo-to-workfront-fusion}

您可以在任何 [!DNL Marketo] 模块中直接创建与 [!DNL Marketo] 帐户的连接。

1. 在任意 Marketo 模块中，点击“连接”字段旁的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>
          <p>选择要连接生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>
          <p>选择连接服务帐户还是个人帐户。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 帐户 / Munchkin ID]</td>
        <td>
          <p>输入您的 [!DNL Marketo] 帐户或 [!DNL Marketo] [!UICONTROL Munchkin] ID。这是分配给您的帐户的基本 URL 或端点中的唯一部分，您将通过该部分使用 [!UICONTROL REST] API 访问 [!DNL Marketo]。有关如何查找此部分的说明，请参阅 [!DNL Marketo] 文档中的[基本 URL](https://developers.marketo.com/rest-api/base-url/)。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端 ID]</td>
        <td>输入您的 Marketo 客户端 ID。有关如何查找此部分的说明，请参阅 [!DNL Marketo] 文档中的[身份验证](https://developers.marketo.com/rest-api/authentication/)。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的 Marketo 客户端密钥。有关如何查找这些信息的说明，请参阅 [!DNL Marketo] 文档中的[身份验证](https://developers.marketo.com/rest-api/authentication/)。</td>
      </tr>
     </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Marketo] 模块及其字段

在您配置 [!DNL Marketo] 模块时，Workfront Fusion 会显示以下字段。除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Marketo] 字段。模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

* [[!UICONTROL 监控事件（即时）]](#watch-events-instant)
* [[!UICONTROL 监控记录]](#watch-records)

#### [!UICONTROL 监控事件（即时）]

当创建或更新记录时，此触发器模块会启动场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>输入您希望模块使用的 Webhook。</p> <p>有关 Webhook 的更多信息，请参阅 <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhook</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 监控记录]

当创建或更新记录时，此触发器模块会启动场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择要创建的记录类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 活动]</strong> </p> <p>选择您想关注的活动类型。 </p> <p>该模块仅监控新增活动。<br></p> </li> 
     <li> <p><strong>[!UICONTROL 商机]</strong> </p> <p>在<b>事件类型</b>字段中，选择是否要监控新增记录、更新记录、同时监控新增和更新记录，或监控特定字段更新。如果选择监控特定字段更新，请选择您希望模块监控的字段。</p> </li> 
     <li> <p><strong>[!UICONTROL 项目群]</strong> </p> <p>在<b>事件类型</b>字段中，选择是否要监控新增记录、更新记录或同时监控新增和更新记录。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td> <p>选择您希望包含在此模块输出捆绑包中的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 在列表中添加商机]](#add-leads-to-a-list)
* [[!UICONTROL 克隆项目群]](#clone-a-program)
* [[!UICONTROL 创建记录]](#create-a-record)
* [[!UICONTROL 自定义 API 调用]](#custom-api-call)
* [[!UICONTROL 下载文件]](#download-a-file)
* [[!UICONTROL 读取记录]](#read-a-record)
* [[!UICONTROL 从列表中移除商机]](#remove-leads-from-a-list)
* [[!UICONTROL 计划营销活动]](#schedule-a-campaign)
* [[!UICONTROL 更新记录]](#update-a-record)
* [[!UICONTROL 上传文件]](#upload-a-file)

#### [!UICONTROL 在列表中添加商机]

此操作模块会根据商机 ID，将一个或多个商机添加到列表中。您一次最多可以添加 300 个商机。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 列表 ID]</td> 
   <td>输入或映射您要添加商机的列表 ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 商机 ID]</td> 
   <td> <p>对于每个要添加到列表中的商机，点击<b>[!UICONTROL 添加]</b>，然后输入或映射该商机的 ID。您最多可以添加 300 个商机，让模块将其加入列表。</p> <p>点击映射切换开关，将您希望添加到列表的现有商机集合进行映射。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 克隆项目群]

此操作模块会使用现有项目群的 ID 创建项目群副本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 现有项目群 ID]</td> 
   <td>输入或映射您想复制的项目群 ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 新项目群名称]</p> </td> 
   <td> <p>输入或映射新项目群的名称。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹 ID]</td> 
   <td>输入或映射新项目群要放置的文件夹 ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建记录]

此操作模块会在 [!DNL Marketo] 中创建一条新记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择要创建的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL 公司]</p> </li> 
     <li> <p>[!UICONTROL 文件夹]</p> </li> 
     <li> <p>[!UICONTROL 商机]</p> </li> 
     <li> <p>[!UICONTROL 项目群]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择要映射的字段]</td> 
   <td>如果您正在创建“公司”或“商机”记录，请选择您希望在新记录创建时设置值的字段，然后为这些字段输入相应的值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目群类型]</td> 
   <td>如果您正在创建项目群，请选择您要创建的项目群类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目群渠道] </td> 
   <td>如果您正在创建项目群，请选择您希望创建该项目群的项目群渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹] / [!UICONTROL 项目群名称]</td> 
   <td>如果您正在创建文件夹或项目群，请输入或映射新记录的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 描述]</td> 
   <td> <p>如果您正在创建文件夹或项目群，请输入或映射新记录的描述。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 父文件夹 ID]</td> 
   <td>如果您正在创建文件夹或项目群，请输入或映射您希望创建新记录的父文件夹 ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 成本]</td> 
   <td>如果您正在创建项目群，请添加相关成本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标记]</td> 
   <td>如果您正在创建项目群，请添加相关标记。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义 API 调用]

此操作模块允许您向 [!DNL Marketo] API 发起自定义的已经过身份认证的调用。通过这种方式，您可以构建其他 [!DNL Marketo] 模块无法实现的数据流自动化。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于 <code>https://{your-base-url}.mktorest.com/</code> 的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 请求方法</a>。</p> </td> 
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
   <td role="rowheader">[!UICONTROL 字段]</td> 
   <td> <p>对于每个要添加到 API 调用中的字段，点击<b>添加项目</b>，并输入该字段的键和值。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 下载文件]

此操作模块通过文件 ID 下载文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件 ID]</td> 
   <td>输入或映射您想下载的文件 ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

此操作模块根据记录 ID 读取记录信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择要创建的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL 营销活动]</p> </li> 
     <li> <p>[!UICONTROL 公司]</p> </li> 
     <li> <p>[!UICONTROL 商机]</p> </li> 
     <li> <p>[!UICONTROL 列表]</p> </li> 
     <li> <p>[!UICONTROL 项目群]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要包含在此模块输出捆绑包中的信息。可用字段取决于您选择的[!UICONTROL 记录类型]。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;Object&gt; ID]</td> 
   <td>输入或映射您希望检索信息的对象 ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 从列表中移除商机]

此操作模块会根据商机 ID 将一个或多个商机从列表中移除。您一次最多可以移除 300 个商机。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 列表 ID]</td> 
   <td>输入或映射您希望从中移除商机的列表 ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 商机 ID]</td> 
   <td> <p>对于每个要从列表中移除的商机，点击<b>[!UICONTROL 添加项目]</b>，然后输入或映射要移除的商机 ID。您最多可以添加 300 个商机以供模块从列表中移除。 </p> <p>点击映射切换开关，将您希望从列表中移除的现有商机集合映射到此字段。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 计划营销活动]

此操作模块会为特定日期计划一个现有的营销活动。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 营销活动 ID]</td> 
   <td>输入或映射您希望计划的营销活动的 ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 计划日期]</p> </td> 
   <td>选择您希望该营销活动运行的日期。如果该字段留空，营销活动将在场景开始后五分钟运行。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新记录]

此操作模块会根据记录 ID 更新现有记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择要创建的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL 公司]</p> </li> 
     <li> <p>[!UICONTROL 商机]</p> </li> 
     <li> <p>[!UICONTROL 项目群]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 公司] / [!UICONTROL 商机] / [!UICONTROL 项目群 ID]</td> 
   <td>输入或映射您希望更新的记录 ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择要映射的字段]</td> 
   <td>如果您正在更新“公司”或“商机”，请选择您希望更新其值的字段，然后为这些字段输入新的值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目群名称]</td> 
   <td>如果您正在更新项目群，请输入或映射项目群的新名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 描述]</td> 
   <td> <p>如果您正在更新项目群，请输入或映射项目群的新描述。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 开始日期]</td> 
   <td>如果您正在更新项目群，请输入或映射项目群的新开始日期。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 结束日期]</td> 
   <td>如果您正在更新项目群，请输入或映射项目群的新结束日期。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 成本]</td> 
   <td>如果您正在更新项目群，请添加相关成本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标记]</td> 
   <td>如果您正在更新项目群，请添加相关标记。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上传文件]

此操作模块会将新文件上传到 [!UICONTROL Marketo]。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td>从上一个模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹 ID]</td> 
   <td>输入或映射新文件要放置的文件夹 ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 描述]</td> 
   <td>输入上传文件的描述。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL 列出记录]](#list-records)
* [[!UICONTROL 搜索记录]](#update-a-record)

#### [!UICONTROL 列出记录]

此操作模块会检索指定类型的所有记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择您要列出的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL 读取所有营销活动]</p> </li> 
     <li> <p>[!UICONTROL 读取所有项目群]</p> </li> 
     <li> <p>[!UICONTROL 读取所有商机] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 字段]</td> 
   <td>如果您选择检索商机，请选择是从列表中检索还是从项目群中检索商机。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要包含在此模块输出捆绑包中的信息。可用字段取决于您选择的[!UICONTROL 记录类型]。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索记录]

此搜索模块会检索符合特定搜索条件的记录列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将 [!DNL Marketo] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-marketo-to-workfront-fusion" class="MCXref xref">将 [!DNL Marketo] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择您要搜索的记录类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL 营销活动]</p> </li> 
     <li> <p>[!UICONTROL 商机]</p> </li> 
     <li> <p>[!UICONTROL 项目群]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 字段]</p> </td> 
   <td> <p>选择您要用于搜索的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 值]</td> 
   <td>输入您要搜索的字段值。如果该字段允许搜索多个值，请对每个要搜索的值点击<b>[!UICONTROL 添加项目]</b>，并输入该值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在此模块输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
 </tbody> 
</table>
