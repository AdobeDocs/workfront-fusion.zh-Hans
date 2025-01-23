---
title: Microsoft OneDrive模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用OneDrive的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: d21eafad-9c67-4f42-b718-0aa4223846e6
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '3285'
ht-degree: 0%

---

# [!DNL Microsoft OneDrive]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL OneDrive]的工作流，并将其连接到多个第三方应用程序和服务。

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

## 先决条件

要使用[!DNL OneDrive]模块，您必须具有[!DNL Microsoft OneDrive]帐户。



## OneDrive API信息

OneDrive连接器使用以下功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://graph.microsoft.com/v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>


## 正在将[!DNL OneDrive]服务连接到[!DNL Workfront Fusion]

有关将[!DNL OneDrive]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
>
>例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。

## [!DNL Microsoft OneDrive]模块及其字段

配置[!DNL OneDrive]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL OneDrive]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [文件/文件夹](#filefolder)
* [其他](#other)

### 文件/文件夹

* [[!UICONTROL Watch Files/Folders]](#watch-filesfolders)
* [[!UICONTROL Search Files/Folders]](#search-filesfolders)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL Download a file]](#download-a-file)
* [[!UICONTROL Upload a file]](#upload-a-file)
* [[!UICONTROL Create a Folder]](#create-a-folder)
* [[!UICONTROL Get a Share Link]](#get-a-share-link)
* [[!UICONTROL Move a File/Folder]](#move-a-filefolder)
* [[!UICONTROL Copy a File]](#copy-a-file)
* [[!UICONTROL Delete a File/Folder]](#delete-a-filefolder)

#### [!UICONTROL Watch Files/Folders]

此触发器模块会在创建或更新文件或文件夹时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Files/Folders]</td> 
   <td> <p>选择监视文件或文件夹的方式：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL By Created Time]</b> </p> <p>请注意新文件或文件夹。</p> </li> 
     <li> <p><b>[!UICONTROL By Updated Time]</b> </p> <p>请注意已更新的现有文件或文件夹。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择要监视的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入您希望模块监视的驱动器ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> <p>导航到您希望模块监视的文件夹。 您还可以输入查询以筛选返回的结果。</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Shared With Me]</b> </p> <p>模块会监视与驱动器所有者共享的文件。</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择要让模块关注的SharePoint站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择要让模块监视其驱动器的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose an Item Type]</td> 
   <td> <p>选择是要监视文件、文件夹还是同时监视两者。</p> <p>注意：您无法监视[!UICONTROL Shared With Me]驱动器中的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Search Files/Folders]

此搜索模块会根据您设置的条件返回文件和文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择要搜索的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入您希望模块搜索的驱动器的ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> <p>导航到您希望模块搜索的文件夹。 您还可以输入查询以筛选返回的结果。</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Shared With Me]</b> </p> <p>模块将搜索与驱动器所有者共享的文件。</p> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择要模块搜索的[!DNL SharePoint]站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择要搜索模块的驱动器的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose an Item Type]</td> 
   <td> <p>选择是要搜索文件、文件夹，还是同时搜索两者。</p> <p>注意：您不能在[!UICONTROL Shared With Me]驱动器中搜索文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a file]

此操作模块获取指定文件的元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>选择是要按文件ID还是按文件路径标识文件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>选择您要如何输入文件ID或文件路径：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>如果要直接输入ID或路径，或者从上一个模块中映射该ID或路径，请选择此选项。</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>如果要从可用文件或路径列表中进行选择，请选择此选项。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择要搜索的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入包含要获取文件的驱动器的ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择包含要获取的文件的SharePoint站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择其驱动器包含要获取文件的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择或映射包含要获取文件的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td> 
   <td> <p>如果您选择了[!UICONTROL Enter Manually]，请输入或映射要获取的文件ID或路径。</p> <p>如果您选择了[!UICONTROL Select from the list]，请选择要获取的文件。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a file]

此操作模块下载指定的文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>选择是要按文件ID还是按文件路径标识文件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">输入文件ID/文件路径</td> 
   <td> <p>选择您要如何输入文件ID或文件路径：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>如果要直接输入ID或路径，或者从上一个模块中映射该ID或路径，请选择此选项。</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>如果要从可用文件或路径列表中进行选择，请选择此选项。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择要包含要下载的文件的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入包含要下载的文件的驱动器的ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择包含要下载的文件的SharePoint站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择其驱动器包含要下载的文件的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择或映射包含要下载的文件的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td>
   <td> <p>如果选择[!UICONTROL Enter Manually]，请输入或映射要下载的文件的文件ID或路径。</p> <p>如果您选择了[!UICONTROL Select from the list]，请选择要下载的文件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Convert to PDF]</td> 
   <td> <p>启用此选项可将文件转换为PDF文件。 您可以从以下文件类型进行转换：</p> 
    <table style="table-layout:auto"> 
     <col> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td> 
        <ul> 
         <li> <p> <p>CSV</p> </p> </li> 
         <li> <p> <p>DOC</p> </p> </li> 
         <li> <p> <p>DOCX</p> </p> </li> 
         <li> <p> <p>ODP</p> </p> </li> 
         <li> <p> <p>ODS</p> </p> </li> 
         <li> <p> <p>ODT</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p> <p>POT</p> </p> </li> 
         <li> <p> <p>POTM</p> </p> </li> 
         <li> <p> <p>POTX</p> </p> </li> 
         <li> <p> <p>PPS</p> </p> </li> 
         <li> <p> <p>PPSX</p> </p> </li> 
         <li> <p> <p>PPSXM</p> </p> </li> 
        </ul> </td> 
       <td> 
        <ul> 
         <li> <p>PPT</p> </li> 
         <li> <p>PPTM</p> </li> 
         <li> <p>PPTX</p> </li> 
         <li> <p>RTF</p> </li> 
         <li> <p>XLS</p> </li> 
         <li> <p>XLSX</p> </li> 
        </ul> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

此操作模块将文件上传到指定的文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">输入（文件夹位置ID和路径）</td> 
   <td>选择是要按ID还是按路径标识目标文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择上载文件的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>选择包含要获取文件的驱动器。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择包含要上载文件的文件夹的[!DNL SharePoint]站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择其驱动器包含要上载文件的文件夹的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择包含要上载文件的文件夹的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL If the File with the Same Name Exists]</td> 
   <td>选择当同名文件已存在时如何继续。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>向上传的文件添加说明。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Folder]

此操作模块在指定的驱动器中创建新文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择要创建文件夹的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>选择要创建文件夹的驱动器。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择要创建文件夹的[!DNL SharePoint]站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择拥有要在其中创建文件夹的驱动器的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择要创建文件夹的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>如果您希望新文件夹成为子文件夹，请导航到您希望它成为子文件夹的文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Folder Name]</td> 
   <td> <p>输入或映射新文件夹的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL If the Folder with the Same Name Exists]</td> 
   <td>选择当同名文件已存在时如何继续。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a Share Link]

此操作模块返回指定文件的共享链接。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>选择是要按文件ID还是按文件路径标识文件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>选择您要如何输入文件ID或文件路径：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>如果要直接输入ID或路径，或者从上一个模块中映射该ID或路径，请选择此选项。</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>如果要从可用文件或路径列表中进行选择，请选择此选项。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择要检索共享链接的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入包含要检索共享链接文件的驱动器ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择包含要检索共享链接的文件的SharePoint站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择其驱动器包含要检索共享链接文件的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择或映射包含要检索共享链接文件的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td> 
   <td> <p>如果选择[!UICONTROL Enter Manually]，请输入或映射要检索共享链接的文件的ID或路径。</p> <p>如果您从列表中选择[!UICONTROL Select]，请选择您要检索共享链接的文件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Permission Type]</td> 
   <td> <p>选择您希望具有链接的用户能够读写文件，还是只读。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scope]</td> 
   <td>选择您希望文件对具有此链接的任何人都可用，还是只对具有此链接的组织成员可用。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a File/Folder]

此操作模块会将文件或文件夹移动到新的文件夹位置

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>选择是要按文件ID还是按文件路径标识文件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID / File Path]</td> 
   <td> <p>选择您要如何输入文件ID或文件路径：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>如果要直接输入ID或路径，或者从上一个模块中映射该ID或路径，请选择此选项。</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>如果要从可用文件或路径列表中进行选择，请选择此选项。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择包含要移动的文件或文件夹的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入包含要移动的文件或文件夹的驱动器的ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择包含要移动的文件或文件夹的[!DNL SharePoint]站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择其驱动器包含要移动的文件或文件夹的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择或映射包含要移动的文件或文件夹的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">选择 [!UICONTROL File/Folder]</td> 
   <td>选择您要移动文件或文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</p> <p role="rowheader">[!UICONTROL Folder] / [!UICONTROL Folder ID] / [!UICONTROL Folder Path]</p> </td> 
   <td> <p>如果选择[!UICONTROL Enter Manually]，请输入或映射要移动的文件或文件夹的ID或路径。</p> <p>如果您从列表中选择[!UICONTROL Select]，请选择要移动的文件或文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a New Folder Location]</td> 
   <td> <p>选择您希望如何输入要将文件或文件夹移动到的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>如果要直接输入ID或路径，或者从上一个模块中映射该ID或路径，请选择此选项。</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>如果要从可用文件或路径列表中进行选择，请选择此选项。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择要移动文件或文件夹的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入要移动文件或文件夹的驱动器的ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择要移动文件或文件夹的[!DNL SharePoint]站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择要将文件或文件夹移动到其驱动器的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择或映射包含要移动文件或文件夹的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> <p>如果将此留空，则文件或文件夹只能在同一[!DNL OneDrive]中移动。</p> <p>您可以将文件和文件夹从[!UICONTROL My Drive]移动到[!UICONTROL Site's Drive]或[!UICONTROL Group's Drive]。 </p> <p>您只能将文件从[!UICONTROL Site's Drive]移到同一站点中的同一驱动器。</p> <p>您只能将文件从[!UICONTROL Group's Drive]移到同一组中的同一驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>输入或映射要移动文件或文件夹的文件夹。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy a File]

此操作模块将文件复制到新的文件夹位置

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File ID & File Path)]</td> 
   <td>选择是要按文件ID还是按文件路径标识文件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File ID] / [!UICONTROL File Path]</td> 
   <td> <p>选择您要如何输入文件ID或文件路径：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>如果要直接输入ID或路径，或者从上一个模块中映射该ID或路径，请选择此选项。</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>如果要从可用文件或路径列表中进行选择，请选择此选项。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择包含要复制文件的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入包含要复制的文件或文件夹的驱动器的ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择包含要移动的文件的SharePoint站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择其驱动器包含要复制文件的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择或映射包含要复制文件的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</p> </td> 
   <td> <p>如果您选择了[!UICONTROL Enter Manually]，请输入或映射要复制的文件的ID或路径。</p> <p>如果您从列表中选择[!UICONTROL Select]，请选择要复制的文件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a New Folder Location]</td> 
   <td> <p>选择您希望如何输入要复制文件的位置或：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>如果要直接输入ID或路径，或者从上一个模块中映射该ID或路径，请选择此选项。</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>如果要从可用文件夹列表中进行选择，请选择此选项。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New OneDrive location]</td> 
   <td> <p>选择要复制文件服务器的位置。 如果您选择从列表中选择新文件夹位置，则此选项可用。</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入要复制文件的驱动器的ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择要将文件复制到其中的[!DNL SharePoint]站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择要将文件复制到其驱动器的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择或映射包含要向其复制文件的文件夹的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> <p>如果将此留空，则文件或文件夹只能复制到同一[!UICONTROL OneDrive]中。</p> <p>您可以将文件和文件夹从[!UICONTROL My Drive]复制到[!UICONTROL Site's Drive]或[!UICONTROL Group's Drive]。 </p> <p>您只能将文件从[!UICONTROL Site's Drive]复制到同一站点中的同一驱动器。</p> <p>您只能将文件从[!UICONTROL Group's Drive]复制到同一组中的同一驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>输入或映射要移动副本或文件夹的文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New Copied File Name]</td> 
   <td> <p>输入或映射文件新副本的名称。 如果不想更改原始文件名，可将此项留空。</p> <p>名称必须包含文件扩展名。 示例：<code> file.txt</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a File/Folder]

此操作模块删除选定的文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter (File/Folder ID & Path)]</td> 
   <td>选择是要按文件ID还是按文件路径标识文件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a File/Folder ID /Enter a File/Folder Path]</td> 
   <td> <p>选择您要如何输入文件ID或文件路径：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Enter Manually]</b> </p> <p>如果要直接输入ID或路径，或者从上一个模块中映射该ID或路径，请选择此选项。</p> </li> 
     <li> <p><b>[!UICONTROL Select from a list]</b> </p> <p>如果要从可用文件或路径列表中进行选择，请选择此选项。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Choose your [!DNL OneDrive] 位置]</td> 
   <td> <p>选择要搜索的位置：</p> 
    <ul> 
     <li> <p><b>[!UICONTROL My Drive]</b> </p> <p>选择是否启用模块以输入驱动器ID。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Yes]</b> </p> <p>输入包含要删除的文件或文件夹的驱动器ID。</p> </li> 
       <li> <p><b>[!UICONTROL No]</b> </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Site's Drive]</b> </p> <p>选择包含要删除的文件或文件夹的[!DNL SharePoint]站点。 可用站点是后跟登录用户的站点。</p> </li> 
     <li> <p><b>[!UICONTROL Group's Drive]</b> </p> <p>选择其驱动器包含要删除的文件或文件夹的组。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Drive ID]</td> 
   <td> <p>选择或映射包含要删除的文件或文件夹的驱动器。 如果您在[!UICONTROL Enable to Enter a Drive ID]字段中选择了[!UICONTROL No]，则此字段不可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">选择 [!UICONTROL File/Folder]</td> 
   <td>选择您要删除文件或文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File] / [!UICONTROL File ID] / [!UICONTROL File Path]</td>
   <td> <p>如果选择[!UICONTROL Enter Manually]，请输入或映射要删除的文件的文件ID或路径。</p> <p>如果您从列表中选择[!UICONTROL Select]，请选择要删除的文件。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

#### [!UICONTROL Make an API Call]

此模块执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关将[!DNL OneDrive]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code>https://graph.microsoft.com</code>的路径。 示例：<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>



## 如果您无法上传或更新文件

上传或更新文件失败时，可能会出现几个问题：

* 上传的文件太大，超过了您[!DNL OneDrive]计划的最大文件大小限制，或者您已使用所有[!DNL OneDrive]帐户的存储配额。 若要获得更多存储空间，请从[!DNL OneDrive]中删除现有文件或升级您的[!DNL OneDrive]帐户。
* OneDrive不允许将两个同名文件上载到一个文件夹。 如果目标文件夹包含的文件与正在上传的文件同名，则场景运行将终止，并出现错误。 解决方案是简单地重命名要上传的文件。 如果您的目的是更新文件，请使用[!UICONTROL Update a file]操作。
* 先前选择的文件夹（文件将上载到该文件夹）不再存在。 场景将停止，您将需要再次选择目标文件夹。
