---
title: HTTP >生成客户端证书授权请求模块
description: 此 [!DNL Adobe Workfront Fusion] 模块允许您配置具有HTTP客户端证书授权的HTTP请求并将其提交到服务器。 接收的HTTP响应随后包含在输出包中。
author: Becky
feature: Workfront Fusion
exl-id: cc33530c-3010-4955-8819-5eb8373a0e10
source-git-commit: c2680972c616a90b55fdaf2c907920e435f23469
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 1%

---

# HTTP > [!UICONTROL Make a Client Certificate Authorization request]模块

>[!NOTE]
>
>除了Adobe Workfront许可证之外，Adobe Workfront Fusion还需要[!DNL Adobe Workfront Fusion]许可证。

此[!DNL Adobe Workfront Fusion]模块允许您使用HTTP客户端证书授权配置HTTP请求并将其提交到服务器。 接收的HTTP响应随后包含在输出包中。

>[!NOTE]
>
>如果您要连接到当前没有专用连接器的Adobe产品，我们建议您使用Adobe Authenticator模块。
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

## [!UICONTROL HTTP] > [!UICONTROL Make a Client Certificate Authorization request]模块配置

配置[!UICONTROL HTTP] > [!UICONTROL Make a Client Certificate Authorization request]模块时，[!DNL Adobe Workfront Fusion]显示下面列出的字段。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[在 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)中将信息从一个模块映射到另一个模块。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Credentials]</td> 
   <td> <p>选择包含您的客户端证书身份验证凭据的密钥，或单击<strong>[!UICONTROL Add]</strong>将您的凭据添加到新密钥中。 </p> <p>注意：您可以添加更多凭据以便轻松地在每个连接之间切换。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx )] </td> 
   <td> <p>使用此选项可设置错误处理。</p> <p>有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">错误处理。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>输入要向其发送请求的URL，如API端点、网站等。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
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
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>原始正文类型通常适用于大多数HTTP正文请求，即使在开发人员文档未指定要发送的数据的情况下也是如此。</p> <p>在[!UICONTROL Content type]字段中指定解析数据的形式。</p> <p>尽管选择了内容类型，模块仍会以开发人员文档规定或要求的任何格式输入数据。</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>此正文类型使用<code>application/x-www-form-urlencoded</code>为[!UICONTROL POST]数据。</p> <p>对于<code>[!UICONTROL application/x-www-form-urlencoded]</code>，发送到服务器的HTTP消息正文本质上是一个查询字符串。 键和值在键值对中进行编码，键值对以<code>&amp;</code>分隔，在键和值之间使用<code>=</code>。 </p> <p>对于二进制数据，请改用<code>[!UICONTROL multipart/form-data]</code>。</p> <p>对于要添加的每个键值对，在“字段”字段中，单击“<b>添加项</b>”，然后输入键和值。</p>
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>示例： </b></span></span> 
       <p>生成的HTTP请求格式的示例：</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data]是用于发送文件和数据的HTTP多部分请求。 它通常用于将文件上传到服务器。</p> <p>添加要在请求中发送的字段。 每个字段都必须包含键值对。</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Text]</strong> </p> <p>输入要在请求正文中发送的键和值。</p> </li> 
       <li> <p><strong>[!UICONTROL File]</strong> </p> <p>输入密钥，并在请求正文中指定要发送的源文件。 从上一个模块中选择一个源文件，或映射文件的名称和数据。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Parse response]</p> </td> 
   <td> <p>启用此选项可自动解析响应并转换JSON和XML响应，因此您无需使用[!UICONTROL JSON] &gt; [!UICONTROL Parse JSON]或[!UICONTROL XML] &gt; [!UICONTROL Parse XML]模块。</p> <p>在使用解析的JSON或XML内容之前，请手动运行一次模块，以便模块能够识别响应内容并允许您在后续模块中映射该内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Timeout] </td> 
   <td> <p>以秒为单位指定请求超时(1-300)。 默认值为40秒。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules]</td> 
   <td> <p> 启用此选项可将来自服务器的Cookie与场景中的所有HTTP模块共享。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Self-signed certificate]</td> 
   <td> <p>要添加自签名证书，请执行以下操作：</p>
          <ol>
            <li value="1">
              <p>单击 <b>[!UICONTROL Extract]</b>。</p>
            </li>
            <li value="2">
              <p>选择要提取的文件类型。</p>
            </li>
            <li value="3">
              <p>选择包含或证书的文件。</p>
            </li>
            <li value="4">
              <p>输入文件的密码。</p>
            </li>
            <li value="5">
              <p>单击<b>[!UICONTROL Save]</b>提取文件并返回模块设置。</p>
            </li>
          </ol>
</p> </td> 
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
   <td> <p> 启用此选项可请求网站的压缩版本。</p> <p>添加<code>[!UICONTROL Accept-Encoding]</code>标头以请求压缩的内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Mutual TLS]</td> 
   <td> <p>启用此选项可在HTTP请求中使用双向TLS。</p> <p>有关双方TLS的详细信息，请参阅<a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">在HTTP模块中使用双方TLS</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>
