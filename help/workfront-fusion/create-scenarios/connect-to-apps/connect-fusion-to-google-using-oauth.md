---
title: 使用自定义OAuth客户端将Adobe Workfront Fusion连接到Google Services
description: 您可以使用Adobe Workfront Fusion通过自定义OAuth客户端连接到Google服务。 此过程需要现有的Google帐户。
author: Becky
feature: Workfront Fusion
exl-id: 2f0bc289-4ecf-4a31-9d7b-641bbca6fc95
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 1%

---

# 使用自定义OAuth客户端将Adobe Workfront Fusion连接到Google Services

您可以使用Adobe Workfront Fusion通过自定义OAuth客户端连接到Google服务。 此过程需要现有的Google帐户。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包 
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
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront计划：包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

您需要一个现有的Google帐户才能建立此连接。

## 使用自定义OAuth客户端将Fusion连接到Google服务

要创建此连接，必须在Google Cloud平台上创建和配置项目，然后根据该项目在Fusion中配置连接。

>[!NOTE]
>
>此过程适用于：
>
>* 个人使用（`@gmail.com`和`@googlemail.com`用户）
>* 内部使用(更喜欢使用自定义OAuth客户端的Google Workspace用户)

* [在Google Cloud Platform上创建项目](#create-a-project-on-google-cloud-platform)
* [配置OAuth同意设置](#configure-oauth-consent-settings)
* [创建OAuth凭据](#create-oauth-credentials)
* [连接到Workfront Fusion中的Google](#connect-to-google-in-workfront-fusion)

### 在Google Cloud Platform上创建项目

要在Google Cloud Platform中创建项目，请执行以下操作：

1. 开始在Google Cloud Platform上创建项目。

   有关说明，请参阅Google文档中的[创建Google云项目](https://developers.google.com/workspace/guides/create-project)。
1. 启用API时，必须启用Google驱动器API以及要使用的所有Google应用程序的API(例如Google Sheets API)。
1. 完成创建项目。
1. 继续阅读本文中的[配置OAuth同意设置](#configure-oauth-consent-settings)部分。

### 配置OAuth同意设置

1. 开始为项目配置OAuth

   有关说明，请参阅Google文档中的[配置OAuth同意屏幕并选择范围](https://developers.google.com/workspace/guides/configure-oauth-consent)。
1. 选择&#x200B;**外部**，然后单击&#x200B;**创建**。

   >[!NOTE]
   >
   >选择此选项时不会向您收取费用。 有关详细信息，请参阅Google关于验证要求例外的信息。

1. 按如下方式填写必填字段：

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>应用程序名称</p> </td> 
      <td> <p>输入请求同意的应用程序名称。</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>示例：</b></span></span>Adobe Workfront Fusion </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">用户支持电子邮件</td> 
      <td>输入电子邮件地址，以便用户在连接到此应用程序时能够就同意问题与您联系。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">电子邮件地址</td> 
      <td>输入一个或多个电子邮件地址，Google可使用这些地址通知您对项目所做的任何更改。</td> 
     </tr> 
    </tbody> 
   </table>

1. 在“授权域”下，单击&#x200B;**添加域**，然后输入`workfrontfusion.com`。
1. 添加以下范围：

   <table style="table-layout:auto">
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>服务/API</th> 
      <th>所需的范围</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td> <p>Gmail</p> </td> 
      <td> <p>https://mail.google.com/</p> <p>https://www.googleapis.com/auth/gmail.labels</p> <p>https://www.googleapis.com/auth/gmail.send</p> <p>https://www.googleapis.com/auth/gmail.readonly</p> <p>https://www.googleapis.com/auth/gmail.compose</p> <p>https://www.googleapis.com/auth/gmail.insert</p> <p>https://www.googleapis.com/auth/gmail.modify</p> <p>https://www.googleapis.com/auth/gmail.metadata</p> </td> 
     </tr> 
     <tr> 
      <td> <p>Google Drive</p> </td> 
      <td> <p>https://www.googleapis.com/auth/drive</p> <p>https://www.googleapis.com/auth/drive.readonly</p> </td> 
     </tr> 
    </tbody> 
   </table>

   您可能需要展开列表或转到列表的下一页以查看所有内容。

1. （可选）将任何测试用户添加到项目。
1. 检查信息是否准确，然后单击&#x200B;**返回仪表板**。

   >[!NOTE]
   >
   >您无需提交同意屏幕和Google验证申请。

1. 继续[创建OAuth凭据](#create-oauth-credentials)。

### 创建OAuth凭据

1. 开始创建OAuth客户端ID凭据。

   有关说明，请参阅Google文档中的[创建访问凭据](https://developers.google.com/workspace/guides/create-credentials)。

   >[!NOTE]
   >
   >如果这不是您启用的第一个API或服务(Gmail或Google Drive)，则无需创建新凭据。

1. 按如下方式填写必填字段：

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">应用程序类型</td> 
      <td> <p> Web应用程序</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">名称</td> 
      <td>Workfront Fusion </td> 
     </tr> 
    </tbody> 
   </table>

1. 在“授权的重定向URI”下，输入以下&#x200B;**一个**：

   * 对于Gmail或Google驱动器： `https://app.workfrontfusion.com/oauth/cb/google-restricted`

   * 对于其他Google应用： `https://app.workfrontfusion.com/oauth/cb/google`

1. 单击&#x200B;**创建**。

   此时将显示客户端ID和客户端密钥。

1. 将客户端ID和客户端密钥复制到安全位置。 您将使用它们在Workfront Fusion中进行连接。
1. 继续[连接到Workfront Fusion中的Google](#connect-to-google-in-workfront-fusion)。

### 连接到Workfront Fusion中的Google

创建与Google连接的过程有所不同，具体取决于您是使用Google服务(例如Google Sheets或Google Docs)中的模块，还是通过HTTP >创建OAuth2.0请求模块连接到Google。

* [在Google服务中连接到Google](#connect-to-google-in-a-google-service)
* [在HTTP >创建OAuth2.0请求模块中连接到Google](#connect-to-google-in-the-http--make-an-oauth20-request-module)

#### 在Google服务中连接到Google

1. 在Workfront Fusion中，找到需要创建连接的Google模块。
1. 单击&#x200B;**创建连接**，然后单击&#x200B;**显示高级设置**。
1. 填写连接名称、环境和类型字段（如果适用）。
1. 在相应的字段中输入您在[创建OAuth凭据](#create-oauth-credentials)中检索到的客户端ID和客户端密钥，然后单击&#x200B;**继续**。

1. 使用您的Google帐户登录。

   显示&#x200B;**此应用未验证**&#x200B;窗口。 请注意，窗口标题中提到的“应用程序”是您在上面创建的OAuth客户端。

1. 单击&#x200B;**高级**，然后单击&#x200B;**转到Workfront Fusion （不安全）**&#x200B;以允许使用您的自定义OAuth客户端进行访问。

1. 单击&#x200B;**允许**&#x200B;以授予Workfront Fusion权限。
1. 在出现的窗口中，再次单击&#x200B;**允许**&#x200B;以确认您的选择。

   使用自定义OAuth客户端与所需的Google服务建立了连接。

#### 在HTTP >创建OAuth2.0请求模块中连接到Google {#connect-to-google-in-the-http--make-an-oauth20-request-module}

有关在HTTP >创建OAuth2.0请求模块中连接到Google的说明，请参阅HTTP >创建OAuth 2.0请求模块一文中的[有关在HTTP中创建与Google的连接的说明](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module)。

## 可能的错误消息：[403未配置访问]

如果显示`403 Access Not Configured`错误消息，则必须在Google Cloud平台中启用相应的API。 要启用API，请按照本文中[在Google Cloud Platform上创建项目](#create-a-project-on-google-cloud-platform)部分中的步骤操作。
