---
title: Veeva Vault 模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Veeva Vault的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
source-git-commit: b57ae36cf9225705c7f4923d7302b1749aa04d94
workflow-type: tm+mt
source-wordcount: '2539'
ht-degree: 19%

---

# Veeva Vault 模块

在Adobe Workfront Fusion场景中，您可以自动使用Veeva Vault的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用Veeva Vault模块，您必须具有Veeva Vault帐户。

## 将Veeva Vault连接到Workfront Fusion

您可以直接从Veeva Vault模块内创建与Veeva Vault帐户的连接。

创建连接时，您可以选择是否使用密码，或者是否使用OAuth2身份验证。

### 使用用户名和密码连接到Veeva Vault

1. 在任何Veeva保险库模块中，单击“连接”字段旁边的&#x200B;**添加**。
1. 在&#x200B;**连接类型**&#x200B;字段中，选择`Veeva Username Password`。
1. 填写以下字段。

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">连接名称</td> 
       <td> <p>输入连接名称。</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">用户名</td>
        <td>
          <p>输入Veeva保险库帐户的用户名。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">密码</td>
        <td>
          <p>输入Veeva Vault帐户的密码。</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">保险库DNS</td> 
       <td>输入您的Veeva Vault DNS（域名）。</p><p>要找到Veeva Vault DNS，请检查用于访问Veeva Vault的URL。</p>例如，在URL <code>https://my-dns.veevavault.com</code>中，DNS是<code>my-dns</code>。 您无需输入整个URL。</td> 
      </tr> 
     </tbody> 
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

### 使用OAuth2身份验证连接到Veeva Vault

1. 在任何Veeva保险库模块中，单击“连接”字段旁边的&#x200B;**添加**。
1. 在&#x200B;**连接类型**&#x200B;字段中，选择`Veeva Oauth 2`。
1. 填写以下字段。

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">连接名称</td> 
       <td> <p>输入连接名称。</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader">授权服务器提供程序</td> 
       <td> <p>选择要用于此身份验证的提供程序。</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader">Ping主机</td> 
       <td> <p>如果使用的是PingFederate，请输入Ping主机。</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">范围</td>
        <td>
          <p>输入此连接的范围。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">租户ID</td>
        <td>
          <p>如果您正在将Azure AD/Microsoft Entra ID用于授权服务器提供程序，请输入此连接的租户ID。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">客户端 ID</td>
        <td>
          <p>输入此连接将使用的Veeva Vault应用程序的客户端ID。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">客户端密钥</td>
        <td>
          <p>输入此连接将使用的Veeva Vault应用程序的客户端密钥。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">配置文件ID</td>
        <td>
          <p>输入OAuth2 / Copen ID Connect配置文件的ID。</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">保险库DNS</td> 
       <td>输入您的Veeva Vault DNS（域名）。</p><p>要找到Veeva Vault DNS，请检查用于访问Veeva Vault的URL。</p>例如，在URL <code>https://my-dns.veevavault.com</code>中，DNS是<code>my-dns</code>。 您无需输入整个URL。</td> 
      </tr> 
      <tr>
        <td role="rowheader">会话过期时间（分钟）</td>
        <td>
          <p>输入会话的过期时间（分钟）。</p>
        </td>
      </tr>
     </tbody> 
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。


## Veeva Vault模块及其字段

配置Veeva Vault模块时，Workfront Fusion会显示以下列出的字段。 除此之外，可能还会显示其他Veeva Vault字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [文档](#document)
* [对象](#object)
* [其他](#other)

### 文档

* [创建单个文档](#create-a-single-document)
* [创建多个文档](#create-multiple-documents)
* [删除单个文档](#delete-a-single-document)
* [下载文件](#download-file)
* [导出文档](#export-documents)
* [获取单个文档](#get-a-single-document)
* [启动用户操作](#initiate-user-action)
* [列出文档](#list-documents)
* [检索文档导出结果](#retrieve-document-export-results)
* [更新单个文档](#update-a-single-document)
* [更新多个文档](#update-multiple-documents)

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

#### 下载文件

此模块从Veeva Vault下载文档、文档版本或模板。

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
   <td> <p>选择您要下载文档还是模板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>下载类型</p> </td> 
   <td> <p>选择您要下载文档还是文档版本。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>文档ID/模板名称</p> </td> 
   <td> <p>输入或映射文档的ID或要下载的模板的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>签出文档</p> </td> 
   <td> <p>如果您正在下载文档，请启用此选项，以在下载文档之前签出该文档。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"><p>版本</p> </td> 
   <td> <p>如果您正在下载文档版本，请选择要下载的版本。</td> 
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
   <td>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</td> 
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
   <td role="rowheader"> <p>作业 ID</p> </td> 
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
   <td> <p>选择是要创建文档、文档版本、绑定器还是模板。</p> </td> 
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

* [创建单个对象记录](#create-a-single-object-record)
* [删除单个对象记录](#delete-a-single-object-record)
* [获取单个对象](#get-a-single-object)
* [列出对象记录](#list-objects-records)
* [更新单个对象记录](#update-a-single-object-record)

#### 创建单个对象记录

此模块创建、复制或深层复制单个对象记录。

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
   <td> <p>选择是创建或复制记录，还是深度复制记录。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">迁移模式</td> 
   <td>如果创建或复制记录，请启用此选项以创建或更新处于非初始状态且验证最少的对象记录，创建非活动记录，并设置标准和系统管理的字段，如<code>createdby_v</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">无触发器</td> 
   <td>如果设置为true并启用迁移模式，则模块将绕过所有系统、标准、自定义SDK触发器和操作触发器。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">对象名称</td> 
   <td>输入或映射对象名称__v字段值，如<code>product__v</code>、<code>country__v</code>或<code>custom_object__c</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录Id</td> 
   <td>如果要深度复制记录，请选择要复制的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录字段</td> 
   <td>如果要深度复制记录，请选择要为其提供值的字段，然后提供这些值。</td> 
  </tr> 
 </tbody> 
</table>

#### 删除单个对象记录

此模块删除或级联删除单个对象记录。 级联删除记录会删除该记录及其所有子对象。

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
   <td> <p>选择是删除记录，还是级联删除记录。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">对象名称</td> 
   <td>选择要删除的对象。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录Id</td> 
   <td>选择要删除的记录的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">外部 ID</td> 
   <td>您可以使用此用户定义的文档外部ID，而不是记录ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 获取单个对象

此模块可检索在存储库中的特定对象记录上配置的元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Veeva Vault帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">对象名称</td> 
   <td>选择要为其检索元数据的对象。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录Id</td> 
   <td>选择要为其检索元数据的记录的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 列出对象记录

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
   <td>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</td> 
  </tr> 
 </tbody> 
</table>

<!--#### Update a single object record-->

此模块更新现有对象记录中的字段。

此模块创建、复制或深层复制单个对象记录。

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
   <td> <p>选择是创建或复制记录，还是深度复制记录。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">迁移模式</td> 
   <td>启用此选项可以在非初始状态下以最少的验证创建或更新对象记录，创建非活动记录，并设置标准和系统管理的字段，如<code>createdby_v</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">无触发器</td> 
   <td>如果启用了迁移模式，则可以启用此选项以绕过所有系统、标准、自定义SDK触发器和操作触发器。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">对象名称</td> 
   <td>输入或映射对象名称__v字段值，如<code>product__v</code>、<code>country__v</code>或<code>custom_object__c</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录Id</td> 
   <td>选择要更新的记录的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">State</td> 
   <td>指定将<code>X-VaultAPI-MigrationMode</code>设置为true时记录的生命周期状态。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">状态标签</td> 
   <td>在<code>X-VaultAPI-MigrationMode</code>设置为true时指定记录的生命周期状态类型。 使用格式<code>base:object_lifecycle:</code>，后跟对象状态类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录字段</td> 
   <td>如果要深度复制记录，请选择要为其提供值的字段，然后提供这些值。</td> 
  </tr> 
 </tbody> 
</table>

### 其他

* [发起自定义 API 调用](#make-a-custom-api-call)
* [进行VQL查询](#make-a-vql-query)
* [读取日志](#read-logs)

#### 发起自定义 API 调用

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
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">标头</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">查询字符串</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">正文</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
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
   <td> <p>输入或映射要检索的审核的开始日期。</p><p>有关支持的日期和时间格式列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制转换</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>结束日期</p> </td> 
   <td> <p>输入或映射要检索的审核的结束日期。</p><p>有关支持的日期和时间格式列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制转换</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>结果URL </p> </td> 
   <td> <p>如果要获取URL以下载结果的CSV，请选择CSV。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">返回结果的最大数目</td> 
   <td>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</td> 
  </tr> 
 </tbody> 
</table>


