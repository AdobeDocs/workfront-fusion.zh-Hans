---
title: Adobe Workfront 模块
description: 您可以使用 Adobe Workfront Fusion 的 Adobe Workfront 连接器，在 Workfront 中自动化各类流程。如果您拥有 Workfront Fusion for Work Automation and Integration 许可证，还可以使用该连接器将 Workfront 与第三方应用程序和服务连接起来。
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: ab12dbf0dbad25a8300eb1201fa3e0fde9148acc
workflow-type: ht
source-wordcount: '7366'
ht-degree: 100%

---

# Adobe Workfront 模块

>[!IMPORTANT]
>
>本文介绍的是新版 Workfront 连接器的使用说明，该版本于 2025 年 10 月 22 日发布。此新版连接器反映了 Workfront API 的最新更新。
>
>新版连接器标记为“Workfront”，而原有版本则标记为“Workfront（旧版）”。
>
>我们建议：
>
>* 在创建或更新场景时使用新版连接器。
>* 将现有模块升级为新版连接器。
>
>旧版 Workfront 连接器使用 Workfront API 版本 20，该版本计划在 28.4 版本（2028 年 4 月）中停用。旧版连接器中的模块将在此之前继续正常运行。
>
>如需了解如何升级现有模块，请参阅文章《升级模块到新版本》中的[升级 Workfront 模块到新版本](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md)部分。
>
>如需了解为何有时需要推出新版连接器，请参阅 [Fusion 中的 API 概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md)。

您可以使用 Adobe Workfront Fusion 的 Adobe Workfront 连接器，在 Workfront 中自动化各类流程。您也可以将 Workfront 与其他应用程序和服务连接。

有关创建场景的说明，请参阅[创建场景：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)中的相关文章。有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的相关文章。

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
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 将 Workfront 连接到 Workfront Fusion

Workfront 连接器使用 OAuth 2.0 与 Workfront 建立连接。

您可以在 Workfront Fusion 模块内直接创建到您 Workfront 帐户的连接。

* [使用客户端 ID 和客户端密钥连接到 Workfront](#connect-to-workfront-using-client-id-and-client-secret)
* [使用服务器到服务器连接方式连接到 Workfront](#connect-to-workfront-using-a-server-to-server-connection)

### 使用客户端 ID 和客户端密钥连接到 Workfront

1. 在任意 Adobe Workfront 模块中，点击“连接”字段旁的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接类型]</td>
        <td>
          <p>选择 <b>Adobe Workfront 身份验证连接</b>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端 ID]</td>
        <td>请输入您的 Workfront 客户端 ID。您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。打开您要连接的特定应用程序即可查看客户端 ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的 Workfront 客户端密钥。 您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。如果您的 Workfront OAuth2 应用程序没有客户端密钥，您可以重新生成一个。有关操作说明，请参阅 Workfront 文档。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 身份验证 URL]</td>
        <td>此项可保持默认值，或输入您 Workfront 实例的 URL，并在后面添加 <code>/integrations/oauth2</code>。 <p>示例： <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 主机前缀]</td>
        <td>在大多数情况下，此值应为 <code>origin</code>。
      </tr>
    </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

   如果您尚未登录 Workfront，系统会将您引导至登录界面。登录后，您即可允许该连接。

>[!NOTE]
>
>* 通过 OAuth 2.0 连接到 Workfront API 不再依赖 API 密钥。
>* 要连接到 Workfront 沙盒环境，您必须在该环境中创建 OAuth2 应用程序，然后使用该应用程序生成的客户端 ID 和客户端密钥建立连接。

### 使用服务器到服务器连接方式连接到 Workfront

1. 在任意 Adobe Workfront 模块中，点击“连接”字段旁的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接类型]</td>
        <td>
          <p>选择 <b>Adobe Workfront 服务器到服务器连接</b>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 实例名称]</td>
        <td>
          <p>输入您的实例名称，即您的域。</p><p>示例：如果您的 URL 为 <code>https://example.my.workfront.com</code>，请输入 <code>example</code>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 实例通道]</td>
        <td>
          <p>输入此连接要访问的环境类型。</p><p>示例：如果您的 URL 为 <code>https://example.my.workfront.com</code>，请输入 <code>my</code>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端 ID]</td>
        <td>请输入您的 Workfront 客户端 ID。您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。打开您要连接的特定应用程序即可查看客户端 ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的 Workfront 客户端密钥。 您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。如果您的 Workfront OAuth2 应用程序没有客户端密钥，您可以重新生成一个。有关操作说明，请参阅 Workfront 文档。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 范围]</td>
        <td>输入此连接所需的相关范围。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 主机前缀]</td>
        <td>在大多数情况下，此值应为 <code>origin</code>。
      </tr>
    </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

   如果您尚未登录 Workfront，系统会将您引导至登录界面。登录后，您即可允许该连接。

>[!NOTE]
>
>* 通过 OAuth 2.0 连接到 Workfront API 不再依赖 API 密钥。
>* 要连接到 Workfront 沙盒环境，您必须在该环境中创建 OAuth2 应用程序，然后使用该应用程序生成的客户端 ID 和客户端密钥建立连接。

## Workfront 模块及其字段

在您配置 Workfront 模块时，Workfront Fusion 会显示以下字段。除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 Workfront 字段。模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。


![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* 如果您在 Workfront 模块中未看到最新字段，可能是由于缓存问题所致。请等待一小时后再试。
>* 来自 Adobe Workfront 的 HTTP 429 状态码不会导致停用，而是会使场景短暂暂停执行。

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL 监控事件]**

当在 Workfront 中创建、更新或删除特定类型的对象时，此触发器模块会实时执行一个场景。

该模块会显示与该 Webhook 相关的所有事件订阅。这包括通过 Fusion 创建的事件订阅，以及直接通过 API 创建的事件订阅。旧版监控事件模块中不提供此事件订阅视图。

该模块会返回与记录关联的所有标准字段，以及连接可访问的任何自定义字段及其值。您可以在场景后续的模块中映射这些信息。

1. 单击 **Webhook** 框右侧的&#x200B;**[!UICONTROL 添加]**。

1. 在显示的&#x200B;**[!UICONTROL 添加挂钩]**&#x200B;框中配置该 Webhook。

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook 名称]</td> 
      <td>输入 Webhook 的名称</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 连接]</td> 
      <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 记录类型]</td> 
      <td>选择您希望该模块监控的 Workfront 记录类型。</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 状态]</td> 
      <td>选择您希望关注旧状态还是新状态。<ul><li><p><b>[!UICONTROL 新状态]</b></p><p>当记录状态更改<b>为</b>指定值时触发场景。</p><p>例如，如果状态设置为 [!UICONTROL New State]，并且筛选条件设置为 [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress]，则当 [!UICONTROL Status] 更改为 [!UICONTROL In Progress] 时，Webhook 会触发场景，而不论之前的状态是什么。 </p></li><li><p><b>[!UICONTROL 旧状态]</b></p><p>当记录状态<b>从</b>指定值发生变化时触发场景。</p><p>例如，如果状态设置为 [!UICONTROL Old State]，并且筛选条件设置为 [!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress]，则当当前 [!UICONTROL In Progress] 状态的记录更改为其他状态时，Webhook 会触发场景。 </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL 事件筛选条件]</p> </td> 
      <td> <p>您可以设置筛选条件，仅观看符合您所选条件的记录。</p> <p>对于每个筛选条件，请输入要评估的字段、运算符以及筛选条件应允许的值。您可以通过添加 AND 规则来使用多个筛选条件。</p> <p><b>注意</b>：您无法编辑现有 Workfront Webhook 中的筛选条件。如需为 Workfront 事件订阅设置不同的筛选条件，请删除当前 Webhook 并创建一个新的。</p> <p>有关事件筛选条件的详细信息，请参阅本文中的 <a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">Workfront 中的时间订阅筛选条件 &gt; [!UICONTROL 监控事件]模块</a>。</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>排除由此连接创建的事件</td> 
      <td>启用此选项可排除通过与此触发器模块相同的连接器创建或更新的事件。这可防止场景因自我触发而不断循环执行。<p><b>注意</b>：任务记录类型不包括此选项。</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 记录来源]</td> 
      <td>
       <p>选择是否要让场景监控 [!UICONTROL New Records Only]、[!UICONTROL Updated Records Only]、[!UICONTROL New and Updated Records] 或 [!DNL Deleted Records Only]。</p>
       <p><b>注意</b>：如果您选择 [!UICONTROL New and Updated Records]，在创建 Webhook 时会生成两个事件订阅（使用相同的 Webhook 地址）。</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

Webhook 创建完成后，您可以查看事件发送到的端点地址。

如需了解更多信息，请参阅 Workfront 文档中事件订阅 API 一文的[事件负载示例](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads)部分。

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

+++

+++ **[!UICONTROL 监控字段]**

当更新指定字段时，此触发器模块会执行场景。该模块会返回所指定字段的旧值和新值。您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择您希望该模块监控的 Workfront 记录类型。</p> <p>例如，如果您希望每次在任务的记录字段更新时开始执行场景，请选择 [!UICONTROL Task]。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 字段]</td> 
   <td>选择您希望该模块监控其更新的字段。这些字段反映了您的 Workfront 管理员已启用用于跟踪的字段。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 输出]</td> 
   <td>选择您希望包含在此模块输出捆绑包中的对象字段。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

+++

+++ **[!UICONTROL 监控记录]**

当新增、更新某一类型的对象或同时发生这两种情况时，此触发器模块会执行场景。该模块会返回与记录关联的所有标准字段，以及连接可访问的任何自定义字段及其值。您可以在场景后续的模块中映射这些信息。

在输出中，模块会指明每条记录是新增的还是更新的。

自上次运行场景以来既被新增又被更新的记录会作为新增记录返回。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 筛选条件]</td> 
   <td> <p>选择是否要让场景监控 [!UICONTROL New Records Only]、[!UICONTROL Updated Records Only] 或 [!UICONTROL New and Updated Records]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择您希望该模块监控的 Workfront 记录类型。</p> <p>例如，如果您希望在每次创建新项目时启动该场景，请选择 [!UICONTROL Project]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td> <p>选择您希望包含在此模块输出捆绑包中的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 引用]</td> 
   <td> <p>选择您希望包含在此模块输出捆绑包中的引用字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td> <p>选择您希望包含在此模块输出捆绑包中的收藏集字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 可选筛选条件]</td> 
   <td> <p>（高级）输入 API 代码字符串，以定义可进一步细化筛选条件的其他参数或代码。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

+++


### 操作

<!--
* [Convert object](#convert-object) 
* [Create a record (attaching custom forms)](#create-a-record-attaching-custom-forms) 
* [Create a record](#create-a-record) 
* [Custom API Call](#custom-api-call) 
* [Delete Record](#delete-record) 
* [Download Document](#download-document) 
* [Misc Action](#misc-action) 
* [Read a Record](#read-a-record) 
* [Update Record](#update-record) 
* [Upload Document](#upload-document)
-->

+++ **[!UICONTROL 转化对象]**

此操作模块可执行以下任一转化：

* 将问题转化为项目
* 将问题转化为任务
* 将任务转化为项目

>[!NOTE]
>
>从 2024 年 7 月起，转化对象时可以包含自定义表单。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 对象类型]</td> 
   <td> <p>选择您希望转化的对象类型。这是对象在转化前的类型。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 转化为]</td> 
   <td>选择您希望将其转化成的对象类型。这是对象在转化后的类型。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;Object&gt; ID]</td> 
   <td> <p>输入对象的 ID。 </p> <p>注意：输入对象 ID 时，您可以先输入对象名称，然后从列表中选择。然后，模块会自动将相应的 ID 填入字段。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 模板 ID]</td> 
   <td> <p>如果您正在转化为项目，请选择要用于该项目的模板 ID。</p> <p>注意：输入对象 ID 时，您可以先输入对象名称，然后从列表中选择。然后，模块会自动将相应的 ID 填入字段。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 自定义表单]</td> 
   <td>选择您希望添加到新转换对象的任何自定义表单，并为表单字段输入相应的值。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 选项]</td> 
   <td> <p>在转化对象时启用您所需的任何选项。可用选项取决于转化的源对象和目标对象类型。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 复制原生字段]</td> 
   <td> <p>启用此选项可将原始对象中的原生字段复制到新对象。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 复制自定义表单]</td> 
   <td> <p>启用此选项可将原始对象中的原生字段复制到新对象。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 创建记录]** 

此操作模块会在 Workfront 中创建一个对象（例如项目、任务或问题），并允许您为新对象添加自定义表单。该模块允许您选择对象的哪些字段可在模块中使用。

您需要指定记录的 ID。

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。您可以在场景后续的模块中映射这些信息。

请确保您提供了所需的最少输入字段。例如，如果您要创建问题，则必须在项目 ID 字段中提供有效的父项目 ID，以指明该问题在 Workfront 中归属的位置。您可以使用映射面板从场景中的其他模块映射此信息，也可以通过输入名称并从列表中选择的方式手动输入。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择您希望该模块创建的 Workfront 记录类型。</p> <p>例如，如果您要创建项目，请从下拉列表中选择 [!UICONTROL Project]。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 选择要映射的字段]</td> 
   <td> <p>选择您希望用于数据输入的字段。这样您无需浏览不需要的字段，就能直接使用这些字段。随后您可以向这些字段输入或映射数据。</p> <p>对于自定义表单中的字段，请使用<b>[!UICONTROL 附上自定义表单]</b>字段。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 附上自定义表单]</td> 
   <td>选择您希望添加到新对象的自定义表单，勾选您要输入值的字段，然后为这些字段输入或映射相应的值。</td> 
  </tr> 
 </tbody> 
</table>

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

>[!NOTE]
>
>* 输入对象 ID 时，您可以先输入对象名称，然后从列表中选择。然后，模块会自动将相应的 ID 填入字段。
>* 在为自定义字段或[!UICONTROL 注释]对象（评论或回复）输入文本时，您可以在[!UICONTROL 注释文本]字段中使用 HTML 标记来创建富文本，例如粗体或斜体。
>



>[!NOTE]
>
>用户会以“停用”和“待审批”状态创建。如果您的组织已迁移到 Adobe Admin Console，并且“待审批”标记在几分钟内未移除，您可以手动批准该用户。
>
>* **解决单个用户**
>
>      您可以在“用户”列表中解决单个用户。
>
>      1. 在“用户”列表中选择一个或多个用户。
>      1. 点击列表标题中的三点菜单。
>      1. 选择&#x200B;**批准**。
>      1. 几分钟后刷新页面。
>
>* **解决批量新增的用户**
>
>   要解决批量新增用户的问题，您可以直接将这批用户添加到 Adobe Admin Console 中。
>
>   有关操作说明，请参阅 Adobe 文档中的[管理多个用户 | 批量上传 CSV](https://helpx.adobe.com/cn/enterprise/using/bulk-upload-users.html)。

+++

<!--

+++ **[!UICONTROL Create Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Create a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module creates an object, such as a project, task, or issue in Workfront. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

Make sure you provide the minimum number of input fields. For example, if you want to create an issue, you need to provide a valid parent project ID in the Project ID field to indicate where the issue should live in Workfront. You can use the mapping panel to map this information from another module in your scenario, or you can enter it manually by typing in the name and then selecting it from the list.

This module does not attach custom forms when creating the object. To attach custom forms while creating an object, use the [!UICONTROL Create a record (attaching custom forms)] module.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to create.</p> <p>For example, if you want to create a Project, select [!UICONTROL Project] from the dropdown list.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL 自定义 API 调用]**

此操作模块允许您向 Workfront API 发起自定义的已经过身份认证的调用。通过这种方式，您可以构建其他 Workfront 模块无法实现的数据流自动化。

该模块会返回以下信息：

* **[!UICONTROL 状态代码]**（数字）：指示 HTTP 请求是成功还是失败。这些是标准状态码，您可以在网上查阅其含义。
* **[!UICONTROL 标头]**（对象）：提供与输出正文无关的响应/状态码的详细上下文信息。并非所有出现在响应标头中的字段都是有用的响应标头，因此部分信息可能对您不重要。

  响应标头的内容取决于您在配置模块时选择的 HTTP 请求类型。

* **[!UICONTROL 正文]**（对象）：根据您在配置模块时选择的 HTTP 请求类型，您可能会收到返回的数据。例如 GET 请求返回的数据，这些内容都会包含在此对象中。

您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>输入相对于 <code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code> 的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API 版本]</td> 
   <td>选择您希望模块使用的 Workfront API 版本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。如需了解详情，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 中的 HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。这将决定请求的内容类型。</p> <p>例如，<code> {"Content-type":"application/json"}</code></p> <p>注意：如果出现错误且难以确定来源，请根据 Workfront 文档修改请求标头。如果您的自定义 API 调用返回 422 HTTP 请求错误，请尝试使用 <code>"Content-Type":"text/plain"</code> 标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> <p>提示：建议通过 JSON 正文传递信息，而不是作为查询参数。</p> </td> 
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

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

+++

+++ **[!UICONTROL 删除记录]**

此操作模块会在 Workfront 中删除对象，例如项目、任务或问题。

您需要指定记录的 ID。

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 强制删除]</td> 
   <td>启用此选项可确保记录删除，即使 Workfront UI 需要删除确认。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 异步删除]</td> 
   <td>启用此选项可允许模块异步删除。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>输入您希望模块删除的记录的唯一 Workfront ID。</p> <p>要获取 ID，请在浏览器中打开此 Workfront 对象，并复制 URL 中 “ID=” 后面的文本。例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td>选择您希望该模块删除的 Workfront 记录类型。</td> 
  </tr> 
 </tbody> 
</table>

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

>[!NOTE]
>
>为避免因异步操作导致记录未成功删除，建议采用以下场景配置。
>
>1. 同步删除记录。
>1. 在“删除记录”模块中添加错误处理规则，以忽略因 40 秒超时导致的错误。


+++

+++ **[!UICONTROL 下载文档]**

此操作模块会从 Workfront 下载文档。

您需要指定记录的 ID。

该模块会返回文档的内容、文件名、文件扩展名以及文件大小。您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文档 ID]</td> 
   <td> <p>映射或手动输入您希望模块下载的文档的唯一 Workfront ID。</p> <p>要获取 ID，请在浏览器中打开此 Workfront 对象，并复制 URL 中 “ID=” 后面的文本。例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

+++

### **获取预签名文件 URL**

此操作模块获取预签名的文件 URL，以供其他 API 使用。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文档 ID]</td> 
   <td> <p>映射或手动输入您希望获取预签名 URL 的文档的唯一 Workfront ID。</p> <p>要获取 ID，请在浏览器中打开此 Workfront 对象，并复制 URL 中 “ID=” 后面的文本。例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL 到期时间]</td> 
   <td> <p>输入或映射此 URL 过期前可存在的分钟数。默认值为 1 分钟。</p><p>要更改此值，必须由 Workfront Fusion 团队启用该参数。如果未启用，无论您输入什么数字，该值都会保持 1 分钟。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++ **[!UICONTROL 其他操作]**

此操作模块允许您对 API 执行操作。

>[!NOTE]
>
>自 2024 年 7 月起，`convertToProject` 操作新增字段 `copyCategories`。 当设置为 `TRUE` 时，所有自定义表单都会包含在该问题转化后的项目中。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择此模块需要交互的 Workfront 记录类型。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 操作]</td> 
   <td> <p>选择您希望该模块执行的操作。</p> <p>根据您选择的[!UICONTROL 记录类型]和[!UICONTROL 操作]，可能需要填写其他字段。某些设置组合可能仅需提供记录 ID，而其他组合（例如将<strong>[!UICONTROL 记录类型]</strong>设为“项目”，将<strong>[!UICONTROL 操作]</strong>设为[!UICONTROL 附加模板]）则需要额外信息（例如对象 ID 和模板 ID）。</p><p>若要查看某些操作可用的选项，请参阅本文中的<a href="#misc-action-options" class="MCXref xref">其他操作选项</a>。</p> <p>有关各字段的详细说明，请参阅 <a href="http://developer.workfront.com/">Workfront 开发人员文档</a>。 <p><strong>注意</strong>：开发人员文档网站仅涵盖至 API 版本 14，但其中内容仍对 API 调用具有参考价值。 </p> 
    <ol> 
     <li value="1"> <p>在 Workfront 开发人员文档页面中，从左侧导航中选择记录类型。以下类型各自拥有独立的页面：</p> 
      <ul> 
       <li> <p>[!UICONTROL 项目]</p> </li> 
       <li> <p>[!UICONTROL 任务]</p> </li> 
       <li> <p>[!UICONTROL 问题]</p> </li> 
       <li> <p>[!UICONTROL 用户]</p> </li> 
       <li> <p>[!UICONTROL 文档]</p> </li> 
      </ul> <p>对于其他记录类型，选择<b>[!UICONTROL 其他对象和端点]</b>，并在按字母顺序排列的页面中查找相应的记录类型。</p> </li> 
     <li value="2"> <p>在相应记录类型的页面中，使用搜索功能（Ctrl-F 或 Cmd-F）查找所需的操作。</p> </li> 
     <li value="3"> <p>查看所选操作下可用字段的说明。</p> </li> 
    </ol> <p>注意：  <p>通过 Workfront [!UICONTROL 其他操作]模块创建校样时，最佳做法是先创建一个不带任何高级选项的校样，然后再使用 [!DNL Workfront Proof] SOAP API 更新校样。</p><p>如需了解使用 Workfront API（此模块所使用的 API）创建校样的更多信息，请参阅<a href="https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">通过 Adobe Workfront API 创建校样时添加高级校对选项</a>。</p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>输入或映射该模块要交互的记录的唯一 Workfront ID。<p>要获取 ID，请在浏览器中打开此 Workfront 对象，并复制 URL 中 “ID=” 后面的文本。例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

#### 其他操作选项

##### 任务

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>操作</th> 
   <th>选项</th> 
  </tr> 
  <tr> 
   <td>复制</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearConstraints</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>清除财务数据</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>清除提醒通知</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>移动</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearDocuments</li>
   <li>clearConstraints</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>清除财务数据</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>清除提醒通知</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

##### 问题

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>操作</th> 
   <th>选项</th> 
  </tr> 
  <tr> 
   <td>复制</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearPermissions</li>
   <li>clearProgress</li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>转化为任务</td> 
   <td>
   <ul>
   <li>preserveIssue<p>保持原有问题，并将其解决方案关联到此任务</p></li>
   <li>preservePrimaryContact<p>允许问题的主要联系人访问此任务</p></li>
   <li>preserveCompletionDate<p>保留问题的规划完成日期</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>转化为项目</td> 
   <td>
   <ul>
   <li>preserveIssue<p>保持原有问题，并将其解决方案关联到此任务</p></li>
   <li>preservePrimaryContact<p>允许问题的主要联系人访问此任务</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



##### 项目

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>操作</th> 
   <th>选项</th> 
  </tr> 
  <tr> 
   <td>复制</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>清除财务数据</p></li>
   <li>clearPermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>清除提醒通知</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>附加模板 / 另存为模板</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignments</li>
   <li>clearBillingRates</li>
   <li>clearConstraints</li>
   <li>clearDeliverables<p>清除目标</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>清除财务数据</p></li>
   <li>clearHourTypes</li>
   <li>clearIssueSetup<p>清除队列属性和问题设置</p></li>
   <li>clearPredecessors</li>
   <li>clearRisks</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>清除提醒通知</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL 读取记录]**

此操作模块从单个记录中检索数据。

您需指定记录的 ID。您还可以指定要让模块读取的关联记录。

例如，如果模块正在读取的记录是项目，您可以指定读取该项目的任务。

模块会根据您选择的输出字段返回一个数据数组。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL 连接]</td>
    <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 记录类型]</td>

<td>选择您希望模块读取的 Workfront 对象类型。</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 输出]</td>

<td> <p>选择要包含在此模块输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 输出自定义表单]</td>
     <td> <p>选择要在此模块的输出捆绑包中包含的自定义表单，然后从这些自定义表单中选择需要包含在输出中的具体字段。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 引用]</td>
   <td>选择您希望包含在输出中的任何引用字段。</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 收藏集]</td>
   <td>选择您希望包含在输出中的任何引用字段。</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>输入您希望模块读取的记录的唯一 Workfront ID。</p> <p>要获取 ID，请在浏览器中打开此 Workfront 对象，并复制 URL 中 “ID=” 后面的文本。例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

+++

<!--

+++ **[!UICONTROL Read a Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Read a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module retrieves data from a single record.

You specify the ID of the record. You can also specify which related records you want the module to read.

For example, if the record that the module is reading is a project, you can specify that you want the project's tasks read.

The module returns an array of data from the output fields you specified.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
  
   <td>Choose the Workfront object type that you want the module to read.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
  
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Enter the unique Workfront ID of the record that you want the module to read.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++

-->

+++ **更新事件负载版本**

Workfront 最近发布了新版事件订阅服务。该新版并未更改 Workfront API，而是更新了事件订阅功能。此操作模块用于更新该场景中使用的事件负载版本。

有关新版事件订阅的更多信息，请参阅 Workfront 文档中[事件订阅版本控制](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning)

如需了解在事件订阅升级期间如何保护 Workfront Fusion 场景（包括网络研讨会录像），请参阅[事件订阅 V2 升级期间保护您的 Fusion 场景](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=zh-Hans)。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 版本]</td> 
   <td> 选择要用于此负载的事件订阅版本。 </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **更新记录**


此操作模块用于更新对象，例如项目、任务或问题。该模块允许您选择对象的哪些字段可在模块中使用。

您需要指定记录的 ID。

该模块会返回对象的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>输入您希望模块更新的记录的唯一 Workfront ID。</p> <p>要获取 ID，请在浏览器中打开此 Workfront 对象，并复制 URL 中 “ID=” 后面的文本。例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>选择您希望该模块更新的 Workfront 记录类型。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>选择您希望用于数据输入的字段。这样您无需浏览不需要的字段，就能直接使用这些字段。随后您可以向这些字段输入或映射数据。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>选择要为新记录提供字段值的自定义表单。选择表单后，为该表单中的字段输入数据。<p> 若要为此模块中附加的表单提供字段值，请在要映射的字段区域中包含自定义表单 ID。</td> 
  </tr> 
 </tbody> 
</table>

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

>[!NOTE]
>
> 在为自定义字段或[!UICONTROL 注释]对象（评论或回复）输入文本时，您可以在[!UICONTROL 注释文本]字段中使用 HTML 标记来创建富文本，例如粗体或斜体。


+++

<!--

+++ **[!UICONTROL Update Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Update a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module updates an object, such as a project, task, or issue. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  object and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Enter the unique Workfront ID of the record that you want the module to update.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to update.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need. You can then enter or map data into these fields.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL 上传文档]**

此操作模块会将文档上传到某个 Workfront 对象，例如项目、任务或问题。该模块以分块方式上传文档，从而让 Workfront 更顺畅地处理上传过程。

此模块能够处理比旧版模块更大的文件，并正在逐步向拥有 Ultimate Workfront 套餐的组织转出。

您需要指定文档的存放位置、要上传的文件，以及可选的文件新名称。

该模块会返回文档的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 相关记录 ID]</td> 
   <td>请输入要上传文档的记录的唯一 Workfront ID。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 相关记录类型]</td> 
   <td>选择要让该模块上传文档的 Workfront 记录类型。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文件夹 ID]</td> 
   <td>根据关联记录的类型，您可能需要填写或映射文件夹 ID。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 来源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

有关可与此模块一起使用的 Workfront 对象类型列表，请参阅[每个 Workfront 模块可用的 Workfront 对象类型](#workfront-object-types-available-for-each-workfront-module)。

+++

<!--

+++ **[!UICONTROL Upload Document (Legacy)]**

This action module uploads a document to a Workfront object, such as a project, task, or issue. It uploads the entire document at once. 

You specify the location for the document, the file you want to upload, and an optional new name for the file.

The module returns the ID of the document and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Enter the unique Workfront ID of the record to which you want to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Select the type of Workfront record where you want the module to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Depending on the type of related record, you may need to enter or map a folder ID.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).


+++
-->

### 搜索

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL 读取关联记录]**

此搜索模块会从指定的父对象中读取与您设定的搜索查询匹配的记录。

您可以指定需要在输出中包含的字段。您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择您要读取其关联记录的父记录类型（Workfront 对象）。</p> <p>有关可与此模块一起使用的 Workfront 对象类型列表，请参阅本文中的<a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">每个 Workfront 模块可用的 Workfront 对象类型</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 父记录 ID]</td> 
   <td> <p>输入或映射要读取其关联记录的父记录 ID。</p> <p>要获取 ID，请在浏览器中打开此 Workfront 对象，并复制 URL 中 “ID=” 后面的文本。例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 收藏集]</td> 
   <td>选择或映射要由模块读取的子记录类型。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在此模块输出捆绑包中的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 搜索]**

此搜索模块会在 Workfront 中的对象内查找与您指定的搜索查询匹配的记录。

您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择您希望模块搜索的 Workfront 记录类型。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 自定义表单列表]</td> 
   <td> <p>请选择至少一个自定义表单。这些自定义表单中的字段将可用于搜索查询。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 结果集]</td> 
   <td>选择一个选项，以指定模块是仅获取符合搜索条件的首条结果，还是获取所有匹配结果。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 最大]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 搜索条件字段]</td> 
   <td> <p>选择要用于搜索条件的字段。这些字段随后将显示在“搜索条件”下拉菜单中。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 搜索条件]</td> 
   <td> <p>输入要搜索的字段、查询中要使用的运算符，以及该字段中要搜索的值。</p> <p>注意：请勿在搜索条件中使用 <code>username </code>。 在对 Workfront 的 API 查询中包含 <code>username </code> 会导致用户登录到 Workfront，从而无法成功搜索。</p> <p>注意：<code>In</code> 和 <code>NotIn</code> 适用于数组。输入必须使用数组格式。</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在此模块输出中的字段。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 引用]</td> 
   <td>选择您希望包含在搜索中的任何引用字段。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 收藏集]</td> 
   <td>选择要添加到搜索中的任何收藏集。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 搜索（旧版）]**

>[!IMPORTANT]
>
>此模块已由“搜索记录”模块取代。我们建议在新场景中使用该模块。
>使用此模块的现有场景仍将按预期运行。该模块将于 2025 年 5 月从模块选择器中移除。

此搜索模块会在 Workfront 中的对象内查找与您指定的搜索查询匹配的记录。

您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择您希望模块搜索的 Workfront 记录类型。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 结果集]</td> 
   <td>选择一个选项，以指定模块是仅获取符合搜索条件的首条结果，还是获取所有匹配结果。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 最大]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 搜索条件字段]</td> 
   <td> <p>选择要用于搜索条件的字段。这些字段随后将显示在“搜索条件”下拉菜单中。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 搜索条件]</td> 
   <td> <p>输入要搜索的字段、查询中要使用的运算符，以及该字段中要搜索的值。</p> <p>注意：请勿在搜索条件中使用 <code>username </code>。 在对 Workfront 的 API 查询中包含 <code>username </code> 会导致用户登录到 Workfront，从而无法成功搜索。</p> <p>注意：<code>In</code> 和 <code>NotIn</code> 适用于数组。输入必须使用数组格式。</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在此模块输出中的字段。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 引用]</td> 
   <td>选择您希望包含在搜索中的任何引用字段。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 收藏集]</td> 
   <td>选择要添加到搜索中的任何收藏集。</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--not visible Jan 6, 2025

+++ **[!UICONTROL Search (Legacy)]**

This search module looks for records in an object in Workfront that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Select an option to specify whether you want the module to get the first result that matches your search criteria or all the results that match it.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the output for this module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Select any reference fields that you want to include in the search.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Select any collections that you want to add to the search.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++-->

## 每个 Workfront 模块可用的 Workfront 对象类型

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**各 Workfront 触发器模块支持的对象类型**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL 监控记录]</th> 
   <th>[!UICONTROL 监控字段]</th> 
   <th>[!UICONTROL 监控事件]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>审批流程</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>任务</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>基准</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 账单记录 </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>计费费率</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>公司</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>仪表板</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档文件夹</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>文档请求</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>文档版本</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>费用</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>费用类型</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>组</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>小时</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>小时数类型</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>问题</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>开发周期</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>工作角色</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>日记帐条目</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑路径</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>注释</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>注释标签</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>项目组合</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目群</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目用户</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>校样审批</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>保留时间* </td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>报告</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>风险</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险类型</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>步骤审批者</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>任务</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>团队</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>模板任务</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>时间表</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>用户</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>更新</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**各个 Workfront 操作模块支持的对象类型**

>[!NOTE]
>
>本表未包含[!UICONTROL 下载文档]模块，因为该模块的配置不涉及 Workfront 对象类型。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL 创建记录]</th> 
   <th>[!UICONTROL 更新记录]</th> 
   <th>[!UICONTROL 删除记录]</th> 
   <th>[!UICONTROL 上传文档]</th> 
   <th>[!UICONTROL 读取记录]</th> 
   <th>[!UICONTROL 自定义 API 调用]</th> 
   <th>[!UICONTROL 其他操作]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>审批流程</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>任务</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>基准</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
   <tr> 
   <td>账单记录</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>计费费率</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>公司</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档文件夹</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档版本</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>汇率</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>费用</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>费用类型</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>外部文档</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>组</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>小时</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>小时数类型</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>问题</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>开发周期</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>工作角色</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>日记帐条目</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>里程碑</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑路径</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>注释</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>注释标签</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>项目组合</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目群</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目用户</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>保留时间* </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险类型</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>步骤审批者</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>任务</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>团队</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板任务</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>时间表</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>用户</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>更新</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**各个 Workfront 搜索模块支持的对象类型**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL 搜索]</th> 
   <th>[!UICONTROL 读取相关记录]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>审批流程</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>任务</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>账单记录</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>计费费率</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>公司</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档文件夹</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档版本</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>费用</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>费用类型</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>组</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>小时</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>小时数类型</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>问题</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>开发周期</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>工作角色</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>日记帐条目</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑路径</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>注释</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>注释标签</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>项目组合</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目群</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>项目</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目用户</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>保留时间* </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险类型</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>步骤审批者</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>任务</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>团队</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板任务</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>时间表</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>用户</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>用户委托</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

我们建议您再次确认，以确保其行为符合您的预期。

+++

## Workfront > [!UICONTROL 监控事件]模块中的事件订阅筛选条件

>[!NOTE]
>
>* 我们强烈建议您在[!UICONTROL 监控事件]模块中使用事件订阅筛选条件。
>
>* Workfront 最近发布了新版事件订阅服务。该新版并未更改 Workfront API，而是更新了事件订阅功能。此操作模块用于更新该场景中使用的事件负载版本。
>
>   有关新版事件订阅的更多信息，请参阅 Workfront 文档中[事件订阅版本控制](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning)
>
>   如需了解在事件订阅升级期间如何保护 Workfront Fusion 场景（包括网络研讨会录像），请参阅[事件订阅 V2 升级期间保护您的 Fusion 场景（https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182?profile.language=zh-Hans）]。

Workfront 的[!UICONTROL 监控事件]模块会根据一个在 Workfront API 中创建事件订阅的 Webhook 来触发场景。事件订阅是一组数据，用于确定哪些事件会发送至该 Webhook。例如，如果您设置一个监控问题的[!UICONTROL 监控事件]模块，则该事件订阅只会将与问题相关的事件发送过来。

通过使用事件订阅筛选条件，Fusion 用户可以创建更符合其使用场景的事件订阅。例如，您可以在 Workfront API 中设置事件订阅，使其仅将某个项目下的问题发送到 Webhook，从而确保[!UICONTROL 监控事件]模块只会在该项目的问题上触发。创建更精确的触发条件有助于减少无关触发，从而优化场景设计。

这与在 Workfront Fusion 场景中设置筛选条件不同。如果未配置事件订阅筛选条件，Webhook 将接收与所选对象类型相关的所有事件。其中大多数事件与场景无关，因此必须在场景继续执行前进行过滤。

Workfront > “监控事件”筛选条件支持以下运算符：

* 等于
* 不等于
* 大于
* 小于
* 大于或等于
* 小于或等于
* 包含
* 已存在
   * 此运算符不需要指定值，因此不会显示“值”字段。
* 不存在
   * 此运算符不需要指定值，因此不会显示“值”字段。
* 已更改
   * 此运算符不需要指定值，因此不会显示“值”字段。
   * 此运算符会忽略“状态”字段。
   * 使用 `Changed` 时，请在&#x200B;**记录来源**&#x200B;字段中选择&#x200B;**仅更新事件**。

>[!IMPORTANT]
>
>您无法编辑现有 Workfront Webhook 中的筛选条件。如需为 Workfront 事件订阅设置不同的筛选条件，请删除当前 Webhook 并创建一个新的。

>[!INFO]
>
>**示例：**&#x200B;假设一个场景需要处理分配给特定用户 Ana 的新问题。
>
>### 使用事件订阅筛选条件进行事件筛选（推荐）
>
>通过事件筛选条件，可将 Webhook 配置为在新建问题并将其分配给 Ana 时触发场景。Ana 的用户 ID 为 b378489d8f7cd3cee0539260720a84b7。
>
>![事件筛选条件](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>如果当天创建了 100 个问题，但只有 2 个分配给 Ana，则场景仅会执行两次。
>
>### 在场景内部筛选事件（不推荐）
>
>若要筛选事件，仅处理分配给 Ana 的问题，可在[!UICONTROL 监控事件]模块之后创建一个筛选条件。
>
>![没有事件筛选条件](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>如果当天创建了 100 个问题，但只有 2 个分配给 Ana，则场景将执行 100 次。尽管其中 98 次执行会在筛选条件处停止，但触发器模块仍需在每次执行中消耗数据并执行操作。

有关 Workfront 事件订阅的更多信息，请参阅 [FAQs - 事件订阅](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq)。

有关 Webhook 的更多信息，请参阅 [Adobe Workfront Fusion 中的即时触发器（Webhook）](/help/workfront-fusion/references/modules/webhooks-reference.md)

有关在场景中添加筛选条件的更多信息，请参阅[向场景添加筛选条件](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md)。
