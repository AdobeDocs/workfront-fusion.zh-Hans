---
title: HTTP >创建JWT请求模块
description: Adobe Workfront Fusion HTTP >发出JWT请求模块向URL发送HTTP(S)请求，并为其授权一个JSON Web令牌，Fusion会自动为您签名。
author: Becky
feature: Workfront Fusion
exl-id: 2f8c0b0d-085a-4b49-b350-4fd4cca1d0a7
TQID: 'https://experienceleague.adobe.com/zh-hans'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 5e6403abee4e5767da9134529b9e88070bad5f44
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 11%
---
# [!UICONTROL HTTP] > [!UICONTROL 发出JWT请求]模块

Adobe Workfront Fusion [!UICONTROL HTTP] > [!UICONTROL 发出JWT请求]模块向URL发送HTTP(S)请求，并授权它使用JSON Web令牌(JWT)，该模块会在每次调用时为您签名。 然后，将以与标准[!UICONTROL HTTP] > [!UICONTROL 发出请求]模块中相同的方式处理响应。

此模块的行为类似于标准[!UICONTROL 发出请求]模块，主要区别在于：它自动对您提供的声明签署JWT，并将其添加到请求中，默认情况下为`Authorization: Bearer <token>`。

使用此模块可调用任何需要已签名JWT进行身份验证的API，例如需要使用共享密钥(HMAC)或私钥(RSA/ECDSA)签名的短期持有者令牌的服务，而无需在单独的步骤中创建令牌。

如果API使用OAuth 2.0、基本身份验证、API密钥或客户端证书，请改用匹配的专用HTTP模块。

>[!NOTE]
>
>如果您要连接到当前没有专用连接器的Adobe产品，我们建议您使用Adobe Authenticator模块。
>
>有关详细信息，请参阅[Adobe Authenticator模块](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md)。

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
   <p>基于操作：适用于拥有基于操作的许可证的组织</p>
   <p>基于连接器（旧版）：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

有关 Adobe Workfront Fusion 许可证的详细信息，请参阅 [Adobe Workfront Fusion 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 创建JWT连接

该模块需要JWT连接。 该连接存储签名材料，因此密钥或私钥不必显示在场景中。

### 在Fusion中创建JWT连接

1. 添加[!UICONTROL HTTP] > [!UICONTROL 向方案发出JWT请求]模块。
1. 单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 配置连接字段：

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader"><p>连接名称</p></td>
      <td><p>输入连接名称。</p></td>
     </tr>
     <tr>
      <td role="rowheader"><p>算法</p></td>
      <td>
       <p>选择连接的签名算法。</p>
       <ul>
        <li><code>HS256</code></li>
        <li><code>HS384</code></li>
        <li><code>HS512</code></li>
        <li><code>RS256</code></li>
        <li><code>RS384</code></li>
        <li><code>RS512</code></li>
        <li><code>PS256</code></li>
        <li><code>PS384</code></li>
        <li><code>PS512</code></li>
        <li><code>ES256</code></li>
        <li><code>ES384</code></li>
        <li><code>ES512</code></li>
       </ul>
      </td>
     </tr>
     <tr>
      <td role="rowheader"><p>机密</p></td>
      <td>
       <p>输入签名密钥。</p>
       <ul>
        <li>对于<code>HS*</code>算法，请使用共享机密字符串。</li>
        <li>对于<code>RS*</code>、<code>PS*</code>和<code>ES*</code>算法，请使用PEM编码的私钥。</li>
       </ul>
      </td>
     </tr>
    </tbody>
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

>[!IMPORTANT]
>
>JWT连接仅用一个算法签名。 如果您的方案需要多个签名算法，请为每个算法创建单独的连接。 这与现有的独立JWT应用程序行为匹配。

## [!UICONTROL HTTP] > [!UICONTROL 发出JWT请求]模块及其字段

在配置[!UICONTROL HTTP] > [!UICONTROL 发出JWT请求]模块时，Adobe Workfront Fusion会按照它们在模块UI中的显示顺序显示以下列出的字段。 模块中的加粗标题表示必填字段。 除非选择&#x200B;**[!UICONTROL 显示高级设置]**，否则标记为高级的字段将隐藏。

<table style="table-layout:auto">
 <col>
 <col>
 <tbody>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 连接]</p></td>
   <td><p>选择现有JWT连接或创建新连接。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL URL]</p></td>
   <td><p>请求的目标URL。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 方法]</p></td>
   <td><p>HTTP方法，例如GET、POST、PUT、PATCH或DELETE。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 标头]</p></td>
   <td><p>键/值格式的自定义请求标头。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 查询字符串]</p></td>
   <td><p>键/值格式的查询字符串参数。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 主体类型]</p></td>
   <td><p>如何对请求正文进行编码。 选项包括Raw、application/x-www-form-urlencoded和multipart/form-data。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 解析响应]</p></td>
   <td><p>启用后，Fusion将根据响应内容类型解析响应正文。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL JWT有效负荷（声明）]</p></td>
   <td><p>作为声明包含在JWT有效负载中的键/值对。 保留的声明<code>exp</code>、<code>iat</code>和<code>nbf</code>必须为NumericDate — 自Unix纪元以来的秒数。 声明值将保留其JSON类型，因此数字将保留数字，布尔值将保留布尔值。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Timeout]（高级）</p></td>
   <td><p>以秒为单位指定请求超时(1-300)。 默认值为40秒。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 重试计数]（高级）</p></td>
   <td><p>指定请求因可重试错误而失败时应重试的次数。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 其他重试状态代码]（高级）</p></td>
   <td><p>指定应视为可重试的其他HTTP状态代码。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 与其他HTTP模块共享Cookie]（高级）</p></td>
   <td><p>启用此选项可将来自服务器的Cookie与场景中的所有HTTP模块共享。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 自签名证书]（高级）</p></td>
   <td><p>如果要使用自签名证书的TLS，请上载证书。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 拒绝使用未验证（自签名）证书的连接] （高级）</p></td>
   <td><p>启用此选项可拒绝使用未经验证的TLS证书的连接。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 遵循重定向]（高级）</p></td>
   <td><p>启用此选项可在3xx响应中遵循URL重定向。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 禁用将多个相同的查询字符串键序列化为数组]（高级）</p></td>
   <td><p>默认情况下，Workfront Fusion会处理与数组相同的URL查询字符串参数键的多个值。 例如，<code>www.test.com?foo=bar&amp;foo=baz</code>将转换为<code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>。 激活此选项以禁用此功能。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 请求压缩内容] （高级）</p></td>
   <td><p>启用此选项可请求网站的压缩版本。 添加<code>[!UICONTROL Accept-Encoding]</code>标头以请求压缩的内容。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 使用双向TLS]（高级）</p></td>
   <td><p>启用此选项可在HTTP请求中使用双向TLS。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL Sign Options]（高级）</p></td>
   <td><p>对于要添加到请求中的每个符号选项，单击<b>添加项</b>并输入参数的名称和值。</p><p>传递给JWT签名者的其他选项，如<code>expiresIn</code>、<code>issuer</code>、<code>audience</code>、<code>subject</code>和<code>keyid</code>。 持续时间值（如<code>expiresIn</code>）由<code>jsonwebtoken</code>库解释。 纯数字被视为毫秒，因此使用单位字符串（如<code>"1h"</code>或<code>"3600s"</code>）来明确显示。 算法是从连接中获取的，不能在此处覆盖。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 标头名称] （高级）</p></td>
   <td><p>输入或映射接收已签名JWT的请求标头的名称。 默认值： <code>Authorization</code>。 标头名称不得包含点(<code>.</code>)，因为虚线名称会被拒绝，并且在请求日志中不能被掩盖。</p></td>
  </tr>
  <tr>
   <td role="rowheader"><p>[!UICONTROL 令牌类型]（高级）</p></td>
   <td><p>输入或映射放置在令牌之前的身份验证方案，如<code>Bearer</code>。 将此项留空可发送不带前缀的原始令牌。</p></td>
  </tr>
 </tbody>
</table>

## 如何构建令牌

1. 模块将收集[!UICONTROL JWT有效负荷（声明）]字段中的声明。
1. 保留声明，如<code>费用</code>，<code>iat</code>，和<code>nbf</code> 转换为NumericDate值。
1. 模块应用[!UICONTROL 签名选项]，并使用连接中的算法对令牌进行签名。
1. 签名令牌放置在由[!UICONTROL 标头名称]定义的请求标头中。
1. 如果设置了[!UICONTROL 令牌类型]，则模块会在令牌之前添加前缀。 例如，<code>Bearer eyJ...</code>.
1. 请求已发送，处理响应的方式与标准[!UICONTROL HTTP] > [!UICONTROL 发出请求]模块相同。

已签名的令牌会自动在调试和错误日志中被掩盖，因此永远不会公开。

## 示例

### 连接

- 算法： `HS256`
- 密钥： `my-shared-secret`

### 模块设置

- URL： `https://api.example.com/v1/orders`
- 方法： `GET`
- JWT有效负荷（声明）：
  - `sub` = `service-account-42`
  - `iss` = `make-integration`
- 签名选项：
  - `expiresIn` = `1h`
- 标头名称： `Authorization`
- 令牌类型： `Bearer`

### 结果

模块发送带有类似以下标题的请求：

```text
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...
```

## 常见问题解答/疑问

### 为什么我的令牌过期得这么快？

您可能输入了`expiresIn`的空值，如`3600`。 `jsonwebtoken`库将纯数字解释为毫秒。 请改用单位字符串，如`"1h"`或`"3600s"`。

### 何时创建令牌？

每次运行模块时，模块都会签署新的JWT，而不是在创建连接时。 连接仅存储签名材料和算法，因此声明（如`iat`和`exp`）反映该模块运行的时间。

如果请求在同一模块执行中重试，Fusion会对这些重试尝试重新使用相同的签名令牌，而不是为每次尝试签名一个新令牌。 因此，非常短的`expiresIn`值可能会在重试发生之前过期，并导致重试发送已过期的令牌。 要避免此情况，请使用清除单位字符串，如`"1h"`或`"3600s"`，并避免令牌生命周期过短。

### 我可以根据请求更改算法吗？

不可以。 算法由连接来固定。 如果需要不同的算法，请创建不同的JWT连接。

### 我能否在自定义标头中发送令牌？

可以。 将[!UICONTROL 标头名称]字段设置为自定义名称，但它不能包含点(`.`)。

### 我可以在没有`Bearer`的情况下发送原始令牌吗？

可以。 将[!UICONTROL 令牌类型]留空。

### 令牌是否在日志中可见？

不可以。 已签名的令牌在调试和错误日志中自动被掩盖。


>[!NOTE]
>
>技术说明：签名使用`jsonwebtoken`库并镜像独立JWT应用程序的签名行为，因此相同的输入将生成与独立JWT应用程序相同的令牌。
