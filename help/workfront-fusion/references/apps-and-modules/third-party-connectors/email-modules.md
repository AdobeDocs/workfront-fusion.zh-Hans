---
title: 电子邮件模块
description: 在Adobe Workfront Fusion场景中，您可以将电子邮件帐户连接到多个第三方应用程序和服务。这使您能够通过IMAP下载电子邮件、通过SMTP发送电子邮件、创建新草稿、将电子邮件从一个文件夹移动和复制到另一个文件夹、将电子邮件标记为已读或未读以及删除电子邮件。
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2485'
ht-degree: 0%

---

# 电子邮件模块

在Adobe Workfront Fusion场景中，您可以将电子邮件帐户连接到多个第三方应用程序和服务。这使您能够通过IMAP下载电子邮件、通过SMTP发送电子邮件、创建新草稿、将电子邮件从一个文件夹移动和复制到另一个文件夹、将电子邮件标记为已读或未读以及删除电子邮件。

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

## 将电子邮件连接到Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [连接到Google](#connect-to-google)
* [连接到其他电子邮件服务(IMAP)](#connect-to-other-email-services-smap)

### 连接到[!DNL Google]

使用此选项创建需要连接到[!DNL Google]帐户的电子邮件模块的方案。 这是具有受限范围的帐户。

您可以在电子邮件模块中直接创建与[!DNL Google]帐户的连接。

1. 在任何电子邮件模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
1. 选择&#x200B;**[!DNL Google]**&#x200B;作为连接类型。
1. 输入连接的名称。
1. （可选）输入您的[!UICONTROL [!DNL Google]客户端ID]和[!UICONTROL 客户端密钥]。
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

### 连接到其他电子邮件服务(IMAP)

IMAP连接允许您远程访问邮箱，并读取或处理邮箱中的邮件。 大多数电子邮件模块都使用IMAP连接。

1. 在任何电子邮件模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
1. 选择&#x200B;**[!UICONTROL 其他(SMTP)]**&#x200B;作为连接类型。
1. 输入连接的&#x200B;**[!UICONTROL 名称]**。
1. 从列表中选择您的&#x200B;**[!UICONTROL 电子邮件提供商]**。 如果您的电子邮件提供商不在列表中，请选择“其他”。
1. 输入电子邮件帐户的&#x200B;**[!UICONTROL 用户名]**&#x200B;和您的&#x200B;**[!UICONTROL 密码]**。
1. （视情况而定）如果您的提供商不在列表中，请输入您的&#x200B;**[!UICONTROL SMTP服务器]**&#x200B;和&#x200B;**[!UICONTROL 端口]**，并指定是否要&#x200B;**[!UICONTROL 使用安全连接(TLS)]**。 若要查找此信息，请查看邮箱的[!UICONTROL 帮助]部分。 如果您没有此信息，请与您的电子邮件服务提供商联系。
1. 若要使用自签名证书，请启用&#x200B;**拒绝未经授权的证书**&#x200B;选项并上传您的自签名证书。 有关说明，请参阅[上传自签名证书](#upload-a-self-signed-certificate)
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

#### 上传自签名证书

要添加自签名证书，请执行以下操作：

1. 单击&#x200B;**提取**。
1. 选择要提取的文件类型。
1. 选择包含或证书的文件。
1. 输入文件的密码。
1. 单击&#x200B;**保存**&#x200B;以提取文件并返回模块设置。

## [!UICONTROL 电子邮件]模块及其字段

在配置[!UICONTROL 电子邮件]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，还可能会显示其他字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

某些电子邮件字段可能包含数据，因为您在场景的其他模块中使用了这些数据。 如需有关这些受众的信息，请参阅电子邮件帮助文档。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>称为“[!UICONTROL 电子邮件ID (UID)]”的唯一电子邮件ID是电子邮件的标识符。 电子邮件ID特定于每个电子邮件的文件夹。

* [触发器](#triggers)
* [操作](#actions)
* [迭代器](#iterators)

### 触发器

#### [!UICONTROL 观看电子邮件]

在收到根据指定条件处理的新电子邮件时，此触发器模块会启动一个方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[！UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件夹] </td> 
   <td> <p>选择包含要监视的电子邮件的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL标准]</p> </td> 
   <td> <p>选择要按其监视电子邮件的标准：</p> 
    <ul> 
     <li>[！UICONTROL所有电子邮件]</li> 
     <li>[！UICONTROL仅读取电子邮件]</li> 
     <li>[！UICONTROL Only未读电子邮件]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL发件人电子邮件地址] </td> 
   <td> <p>输入要监视其电子邮件的发件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL主题] </td> 
   <td> <p>输入要监视的电子邮件的主题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL短语] </td> 
   <td> <p>输入任意关键字以仅查看包含该关键字的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL在获取时将消息标记为已读]</td> 
   <td> <p>启用此选项可在检索详细信息后将未读电子邮件标记为已读。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL最大结果数]</td> 
   <td> <p> 输入或映射Workfront Fusion在一个场景执行周期内应返回的最大电子邮件数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 复制电子邮件]](#copy-an-email)
* [[!UICONTROL 创建草稿]](#create-a-draft)
* [[!UICONTROL 删除电子邮件]](#delete-an-email)
* [[!UICONTROL 获取电子邮件]](#get-emails)
* [[!UICONTROL 将电子邮件标记为已读]](#mark-an-email-as-read)
* [[!UICONTROL 将电子邮件标记为未读]](#mark-an-email-as-unread)
* [[!UICONTROL 移动电子邮件]](#move-an-email)
* [[!UICONTROL 发送电子邮件]](#send-an-email)

#### [!UICONTROL 复制电子邮件]

此操作模块将电子邮件或草稿复制到选定的文件夹中。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[！UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[！UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source文件夹]</td> 
   <td>选择要从中复制电子邮件的文件夹。 示例： Primary。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL目标文件夹]</td> 
   <td> <p> 选择要将电子邮件复制到其中的文件夹。 示例：工作。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL电子邮件ID (UID)]</p> </td> 
   <td> <p>输入要复制到目标文件夹的电子邮件的Email UID。</p> <p>可以使用[！UICONTROL Email] &gt; [！UICONTROL Watch Email]模块或[！UICONTROL Search Email]模块获取电子邮件的UID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建草稿]

此操作模块将创建新的草稿并将其添加到选定的文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[！UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[！UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件夹]</td> 
   <td>选择要创建草稿电子邮件的文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL至] </td> 
   <td> <p>输入或映射要向其发送电子邮件的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL主题] </td> 
   <td> <p>输入或映射电子邮件的主题行。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL内容] </td> 
   <td> <p>使用HTML标记以HTML格式或以纯文本输入或映射电子邮件内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL附件]</p> </td> 
   <td> <p>对于要添加的每个附件，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL文件名]</strong> </p> <p>输入文件名，包括扩展名。 </p> </li> 
     <li> <p><strong>[！UICONTROL数据]</strong> </p> <p>输入要上载附件的文件夹的路径。</p> </li> 
     <li> <p><strong>[！UICONTROL Content-ID]</strong> </p> <p>输入内容ID以在内容中插入附件（图像）。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL复制收件人] </td> 
   <td> <p>对于要向其发送此电子邮件副本的每个电子邮件地址，单击“添加项目”<b></b>并输入电子邮件地址。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL盲文复制收件人]</td> 
   <td> <p> 对于要向其发送此电子邮件的副本而不在电子邮件中显示的所有电子邮件地址，单击“<b>添加项</b>”并输入电子邮件地址。</p> </td> 
  </tr> 
  <!--<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Enter or map the email address (and name, if needed) that appears in the [!UICONTROL From] field in the email. </p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code>.</p> <p>Note:  Normally, Workfront Fusion uses the email address that you entered when creating the connection as the sender address. If you enter any other email address, an error may occur when sending a message because your account may not have permission to send emails from a different address than your own. E.g. <code>test@mail.com</code> or "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Enter or map the email address that appears in the [!UICONTROL Sender] field in the email.</p> <p>Tip:  If you are unsure whether to use this field or the From field, we recommend choosing the From field.</p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> If you want replies to this email sent to a different address than the "[!UICONTROL from]" address, enter the email address where you want replies to this email sent.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> If you are replying to a specific email, enter or map the ID of the email you are replying to.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Enter the message IDs of all the replies in the thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Select the priority of the email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Add the headers:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Add the key. For example, Sender, Date, To, and so on.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter the value for the key.</p> </li> 
    </ul> </td> 
  </tr> -->
 </tbody> 
</table>

#### [!UICONTROL 删除电子邮件]

此操作模块可从所选文件夹中删除电子邮件或草稿。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[！UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[！UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件夹]</td> 
   <td>选择包含要删除的电子邮件的文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL电子邮件ID (UID)]</p> </td> 
   <td> <p>输入要删除的电子邮件的电子邮件UID 。</p> <p>您可以使用“电子邮件”&gt;“监视电子邮件”模块或[！UICONTROL搜索电子邮件]模块获取电子邮件的UID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL消除]</td> 
   <td> <p>启用此选项可永久删除当前打开邮箱中标记为[！UICONTROL已删除]的所有邮件。</p> <p>注意：在[!DNL Gmail]中，此行为由[！UICONTROL设置] &gt;[！UICONTROL IMAP访问中的转发POP/IMAP]部分中的设置驱动。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取电子邮件]

此模块会返回符合指定条件的电子邮件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[！UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[！UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件夹] </td> 
   <td> <p>选择包含要检索的电子邮件的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL在获取时将消息标记为已读] </td> 
   <td> <p>如果要在检索详细信息后将未读电子邮件标记为已读，请启用此选项。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL标准]</p> </td> 
   <td> <p>选择要检索的电子邮件的条件：</p> 
    <ul> 
     <li>[！UICONTROL所有电子邮件]</li> 
     <li>[！UICONTROL仅读取电子邮件]</li> 
     <li>[！UICONTROL Only未读电子邮件]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL发件人电子邮件地址] </td> 
   <td> <p>输入或映射要检索其电子邮件的发件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL收件人电子邮件]</td> 
   <td> <p> 输入或映射要检索其电子邮件的收件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL起始日期] </td> 
   <td> <p>输入或映射日期，以检索在指定日期或该日期之后处理的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Before Date]</td> 
   <td> <p> 输入或映射日期，以检索在指定日期或之前处理的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL主题] </td> 
   <td> <p>输入或映射要检索的电子邮件主题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL短语] </td> 
   <td> <p>输入或映射任何关键字以仅检索包含这些关键字的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL电子邮件ID (UID)]</td> 
   <td> <p> 输入要检索其详细信息的电子邮件的电子邮件ID (UID)。</p> <p>您可以使用Workfront Fusion的[！UICONTROL Watch Email]模块或[！UICONTROL Search Email]模块获取电子邮件的UID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL最大结果数]</td> 
   <td> <p> Workfront Fusion应在一个场景执行周期内返回的最大电子邮件数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL即使模块未返回任何结果，仍继续执行路由]</td> 
   <td> <p> 选择是否要在没有返回结果的情况下继续运行模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 将电子邮件标记为已读]

此操作模块通过设置[!UICONTROL Read]标志，将所选文件夹中的电子邮件或草稿标记为已读。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[！UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[！UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件夹]</td> 
   <td>选择包含要标记为已读电子邮件的文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL电子邮件ID (UID)]</p> </td> 
   <td> <p>输入要标记为已读的电子邮件的电子邮件UID 。</p> <p>您可以使用“电子邮件”&gt;“监视电子邮件”模块或[！UICONTROL搜索电子邮件]模块获取电子邮件的UID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 将电子邮件标记为未读]

通过设置未读标志，将所选文件夹中的电子邮件或草稿标记为未读。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[！UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[！UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件夹]</td> 
   <td>选择包含要标记为未读电子邮件的文件夹。 示例： Primary。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL电子邮件ID (UID)]</p> </td> 
   <td> <p>输入要标记为未读的电子邮件的Email UID。</p> <p>您可以使用“电子邮件”&gt;“监视电子邮件”模块或[！UICONTROL搜索电子邮件]模块获取电子邮件的UID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 移动电子邮件]

将所选电子邮件或草稿移动到所选文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[！UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[！UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source文件夹]</td> 
   <td>选择包含要移动的电子邮件的文件夹。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL目标文件夹]</td> 
   <td> <p> 选择要向其中添加电子邮件的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL电子邮件ID (UID)]</p> </td> 
   <td> <p>输入要移动到目标文件夹的电子邮件的Email UID。</p> <p>您可以使用“电子邮件”&gt;“监视电子邮件”模块或[！UICONTROL搜索电子邮件]模块获取电子邮件的UID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 发送电子邮件]

发送新电子邮件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL发送后保存消息]</td> 
   <td>发送电子邮件后，该邮件将保存在您的邮箱中。 如果要将使用Workfront Fusion发送的电子邮件保存到<i>[！UICONTROL已发送邮件]</i>文件夹或邮箱中的其他文件夹，请启用此选项。 某些电子邮件服务（如[!DNL Gmail]）会自动保存已发送的邮件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL至] </td> 
   <td> <p>添加要向其发送电子邮件的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL主题] </td> 
   <td> <p>输入或映射电子邮件的主题行。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL内容类型]</p> </td> 
   <td> <p>选择电子邮件的[！UICONTROL content]类型：</p> 
    <ul> 
     <li>HTML</li> 
     <li>[！UICONTROL纯文本]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL内容] </td> 
   <td> <p>使用HTML标签以HTML格式或以纯文本输入或映射电子邮件内容，具体取决于您在[！UICONTROL内容类型]字段中选择的内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL附件]</p> </td> 
   <td> <p>对于要添加的每个附件，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL文件名]</strong> </p> <p>输入文件名，包括扩展名。 </p> </li> 
     <li> <p><strong>[！UICONTROL数据]</strong> </p> <p>输入要上载附件的文件夹的路径。</p> </li> 
     <li> <p><strong>[！UICONTROL Content-ID]</strong> </p> <p>输入内容ID以在内容中插入附件（图像）。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL复制收件人] </td> 
   <td> <p>对于要向其发送此电子邮件副本的每个电子邮件地址，单击“添加项目”<b></b>并输入电子邮件地址。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL盲文复制收件人]</td> 
   <td> <p> 对于要向其发送此电子邮件的副本而不在电子邮件中显示的所有电子邮件地址，单击“<b>添加项</b>”并输入电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL发件人]</p> </td> 
   <td> <p>输入或映射电子邮件的[！UICONTROL Sender]字段中显示的电子邮件地址。</p> <p>提示：如果您不确定是使用此字段还是从字段，我们建议您选择从字段。</p> <p>重要提示：使用正确的语法： <code>name@email.com</code>或 <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL回复]</td> 
   <td> <p> 如果要将对此电子邮件的回复发送到与“发件人”地址不同的地址，请输入要用于对此电子邮件进行回复的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL In-Reply-To]</td> 
   <td> <p> 如果回复的是特定电子邮件，请输入或映射要回复的电子邮件的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL引用] </td> 
   <td> <p>输入线程中所有回复的消息ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL优先级]</p> </td> 
   <td> <p>选择电子邮件的优先级：</p> 
    <ul> 
     <li>[！UICONTROL高]</li> 
     <li>[！UICONTROL正常]</li> 
     <li>[！UICONTROL低]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Headers]</p> </td> 
   <td> <p>添加标头：</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL键]</strong> </p> <p>添加键。 例如，[！UICONTROL Sender]、[！UICONTROL Date]、[！UICONTROL To]等。</p> </li> 
     <li> <p><strong>[！UICONTROL值]</strong> </p> <p>输入键的值。</p> </li> 
    </ul> </td> 
  </tr> 
<tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL From] </td> 
   <td> <p>输入或映射电子邮件的[！UICONTROL发件人]字段中显示的电子邮件地址（和名称，如果需要）。 </p> <p>重要：使用正确的语法： <code>name@email.com</code>或<code>"Name" name@email.com</code>。</p> <p>注意：通常，Workfront Fusion会将您在创建连接时输入的电子邮件地址用作发件人地址。 如果输入任何其他电子邮件地址，则在发送邮件时可能会发生错误，因为您的帐户可能无权从不同于您自己的地址发送电子邮件。 如<code>test@mail.com</code>或“<code>John Bush" test@email.com</code>”。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 迭代器

#### [!UICONTROL 迭代附件]

逐个接收附件。

电子邮件迭代器模块允许您单独管理电子邮件附件。 例如，您可以设置监视电子邮件，对带有附件的电子邮件进行迭代并接收警报。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source module]</td> 
   <td> <p>选择用于输出带有要对其进行迭代的附件的电子邮件的模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

有关迭代器的详细信息，请参阅[迭代器模块](/help/workfront-fusion/references/modules/iterator-module.md)。
