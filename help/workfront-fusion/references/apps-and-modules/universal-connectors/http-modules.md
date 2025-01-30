---
title: HTTP &amp；gt；其他模块
description: ' [!DNL Adobe Workfront Fusion] HTTP应用为基于超文本传输协议(HTTP)协议的通信提供了各种模块。 HTTP是万维网数据通信的基础。 您可以使用这些模块下载网页和文件、调用Webhook和API端点等。'
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# HTTP >其他模块

>[!NOTE]
>
>除[!UICONTROL Adobe Workfront]许可证外，[!UICONTROL Adobe Workfront Fusion]还需要[!UICONTROL Adobe Workfront Fusion]许可证。

[!DNL Adobe Workfront Fusion] [!UICONTROL HTTP]应用为基于超文本传输协议(HTTP)协议的通信提供了各种模块。 HTTP是万维网数据通信的基础。 您可以使用这些模块下载网页和文件、调用Webhook和API端点等。

模块的正确选择取决于您要访问的资源所采用的身份验证/授权机制。 以下是模块示例

* 发出请求：通用模块主要用于未采用任何类型的身份验证/授权的资源
* 发出基本身份验证请求：针对采用[!DNL HTTP]基本身份验证(BA)的资源
* 发出OAuth 2.0请求：针对采用OAuth 2.0授权协议的资源
* 发出客户端证书身份验证请求：对于采用需要客户端证书的授权协议的资源。
* 发出API密钥授权请求：用于使用API密钥进行授权的资源。

>[!NOTE]
>
>如果您要连接到的Adobe产品当前没有专用连接器，我们建议您使用Adobe Authenticator模块。
>
>有关详细信息，请参阅[Adobe Authenticator模块](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md)。

## 请求模块

有关特定请求模块说明，请参阅以下文章：

* [[!UICONTROL HTTP] > [!UICONTROL Make a request]模块](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Basic Authorization request]模块](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request]模块](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Client Certificate Authorization request]模块](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an API Key Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## 其他操作模块

* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Resolve a target URL]](#resolve-a-target-url)

### [!UICONTROL Get a File]

此操作模块从指定的URL下载文件。 下载文件后，您可以使用场景中的其他模块进一步处理文件（映射文件数据）。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>输入或映射要下载的文件的URL。 </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resolve a target URL]

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
   <td role="rowheader">[!UICONTROL Method] </td> 
   <td> <p>选择您要使用[!UICONTROL HEAD]方法还是[!UICONTROL GET]方法。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 迭代器模块

### [!UICONTROL Retrieve headers]

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
