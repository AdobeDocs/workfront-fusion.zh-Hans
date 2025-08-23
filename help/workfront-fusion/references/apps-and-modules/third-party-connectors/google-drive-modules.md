---
title: Google驱动器模块
description: 通过 [!DNL Adobe Workfront Fusion Google Drive] 模块，您可以监视、搜索、创建、更新、删除和管理 [!DNL Google Drive]中的文件、文件夹或共享驱动器。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 788f4e1b-d774-45ad-a8be-b16922c1d5dc
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2096'
ht-degree: 0%

---

# [!DNL Google Drive]模块

Adobe Workfront Fusion [!DNL Google Drive]模块允许您监视、搜索、创建、更新、删除和管理[!DNL Google Drive]中的文件、文件夹或共享驱动器。

在Adobe Workfront Fusion方案中，您可以将[!DNL Google Drive]帐户连接到多个第三方应用程序和服务。

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
   <p>新：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## Google驱动器API信息

Google驱动器连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
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



## 正在将[!DNL Google Drive]连接到Workfront Fusion

如果您使用[!DNL @gmail.com]或[!DNL @googlemail.com]用户，则必须在[!DNL Google Cloud Platform]上创建OAuth客户端以获取您的[!UICONTROL 客户端ID]和[!UICONTROL 客户端密钥]。

有关如何创建OAuth客户端（并获取[!UICONTROL 客户端ID]和[!UICONTROL 客户端密钥]）的分步说明，请参阅[使用自定义OAuth客户端将Adobe Workfront Fusion连接到 [!DNL Google Services] ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)。

有关将[!DNL Google Drive]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL Google Drive]模块及其字段

在配置[!DNL Google Drive]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Google Drive]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)



* [触发器](#triggers)
* [操作](#actions)

### 触发器

* [[!UICONTROL 观看所有文件]](#watch-all-files)
* [[!UICONTROL 观看评论]](#watch-comments)
* [[!UICONTROL 监视文件夹中的文件]](#watch-files-in-folder)
* [[!UICONTROL 观看共享文件]](#watch-shared-files)

#### [!UICONTROL 观看所有文件]

添加或修改[!DNL Google Drive]中的文件时，此触发器模块会启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL要查看的文件]</td> 
   <td> <p>选择要监视的文件类型。</p> 
    <ul> 
     <li>[！UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[！UICONTROL将[!DNL Google Documents]文件转换为格式]</td>
    <td>选择要将[!DNL Google Documents]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL将[!DNL Google Spreadsheets]文件转换为格式]</td>
    <td>选择要将[!DNL Google Spreadsheets]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL将[!DNL Google Slides]文件转换为格式]</td>
    <td>选择要将[!DNL Google Slides]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL将[!DNL Google Drawings]文件转换为格式]</td>
    <td>选择要将[!DNL Google Drawings]转换为的文件格式。</td>
  </tr>  
  <tr> 
   <td>[！UICONTROL监视]</td> 
   <td>选择是要监视新文件和所有更改，还是只监视新文件。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL最大下载文件数]</td> 
   <td>设置Workfront Fusion在一个周期内下载的最大结果数（每个方案运行的重复次数）。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看评论]

此触发器模块会在选定文件上添加或修改评论时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件]</td> 
   <td>选择要监视其注释的文件。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL监视]</td> 
   <td>选择要监视所有更改还是仅监视新注释</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL返回的最大评论数]</td> 
   <td>设置Workfront Fusion在一个周期内返回的最大评论数（每个方案运行的重复次数）。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 监视文件夹中的文件]

在指定文件夹中添加或修改文件时，此触发器模块将启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[！UICONTROL Connection] </td>
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr>
    <td>[！UICONTROL选择要监视的文件夹]</td>
    <td >选择驱动器上要监视文件的文件夹。</td>
  </tr> 
  <tr> 
    <td>[！UICONTROL要查看的文件]</td>
   <td> <p>选择要监视的文件类型。</p> 
    <ul> 
     <li>[！UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[！UICONTROL将[!DNL Google Documents]文件转换为格式]</td>
    <td>选择要将[!DNL Google Documents]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL将[!DNL Google Spreadsheets]文件转换为格式]</td>
    <td>选择要将[!DNL Google Spreadsheets]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL将[!DNL Google Slides]文件转换为格式]</td>
    <td>选择要将[!DNL Google Slides]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL将[!DNL Google Drawings]文件转换为格式]</td>
    <td>选择要将[!DNL Google Drawings]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL监视]</td>
    <td>选择是要监视新文件和所有更改，还是只监视新文件。</td>
  </tr> 
  <tr> 
    <td>[！UICONTROL最大下载文件数]</td>
    <td>设置Workfront Fusion在一个周期内下载的最大结果数（每个方案运行的重复次数）。</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看共享文件]

当您共享新文件或更新现有共享文件时，会触发该事件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL选择要监视的文件夹]</td> 
   <td>选择要监视文件的共享文件夹。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL要查看的文件]</td> 
   <td> <p>选择要监视的文件类型。</p> 
    <ul> 
     <li>[！UICONTROL All]</li> 
     <li>[!DNL Google Documents]</li> 
     <li>[!DNL Google Spreadsheets]</li> 
     <li>[!DNL Google Slides]</li> 
     <li>[!DNL Google Drawings]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td >[！UICONTROL将[!DNL Google Documents]文件转换为格式]</td>
    <td>选择要将[!DNL Google Documents]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL将[!DNL Google Spreadsheets]文件转换为格式]</td>
    <td>选择要将[!DNL Google Spreadsheets]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL将[!DNL Google Slides]文件转换为格式]</td>
    <td>选择要将[!DNL Google Slides]转换为的文件格式。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL将[!DNL Google Drawings]文件转换为格式]</td>
    <td>选择要将[!DNL Google Drawings]转换为的文件格式。</td>
  </tr> 
  <tr> 
   <td>[！UICONTROL监视]</td> 
   <td>选择是要监视新文件和所有更改，还是只监视新文件。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL最大下载文件数]</td> 
   <td>设置Workfront Fusion在一个周期内下载的最大结果数（每个方案运行的重复次数）。</td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 复制文件]](#copy-a-file)
* [[!UICONTROL 创建fFolder]](#create-a-folder)
* [[!UICONTROL 删除文件]](#delete-a-file)
* [[!UICONTROL 获取文件]](#get-a-file)
* [[!UICONTROL 获取共享链接]](#get-a-share-link)
* [[!UICONTROL 将文件移动到垃圾桶]](#move-a-filefolder-to-trash)
* [[!UICONTROL 搜索文件/文件夹]](#search-for-filesfolders)
* [[!UICONTROL 更新文件]](#update-a-file)
* [[!UICONTROL 上载文件]](#upload-a-file)

#### [!UICONTROL 复制文件]

此操作模块将文件复制到新位置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL目标]</td> 
   <td> <p>选择要将文件复制到的目标。</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL目标文件夹]</td> 
   <td>选择包含要复制文件的文件夹。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件ID]</td> 
   <td>映射要复制的文件的ID。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL副本的名称]</td> 
   <td>输入新文件的标题。 如果不想更改原始文件名，请将此字段留空。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建文件夹]

此操作模块在指定位置创建一个文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL目标]</td> 
   <td> <p>选择要创建文件夹的目标。</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL新建文件夹位置]</td> 
   <td>导航到要创建新文件夹的位置。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL新文件夹的名称]</td> 
   <td>输入正在创建的文件夹的名称。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL共享文件夹]</td> 
   <td>如果要与具有[！UICONTROL共享]链接的任何用户共享文件夹，请选择此选项。 否则，共享链接仅供所有者使用。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除文件]

此操作模块将永久删除文件或文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件ID]</td> 
   <td>映射要删除的文件的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取文件]

此操作模块会检索具有指定ID的文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL将[!DNL Google Documents]文件转换为格式]</td> 
   <td>选择要将[!DNL Google Documents]转换为的文件格式。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL将[!DNL Google Spreadsheets]文件转换为格式]</td> 
   <td>选择要将[!DNL Google Spreadsheets]转换为的文件格式。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL将[!DNL Google Slides]文件转换为格式]</td> 
   <td>选择要将[!DNL Google Slides]转换为的文件格式。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL将[!DNL Google Drawings]文件转换为格式]</td> 
   <td>选择要将[!DNL Google Drawings]转换为的文件格式。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件ID]</td> 
   <td>映射要检索的文件的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取共享链接]

此操作模块检索Google驱动器中文件的共享链接。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件ID]</td> 
   <td>映射要获取共享链接的文件的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 将文件移动到垃圾桶]

此操作模块会将文件或文件夹移至垃圾桶。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件ID]</td> 
   <td>将您要移动的文件的ID映射到垃圾桶。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索文件/文件夹]

此搜索模块根据搜索条件搜索文件或文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL目标]</td> 
   <td> <p>选择要搜索的目标驱动器。</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL列出文件夹]</td> 
   <td>导航到要搜索文件或文件夹的文件夹。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Retrieve]</td> 
   <td> <p> 选择是要搜索文件、文件夹，还是同时搜索两者。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL搜索]</p> </td> 
   <td> <p>选择要执行的搜索类型。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL在文件/文件夹名称内搜索]</strong> </p> 
      <ul> 
       <li> <p><strong>[！UICONTROL查询]</strong> </p> <p>输入要搜索的文件名的一部分或完整文件名（包括后缀）。</p> </li> 
       <li> <p><strong>[！UICONTROL搜索选项]</strong> </p> <p>选择是要搜索确切的搜索词，还是要搜索包含该搜索词的名称。</p> </li> 
      </ul> </li> 
     <li> <p><strong>[！UICONTROL Fulltext]搜索</strong> </p> 
      <ul> 
       <li> <p><strong>[！UICONTROL查询]</strong> </p> <p>输入要在[!DNL Google Drive]中搜索的任何搜索词。</p> </li> 
      </ul> </li> 
     <li> <p><strong>输入自定义搜索查询</strong> </p> 
      <ul> 
       <li> <p><strong>[！UICONTROL查询]</strong> </p> <p>输入自定义搜索查询。 有关更多详细信息，请参阅本文的[！UICONTROL搜索文件]部分。</p> </li> 
       <li> <p><strong>将上面选择的文件夹添加到查询</strong> </p> <p>在父收藏集中搜索文件夹。 这会查找直接位于上面所选文件夹中的所有文件和文件夹。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL返回结果的最大数目]</td> 
   <td>设置Workfront Fusion在一个执行周期内返回的文件或文件夹的最大数量。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL即使模块未返回任何结果，仍继续执行路由]</td> 
   <td>启用此选项以确保在模块未返回任何结果时不会停止该方案。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新文件]

此操作模块可更新文件的元数据或内容。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL目标]</td> 
   <td> <p>选择包含要更新的文件的目标。</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL移至文件夹]</td> 
   <td>如果要将文件移动到特定文件夹，请选择要将文件移动到其中的文件夹。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件ID]</td> 
   <td>映射要更新的文件的ID。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL标题]</td> 
   <td>输入更新文件的标题。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL更改文件内容]</td> 
   <td>选择是否要替换文件的内容。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Source file]</td> 
   <td>如果要替换内容，请从以前的模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Conver a file]</td> 
   <td>启用此选项以将文件转换为相应的Google文件格式。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上载文件]

将文件上传到您的[!DNL Google Drive]。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Drive]帐户连接到Workfront Fusion的说明，请参阅<a href="#connecting-google-drive-to-workfront-fusion" class="MCXref xref">将[!DNL Google Drive]连接到[！UICONTROL Workfront Fusion]</a></p> </td> 
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
   <td>[！UICONTROL目标文件夹]</td> 
   <td>选择要将文件上传到的文件夹。 </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Source file]</td> 
   <td>从上一个模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL标题]</td> 
   <td>输入新文件的标题。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL转换文件]</td> 
   <td>启用此选项将允许模块将文件转换为相应的[!DNL Google]格式。</td> 
  </tr> 
 </tbody> 
</table>

## 故障排除

### 无法上传或更新文件

上传或更新文件失败的原因有多种：

* 上传的文件太大，超过了您的[!DNL Google Drive]计划允许的最大文件大小限制，或者您已超过[!DNL Google Drive]存储限制。 您可以升级存储计划，也可以从[!DNL Google Drive]服务中删除现有文件。
* 要将文件上载到的所选文件夹不再存在。 在这种情况下，场景将停止，您必须在该模块中选择不同的目标文件夹。

<!-- Not present February 2025

## Search for files

In the module List files in a folder you can use your own query which consists of these parts:

* **[!UICONTROL Field]** - Attribute of the file that is being searched, for example, the attribute `name` of the file.

* **[!UICONTROL Operator]** - Test that is performed on the data to provide a match, for example, `contains`.

* **[!UICONTROL Value]** - The content of the attribute that is tested, for example, the name of the file `My cool document`.

Combine clauses with the conjunctions `and` or `or`, and negate the query with `not`.

* [Fields](#fields)
* [Value types](#value-types)
* [Operators](#operators)
* [Examples](#examples)

### Fields 

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Field </th> 
   <th>Value Type </th> 
   <th>Operators</th> 
   <th> <p> Description</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>[!UICONTROL title]</code></td> 
   <td>string</td> 
   <td><code>contains</code><sup>1</sup>, <code>=</code>, <code>!=</code></td> 
   <td> <p> Name of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL fullText]</code> </td> 
   <td>string </td> 
   <td><code>contains</code><sup>2, 3</sup> </td> 
   <td> <p> Full text of the file including name, description, content, and indexable text.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL mimeType]</code> </td> 
   <td> string</td> 
   <td><code>contains</code>, <code>=</code>, <code>!=</code></td> 
   <td> <p> MIME type of the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL modifiedDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code> &lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date of the last modification to the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL lastViewedByMeDate]</code> </td> 
   <td> date<sup>4</sup></td> 
   <td><code>&lt;=</code>, <code>&lt;</code>, <code>=</code>, <code>!=</code>, <code>></code>, <code>>=</code></td> 
   <td> <p> Date that the user last viewed a file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL trashed]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Whether the file is in the trash or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL starred]</code></td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p>Whether the file is starred or not.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL parents]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Whether the [!UICONTROL parents] collection contains the specified ID.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL owners]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who own the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL writers]</code></td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to modify the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL readers] </code> </td> 
   <td>collection </td> 
   <td><code>in </code> </td> 
   <td> <p>Users who have permission to read the file.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL sharedWithMe]</code> </td> 
   <td>boolean </td> 
   <td><code>=</code>, <code>!=</code></td> 
   <td> <p> Files that are in the user's "Shared with me" collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>[!UICONTROL properties] </code> </td> 
   <td>collection</td> 
   <td><code>has </code> </td> 
   <td> <p> Public custom file properties.</p> </td> 
  </tr> 
 </tbody> 
</table>

Consider the following about operators in these fields:

* The `contains` operator only performs prefix matching for a `title`.

   For example, the title "HelloWorld" matches for `title contains 'Hello'` but not for `title contains 'World'`.

* The `contains` operator only performs matching on entire string tokens for `fullText`.

   For example, if the full text of a doc contains the string "HelloWorld" only the query `fullText contains 'HelloWorld'` returns a result. Queries such as `fullText contains 'Hello'` would not return results in this scenario.

* The `contains` operator matches on an exact alphanumeric phrase if it is surrounded by double quotes.

   For example, if the `fullText` of a doc contains the string "Hello there world", then the query `fullText contains '"Hello there"'` returns a result, but the query `fullText contains '"Hello world"'` does not.

   Furthermore, because the search is alphanumeric, if the `fullText` of a doc contains the string "Hello_world", then the query `fullText contains '"Hello world"'` returns a result.

* Fields of `type` date are currently not comparable to each other, only to constant dates.

### Value types

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Value Type</th> 
   <th> <p> Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>String </td> 
   <td> <p>Surround with single quotes '. Escape single quotes in queries with <code>\'</code>, e.g.,<code> 'Valentine\'s Day'</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Boolean </td> 
   <td> <p><code>true </code>or <code>false</code>.</p> </td> 
  </tr> 
  <tr> 
   <td>Date </td> 
   <td> <p>RFC 3339 format, default timezone is UTC, e.g., <code>2012-06-04T12:00:00-08:00</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Operators

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Operator </th> 
   <th> <p>Notes</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>contains</code></td> 
   <td> <p>The content of one string is present in the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>=</code> </td> 
   <td> <p> The content of a string or boolean is equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>!=</code> </td> 
   <td> <p> The content of a string or boolean is not equal to the other.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;</code> </td> 
   <td> <p> A date is earlier than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>&lt;=</code> </td> 
   <td> <p> A date is earlier than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>></code> </td> 
   <td> <p> A date is later than another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>>=</code> </td> 
   <td> <p> A date is later than or equal to another.</p> </td> 
  </tr> 
  <tr> 
   <td><code>in </code> </td> 
   <td> <p>An element is contained within a collection.</p> </td> 
  </tr> 
  <tr> 
   <td><code>and </code> </td> 
   <td> <p>Return files that match both clauses.</p> </td> 
  </tr> 
  <tr> 
   <td><code>or </code> </td> 
   <td> <p>Return files that match either clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>not </code> </td> 
   <td> <p>Negates a search clause.</p> </td> 
  </tr> 
  <tr> 
   <td><code>has </code> </td> 
   <td> <p>A collection contains an element matching the parameters.</p> </td> 
  </tr> 
 </tbody> 
</table>

For compound clauses, you can use parentheses to group clauses together. For example:
`modifiedDate > '2012-06-04T12:00:00' and (mimeType contains 'image/' or mimeType contains 'video/')` This search returns all files with an image or video MIME type that their last modification was after June 4, 2012. Because `and` and `or` operators are evaluated from left to right, without parentheses, the above example would return only images modified after June 4, 2012, but would return all videos, even those before June 4, 2012.

### Examples 

All examples on this page show the unencoded `<q>q</q>` parameter, where `title = 'hello'` is encoded as `title+%3d+%27hello%27`. Client libraries handle this encoding automatically.

* Search for files with the name "hello"
   <pre>title = 'hello'</pre>
* Search for folders using the folder-specific MIME type
   <pre>mimeType = 'application/vnd.google-apps.folder'</pre>
* Search for files that are not folders
   <pre>mimeType != 'application/vnd.google-apps.folder'</pre>
* Search for files with a name containing the words "hello" and "goodbye"
   <pre>title contains 'hello' and [!UICONTROL name] contains 'goodbye'</pre>
* Search for files with a name that does not contain the word "hello"
   <pre>not title contains 'hello'</pre>
* Search for files containing the word "hello" in the content
   <pre>fullText contains 'hello'</pre>
* Search for files not containing the word "hello" in the content
   <pre>not fullText contains 'hello'</pre>
* Search for files containing the exact phrase "hello world" in the content
   <pre>fullText contains '"hello world"'fullText contains '"hello_world"'</pre>
* Search for files with a query containing the "\" character (e.g., "\authors")
   <pre>fullText contains '\\authors'</pre>
* Search for files writeable by the user `test@example.org`
   <pre>'test@example.org' in [!DNL writers]</pre>
* Search for the ID `1234567` in the `parents` collection. This finds all files and folders located directly in the folder whose ID is `1234567`.
   <pre>'1234567' in [!UICONTROL parents]</pre>
* Search for the alias ID `appDataFolder` in the `parents` collection. This finds all files and folders located directly under the [Application Data folder](https://developers.google.com/drive/api/v2/appdata).
   <pre>'appDataFolder' in parents</pre>
* Search for files writeable by the users `test@example.org` and `test2@example.org`
   <pre>'test@example.org' in writers and 'test2@example.org' in writers</pre>
* Search for files containing the text "important" which are in the trash
   <pre>fullText contains 'important' and trashed = true</pre>
* Search for files modified after June 4th 2012
   <pre>modifiedDate > '2012-06-04T12:00:00' // default time zone is UTC</pre><pre>modifiedDate > '2012-06-04T12:00:00-08:00'</pre>
* Search for files shared with the authorized user with "hello" in the name
   <pre>sharedWithMe and title contains 'hello'</pre>
* Search for files with a [custom file property](https://developers.google.com/drive/api/v2/properties) named `additionalID` with the value `8e8aceg2af2ge72e78`.
   <pre>properties has { key='additionalID' and value='8e8aceg2af2ge72e78' and visibility='PRIVATE' }</pre>

Source of this guide is [[!DNL Google Drive] documentation](https://developers.google.com/drive/api/v2/search-shareddrives).

-->
