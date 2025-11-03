---
title: Microsoft OneDrive for Business模块
description: 在Adobe Workfront Fusion方案中，您可以自动使用 [!DNL Microsoft OneDrive for Business]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 657bea46-064e-4333-8e86-81678bb1c3bd
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1150'
ht-degree: 0%

---

# [!DNL Microsoft OneDrive for Business]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Microsoft OneDrive for Business]的工作流，并将其连接到多个第三方应用程序和服务。

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

要将[!DNL Microsoft OneDrive for Business]与Adobe Workfront Fusion结合使用，您需要一个[!DNL Microsoft]帐户。

## 正在将[!DNL Microsoft OneDrive for Business]服务连接到Workfront Fusion

有关将[!DNL Microsoft OneDrive for Business]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
>
>例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。

## [!DNL Microsoft OneDrive for Business]模块及其字段

在配置[!DNL Microsoft OneDrive for Business]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Microsoft OneDrive for Business]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)

### 触发器

* [[!UICONTROL 监视文件]](#watch-files)
* [[!UICONTROL 监视文件夹]](#watch-folders)

#### [!UICONTROL 监视文件]

在被监视的文件夹中添加或更新新文件时，此触发器模块将激活。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 驱动器ID]</p> </td> 
   <td> <p>选择要监视的驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹]</td> 
   <td> <p> 选择要监视的文件夹。 在场景中，您只能监视一个文件夹。</p> <p>提示：要监视多个文件夹，请为每个文件夹创建一个独立的方案。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 我要观看]</p> </td> 
   <td> <p>选择是要监视新文件和所有更改，还是只监视新文件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大行数]</td> 
   <td> <p> 设置您希望模块在一个周期内返回的最大结果数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 监视文件夹]

在将新文件夹添加到受监视的文件夹时，此触发器模块将激活。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 驱动器ID]</p> </td> 
   <td> <p>选择要监视的驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹]</td> 
   <td> <p> 选择要监视的文件夹。 在场景中，您只能监视一个文件夹。</p> <p>提示：要跟踪多个文件夹，请为每个文件夹创建一个独立的方案。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 我要观看]</p> </td> 
   <td> <p>选择是要监视新文件夹和所有更改，还是只监视新文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大行数]</td> 
   <td> <p> 设置您希望模块在一个周期内返回的最大结果数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 创建文件夹]](#create-a-folder)
* [[!UICONTROL 删除文件]](#delete-a-file)
* [[!UICONTROL 删除文件夹]](#delete-a-folder)
* [[!UICONTROL 获取文件]](#get-a-file)
* [[!UICONTROL 获取共享链接]](#get-a-sharing-link)
* [[!UICONTROL 上载文件]](#upload-a-file)

#### [!UICONTROL 创建文件夹]

在指定的父文件夹内创建一个文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><strong>[!UICONTROL 连接]</strong> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL 驱动器ID]</strong> </td> 
   <td> <p>选择要创建新文件夹的驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL 文件夹]</strong> </td> 
   <td> <p>选择要在其中创建新文件夹的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td><strong>[!UICONTROL 文件夹名称]</strong> </td> 
   <td>输入或映射新文件夹的名称。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除文件]

此操作模块将指定的文件移动到回收站。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 驱动器ID]</td> 
   <td> <p>选择要从中删除文件的驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文件ID]</td> 
   <td> <p>输入要删除的文件的ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除文件夹]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 驱动器ID]</td> 
   <td> <p>选择要从中删除文件的驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文件夹ID]</td> 
   <td> <p>输入或映射要删除的文件夹的ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取文件]

此操作模块会检索具有给定ID的文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 驱动器ID]</td> 
   <td> <p>选择要从中检索文件的驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文件ID]</td> 
   <td> <p>输入要检索的文件的ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取共享链接]

此模块会检索可共享的链接，以授予对指定文件的访问权限。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 驱动器ID]</td> 
   <td> <p>选择要将文件上传到的驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enter]</td> 
   <td> <p>选择是要使用“文件ID”还是“文件”路径选择文件。 在显示的字段中输入文件ID或路径。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 权限类型]</p> </td> 
   <td> <p>选择您希望接收链接的人员具有读/写权限还是只读权限。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 作用域]</td> 
   <td> <p> 选择您希望拥有链接的任何人都可以访问文件，还是希望只有贵组织的成员才能访问文件。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上载文件]

此操作模块会将二进制文件或文本文件上传到指定的文件夹

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 驱动器ID]</td> 
   <td> <p>选择要将文件上传到的驱动器。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文件夹] </td> 
   <td> <p>选择驱动器中的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Source File]</p> </td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 如果存在同名文件]</td> 
   <td> <p> 选择当与正在尝试上载的文件同名的文件已存在时要执行的操作。</p> 
    <ul> 
     <li>[!UICONTROL 替换现有文件]</li> 
     <li>[!UICONTROL 重命名新文件]</li> 
     <li>[!UICONTROL 以错误结尾]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
