---
title: Microsoft Office 365电子邮件
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Microsoft Office 365电子邮件的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 5d4072ba-c598-4347-a42f-c59c7add0a1b
source-git-commit: 5a95b2c191d4e6d8750dc57a47923f416612b4a9
workflow-type: tm+mt
source-wordcount: '2354'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Email]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!UICONTROL Microsoft Office 365 Email]的工作流，并将其连接到多个第三方应用程序和服务。

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
   <p>当前：无Workfront Fusion许可证要求。</p>
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

要使用[!DNL Microsoft Office 365 Email]模块，您必须具有[!DNL Microsoft Office 365 Email]帐户。

## Microsoft Office 365电子邮件API信息

Microsoft Office 365电子邮件连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v2.6.5</td> 
  </tr>
 </tbody> 
 </table>

## 正在将[!DNL Office 365 Email]服务连接到[!DNL Workfront Fusion]

有关将[!DNL Office 365 Email]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
>
>例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。

## [!DNL Microsoft Office 365 Email]模块及其字段

配置[!DNL Microsoft Office 365 Email]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Microsoft Office 365 Email]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [消息](#message)
* [草稿消息](#draft-message)
* [附件](#attachment)
* [其他](#other)

### 消息

* [[!UICONTROL Create and Send a Message (legacy)]](#create-and-send-a-message)
* [[!UICONTROL Delete a Message]](#delete-a-message)
* [[!UICONTROL Get a message]](#get-a-message)
* [[!UICONTROL Move a Message]](#move-a-message)
* [[!UICONTROL Search messages]](#search-messages)
* [[!UICONTROL Watch Messages]](#watch-messages)



#### [!UICONTROL Create and Send a Message (legacy)]

此操作模块将创建并发送一封电子邮件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>输入或映射消息的主题行。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>输入或映射电子邮件的邮件正文文本。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>选择电子邮件的重要性</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>对于要向其发送电子邮件的每个收件人，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>对于要向其发送电子邮件副本的每个收件人，单击“添加项目”<b></b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>对于要向其发送电子邮件副本的每个收件人（不允许其他收件人查看其姓名或电子邮件地址），单击“<b>添加项目</b>”并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>对于要添加到电子邮件的每个附件，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Internet Message Headers]</td> 
   <td> <p>对于要添加到电子邮件的每个标头，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入标题的名称</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>输入题头值。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Message]

此操作模块删除现有电子邮件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> 选择或映射要删除的消息的ID。</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a message]

此操作模块获取特定消息的元数据

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> 选择或映射要为其检索元数据的消息的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get MIME contents]</td> 
   <td>启用此选项以检索有关消息的MIME内容的数据。 [!UICONTROL MIME]内容可能包括图像、音频、视频或其他类型的文件。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a Message]

此操作模块将电子邮件移动到邮箱中的选定文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> 选择或映射要移动到其他文件夹的邮件ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mail Folder] </td> 
   <td> <p>选择或映射要将邮件移动到的文件夹的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search messages]

此搜索模块根据特定条件搜索消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Mail Folder]</td> 
   <td> <p>选择包含要搜索邮件的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>输入您的搜索查询。 有关如何编写搜索查询的信息，请参阅[!DNL Microsoft]支持文章<a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">在[!DNL Outlook.com]</a>中搜索邮件和人员。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>选择要对结果进行排序的方式：</p> 
    <ul> 
     <li>[!UICONTROL Subject (Ascending or descending)]</li> 
     <li>[!UICONTROL Created Date Time (Ascending or descending)]</li> 
     <li>[!UICONTROL Last Modified Date Time (Ascending or descending)]</li> 
     <li>[!UICONTROL Received Date Time (Ascending or descending)]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入在一个方案执行周期内应返回的最大邮件数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Messages]

此触发器模块会在发送或接收新电子邮件时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Watch Messages]</p> </td> 
   <td> <p>选择要监视的消息：</p> 
    <ul> 
     <li>[!UICONTROL Only Unread]</li> 
     <li>[!UICONTROL Only read]</li> 
     <li>[!UICONTROL All]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mail Folder]</td> 
   <td> <p>选择包含要监视的邮件的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search]</td> 
   <td>输入您的搜索查询。 模块会返回与此查询匹配的消息。 有关如何编写搜索查询的信息，请参阅[!DNL Microsoft]支持文章<a href="https://support.microsoft.com/en-us/office/search-mail-and-people-in-outlook-com-88108edf-028e-4306-b87e-7400bbb40aa7?ui=en-us&amp;rs=en-us&amp;ad=us">在[!DNL Outlook.com]</a>中搜索邮件和人员。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td> <p>输入在一个方案执行周期内应返回的最大邮件数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 草稿消息

* [创建草稿消息](#create-a-draft-message)
* [发送草稿消息](#send-a-draft-message)
* [更新消息](#update-a-message)

#### [!UICONTROL Create a Draft Message]

此操作模块会将新电子邮件创建为草稿。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>输入消息的主题行。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body Content Type]</td> 
   <td>选择消息正文内容是“HTML”还是“文本”。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>输入或映射电子邮件的邮件正文文本。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>选择电子邮件的重要性</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>对于要向其发送电子邮件的每个收件人，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>对于要向其发送电子邮件副本的每个收件人，单击“添加项目”<b></b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>对于要向其发送电子邮件副本的每个收件人（不允许其他收件人查看其姓名或电子邮件地址），单击“<b>添加项目</b>”并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>对于要添加到电子邮件的每个附件，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send a Draft Message]

该操作模块会发送一封当前为草稿的电子邮件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Draft Message ID]</td> 
   <td> <p> 选择或映射要发送的草稿的消息ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Message]

此操作模块更新现有消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Enter a message ID]</td> 
   <td> <p>选择要如何标识要更新的消息：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter Manually]</strong> </p> <p>输入或映射消息ID。</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>选择包含要更新的邮件的文件夹，然后选择邮件</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>输入消息的主题行。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>输入电子邮件的邮件正文文本。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>选择电子邮件的重要性</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>对于要向其发送电子邮件的每个收件人，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>对于要向其发送电子邮件副本的每个收件人，单击“添加项目”<b></b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>对于要向其发送电子邮件副本的每个收件人（不允许其他收件人查看其姓名或电子邮件地址），单击“<b>添加项目</b>”并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>对于要添加到电子邮件的每个附件，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark it as Read]</td> 
   <td>启用此选项可将更新的邮件标记为已读。</td> 
  </tr> 
 </tbody> 
</table>

### 附件

* [[!UICONTROL Download an Attachment]](#download-an-attachment)
* [[!UICONTROL List Attachments]](#list-attachments)

#### [!UICONTROL Download an Attachment]

此模块下载指定的附件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> 选择或映射包含要下载附件的邮件的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment ID]</td> 
   <td> <p>输入或映射要下载的附件的ID。 您可以使用“列出附件”模块找到此想法。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List Attachments]

此模块检索属于指定邮件的附件列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> 选择或映射要从中检索附件的邮件的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大附件数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

* [[!UICONTROL Add an Attachment]](#add-an-attachment)
* [创建和发送消息](#create-and-send-a-message)
* [[!UICONTROL Make an API Call]](#make-an-api-call)

#### [!UICONTROL Add an Attachment]

此模块向邮件添加大型附件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message ID]</td> 
   <td> <p> 选择或映射要添加附件的邮件的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择一个文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create and Send a Message]

此操作模块将创建并发送一封电子邮件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject]</td> 
   <td> <p>输入或映射消息的主题行。</p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Body content]</td> 
   <td> <p>输入或映射电子邮件的邮件正文文本。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Importance]</td> 
   <td> <p>选择电子邮件的重要性</p> 
    <ul> 
     <li>[!UICONTROL Low]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL High]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL To Recipients]</p> </td> 
   <td> <p>对于要向其发送电子邮件的每个收件人，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL CC Recipients]</p> </td> 
   <td> <p><p>对于要向其发送电子邮件副本的每个收件人，单击“添加项目”<b></b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Bcc Recipients]</p> </td> 
   <td> <p>对于要向其发送电子邮件副本的每个收件人（不允许其他收件人查看其姓名或电子邮件地址），单击“<b>添加项目</b>”并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入联系人的电子邮件地址。</p> </li> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入联系人的姓名。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>对于要添加到电子邮件的每个附件，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Source file]</strong> </p> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Internet Message Headers]</td> 
   <td> <p>添加电子邮件的邮件头。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Name]</strong> </p> <p>输入标题的名称</p> </li> 
     <li> <p><strong>[!UICONTROL Email Address]</strong> </p> <p>输入题头值。</p> </li> 
    </ul> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL From email address]</td> 
   <td> <p> 要使用共享的电子邮件地址，请在此处输入地址。 其凭据用于此模块的连接中的用户必须有权访问共享文件夹。<p>将此字段留空将使用连接所有者自己的电子邮件地址。</p></p> </td> 
  </tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make an API Call]

此模块允许您执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>输入相对于<code>https://graph.microsoft.com</code>的路径。 示例：<code> /v1.0/me/messages</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 例如，<code>{"Content-type":"application/json"}</code>。 [!DNL Workfront Fusion]为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> 以标准JSON对象的形式添加API调用的查询。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
