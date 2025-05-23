---
title: HTTP >发出API密钥授权请求
description: 此 [!DNL Adobe Workfront Fusion] 操作模块向需要API密钥身份验证授权的指定URL发送HTTPS请求，并处理响应。
author: Becky
feature: Workfront Fusion
exl-id: 362b80b5-42f4-4b82-b06c-39c7c5a1eb1a
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1020'
ht-degree: 1%

---

# HTTP > [!UICONTROL 发出API密钥授权请求]

此[!DNL Adobe Workfront Fusion]操作模块向需要API密钥身份验证授权的指定URL发送HTTPS请求，并处理响应。

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
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## [!UICONTROL HTTP] > [!UICONTROL 发出API密钥授权请求]模块配置

配置[!UICONTROL HTTP] > [!UICONTROL 发出API密钥授权请求]模块时，[!DNL Adobe Workfront Fusion]显示以下列出的字段。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[在 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)中将信息从一个模块映射到另一个模块。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 凭据]</td> 
   <td> <p>选择包含API密钥身份验证凭据的密钥。 要添加新键，请单击<strong>[!UICONTROL Add]</strong>并配置以下信息：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 键名]</strong></p> <p>输入这组API凭据的名称。</p> </li> 
     <li> <p><strong>[!UICONTROL 键]</strong> </p> <p>输入API密钥。</p> </li> 
     <li> <p><strong>[!UICONTROL API密钥放置]</strong> </p> <p>选择是将API密钥放在API调用的标头中还是查询中。</p> </li> 
     <li> <p><strong>[!UICONTROL API密钥参数名称]</strong> </p> <p>输入API调用用于标识API密钥的名称，如“apiKey”或“X-API-Key”。 您可以在该模块所连接的Web服务的文档中查找此信息。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">&lbrack;！UICONTROL将所有状态计算为错误（2xx和3xx除外） </td> 
   <td> <p>使用此选项可设置错误处理。</p> <p>有关详细信息，请参阅<a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref">错误处理</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>输入要向其发送请求的URL，如API端点、网站等。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 方法]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers] </td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 例如， <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p> 输入所需的查询键值对。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 主体类型]</p> </td> 
   <td> <p>HTTP正文是在HTTP事务消息中传输的数据字节，这些字节紧跟在标头之后（如果存在任何要使用的标头）。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p>原始正文类型通常适用于大多数HTTP正文请求，即使在开发人员文档未指定要发送的数据的情况下也是如此。</p> <p>在[!UICONTROL 内容类型]字段中指定解析数据的形式。</p> <p>尽管选择了内容类型，模块仍会以开发人员文档规定或要求的任何格式输入数据。</p> </li> 
     <li> <p><strong>[!UICONTROL Application/x-www-form-urlencoded]</strong> </p> <p>此正文类型使用<code>application/x-www-form-urlencoded</code>对[!UICONTROL POST]数据进行处理。</p> <p>对于<code>[!UICONTROL application/x-www-form-urlencoded]</code>，发送到服务器的HTTP消息正文本质上是一个查询字符串。 键和值在键值对中进行编码，键值对以<code>&amp;</code>分隔，在键和值之间使用<code>=</code>。 </p> <p>对于二进制数据，请改用<code>[!UICONTROL multipart/form-data]</code>。</p> 
      <div class="example" data-mc-autonum="<b>Example: </b>">
       <span class="autonumber"><span><b>示例： </b></span></span> 
       <p>生成的HTTP请求格式的示例：</p> 
       <p><code>field1=value1&amp;field2=value2</code> </p> 
      </div> </li> 
     <li> <p><strong>[!UICONTROL Multipart/form-data]</strong> </p> <p>[!UICONTROL Multipart/form-data]是用于发送文件和数据的HTTP多部分请求。 它通常用于将文件上传到服务器。</p> <p>添加要在请求中发送的字段。 每个字段都必须包含键值对。</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL 文本]</strong> </p> <p>输入要在请求正文中发送的键和值。</p> </li> 
       <li> <p><strong>[!UICONTROL 文件]</strong> </p> <p>输入密钥，并在请求正文中指定要发送的源文件。</p> <p>映射您要从上一个模块上传的文件(如[!UICONTROL HTTP] &gt; [!UICONTROL Get a File]或[!UICONTROL Google Drive] &gt;[!UICONTROL Download a File])，或手动输入文件名和文件数据。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 解析响应]</p> </td> 
   <td> <p>启用此选项可自动解析响应并转换JSON和XML响应，因此您无需使用[!UICONTROL JSON] &gt; [!UICONTROL Parse JSON]或[!UICONTROL XML] &gt; [!UICONTROL Parse XML]模块。</p> <p>在使用解析的JSON或XML内容之前，请手动运行一次模块，以便模块能够识别响应内容并允许您在后续模块中映射该内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 超时] </td> 
   <td> <p>以秒为单位指定请求超时(1-300)。 默认值为40秒。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 与其他HTTP模块共享Cookie]</td> 
   <td> <p> 启用此选项可将来自服务器的Cookie与场景中的所有HTTP模块共享。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 自签名证书]</td> 
   <td> <p>要添加自签名证书，请执行以下操作：</p>
          <ol>
            <li value="1">
              <p>单击<b>[!UICONTROL 提取]</b>。</p>
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
              <p>单击<b>[!UICONTROL 保存]</b>以提取文件并返回到模块设置。</p>
            </li>
          </ol>
</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拒绝使用未验证（自签名）证书的连接] </td> 
   <td> <p>启用此选项可拒绝使用未经验证的TLS证书的连接。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 遵循重定向]</td> 
   <td> <p> 启用此选项可在3xx响应中遵循URL重定向。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 遵循所有重定向] </td> 
   <td> <p>启用此选项后，URL重定向会带有所有响应代码。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 禁用将多个相同的查询字符串键序列化为数组]</p> </td> 
   <td> <p>默认情况下，[!DNL Workfront Fusion]处理与数组相同的URL查询字符串参数键的多个值。 例如，<code>www.test.com?foo=bar&amp;foo=baz</code>将转换为<code>www.test.com?foo[0]=bar&amp;foo[1]=baz</code>。 激活此选项以禁用此功能。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 请求压缩内容]</td> 
   <td> <p> 启用此选项可请求网站的压缩版本。</p> <p>添加<code>[!UICONTROL Accept-Encoding]</code>标头以请求压缩的内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 使用双向TLS]</td> 
   <td> <p>启用此选项可在HTTP请求中使用双向TLS。</p> <p>有关双方TLS的详细信息，请参阅<a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/use-mtls-in-http-modules.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中的HTTP模块中使用双方TLS。</p> </td> 
  </tr> 
 </tbody> 
</table>
