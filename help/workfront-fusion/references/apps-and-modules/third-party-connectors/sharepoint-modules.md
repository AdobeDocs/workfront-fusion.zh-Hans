---
title: SharePoint模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Microsoft SharePoint Online的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 1a09aa86-5e0e-4347-b4cf-2b0a95e5b049
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '4124'
ht-degree: 0%

---

# Microsoft SharePoint Online模块

在Adobe Workfront Fusion场景中，您可以自动使用Microsoft SharePoint Online的工作流，并将其连接到多个第三方应用程序和服务。

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

## 先决条件

要使用Microsoft SharePoint Online模块，您必须拥有Microsoft SharePoint Online帐户。

## SharePoint API信息

SharePoint连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
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

## 将Microsoft SharePoint Online连接到Workfront Fusion {#connect-microsoft-sharepoint-online-to-workfront-fusion}

* [使用 [!DNL Microsoft] 帐户将Microsoft SharePoint Online连接到Workfront Fusion](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-a-microsoft-account)
* [使用高级设置将Microsoft SharePoint Online连接到Workfront Fusion](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-advanced-settings)
* [使用证书授权将Microsoft SharePoint Online连接到Workfront Fusion](#connect-microsoft-sharepoint-online-to-workfront-fusion-using-certificate-authorization)

### 使用[!DNL Microsoft]帐户将Microsoft SharePoint Online连接到Workfront Fusion

您可以使用您的[!DNL Microsoft]帐户创建与Microsoft SharePoint Online的连接。 有关将[!DNL Sharepoint]帐户连接到Workfront Fusion的说明，请参阅[创建与Adobe Workfront Fusion的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

### 使用高级设置将Microsoft SharePoint Online连接到Workfront Fusion

要在连接中包含凭据，请启用显示高级设置选项。 对于此类连接，您需要客户端ID、客户端密钥和租户ID。

1. 在任意SharePoint模块中，单击“连接”字段附近的&#x200B;**[!UICONTROL 添加]**&#x200B;以打开&#x200B;**[!UICONTROL 创建连接]**&#x200B;框。
1. 单击&#x200B;**[!UICONTROL 显示高级设置]**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL连接类型]</p> </td> 
      <td>若要使用客户端凭据，请选择<b>Microsoft 365电子邮件</b>。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL连接名称]</p> </td> 
      <td>输入连接的名称。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL客户端ID]</p> </td> 
      <td>输入您正在连接的SharePoint应用程序的客户端ID。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL客户端密码]</p> </td> 
      <td>输入您连接到的某个SharePoint应用程序的客户端密码。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL租户ID]</p> </td> 
      <td>输入您正在连接的SharePoint应用程序的租户ID。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**继续**&#x200B;保存连接并返回模块。

### 使用证书授权将Microsoft SharePoint Online连接到Workfront Fusion

您可以使用证书授权连接到SharePoint。

>[!IMPORTANT]
>
>要使用证书授权，您必须首先在Microsoft Entra中创建应用程序并将证书上传到该处。
>
>有关说明，请参阅Microsoft文档中的[如何为Microsoft Entra基于证书的身份验证配置证书颁发机构](https://learn.microsoft.com/en-us/entra/identity/authentication/how-to-configure-certificate-authorities)。

1. 在任意SharePoint模块中，单击“连接”字段附近的&#x200B;**[!UICONTROL 添加]**&#x200B;以打开&#x200B;**[!UICONTROL 创建连接]**&#x200B;框。
1. 单击&#x200B;**[!UICONTROL 显示高级设置]**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL连接类型]</p> </td> 
      <td>要使用证书授权，请选择<b>Microsoft SharePoint Online （证书身份验证）</b>。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL连接名称]</p> </td> 
      <td>输入连接的名称。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL客户端ID]</p> </td> 
      <td>输入您正在连接的SharePoint应用程序的客户端ID。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL指纹]</p> </td> 
      <td>输入您要连接的SharePoint应用程序的指纹。</td> 
     </tr> 
      <tr>
        <td role="rowheader">[！UICONTROL私钥]</td>
        <td>
          <p>输入在Microsoft中创建凭据时生成的证书或私钥。 </p>
          <p>要提取您的私钥或证书，请执行以下操作：</p>
          <ol>
            <li>
              <p>单击<b>[！UICONTROL提取]</b>。</p>
            </li>
            <li>
            <p>选择是提取证书还是私钥。</li>
            <li>
              <p>选择要提取的文件类型。</p>
            </li>
            <li>
              <p>选择包含私钥或证书的文件。</p>
            </li>
            <li>
              <p>输入文件的密码。</p>
            </li>
            <li>
              <p>单击<b>[！UICONTROL保存]</b>以提取文件并返回到连接设置。</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody> 
   </table>

1. 单击&#x200B;**继续**&#x200B;保存连接并返回模块。

## Microsoft SharePoint模块及其字段

配置Microsoft SharePoint Online模块时，Workfront Fusion会显示以下列出的字段。 除了这些以外，还可能会显示其他Microsoft SharePoint Online字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [驱动器项目](#drive-item)
* [项目](#item)
* [列表](#list)
* [页面(Beta)](#page-beta)
* [站点](#site)
* [其他](#other)

### 驱动器项目

* [创建文件](#create-a-file)
* [创建文件夹](#create-a-folder)
* [获取文件](#get-a-file)
* [获取文件夹](#get-a-folder)
* [更新文件夹或文件](#update-a-folder-or-a-file)
* [监视文件夹项目](#watch-folder-items)

#### 创建文件

此模块会返回在SharePoint中所做的更改。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点、驱动器和文件夹ID]</td> 
   <td> <p>选择您希望如何标识要检索更改的文件夹的位置。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射文件创建位置的<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL驱动器ID]</strong>和<strong>[！UICONTROL文件夹ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>选择要创建文件的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
      <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p>
  </tr>  </tbody> 
</table>

#### 创建文件夹

此操作模块在SharePoint中创建新文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点、驱动器和文件夹ID]</td> 
   <td> <p>选择您希望如何标识要创建的文件夹的位置。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要创建文件夹的位置的<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL驱动器ID]</strong>和<strong>[！UICONTROL文件夹ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>选择要创建文件夹的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件夹名称]</td> 
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
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点、驱动器和文件夹ID]</td> 
   <td> <p>选择您希望如何标识要获取的文件位置。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>为要检索的文件输入或映射<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL列表ID]</strong>和<strong>[！UICONTROL文件ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>选择文件的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### 获取文件夹

此模块已检索有关指定文件夹的详细信息

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点、驱动器和文件                ID]</td> 
   <td> <p>选择您希望如何标识要获取的文件位置。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>为要检索的文件夹输入或映射<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL列表ID]</strong>和<strong>[！UICONTROL文件夹路径]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>选择文件夹的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
</tbody> 
</table>

#### 更新文件夹或文件

此操作模块更新文件夹或文件的元数据

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点、驱动器和文件                ID]</td> 
   <td> <p>选择您希望如何标识要获取的文件位置。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>为要检索的文件夹或文件输入或映射<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL列表ID]</strong>和<strong>[！UICONTROL文件夹或项ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>选择文件夹的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
  </tr> 
   <td role="rowheader">[！UICONTROL字段]</td> 
   <td>对于要更新的每个元数据字段，单击<b>添加项</b>并输入该字段的路径和值。</td> 
  <tr>
</tbody> 
</table>

#### 监视文件夹项目

当您选择的文件夹中更新了某个项目时，此触发器模块会启动一个方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点、驱动器和文件夹ID]</td> 
   <td> <p>选择您希望如何标识要获取的文件位置。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在显示的字段中输入或映射<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL列表ID]</strong>和<strong>[！UICONTROL文件夹ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>选择要监视的文件夹的位置。 </p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td>输入Workfront Fusion应在一个方案执行周期内返回的最大项目数。</td> 
  <tr>
  </tr>
</tbody> 
</table>

### 项目

* [[!UICONTROL 复制项目]](#copy-an-item)
* [[!UICONTROL 创建项]](#create-an-item)
* [[!UICONTROL 删除项]](#delete-an-item)
* [[!UICONTROL 获取项目]](#get-an-item)
* [获取详细信息](#get-details)
* [[!UICONTROL 列表项]](#list-items)
* [[!UICONTROL 移动项]](#move-an-item)
* [[!UICONTROL 更新项]](#update-an-item)
* [[!UICONTROL 关注项目]（已计划）](#watch-items-scheduled)


#### [!UICONTROL 复制项目]

此操作模块复制SharePoint列表中的现有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">输入站点、驱动器和文件夹ID</td> 
   <td> <p>选择您要如何标识包含要复制项目的站点和驱动器。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要复制的项的<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL驱动器ID]</strong>和<strong>[！UICONTROL项ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>在“项目类型”字段中，选择要移动字段还是文件夹。  选择包含要复制项目的站点，然后选择列表，然后选择项目。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL目标ID]</td> 
   <td> 输入或映射要向其复制项目的文件夹的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL新名称]</td> 
   <td>输入或映射项目新副本的名称。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建项]

此操作模块在SharePoint列表中创建新项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL创建项目]</td> 
   <td> <p>选择您希望如何标识站点和要在其中创建项目的驱动器。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要在其中创建该项的<strong>[！UICONTROL站点ID]</strong>和<strong>[！UICONTROL列表ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要在其中创建项目的列表的站点，然后选择列表。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL字段]</td> 
   <td>对于要为新项设置的每个字段，单击<b>添加项</b>，然后输入字段的键（用于标识该字段）以及您希望新项对该字段具有的值。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除项]

此操作模块删除SharePoint列表中的现有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL更新项]</td> 
   <td> <p>选择您希望如何标识站点以及包含要删除项目的列表。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要删除的项目的<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL列表ID]</strong>和<strong>[！UICONTROL项目ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要删除项目的站点，然后选择列表，然后选择项目。 </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取项目]

此操作模块返回指定项的数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL获取项目]</td> 
   <td> <p>选择您希望如何标识站点以及包含您要获取项目的列表。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要为其返回数据的项的<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL列表ID]</strong>和<strong>[！UICONTROL项ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要从中检索项目的列表的站点，然后选择该列表，然后选择该项目。 </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取详细信息

此模块从指定的URL获取项目详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Web URL</td> 
   <td> 输入或映射要检索其详细信息的项目的URL。 </td> 
  </tr> 
</tbody> 
</table>

#### [!UICONTROL 列表项]

此操作模块检索指定列表中所有项目的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL列表项]</td> 
   <td> <p>选择您希望如何标识要从中检索项目的列表。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射<strong>[！UICONTROL站点ID]</strong>和<strong>[！UICONTROL列表ID]</strong>作为要为其列出项目的列表。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要从中检索项目的列表的站点，然后选择该列表。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大项目数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 移动项]

此操作模块复制SharePoint列表中的现有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">输入站点、驱动器和文件夹ID</td> 
   <td> <p>选择您希望如何标识站点以及包含要移动项目的列表。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>为要移动的项输入或映射<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL列表ID]</strong>和<strong>[！UICONTROL项ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>在“项目类型”字段中，选择要移动字段还是文件夹。 选择包含要复制项目的站点，然后选择列表，然后选择项目。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL目标ID]</td> 
   <td> 输入或映射要将项目移动到的文件夹的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL新名称]</td> 
   <td>输入或映射已移动项目的名称。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新项]

此操作模块更新SharePoint列表中的现有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL更新项]</td> 
   <td> <p>选择您要如何标识包含要更新的项目的站点和列表。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要更新的项的<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL列表ID]</strong>和<strong>[！UICONTROL项ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要更新的项目的站点，然后选择列表，然后选择项目。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL字段]</td> 
   <td>对于要为新项更新的每个字段，单击“添加项”<b></b>，然后输入字段的键（用于标识该字段）以及您希望该项为该字段提供的新值。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 关注项目]（已计划）

此触发器模块会在创建或修改项目时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL监视列表]</td> 
   <td>选择是要按创建时间（新项目）还是按修改时间（更新项目）监视列表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点和列表ID]</td> 
   <td> <p>选择您希望如何识别要监视的站点和列表。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要监视的<strong>[！UICONTROL站点ID]</strong>和<strong>[！UICONTROL列表ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>选择要监视的站点，然后选择列表。 这些下拉列表仅检索关注的网站。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大项目数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 列表

* [[!UICONTROL 创建列表]](#create-a-list)
* [[!UICONTROL 获取列表]](#get-a-list)
* [[!UICONTROL 列表列表]](#list-lists)
* [[!UICONTROL 观看列表]](#watch-lists)

#### [!UICONTROL 创建列表]

此操作模块可在SharePoint中创建新列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点ID]</td> 
   <td> <p>选择您希望如何标识要创建列表的站点。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要在其中创建列表的<strong>[！UICONTROL站点ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择要创建列表的站点。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示名称]</td> 
   <td>输入或映射新列表的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL描述]</td> 
   <td>输入或映射新列表的说明。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Add Columns]</td> 
   <td>对于要为新列表设置的每一列，单击<b>添加项</b>，为该字段输入<strong>[！UICONTROL名称]</strong>，然后选择希望新列具有的值<strong>[！UICONTROL类型]</strong>。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取列表]

此操作模块返回指定列表的数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL获取列表]</td> 
   <td> <p>选择您希望如何标识站点以及包含您要获取项目的列表。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要返回的<strong>[！UICONTROL站点ID]</strong>和<strong>列表ID</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要检索的列表的站点，然后选择该列表。 </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列表列表]

此操作模块检索指定站点中所有项目的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL列表列表]</td> 
   <td> <p>选择您希望如何标识要从其中检索列表的站点。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射包含要返回的列表的<strong>[！UICONTROL站点ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要检索的列表的站点。 下拉列表将仅检索您关注的站点。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大列表数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看列表]

此触发器模块会在创建或修改列表时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL监视列表]</td> 
   <td>选择是要按创建时间（新项目）还是按修改时间（更新项目）监视列表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点ID]</td> 
   <td> <p>选择您希望如何识别要监视列表的站点。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射要监视列表的<strong>[！UICONTROL站点ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>选择要监视的站点。 下拉列表只会检索您关注的站点。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大列表数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 页面(Beta)

>[!NOTE]
>
>`beta`中[!DNL Microsoft Graph]版本的API可能会发生更改。 不支持在生产应用程序中使用这些API。

* [获取页面](#get-a-page)
* [列表页面](#list-pages)
* [发布页面](#publish-a-page)
* [关注页面](#watch-pages)

#### [!UICONTROL 获取页面]

此操作模块返回指定页面的数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL获取页面]</td> 
   <td> <p>选择您希望如何标识要检索的页面。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射<strong>[！UICONTROL站点ID]</strong>和<strong>[！UICONTROL页面ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要检索的页面的站点，然后选择该页面。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 列表页面

此模块可检索所有页面的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL列表页面]</td> 
   <td> <p>选择您希望如何标识要列出的页面。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射包含要列出的页面的网站的<strong>[！UICONTROL网站ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要列出的页面的网站。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大页数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 发布页面

此操作模块发布所选页面的最新版本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL发布页面]</td> 
   <td> <p>选择您希望如何识别要发布的页面。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射<strong>[！UICONTROL站点ID]</strong>和<strong>[！UICONTROL页面ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要发布的页面的站点，然后选择该页面。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 关注页面

此触发器模块会在指定网站上修改页面时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点ID]</td> 
   <td> <p>选择您希望如何标识要列出的页面。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射包含要监视的页面的网站的<strong>[！UICONTROL网站ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从您关注的列表中选择]</strong> </p> <p>选择包含要监视的页面的网站。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大页数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 站点

* [[!UICONTROL 获取站点]](#get-a-site)
* [[!UICONTROL 搜索站点]](#search-sites)

#### [!UICONTROL 获取站点]

此操作模块返回指定站点的数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL获取站点]</td> 
   <td> <p>选择您希望如何标识要检索的页面。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射<strong>[！UICONTROL站点ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择要检索的站点。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索站点]

此操作模块按您指定的参数搜索站点。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">显示名称的[！UICONTROL关键字]</td> 
   <td> <p>输入或映射要搜索网站的搜索词。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
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
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入站点、驱动器和文件夹ID]</td> 
   <td> <p>选择您要如何标识包含要更新的项目的站点和驱动器。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在显示的字段中输入或映射<strong>[！UICONTROL站点ID]</strong>、<strong>[！UICONTROL驱动器ID]</strong>和<strong>[！UICONTROL文件夹ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要更新的项目的站点，然后选择驱动器，然后选择文件夹。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL令牌]</td> 
   <td> 该令牌可标识模块应从何时开始检索更改。  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 进行API调用]

此模块允许您执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Microsoft SharePoint Online帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Microsoft SharePoint Online连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL URL]</p> </td> 
   <td> <p>输入相对于<code>https://graph.microsoft.com</code>的路径。 示例：<code> /beta/sites</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL方法]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 例如：<code>{"Content-type":"application/json"}</code>。Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串]</td> 
   <td> <p> 以标准JSON对象的形式添加API调用的查询。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL类型]</td> 
   <td>选择您要在API调用中发送的数据类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
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
   <td> <p>For instructions about connecting your Microsoft SharePoint Online account to Workfront Fusion, see <a href="#connect-microsoft-sharepoint-online-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">Connect Microsoft SharePoint Online to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  -->
  <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td> <p>选择现有的webhook，或单击“添加”并输入连接以创建新的webhook。</p> 
   </td> 
  </tr> 
 </tbody> 
</table>
