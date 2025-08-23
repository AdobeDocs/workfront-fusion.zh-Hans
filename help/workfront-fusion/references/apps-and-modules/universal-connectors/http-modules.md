---
title: HTTP >其他模块
description: Adobe Workfront Fusion HTTP应用程序为基于超文本传输协议(HTTP)协议的通信提供各种模块。 HTTP是万维网数据通信的基础。 您可以使用这些模块下载网页和文件、调用Webhook和API端点等。
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# HTTP >其他模块

Adobe Workfront Fusion [!UICONTROL HTTP]应用程序为基于超文本传输协议(HTTP)协议的通信提供各种模块。 HTTP是万维网数据通信的基础。 您可以使用这些模块下载网页和文件、调用Webhook和API端点等。

模块的正确选择取决于您要访问的资源所采用的身份验证/授权机制。 以下是模块示例

* **发出请求**：主要用于不使用任何身份验证或授权的资源
* **发出基本身份验证请求**：对于使用[!DNL HTTP]基本身份验证(BA)的资源
* **发出OAuth 2.0请求**：对于使用OAuth 2.0授权协议的资源
* **发出客户端证书身份验证请求**：对于采用需要客户端证书的授权协议的资源
* **发出API密钥授权请求**：对于采用API密钥进行授权的资源

>[!NOTE]
>
>如果您要连接到当前没有专用连接器的Adobe产品，我们建议您使用Adobe Authenticator模块。
>
>有关详细信息，请参阅[Adobe Authenticator模块](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md)。

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

## 请求模块

有关特定请求模块说明，请参阅以下文章：

* [[!UICONTROL HTTP] > [!UICONTROL 发出请求]模块](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL 发出基本授权请求]模块](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL 发出OAuth 2.0请求]模块](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL 发出客户端证书授权请求]模块](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL 发出API密钥授权请求]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## 其他操作模块

* [[!UICONTROL 获取文件]](#get-a-file)
* [[!UICONTROL 解析目标URL]](#resolve-a-target-url)

### [!UICONTROL 获取文件]

此操作模块从指定的URL下载文件。 下载文件后，您可以使用场景中的其他模块进一步处理文件（映射文件数据）。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 将所有状态计算为错误（2xx和3xx除外）] </td> 
   <td> <p>使用此选项可设置错误处理。</p> <p>有关详细信息，请参阅Adobe Workfront Fusion中的<a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">错误处理</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>输入或映射要下载的文件的URL。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 与其他HTTP模块共享Cookie] </td> 
   <td> <p>如果您希望此站点的Cookie对其他模块可用，请启用此选项。 </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 解析目标URL]

此操作模块解析HTTP重定向链并返回目标URL。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>输入或映射要解析的URL，如[!DNL bit.ly] URL。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法] </td> 
   <td> <p>选择您要使用[!UICONTROL HEAD]方法还是[!UICONTROL GET]方法。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 迭代器模块

### [!UICONTROL 检索标头]

此模块在一个单独的捆绑包中从指定的HTTP模块返回每个标头（名称和值）。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> 选择要从中检索标头的模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 生成JSON Web令牌(JWT)

可以使用内置函数生成JWT令牌：

标题：

![JWT标头](/help/workfront-fusion/references/apps-and-modules/assets/jwt-header-350x19.png)

用于复制粘贴的代码(&amp;P)：

```
{{replace(replace(replace(base64("{""alg"":""HS256"",""typ"":""JWT""}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

有效负载：

![JWT有效负荷](/help/workfront-fusion/references/apps-and-modules/assets/jwt-payload-350x17.png)

用于复制粘贴的代码(&amp;P)：

```
{{replace(replace(replace(base64("{""iss"":""key"",""exp"":" + (timestamp + 60) + "}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

令牌：

![JWT令牌](/help/workfront-fusion/references/apps-and-modules/assets/jwt-token-350x15.png)

用于复制粘贴的代码(&amp;P)：

```
{{1.value}}.{{2.value}}.{{replace(replace(replace(sha256(1.value + "." + 2.value; "base64"; "secret"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```
