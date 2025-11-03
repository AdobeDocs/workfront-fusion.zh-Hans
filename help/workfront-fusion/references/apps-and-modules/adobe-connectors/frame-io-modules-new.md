---
title: Frame.io (Beta)模块
description: ' [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] 帐户。'
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '3559'
ht-degree: 1%

---

# [!DNL Frame.io] V4模块

>[!IMPORTANT]
>
>本文介绍了新版本的Frame.io连接器。 此连接器用于连接到Frame.io版本4。
>
>有关旧版Frame.io连接器的说明，请参阅[Frame.io旧版连接器](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)。

通过Adobe Workfront Fusion [!DNL Frame.io]模块，您可以在[!DNL Frame.io]帐户中监视、创建、更新、检索或删除资源和评论。

Workfront提供了两个Frame.io连接器，它们基于您所连接的Frame.io版本。

| 连接器 | Frame.io版本 |
|---|---|
| Frame.io | V4 |
| Frame.io（旧版） | V3 |

有关旧版Frame.io连接器的说明，请参阅[Frame.io旧版连接器](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)。


有关Frame.io连接器的视频介绍，请参阅：

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

要使用[!DNL Frame.io]模块，您必须具有[!DNL Frame.io]帐户

## Frame.io API信息

Frame.io连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td> https://api.frame.io/v4</td> 
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

您可以使用用户凭据自动连接、手动创建用户凭据连接或创建服务器到服务器连接。

* [使用用户凭据自动连接](#connect-automatically-with-user-credentials#)
* [手动创建用户凭据连接](#create-a-user-credentials-connection-manually)
* [创建服务器到服务器连接](#create-a-server-to-server-connection)

### 使用用户凭据自动连接

如果您已登录到Frame.io，此方法会自动创建连接，或者将您连接到Frame.io登录页面，以便您能够登录。

1. 在任意Frame.io Beta模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。
1. 输入连接的名称。
1. 单击&#x200B;**继续**。
1. 如果系统提示您登录Frame.io帐户，请登录。
1. 如果您属于多个Frame.io组织，请选择要用于此连接的组织。

将创建连接。

### 手动创建用户凭据连接

您可以通过登录Frame.io或者提供客户端ID或客户端密钥来创建用户凭据连接。

要创建服务器到服务器连接，必须首先在Adobe Developer Console中配置应用程序。

* [在Adobe Developer Console中创建用户凭据](#create-user-credentials-in-the-adobe-developer-console)
* [配置用户身份验证连接](#configure-a-user-authentication-connection)

#### 在Adobe Developer Console中创建用户凭据

如果您在Adobe Developer Console项目中还没有服务器到服务器凭据，则可以创建这些凭据。

1. 打开[Adobe Developer Console](https://developer.adobe.com/)。
1. 在Adobe Developer Console中选择要用于此连接的现有项目

   或

   在Adobe Developer Console中创建新项目。 有关说明，请参阅[创建空项目](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty)。

1. 在项目概述页面或开始使用新项目页面上，单击&#x200B;**添加API**。
1. 在打开的页面上，找到并单击&#x200B;**Frame.io API**。
1. 在“选择身份验证类型”页面上，选择&#x200B;**用户身份验证**，然后单击&#x200B;**下一步**。
1. 在“添加用户身份验证凭据”页面上，选择&#x200B;**OAuth Web App**，然后单击&#x200B;**下一步**。
1. 在配置OAuth Web应用程序凭据页面上，输入以下内容：   <table style="table-layout:auto">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL 默认重定向URI]</td>
          <td>
            <p><code>https://oauth.app.workfrontfusion.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 重定向URI模式]</td>
          <td>
            <p><code>https://oauth\.app\.workfrontfusion\.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
       </tbody>
    </table>
1. 单击&#x200B;**下一步**。
1. 单击&#x200B;**保存配置的API**。
1. 在产品页面上，单击您刚刚创建的凭据的卡。

   在这里，您可以找到您的客户端ID和客户端密钥。

>[!NOTE]
>
> 当您开始在Adobe Workfront Fusion中配置连接时，我们建议您保持此窗口处于打开状态。 您可以复制客户端ID，并在此页面中检索和复制客户端密钥，以粘贴到连接字段中。


#### 配置用户身份验证连接

1. 在任意Frame.io Beta模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。
1. 在“创建连接”框中，单击&#x200B;**显示高级设置**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL 连接类型]</td>
          <td>
            <p>选择<b>IMS用户身份验证</b>。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 连接名称]</td>
          <td>
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端ID]</td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端ID]。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。<p>有关创建凭据的说明，请参阅本文中的<a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">在Adobe Developer Console中创建用户凭据</a>。</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端密钥]</td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。<p>有关创建凭据的说明，请参阅本文中的<a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">在Adobe Developer Console中创建用户凭据</a>。</p>
        </tr>
       </tbody>
    </table>
1. 如果系统提示您登录Frame.io帐户，请登录。
1. 如果您属于多个Frame.io组织，请选择要用于此连接的组织。

将创建连接。


### 创建服务器到服务器连接

要创建服务器到服务器连接，必须首先在Adobe Developer Console中配置应用程序。

* [在Adobe Developer Console中创建服务器到服务器凭据](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [配置服务器到服务器连接](#configure-a-server-to-server-connection)

#### 在Adobe Developer Console中创建服务器到服务器凭据

如果您在Adobe Developer Console项目中还没有服务器到服务器凭据，则可以创建这些凭据。

1. 打开[Adobe Developer Console](https://developer.adobe.com/)。
1. 在Adobe Developer Console中选择要用于此连接的现有项目

   或

   在Adobe Developer Console中创建新项目。 有关说明，请参阅[创建空项目](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty)。

1. 在项目概述页面或开始使用新项目页面上，单击&#x200B;**添加API**。
1. 在打开的页面上，找到并单击&#x200B;**Frame.io API**。
1. 在“选择身份验证类型”页面上，选择&#x200B;**服务器到服务器身份验证**，然后单击&#x200B;**下一步**。
1. 输入凭据的名称。 这允许您稍后在Adobe Admin Console的API凭据区域中识别凭据。
1. 单击&#x200B;**下一步**。
1. 在选择产品配置文件页面上，选择包含要连接到的Frame.io帐户的产品配置文件。
1. 单击&#x200B;**保存配置的API**。
1. 在产品页面上，单击您刚刚创建的凭据的卡。

   在这里，您可以找到您的客户端ID和客户端密钥。

>[!NOTE]
>
> 当您开始在Adobe Workfront Fusion中配置连接时，我们建议您保持此窗口处于打开状态。 您可以复制客户端ID，并在此页面中检索和复制客户端密钥，以粘贴到连接字段中。


#### 配置服务器到服务器连接

1. 在任意Frame.io Beta模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL 连接类型]</td>
          <td>
            <p>选择<b>IMS服务器到服务器</b>。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 连接名称]</td>
          <td>
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端ID]</td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端ID]。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。<p>有关创建凭据的说明，请参阅本文中的<a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">在Adobe Developer Console中创建服务器到服务器凭据</a>。</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端密钥]</td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。<p>有关创建凭据的说明，请参阅本文中的<a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">在Adobe Developer Console中创建服务器到服务器凭据</a>。</p>
        </tr>
       </tbody>
    </table>
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。




## [!DNL Frame.io]模块及其字段

在配置[!DNL Frame.io]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Frame.io]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [资源](#assets)
* [评论](#comments)
* [文件夹](#folders)
* [项目](#projects)
* [共享](#shares)
* [Workspace](#workspaces)
* [其他](#other)

### 资源

* [[!UICONTROL 创建资产]](#create-an-asset)
* [[!UICONTROL 删除资产]](#delete-an-asset)
* [[!UICONTROL 获取资源]](#get-an-asset)
* [[!UICONTROL 列出资源]](#list-assets)
* [观看资源已删除](#watch-asset-deleted)
* [观看新资源](#watch-new-asset)

#### [!UICONTROL 创建资产] <!--different for v4-->

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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射包含要为其创建资源的项目的帐户的ID。</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>选择工作区或映射包含要为其创建资源的项目的工作区的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择项目或映射要为其创建资源的项目的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 路径] </td> 
   <td> <p>选择要创建资产的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件名] </td> 
   <td> <p>输入要用于此资源的文件的名称。</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">文件大小 </td> 
    <td> <p>输入或映射文件大小（字节）。</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL Source URL] </td> 
   <td> <p>如果创建文件，请输入要上载的文件的URL。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 媒体类型] </td> 
   <td> <p>为此资源选择媒体类型。</p> </td> 
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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射包含要删除的资产的帐户的ID。</p> </td> 
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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射包含要检索的资产的帐户的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>选择或映射要检索的资源。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出资源]

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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射包含要列出的资产的帐户的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大资产数] </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大资源数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 观看资源已删除

此触发器模块会在删除资产后启动方案。

选择要用于此模块的webhook，或单击Webhook字段旁边的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称] </td> 
   <td> <p>输入新webhook的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射您要监视已删除资产的帐户ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 观看新资源

此触发器模块会在创建新资产后启动方案。

选择要用于此模块的webhook，或单击Webhook字段旁边的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称] </td> 
   <td> <p>输入新webhook的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射要监视新资产的帐户的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 评论

* [[!UICONTROL 创建评论]](#create-a-comment)
* [[!UICONTROL 删除评论]](#delete-a-comment)
* [[!UICONTROL 获取评论]](#get-a-comment)
* [[!UICONTROL 列出评论]](#list-comments)
* [[!UICONTROL 更新评论]](#update-a-comment)
* [观看评论已更新](#watch-comment-updated)
* [观看新评论](#watch-new-comment)

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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射包含要向其添加评论的资源的帐户的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>选择帐户或映射包含要向其添加评论的资源的工作区的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择项目或映射项目ID，该项目包含要添加注释的资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 路径] </td> 
   <td> <p>选择要在其中添加评论的资源路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td> <p> 输入评论或回复的文本内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timestamp] </td> 
   <td> <p>在视频中输入评论应链接到的帧号。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 页] </td> 
   <td> <p>如果资源是PDF，请输入或映射评论应附加到的页面。</p> </td> 
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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射包含要删除的评论的帐户的ID。</p> </td> 
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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户，或映射包含要检索其详细信息的注释的帐户的ID。</p> </td> 
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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射包含要从中检索评论的资源的Account。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>选择或映射包含要从中检索注释的资源的工作区。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择包含要从中检索注释的资源的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 路径] </td> 
   <td> <p>选择指向要从中列出评论的资源的path。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大评论数] </td> 
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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射包含项目的帐户，该项目包含要更新评论的资产。</p> </td> 
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
  <tr> 
   <td role="rowheader">[!UICONTROL 页] </td> 
   <td> <p>如果资源是PDF，请输入或映射注释所附加到的页面。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 观看评论已更新

此触发器模块会在注释更新后启动方案。

选择要用于此模块的webhook，或单击Webhook字段旁边的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称] </td> 
   <td> <p>输入新webhook的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射要监视其更新注释的帐户的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 观看新评论

此触发器模块会在创建评论时启动方案。

选择要用于此模块的webhook，或单击Webhook字段旁边的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称] </td> 
   <td> <p>输入新webhook的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射要监视新评论的帐户的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 文件夹

#### 创建文件夹

此操作模块将在Frame.io中创建新文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射要在其中创建文件夹的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>选择或映射要在其中创建文件夹的工作区。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择要创建文件夹的位置。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 路径] </td> 
   <td> <p>选择要创建文件夹的路径。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">名称 </td> 
   <td> <p>输入或映射新文件夹的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 项目

* [创建项目](#create-a-project)
* [邀请用户加入Frame.io项目](#invite-users-to-frameio-project)
* [列出项目](#list-projects)

#### 创建项目

此操作模块在Frame.io中创建新项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射要在其中创建项目的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>选择或映射要在其中创建项目的工作区。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">名称 </td> 
   <td> <p>输入或映射新项目的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 邀请用户加入Frame.io项目

此操作模块邀请用户访问指定的Frame.io项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射包含要邀请用户加入的项目的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>选择或映射包含要邀请用户访问的项目的工作区。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">项目 ID </td> 
   <td> <p>选择或映射要邀请用户的项目。</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">用户 ID </td> 
   <td> <p>选择或映射要邀请其加入项目的用户。</p> </td> 
  </tr> 
 </tbody> 
</table>

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
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射包含要从中检索项目的资源的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>选择或映射包含要从中检索项目的资源的工作区。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大项目数] </td> 
   <td> <p>输入或映射最大项目数
   您希望模块在每个场景执行周期中返回。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 共享

* [将资产添加到共享链接](#add-an-asset-to-a-share-link)
* [创建共享链接](#create-a-share-link)

#### 将资产添加到共享链接

此操作模块会将资产添加到Frame.io中的共享链接。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射包含要将资产添加到的共享链接的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 共享链接ID] </td> 
   <td> <p>选择或映射要将资产添加到的共享链接。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 资产ID] </td> 
   <td> <p>输入或映射要添加到共享链接的资产ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 创建共享链接

此操作模块在Frame.io中创建一个新的共享链接。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射要在其中创建共享链接的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID] </td> 
   <td> <p>选择或映射要在其中创建共享链接的工作区。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目ID] </td> 
   <td> <p>选择或映射要在其中创建共享链接的项目。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">访问 </td> 
   <td> <p>选择此链接是具有公共访问权限还是受限制访问权限。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">资源 </td> 
   <td> <p>对于要添加到共享链接的每个资产，单击<b>添加项</b>并输入资产的ID。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">描述 </td> 
   <td> <p>输入或映射共享链接的描述。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">名称 </td> 
   <td> <p>输入或映射共享链接的到期日期。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">名称 </td> 
   <td> <p>输入或映射新共享链接的名称。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">名称 </td> 
   <td> <p>输入或映射共享链接的密码。</p> </td> 
  </tr> 
 </tbody> 
</table>

### Workspace

#### 创建 Workspace

此操作模块在Frame.io中创建新工作区

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射要在其中创建工作区的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 名称] </td> 
   <td> <p>输入或映射工作区的新名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 列出工作区

此模块列出了帐户中的所有工作区。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择或映射包含要从中检索工作区的资源的帐户。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 返回工作区的最大数目] </td> 
   <td> <p>输入或映射最大工作区数
   您希望模块在每个场景执行周期中返回。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

* [进行自定义API调用](#make-a-custom-api-call)
* [监视元数据值已更新](#watch-metadata-value-updated)


#### [!UICONTROL 进行自定义API调用]

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
   <td> <p>输入相对于<code>https://api.frame.io</code>的路径。 示例： <code> /v4/me</code></p> <p>注意：有关可用端点的列表，请参阅[!DNL Frame.io] API参考。</p> </td> 
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

#### 监视元数据值已更新

此触发器模块会在注释更新后启动方案。

选择要用于此模块的webhook，或单击Webhook字段旁边的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook名称] </td> 
   <td> <p>输入新webhook的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td> 
   <td>有关创建与[!DNL Frame.io]的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Frame.io]连接到Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户ID] </td> 
   <td> <p>选择帐户或映射要监视更新后元数据值的帐户的ID。</p> </td> 
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
