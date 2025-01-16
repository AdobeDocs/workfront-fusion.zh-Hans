---
title: Gmail模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Gmail的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: 0581601a254a9492f4166d78eb0f11868d390f24
workflow-type: tm+mt
source-wordcount: '1527'
ht-degree: 0%

---

# [!DNL Gmail]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Gmail]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。 有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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

要使用[!DNL Gmail]模块，您必须具有[!DNL Gmail]帐户。

## 将[!DNL Gmail]连接到[!DNL Workfront Fusion] {#connect-gmail-to-workfront-fusion}

* [使用 [!DNL Google Workspace]连接 [!DNL Gmail] 到 [!DNL Workfront Fusion] ](#connect-gmail-to-workfront-fusion-usingg-suite)
* [使用 [!DNL gmail.com] 或 [!DNL googlemail].com连接 [!DNL Gmail] 到 [!DNL Workfront Fusion] ](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### 使用[!DNL  Google Workspace]将[!DNL Gmail]连接到[!DNL Workfront Fusion] {#connect-gmail-to-workfront-fusion-using-g-suite}

有关将[!DNL Google Workspace]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)。

### 使用[!DNL gmail.com]或[!DNL googlemail].com连接[!DNL Gmail]到[!DNL Workfront Fusion] {#connect-gmail-to-workfront-fusion-using-gmail-com-or-googlemail-com}

如果您是[!DNL @gmail.com]或[!DNL @googlemail.com]用户，则必须在[the [!DNL Google Cloud Platform]](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project)上创建OAuth客户端才能获取[!UICONTROL Client ID]和[!UICONTROL Client Secret]。

有关如何创建OAuth客户端并获取[!UICONTROL Client ID]和[!UICONTROL Client Secret]的分步说明，请参阅[使用自定义OAuth客户端将Adobe Workfront Fusion连接到Google服务](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)。

## [!DNL Gmail]模块及其字段

配置[!DNL Gmail]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Gmail]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [迭代器](#iterators)

### 触发器

#### [!UICONTROL Watch emails]

此触发器模块在收到要处理的新电子邮件时执行场景。

该模块返回与一个或多个记录关联的所有标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Gmail]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">将[!DNL Gmail]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>选择要监视的电子邮件文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter type] </td> 
   <td> <p>选择要用于观看电子邮件的过滤器类型</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Simple filter]</strong> </p> <p>填写[!UICONTROL Criteria]、[!UICONTROL Sender Email Address]、[!UICONTROL Subject]和[!UICONTROL Search Phrase]字段</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail filter]</strong> </p> <p>在[!UICONTROL Query]字段中，输入要用于过滤电子邮件的查询。</p> <p>有关[!DNL Gmail]筛选器的详细信息，请参阅[!DNL Gmail]文档中的<a href="https://support.google.com/mail/answer/7190">搜索运算符</a>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteria]</td> 
   <td>选择您要观看[!UICONTROL all email]、[!UICONTROL only read emails]还是[!UICONTROL only unread]电子邮件。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sender email address]</td> 
   <td> <p> 输入电子邮件地址，以便仅监视从该地址发送的电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>输入一个文本字符串，以仅观看主题中带有该文本字符串的电子邮件。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search phrase]</td> 
   <td>输入一个文本字符串，以仅查看电子邮件中任何位置具有该文本字符串的电子邮件。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mark email message(s) as read when fetched]</td> 
   <td> <p> 启用此选项可将检索到的电子邮件标记为已读。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of results]</td> 
   <td> <p> 设置[!DNL Workfront Fusion]在一个周期内可处理的最大结果数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Send an email]](#send-an-email)
* [[!UICONTROL Create a draft]](#create-a-draft)
* [[!UICONTROL Mark an email as read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an email as unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an email]](#move-an-email)
* [[!UICONTROL Copy an email]](#copy-an-email)
* [[!UICONTROL Delete an email]](#delete-an-email)
* [[!UICONTROL Modify email labels]](#modify-email-labels)

#### [!UICONTROL Send an email]

此操作模块会发送一封新电子邮件。

指定电子邮件的收件人。

模块会返回电子邮件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Gmail]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">将[!DNL Gmail]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL From]</td> 
   <td> <p>输入或映射发件人电子邮件地址。</p> <p>注意：如果输入的电子邮件地址不正确，则在发送邮件时可能会发生错误，因为您的帐户可能无权从不同于您自己的地址发送电子邮件。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>单击<strong>[!UICONTROL Add]</strong>，然后输入或映射每个收件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>输入或映射电子邮件主题。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>输入或映射电子邮件内容（邮件正文）。 允许使用HTML标记。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>单击<strong>[!UICONTROL Add]</strong>添加附件。 您可以从以前的模块映射文件。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> 单击<strong>[!UICONTROL Add]</strong>，然后输入或映射每个副本收件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> 单击<strong>[!UICONTROL Add]</strong>，然后为每个盲文收件人输入或映射电子邮件地址。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a draft]

此操作模块将创建新的电子邮件草稿，并将其添加到您指定的文件夹中。

指定要在其中创建草稿的文件夹。

模块会返回电子邮件草稿的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Gmail]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">将[!DNL Gmail]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>选择要在其中创建草稿的[!DNL Gmail]文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>单击<strong>[!UICONTROL Add]</strong>，然后输入或映射每个收件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>输入或映射电子邮件主题。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>输入或映射电子邮件内容（邮件正文）。 允许使用HTML标记。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>单击<strong>[!UICONTROL Add]</strong>添加附件。 您可以从以前的模块映射文件。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> 单击<strong>[!UICONTROL Add]</strong>，然后输入或映射每个副本收件人的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> 单击<strong>[!UICONTROL Add]</strong>，然后为每个盲文收件人输入或映射电子邮件地址。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as read]

此操作模块将电子邮件标记为已读。

指定电子邮件及其文件夹的ID。

模块会返回电子邮件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Gmail]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">将[!DNL Gmail]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>选择包含电子邮件的[!DNL Gmail]文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> 输入或映射电子邮件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as unread]

此操作模块将电子邮件或电子邮件草稿标记为未读。

指定电子邮件及其文件夹的ID。

模块会返回电子邮件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Gmail]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">将[!DNL Gmail]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>选择包含电子邮件的[!DNL Gmail]文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)] </td> 
   <td> <p>输入或映射要标记为未读的电子邮件的电子邮件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an email]

此操作模块会将电子邮件或电子邮件草稿移动到您指定的文件夹。

您可以指定文件夹、目标文件夹和电子邮件的ID。

模块会返回电子邮件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Gmail]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">将[!DNL Gmail]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>选择包含要移动的电子邮件的[!DNL Gmail]源文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p> 选择要将电子邮件移动到的[!DNL Gmail]目标文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> 输入或映射要移动的电子邮件的电子邮件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy an email]

此操作模块会将电子邮件或电子邮件草稿复制到您指定的文件夹中。

您可以指定文件夹、目标文件夹和电子邮件的ID。

模块会返回电子邮件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Gmail]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">将[!DNL Gmail]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>选择包含要复制的电子邮件的[!DNL Gmail]源文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p>选择要将电子邮件复制到其中的[!DNL Gmail]目标文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p>输入或映射要复制的电子邮件的电子邮件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an email]

此操作模块会从您指定的文件夹中删除电子邮件或电子邮件草稿。

模块会返回电子邮件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Gmail]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">将[!DNL Gmail]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] 消息ID</p> </td> 
   <td> <p>输入或映射要删除的电子邮件的电子邮件ID。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Permanently] </td> 
   <td> <p>启用此选项可允许模块永久删除电子邮件，而不是将其移至垃圾桶文件夹。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify email labels]

此操作模块可修改您指定的电子邮件上的标签。

模块会返回电子邮件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Gmail]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-gmail-to-workfront-fusion" class="MCXref xref">将[!DNL Gmail]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] 消息ID</td> 
   <td> <p> 输入或映射要删除的电子邮件的电子邮件ID。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Labels to add]</p> </td> 
   <td> <p>选择或映射要添加到所选电子邮件的标签。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Labels to remove]</td> 
   <td> <p> 选择或映射要从所选电子邮件中删除的标签。</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!UICONTROL Label to add]和[!UICONTROL Label to remove]字段仅加载用户创建的标签。

### 迭代器

#### [!UICONTROL Iterate attachments]

您可以对电子邮件附件进行迭代。 每个附件都是一个单独的捆绑包，位于模块的输出中。 有关详细信息，请参阅[迭代器模块](/help/workfront-fusion/references/modules/iterator-module.md)。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> <p>选择要从中迭代处理附件的模块。 </p> </td> 
  </tr> 
 </tbody> 
</table>
