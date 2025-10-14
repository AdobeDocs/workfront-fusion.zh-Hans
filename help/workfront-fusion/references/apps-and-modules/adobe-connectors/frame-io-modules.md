---
title: Frame.io（旧版）模块
description: ' [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] 帐户。'
author: Becky
feature: Workfront Fusion
exl-id: 121b145c-d04d-44b9-b673-ea2928e2346d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2661'
ht-degree: 0%

---

# [!DNL Frame.io]个旧模块

>[!IMPORTANT]
>
>本文介绍了旧版Frame.io连接器。 此连接器用于连接到Frame.io版本3。
>
>有关Frame.io连接器的新（测试版）版本的说明，请参阅[Frame.io Beta连接器](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules-new.md)。

通过Adobe Workfront Fusion [!DNL Frame.io]模块，您可以在[!DNL Frame.io]帐户中监视、创建、更新、检索或删除资源和评论。

Workfront提供了两个Frame.io连接器，它们基于您所连接的Frame.io版本。

| 连接器 | Frame.io版本 |
|---|---|
| Frame.io (Beta) | V4 |
| Frame.io（旧版） | V3 |

有关Frame.io连接器的新（测试版）版本的说明，请参阅[Frame.io Beta连接器](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules-new.md)。

有关Frame.io连接器的视频介绍，请参阅：

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

要使用[!DNL Frame.io]模块，您必须具有[!DNL Frame.io]帐户

## Frame.io API信息

Frame.io连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td> https://api.frame.io/v2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Frame.io]连接到[!UICONTROL Adobe Workfront Fusion]

您可以使用API令牌或使用OAuth 2.0连接到[!DNL Frame.io]。

[使用API令牌连接到 [!DNL Frame.io] &#x200B;](#connect-to-frameio-using-an-api-token)

[使用OAuth 2.0 PKCE连接到 [!DNL Frame.io] &#x200B;](#connect-to-frameio-using-oauth-20-pkce)

### 使用API令牌连接到[!DNL Frame.io]

要使用API令牌将您的[!DNL Frame.io]帐户连接到Workfront Fusion，您必须在[!DNL Frame.io]帐户中创建API令牌，并将其插入到Workfront Fusion [!DNL Frame.io] [!UICONTROL 创建连接]对话框。

1. 登录到您的[!DNL Frame.io]帐户。
1. 转到&#x200B;**[!UICONTROL 开发人员中的]**&#x200B;令牌[!DNL Frame.io]页面。
1. 单击&#x200B;**[!UICONTROL 新建]**。
1. 输入令牌的名称，选择要使用的范围，然后单击&#x200B;**[!UICONTROL 创建]**。
1. 复制提供的令牌。
1. 转到Workfront Fusion并打开[!DNL Frame.io]模块的&#x200B;**[!UICONTROL 创建连接]**&#x200B;对话框。
1. 在&#x200B;**[!UICONTROL 连接类型]**&#x200B;字段中，选择&#x200B;**[!DNL Frame.io]**。
1. 输入您在步骤5中复制到&#x200B;**[!UICONTROL 您的[!DNL Frame.io] API密钥]**&#x200B;字段的令牌
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以建立连接并返回模块。

### 使用OAuth 2.0 PKCE连接到[!DNL Frame.io]

您可以使用带有可选客户端ID的OAuth 2.0 PKCE创建与[!DNL Frame.io]的连接。 如果要在连接中包含客户端ID，则必须在[!DNL Frame.io]帐户中创建OAuth 2.0应用程序。

* [使用OAuth 2.0 PKCE（不含客户端ID）连接到 [!DNL Frame.io] &#x200B;](#connect-to-frameio-using-using-oauth-20-pkce-without-client-id)
* [使用OAuth 2.0 PKCE（带有客户端ID）连接到 [!DNL Frame.io] &#x200B;](#connect-to-frameio-using-using-oauth-20-pkce-with-client-id)

#### 使用OAuth 2.0 PKCE（不带客户端ID）连接到[!DNL Frame.io]

1. 转到Workfront Fusion并打开[!DNL Frame.io]模块的&#x200B;**[!UICONTROL 创建连接]**&#x200B;对话框。
1. 在&#x200B;**[!UICONTROL 连接类型]**&#x200B;字段中，选择&#x200B;**[!UICONTROL [!DNL Frame.io]OAuth 2.0 PKCE]**。
1. 在&#x200B;**[!UICONTROL 连接名称]**&#x200B;字段中输入新连接的名称。
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以建立连接并返回模块。

#### 使用OAuth 2.0 PKCE（带客户端ID）连接到[!DNL Frame.io]

1. 在[!DNL Frame.io]中创建OAuth 2.0应用程序。 有关说明，请参阅有关[!DNL Frame.io]OAuth 2.0代码授权流[!UICONTROL 的]文档。

   >[!IMPORTANT]
   >
   >在[!DNL Frame.io]中创建OAuth 2.0应用程序时：
   >
   >* 输入以下内容作为重定向URI：
   >   
   >     * **美洲/APAC**： `https://app.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >     * **EMEA**： `https://app-eu.workfrontfusion.com/oauth/cb/frame-io5`
   >
   >* 启用PCKE选项。


1. 复制提供的`client_id`。
1. 转到Workfront Fusion并打开[!DNL Frame.io]模块的&#x200B;**[!UICONTROL 创建连接]**&#x200B;对话框。
1. 在&#x200B;**[!UICONTROL 连接类型]**&#x200B;字段中，选择&#x200B;**[!UICONTROL [!DNL Frame.io]OAuth 2.0 PKCE]**。
1. 在&#x200B;**[!UICONTROL 连接名称]**&#x200B;字段中输入新连接的名称。
1. 单击&#x200B;**[!UICONTROL 显示高级设置]**。
1. 输入您在步骤2中复制到`client_id`客户端ID **[!UICONTROL 字段的]**。
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以建立连接并返回模块。

## [!DNL Frame.io]模块及其字段

在配置[!DNL Frame.io]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Frame.io]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [资源](#assets)
* [评论](#comments)
* [项目](#projects)
* [其他](#other)

### 资源

* [[!UICONTROL 创建资产]](#create-an-asset)
* [[!UICONTROL 删除资产]](#delete-an-asset)
* [[!UICONTROL 获取资源]](#get-an-asset)
* [[!UICONTROL 列出Assets]](#list-assets)
* [[!UICONTROL 更新资产]](#update-an-asset)
* [[!UICONTROL 观看资源已删除]](#watch-asset-deleted)
* [[!UICONTROL 监视资产标签已更新]](#watch-asset-label-updated)
* [[!UICONTROL 观看新资源]](#watch-new-asset)

#### [!UICONTROL 创建资产]

此操作模块将创建新资源。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射拥有要为其创建资源的项目的团队。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择项目或映射要为其创建资源的项目的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID] </td> 
   <td> <p>选择文件夹或映射要在其中创建资产的文件夹的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 类型] </td> 
   <td> <p>选择创建文件夹还是文件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 名称] </td> 
   <td> <p>输入新文件或文件夹的名称。</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">File Type </td> 
    <td> <p>Select the type of file you want to upload.</p> </td> 
   </tr>
  --> <!--
   <tr> 
    <td role="rowheader">File Size </td> 
    <td> <p>The file size in bytes.</p> </td> 
   </tr>
  --> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>如果创建文件，请输入要上载的文件的URL。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 描述] </td> 
   <td> <p>如果创建文件，请输入资源的简短说明。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标签] </td> 
   <td> <p>如果创建文件，请选择文件是正在进行、需要审核还是已批准。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除资产]

此操作模块删除指定的资产。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射拥有包含要删除的资产项目的团队。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID]</td> 
   <td> <p> 选择包含要删除的资产的项目或。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID] </td> 
   <td> <p>选择包含要删除的资源的文件夹</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>选择或映射要删除的资源。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取资源]

此操作模块可检索资产详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射拥有项目的团队，该项目包含要检索其详细信息的资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID]</td> 
   <td> <p> 选择包含要检索其详细信息的资源的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID] </td> 
   <td> <p>选择包含要检索其详细信息的资源的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>选择资源或映射要检索其详细信息的资源的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出Assets]

此搜索模块可检索指定项目文件夹中的所有资产。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射拥有项目的团队，该项目包含要从中检索资产的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID]</td> 
   <td> <p> 选择包含要从中检索资源的文件夹的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID] </td> 
   <td> <p>选择要从中列出资产的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新资产]

使用此操作模块，可更新现有资源的名称、描述或自定义字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射拥有要为其更新资产的项目的团队。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择项目或映射要为其更新资源的项目的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID] </td> 
   <td> <p>选择文件夹或映射要更新其中资产的文件夹的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>输入或映射要更新的资源的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 名称] </td> 
   <td> <p>输入更新文件的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 描述] </td> 
   <td> <p>输入已更新资源的简短说明。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看资源已删除]

此触发器模块在删除属于指定团队的资源时启动方案。

由于这是一个即时触发器，因此您必须为要使用的模块选择或创建webhook。

如果添加webhook，请输入以下信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称]</td> 
   <td> <p> 输入webhook的名称，如“已删除资产”。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择为此webhook创建的团队。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 监视资产标签已更新]

此触发器模块会在指定团队集所拥有的资产的标签被更改、更改或删除时启动一个方案。

由于这是一个即时触发器，因此您必须为要使用的模块选择或创建webhook。

如果添加webhook，请输入以下信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称]</td> 
   <td> <p> 输入webhook的名称，如“资产状态已更新”。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择为此webhook创建的团队。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看新资源]

在为指定团队创建新资产时，此触发器模块会启动一个方案。

由于这是一个即时触发器，因此您必须为要使用的模块选择或创建webhook。

如果添加webhook，请输入以下信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称]</td> 
   <td> <p> 输入webhook的名称，如“创建的资产”。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择为此webhook创建的团队。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 评论

* [[!UICONTROL 创建评论]](#create-a-comment)
* [[!UICONTROL 删除评论]](#delete-a-comment)
* [[!UICONTROL 获取评论]](#get-a-comment)
* [[!UICONTROL 列出评论]](#list-comments)
* [[!UICONTROL 更新评论]](#update-a-comment)
* [[!UICONTROL 观看评论已更新]](#watch-comment-updated)
* [[!UICONTROL 观看新评论]](#watch-new-comment)

#### [!UICONTROL 创建评论]

此操作模块向资源添加新评论或回复。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 类型] </td> 
   <td> <p>选择是要创建注释还是要回复注释。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射拥有项目的团队，该项目包含要添加注释的资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择项目或映射项目ID，该项目包含要添加注释的资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID] </td> 
   <td> <p>选择文件夹，或映射包含要添加注释的资源的文件夹的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>选择或映射要将评论添加到的资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 注释ID] </td> 
   <td> <p>选择或映射您要添加回复的注释。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> 输入评论或回复的文本内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>在视频中输入评论应链接到的帧号。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除评论]

此操作模块删除现有评论。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID]</td> 
   <td> <p> 选择或映射拥有项目的团队，该项目包含您要从中删除评论的资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID]</td> 
   <td> <p> 选择项目或映射项目ID，该项目包含您要从中删除评论的资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID]</td> 
   <td> <p> 选择包含要删除评论的资源的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>输入或映射包含要删除的评论的资源ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 注释ID] </td> 
   <td> <p>输入或映射要删除的评论的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取评论]

此操作模块检索指定注释的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射拥有项目的团队，该项目包含要从中检索资产的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择包含要从中检索资源的文件夹的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID] </td> 
   <td> <p>选择要从中列出资产的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>选择包含要检索的注释的资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 注释ID] </td> 
   <td> <p>选择要检索其详细信息的注释。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出评论]

此搜索模块检索指定资源的所有注释。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射拥有项目的团队，该项目包含要从中检索注释的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择包含要从中检索注释的文件夹的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID] </td> 
   <td> <p>选择包含要从中列出注释的资源文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>选择要为其列出注释的资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大注释数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新评论]

此操作模块编辑现有评论。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射拥有项目的团队，该项目包含要更新评论的资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择包含要更新评论的资源的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹ID] </td> 
   <td> <p>选择包含要更新评论的资源的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>选择要更新评论的资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 注释ID] </td> 
   <td> <p>选择要更新的注释。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> 输入注释的文本内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>在评论链接到的视频中输入帧号。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看评论已更新]

此触发器模块在编辑评论时启动方案。

由于这是一个即时触发器，因此您必须为要使用的模块选择或创建webhook。

如果添加webhook，请输入以下信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称] </td> 
   <td> <p>输入webhook的名称，例如“编辑的注释”。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择为此webhook创建的团队。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看新评论]

此触发器模块会在创建新评论或回复时启动方案。

由于这是一个即时触发器，因此您必须为要使用的模块选择或创建webhook。

如果添加webhook，请输入以下信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称] </td> 
   <td> <p>输入webhook的名称，例如新建注释。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择为此webhook创建的团队。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 项目

#### [!UICONTROL 列出项目]

此搜索模块检索指定团队的所有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 团队ID] </td> 
   <td> <p>选择或映射要为其检索项目的团队。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大项目数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

#### [!UICONTROL 进行API调用]

此模块允许您执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>输入相对于<code>https://api.frame.io</code>的路径。 示例： <code> /v2/teams</code></p> <p>注意：有关可用端点的列表，请参阅[!DNL Frame.io] API参考。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 方法]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串] </td> 
   <td> <p>输入请求查询字符串。 对于要包含在查询字符串中的每个参数，单击<b>[!UICONTROL 添加项]</b>并输入字段名称和所需值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


<!-- 
**Example:** The following API call returns all teams and its details in your [!DNL Frame.io] account:

URL: `/v2/teams`

Method: `GET`

![API call example](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

The result can be found in the module's Output under Bundle > Body.

In our example, the details of 1 team were returned:

![API call output](/help/workfront-fusion/references/apps-and-modules/assets/api-call-output.png)

-->
