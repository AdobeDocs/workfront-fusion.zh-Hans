---
title: Slack模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用Slack的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: c9c68a4c-f592-42d1-b15f-a525b9aa3944
source-git-commit: e52af924094722b0d212098ae2af5eded12a5309
workflow-type: tm+mt
source-wordcount: '1864'
ht-degree: 0%

---

# [!DNL Slack]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Slack]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL Slack]模块，您必须具有[!DNL Slack]帐户。

## Slack API信息

Slack连接器使用以下对象：

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
   <td>v4.0.15</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Slack]模块及其字段

配置[!DNL Slack]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Slack]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

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
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL渠道ID或名称]</strong>字段中，输入或映射要发布消息的渠道的渠道ID或名称。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索渠道ID。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择渠道类型，然后选择渠道。</p> </li> 
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
   <td>如果新消息是回复，请输入要回复的消息的时间戳。 不要输入已经是回复的消息的时间戳。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL回复广播]</td> 
   <td> <p>如果同时满足以下两个条件，请选择<strong>[！UICONTROL是]</strong>：</p> 
    <ul> 
     <li> <p>新消息是对另一消息的回复</p> </li> 
     <li> <p>您希望频道中的所有人都能够看到新消息</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL附件]</td> 
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
   <td> <p>启用此选项以允许名称和渠道使用<code>@username</code>或<code>#channel</code>格式。 </p> <p>有关详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/docs/formatting">设置应用程序表面文本格式</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL解析消息文本]</p> </td> 
   <td> <p>启用此选项以允许自动分析。 </p> <p>有关详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/docs/formatting">设置应用程序表面文本格式</a>。</p> <p>注意：如果您在原始消息中使用了[！UICONTROL链接名称]或[！UICONTROL解析消息文本]选项，则您还应在运行[！UICONTROL更新消息]模块时指定这些选项。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL使用Markdown]</p> </td> 
   <td> <p>启用此选项以允许[!DNL Slack]在文本中使用Markdown。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL主要展开基于文本的内容]</p> </td> 
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

<!--Becky start here-->


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
   <td> <p> 输入或映射要删除的消息的时间戳。</p> <p>注意：可使用其他模块（如Watch Private Channel模块）检索时间戳。</p> </td> 
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
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL渠道ID]</p> </td> 
   <td> <p>输入（映射）渠道ID。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL消息ID（时间戳）]</p> </td> 
   <td> <p> 输入或映射要检索相关信息的消息的消息时间戳。</p> <p>注意：可以使用其他模块（例如[！UICONTROL Watch Public Channel]模块）检索时间戳。</p> </td> 
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
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL渠道ID]</p> </td> 
   <td> <p>输入或映射渠道ID。</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL消息ID（时间戳）]</td> 
   <td> <p> 输入或映射要检索相关信息的消息的消息时间戳。</p> <p>注意：可以使用其他模块（例如[！UICONTROL Watch Public Channel]模块）检索时间戳。</p> </td> 
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
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL输入渠道ID或名称]</p> </td> 
   <td> <p>选择您希望如何选择要发送的消息。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL渠道ID或名称]</strong>字段中，输入或映射包含该消息的渠道ID，然后输入该消息的<strong>[！UICONTROL时间戳（消息ID）]</strong>。.</p> <p>注意：可以使用[！UICONTROL List Channels]模块检索渠道ID。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择渠道类型，然后选择渠道，最后选择消息。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Text]</p> </td> 
   <td> <p>输入要更新的消息的新文本内容。</p> <p>有关详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/docs/formatting">设置应用程序表面文本格式</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL块]</td> 
   <td>块是可重用组件，可用于自定义和组织消息。 有关块的详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/block-kit">块套件</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL链接名称]</p> </td> 
   <td> <p>启用此选项以允许名称和渠道使用<code>@username</code>或<code>#channel</code>格式。 </p> <p>有关详细信息，请参阅[!DNL Slack]文档中的<a href="https://api.slack.com/docs/formatting">设置应用程序表面文本格式</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL解析消息文本]</p> </td> 
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

* [获取渠道](#get-a-channel)
* [列出渠道](#list-channels)
* [在渠道中列出成员](#list-members-in-channel)

#### [!UICONTROL 获取频道]

此操作模块返回有关工作区渠道的信息。

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

此搜索模块返回工作区中所有渠道的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL排除已存档的]</p> </td> 
   <td> <p>选择[！UICONTROL是]可在结果中排除存档的渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL类型] </td> 
   <td> <p>选择要检索的渠道类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制] </td> 
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
   <td role="rowheader">[！UICONTROL渠道类型]</td> 
   <td>选择包含要列出的成员列表的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Public] / [！UICONTROL Private Channel]</td> 
   <td>选择要为其列出成员的渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制] </td> 
   <td> <p>设置在一个执行周期内[!DNL Workfront Fusion]返回的最大成员数。</p> </td> 
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
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
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
 </tbody> 
</table>

## 术语

在配置[!DNL Slack]模块时，以下术语可能很有用：

* **DM**： [!UICONTROL 直接消息]
* **即时消息**： [!UICONTROL 即时消息]
* **专用频道**：以前为[!UICONTROL 组]
* **直接消息**：以前为[!UICONTROL IM]
* **频道**： API文档中的[!UICONTROL 对话]，[!DNL Slack]应用程序中的[!UICONTROL 频道]。
