---
title: AWS S3模块
description: ' [!DNL Adobe Workfront Fusion AWS] S3模块允许您对S3存储桶执行操作。'
author: Becky
feature: Workfront Fusion
exl-id: 6b2d9dd5-0b33-4297-aea0-aba26072b26a
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1468'
ht-degree: 0%

---

# AWS S3模块

[!DNL Adobe Workfront Fusion AWS] S3模块允许您对S3存储桶执行操作。

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

要使用[!UICONTROL AWS S3]模块，您必须拥有[!DNL Amazon Web Service]帐户。

## AWS S3 API信息

AWS S3连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td>https://s3.{{parameters.region}}.amazonaws.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.5.21</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL AWS]连接到Workfront Fusion {#connect-aws-to-workfront-fusion}

要将[!DNL AWS S3]连接到Workfront Fusion，您必须将您的[!DNL AWS]帐户连接到Workfront Fusion。 为此，您首先需要在[!DNL AWS] [!UICONTROL IAM]中创建API用户。

1. 登录到您的[!DNL AWS] [!UICONTROL IAM]帐户。
1. 导航到&#x200B;**[!UICONTROL 身份和访问管理]** > **[!UICONTROL 访问管理]** > **[!UICONTROL 用户]**。

1. 单击&#x200B;**[!UICONTROL 添加用户]**。
1. 输入新用户的名称并在&#x200B;**[!UICONTROL 访问类型]**&#x200B;部分中选择[!UICONTROL 编程访问]选项。
1. 单击&#x200B;**[!UICONTROL 直接附加现有策略]**，然后在搜索栏中搜索&#x200B;**[!UICONTROL AmazonS3FullAccess]**。 出现时单击它，然后单击&#x200B;**[!UICONTROL 下一步]**。

1. 继续其他对话框屏幕，然后单击&#x200B;**[!UICONTROL 创建用户]**。
1. 复制提供的&#x200B;**[!UICONTROL 访问密钥ID]**&#x200B;和&#x200B;**[!UICONTROL 访问密钥]**。

1. 转到Workfront Fusion并打开[!DNL AWS S3]模块的&#x200B;**[!UICONTROL 创建连接]**&#x200B;对话框。
1. 从步骤7到相应的字段输入[!UICONTROL 访问密钥ID]和[!UICONTROL 访问密钥]，然后单击&#x200B;**[!UICONTROL 继续]**&#x200B;建立连接。

已建立连接。 您可以继续设置模块。

## [!DNL AWS S3]模块及其字段

在配置[!DNL AWS S3]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL AWS S3]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)
* [搜索](#searches)

### 操作

* [[!UICONTROL 创建存储桶]](#create-bucket)
* [[!UICONTROL 获取文件]](#get-file)
* [[!UICONTROL 进行API调用]](#make-an-api-call)
* [[!UICONTROL 上载文件]](#upload-file)

#### [!UICONTROL 创建存储桶]

此操作模块可在AWS中创建存储段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL AWS]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-aws-to-workfront-fusion" class="MCXref xref">将[!DNL AWS]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL名称] </td> 
   <td> <p>输入新存储段的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL区域] </td> 
   <td> <p>选择您的区域端点。 有关详细信息，请参阅AWS文档中的<a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">区域端点</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取文件]

此操作模块从存储段下载文件。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL AWS]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-aws-to-workfront-fusion" class="MCXref xref">将[!DNL AWS]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL区域] </td> 
   <td> <p>选择您的区域端点。 有关详细信息，请参阅<a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">文档中的</a>区域端点[!DNL AWS]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Bucket] </td> 
   <td> <p>选择要从中下载文件的存储桶。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL路径]</p> </td> 
   <td> <p>输入文件的路径。 示例：<code>/photos/2019/February/image023.jpg</code>。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 进行API调用]

此操作模块对AWS S3 API进行自定义调用。

有关[!DNL Amazon S3] API的详细讨论，请参阅[[!DNL Amazon S3] [!UICONTROL REST] API简介](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html)。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL AWS]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-aws-to-workfront-fusion" class="MCXref xref">将[!DNL AWS]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL区域] </td> 
   <td> <p>选择您的区域端点。 有关详细信息，请参阅<a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">文档中的</a>区域端点[!DNL AWS]。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL URL]</td> 
   <td> <p>输入主机URL。 路径必须相对于<code> https://s3.&lt;selected-region>.amazonaws.com/</code>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL方法]</td> 
   <td> <p>选择配置API调用所需的[！UICONTROL HTTP]请求方法。 有关详细信息，请参阅Adobe Workfront Fusion<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">中的</a>[！UICONTROL HTTP]请求方法。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Headers]</td> 
   <td> <p>添加请求标头。 对于要添加的每个标头，单击<b>添加项</b>并输入标头。 您可以使用以下常用请求标头。 有关更多请求标头，请参阅<a href="https://docs.aws.amazon.com/AmazonS3/latest/API/RESTCommonRequestHeaders.html">[!DNL AWS S3] API文档</a>。</p> <p>Workfront Fusion会自动添加授权标头。</p> 
    <table style="table-layout:auto">
     <col> 
     <col> 
     <thead> 
      <tr> 
       <th>标题名称</th> 
       <th> <p> 描述</p> </th> 
      </tr> 
     </thead> 
     <tbody> 
      <tr> 
       <td role="rowheader"> <p>[！UICONTROL Content-Length]</p> </td> 
       <td> <p>根据RFC 2616的消息长度（不带标头）。 加载XML的[！UICONTROL PUT]和操作（如日志记录和ACL）需要此标头。</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[！UICONTROL Content-Type]</p> </td> 
       <td> <p>资源的内容类型（如果请求内容位于正文中）。 示例：<code>text/plain</code>。</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[！UICONTROL Content-MD5]</p> </td> 
       <td> <p>根据RFC 1864对消息的128位MD5摘要（不包括标头）进行Base64编码。 此标头可用作消息完整性检查，以验证数据是否与最初发送的数据相同。 虽然这是可选的，但我们建议使用[！UICONTROL Content-MD5]机制作为端到端完整性检查。 有关[！UICONTROL REST]请求身份验证的更多信息，请参阅AWS文档中的<a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/RESTAuthentication.html?r=1821">签名和身份验证REST请求</a>。</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[！UICONTROL日期]</p> </td> 
       <td> <p>请求者的当前日期和时间。 示例： <code>Wed, 01 Mar 2006 12:00:00 GMT</code>。 指定<code>Authorization </code>标头时，必须指定<code>x-amz-date</code>或<code>Date </code>标头。</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[！UICONTROL Expect]</p> </td> 
       <td> <p>当您的应用程序使用[！UICONTROL 100-continue]时，它会在收到确认后才发送请求正文。 如果根据标头拒绝消息，则不会发送消息正文。 仅当您发送正文时，才能使用此标头。</p> <p>有效值： [！UICONTROL 100-continue]</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[！UICONTROL主机]</p> </td> 
       <td> <p>对于路径样式请求，值为<code>s3.amazonaws.com</code>。 对于虚拟样式请求，值为<code>BucketName.s3.amazonaws.com</code>。 有关详细信息，请参阅AWS文档中的<a href="https://docs.aws.amazon.com/AmazonS3/latest/dev/VirtualHosting.html">虚拟托管</a>。</p> <p>HTTP 1.1需要此标头（大多数工具包会自动添加此标头）；HTTP/1.0请求可以选择此标头。</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[！UICONTROL x-amz-content-sha256]</p> </td> 
       <td> <p>使用签名版本4对请求进行身份验证时，此标头提供请求有效负载的哈希。 以块形式上传对象时，将值设置为<code>STREAMING-AWS4-HMAC-SHA256-PAYLOAD</code>以指示签名仅涵盖标头并且没有有效负载。 有关详细信息，请参阅AWS文档中<a href="https://docs.aws.amazon.com/AmazonS3/latest/API/sigv4-streaming.html">授权标头</a>的签名计算。</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[！UICONTROL x-amz-date]</p> </td> 
       <td> <p>请求者的当前日期和时间。 示例： <code>Wed, 01 Mar 2006 12:00:00 GMT</code>。 指定<code>Authorization </code>标头时，必须指定<code>x-amz-date</code>或<code>Date </code>标头。 如果同时指定两者，则优先使用为<code>x-amz-date</code>标头指定的值。</p> </td> 
      </tr> 
      <tr> 
       <td role="rowheader"> <p>[！UICONTROL x-amz-security-token]</p> </td> 
       <td> <p>此标头可用于以下方案：</p> 
        <ul> 
         <li>为[!DNL Amazon DevPay]操作提供安全令牌。 使用[!DNL Amazon DevPay]的每个请求都需要两个<code>x-amz-security-token</code>标头：一个用于产品令牌，另一个用于用户令牌。 当[!DNL Amazon S3]收到经过身份验证的请求时，它将计算的签名与提供的签名进行比较。 用于计算签名的多值标头格式不正确可能会导致身份验证问题。</li> 
         <li>使用临时安全凭据时提供安全令牌。 使用从IAM获得的临时安全凭据发出请求时，必须使用此标头提供安全令牌。 要了解有关临时安全凭据的更多信息，请转到发出请求。</li> 
        </ul> <p>使用[!DNL Amazon DevPay]的请求和使用临时安全凭据签名的请求需要此标头。</p> </td> 
      </tr> 
     </tbody> 
    </table> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL查询字符串]</td> 
   <td> <p>添加所需的查询字符串，如参数或表单字段。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：   <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上载文件]

此操作模块会将文件上传到AWS S3存储段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL AWS]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-aws-to-workfront-fusion" class="MCXref xref">将[!DNL AWS]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL区域] </td> 
   <td> <p>选择您的区域端点。 有关详细信息，请参阅<a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">文档中的</a>区域端点[!DNL AWS]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL文件夹] </p> </td> 
   <td> <p>指定要上载文件的目标文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Headers]（可选）</p> </td> 
   <td> <p> 对于要添加的每个标头，单击<b>添加项</b>并输入标头的键和值。</p><p> 有关可用的标头，请参阅AWS文档中的<a href="https://docs.aws.amazon.com/AmazonS3/latest/API/API_PutObject.html">PutObject</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL 列出文件]](#list-files)
* [[!UICONTROL 列出文件夹]](#list-folders)

#### [!UICONTROL 列出文件]

从指定位置返回文件列表。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL AWS]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-aws-to-workfront-fusion" class="MCXref xref">将[!DNL AWS]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL区域] </td> 
   <td> <p>选择您的区域端点。 有关详细信息，请参阅<a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">文档中的</a>区域端点[!DNL AWS]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Bucket] </td> 
   <td> <p>选择要搜索文件的[!DNL Amazon S3]存储段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL前缀]</p> </td> 
   <td> <p> 输入要在其中查找文件的文件夹的路径，例如 <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出文件夹]

从指定位置返回文件夹列表。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL AWS]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-aws-to-workfront-fusion" class="MCXref xref">将[!DNL AWS]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL区域] </td> 
   <td> <p>选择您的区域端点。 有关详细信息，请参阅<a href="https://docs.aws.amazon.com/general/latest/gr/rande.html#regional-endpoints">文档中的</a>区域端点[!DNL AWS]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Bucket] </td> 
   <td> <p>选择要搜索文件夹的[!DNL Amazon S3]存储段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL前缀]（可选）</p> </td> 
   <td> <p> 要在其中查找文件夹的文件夹路径，例如 <code>workfrontfusion/work.</code></p> </td> 
  </tr> 
 </tbody> 
</table>
