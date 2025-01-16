---
title: 电子邮件模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，可以将电子邮件帐户连接到多个第三方应用程序和服务。这允许您通过IMAP下载电子邮件、通过SMTP发送电子邮件、创建新草稿、将电子邮件从一个文件夹移动和复制到另一个文件夹、将电子邮件标记为已读或未读以及删除电子邮件。
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2103'
ht-degree: 0%

---

# 电子邮件模块

在[!DNL Adobe Workfront Fusion]方案中，您可以将电子邮件帐户连接到多个第三方应用程序和服务。这允许您通过IMAP下载电子邮件、通过SMTP发送电子邮件、创建新草稿、将电子邮件从一个文件夹移动和复制到另一个文件夹、将电子邮件标记为已读或未读以及删除电子邮件。

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

## 将电子邮件连接到Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [连接到Google](#connect-to-google)
* [连接到其他电子邮件服务(SMAP)](#connect-to-other-email-services-smap)

### 连接到[!DNL Google]

使用此选项创建需要连接到[!DNL Google]帐户的电子邮件模块的方案。 这是具有受限范围的帐户。

您可以在电子邮件模块中直接创建与[!DNL Google]帐户的连接。

1. 在任何电子邮件模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 选择&#x200B;**[!DNL Google]**&#x200B;作为连接类型。
1. 输入连接的名称。
1. （可选）输入您的[!UICONTROL [!DNL Google] Client ID]和[!UICONTROL Client Secret]。
1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。

### 连接到其他电子邮件服务(SMAP)

SMAP连接允许您远程访问邮箱，并读取或处理邮箱中的邮件。 大多数电子邮件模块都使用SMAP连接。

1. 在任何电子邮件模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 选择&#x200B;**[!UICONTROL Others (SMTP)]**&#x200B;作为连接类型。
1. 输入连接的&#x200B;**[!UICONTROL Name]**。
1. 从列表中选择您的&#x200B;**[!UICONTROL Email provider]**。 如果您的电子邮件提供商不在列表中，请选择“其他”。
1. 输入您的&#x200B;**[!UICONTROL Email address]**、**[!UICONTROL Your full name]**、**[!UICONTROL User name]**&#x200B;和&#x200B;**[!UICONTROL Password]**。
1. （视情况而定）如果您的提供商不在列表中，请输入您的&#x200B;**[!UICONTROL SMTP server]**&#x200B;和&#x200B;**[!UICONTROL Port]**，并指定是否要&#x200B;**[!UICONTROL Use a secure connection (TLS)]**。 若要查找此信息，请检查邮箱的[!UICONTROL Help]部分。 如果您没有此信息，请与您的电子邮件服务提供商联系。
1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。

## [!UICONTROL Email]模块及其字段

配置[!UICONTROL Email]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，还可能会显示其他字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

某些电子邮件字段可能包含数据，因为您在场景的其他模块中使用了这些数据。 如需有关这些受众的信息，请参阅电子邮件帮助文档。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>称为“[!UICONTROL Email ID (UID)]”的唯一电子邮件ID是电子邮件的标识符。 电子邮件ID特定于每个电子邮件的文件夹。

* [触发器](#triggers)
* [操作](#actions)
* [迭代器](#iterators)

### 触发器

#### [!UICONTROL Watch Emails]

在收到新电子邮件并根据指定条件进行处理时触发。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>选择包含要监视的电子邮件的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>选择要按其监视电子邮件的标准：</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>输入要监视其电子邮件的发件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email Address]</td> 
   <td> <p> 输入要监视其电子邮件的收件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>输入要监视的电子邮件的主题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>输入任意关键字以仅查看包含特定短语的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched]</td> 
   <td> <p>启用此选项可在检索详细信息后将未读电子邮件标记为已读。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> 在一个方案执行周期内应返回的最大电子邮件数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Send an Email]](#send-an-email)
* [[!UICONTROL Create a Draft]](#create-a-draft)
* [[!UICONTROL Mark an Email as Read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an Email as Unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an Email]](#move-an-email)
* [[!UICONTROL Copy an Email]](#copy-an-email)
* [[!UICONTROL Delete an Email]](#delete-an-email)
* [[!UICONTROL Get Emails]](#get-emails)

#### [!UICONTROL Send an Email]

发送新电子邮件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save Message after Sending]</td> 
   <td>发送电子邮件后，该邮件将保存在您的邮箱中。 如果要将使用[!DNL Workfront Fusion]发送的电子邮件保存到<i>[!UICONTROL Sent mail]</i>文件夹或邮箱中的其他文件夹，请启用此选项。 某些电子邮件服务（如[!DNL Gmail]）会自动保存已发送的邮件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>添加要向其发送电子邮件的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>输入或映射电子邮件的主题行。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>为电子邮件选择[!UICONTROL content]类型：</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plaintext]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>使用HTML标签以HTML格式输入或映射电子邮件内容，或者以纯文本输入或映射电子邮件内容，具体取决于您在[!UICONTROL Content Type]字段中选择的内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>添加附件：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>输入文件名。 例如， sample.doc。</p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>输入要上载附件的文件夹的路径。</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>输入[!UICONTROL content ID]以在内容中插入附件（图像）。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>输入或映射要向其发送此电子邮件副本的一个或多个电子邮件地址。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> 输入或映射您要向其发送此电子邮件副本的一个或多个电子邮件地址，而不在电子邮件中显示该电子邮件地址。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>输入或映射电子邮件中[!UICONTROL From]字段中显示的电子邮件地址（和名称，如果需要）。 </p> <p>重要：使用正确的语法： <code>name@email.com</code>或<code>"Name" name@email.com</code>。</p> <p>注意：通常，[!DNL Workfront Fusion]会将您在创建连接时输入的电子邮件地址用作发件人地址。 如果输入任何其他电子邮件地址，则在发送邮件时可能会发生错误，因为您的帐户可能无权从不同于您自己的地址发送电子邮件。 如<code>test@mail.com</code>或“<code>John Bush" test@email.com</code>”。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>输入或映射显示在电子邮件的[!UICONTROL Sender]字段中的电子邮件地址。</p> <p>提示：如果您不确定是使用此字段还是从字段，我们建议您选择从字段。</p> <p>重要提示：使用正确的语法： <code>name@email.com</code>或 <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> 如果要将对此电子邮件的回复发送到与“发件人”地址不同的地址，请输入要用于对此电子邮件进行回复的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> 如果回复的是特定电子邮件，请输入或映射要回复的电子邮件的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>输入线程中所有回复的消息ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>选择电子邮件的优先级：</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>添加标头：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>添加键。 例如，[!UICONTROL Sender]、[!UICONTROL Date]、[!UICONTROL To]等。</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>输入键的值。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Draft]

创建新草稿并将其添加到选定文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[!UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>选择要创建草稿电子邮件的文件夹。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>输入或映射要向其发送电子邮件的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>输入或映射电子邮件的主题行。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>选择电子邮件的内容类型：</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plain Text]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>使用HTML标签以HTML格式输入或映射电子邮件内容，或者以纯文本输入或映射电子邮件内容，具体取决于您在[!UICONTROL Content Type]字段中选择的内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>添加附件：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>输入文件名。 例如， sample.doc。</p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>输入要上载附件的文件夹的路径。</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>输入内容ID以在内容中插入附件（图像）。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>输入或映射要向其发送此电子邮件副本的一个或多个电子邮件地址。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> 输入或映射您要向其发送此电子邮件副本的一个或多个电子邮件地址，而不在电子邮件中显示该电子邮件地址。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>输入或映射电子邮件中[!UICONTROL From]字段中显示的电子邮件地址（和名称，如果需要）。 </p> <p>重要：使用正确的语法： <code>name@email.com</code>或<code>"Name" name@email.com</code>。</p> <p>注意：通常，[!DNL Workfront Fusion]会将您在创建连接时输入的电子邮件地址用作发件人地址。 如果输入任何其他电子邮件地址，则在发送邮件时可能会发生错误，因为您的帐户可能无权从不同于您自己的地址发送电子邮件。 如<code>test@mail.com</code>或“<code>John Bush" test@email.com</code>”。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>输入或映射显示在电子邮件的[!UICONTROL Sender]字段中的电子邮件地址。</p> <p>提示：如果您不确定是使用此字段还是从字段，我们建议您选择从字段。</p> <p>重要提示：使用正确的语法： <code>name@email.com</code>或 <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> 如果要将对此电子邮件的回复发送到与“[!UICONTROL from]”地址不同的地址，请输入要将此电子邮件的回复发送到的电子邮件地址。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> 如果回复的是特定电子邮件，请输入或映射要回复的电子邮件的ID。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>输入线程中所有回复的消息ID。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>选择电子邮件的优先级：</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>添加标头：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>添加键。 例如，“发件人”、“日期”、“收件人”等。</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>输入键的值。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Read]

通过设置[!UICONTROL Read]标志，将所选文件夹中的电子邮件或草稿标记为已读。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[!UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>选择要标记为已读的电子邮件文件夹。 示例： Primary。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>输入要标记为已读的电子邮件的电子邮件UID 。</p> <p>您可以使用[!UICONTROL Email] &gt;[!UICONTROL Watch Email]模块或[!UICONTROL Search Email]模块获取电子邮件的UID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Unread]

通过设置未读标志，将所选文件夹中的电子邮件或草稿标记为未读。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[!UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>选择要标记为未读的电子邮件文件夹。 示例： Primary。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>输入要标记为未读的电子邮件的Email UID。</p> <p>您可以使用[!UICONTROL Email] &gt;[!UICONTROL Watch Email]模块或[!UICONTROL Search Email]模块获取电子邮件的UID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Email]

将所选电子邮件或草稿移动到所选文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[!UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>选择包含要从中移动电子邮件的电子邮件的文件夹。 示例： Primary。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> 选择要向其中添加电子邮件的文件夹。 示例：工作。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>输入要移动到目标文件夹的电子邮件的Email UID。</p> <p>您可以使用[!UICONTROL Email] &gt;[!UICONTROL Watch Email]模块或[!UICONTROL Search Email]模块获取电子邮件的UID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy an Email]

将电子邮件或草稿复制到选定的文件夹中。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[!UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>选择要从中复制电子邮件的文件夹。 示例： Primary。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> 选择要将电子邮件复制到其中的文件夹。 示例：工作。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>输入要复制到目标文件夹的电子邮件的Email UID。</p> <p>您可以使用[!UICONTROL Email] &gt;[!UICONTROL Watch Email]模块或[!UICONTROL Search Email]模块获取电子邮件的UID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an Email]

从所选文件夹中删除电子邮件或草稿。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[!UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>选择要删除的电子邮件的文件夹。 示例： Primary。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>输入要删除的电子邮件的电子邮件UID 。</p> <p>您可以使用[!UICONTROL Email] &gt;[!UICONTROL Watch Email]模块或[!UICONTROL Search Email]模块获取电子邮件的UID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expunge]</td> 
   <td> <p>启用此选项以允许模块永久删除当前打开邮箱中标记为[!UICONTROL Deleted]的所有邮件。</p> <p>注意：在[!DNL Gmail]中，此行为由[!UICONTROL Settings] &gt;[!UICONTROL Forwarding POP/IMAP in IMAP access]部分中的设置驱动。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Emails]

返回与指定条件匹配的电子邮件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将电子邮件帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-your-email-to-workfront-fusion" class="MCXref xref">将电子邮件连接到[!UICONTROL Workfront Fusion]</a>。</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>选择包含要检索的电子邮件的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched] </td> 
   <td> <p>如果要在检索详细信息后将未读电子邮件标记为已读，请启用此选项。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>选择要检索的电子邮件的条件：</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>输入或映射要检索其电子邮件的发件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email Address]</td> 
   <td> <p> 输入或映射要检索其电子邮件的收件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From date] </td> 
   <td> <p>输入或映射日期，以检索在指定日期或该日期之后处理的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before date]</td> 
   <td> <p> 输入或映射日期，以检索在指定日期或之前处理的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>输入或映射要检索的电子邮件主题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>输入或映射任何关键字以仅检索包含特定短语的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email ID (UID)]</td> 
   <td> <p> 输入要检索其详细信息的电子邮件的电子邮件ID (UID)。</p> <p>您可以使用[!DNL Workfront Fusion]的[!UICONTROL  Watch Email]模块或[!UICONTROL Search Email]模块获取电子邮件的UID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> 在一个方案执行周期内应返回的最大电子邮件数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p> 选择是否要在没有返回结果的情况下继续运行模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 迭代器

#### [!UICONTROL Iterate Attachments]

逐个接收附件。

电子邮件迭代器模块允许您单独管理电子邮件附件。 例如，您可以设置监视电子邮件，对带有附件的电子邮件进行迭代并接收警报。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module]</td> 
   <td> <p>选择用于输出带有要对其进行迭代的附件的电子邮件的模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

有关迭代器的详细信息，请参阅[迭代器模块](/help/workfront-fusion/references/modules/iterator-module.md)。
