---
title: Dropbox模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Dropbox的工作流，并将其连接到多个第三方应用程序和服务。这样，您就可以自动执行Dropbox中的各种活动，如监视、搜索、检索、列出、创建和编辑文件和文件夹。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 29ce5940-4d71-4719-ab5e-f03c44b28c8c
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '3203'
ht-degree: 0%

---

# [!DNL Dropbox]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动执行使用[!UICONTROL Dropbox]或[!DNL Dropbox Business]的工作流，还可以将其连接到多个第三方应用程序和服务。这样，您就可以自动执行[!UICONTROL Dropbox]中的文件和文件夹等活动。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求</p>
   <p>或</p>
   <p>旧版：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

* 要使用[!DNL Dropbox]模块，您必须具有[!DNL Dropbox]帐户。

>[!IMPORTANT]
>
>Dropbox必须批准用户数超过50的应用程序。
>
>有关更多信息，请在Dropbox开发人员指南中搜索“生产批准”。

## Dropbox API信息

Dropbox连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://api.dropboxapi.com/2    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> 2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td><ul><li><p>Dropbox</p><p>v5.3.9</p></li><li><p>Dropbox业务</p><p>v1.0.12</p></li></ul></td> 
  </tr>
 </tbody> 
 </table>


## 创建与[!DNL Dropbox]的连接

要为您的[!DNL Dropbox]模块创建连接：

1. 在任意模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[！UICONTROL连接名称]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
        <tr>
        <td role="rowheader">[！UICONTROL环境]</td>
        <td>选择此连接是用于生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL类型]</td>
        <td>选择您是要连接到服务帐户还是个人帐户。</td>
        </tr>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL客户端ID]</td>
        <td>输入您的[！UICONTROL Dropbox] [！UICONTROL客户端ID]。 </tr>
        <tr>
        <td role="rowheader">[！UICONTROL客户端密钥]</td>
        <td>输入您的[!DNL Dropbox] [！UICONTROL客户端密钥]。 </td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL帐户类型]</td>
        <td>选择您是连接到个人Dropbox帐户还是企业(Dropbox Business)帐户。</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL排除dropbox-api-path-root标头]</td>
        <td>启用此选项以排除具有应用程序文件夹访问权限的Dropbox应用程序的dropbox-api-path-root标头</td>
        </tr>
      </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。## [!DNL Dropbox]模块及其字段

## [!DNL Dropbox]模块及其字段

配置[!DNL Dropbox]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Dropbox]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器模块](#trigger-modules)
* [用于获取 [!DNL Dropbox] 文件和文件夹的模块](#modules-for-getting-dropbox-files-and-folders)
* [用于创建和编辑 [!DNL Dropbox] 文件和文件夹的模块](#modules-for-creating-and-editing-dropbox-files-and-folders)
* [其他模块](#other-modules)

### 触发器模块

#### [!UICONTROL 监视文件]

修改指定文件夹中的文件时，此触发器类型模块会返回文件详细信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件夹] </td> 
   <td> <p>选择要监视更改的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Watch also subfolders]</td> 
   <td> <p> 启用此选项还可以监视所选文件夹中用于修改文件的子文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL限制] </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 用于获取[!DNL Dropbox]文件和文件夹的模块

* [[!UICONTROL 下载文件]](#download-a-file)
* [[!UICONTROL 获取文件夹元数据]](#get-a-folder-metadata)
* [[!UICONTROL 列出文件夹中的所有文件/子文件夹]](#list-all-filessubfolders-in-a-folder)
* [[!UICONTROL 列出文件修订]](#list-file-revisions)
* [[!UICONTROL 搜索文件/文件夹]](#search-filesfolders)

#### [!UICONTROL 下载文件]

此操作模块从文件夹下载文件。

指定文件及其位置。

模块会返回文件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

>[!NOTE]
>
>此模块在向后续模块提供文件时非常有用。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>选择文件的方法</td> 
   <td> <p> 选择是要映射文件路径还是手动选择文件。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>文件路径/文件</p> </td> 
   <td> <p style="font-weight: bold;">文件路径</p> <p>输入或映射目标路径到文件。</p> <p style="font-weight: bold;">文件</p> <p>从菜单中选择文件。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取文件夹元数据]

此操作模块可检索共享文件夹的详细信息。

指定文件夹的ID。

该模块会返回文件夹ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>共享文件夹ID</td> 
   <td> <p> 输入或映射要检索其详细信息的文件夹的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出文件夹中的所有文件/子文件夹]

此操作模块列出特定文件夹中的文件或文件夹。

指定文件夹的ID。

该模块返回文件或文件夹的ID以及任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>列表 </td> 
   <td> <p>选择是要检索文件或文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>仅显示可下载的文件</td> 
   <td> <p> 启用此选项可仅返回可下载的文件。 某些类型的文件(如Google Docs)不可下载。</p> </td> 
  </tr> 
  <tr> 
   <td>文件夹 </td> 
   <td> <p>输入或映射要从中检索文件或文件夹的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>限制 </td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块列出的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出文件修订]

此操作模块可检索特定文件的所有文件修订版本（版本历史记录）。\
指定文件的ID。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>选择文件的方法</td> 
   <td> <p> 选择是要映射文件路径还是手动选择文件。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>文件路径/文件</p> </td> 
   <td> <p><b>文件路径</b></p> <p>输入或映射目标路径到文件。</p> <p><b>文件</b></p> <p>从菜单中选择文件。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>限制</p> </td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块列出的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索文件/文件夹]

此搜索模块在[!DNL Dropbox]中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL搜索] </td> 
   <td> <p>输入搜索词。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件夹] </td> 
   <td> <p>选择要搜索的文件夹。 如果未选择文件夹，此模块将搜索整个[!DNL Dropbox]帐户。</p> </td> 
  </tr> 
  <tr> 
   <td>文件状态</td> 
   <td> <p> 选择要包含在搜索中的文件状态。</p> </td> 
  </tr> 
  <tr> 
   <td>文件类别</td> 
   <td> <p> 选择要包含在搜索中的文件类别。</p> </td> 
  </tr> 
  <tr> 
   <td>文件扩展名</td> 
   <td> <p>对于要包含在搜索中的每个文件扩展名，单击<b>添加项</b>并输入或映射文件扩展名。</p> </td> 
  </tr> 
  <tr> 
   <td>限制 </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 用于创建和编辑[!DNL Dropbox]文件和文件夹的模块

* [[!UICONTROL 创建文件夹]](#create-a-folder)
* [[!UICONTROL 创建/覆盖文本文件]](#createoverwrite-a-text-file)
* [[!UICONTROL 创建/更新共享链接]](#createupdate-a-share-link)
* [[!UICONTROL 删除文件/文件夹]](#delete-a-filefolder)
* [[!UICONTROL 移动文件/文件夹]](#move-a-filefolder)
* [[!UICONTROL 重命名文件/文件夹]](#rename-a-filefolder)
* [[!UICONTROL 还原文件]](#restore-a-file)
* [[!UICONTROL 上传]文件](#upload-a-file)

#### [!UICONTROL 创建文件夹]

此操作模块将创建新文件夹。

指定文件夹的路径和名称。

该模块会返回文件夹ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件夹名称] </td> 
   <td> <p>输入新文件夹的名称。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL文件夹]</p> </td> 
   <td> <p>输入或映射要创建新文件夹的路径。</p> <p>注意：   <p>如果您使用[!DNL Dropbox Business]帐户（包含团队空间），则必须删除斜杠<code>/</code>，或者不要单击<strong>单击此处选择文件夹</strong>以在根目录中创建团队文件夹。</p> <p>如果未删除斜杠，则会返回错误<code>[409] path/malformed_path/..</code>。</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL自动重命名]</td> 
   <td> <p> 启用此选项可重命名新文件夹（如果目标位置中已存在同名文件夹）。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建/覆盖文本文件]

此操作模块创建DOC文件，或覆盖现有文件的内容。

指定源文件和文件夹。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL选择至]</td> 
   <td> <p> 选择是要创建或覆盖DOC文件。</p><ul><li><b>创建</b></p>选择要创建文件的文件夹。</li><li><b>覆盖</b><p>选择要如何选择要覆盖的文件，然后映射文件路径或选择文件。 </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL Source File]</p> </td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的内容。 </p> <p>如果要创建文件，请选择<b>空</b>。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建/更新共享链接]

此操作模块创建指向文件的公共链接。

指定文件以及有关链接的信息。

模块会返回链接的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL选择文件的方法]</td> 
   <td> <p> 选择是要映射还是输入文件路径，或者手动选择文件。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL文件路径/文件]</p> </td> 
   <td> <p style="font-weight: bold;">[！UICONTROL文件路径]</p> <p>输入或映射目标文件的路径。</p> <p style="font-weight: bold;">[！UICONTROL文件]</p> <p>选择目标文件。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL请求的可见性]</p> </td> 
   <td> <p>选择链接是公共链接、团队链接还是密码受限链接。</p> <p><b>注意：</b></p><p> [！UICONTROL团队]仅适用于Dropbox商业帐户。 [！UICONTROL密码访问]仅适用于[!DNL Dropbox Pro]或Dropbox商业帐户。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL链接的到期日期]</td> 
   <td> <p> 输入链接到期且无法再访问的日期和时间。 如果此字段留空，链接将不会过期。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">类型强制</a>。</p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL Link的访问级别]</p> </td> 
   <td> <p>设置链接收件人的权限。</p> <ul><li><strong>[！UICONTROL查看器]</strong> <p>使用该链接的用户可以查看和评论内容。</p> </li><li><strong>[！UICONTROL编辑器]</strong><p> 使用该链接的用户可以编辑、查看和评论内容。 此访问级别仅适用于基于云的文档。</p> </li><li><strong>[！UICONTROL Max]</strong> <p>使用该链接的用户将获得您可以设置该链接的最大访问级别。</p></li><ul> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL 删除文件/文件夹]

此操作模块删除文件或文件夹。

指定文件或文件夹。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL选择文件的方法]</td> 
   <td> <p> 选择是要映射还是输入文件路径，或者手动选择文件。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL文件或文件夹路径] / [！UICONTROL文件或文件夹]</p> </td> 
   <td> <p style="font-weight: bold;">[！UICONTROL文件/文件夹路径]</p> <p>输入目标路径或将目标路径映射到文件或文件夹。</p> <p style="font-weight: bold;">[！UICONTROL文件/文件夹]</p> <p>从菜单中选择文件或文件夹。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 移动文件/文件夹]

此操作模块会将文件或文件夹移动到其他位置。

您可以指定文件或文件夹，以及移动它的方法和位置。

该模块会返回文件或文件夹的ID以及任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL选择文件/文件夹的方法] </td> 
   <td> <p>选择是要映射还是输入文件或文件夹路径，或者手动选择文件或文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL文件/文件夹路径] /</p> </td> 
   <td> <p style="font-weight: bold;">[！UICONTROL文件/文件夹路径]</p> <p>输入目标路径或将目标路径映射到文件或文件夹。</p> <p style="font-weight: bold;">[！UICONTROL文件/文件夹]</p> <p>选择是要移动文件或文件夹，然后选择文件或文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL到文件夹]</p> </td> 
   <td> <p>输入或映射文件或文件夹的目标位置。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL新名称]</p> </td> 
   <td> <p>在新位置输入文件或文件夹的新名称。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL自动重命名]</p> </td> 
   <td> <p>启用此选项以确保如果存在同名的文件或文件夹，模块会重命名新的文件或文件夹，方法是在文件或文件夹名称后添加([！UICONTROL NUMBER])。 否则，将覆盖目标位置中的文件或文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL允许所有权转让]</p> </td> 
   <td> <p>启用此选项可允许所有者移动，即使这会导致所移动内容的所有权转移。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 重命名文件/文件夹]

此操作模块将重命名文件或文件夹。

指定文件或文件夹以及新名称。

该模块会返回文件或文件夹的ID以及任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>选择文件的方法</td> 
   <td> <p> 选择是要映射还是输入文件路径，或者手动选择文件。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>文件/文件夹路径/文件/文件夹</p> </td> 
   <td> <p style="font-weight: bold;">文件/文件夹路径</p> <p>输入目标路径或将目标路径映射到文件或文件夹。</p> <p style="font-weight: bold;">文件/文件夹</p> <p>选择是要移动文件或文件夹，然后选择文件或文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>重命名 </td> 
   <td> <p>输入文件的新名称，包括文件扩展名。</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL 还原文件]

此操作模块恢复文件的先前版本。

指定所需的文件和修订版本号。

模块会返回版本ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL选择文件的方法]</td> 
   <td> <p> 选择是要映射还是输入文件路径，或者手动选择文件。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL文件路径] / [！UICONTROL文件]</p> </td> 
   <td> <p><strong>[！UICONTROL文件路径]</strong> </p> <p>输入或映射目标路径到文件。</p> <p><strong>[！UICONTROL文件]</strong> </p> <p>从菜单中选择文件。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL修订版]</p> </td> 
   <td> <p>输入或映射要恢复的修订版本的修订号。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上载文件]

此操作模块将文件上传到文件夹。

您可以指定信息，例如文件的位置、要上传的文件以及文件的可选新名称。

模块会返回文件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件夹]</td> 
   <td> <p> 选择要将文件上传到的[!DNL Dropbox]的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL Source File]</p> </td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p><b>注意：</b></p><p> 上传文件的最大大小为150 MB。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL覆盖现有文件]</td> 
   <td> <p> 启用此选项可使用新文件替换现有文件。 如果将此选项保留为禁用，则将重命名上传的文件。</p> </td> 
  </tr> 
 </tbody> 
</table>


### 其他模块

#### [!UICONTROL 进行API调用]

此操作模块允许您对[!DNL Dropbox] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Dropbox]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Dropbox]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-dropbox" class="MCXref xref">创建与[!DNL Dropbox]</a>的连接。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL URL]</p> </td> 
   <td> <p>输入相对路径。输入相对于<code>https://api.dropboxapi.com</code>的路径。 例如， <code>/2/files/list_folder</code></p>  </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL方法]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Headers] </td> 
   <td> <p>输入所需的请求标头。 [!DNL Workfront Fusion]自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL查询字符串]</td> 
   <td> <p> 输入请求查询字符串。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Body] </td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：   <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**

以下API调用从[!DNL Dropbox]帐户的[!DNL /Text files]文件夹中返回前10个文件：

URL： `/2/files/list_folder`

正文：

```
{
"path": "/Text files",
"limit": 10,
"recursive": false,
"include_deleted": false
}
```

在[!UICONTROL 包] > [!UICONTROL 正文] >条目下的模块输出中可以找到搜索匹配项。

在本例中，我们返回了10张票证。

>[!ENDSHADEBOX]

## 常见问题

* [无法上传或更新文件](#unable-to-upload-or-update-a-file)
* [无法呈现通过共享链接引用的图像](#image-referenced-via-a-shared-link-does-not-render)

### 无法上传或更新文件

以下可能是上传或更新文件失败的原因：

* 上传的文件太大，超过了您的[!DNL Dropbox]计划允许的最大文件大小，或者您已使用所有[!DNL Dropbox]帐户的存储配额。 您必须从[!DNL Dropbox]帐户中删除现有文件或升级计划。
* 先前选择的文件夹（文件将上载到该文件夹）不再存在。 场景将停止，您必须再次选择目标文件夹。

### 无法呈现通过共享链接引用的图像

[!UICONTROL Dropbox] >[!UICONTROL 创建共享链接]返回的URL未直接链接到图像，而是链接到[!DNL Dropbox]页面。 要强制下载图像，请将尾部`?dl=0`替换为`?dl=1`。 要强制呈现图像（例如，在Web浏览器或Facebook Messenger中），请将`&raw=1`附加到URL。

如果需要获取您网站或其他[!DNL Workfront Fusion]模块的图像的直接或原始链接，则必须通过以下方式修改初始共享URL：

原始URL：

`https://www.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png?dl=0`

1. 将`www`替换为`dl`。
1. 删除`?dl=0`。

最终URL：

`https://dl.dropbox.com/s/ia8qtvs20f3a5ux/Screen%20Shot%202018-10-15%20at%204.21.11%20PM.png`

要自动修改URL，您可以使用`replace()`函数两次：

* 将www替换为dl

  ![用dl](/help/workfront-fusion/references/apps-and-modules/assets/www-to-dl-350x32.png)替换www

* 要删除？dl=0

  ![删除DL](/help/workfront-fusion/references/apps-and-modules/assets/remove-dl0-350x33.png)

要一次性完成此操作，请组合以下函数：

![替换两者](/help/workfront-fusion/references/apps-and-modules/assets/replace-both-350x47.png)

您也可以复制该模板并将其粘贴到字段中。 将`1.url`替换为URL。

```
{{replace(replace(1.url; "?dl=0"; ""); "www"; "dl")}}
```
