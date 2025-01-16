---
title: Google驱动器模块
description: 通过 [!DNL Adobe Workfront Fusion Google Drive] 模块，您可以监视、搜索、创建、更新、删除和管理 [!DNL Google Drive]中的文件、文件夹或共享驱动器。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2489'
ht-degree: 1%

---

# [!DNL Google Drive]模块

通过[!DNL Adobe Workfront Fusion] [!DNL Google Drive]模块，您可以监视、搜索、创建、更新、删除和管理[!DNL Google Drive]中的文件、文件夹或共享驱动器。

在[!DNL Adobe Workfront Fusion]方案中，您可以将[!DNL Google Drive]帐户连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
  <td> <p>[!UICONTROL Pro] 或更高</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
   <td> <p>[!UICONTROL Plan]， [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前许可证要求：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Adobe Workfront]计划，则您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[!UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## Google驱动器API信息

Google驱动器连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://www.googleapis.com/drive/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v4.1.22</td> 
  </tr>
 </tbody> 
 </table>



## 正在将[!DNL Google Drive]连接到[!DNL Workfront Fusion]

如果您是[!DNL @gmail.com]或[!DNL @googlemail.com]用户，则需要在[the [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project)上创建OAuth客户端才能获取[!UICONTROL Client ID]和[!UICONTROL Client Secret]。

有关如何创建OAuth客户端（并获取[!UICONTROL Client ID]和[!UICONTROL Client Secret]）的分步说明，请参阅[使用自定义OAuth客户端](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)连接 [!DNL Adobe Workfront Fusion] 到 [!DNL Google Services] 。

有关将[!DNL Google Drive]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL Google Drive]模块及其字段

配置[!DNL Google Drive]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Google Drive]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [触发器](#triggers)
* [操作](#actions)

### 触发器

* [[!UICONTROL Watch Files In Folder]](#watch-files-in-folder)
* [[!UICONTROL Watch All Files]](#watch-all-files)
* [[!UICONTROL Watch shared files]](#watch-shared-files)
* [[!UICONTROL Watch Comments]](#watch-comments)

#### [!UICONTROL Watch Files In Folder]

在指定的文件夹中添加或修改文件时检索文件详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Select the folder to be watched]</td>
    <td >选择驱动器上要监视文件的文件夹。</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL What files to watch]</td>
   <td> <p>选择要监视的文件类型。</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Documents]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Spreadsheets]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Slides]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Drawings]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Watch]</td>
    <td>选择是要监视新文件和所有更改，还是只监视新文件。</td>
  </tr> 
  <tr> 
    <td>[!UICONTROL Maximum number of downloaded files]</td>
    <td>设置[!DNL Workfront Fusion]在一个周期内下载的最大结果数（每个方案运行的重复次数）。</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch All Files]

在添加或修改您[!DNL Google Drive]中的某个文件时检索文件详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p>选择要监视的文件类型。</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Documents]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Spreadsheets]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Slides]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Drawings]转换为的文件格式。</td>
  </tr>  
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>选择是要监视新文件和所有更改，还是只监视新文件。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>设置[!DNL Workfront Fusion]在一个周期内下载的最大结果数（每个方案运行的重复次数）。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch shared files]

当您共享新文件或更新现有共享文件时，会触发该事件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Select the folder to be watched]</td> 
   <td>选择要监视文件的共享文件夹。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL What files to watch]</td> 
   <td> <p>选择要监视的文件类型。</p> 
    <ul> 
     <li>[!UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[!UICONTROL Convert [!DNL Google Documents] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Documents]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Spreadsheets] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Spreadsheets]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Slides] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Slides]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[!UICONTROL Convert [!DNL Google Drawings] 要格式化的文件]</td>
    <td>选择要将[!DNL Google Drawings]转换为的文件格式。</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>选择是要监视新文件和所有更改，还是只监视新文件。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of downloaded files]</td> 
   <td>设置[!DNL Workfront Fusion]在一个周期内下载的最大结果数（每个方案运行的重复次数）。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Comments]

在选定文件上添加或修改评论时触发。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File]</td> 
   <td>选择要监视其注释的文件。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td>选择要监视所有更改还是仅监视新注释</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned comments]</td> 
   <td>设置[!DNL Workfront Fusion]在一个周期内返回的最大评论数（每个方案运行的重复次数）。</td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Upload a File]](#upload-a-file)
* [[!UICONTROL Update a File]](#update-a-file)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File]](#delete-a-file)
* [[!UICONTROL Move a File/Folder to Trash]](#move-a-filefolder-to-trash)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Search for Files/Folders]](#search-for-filesfolders)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Get a share link]](#get-a-share-link)

#### [!UICONTROL Upload a File]

将文件上传到您的[!DNL Google Drive]。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Destination]</td> 
   <td> <p>选择要将文件上载到的目标。</p> 
    <ul> 
     <li>[!DNL My Drive]</li> 
     <li>[!DNL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>选择要将文件上传到的文件夹。 </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>选择是要使用从上一个模块传入的文件，还是要手动映射文件。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td>选择文件名。 如果您在[!UICONTROL source file]字段中选择“[!UICONTROL Map]”，则此选项可用。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data]</td> 
   <td>选择要上载的数据文件。 如果您在[!UICONTROL source file]字段中选择“[!UICONTROL Map]”，则此选项可用。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>输入新文件的标题。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert a file]</td> 
   <td>启用此选项将允许模块将文件转换为相应的[!DNL Google]格式。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a File]

更新文件的元数据或内容。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>选择要将文件上载到的目标。</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Move to a folder]</td> 
   <td>如果要将文件移动到其他文件夹，请选择要将文件移动到其中的文件夹。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>映射要更新的文件的ID。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Title]</td> 
   <td>输入更新文件的标题。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Change a file content]</td> 
   <td>选择是否要替换文件的内容。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td>选择是要使用从上一个模块传入的文件，还是要手动映射文件。 如果您在上一个字段中选择了更改文件的内容，则此字段可用。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td>选择文件名。 如果您在[!UICONTROL source file]字段中选择“[!UICONTROL Map]”，则此选项可用。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Data]</td> 
   <td>选择要上载的数据文件。 如果您在[!UICONTROL source file]字段中选择“[!UICONTROL Map]”，则此选项可用。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

将文件复制到新位置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>选择要将文件上载到的目标。</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Target folder]</td> 
   <td>选择要复制的文件所在的文件夹/</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>映射要更新的文件的ID。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the copy]</td> 
   <td>输入新文件的标题。 如果不想更改原始文件名，请将此字段留空。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File]

永久删除文件或文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>映射要删除的文件的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder to Trash]

将文件或文件夹移至垃圾桶。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>将您要移动的文件的ID映射到垃圾桶。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

检索具有指定ID的文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Documents] 要格式化的文件]</td> 
   <td>选择要将[!DNL Google Documents]转换为的文件格式。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Spreadsheets] 要格式化的文件]</td> 
   <td>选择要将[!DNL Google Spreadsheets]转换为的文件格式。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Slides] 要格式化的文件]</td> 
   <td>选择要将[!DNL Google Slides]转换为的文件格式。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Convert [!DNL Google Drawings] 要格式化的文件]</td> 
   <td>选择要将[!DNL Google Drawings]转换为的文件格式。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>映射要检索的文件的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search for Files/Folders]

根据搜索条件搜索文件或文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>选择要搜索的目标。</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL List a folder]</td> 
   <td>导航到要搜索文件或文件夹的文件夹。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Retrieve]</td> 
   <td> <p> 选择是要搜索文件、文件夹，还是同时搜索两者。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Search]</p> </td> 
   <td> <p>选择要执行的搜索类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Search within file/folder names]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>输入要搜索的文件名的一部分或完整文件名（包括后缀）。</p> </li> 
       <li> <p><strong>[!UICONTROL Search Options]</strong> </p> <p>选择是要搜索确切的搜索词，还是要搜索包含该搜索词的名称。</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Fulltext]搜索</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>输入要在[!DNL Google Drive]中搜索的任何搜索词。</p> </li> 
      </ul> </li> 
     <li> <p><strong>输入自定义搜索查询</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Query]</strong> </p> <p>输入自定义搜索查询。 有关更多详细信息，请参阅本文的[!UICONTROL Search for Files]部分。</p> </li> 
       <li> <p><strong>将上面选择的文件夹添加到查询</strong> </p> <p>在父收藏集中搜索文件夹。 这会查找直接位于上面所选文件夹中的所有文件和文件夹。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned results]</td> 
   <td>设置在一个执行周期内[!DNL Workfront Fusion]将返回的最大文件或文件夹数。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td>启用此选项以确保在模块未返回任何结果时不会停止该方案。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

在指定位置创建文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination]</td> 
   <td> <p>选择要将文件上载到的目标。</p> 
    <ul> 
     <li>[!UICONTROL My Drive]</li> 
     <li>[!UICONTROL Shared with Me]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL New folder location]</td> 
   <td>导航到要创建新文件夹的位置。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL The name of the new folder]</td> 
   <td>输入正在创建的文件夹的名称。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Share folder]</td> 
   <td>如果要与具有[!UICONTROL Share]链接的任何人共享文件夹，请选择此选项。 否则，共享链接仅供所有者使用。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a share link]

在Google驱动器中检索文件的共享链接。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[!UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File ID]</td> 
   <td>映射要获取共享链接的文件的ID。</td> 
  </tr> 
 </tbody> 
</table>

## 故障排除

### 无法上传或更新文件

上传或更新文件失败时，可能会出现以下几种情况：

* 上传的文件太大，超过了您的[!DNL Google Drive]计划允许的最大文件大小限制，或者您已超过[!DNL Google Drive]存储限制。 您可以升级存储计划，也可以从[!DNL Google Drive]服务中删除现有文件。
* 要将文件上载到的所选文件夹不再存在。 此方案将停止，随后需要再次选择目标文件夹。

## 搜索文件

在模块的List files in a folder中，您可以使用自己的查询，该查询包含以下部分：

* **[!UICONTROL Field]** — 正在搜索文件的属性，例如文件的属性`name`。

* **[!UICONTROL Operator]** — 为提供匹配项而对数据执行的测试，例如`contains`。

* **[!UICONTROL Value]** — 测试的属性的内容，例如，文件`My cool document`的名称。

将子句与连接项`and`或`or`组合，并使用`not`否定查询。

* [字段](#fields)
* [值类型](#value-types)
* [运算符](#operators)
* [示例](#examples)

### 字段

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>字段 </th> 
   <th>值类型 </th> 
   <th>运算符</th> 
   <th> <p> 描述</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>字符串</td> 
   <td><code>contains</code><sup>1</sup>，<code>=</code>， <code>!=</code></td> 
   <td> <p> 文件的名称。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>字符串 </td> 
   <td><code>contains</code><sup>2， 3</sup> </td> 
   <td> <p> 文件的全文，包括名称、描述、内容和可索引文本。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> 字符串</td> 
   <td><code>contains</code>，<code>=</code>， <code>!=</code></td> 
   <td> <p> 文件的MIME类型。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> 日期<sup>4</sup></td> 
   <td><code> &lt;=</code>，<code>&lt;</code>，<code>=</code>，<code>!=</code>，<code>></code>， <code>>=</code></td> 
   <td> <p> 上次修改文件的日期。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> 日期<sup>4</sup></td> 
   <td><code>&lt;=</code>，<code>&lt;</code>，<code>=</code>，<code>!=</code>，<code>></code>， <code>>=</code></td> 
   <td> <p> 用户上次查看文件的日期。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>布尔值 </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> 文件是否在垃圾桶中。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>布尔值 </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>文件是否处于星型状态。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>收藏集 </td> 
   <td><code>in </code> </td> 
   <td> <p>[!UICONTROL parents]集合是否包含指定的ID。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>收藏集 </td> 
   <td><code>in </code> </td> 
   <td> <p>拥有文件的用户。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>收藏集 </td> 
   <td><code>in </code> </td> 
   <td> <p>有权修改文件的用户。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>收藏集 </td> 
   <td><code>in </code> </td> 
   <td> <p>有权读取文件的用户。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>布尔值 </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> 用户“已与我共享”收藏集中的文件。</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>收藏集</td> 
   <td><code>has </code> </td> 
   <td> <p> 公共自定义文件属性。</p> </td> 
  </tr> 
 </tbody> 
</table>

请考虑以下有关这些字段中的运算符的信息：

* `contains`运算符仅对`title`执行前缀匹配。

  例如，标题“HelloWorld”与`title contains 'Hello'`匹配，但与`title contains 'World'`不匹配。

* `contains`运算符仅对`fullText`的整个字符串令牌执行匹配。

  例如，如果文档的全文包含字符串“HelloWorld”，则只有查询`fullText contains 'HelloWorld'`返回结果。 在此方案中，诸如`fullText contains 'Hello'`之类的查询不会返回结果。

* 如果`contains`运算符由双引号括起来，则它匹配精确字母数字短语。

  例如，如果文档的`fullText`包含字符串“Hello there world”，则查询`fullText contains '"Hello there"'`返回结果，但查询`fullText contains '"Hello world"'`未返回结果。

  此外，由于搜索是字母数字的，因此如果文档的`fullText`包含字符串“Hello_world”，则查询`fullText contains '"Hello world"'`将返回结果。

* `type`日期的字段当前无法相互比较，只能比较固定日期。

### 值类型

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>值类型</th> 
   <th> <p> 注释</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>字符串 </td> 
   <td> <p>用单引号'. 对包含<code>\'</code>的查询（例如，<code> 'Valentine\'s Day'</code>）中的单引号进行转义。</p> </td> 
  </tr> 
  <tr> 
   <td>布尔型 </td> 
   <td> <p><code>true </code>或<code>false</code>。</p> </td> 
  </tr> 
  <tr> 
   <td>日期 </td> 
   <td> <p>RFC 3339格式，默认时区为UTC，例如<code>2012-06-04T12:00:00-08:00</code>。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 运算符

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>操作员 </th> 
   <th> <p>注释</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>一个字符串的内容存在于另一个字符串中。</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> 字符串或布尔值的内容等于另一个字符串或布尔值。</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> 字符串或布尔值的内容不等于另一个字符串或布尔值。</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> 日期早于另一个日期。</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> 日期早于或等于另一个日期。</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> 日期晚于另一个日期。</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> 日期晚于或等于另一个日期。</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>元素包含在收藏集中。</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>返回匹配两个子句的文件。</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>返回与任一子句匹配的文件。</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>使搜索子句无效。</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>收藏集包含与参数匹配的元素。</p> </td> 
  </tr> 
 </tbody> 
</table>

对于复合子句，可以使用括号将子句组合在一起。 例如：
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')`此搜索返回其上次修改是在2012年6月4日之后且图像或视频MIME类型的所有文件。 由于`and`和`or`运算符是从左到右计算的，没有括号，因此上述示例将仅返回在2012年6月4日之后修改的图像，但会返回所有视频，甚至是2012年6月4日之前的视频。

### 示例

此页面上的所有示例都显示了未编码的`<q>q</q>`参数，其中`title = 'hello'`编码为`title+%3d+%27hello%27`。 客户端库会自动处理此编码。

* 搜索名为“hello”的文件
  <pre>标题= 'hello'</pre>
* 使用文件夹特定的MIME类型搜索文件夹
  <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* 搜索不是文件夹的文件
  <pre>mimeType ！= 'application/vnd.google-apps.folder'</pre>
* 搜索名称中包含“hello”和“goodbye”字样的文件
  <pre>标题包含“hello”，[!UICONTROL name]包含“goodbye”</pre>
* 搜索名称中不包含单词“hello”的文件
  <pre>标题不包含“hello”</pre>
* 搜索内容中包含“hello”一词的文件
  <pre>全文包含“hello”</pre>
* 搜索内容中不包含单词“hello”的文件
  <pre>非fullText包含“hello”</pre>
* 搜索内容中包含精确短语“hello world”的文件
  <pre>全文包含“ hello world”。全文包含“ hello_world”</pre>
* 使用包含“\”字符（如“\authors”）的查询搜索文件
  <pre>全文包含'\\authors'</pre>
* 搜索用户`test@example.org`可写的文件
  <pre>中的“test@example.org” [!DNL writers]</pre>
* 在`parents`集合中搜索ID `1234567`。 这会查找直接位于ID为`1234567`的文件夹中的所有文件和文件夹。
  <pre>中的“1234567” [!UICONTROL parents]</pre>
* 在`parents`集合中搜索别名ID `appDataFolder`。 这会查找直接位于[应用程序数据文件夹](https://developers.google.com/drive/api/v2/appdata)下的所有文件和文件夹。
  <pre>父级中的“appDataFolder”</pre>
* 搜索用户`test@example.org`和`test2@example.org`可写的文件
  <pre>作者中的“test@example.org”和作者中的“test2@example.org”</pre>
* 搜索垃圾桶中包含“important”文本的文件
  <pre>fullText包含“important”，并且已置入垃圾桶= true</pre>
* 搜索在2012年6月4日之后修改的文件
  <pre>modifiedDate &gt; '2012-06-04T12:00:00' //默认时区为UTC</pre><pre>modifiedDate &gt; '2012-06-04T12:00:00-08:00'</pre>
* 搜索与名称中带有“hello”的授权用户共享的文件
  <pre>sharedWithMe，标题包含“hello”</pre>
* 搜索具有名为`additionalID`且值为`8e8aceg2af2ge72e78`的[自定义文件属性](https://developers.google.com/drive/api/v2/properties)的文件。
  <pre>属性具有{ key='additionalID'和value='8e8aceg2af2ge72e78'和visibility='PRIVATE' }</pre>

本指南的Source是[[!DNL Google Drive] 文档](https://developers.google.com/drive/api/v2/search-shareddrives)。
