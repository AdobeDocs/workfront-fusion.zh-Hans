---
title: 调用MS Graph REST API
description: 通过Adobe Workfront Fusion HTTP调用MS Graph REST API &>发出OAuth 2.0请求模块
author: Becky
feature: Workfront Fusion
exl-id: f411c807-955d-44fe-98b1-3ebba3fe0861
source-git-commit: a7ee3e751b75523c4da62cea71e59a63f98b95e0
workflow-type: tm+mt
source-wordcount: '679'
ht-degree: 2%

---

# 调用MS Graph REST API

许多Microsoft Web服务是通过Microsoft Graph API访问的。 您可以使用Workfront Fusion HTTP >创建OAuth 2.0请求模块来创建与Microsoft Graph API的连接。

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
   <p>当前：无Workfront Fusion许可证要求。</p>
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

## 在Workfront应用程序注册门户中注册Microsoft Fusion

要创建与Microsoft Graph REST API的连接，必须首先注册Adobe Workfront Fusion。

1. 开始注册新应用程序，如Microsoft文档中的[在Microsoft标识平台中注册应用程序](https://docs.microsoft.com/en-us/graph/auth-register-app-v2)中所述。

   作为注册的一部分，Microsoft需要以下信息：

   <table style="table-layout:auto">
      <tr>
        <td>应用程序名称</td>
        <td>输入应用程序的名称，如“我的Workfront Fusion应用程序”。</td>
      </tr>
      <tr>
        <td>重定向 URL</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/oauth2</code></td>
      </tr>
    </table>

1. 完成应用程序注册后，记下应用程序ID。

   >[!IMPORTANT]
   >
   >您需要具有应用程序ID才能在Workfront Fusion中设置连接。

1. 生成客户端密码。 记下这个秘密。

   有关说明，请参阅Microsoft文档中的[在Microsoft标识平台中注册应用程序](https://docs.microsoft.com/en-us/graph/auth-register-app-v2)。

   >[!IMPORTANT]
   >
   >您需要客户端密钥才能在Workfront Fusion中设置连接。

1. 配置应用程序的权限。

   有关查找和配置这些字段的详细信息，请参阅Microsoft文档中[无需用户即可访问](https://docs.microsoft.com/en-us/graph/auth-v2-service)的“配置Microsoft Graph的权限”部分。

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">您的应用程序需要哪种类型的权限？</td> 
      <td>选择 <code>Delegated permissions</code>。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">选择权限</td> 
      <td> <p>选择以下权限：</p> 
       <ul> 
        <li> <p><code>offline_access</code> </p> </li> 
        <li> <p><code>openid</code> </p> </li> 
        <li> <p>您的集成所需的任何其他权限（示例： <code>User.Read</code>）</p> </li> 
       </ul> <p><b>重要信息</b>：您需要具有所选权限才能在Workfront Fusion中设置连接。</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 继续[在Workfront Fusion中配置MS Graph API连接](#configure-your-ms-graph-api-connection-in-workfront-fusion)。

## 在Workfront Fusion中配置MS Graph API连接

按照[在Workfront应用程序注册门户](#register-workfront-fusion-in-the-microsoft-application-registration-portal)中注册Workfront Fusion中所述，注册Microsoft Fusion后，可以在HTTP >发出Oauth 2.0请求模块中配置连接。

1. 添加HTTP >向方案发出OAuth 2.0调用模块。
1. 单击连接字段旁边的&#x200B;**添加**。
1. 按如下方式配置连接字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">连接名称</td> 
      <td>输入连接的名称。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">环境</p> </td> 
      <td>选择您是连接到生产帐户还是非生产帐户。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">类型</p> </td> 
      <td>选择您是要连接到服务帐户还是个人帐户。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p role="rowheader">流类型</p> </td> 
      <td>选择 <code>Authorization Code</code>。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader">授权URI</td> 
      <td>输入<code>https://login.microsoftonline.com/common/oauth2/v2.0/authorize</code>。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader">令牌URI</td> 
      <td>输入<code>https://login.microsoftonline.com/common/oauth2/v2.0/token</code>。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader">范围</td> 
      <td> <p>按照在Microsoft应用程序注册门户中<a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">注册Workfront Fusion</a>中所述，输入注册时您在中选择的权限。</p> <p>对于每个作用域，单击<b>添加</b>并键入权限。</p> <p>示例： <code>offline_access</code>。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">范围分隔符</td> 
      <td>选择 <code>SPACE</code>。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader">客户端 ID</td> 
      <td>在Microsoft应用程序注册门户</a>的<a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">注册Workfront Fusion中输入步骤2中的应用程序ID。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">客户端密码</td> 
      <td>在Microsoft应用程序注册门户</a>的<a href="#register-workfront-fusion-in-the-microsoft-application-registration-portal" class="MCXref xref">注册Workfront Fusion中，输入您在步骤3中生成的客户端密钥。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">授权参数</td> 
      <td> <p>添加以下授权参数。 对于要添加的每个参数，单击<b>添加项</b>并输入以下内容： </p> 
       <ul> 
        <li> <p>键： <code> response_mode</code>值： <code>query</code></p> </li> 
        <li> <p>键： <code>prompt </code>值： <code>consent</code></p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">访问令牌参数</td> 
      <td>您无需在此字段中输入任何内容。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">刷新令牌参数</td> 
      <td> 
       <ol> 
        <li value="1"> <p>单击<b>添加项</b>。</p> </li> 
        <li value="2"> <p>在<b>键</b>字段中，输入<code>scope</code>。</p> </li> 
        <li value="3"> <p>在<b>值</b>字段中，输入您在范围字段中输入的所有范围，并以空格分隔。</p> <p>示例： <code>offline_access openid User.Read</code></p> </li> 
       </ol> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">自定义标题</td> 
      <td>您无需在此字段中输入任何内容。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">令牌放置</td> 
      <td><code>In the header</code> </td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**继续**。
1. 在出现的窗口中，单击&#x200B;**接受**&#x200B;以完成连接并返回模块。
