---
title: Frame.io 模块
description: ' [!DNL Adobe Workfront Fusion Frame].io modules enable you to monitor, create, update, retrieve, or delete assets and comments in your [!DNL Frame.io] 帐户。'
author: Becky
feature: Workfront Fusion
exl-id: 16d32ebd-1807-495e-8aaf-27346056ec71
source-git-commit: 3cb613c11500dfc94774783ee0b38e6f1768de20
workflow-type: tm+mt
source-wordcount: '4539'
ht-degree: 85%

---

# [!DNL Frame.io] V4 模块

>[!IMPORTANT]
>
>本文介绍新版 Frame.io 连接器。此连接器用于连接到 Frame.io 版本 4。
>
>有关旧版 Frame.io 连接器的使用说明，请参阅 [Frame.io 旧版连接器](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)。

Adobe Workfront Fusion 的 [!DNL Frame.io] 模块可用于在您的 [!DNL Frame.io] 帐户中监控、创建、更新、检索或删除资源和评论。

根据您要连接的 Frame.io 版本，Workfront 提供两个不同的 Frame.io 连接器。

| 连接器 | Frame.io 版本 |
|---|---|
| Frame.io | V4 |
| Frame.io（旧版） | V3 |

有关旧版 Frame.io 连接器的使用说明，请参阅 [Frame.io 旧版连接器](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/frame-io-modules.md)。


有关 Frame.io 连接器的视频介绍，请参阅：

* [Frame.io](https://video.tv.adobe.com/v/3427032/){target=_blank}

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

要使用 [!DNL Frame.io] 模块，您必须拥有一个 [!DNL Frame.io] 帐户

## Frame.io API 信息

Frame.io 连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td> https://api.frame.io/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 版本</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.0.76</td> 
  </tr>
 </tbody> 
 </table>

## 将 [!DNL Frame.io] 连接到 [!UICONTROL Adobe Workfront Fusion]

您可以通过用户凭据自动连接、手动创建用户凭据连接，或创建服务器到服务器的连接。

* [使用用户凭据自动连接](#connect-automatically-with-user-credentials#)
* [手动创建用户凭据连接](#create-a-user-credentials-connection-manually)
* [创建服务器到服务器连接](#create-a-server-to-server-connection)

### 使用用户凭据自动连接

如果您已登录 Frame.io，此方法将自动创建连接；如果未登录，则会跳转至 Frame.io 登录页面以便您登录。

1. 在任意 Frame.io 模块中，点击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。
1. 输入连接名称。
1. 单击&#x200B;**继续**。
1. 如果系统提示您登录 Frame.io 帐户，请完成登录。
1. 如果您属于多个 Frame.io 组织，请选择要用于此次连接的组织。

连接已创建。

### 手动创建用户凭据连接

您可以通过登录 Frame.io，或提供客户端 ID 与客户端密钥来创建用户凭据连接。

若要创建服务器到服务器连接，必须先在 Adobe Developer Console 中配置一个应用程序。

* [在 Adobe Developer Console 中创建用户凭据](#create-user-credentials-in-the-adobe-developer-console)
* [配置用户身份验证连接](#configure-a-user-authentication-connection)

#### 在 Adobe Developer Console 中创建用户凭据

如果您的 Adobe Developer Console 项目中尚未包含服务器到服务器凭据，您可以创建新的凭据。

1. 打开 [Adobe Developer Console](https://developer.adobe.com/)。
1. 选择 Adobe Developer Console 中的现有项目以用于此连接。

   或

   在 Adobe Developer Console 中创建新项目。有关操作步骤，请参阅[创建空白项目](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty)。

1. 在“项目”概述页面或“开始使用”新项目页面，点击&#x200B;**添加 API**。
1. 在打开的页面中找到并点击 **Frame.io API**。
1. 在“选择”身份验证类型页面，选择&#x200B;**用户身份验证**，然后点击&#x200B;**下一步**。
1. 在“添加用户身份验证凭据”页面，选择 **OAuth Web App**，然后点击&#x200B;**下一步**。
1. 在“配置 OAuth Web App 凭据”页面，输入以下信息：   <table style="table-layout:auto">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL 默认重定向 URI]</td>
          <td>
            <p><code>https://oauth.app.workfrontfusion.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 重定向 URI 模式]</td>
          <td>
            <p><code>https://oauth\.app\.workfrontfusion\.com/oauth/cb/frame-io2</code></p>
          </td>
        </tr>
       </tbody>
    </table>
1. 单击&#x200B;**下一步**。
1. 单击&#x200B;**保存配置的 API**。
1. 在产品页面，点击刚创建的凭据卡片。

   您可以在此处找到您的客户端 ID 和客户端密钥。

>[!NOTE]
>
> 建议在开始在 Adobe Workfront Fusion 中配置连接时保持此窗口打开。您可以从此页面复制客户端 ID，并获取并复制客户端密钥，然后粘贴到连接字段中。


#### 配置用户身份验证连接

1. 在任意 Frame.io 模块中，点击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。
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
            <p>选择 <b>IMS 用户身份验证</b>。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 连接名称]</td>
          <td>
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端 ID]</td>
          <td>输入您的 [!DNL Adobe] [!UICONTROL 客户端 ID]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。<p>有关创建凭据的说明，请参阅本文中的<a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">在 Adobe Developer Console 中创建用户凭据</a>。</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端密钥]</td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。<p>有关创建凭据的说明，请参阅本文中的<a href="#create-user-credentials-in-the-adobe-developer-console" class="MCXref xref">在 Adobe Developer Console 中创建用户凭据</a>。</p>
        </tr>
       </tbody>
    </table>
1. 如果系统提示您登录 Frame.io 帐户，请完成登录。
1. 如果您属于多个 Frame.io 组织，请选择要用于此次连接的组织。

连接已创建。


### 创建服务器到服务器连接

若要创建服务器到服务器连接，必须先在 Adobe Developer Console 中配置一个应用程序。

* [在 Adobe Developer Console 中创建服务器到服务器凭据](#create-server-to-server-credentials-in-the-adobe-developer-console)
* [配置服务器到服务器连接](#configure-a-server-to-server-connection)

#### 在 Adobe Developer Console 中创建服务器到服务器凭据

如果您的 Adobe Developer Console 项目中尚未包含服务器到服务器凭据，您可以创建新的凭据。

1. 打开 [Adobe Developer Console](https://developer.adobe.com/)。
1. 选择 Adobe Developer Console 中的现有项目以用于此连接。

   或

   在 Adobe Developer Console 中创建新项目。有关操作步骤，请参阅[创建空白项目](https://developer.adobe.com/developer-console/docs/guides/projects/projects-empty)。

1. 在“项目”概述页面或“开始使用”新项目页面，点击&#x200B;**添加 API**。
1. 在打开的页面中找到并点击 **Frame.io API**。
1. 在“选择身份验证类型”页面，选择&#x200B;**服务器到服务器身份验证**，然后点击&#x200B;**下一步**。
1. 输入此凭据的名称。此名称将用于在 Adobe Admin Console 的 API 凭据区域中识别该凭据。
1. 单击&#x200B;**下一步**。
1. 在“选择产品轮廓”页面，选择包含您要连接的 Frame.io 帐户的产品轮廓。
1. 单击&#x200B;**保存配置的 API**。
1. 在产品页面，点击刚创建的凭据卡片。

   您可以在此处找到您的客户端 ID 和客户端密钥。

>[!NOTE]
>
> 建议在开始在 Adobe Workfront Fusion 中配置连接时保持此窗口打开。您可以从此页面复制客户端 ID，并获取并复制客户端密钥，然后粘贴到连接字段中。


#### 配置服务器到服务器连接

1. 在任意 Frame.io 模块中，点击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

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
            <p>选择 <b>IMS 服务器到服务器</b>。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 连接名称]</td>
          <td>
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端 ID]</td>
          <td>输入您的 [!DNL Adobe] [!UICONTROL 客户端 ID]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。<p>有关创建凭据的说明，请参阅本文中的<a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">在 Adobe Developer Console 中创建服务器到服务器凭据</a>。</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端密钥]</td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。<p>有关创建凭据的说明，请参阅本文中的<a href="#create-server-to-server-credentials-in-the-adobe-developer-console" class="MCXref xref">在 Adobe Developer Console 中创建服务器到服务器凭据</a>。</p>
        </tr>
       </tbody>
    </table>
1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。




## [!DNL Frame.io] 模块及其字段

在您配置 [!DNL Frame.io] 模块时，Workfront Fusion 会显示以下字段。除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Frame.io] 字段。模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [资源](#assets)
* [评论](#comments)
* [文件夹](#folders)
* [项目](#projects)
* [共享](#shares)
* [工作区](#workspaces)
* [元数据](#metadata)
* [其他](#other)

### 资源

* [[!UICONTROL 创建资源]](#create-an-asset)
* [[!UICONTROL 删除资源]](#delete-an-asset)
* [[!UICONTROL 获取资源]](#get-an-asset)
* [[!UICONTROL 列出资源]](#list-assets)
* [监控已删除的资源](#watch-asset-deleted)
* [监控新资源](#watch-new-asset)

#### [!UICONTROL 创建资源] <!--different for v4-->

此操作模块将创建新资源。 您可以上传本地文件，也可以提供从中创建资产的远程文件的URL。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择包含要创建资源的项目的帐户，或映射该帐户 ID。</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择包含要创建资源的项目的工作区，或映射该工作区 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目 ID] </td> 
   <td> <p>选择您要在其中创建资源的项目，或映射该项目 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 路径] </td> 
   <td> <p>选择要创建资源的路径。</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL File Name] </td> 
   <td> <p>Enter the name of the file that you want to use for this asset.</p> </td> 
  </tr> -->
    <tr> 
    <td role="rowheader">上传类型 </td> 
    <td> <p>选择是从本地文件还是从远程生命周期创建资产。</p> </td> 
   </tr>
    <tr> 
    <td role="rowheader">文件大小 </td> 
    <td> <p>如果要上载本地文件，请输入或映射文件大小（以字节为单位）。</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL 源 URL] </td> 
   <td> <p>如果从远程文件创建资产，请输入要上传的文件的URL。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称。</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">[!UICONTROL Media type] </td> 
   <td> <p>Select the media type for this asset.</p> </td> 
  </tr> -->
  </tbody> 
</table>

#### [!UICONTROL 创建资产（旧版）] <!--different for v4-->

此操作模块用于创建新资源。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择包含要创建资源的项目的帐户，或映射该帐户 ID。</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择包含要创建资源的项目的工作区，或映射该工作区 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目 ID] </td> 
   <td> <p>选择您要在其中创建资源的项目，或映射该项目 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 路径] </td> 
   <td> <p>选择要创建资源的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件名] </td> 
   <td> <p>输入要用于此资源的文件的名称。</p> </td> 
  </tr>
    <tr> 
    <td role="rowheader">文件大小 </td> 
    <td> <p>输入或映射文件大小（以字节为单位）。</p> </td> 
   </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL 源 URL] </td> 
   <td> <p>如果要创建文件，请输入您要上传的文件 URL。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 媒体类型] </td> 
   <td> <p>选择此资源的媒体类型。</p> </td> 
  </tr> 
  </tbody> 
</table>

#### [!UICONTROL 删除资源]

此操作模块用于删除指定资源。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择包含要删除资源的帐户，或映射该帐户 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资源 ID] </td> 
   <td> <p>选择或映射您要删除的资源。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取资源]

此操作模块用于检索资源详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择包含要检索的资源的帐户，或映射该帐户 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 资源 ID] </td> 
   <td> <p>选择或映射您要检索的资源。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出资源]

此搜索模块会检索指定项目文件夹中的所有资源。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择包含要列出的资源的帐户，或映射该帐户 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回资源的最大数量] </td> 
   <td> <p>输入或映射该模块在每次场景执行周期内应返回的资源最大数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 监控已删除的资源

当删除资源时，此触发器模块会启动一个场景。

选择要用于此模块的 Webhook，或点击 Webhook 字段旁的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook 名称] </td> 
   <td> <p>输入新 Webhook 的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射您希望关注其资源删除事件的帐户 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 监控新资源

当创建新资源时，此触发器模块会启动一个场景。

选择要用于此模块的 Webhook，或点击 Webhook 字段旁的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook 名称] </td> 
   <td> <p>输入新 Webhook 的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射您希望关注其新资源创建事件的帐户 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 评论

* [[!UICONTROL 创建评论]](#create-a-comment)
* [[!UICONTROL 删除评论]](#delete-a-comment)
* [[!UICONTROL 获取评论]](#get-a-comment)
* [[!UICONTROL 列出评论]](#list-comments)
* [[!UICONTROL 更新评论]](#update-a-comment)
* [监控更新的评论](#watch-comment-updated)
* [监控新评论](#watch-new-comment)

#### [!UICONTROL 创建评论]

此操作模块会向资源添加新的评论或回复。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择包含要添加评论的资源的帐户，或映射该帐户 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择包含要添加评论的资源的帐户，或映射该工作区的 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目 ID] </td> 
   <td> <p>选择包含要添加评论的资源的项目，或映射该项目的 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 路径] </td> 
   <td> <p>选择您想要添加评论的资源路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文本]</td> 
   <td> <p> 输入评论或回复的文本内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 时间戳] </td> 
   <td> <p>输入该评论在视频中所对应的帧编号。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 页面] </td> 
   <td> <p>如果资源为 PDF，请输入或映射评论应附加到的页面编号。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除评论]

此操作模块用于删除现有评论。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择包含要删除评论的帐户，或映射该帐户 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 评论 ID] </td> 
   <td> <p>输入或映射您要删除的评论 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取评论]

此操作模块用于检索指定评论的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择包含您要检索详细信息的评论所在帐户，或映射该帐户 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 评论 ID] </td> 
   <td> <p>选择您要检索详细信息的评论。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出评论]

此搜索模块会检索指定资源的所有评论。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射包含您想要检索评论的资源的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择或映射包含您想要检索评论的资源的工作区。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目 ID] </td> 
   <td> <p>选择包含您想要检索评论的资源的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 路径] </td> 
   <td> <p>选择指向要列出评论的资源的路径。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 返回评论的最大数量] </td> 
   <td> <p>输入或映射该模块在每次场景执行周期内应返回的评论最大数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新评论]

此操作模块用于编辑现有评论。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射包含该项目的帐户，该项目中包含要更新评论的资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 评论 ID] </td> 
   <td> <p>选择要更新的评论。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文本]</td> 
   <td> <p> 输入评论的文本内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 时间戳] </td> 
   <td> <p>输入该评论在视频中对应的帧编号。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 页面] </td> 
   <td> <p>如果资源为 PDF，请输入或映射评论所在的页面编号。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 监控更新的评论

当更新评论时，此触发器模块会启动一个场景。

选择要用于此模块的 Webhook，或点击 Webhook 字段旁的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook 名称] </td> 
   <td> <p>输入新 Webhook 的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择您想要关注更新评论的帐户，或映射该帐户的 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 监控新评论

当创建评论时，此触发器模块会启动一个场景。

选择要用于此模块的 Webhook，或点击 Webhook 字段旁的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook 名称] </td> 
   <td> <p>输入新 Webhook 的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射您希望关注其新评论的帐户 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 文件夹

#### 创建文件夹

此操作模块会在 Frame.io 中创建一个新文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射您希望创建文件夹的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择或映射您希望创建文件夹的工作区。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目 ID] </td> 
   <td> <p>选择您希望创建文件夹的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 路径] </td> 
   <td> <p>选择您希望创建文件夹的路径。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">名称 </td> 
   <td> <p>输入或映射新文件夹的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 项目

* [创建项目](#create-a-project)
* [邀请用户加入 Frame.io 项目](#invite-users-to-frameio-project)
* [列出项目 &#x200B;](#list-projects)

#### 创建项目

此操作模块会在 Frame.io 中创建一个新项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射您希望创建项目的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择或映射您希望创建项目的工作区。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">名称 </td> 
   <td> <p>输入或映射新项目的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 邀请用户加入 Frame.io 项目

此操作模块会将用户邀请至指定的 Frame.io 项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射包含要邀请用户加入的项目的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择或映射包含要邀请用户访问的项目的工作区。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">项目 ID </td> 
   <td> <p>选择或映射您希望邀请用户加入的项目。</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">用户 ID </td> 
   <td> <p>选择或映射您希望邀请加入该项目的用户。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出项目 &#x200B;]

此搜索模块会检索指定团队的所有项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射包含您想要检索项目的资源的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择或映射包含您想要检索项目的资源的工作区。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 返回项目的最大数量] </td> 
   <td> <p>输入或映射模块在每次场景执行周期中应返回的最大项目数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 共享

* [将资源添加到共享链接](#add-an-asset-to-a-share-link)
* [创建共享链接](#create-a-share-link)

#### 将资源添加到共享链接

此操作模块会将资源添加到 Frame.io 中的共享链接。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射包含您想要向其添加资源的共享链接的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 共享链接 ID] </td> 
   <td> <p>选择或映射您希望添加资源的共享链接。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 资源 ID] </td> 
   <td> <p>输入或映射您要添加至共享链接的资源 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 创建共享链接

此操作模块会在 Frame.io 中创建一个新的共享链接。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射您希望创建共享链接的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择或映射您希望创建共享链接的工作区。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目 ID] </td> 
   <td> <p>选择或映射您希望创建共享链接的项目。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">访问 </td> 
   <td> <p>选择共享链接的访问权限为公开或受限。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">资源 </td> 
   <td> <p>对于每一个要添加到共享链接的资源，点击<b>添加项目</b>并输入该资源的 ID。</p> </td> 
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
   <td> <p>输入或映射共享链接的密码短语。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 工作区

#### 创建工作区

此操作模块会在 Frame.io 中创建一个新工作区。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射您希望创建工作区的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 名称] </td> 
   <td> <p>输入或映射工作区的新名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 列出工作区

此模块会列出帐户中的所有工作区。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射包含您想要检索工作区的资源的帐户。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 返回工作区的最大数量] </td> 
   <td> <p>输入或映射模块在每次场景执行周期中应返回的工作区最大数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 元数据

* [创建帐户级别字段](#create-an-account-level-field)
* [删除帐户级别字段](#delete-an-account-level-field)
* [获取元数据](#get-metadata)
* [列出帐户级别字段](#list-account-level-fields)
* [更新帐户级别字段定义](#update-an-account-level-field-definition)
* [跨多个文件更新元数据](#update-metadata-across-multiple-files)

#### 创建帐户级别字段

此操作模块会创建并配置新的帐户级别元数据字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射要在其中创建元数据的帐户。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">字段类型 </td> 
   <td> <p>选择要创建的元数据字段类型，然后配置该字段的选项。</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">名称 </td> 
   <td> <p>输入或映射新字段的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 删除帐户级别字段

此操作模块会删除单个帐户级别的元数据字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射包含要删除的元数据字段的帐户。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">字段定义Id </td> 
   <td> <p>输入或映射要删除的字段的ID。 您可以使用列表帐户级别字段模块查找字段ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取元数据

此操作模块检索Frame.io中文件的元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射包含要检索元数据的文件的帐户。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">文件Id </td> 
   <td> <p>输入或映射要为其检索元数据的文件的ID。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">显示null </td> 
   <td> <p>启用此选项以在输出中包含值为null的字段。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 列出帐户级别字段

此模块检索指定帐户的帐户级别元数据字段列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射要从中列出字段的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大协议数]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大字段数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 更新帐户级别字段定义

此模块更新单个现有元数据字段的定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射要在其中创建元数据的帐户。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">字段定义Id </td> 
   <td> <p>输入或映射要更新的字段的ID。 您可以使用列表帐户级别字段模块查找字段ID。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">字段类型 </td> 
   <td> <p>如果要更改字段的字段类型，请选择要创建的元数据字段类型，然后配置该字段的选项。</p> </td> 
  </tr> 
  </tr> 
   <tr> 
   <td role="rowheader">名称 </td> 
   <td> <p>输入或映射字段的新名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 跨多个文件更新元数据

此模块使用您指定的值更新一个或多个文件上的元数据字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择或映射包含要为其更新元数据的文件的帐户。</p> </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL 工作区 ID] </td> 
   <td> <p>选择包含要创建资源的项目的工作区，或映射该工作区 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目 ID] </td> 
   <td> <p>选择您要在其中创建资源的项目，或映射该项目 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件ID] </td> 
   <td> <p>对于每个要更新元数据的文件，单击<b>添加项</b>并输入或映射文件的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values] </td> 
   <td> <p>对于要更新元数据的每个字段，单击<b>添加项</b>，然后输入或映射字段定义的ID以及要放入该字段中的值。 在“文件ID”字段中指定的所有文件都将使用此字段值更新。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

* [发起自定义 API 调用](#make-a-custom-api-call)
* [观看活动](#watch-events)
* [监控更新的元数据值](#watch-metadata-value-updated)


#### [!UICONTROL 发起自定义 API 调用]

此模块允许您执行自定义 API 调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>输入相对于 <code>https://api.frame.io</code> 的路径。示例： <code> /v4/me</code></p> <p>注意：有关可用端点列表，请参阅 [!DNL Frame.io] API 参考文档。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 方法]</p> </td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion 会自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串] </td> 
   <td> <p>输入请求的查询字符串。对于向查询字符串中添加的每一个参数，点击<b>[!UICONTROL 添加项目]</b>并输入字段名称和对应的值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 正文]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 观看活动

此即时触发器模块会在Frame.io中发生选定事件时启动方案。

您可以使用现有的webhook，也可以创建一个新的webhook。

要创建新的 Webhook：

1. 单击 Webhook 字段旁边的&#x200B;**添加**。
1. 填写以下信息：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
     <td role="rowheader">Webhook名称 </td> 
      <td> <p>输入新 Webhook 的名称。</p> </td> 
     </tr> 
     <tr> 
       <td role="rowheader">[!UICONTROL 连接] </td> 
       <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
     </tr> 
     <tr> 
     <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
      <td> <p>选择或映射包含要监视事件的工作区的帐户。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 工作区 ID]</td> 
      <td> <p>输入要监视活动的工作区的ID。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 事件]</td> 
      <td> <p>选择要触发此模块的事件</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**保存**&#x200B;以保存webhook并返回模块。
1. 在“监视事件”模块中单击&#x200B;**确定**&#x200B;以保存配置。


#### 监控更新的元数据值

当更新评论时，此触发器模块会启动一个场景。

选择要用于此模块的 Webhook，或点击 Webhook 字段旁的“添加”并输入以下信息：

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook 名称] </td> 
   <td> <p>输入新 Webhook 的名称。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL 连接] </td> 
   <td>有关创建与 [!DNL Frame.io] 的连接的说明，请参阅本文中的<a href="#connect-frameio-to-adobe-workfront-fusion" class="MCXref xref">将 [!DNL Frame.io] 连接到 Adobe Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 帐户 ID] </td> 
   <td> <p>选择您想要关注元数据值更新的帐户，或映射该帐户的 ID。</p> </td> 
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
