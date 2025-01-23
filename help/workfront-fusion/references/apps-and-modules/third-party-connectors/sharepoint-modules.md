---
title: SharePoint模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用SharePoint的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '2270'
ht-degree: 0%

---

# [!DNL SharePoint]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL SharePoint]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL SharePoint]模块，您必须具有[!DNL SharePoint]帐户。

## SharePoint API信息

SharePoint连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.14.2</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL SharePoint]连接到[!DNL Workfront Fusion] {#connect-sharepoint-to-workfront-fusion}

* [使用 [!DNL Microsoft] 帐户连接 [!DNL SharePoint] 到 [!DNL Workfront Fusion] ](#connect-sharepoint-to-workfront-fusion-using-a-microsoft-account)
* [使用高级设置连接 [!DNL SharePoint] 到 [!DNL Workfront Fusion] ](#connect-sharepoint-to-workfront-fusion-using-advanced-settings)

### 使用[!DNL Microsoft]帐户将[!DNL SharePoint]连接到[!DNL Workfront Fusion]

您可以使用您的[!DNL Microsoft]帐户创建与[!DNL SharePoint]的连接。 有关将[!DNL Sharepoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅[创建与 [!DNL Adobe Workfront Fusion] 的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### 使用高级设置将[!DNL SharePoint]连接到[!DNL Workfront Fusion]

要在没有[!DNL Microsoft]帐户的情况下将[!DNL SharePoint]连接到[!DNL Workfront Fusion]，您需要客户端ID、客户端密钥和租户ID。

1. 单击&#x200B;**[!DNL SharePoint]**&#x200B;框顶部附近的&#x200B;**[!UICONTROL Add]**&#x200B;以打开&#x200B;**[!UICONTROL Create a connection]**&#x200B;框。

1. （可选）更改默认&#x200B;**[!UICONTROL Connection name]**。
1. 单击 **[!UICONTROL Show advanced settings]**。
1. 输入[!DNL SharePoint] **[!UICONTROL Client ID]**&#x200B;和&#x200B;**[!UICONTROL Client Secret]**。

1. 单击 **[!UICONTROL Continue]**。
1. 在显示的登录窗口中，输入您的凭据以登录应用程序（如果尚未登录）。
1. （视情况而定）如果显示&#x200B;**[!UICONTROL Allow]**&#x200B;按钮，请单击该按钮以将应用程序连接到[!DNL Workfront Fusion]。

## [!DNL SharePoint]模块及其字段

配置[!DNL SharePoint]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL SharePoint]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [驱动器项目](#drive-item)
* [项](#item)
* [列表](#list)
* [页面(Beta)](#page-beta)
* [站点](#site)
* [其他](#other)

### 驱动器项目

* [创建文件](#create-a-file)
* [创建文件夹](#create-a-folder)
* [获取文件](#get-a-file)
* [监视文件夹项目](#watch-folder-items)

#### 获取更改

此模块会返回在SharePoint中所做的更改。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>选择您希望如何标识要检索更改的文件夹的位置。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL List ID]</strong>和<strong>[!UICONTROL Folder ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>选择要检索更改的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> </td> 
  </tr>  </tbody> 
</table>

#### 创建文件夹

此操作模块在SharePoint中创建新文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>选择您希望如何标识要创建的文件夹的位置。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL List ID]</strong>和<strong>[!UICONTROL Folder ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>选择要创建文件夹的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder name]</td> 
   <td>输入或映射新文件夹的名称。</td> 
  </tr>
  </tbody> 
</table>

#### 获取文件

此操作模块可检索指定的SharePoint文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>选择您希望如何标识要获取的文件位置。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL List ID]</strong>和<strong>[!UICONTROL File ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>选择文件的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### 监视文件夹项目

当您选择的文件夹中更新了某个项目时，此触发器模块会启动一个方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>选择您希望如何标识要获取的文件位置。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL List ID]</strong>和<strong>[!UICONTROL folder ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>选择要监视的文件夹的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入在一个方案执行周期内应返回的项目[!DNL Workfront Fusion]的最大数目。</td> 
  <tr>
  </tr>
</tbody> 
</table>

### 项

* [[!UICONTROL Copy an item]](#copy-an-item)
* [[!UICONTROL Create an item]](#create-an-item)
* [[!UICONTROL Delete an item]](#delete-an-item)
* [[!UICONTROL Get an Item]](#get-an-item)
* [[!UICONTROL List Items]](#list-items)
* [[!UICONTROL Move Item]](#move-an-item)
* [[!UICONTROL Update an item]](#update-an-item)
* [[!UICONTROL Watch Items] （已计划）](#watch-items-scheduled)


#### [!UICONTROL Copy Item]

此操作模块复制SharePoint列表中的现有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">输入站点、驱动器和文件夹ID</td> 
   <td> <p>选择您希望如何标识站点以及包含要复制项目的列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL List ID]</strong>和<strong>[!UICONTROL Item ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>在“项目类型”字段中，选择要移动字段还是文件夹。  选择包含要复制项目的站点，然后选择列表，然后选择项目。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> 输入或映射要向其复制项目的文件夹的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>输入或映射项目新副本的名称。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an item]

此操作模块在SharePoint列表中创建新项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Create an Item]</td> 
   <td> <p>选择您希望如何标识站点以及您希望创建项目的列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>和<strong>[!UICONTROL List ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要在其中创建项目的列表的站点，然后选择列表。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>对于要为新项目设置的每个字段，输入该字段的键（标识该字段），以及您希望新项目在该字段中的值。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an item]

此操作模块删除SharePoint列表中的现有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>选择您希望如何标识站点以及包含要删除项目的列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL List ID]</strong>和<strong>[!UICONTROL Item ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要删除项目的站点，然后选择列表，然后选择项目。 </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an Item]

此操作模块返回指定项的数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get an Item]</td> 
   <td> <p>选择您希望如何标识站点以及包含您要获取项目的列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL List ID]</strong>和<strong>[!UICONTROL Item ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要从中检索项目的列表的站点，然后选择该列表，然后选择该项目。 </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Items]

此操作模块检索指定列表中所有项目的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Items]</td> 
   <td> <p>选择您希望如何标识要从中检索项目的列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>和<strong>[!UICONTROL List ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要从中检索项目的列表的站点，然后选择该列表。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大项目数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Item]

此操作模块复制SharePoint列表中的现有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">输入站点、驱动器和文件夹ID</td> 
   <td> <p>选择您希望如何标识站点以及包含要移动项目的列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL List ID]</strong>和<strong>[!UICONTROL Item ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from list that you follow]</strong> </p> <p>在“项目类型”字段中，选择要移动字段还是文件夹。 选择包含要复制项目的站点，然后选择列表，然后选择项目。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination ID]</td> 
   <td> 输入或映射要将项目移动到的文件夹的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL New name]</td> 
   <td>输入或映射已移动项目的名称。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an item]

此操作模块更新SharePoint列表中的现有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update an Item]</td> 
   <td> <p>选择您要如何标识包含要更新的项目的站点和列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL List ID]</strong>和<strong>[!UICONTROL Item ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要更新的项目的站点，然后选择列表，然后选择项目。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td>对于要更新新项目的每个字段，请输入该字段的键值（标识该字段），以及希望项目在该字段具有的新值。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Items] （已计划）

此触发器模块会在创建或修改项目时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>选择是要按创建时间（新项目）还是按修改时间（更新项目）监视列表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>选择您希望如何识别要监视的站点和列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>和<strong>[!UICONTROL List ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>选择要监视的站点，然后选择列表。 这些下拉列表仅检索关注的网站。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大项目数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 列表

* [[!UICONTROL Create a List]](#create-a-list)
* [[!UICONTROL Get a List]](#get-a-list)
* [[!UICONTROL List Lists]](#list-lists)
* [[!UICONTROL Watch Lists]](#watch-lists)

#### [!UICONTROL Create a List]

此操作模块可在SharePoint中创建新列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a Site ID]</td> 
   <td> <p>选择您希望如何标识站点以及您希望创建列表的列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>输入或映射要在其中创建列表的<strong>[!UICONTROL Site ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择要创建列表的站点。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display Name]</td> 
   <td>输入或映射新列表的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>输入或映射新列表的说明。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Add Columns]</td> 
   <td>对于要为新列表设置的每一列，为该字段输入<strong>[!UICONTROL Name]</strong>，然后选择希望新列具有的值<strong>[!UICONTROL Type]</strong>。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a List]

此操作模块返回指定列表的数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a List]</td> 
   <td> <p>选择您希望如何标识站点以及包含您要获取项目的列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>和<strong>列表ID</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要检索的列表的站点，然后选择该列表。 </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Lists]

此操作模块检索指定列表中所有项目的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List Lists]</td> 
   <td> <p>选择您希望如何标识要从其中检索列表的站点。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>输入或映射<strong>[!UICONTROL Site ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要检索的列表的站点。 下拉列表将仅检索您关注的站点。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大列表数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Lists]

此触发器模块会在创建或修改列表时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch Lists]</td> 
   <td>选择是要按创建时间（新项目）还是按修改时间（更新项目）监视列表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site and List ID]</td> 
   <td> <p>选择您希望如何识别要监视的站点和列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>输入或映射要监视的列表所在的<strong>[!UICONTROL Site ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list that you follow]</strong> </p> <p>选择要监视的站点。 下拉列表只会检索您关注的站点。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大列表数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 页面(Beta)

>[!NOTE]
>
>[!DNL Microsoft Graph]中`beta`版本的API可能会发生更改。 不支持在生产应用程序中使用这些API。

#### [!UICONTROL Get a Page]

此操作模块返回指定页面的数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Page]</td> 
   <td> <p>选择您希望如何标识要检索的页面。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>输入或映射<strong>[!UICONTROL Site ID]</strong>和<strong>[!UICONTROL Page ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要检索的页面的站点，然后选择该页面。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### 站点

* [[!UICONTROL Get a Site]](#get-a-site)
* [[!UICONTROL Search Sites]](#search-sites)

#### [!UICONTROL Get a Site]

此操作模块返回指定站点的数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get a Site]</td> 
   <td> <p>选择您希望如何标识要检索的页面。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>输入或映射<strong>[!UICONTROL Site ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择要检索的站点。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Sites]

此操作模块按您指定的参数搜索站点。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword of Display Name]</td> 
   <td> <p>输入或映射要搜索网站的搜索词。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大网站数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

* [获取更改](#get-changes)
* [进行API调用](#make-an-api-call)
* [观看活动](#watch-events)

#### 获取更改

此模块可检索在SharePoint文件夹中所做的添加、更新和删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter Site, Drive, and Folder IDs]</td> 
   <td> <p>选择您要如何标识包含要更新的项目的站点和列表。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>在显示的字段中输入或映射<strong>[!UICONTROL Site ID]</strong>、<strong>[!UICONTROL Drive ID]</strong>和<strong>[!UICONTROL Folder ID]</strong>。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要更新的项目的站点，然后选择驱动器，然后选择文件夹。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Token]</td> 
   <td> 该令牌可标识模块应从何时开始检索更改。  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

此模块允许您执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL SharePoint]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL SharePoint]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>输入相对于<code>https://graph.microsoft.com</code>的路径。 示例：<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。例如，<code>{"Content-type":"application/json"}</code>。 [!DNL Workfront Fusion]为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> 以标准JSON对象的形式添加API调用的查询。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>选择您要在API调用中发送的数据类型。</td> 
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

#### 观看活动

在SharePoint中添加、更新或删除项目时，此即时触发模块会启动一个场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
  <!--
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL SharePoint] account to [!DNL Workfront Fusion], see <a href="#connect-sharepoint-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect [!DNL SharePoint] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>选择现有的webhook，或单击“添加”创建新的webhook。</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
