---
title: Box 模块
description: 在Adobe Workfront Fusion场景中，您可以自动执行使用Box的工作流，并将其连接到多个第三方应用程序和服务。 监视指定的文件夹，以检查文件更改、修改和删除现有文件，或将新文件上传到文件夹。
author: Becky
feature: Workfront Fusion
exl-id: 9e741dce-05a6-4e13-8d58-fbe3b4900d7e
source-git-commit: 72abd9b5aa73d54edd73dc16f7695d2b01cc8624
workflow-type: tm+mt
source-wordcount: '1548'
ht-degree: 25%

---

# Box 模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Box]的工作流，并将其连接到多个第三方应用程序和服务。 监视指定的文件夹，以检查文件更改、修改和删除现有文件，或将新文件上传到文件夹。

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

要使用 [!DNL Box] 模块，您必须拥有一个 [!DNL Box] 帐户。

## 框API信息

Box连接器使用下列方法：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td> https://api.box.com/2.0
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 版本</td> 
   <td> v2.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v3.0.3</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Box] 模块及其字段

在您配置 [!DNL Box] 模块时，Workfront Fusion 会显示以下字段。除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Box] 字段。模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

* [[!UICONTROL 新文件事件]](#new-file-event)
* [新建文件夹事件](#new-folder-event)
* [[!UICONTROL 监视文件]](#watch-files)

#### [!UICONTROL 新文件事件]

此即时触发器模块会在文件上发生选定操作时启动方案。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>选择要用于监视传出消息的webhook，或添加webhook。 </p><p>要添加webhook，请单击<strong>[!UICONTROL 添加]</strong>并输入webhook的名称和连接、要监视的文件以及要监视的触发器。</p> <p> 有关将您的[!UICONTROL Box]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">连接到服务 — 基本说明</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 新建文件夹事件

此即时触发器模块会在文件夹中发生选择操作时启动方案。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>选择要用于监视传出消息的webhook，或添加webhook。 </p><p>要添加webhook，请单击<strong>[!UICONTROL 添加]</strong>并输入webhook的名称和连接、要监视的文件夹以及要监视的触发器。</p> <p> 有关将您的[!UICONTROL Box]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">连接到服务 — 基本说明</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 监视文件]

在监视的文件夹中添加新文件或更新现有文件时，此触发器模块将启动一个方案。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将[!DNL Box]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  <tr> 
   <td role="rowheader">在文件夹中监视</td> 
   <td> <p>选择要监视的文件夹。 场景可以监视单个文件夹。</p> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">观看</td> 
   <td> <p>选择要监视的文件类型。</p> 
    <ul> 
     <li> <p><strong>仅新文件</strong> </p> <p>添加新文件后，将开始此方案。</p> </li> 
     <li> <p><strong>新文件和所有更改</strong> </p> <p>当添加文件，或修改文件内容或文件属性（如文件名称）时，将开始使用此方案。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>最大下载文件数</p> </td> 
   <td> <p>输入您希望模块在每个方案执行周期中返回的最大文件数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

<!--
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Update a file]](#update-a-file)
* [[!UICONTROL Upload] a file](#upload-a-file)
-->
* [创建文件夹](#create-a-folder)
* [获取文件夹](#get-a-folder)
* [获取文件夹元数据](#get-folder-metadata)
* [进行API调用](#make-an-api-call)
* [更新文件夹元数据](#update-folder-metadata)

<!--
#### [!UICONTROL Delete a file]

This action module deletes a file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to delete.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

This action module downloads a file.

You specify the ID of the file.

>[!NOTE]
>
>This module is useful for providing files to subsequent modules.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to retrieve.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a file] 

This action module updates a file.

You specify the ID of the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Enter or map the unique ID of the file that you want the module to update.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file] 

This action module uploads a file.

You specify the file. You can also provide a new filename for the file.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL Box] account to Workfront Fusion, see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to Adobe Workfront Fusion - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td> <p>Select the folder where you want to upload the file.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If this module is not successful, consider the following:
>
>* The size of the file might exceed the maximum file size limit for your [!DNL Box] plan, or you may have used all of your [!DNL Box] account's storage quota. To get more storage space, delete existing files from [!DNL Box] or upgrade your [!DNL Box] account.
>* [!DNL Box] does not upload more than one files with the same name to a single folder. If the destination folder contains a file with the same name as the file being uploaded, the scenario run terminates with an error. To avoid this, rename the file. If you want to update the file, use the **[!UICONTROL Update a file]** module.
-->

#### 创建文件夹

此操作模块在指定的父文件夹内创建新的空文件夹。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Box]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 名称]</td> 
   <td> <p>输入或映射新文件夹的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 父文件夹]</td> 
   <td> <p>选择要创建新文件夹的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹上传电子邮件访问权限]</td> 
   <td> <p>设置此参数后，用户可以通过电子邮件将文件发送到为此文件夹自动创建的电子邮件地址。 协作者选项只允许协作者使用注册的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 同步状态]</td> 
   <td> <p>指定是否应将文件夹同步到用户设备。 Box Sync（已停用）使用，Box Drive不使用。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取文件夹

此操作模块检索文件夹的详细信息，包括文件夹中的前100个条目。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Box]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹]</td> 
   <td> <p>选择要检索其详细信息的文件夹。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取文件夹元数据

此操作模块按文件夹ID检索文件夹元数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Box]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 作用域]</td> 
   <td> <p>选择要用于此元数据检索的范围。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹]</td> 
   <td> <p>选择要为其检索元数据的文件夹。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 进行API调用

此操作模块对Box API进行自定义调用。



<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Bynder]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-bynder-to-workfront-fusion" class="MCXref xref">将[!DNL Bynder]连接到Workfront Fusion </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>输入相对于 <code>https://api.box.com</code> 的路径。 <p>示例： <code>/2.0/users/me</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如： <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
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

#### 更新文件夹元数据

此操作模块创建或更新文件夹的元数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Box]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 作用域]</td> 
   <td> <p>选择要用于此元数据更新的范围。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹]</td> 
   <td> <p>选择要为其更新元数据的文件夹。</p> </td> 
  </tr> 
 </tbody> 
</table>


### 搜索

#### 搜索内容

此搜索模块会搜索可供用户或整个企业使用的项目。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Box]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>输入或映射要搜索的字符串。 此查询根据项目名称、说明、文件的文本内容以及不同项目类型的各种其他字段进行匹配。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 作用域]</td> 
   <td> <p>选择是搜索与用户相关的内容，该用户的凭据用于此模块中使用的连接，还是搜索与整个企业相关的内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 类型]</td> 
   <td> <p>选择是要搜索文件、文件夹还是Web链接。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 排序]</td> 
   <td> <p>选择您要按相关性还是按修改日期排序。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 垃圾桶内容]</td> 
   <td> <p>选择是要搜索置入垃圾桶的内容还是尚未置入垃圾桶的内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 父文件夹ID]</td> 
   <td> <p>若要在特定文件夹中搜索，请针对要搜索的每个文件夹，单击“添加项目”<b></b>并输入文件夹的ID。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 创建自]</td> 
   <td> <p>要搜索在特定日期范围内创建的资产，请输入该范围内的最早日期。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 已创建到]</td> 
   <td> <p>要搜索在特定日期范围内创建的资产，请输入该范围内的最新日期。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 更新自]</td> 
   <td> <p>要搜索在特定日期范围内更新的资产，请输入该范围内的最早日期。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 已更新至]</td> 
   <td> <p>要搜索在特定日期范围内更新的资产，请输入该范围内的最新日期。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 字段]</td> 
   <td> <p>对于要在模块的响应中返回的每个属性，单击<b>添加项</b>并输入字段。</p><p>这可用于请求标准响应中通常不返回的字段。 请注意，指定此参数将导致响应中不会返回任何标准字段，除非明确指定。 </p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件扩展名]</td> 
   <td> <p>要将搜索限制到特定的文件扩展名，请输入以逗号分隔的文件扩展名列表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 大小自]</td> 
   <td> <p>要搜索特定大小范围内的资源，请输入该范围的小端（字节）。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 大小为]</td> 
   <td> <p>要搜索特定大小范围内的资源，请输入该范围的大端（以字节为单位）。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 所有者用户ID]</td> 
   <td> <p>要搜索特定用户拥有的资产，请输入以逗号分隔的所有者ID列表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射您希望模块在每个执行周期中返回的最大结果数。</p> </td> 
  </tr> 
 </tbody> 
</table>


