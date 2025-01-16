---
title: HTTP &amp；gt；创建OAuth 2.0请求模块
description: 若要向需要OAuth 2.0授权的服务器发出 [!DNL Adobe Workfront Fusion] HTTP(S)请求，您首先需要创建OAuth连接。 [!DNL Adobe Workfront Fusion] 确保通过此连接进行的所有调用都具有适当的授权标头，并在需要时自动刷新关联的令牌。
author: Becky
feature: Workfront Fusion
exl-id: a302a1d4-fddf-4a71-adda-6b87ff7dba4b
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1918'
ht-degree: 0%

---

# [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]模块

>[!NOTE]
>
>除[!DNL Adobe Workfront]许可证外，[!DNL Adobe Workfront Fusion]还需要[!DNL Adobe Workfront Fusion]许可证。

要向需要OAuth 2.0授权的服务器发出[!DNL Adobe Workfront Fusion] HTTP(S)请求，您首先需要创建OAuth连接。 [!DNL Adobe Workfront Fusion]确保通过此连接进行的所有调用都具有适当的授权标头，并在需要时自动刷新关联的令牌。

[!DNL Workfront Fusion]支持以下OAuth 2.0身份验证流程：

* 授权代码流程
* 隐式流

其他流（如资源所有者密码凭据流和客户端凭据流）不自动支持通过此模块运行。

有关OAuth 2.0身份验证的更多信息，请参阅[OAuth 2.0授权框架](https://tools.ietf.org/html/rfc6749)。

>[!NOTE]
>
>如果您要连接到的Adobe产品当前没有专用连接器，我们建议您使用Adobe Authenticator模块。
>
>有关详细信息，请参阅[Adobe Authenticator模块](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md)。

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

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## 正在为[!DNL OAuth]请求创建连接

* [有关在HTTP >发出OAuth 2.0请求模块中创建连接的一般说明](#general-instructions-for-creating-a-connection-in-the-http--make-an-oauth-20-request-module)
* [有关在HTTP >[!UICONTROL Make] OAuth 2.0请求模块中创建与Google的连接的说明](#instructions-for-creating-a-connection-to-google-in-the-http-make-an-oauth-20-request-module)
* [有关通过HTTP >发出OAuth 2.0请求模块连接到Microsoft Graph API的说明](#instructions-for-connecting-to-microsoft-graph-api-via-the-http--make-an-oauth-20-request-module)

### 有关在[!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]模块中创建连接的一般说明

1. 在[!DNL target]服务中创建要[!DNL Adobe Workfront Fusion]与之通信的OAuth客户端。 此选项很可能在给定服务的[!UICONTROL Developer]部分中找到。

   1. 创建客户端时，在`[!UICONTROL Redirect URL]`或`[!UICONTROL Callback URL]`字段中输入相应的URL：

      | 美洲/APAC | `https://app.workfrontfusion.com/oauth/cb/oauth2` |
      |---|---|
      | EMEA | `https://app-eu.workfrontfusion.com/oauth/cb/oauth2` |

   1. 创建客户端后，给定服务显示2个密钥： `[!UICONTROL Client ID]`和`[!UICONTROL Client Secret]`。 某些服务调用这些`[!UICONTROL App Key]`和`[!UICONTROL App Secret]` 。 将密钥和秘密保存到安全位置，以便您可以在Workfront Fusion中创建连接时提供它们。

1. 在给定服务的API文档中查找`[!UICONTROL Authorize URI]`和`[!UICONTROL Token URI]`。 这些是[!DNL Workfront Fusion]与[!DNL target]服务通信的URL地址。 这些地址用于OAuth授权。

   >[!NOTE]
   >
   >如果服务使用隐式流，则您只需要`[!UICONTROL Authorize URI]`。

   >[!INFO]
   >
   >**示例：** Yahoo地址：
   >
   >* 授权URI：
   >
   >`https://api.login.yahoo.com/oauth2/request_auth`
   >
   >* 令牌URI：
   >
   >`https://api.login.yahoo.com/oauth2/get_token`

1. （视情况而定）如果目标服务使用作用域（访问权限），请检查服务如何分隔各个作用域，并确保在高级设置中相应地设置分隔符。 如果未正确设置分隔符，[!DNL Workfront Fusion]将无法创建连接，并且您会收到无效的范围错误。
1. 完成上述步骤后，即可开始在[!DNL Workfront Fusion]中创建OAuth连接。 将OAuth 2.0 HTTP(S)请求和响应处理模块添加到您的方案。
1. 在模块的“连接”字段中，单击&#x200B;**[!UICONTROL Add]**。

1. 填写以下字段以创建连接：

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>输入连接的名称。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>选择获取令牌的流程。</p> 
       <ul> 
        <li><strong>[!UICONTROL Authorization Code]</strong>：输入服务API文档中的<code>[!UICONTROL Authorize URI]</code>和<code>[!UICONTROL Token URI]</code>。</li> 
        <li><strong>[!UICONTROL Implicit]</strong>：输入服务API文档中的<code>[!UICONTROL Authorize URI]</code>。</li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>添加单个范围。 您可以在给定服务的开发人员(API)文档中找到此信息。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>选择上面输入的范围应该用分隔符。 您可以在给定服务的开发人员(API)文档中找到此信息。</p> <p>警告：如果未正确设置分隔符，[!DNL Workfront Fusion]将无法创建连接，并且您会收到无效的范围错误。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>输入客户端ID。 在要连接的服务中创建OAuth客户端时，您获得了客户端ID。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p> 输入客户端密码。 在要连接的服务中创建OAuth客户端时，您获得了客户端密钥。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p>添加要包含在授权调用中的任何参数。 以下标准参数始终自动包含在内，无需添加。</p> <p>标准参数：</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL response_type]</strong> </p> <p> <code>code </code>（对于[!UICONTROL Authorization Code flow]和<code>token </code>） [!UICONTROL Implicit flow]</p> </li> 
        <li> <p><strong>[!UICONTROL redirect_uri]</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">美洲/APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong> </p> <p> 创建帐户时收到的客户端ID</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Access token parameters]</p> </td> 
      <td> <p>添加要包含在令牌调用中的任何参数。 以下标准参数始终自动包含在内，无需添加。</p> <p>标准参数：</p> 
       <ul> 
        <li><strong>[!UICONTROL grant_type]</strong>： <code>authorization_code</code></li> 
        <li> <p><strong>[!UICONTROL redirect_uri]：</strong> </p> 
         <table style="table-layout:auto">  
          <col> 
          <col> 
          <tbody> 
           <tr> 
            <td role="rowheader">美洲/APAC</td> 
            <td>https://app.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
           <tr> 
            <td role="rowheader">EMEA </td> 
            <td>https://app-eu.workfrontfusion.com/oauth/cb/oauth2</td> 
           </tr> 
          </tbody> 
         </table> </li> 
        <li><strong>[!UICONTROL client_id]</strong>：创建帐户时收到的客户端ID会自动包含在请求正文中</li> 
        <li><strong>client_secret</strong>：您在创建帐户时收到的客户端密钥会自动包含在请求正文中</li> 
        <li><strong>代码</strong>：授权请求返回的代码</li> 
       </ul> <p>注意：  <p>OAuth 2.0标准在此步骤中支持至少2种客户端身份验证方法（<code>[!UICONTROL client_secret_basic]</code>和<code>[!UICONTROL client_secret_post]</code>）。 [!DNL Workfront Fusion]通过<code>[!UICONTROL client_secret_post]</code>方法自动发送指定的客户端ID和密码。 因此，这些参数会自动包含在令牌请求正文中。 </p> <p>有关OAuth 2.0身份验证的更多信息，请参阅<a href="https://tools.ietf.org/html/rfc6749">OAuth 2.0授权框架</a>。</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Refresh token parameters]</p> </td> 
      <td> <p>添加要包含在令牌调用中的任何参数。 以下标准参数始终自动包含在内，无需添加。</p> <p>标准参数：</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL grant_type]</strong>： <code>refresh_token</code></p> </li> 
        <li> <p><strong>[!UICONTROL refresh_token]</strong>：由您连接到的服务获取的最新刷新令牌</p> </li> 
        <li> <p><strong>[!UICONTROL client_id]</strong>：创建帐户时收到的客户端ID会自动包含在请求正文中</p> </li> 
        <li> <p><strong>[!UICONTROL client_secret]</strong>：您在创建帐户时收到的客户端密钥会自动包含在请求正文中</p> </li> 
       </ul> <p>注意：  <p>OAuth 2.0标准在此步骤中支持至少2种客户端身份验证方法（<code>[!UICONTROL client_secret_basic]</code>和<code>[!UICONTROL client_secret_post]</code>）。 [!DNL Workfront Fusion]通过<code>[!UICONTROL client_secret_post]</code>方法自动发送指定的客户端ID和密码。 因此，这些参数会自动包含在令牌请求正文中。 </p> <p>有关OAuth 2.0身份验证的更多信息，请参阅<a href="https://tools.ietf.org/html/rfc6749">OAuth 2.0授权框架</a>。</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Custom Headers]</p> </td> 
      <td> <p>指定要包含在[!UICONTROL Token]和R[!UICONTROL efresh Token]步骤的标头中的任何其他键和值。</p> <p>注意：  <p>OAuth 2.0标准在此步骤中支持至少2种客户端身份验证方法（<code>[!UICONTROL client_secret_basic]</code>和<code>[!UICONTROL client_secret_post]</code>）。 [!DNL Workfront Fusion]不自动支持<code>[!UICONTROL client_secret_basic]</code>方法。 如果您连接的服务要求将客户端ID和客户端密钥组合为一个字符串，然后将base64编码到授权标头，则您应在此处添加该标头和密钥值。</p> <p> 有关OAuth 2.0身份验证的更多信息，请参阅<a href="https://tools.ietf.org/html/rfc6749">OAuth 2.0授权框架</a>。</p> </p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Token placement]</p> </td> 
      <td> <p>选择在连接到指定的URL时是在[!UICONTROL header]、[!UICONTROL query string]中还是同时在这两个中发送令牌。</p> <p>令牌最常在请求标头中发送。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Header token name] </td> 
      <td> <p>在标头中输入授权令牌的名称。 默认值： <code>[!UICONTROL Bearer]</code>。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Query string parameter name] </td> 
      <td> <p>在查询字符串中输入授权令牌的名称。 默认值： <code>[!UICONTROL access_token]</code>。</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;保存连接设置。
1. 继续[OAuth 2.0请求模块设置](#oauth-20-request-module-setup)。

### 有关在[!UICONTROL HTTP] >[!UICONTROL Make an OAuth 2.0 request module]中创建与[!DNL Google]的连接的说明

以下示例显示如何使用[!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0]请求模块连接到[!DNL Google]。

1. 请确保已创建项目、配置OAuth设置并生成凭据，如[使用自定义OAuth客户端](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)连接 [!DNL Adobe Workfront Fusion] 到 [!DNL Google Services] 中所述。
1. 打开[!UICONTROL HTTP] >[!UICONTROL Make an OAuth 2.0 request]模块。
1. 单击连接框旁边的&#x200B;**[!UICONTROL Add]**。
1. 输入以下值：

   <table style="table-layout:auto">  
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection name] </td> 
      <td> <p>输入连接的名称。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Flow type]</p> </td> 
      <td> <p>[!UICONTROL Authorization Code]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Authorize URI]</td> 
      <td><code>https://accounts.google.com/o/oauth2/v2/auth</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Token URI]</td> 
      <td><code>https://www.googleapis.com/oauth2/v4/token</code> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope] </td> 
      <td> <p>添加单个范围。 有关范围的更多信息，请参阅[!DNL Google]文档中的[!DNL Google] API的<a href="https://developers.google.com/identity/protocols/oauth2/scopes">OAuth 2.O范围</a>。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Scope separator] </td> 
      <td> <p>[!UICONTROL SPACE]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client ID] </td> 
      <td> <p>输入您的[!DNL Google]客户端ID。 </p> <p>若要创建客户端ID，请参阅在<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md" class="MCXref xref">[!DNL Connect Adobe Workfront Fusion]中使用自定义OAuth客户端</a>创建[!DNL Google Services]的OAuth凭据</a>。<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create2" class="MCXref xref"></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Client Secret]</td> 
      <td> <p>输入您的[!DNL Google]客户端密钥。 </p> <p>要创建客户端密钥，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md#create2" class="MCXref xref">在<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md" class="MCXref xref">[!DNL Connect Adobe Workfront Fusion]中使用自定义OAuth客户端</a>创建[!DNL Google]服务的OAuth凭据</a>。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Authorize parameters]</p> </td> 
      <td> <p>添加<code>[!UICONTROL access_type]</code> - <code>[!UICONTROL offline] </code>键值对。</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/google-authentication-http.png"> </p> <p>注意：如果您遇到身份验证问题，例如令牌刷新问题，请尝试添加<code>[!UICONTROL prompt] </code>- <code>[!UICONTROL consent] </code>键值对。</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;保存连接设置。
1. 继续[OAuth 2.0请求模块设置](#oauth-20-request-module-setup)。

<!--### Instructions for connecting to [!DNL Microsoft Graph API] via the [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module 

For instructions regarding [!DNL Microsoft Graph API], see [Call the [!DNL MS Graph REST API] via the [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md).-->

## OAuth 2.0请求模块设置

当您已建立[!DNL Oauth 2].0连接（如[为 [!DNL OAuth] 请求创建连接](#creating-a-connection-for-an-oauth-request)中所述），请根据需要继续设置模块。 所有授权令牌都会自动包含在此请求中，以及任何其他使用相同连接的请求中。

配置[!UICONTROL HTTP] >[!UICONTROL Make an OAuth 2.0 request]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[在 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)中将信息从一个模块映射到另一个模块。

<!--
<img src="" style="width: 350;height: 74;">
-->

<table style="table-layout:auto">  
 <col> 
 <col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关设置连接的信息，请参阅本文中的<a href="#creating-a-connection-for-an-oauth-request" class="MCXref xref">为OAuth请求创建连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx]) </td> 
   <td> <p>使用此选项可设置错误处理。</p> <p>有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">错误处理。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>输入要向其发送请求的URL，如API端点、网站等。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 例如， <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> 输入所需的查询键值对。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Body type]</p> </td> 
   <td> <p>HTTP正文是在HTTP事务消息中传输的数据字节，这些字节紧跟在标头之后（如果存在任何要使用的标头）。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>原始正文类型通常适用于大多数HTTP正文请求，即使在开发人员文档未指定要发送的数据的情况下也是如此。</p> <p>在[!UICONTROL Content type]字段中指定解析数据的形式。</p> <p>尽管选择了内容类型，但数据仍会以开发人员文档规定或要求的任何格式输入。</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>此正文类型将使用<code>[!UICONTROL application/x-www-form-urlencoded]</code>POST数据。</p> <p>对于<code>[!UICONTROL application/x-www-form-urlencoded]</code>，发送到服务器的HTTP消息正文本质上是一个查询字符串。 键和值在以<code>&amp;</code>分隔的键值对中进行编码，且键和值之间有<code>=</code>。 </p> <p>对于二进制数据，改为<code>use [!UICONTROL multipart/form-data]</code>。</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>示例： </b></span></span> 
       <p>生成的HTTP请求格式的示例：</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data]是用于发送文件和数据的HTTP多部分请求。 它通常用于将文件上传到服务器。</p> <p>添加要在请求中发送的字段。 每个字段必须包含一个键值对。</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>输入要在请求正文中发送的键和值。</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>输入密钥，并在请求正文中指定要发送的源文件。</p> <p>映射您要从上一个模块上传的文件(如[!UICONTROL HTTP] &gt;[!UICONTROL Get a File]或[!UICONTROL Google Drive] &gt;[!UICONTROL Download a File)]，或手动输入文件名和文件数据。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>启用此选项可自动解析响应并转换JSON和XML响应，因此您无需使用[!UICONTROL JSON] &gt; [!UICONTROL Parse JSON]或[!UICONTROL XML] &gt; [!UICONTROL Parse XML]模块。</p> <p>在使用解析的JSON或XML内容之前，请手动运行一次模块，以便模块能够识别响应内容并允许您在后续模块中映射该内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>输入请求超时，以秒为单位(1-300)。 默认值为40秒。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> 启用此选项可将来自服务器的Cookie与场景中的所有HTTP模块共享。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p> 如果要使用自签名证书的TLS，请上载证书。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reject connections that are using unverified (self-signed) certificates] </td> 
   <td> <p>启用此选项可拒绝使用未经验证的TLS证书的连接。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow redirect]</td> 
   <td> <p> 启用此选项可在3xx响应中遵循URL重定向。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Follow all redirects] </td> 
   <td> <p>启用此选项后，URL重定向会带有所有响应代码。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Disable serialization of multiple same query string keys as arrays]</p> </td> 
   <td> <p>默认情况下，[!DNL Workfront Fusion]处理与数组相同的URL查询字符串参数键的多个值。 例如，<code>www.test.com?foo=bar&amp;foo=baz</code>将转换为<code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>。 激活此选项以禁用此功能。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request compressed content]</td> 
   <td> <p> 启用此选项可请求网站的压缩版本。</p> <p>这会添加<code>[!UICONTROL Accept-Encoding]</code>标头以请求压缩的内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>启用此选项可在HTTP请求中使用双向TLS。</p> <p>有关双方TLS的详细信息，请参阅<a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中的HTTP模块中使用双方TLS。</p> </td> 
  </tr> 
 </tbody> 
</table>
