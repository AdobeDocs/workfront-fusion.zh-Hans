---
title: Slack模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Slack的工作流，以及将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
source-git-commit: eb0518ba0d1a0c758cb547e362c722f4be3674c7
workflow-type: tm+mt
source-wordcount: '1954'
ht-degree: 0%

---

# [!DNL Slack]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Slack]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有下列访问权限，才能使用本文中的功能：

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
   <td> <p>新功能：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
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
   <p>新功能：</p> <ul><li>选择或Prime Workfront程序包：您的企业必须购买Adobe Workfront Fusion。</li><li>终极Workfront包：包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中的信息的更多详细信息，请参阅[文档中的访问要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

有关[!DNL Adobe Workfront Fusion]个许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

若要使用[!DNL Slack]模块，您必须拥有[!DNL Slack]帐户。

## SlackAPI信息

Slack连接器使用下列内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td>{{ifempty(parameters.domain， 'https://slack.com/api/')}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>版本4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Slack]模块及其字段

配置[!DNL Slack]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Slack]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果在字段或函数上方看到“映射”按钮，则可以使用该按钮为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [消息](#messages)
* [对话](#channels)
* [其他](#other)

### 消息

* [创建消息](#create-a-message)
* [删除消息](#delete-a-message)
* [获取专用渠道消息](#get-a-private-channel-message)
* [获取公共渠道消息](#get-a-public-channel-message)
* [更新消息](#update-a-message)
* [观看专用渠道消息](#watch-private-channel-messages)
* [观看公共渠道消息](#watch-public-channel-messages)

### [!UICONTROL 创建消息]

此操作模块将创建新消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL输入渠道ID或名称]</p> </td> 
   <td> <p>选择您希望如何选择要创建消息的渠道。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL通道ID或名称]</strong>字段中，输入或映射要发布消息的通道的通道ID或名称。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索通道ID。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择声道类型，然后选择声道。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Text]</p> </td> 
   <td> <p>输入要创建的消息的文本内容。</p> <p>注意：有关文本格式化的详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/reference/surfaces/formatting">设置应用程序表面文本的格式</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL作为用户]</td> 
   <td>启用此选项以拥有此模块连接使用的凭据的用户身份发布消息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL线程消息ID（时间戳）]</td> 
   <td>如果新邮件是回复，请输入您要回复的邮件的时间戳。 不要输入已经是回复的邮件的时间戳。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Reply broadcast]</td> 
   <td> <p>如果同时满足以下两个条件，请选择“<strong>[！UICONTROL是]</strong>”：</p> 
    <ul> 
     <li> <p>新邮件是对另一邮件的回复</p> </li> 
     <li> <p>您希望渠道中的每个人都可以看到新消息</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Attachments]</td> 
   <td>对于要附加到邮件的每个项目，单击<b>添加项目</b>并填写项目的详细信息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL图标表情符号]</td> 
   <td>输入或映射要用作此邮件图标的表情符号，格式为<code>:icon-name:</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL图标URL]</td> 
   <td>输入或映射要用作此消息图标的图像的URL。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL链接名称]</p> </td> 
   <td> <p>启用此选项以允许名称和通道使用<code>@username</code>或<code>#channel</code>格式。 </p> <p>有关详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/docs/formatting">设置应用程序表面的文本格式</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Parse message text]</p> </td> 
   <td> <p>启用此选项以允许自动分析。 </p> <p>有关详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/docs/formatting">设置应用程序表面的文本格式</a>。</p> <p>注意：如果在原始消息中使用了[！UICONTROL Link names]或[！UICONTROL Parse message text]选项，则还应在运行[！UICONTROL Update a Message]模块时指定这些选项。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Use markdown]</p> </td> 
   <td> <p>启用此选项可允许[!DNL Slack]在文本中使用markdown。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Unfurl主要基于文本的内容]</p> </td> 
   <td> <p>启用此选项以允许展开主要基于文本的内容。 </p> <p>有关[!DNL Slack]中展开的详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/reference/messaging/link-unfurling">消息中的展开链接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL展开媒体内容]</p> </td> 
   <td> <p>启用此选项以允许展开媒体内容。 </p> <p>有关[!DNL Slack]中展开的详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/reference/messaging/link-unfurling">消息中的展开链接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL用户名]</td> 
   <td>指定用于发布消息的用户名。 如果未指定用户名，则使用名称“Bot”。</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL 删除邮件]

此操作模块删除指定的消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL渠道ID]</p> </td> 
   <td> <p>输入或映射渠道ID。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL消息ID]</td> 
   <td> <p> 输入或映射要删除的消息的时间戳。</p> <p>注意：可使用其他模块（如Watch Private Channel Messages模块）检索时间戳。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL作为用户]</td> 
   <td> <p> 启用此选项可将消息以具有连接中所用凭据的用户身份删除。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取私人频道消息]

此操作模块从所选渠道检索消息的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建到[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL通道ID]</p> </td> 
   <td> <p>输入（映射）通道ID。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索通道ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL消息ID（时间戳）]</p> </td> 
   <td> <p> 输入或映射要检索相关信息的邮件的邮件时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[！UICONTROL Watch Private Channel Messages]模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取公共频道消息]**

此操作模块从指定的公共渠道返回具有给定ID的消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建到[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL通道ID]</p> </td> 
   <td> <p>输入或映射通道ID。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索通道ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL消息ID（时间戳）]</td> 
   <td> <p> 输入或映射要检索相关信息的邮件的邮件时间戳。</p> <p>注意：可使用其他模块（如[！UICONTROL Watch Public Channel Messages]模块）检索时间戳。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新消息]

此操作模块允许您编辑现有消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Enter a channel ID or name]</p> </td> 
   <td> <p>Choose how you want to select the message you want to .</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Enter manually]</strong> </p> <p>In the <strong>[!UICONTROL Channel ID or name]</strong> field, enter or map the Channel ID or of the channel that contains the message, then enter the <strong>[!UICONTROL Time Stamp (Message ID)]</strong> of the message.</p> <p>Note: The Channel ID can be retrieved using the [!UICONTROL List Channels] module.</p> </li> 
     <li> <p><strong>[!UICONTROL Select from the list]</strong> </p> <p>Select the type of channel, then select the channel, then select the message.</p> </li> 
    </ul> </td> 
  </tr> -->
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL渠道ID]</p> </td> 
   <td> <p>输入或映射包含要更新的消息的频道ID。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索渠道ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL消息ID（时间戳）]</p> </td> 
   <td> <p> 输入或映射要检索相关信息的邮件的邮件时间戳。</p> <p>注意：可使用其他模块（如[！UICONTROL Watch Public Channel Messages]模块）检索时间戳。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL文本]</p> </td> 
   <td> <p>输入要更新的邮件的新文本内容。</p> <p>有关详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/docs/formatting">设置应用程序表面的文本格式</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL As user]</td> 
   <td>启用此选项，以拥有此模块的连接所使用的凭据的用户身份更新消息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Attachments]</td> 
   <td>对于要附加到邮件的每个项目，单击<b>添加项目</b>并填写项目的详细信息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL链接名称]</p> </td> 
   <td> <p>启用此选项以允许名称和渠道使用<code>@username</code>或<code>#channel</code>格式。 </p> <p>有关详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/docs/formatting">设置应用程序表面的文本格式</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Parse message text]</p> </td> 
   <td> <p>启用此选项以允许自动分析。 </p> <p> 有关详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/docs/formatting">设置应用程序表面文本格式</a>。</p> <p>注意：如果您在原始消息中使用了[！UICONTROL链接名称]或[！UICONTROL解析消息文本]选项，则您还应在运行更新消息模块时指定这些选项。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 观看私人频道留言]

此触发器模块在将新消息添加到专用渠道（组）后启动场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Channel] </td> 
   <td> <p>选择要监视新消息的专用渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制] </td> 
   <td> <p>设置在一个执行周期内将返回的最大邮件数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看公共渠道消息]

在将新消息添加到公共渠道时，此触发器模块将启动场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Channel] </td> 
   <td> <p>选择要监视新消息的公共渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制] </td> 
   <td> <p>设置在一个执行周期内将返回的最大邮件数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>



### 对话

* [获取频道](#get-a-channel)
* [列出声道](#list-channels)
* [列出渠道中的成员](#list-members-in-channel)

#### [!UICONTROL 获取频道]

此操作模块返回有关工作区通道的信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL渠道ID]</p> </td> 
   <td> <p>输入或映射要检索相关信息的渠道ID。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
 </tbody>

#### [!UICONTROL 列出频道]

此搜索模块返回工作区中所有通道的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建到[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL排除已存档]</p> </td> 
   <td> <p>选择[！UICONTROL Yes]以在结果中排除存档的通道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Type] </td> 
   <td> <p>选择要检索的通道类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Limit] </td> 
   <td> <p>设置在一个执行周期内返回的最大通道数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL 列出渠道中的成员]

此搜索模块返回选定渠道中的用户列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
<tr> 
   <td role="rowheader"> <p>[！UICONTROL输入渠道ID或名称]</p> </td> 
   <td> <p>选择您希望如何选择要发送的消息。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL渠道ID或名称]</strong>字段中，输入或映射要从中列出用户的渠道或渠道ID。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索渠道ID。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择渠道类型，然后选择渠道。</p> </li> 
    </ul> </td> 
  </tr>
  <tr> 
   <td role="rowheader">[！UICONTROL Limit] </td> 
   <td> <p>设置在一个执行周期中将返回的最大成员数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>


### 其他

#### [!UICONTROL 进行API调用]

此操作模块允许您对[!DNL Slack] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Slack]模块无法实现的数据流自动化。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建到[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL URL]</td> 
   <td>输入相对于<code>https://slack.com/api/</code>的路径。 示例： <code>/users/identity</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL方法]</td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[！UICONTROL Workfront Fusion]会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL基本URL]</td> 
   <td>选择要用于API调用的基本URL。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL发送访问令牌]</td> 
   <td>选择您希望将访问令牌作为标头还是查询参数发送。</td> 
  </tr> 
 </tbody> 
</table>

## 术语

在配置[!DNL Slack]模块时，以下术语可能很有用：

* **DM**： [!UICONTROL 直接消息]
* **即时消息**： [!UICONTROL 即时消息]
* **专用频道**：之前为[!UICONTROL 组]
* **直接消息**：以前为[!UICONTROL IM]
* **频道**： API文档中的[!UICONTROL 对话]，[!DNL Slack]应用程序中的[!UICONTROL 频道]。
