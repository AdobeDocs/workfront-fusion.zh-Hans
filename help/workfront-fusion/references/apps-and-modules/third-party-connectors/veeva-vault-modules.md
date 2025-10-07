---
title: Veeva Vault模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Veeva Vault的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
source-git-commit: 6e7125bee77526caa93edc17f05b75bdfd7d7ac4
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 3%

---

# Veeva Vault模块

在Adobe Workfront Fusion场景中，您可以自动使用Veeva Vault的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用Veeva Vault模块，您必须具有Veeva Vault帐户。

## Veeva Vault模块及其字段

配置Veeva Vault模块时，Workfront Fusion会显示以下列出的字段。 除此之外，可能还会显示其他Veeva Vault字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 文档

* [创建单个文档](#create-a-single-document)
* [创建多个文档](#create-multiple-documents)
* [删除单个文档](#delete-a-single-document)
* [导出文档](#export-documents)
* [获取单个文档](#get-a-single-document)
* [启动用户操作](#initiate-user-action)
* [列出文档](#list-documents)
* [检索文档导出结果](#retrieve-document-export-results)
* [更新多个文档](#update-multiple-documents)
* [更新单个文档](#update-a-single-document)

#### 创建单个文档

此模块创建单个文档、文件夹或模板。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择您要创建文档、活页夹还是模板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>选择字段</p> </td> 
   <td> <p>选择要为其输入数据的字段，然后在这些字段中输入数据。</td> 
  </tr> 
 </tbody> 
</table>

#### 创建多个文档

此模块使用CSV文件创建多个文档或模板。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择您要创建模板还是文档</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>文件数据</p> </td> 
   <td> <p>映射将用于创建文档的CSV文件。</td> 
  </tr> 
 </tbody> 
</table>

#### 删除单个文档

此模块删除单个文档、文件夹或模板。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择您要删除文档、活页夹还是模板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>文档ID/绑定器ID/模板名称</p> </td> 
   <td> <p>选择要删除的字段。</td> 
  </tr> 
 </tbody> 
</table>

#### 导出文档

此模块可导出您指定的文档，包括源、演绎版和文本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择您要删除文档、活页夹还是模板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>来源</p> </td> 
   <td> <p>启用此选项以在导出中包括源文件。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>节目</p> </td> 
   <td> <p>启用此选项以在导出中包括格式副本文件。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>所有版本</p> </td> 
   <td> <p>启用此选项以在导出中包括文档文件的所有版本。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>文本</p> </td> 
   <td> <p>启用此选项以在导出中包括源文档文本。</p></td> 
  </tr> 
 </tbody> 
</table>

#### 获取单个文档

此模块检索单个文档、文件夹或模板的元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择是要检索文档、文件夹还是模板的数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>文档ID/绑定器ID/模板名称</p> </td> 
   <td> <p>选择要为其检索数据的字段。</td> 
  </tr> 
 </tbody> 
</table>

#### 启动用户操作

此模块对文档和绑定器启动操作，例如发送文档以供审阅或更改其状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择是对文档还是对文件夹执行操作。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>文档/文件夹</p> </td> 
   <td> <p>选择要对其执行操作的文档或文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>文档版本/绑定器版本</p> </td> 
   <td> <p>选择要对其执行操作的文档或文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>操作</p> </td> 
   <td> <p>选择要对文档或文件夹执行的操作。</td> 
  </tr> 
 </tbody> 
</table>

#### 列出文档

此模块列出选定类型的所有文档。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择您要列出文档、绑定器还是模板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">返回结果的最大数目</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

#### 检索文档导出结果

此模块返回先前请求的文档导出的结果。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>作业ID</p> </td> 
   <td> <p>输入或映射要为其返回结果的作业的ID。 </p> </td> 
  </tr> 
  </tbody> 
</table>

#### 更新多个文档

此模块使用CSV文件更新多个文档或模板。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择您要创建模板还是文档</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>文件数据</p> </td> 
   <td> <p>映射将用于创建文档的CSV文件。</td> 
  </tr> 
 </tbody> 
</table>

#### 更新单个文档

此模块可更新单个文档、活页夹或模板。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择您要创建文档、活页夹还是模板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID/名称</p> </td> 
   <td> <p>如果要更新模板，请输入模板的新名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>新模板名称</p> </td> 
   <td> <p>输入或映射要更新的对象的ID或名称。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">  <p>选择字段</p> </td> 
   <td> <p>选择要为其输入数据的字段，然后在这些字段中输入数据。</td> 
  </tr> 
 </tbody> 
</table>

### 对象



#### 列出对象

此模块检索已验证的存储库中的所有存储库对象。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>检索本地化的标签</p> </td> 
   <td> <p>选择“是”可检索label和label_plural对象字段的本地化（已翻译）字符串。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">返回结果的最大数目</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

### 其他

* [进行自定义API调用](#make-a-custom-api-call)
* [进行VQL查询](#make-a-vql-query)
* [读取日志](#read-logs)

#### 进行自定义API调用

此操作模块对Veeva保险库API进行自定义调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>输入相对于<code>baseurl/api/v</code>的路径。  例如： <code>/objects/documents</code>。 不包括<code>baseurl/api/v/</code>，因为它已包括在内。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">方法</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">标头</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">查询字符串</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">正文</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 进行VQL查询

此模块使用保险库查询语言(VQL)进行查询。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>类型</p> </td> 
   <td> <p>选择您要创建模板还是文档</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">  <p>文件数据</p> </td> 
   <td> <p>映射将用于创建文档的CSV文件。</td> 
  </tr> 
 </tbody> 
</table>

#### 读取日志

此模块从审核跟踪返回数据

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>审核类型</p> </td> 
   <td> <p>选择要为其检索数据的审核类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>开始日期</p> </td> 
   <td> <p>输入或映射要检索的审核的开始日期。</p><p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>结束日期</p> </td> 
   <td> <p>输入或映射要检索的审核的结束日期。</p><p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>结果URL </p> </td> 
   <td> <p>如果要获取URL以下载结果的CSV，请选择CSV。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">返回结果的最大数目</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>


