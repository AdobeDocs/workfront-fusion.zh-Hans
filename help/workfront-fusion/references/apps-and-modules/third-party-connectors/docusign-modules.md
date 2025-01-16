---
title: DocuSign模块
description: 通过 [!DNL Adobe Workfront Fusion DocuSign] 模块，您可以监视和检索信封状态、搜索和检索信封，或者下载并发送文档以登录您的 [!DNL DocuSign] 帐户。
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '1632'
ht-degree: 0%

---

# DocuSign模块

通过[!DNL Adobe Workfront Fusion] [!DNL DocuSign]模块，您可以监视和检索信封状态、搜索和检索信封，或者下载并发送文档以登录您的[!DNL DocuSign]帐户。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## 先决条件

要使用[!DNL DocuSign]模块，您必须具有[!DNL DocuSign]帐户。

## DocuSign API信息

DocuSign连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>1.18.11</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL DocuSign]连接到[!DNL Workfront Fusion] {#connect-docusign-to-workfront-fusion}

要为您的[!DNL DocuSign]模块创建连接：

1. 开始配置第一个[!DNL DocuSign]模块时，单击[!UICONTROL Connection]框旁边的&#x200B;**[!UICONTROL Add]**。
1. 输入以下内容：

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>输入新[!DNL DocuSign]连接的名称</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Account type]</td> 
      <td>选择要连接的帐户是生产帐户还是演示帐户。</td> 
     </tr> 
    </tbody> 
   </table>

1. 按照[创建与 [!DNL Adobe Workfront Fusion] 的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md#connect)中的说明继续操作。

## [!DNL DocuSign]模块及其字段

配置[!DNL DocuSign]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL DocuSign]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)

### 触发器

#### [!UICONTROL Watch envelopes]

当信封被发送、投放、签署、完成或拒绝时，此触发器模块会启动一个场景。

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>选择包含要监视的记录的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event type]</td> 
   <td> <p> 选择要监视的事件类型。</p> 
    <ul> 
     <li>[!UICONTROL Document completed]</li> 
     <li>[!UICONTROL Document declined]</li> 
     <li>[!UICONTROL Document sent]</li> 
     <li>[!UICONTROL Document signed]</li> 
     <li>[!UICONTROL New document in Inbox]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Output fields]</p> </td> 
   <td> <p>选择要包含在模块输出中的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射每个方案执行周期中您希望模块使用的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download a document]](#download-a-document)
* [[!UICONTROL Read an envelope]](#read-an-envelope)
* [[!UICONTROL Upload a file to an envelope]](#upload-a-file-to-an-envelope)
* [[!UICONTROL Create a new envelope]](#create-a-new-envelope)
* [[!UICONTROL Add Recipient to Envelope]](#add-recipient-to-envelope)
* [[!UICONTROL Add custom field]](#add-custom-field)
* [[!UICONTROL Modify custom field]](#modify-custom-field)
* [[!UICONTROL Send envelope]](#send-envelope)

#### [!UICONTROL Custom API Call]

此操作模块允许您执行自定义API调用。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Account]</td> 
   <td>输入或映射要用于访问[!DNL DocuSign] API的帐户。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL]</td> 
   <td> <p>键入您希望模块与之交互的Web服务器上的地址。</p> <p>您可以键入相对URL，这意味着您不必在开头包含协议（如<code>http://</code>）。 这向Web服务器表明交互正在服务器上发生。</p> <p>例如： <code>[!DNL /api/conversations].create</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Method]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 这会确定请求的内容类型。</p> <p>例如，<code> {"Content-type":"application/json"}</code></p> <p>注意：如果您收到错误并且难以确定其来源，请考虑根据[!DNL Workfront]文档修改标头。 如果自定义API调用返回422 HTTP请求错误，请尝试使用“Content-Type”：“text/plain”标头。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query String]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>输入或映射在一个执行周期内要处理的最大结果数。</td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**示例：**&#x200B;列表信封
>
>以下API调用从您[!DNL DocuSign]帐户中的指定日期开始返回信封：
>
>**URL**： `/v2.1/accounts/{accountId}/envelopes/`
>
>**方法**： `GET`
>
>**查询字符串**：
>
>* **键**： `from_date`
>
>* **值**： `YYYY-MM-DD`
>
>指定请求何时开始检查帐户信封的状态更改。
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)
>
>可以在“包”>“主体”>“信封”下的模块输出中找到结果。
>
>在我们的示例中，返回了6个信封：
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

#### [!UICONTROL Download a document]

此操作模块下载单个文档。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>选择包含要下载的文档的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 输入或映射要下载的信封ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Document ID]</p> </td> 
   <td> <p>输入或映射要下载的文档的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Certificate]</td> 
   <td>如果要将信封签名证书包含在下载中，请选择<strong>[!UICONTROL Yes]</strong>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Documents by User ID]</td> 
   <td>如果要允许收件人按用户ID检索文档，请选择<strong>[!UICONTROL Yes]</strong>。 例如，如果将用户包括在具有不同可见性的两个不同的工艺路线订单中，则使用此选项将返回来自两个工艺路线的所有单据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Encrypt]</td> 
   <td>如果希望为在[!DNL DocuSign]帐户上配置的所有密钥管理器加密响应中返回的PDF字节，请选择<strong>[!UICONTROL Yes]</strong>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Language]</td> 
   <td>选择语言。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show Changes]</td> 
   <td>当设置为<strong>[!UICONTROL Yes]</strong>时，返回的PDF的任何更改字段都会以黄色突出显示，可选签名或缩写则以红色列出。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watermark]</td> 
   <td> <p>选择<strong>[!UICONTROL No]</strong>以从PDF文档中删除水印。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read an envelope]

此操作模块使用信封ID读取[!DNL DocuSign]中信封的相关信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>选择包含要从中读取信息的文档的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 输入或映射包含要从中读取信息的文档的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>选择要显示在模块输出中的属性。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file to an envelope]

此模块将指定的文件上传到DocuSign中的现有信封。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>选择包含要上载文件的信封的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 输入或映射要上载文件的信封的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>从以前的模块中选择源文件，或输入源文件的名称和数据。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a new envelope]

此操作模块从模板创建新信封。 它返回新信封的ID以及新信封的状态。

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!UICONTROL Connection] </td>

<td> <p>有关将DocuSign帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>下的文章。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Account] </td>
   <td> <p>选择包含要上载文件的信封的帐户。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template]</td>
   <td> <p> 选择要从中创建新信封的模板。 基于您选择的[!UICONTROL Account]有可用的模板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [!UICONTROL After creation]
   </td> 
   <td> <p>选择是将信封另存为草稿还是发送信封以供签名。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL Template recipients]</td>
    <td>选择此信封的收件人</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add Recipient to Envelope]

此操作模块将一个或多个收件人添加到现有信封。 如果信封已发送，则会向收件人发送电子邮件。 此模块对已完成的信封无效。

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Connection] </td>
   <td> <p>有关将DocuSign帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Account] </td>
   <td> <p>选择包含要添加收件人的信封的帐户。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Envelope ID]</td>
    <td>选择或映射要添加收件人的信封的ID。</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[!UICONTROL Recipient type]</td>
   <td> <p> 选择要添加到信封中的收件人类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL Agent]</p> </li> 
     <li> <p>[!UICONTROL Carbon copy]</p> </li> 
     <li> <p>[!UICONTROL Certified delivery]</p> </li> 
     <li> <p>[!UICONTROL In-person signer]</p> </li> 
     <li> <p>[!UICONTROL Intermediary]</p> </li> 
     <li> <p>[!UICONTROL Signer]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Email]</td>
   <td> <p>输入或映射要添加到信封的收件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Name]</td>
   <td>输入或映射要添加到信封的收件人名称。</td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Routing order]</td>
   <td> <p>输入或映射收件人的路由编号。 路由号码确定收件人接收和签署文档的顺序。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[!UICONTROL Email body]</td>
   <td>输入或映射发送给收件人的电子邮件正文（内容）。</td> 
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Email subject]</td>
   <td>输入或映射发送给收件人的电子邮件的主题。</td> 
  </tr> 
    <td role="rowheader">[!UICONTROL Private message]</td>
   <td> <li> <p>只有选定的收件人会看到该私人邮件以及常规邮件。 私密消息长度限制为1000个字符。</p> </li> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Authentication]</td> 
   <td> <p>选择要用于确认收件人身份的身份验证方法。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL None]</strong> </p> </li> 
     <li> <p><strong>[!UICONTROL Access code]</strong> </p> <p>输入或映射访问代码。</p> </li> 
     <li> <p><strong>[!UICONTROL Phone]</strong> </p> <p>输入或映射电话号码</p> </li> 
     <li> <p><strong>[!UICONTROL SMS]</strong> </p> <p>输入或映射电话号码</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add custom field]

此操作模块向文档添加自定义字段

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>选择包含要添加自定义字段的文档的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 输入或映射包含要添加自定义字段的文档的信封的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>为要添加的新字段输入或映射名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>如果您希望添加的字段为必填字段，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>如果您希望字段可见，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>输入或映射添加字段的值（内容）。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify custom field]

此操作模块使用字段名称修改自定义字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>选择包含要修改自定义字段的文档的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 输入或映射包含要修改自定义字段的文档的信封的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field ID]</td> 
   <td>输入或映射要修改的字段的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field name]</td> 
   <td>输入或映射要修改的字段的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Required]</td> 
   <td>如果希望修改的字段为必填字段，则启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show field]</td> 
   <td>如果您希望字段可见，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value]</td> 
   <td>输入或映射已修改字段的值（内容）。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send envelope]

该操作模块会向其收件人发送草稿信封。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Account] </td> 
   <td> <p>选择包含要发送给其收件人的草稿信封的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Envelope ID]</td> 
   <td> <p> 输入或映射要发送给其收件人的草稿信封的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>
