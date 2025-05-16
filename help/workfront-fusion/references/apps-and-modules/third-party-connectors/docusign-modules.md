---
title: DocuSign模块
description: 通过 [!DNL Adobe Workfront Fusion DocuSign] 模块，您可以监视和检索信封状态、搜索和检索信封，或者下载并发送文档以登录您的 [!DNL DocuSign] 帐户。
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: 94a823a6-3c70-42a1-b6cf-298591dbca15
source-git-commit: 2b2030d062b5ec8c81476a8950fee3b15f96dcd2
workflow-type: tm+mt
source-wordcount: '2200'
ht-degree: 0%

---

# DocuSign模块

通过[!DNL Adobe Workfront Fusion] [!DNL DocuSign]模块，您可以监视和检索信封状态、搜索和检索信封，或者下载并发送文档以登录您的[!DNL DocuSign]帐户。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

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

1. 开始配置第一个[!DNL DocuSign]模块时，单击[!UICONTROL 连接]框旁边的&#x200B;**[!UICONTROL 添加]**。
1. 输入以下内容：

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL连接名称]</p> </td> 
      <td>输入新[!DNL DocuSign]连接的名称。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL环境]</p> </td> 
      <td>选择是否连接到非生产环境中的生产。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL连接名称]</p> </td> 
      <td>选择您是要连接到服务帐户还是个人帐户。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL帐户类型]</td> 
      <td>选择要连接的帐户是生产帐户还是演示帐户。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**继续**&#x200B;保存连接并返回模块。

## [!DNL DocuSign]模块及其字段

配置[!DNL DocuSign]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL DocuSign]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)

### 触发器

#### [!UICONTROL 观看信封]

当信封被发送、投放、签署、完成或拒绝时，此触发器模块会启动一个场景。

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将Docusign连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL帐户] </td> 
   <td> <p>选择包含要监视的记录的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL事件类型]</td> 
   <td> <p> 选择要监视的事件类型。</p> 
    <ul> 
     <li>[！UICONTROL文档已完成]</li> 
     <li>[！UICONTROL文档已拒绝]</li> 
     <li>[！UICONTROL文档已发送]</li> 
     <li>[！UICONTROL文档已签名]</li> 
     <li>[！UICONTROL收件箱中的新文档]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL输出]</p> </td> 
   <td> <p>选择要包含在模块输出中的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td>输入或映射每个方案执行周期中您希望模块使用的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 添加自定义字段]](#add-a-custom-field)
* [[!UICONTROL 将收件人添加到信封]](#add-recipient-to-envelope)
* [[!UICONTROL 新建信封]](#create-a-new-envelope)
* [[!UICONTROL 自定义API调用]](#custom-api-call)
* [[!UICONTROL 下载文档]](#download-a-document)
* [[!UICONTROL 修改自定义字段]](#modify-custom-field)
* [[!UICONTROL 读取信封]](#read-an-envelope)
* [[!UICONTROL 发送信封]](#send-envelope)
* [[!UICONTROL 将文件上载到信封]](#upload-a-file-to-an-envelope)

#### [!UICONTROL 添加自定义字段]

此操作模块向文档添加自定义字段

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL帐户] </td> 
   <td> <p>选择包含要添加自定义字段的文档的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL信封ID]</td> 
   <td> <p> 输入或映射包含要添加自定义字段的文档的信封的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL字段名称]</td> 
   <td>为要添加的新字段输入或映射名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL必填]</td> 
   <td>如果您希望添加的字段为必填字段，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示字段]</td> 
   <td>如果您希望字段可见，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL值]</td> 
   <td>输入或映射添加字段的值（内容）。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 将收件人添加到信封]

此操作模块将一个或多个收件人添加到现有信封。 如果信封已发送，则会向收件人发送电子邮件。 此模块对已完成的信封无效。

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr data-mc-conditions=""> 
    <td>[！UICONTROL Connection] </td>
   <td> <p>有关将DocuSign帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[！UICONTROL帐户] </td>
   <td> <p>选择包含要添加收件人的信封的帐户。</p> </td> 
  </tr> 
  <tr> 
    <td>[！UICONTROL信封ID]</td>
    <td>选择或映射要添加收件人的信封的ID。</td>
  </tr> 
  <tr data-mc-conditions="">
    <td role="rowheader">[！UICONTROL收件人类型]</td>
   <td> <p> 选择要添加到信封中的收件人类型。</p> 
    <ul> 
     <li> <p>[！UICONTROL Agent]</p> </li> 
     <li> <p>[！UICONTROL Carbon copy]</p> </li> 
     <li> <p>[！UICONTROL认证交付]</p> </li> 
     <li> <p>[！UICONTROL现场签名者]</p> </li> 
     <li> <p>[！UICONTROL Intermediate]</p> </li> 
     <li> <p>[！UICONTROL签名者]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td>[！UICONTROL电子邮件]</td>
   <td> <p>输入或映射要添加到信封的收件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
    <td>[！UICONTROL名称]</td>
   <td>输入或映射要添加到信封的收件人名称。</td> 
  </tr> 
  <tr>
    <td>[！UICONTROL路由顺序]</td>
   <td> <p>输入或映射收件人的路由编号。 路由号码确定收件人接收和签署文档的顺序。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[！UICONTROL电子邮件正文]</td>
   <td>输入或映射发送给收件人的电子邮件的正文（内容）。</td> 
  </tr> 
  <tr>
    <td role="rowheader">[！UICONTROL电子邮件主题]</td>
   <td>输入或映射发送给收件人的电子邮件的主题。</td> 
  </tr> 
    <td role="rowheader">[！UICONTROL私人消息]</td>
   <td> 如果要向收件人发送私人邮件，请输入或映射邮件的文本。 <p>只有选定的收件人会看到该私人邮件以及常规邮件。 私密消息长度限制为1000个字符。</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Authentication]</td> 
   <td> <p>选择要用于确认收件人身份的身份验证方法。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL无]</strong> </p> </li> 
     <li> <p><strong>[！UICONTROL访问代码]</strong> </p> <p>输入或映射访问代码。</p> </li> 
     <li> <p><strong>[！UICONTROL Phone]</strong> </p> <p>输入或映射电话号码。</p> </li> 
     <li> <p><strong>[！UICONTROL短信]</strong> </p> <p>输入或映射电话号码。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 新建信封]

此操作模块从模板创建新信封。 它返回新信封的ID以及新信封的状态。

<table style="table-layout:auto">
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td role="rowheader">[！UICONTROL Connection] </td>

<td> <p>有关将DocuSign帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>下的文章。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader">[！UICONTROL帐户] </td>
   <td> <p>选择包含要上载文件的信封的帐户。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL模板]</td>
   <td> <p> 选择要从中创建新信封的模板。 根据您选择的[！UICONTROL帐户]，可以使用模板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL创建后]
   </td> 
   <td> <p>选择是将信封另存为草稿还是发送信封以供签名。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL模板收件人]</td>
    <td>对于要添加到此信封的每个收件人，单击<b>添加项</b>并输入以下详细信息：
    <ul>
    <li><b>访问代码</b><p>输入或映射收件人用于访问信封的代码。<p></li>
    <li><b>电子邮件</b><p>输入或映射收件人的电子邮件地址。<p></li>
    <li><b>名称</b><p>输入或映射收件人的名称。<p></li>
    <li><b>角色名称</b><p>输入或映射收件人的角色名称。<p></li>
    <li><b>路由顺序</b><p>输入或映射收件人的路由编号。 路由号码确定收件人接收和签署文档的顺序。<p></li>
    </ul>
    </td>
    </tr>
  <tr> 
   <td role="rowheader">
     [！UICONTROL Allow Print and Sign]
   </td> 
   <td> <p>启用此选项可允许收件人打印文档并签署纸张。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL允许重新分配]
   </td> 
   <td> <p>如果希望收件人能够将文档重新分配给其他用户，请启用此选项。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL允许收件人递归]
   </td> 
   <td> <p>启用此选项以允许收件人递归。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL权威副本]
   </td> 
   <td> <p>启用此选项可将此信封中的文档标记为授权副本。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL自动导航]
   </td> 
   <td> <p>启用此选项可设置收件人的自动导航。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL品牌ID]
   </td> 
   <td> <p>输入或映射品牌的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL标记已启用]
   </td> 
   <td> <p>启用此选项以启用文档标记。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL过期已启用]
   </td> 
   <td> <p>启用此选项可设置此信封的过期时间。 如果启用此选项，请填写以下字段：<ul><li><b>过期时间</b><p>输入或映射此信封过期的天数。</p></li><li><b>过期警告</b><p>输入或映射向收件人发送提醒电子邮件之前的天数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL Body]
   </td> 
   <td> <p>输入或映射此信封随附的电子邮件的正文（内容）。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">
     [！UICONTROL主题]
   </td> 
   <td> <p>输入或映射此信封随附的电子邮件的主题。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义API调用]

此操作模块允许您执行自定义API调用。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL帐户]</td> 
   <td>输入或映射要用于访问[!DNL DocuSign] API的帐户。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL URL]</td> 
   <td> <p>输入或映射相对路径 <code>https://&lt;BASE_URI>/v2/accounts/&lt;ACCOUNT_ID>.</code></p>  </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 这会确定请求的内容类型。</p> <p>例如，<code> {"Content-type":"application/json"}</code></p> <p>注意：如果您收到错误并且难以确定其来源，请考虑根据[!DNL Workfront]文档修改标头。 如果自定义API调用返回422 HTTP请求错误，请尝试使用“Content-Type”：“text/plain”标头。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL限制]</td> 
   <td>输入或映射在一个执行周期内要处理的最大结果数。</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**&#x200B;列表信封

以下API调用从您[!DNL DocuSign]帐户中的指定日期开始返回信封：

**URL**： `/v2.1/accounts/{accountId}/envelopes/`

**方法**： `GET`

**查询字符串**：

* **键**： `from_date`

* **值**： `YYYY-MM-DD`

指定请求何时开始检查帐户信封的状态更改。

![示例Docusign设置](/help/workfront-fusion/references/apps-and-modules/assets/example-docusign-setup-350x770.png)

可以在“包”>“主体”>“信封”下的模块输出中找到结果。

在我们的示例中，返回了6个信封：

![示例docusign输出](/help/workfront-fusion/references/apps-and-modules/assets/docusign-example-output-350x677.png)

>[!ENDSHADEBOX]

#### [!UICONTROL 下载文档]

此操作模块下载单个文档。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL帐户] </td> 
   <td> <p>选择包含要下载的文档的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL信封ID]</td> 
   <td> <p> 输入或映射要下载的信封ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL文档ID]</p> </td> 
   <td> <p>输入或映射要下载的文档的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL证书]</td> 
   <td>启用此选项以在下载中包含信封签名证书。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文档（按用户ID）</td> 
   <td>启用此选项可允许收件人按用户ID检索文档。 例如，如果将用户包括在具有不同可见性的两个不同的工艺路线订单中，则使用此选项将返回来自两个工艺路线的所有单据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL加密]</td> 
   <td>如果希望为[!DNL DocuSign]帐户上配置的所有密钥管理器加密响应中返回的PDF字节，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL语言]</td> 
   <td>选择语言。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示更改]</td> 
   <td>启用此选项以突出显示返回的PDF的任何更改字段，并以黄色突出显示可选签名或缩写符号。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL水印]</td> 
   <td> <p>启用此选项可启用水印功能。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 修改自定义字段]

此操作模块使用字段名称修改自定义字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL帐户] </td> 
   <td> <p>选择包含要修改自定义字段的文档的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL信封ID]</td> 
   <td> <p> 输入或映射包含要修改自定义字段的文档的信封的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL字段ID]</td> 
   <td>输入或映射要修改的字段的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL字段名称]</td> 
   <td>输入或映射要修改的字段的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL必填]</td> 
   <td>如果希望修改的字段为必填字段，则启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示字段]</td> 
   <td>如果您希望字段可见，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL值]</td> 
   <td>输入或映射已修改字段的值（内容）。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取信封]

此操作模块使用信封ID读取[!DNL DocuSign]中信封的相关信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL帐户] </td> 
   <td> <p>选择包含要从中读取信息的文档的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL信封ID]</td> 
   <td> <p> 输入或映射包含要从中读取信息的文档的信封的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td>选择要显示在模块输出中的属性。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 发送信封]

该操作模块会向其收件人发送草稿信封。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL帐户] </td> 
   <td> <p>选择包含要发送给其收件人的草稿信封的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL信封ID]</td> 
   <td> <p> 输入或映射要发送给其收件人的草稿信封的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 将文件上载到信封]

此模块将指定的文件上传到DocuSign中的现有信封。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL DocuSign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-docusign-to-workfront-fusion" class="MCXref xref">将[!DNL DocuSign]连接到[!DNL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL帐户] </td> 
   <td> <p>选择包含要上载文件的信封的帐户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL信封ID]</td> 
   <td> <p> 输入或映射要上载文件的信封的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td>从以前的模块中选择源文件，或输入源文件的名称和数据。</td> 
  </tr> 
 </tbody> 
</table>
