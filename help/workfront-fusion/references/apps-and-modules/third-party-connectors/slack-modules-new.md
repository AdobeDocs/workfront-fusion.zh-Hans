---
title: Slack模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用Slack的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: bb1cd0c54ae2c81c601d463cdc281d6ae7b8c434
workflow-type: tm+mt
source-wordcount: '4560'
ht-degree: 0%

---

# [!DNL Slack]模块

>[!IMPORTANT]
>
>本文介绍了在2025年11月14日发布的新Slack连接器中可用的模块。
>
>有关旧版Slack连接器的信息，请参阅[[!DNL Slack] 模块（旧版）](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/slack-modules.md)。

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Slack]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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

要使用[!DNL Slack]模块，您必须具有[!DNL Slack]帐户。

## Slack API信息

Slack连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
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
* [文件](#files)
* [渠道](#channels)
* [反应](#reactions)
* [星级](#stars)
* [已保存的项目](#saved-items)
* [固定](#pins)
* [用户](#users)
* [提醒](#reminders)
* [事件](#events)
* [轮廓](#profile)
* [其他](#other)

### 消息

+++ **[!UICONTROL 创建消息]**

此操作模块将创建新消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 输入渠道ID或名称]</p> </td> 
   <td> <p>选择您希望如何选择要创建消息的渠道。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 手动输入]</strong> </p> <p>在<strong>[!UICONTROL 渠道ID或名称]</strong>字段中，输入或映射要发布消息的渠道的渠道ID或名称。</p> <p>注意：可以使用[!UICONTROL List Channels]模块检索渠道ID。</p> </li> 
     <li> <p><strong>[!UICONTROL 从列表中选择]</strong> </p> <p>选择渠道类型，然后选择渠道。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>输入要创建的消息的文本内容。</p> <p>注意：有关文本格式化的详细信息，请参阅<a href="https://api.slack.com/reference/surfaces/formatting">文档中的</a>设置应用程序表面文本的格式[!DNL Slack]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 块]</td> 
   <td>块是可重用组件，可用于自定义和组织消息。 有关块的详细信息，请参阅<a href="https://api.slack.com/block-kit">文档中的</a>块套件[!DNL Slack]。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 线程消息ID （时间戳）]</td> 
   <td>如果新消息是回复，请输入要回复的消息的时间戳。 不要输入已经是回复的消息的时间戳。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 回复广播]</td> 
   <td> <p>如果同时满足以下两个条件，请选择<strong>[!UICONTROL 是]</strong>：</p> 
    <ul> 
     <li> <p>新消息是对另一消息的回复</p> </li> 
     <li> <p>您希望频道中的所有人都能够看到新消息</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 链接名称]</p> </td> 
   <td> <p>启用此选项以允许名称和渠道使用<code>@username</code>或<code>#channel</code>格式。 </p> <p>有关详细信息，请参阅<a href="https://api.slack.com/docs/formatting">文档中的</a>设置应用程序表面文本格式[!DNL Slack]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 解析消息文本]</p> </td> 
   <td> <p>启用此选项以允许自动分析。 </p> <p>有关详细信息，请参阅<a href="https://api.slack.com/docs/formatting">文档中的</a>设置应用程序表面文本格式[!DNL Slack]。</p> <p>注意：如果您在原始消息中使用了[!UICONTROL 链接名称]或[!UICONTROL 解析消息文本]选项，则您还应在运行[!UICONTROL 更新消息]模块时指定这些选项。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 使用Markdown]</p> </td> 
   <td> <p>启用此选项以允许[!DNL Slack]在文本中使用Markdown。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 主要展开基于文本的内容]</p> </td> 
   <td> <p>启用此选项以允许展开主要基于文本的内容。 </p> <p>有关[!DNL Slack]中展开的详细信息，请参阅<a href="https://api.slack.com/reference/messaging/link-unfurling">文档中的</a>消息中的展开链接[!DNL Slack]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 展开媒体内容]</p> </td> 
   <td> <p>启用此选项以允许展开媒体内容。 </p> <p>有关[!DNL Slack]中展开的详细信息，请参阅<a href="https://api.slack.com/reference/messaging/link-unfurling">文档中的</a>消息中的展开链接[!DNL Slack]。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 删除邮件]**

此操作模块删除指定的消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 渠道ID]</p> </td> 
   <td> <p>输入或映射渠道ID。</p> <p>注意：可以使用[!UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 消息ID （时间戳）]</td> 
   <td> <p> 输入或映射要删除的消息的时间戳。</p> <p>注意：可使用其他模块（如Watch Private Channel模块）检索时间戳。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 获取私人频道消息]**

此操作模块从所选渠道检索消息的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Channel]</p> </td> 
   <td> <p>选择包含消息的渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 消息ID（时间戳）]</p> </td> 
   <td> <p> 输入或映射要检索有关信息的消息的消息时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Public Channel]模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 获取公共频道消息]**

此操作模块从指定的公共渠道返回具有给定ID的消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 渠道ID]</p> </td> 
   <td> <p>选择包含消息的渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 消息ID（时间戳）]</td> 
   <td> <p> 输入或映射要检索有关信息的消息的消息时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Public Channel]模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 列出回复]**

此操作模块可检索发布到对话的消息线程。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择包含要为其检索回复的邮件的渠道类型，然后选择该渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 父消息ID（时间戳）]</td> 
   <td> <p> 输入或映射要检索其回复的消息的消息时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Public Channel]模块。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大回复数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 搜索邮件]**

此搜索模块返回与搜索查询匹配的消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>输入要作为搜索依据的查询。 </p> <p>有关从映射面板创建公式的信息，请参阅<a href="/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md" class="MCXref xref">使用[!DNL Adobe Workfront Fusion]</a>中的函数映射项。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>输入您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 排序方式] </td> 
   <td> <p>选择是否要按返回消息的分数或时间戳对返回消息进行排序。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>选择是否要按升序或降序对消息进行排序。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 更新消息]**

此操作模块允许您编辑现有消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 输入渠道ID或名称]</p> </td> 
   <td> <p>选择您希望如何选择要发送的消息。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 手动输入]</strong> </p> <p>在<strong>[!UICONTROL 渠道ID或名称]</strong>字段中，输入或映射包含该消息的渠道ID，然后输入该消息的<strong>[!UICONTROL 时间戳（消息ID）]</strong>。.</p> <p>注意：可以使用[!UICONTROL List Channels]模块检索渠道ID。</p> </li> 
     <li> <p><strong>[!UICONTROL 从列表中选择]</strong> </p> <p>选择渠道类型，然后选择渠道，最后选择消息。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Text]</p> </td> 
   <td> <p>输入要更新的消息的新文本内容。</p> <p>有关详细信息，请参阅<a href="https://api.slack.com/docs/formatting">文档中的</a>设置应用程序表面文本格式[!DNL Slack]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 块]</td> 
   <td>块是可重用组件，可用于自定义和组织消息。 有关块的详细信息，请参阅<a href="https://api.slack.com/block-kit">文档中的</a>块套件[!DNL Slack]。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 链接名称]</p> </td> 
   <td> <p>启用此选项以允许名称和渠道使用<code>@username</code>或<code>#channel</code>格式。 </p> <p>有关详细信息，请参阅<a href="https://api.slack.com/docs/formatting">文档中的</a>设置应用程序表面文本格式[!DNL Slack]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 解析消息文本]</p> </td> 
   <td> <p>启用此选项以允许自动分析。 </p> <p> 有关详细信息，请参阅<a href="https://api.slack.com/docs/formatting">文档中的</a>设置应用程序表面文本格式[!DNL Slack]。</p> <p>注意：如果您在原始消息中使用了[!UICONTROL 链接名称]或[!UICONTROL 解析消息文本]选项，则您还应在运行更新消息模块时指定这些选项。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 观看私信]**

此触发器模块在将新消息添加到直接消息时启动场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>选择要监视新消息的直接消息对话。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>输入您希望模块在每个方案执行周期中返回的最大消息数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 观看多方私信]**

在将新消息添加到多方直接消息渠道时，此触发器模块将启动场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>选择要监视新消息的直接消息对话。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>输入您希望模块在每个方案执行周期中返回的最大消息数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL 观看私人频道留言]**

此触发器模块在将新消息添加到专用渠道（组）后启动场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>选择要监视新消息的专用渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>输入您希望模块在每个方案执行周期中返回的最大消息数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL 观看公共渠道消息]**

在将新消息添加到公共渠道时，此触发器模块将启动场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channel] </td> 
   <td> <p>选择要监视新消息的公共渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>输入您希望模块在每个方案执行周期中返回的最大消息数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 文件

+++ **[!UICONTROL 删除文件]**

此操作模块返回删除指定的文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件ID]</td> 
   <td> <p>输入或映射要删除的文件的ID。 </p> <p>注意：可以使用其他模块（如[!DNL Watch Files]模块）检索文件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 获取文件]**

此操作模块返回有关指定文件的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件ID]</td> 
   <td> <p>输入或映射要检索的文件的ID。 </p> <p>注意：可以使用其他模块（如[!DNL Watch Files]模块）检索文件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 列出文件]**

此操作模块根据指定的筛选器返回文件列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 类型] </td> 
   <td> <p>选择要检索的文件类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 渠道类型]</p> </td> 
   <td> <p>选择表示要从中列出文件的通道的通道类型，然后选择该通道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 创建者]</td> 
   <td> <p>选择一个用户以仅返回由指定用户创建的文件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 起始日期]</td> 
   <td>输入要从中返回文件的最早日期。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 结束日期]</td> 
   <td>输入要从中返回文件的最晚日期。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射每个方案执行周期中您希望模块返回的最大文件数。</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Download a File]**

This action module downloads a file from a URL. It must follow the [!UICONTROL Slack] >[!UICONTROL Get a File] module in a scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL private download]</td> 
   <td> <p>Map the <b>[!UICONTROL URL Private download]</b> value from the [!DNL Slack] >[!UICONTROL Get a File] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL 上载文件]**

此操作模块将文件创建或上传到[!DNL Slack]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 通道]</td> 
   <td> <p>对于要上载文件的每个渠道，单击<b>[!UICONTROL 添加项]</b>，然后选择渠道类型和渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>从上一个模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标题]</td> 
   <td>为要上传的文件输入标题</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 线程ID （时间戳）]</td> 
   <td> <p>如果以回复方式上传文件，请输入或映射要回复的消息的时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Private Channel]模块。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 初始注释]</td> 
   <td> <p>输入或映射引入文件的消息的文本。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 监视文件]**

此触发器模块在添加新文件后启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 类型]</td> 
   <td>选择您希望模块监视的文件类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td> <p>选择要监视文件的渠道类型，然后选择该渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 创建者]</td> 
   <td> <p>选择一个用户以仅返回由指定用户创建的文件。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大文件数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 渠道

+++ **[!UICONTROL 存档频道]**

此操作模块存档渠道。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 渠道ID]</p> </td> 
   <td> <p>输入或映射要存档的渠道ID。</p> <p>注意：可以使用[!UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 创建频道]**

此操作模块将创建新渠道。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 名称]</p> </td> 
   <td> <p>输入或映射新渠道的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 是私有的]</td> 
   <td>启用此选项可将新渠道设置为专用。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 获取频道]**

此操作模块返回有关工作区渠道的信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 渠道ID]</p> </td> 
   <td> <p>输入或映射要检索相关信息的渠道ID。</p> <p>注意：可以使用[!UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 加入频道]**

此操作模块将用户加入渠道。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 渠道ID]</p> </td> 
   <td> <p>输入或映射要加入的渠道ID。</p> <p>注意：可以使用[!UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 离开频道]**

此操作模块会将用户从渠道中删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 渠道ID]</p> </td> 
   <td> <p>输入或映射要离开的渠道ID。</p> <p>注意：可以使用[!UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 列出频道]**

此搜索模块返回工作区中所有渠道的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 排除已存档的]</p> </td> 
   <td> <p>选择[!UICONTROL 是]可在结果中排除存档的渠道。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 类型] </td> 
   <td> <p>选择要检索的渠道类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>设置您希望模块在每个方案执行周期中返回的最大渠道数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 列出渠道中的成员]**

此搜索模块返回选定渠道中的用户列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择包含要列出的成员的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private Channel]</td> 
   <td>选择要为其列出成员的渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>设置您希望模块在每个方案执行周期中返回的最大成员数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 设置渠道的目的]**

此操作模块会更改渠道的用途

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要更改其用途的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] /用户/ [!UICONTROL 多个IM渠道]</td> 
   <td>选择要更改其用途的渠道或用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 用途]</td> 
   <td>输入或映射渠道的新用途。 此字段不支持设置格式或链接。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 设置频道的主题]**

此操作模块会更改渠道主题

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要为其更改主题的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM Channel]</td> 
   <td>选择要为其更改主题的渠道或用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 主题]</td> 
   <td>输入或映射渠道的新主题。 此字段不支持设置格式或链接。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 取消存档频道]**

此操作模块将取消存档渠道。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 渠道ID]</p> </td> 
   <td> <p>输入或映射要取消存档的渠道ID。</p> <p>注意：可以使用[!UICONTROL List Channels]模块检索渠道ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 反应

+++ **[!UICONTROL 添加反应]**

此操作模块添加对项目的反应。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要向其添加反应的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>选择要向其添加反应的渠道或用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 消息ID （时间戳）]</td> 
   <td> <p> 输入或映射要向其添加反应的消息的时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Private Channel]模块。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 反应（表情符号）名称]</td> 
   <td>输入或映射要用于反应的表情符号名称。 示例：<code>thumbsup</code>。 </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 列出反应]**

该操作模块返回用户做出的反应。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 用户]</p> </td> 
   <td> <p>选择作出要列出的反应的用户。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大反应数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 删除反应]**

此操作模块从项目中删除反应。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要从中删除反应的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>选择要从中删除反应的渠道或用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 消息ID]</td> 
   <td> <p> 输入或映射要从其中删除反应的消息的时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Private Channel]模块。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 反应（表情符号）名称]</td> 
   <td>输入或映射要从消息中删除的emoji的名称。 示例：<code>thumbsup</code>。 </td> 
  </tr> 
 </tbody> 
</table>

+++

### 星级

+++ **[!UICONTROL 添加星形]**

该操作模块可将渠道设置为星级渠道。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要向其中添加星号的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>选择要向其添加星号的渠道或用户。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 删除星标]**

此操作模块从星形通道中删除星形。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要向其中添加星号的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL User] / [!UICONTROL Multiple IM channel]</td> 
   <td>选择要向其添加星号的渠道或用户。</td> 
  </tr> 
 </tbody> 
</table>

+++

### 已保存的项目

+++ **[!UICONTROL 删除已保存的项目]**

此操作模块会从保存的项目中删除项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 消息ID（时间戳）]</td> 
   <td> <p> 输入或映射要从保存的项目中删除的消息的时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Private Channel]模块。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件ID]</td> 
   <td> <p>输入或映射要从保存的项目中删除的文件。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 保存项目]**

此操作模块会将项目添加到已保存的项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 消息ID（时间戳）]</td> 
   <td> <p> 输入或映射要保存的消息的时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Private Channel]模块。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件ID]</td> 
   <td> <p>输入或映射要保存的文件。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 固定

+++ **[!UICONTROL 固定项目]**

此操作模块将项目固定到渠道。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要将项目固定到的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL Multiple IM Channel] / [!UICONTROL User]</td> 
   <td>选择要将项目固定到的渠道或用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 消息ID]</td> 
   <td> <p> 输入或映射要固定消息的时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Private Channel]模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 取消固定项目]**

此操作模块从渠道中取消固定项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要取消固定项目的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private] / [!UICONTROL Multiple IM Channel] / [!UICONTROL User]</td> 
   <td>选择要从中取消固定项目的渠道或用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 消息ID]</td> 
   <td> <p> 输入或映射要取消固定的消息的时间戳。</p> <p>注意：可使用其他模块检索时间戳，例如[!UICONTROL Watch Private Channel]模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 用户

+++ **[!UICONTROL 获取用户]**

此操作模块可检索有关工作区成员的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 用户ID]</p> </td> 
   <td> <p>输入或映射要检索其详细信息的用户的用户ID。</p> <p>注意：可以使用其他模块（如[!DNL List Users]模块）检索用户ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 邀请用户]**

此操作模块邀请1-30个用户访问公共或专用渠道。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要邀请用户访问的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private channel]</td> 
   <td>选择要邀请用户访问的渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 用户]</td> 
   <td> <p>选择要添加到渠道的用户。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 启动用户]**

此操作模块从渠道中删除用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 渠道类型]</td> 
   <td>选择要从中删除用户的渠道类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Public] / [!UICONTROL Private channel]</td> 
   <td>选择要从中删除用户的渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 用户]</td> 
   <td> <p>选择要从渠道中删除的用户。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 列出用户]**

此操作模块返回工作区中所有用户的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 限制]</p> </td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大用户数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 搜索用户]**

此操作模块使用单个用户的电子邮件地址检索有关该用户的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 电子邮件] </p> </td> 
   <td> <p>输入或映射要检索其详细信息的用户的电子邮件地址。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 监视用户]**

此触发器模块在将新用户添加到[!DNL Slack]工作区时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>设置您希望模块在每个方案执行周期中返回的最大用户数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 提醒

<!--

+++ **[!UICONTROL List Reminders]**

This action module returns a list of all reminders created by or given to the currently authenticated user.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Limit]</p> </td> 
   <td> <p>Enter or map the maximum number of reminders you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Get a Reminder]**

This action module retrieves details about a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to retrieve details for.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

+++ **[!UICONTROL 创建提醒]**

此操作模块创建一个提醒。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text]</td> 
   <td>输入或映射提醒的内容</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 时间]</td> 
   <td> <p>输入或映射此提醒应该发生的日期和时间。 输入以下选项之一： </p> 
    <ul> 
     <li> <p>Unix时间戳（自现在起最多五年）</p> </li> 
     <li> <p>提醒前的秒数（如果在24小时内） </p> </li> 
     <li> <p>自然语言描述（示例：“15分钟内”或“每星期四”）</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 用户] </p> </td> 
   <td> <p>选择接收提醒的用户。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

<!--

+++ **[!UICONTROL Complete a Reminder]**

This action module completes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to complete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Delete a Reminder]**

This action module deletes a specific reminder.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>For instructions about connecting your [!DNL Slack] account to [!DNL Workfront Fusion], see <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">Create a connection to [!DNL Adobe Workfront Fusion] - Basic instructions</a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Reminder ID]</p> </td> 
   <td> <p>Enter or map the Reminder ID of the reminder you want to delete.</p> <p>Note: The Reminder ID can be retrieved using another module, such as the [!UICONTROL List Reminders] module.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

-->

### 事件

+++ **[!UICONTROL 新事件]**

此即时触发器会在创建新消息或其他事件时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>选择要使用的webhook。</p> <p>或</p> <p>创建新的webhook。</p> 
    <ol> 
     <li value="1"> <p>单击<b>[!UICONTROL 添加]</b>。</p> </li> 
     <li value="2"> <p>选择事件类型。</p> </li> 
     <li value="3"> <p>选择或添加连接。 有关将[!DNL Slack]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明</a></p> </li> 
     <li value="4"> <p>如果出现提示，请选择要观看的频道。</p> </li> 
     <li value="5"> <p>单击<b>[!UICONTROL 保存]</b>以保存webhook并返回模块。</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 轮廓

+++ **[!UICONTROL 设置状态]**

此操作模块更新用户的当前状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 状态文本]</p> </td> 
   <td> <p>输入或映射状态文本。 请考虑以下事项：</p> 
    <ul> 
     <li> <p>最多可输入100个字符。</p> </li> 
     <li> <p>您可以使用标记或其他格式，例如用户提及。</p> </li> 
     <li> <p>您可以使用格式<code>:emojiname:</code>在状态文本中包含表情符号。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 状态表情符号]</td> 
   <td> <p>输入或映射要用于表示状态的表情符号。 使用格式<code>:emojiname:</code>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 状态过期]</td> 
   <td>输入或映射希望状态到期的日期和时间。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">类型强制</a>。</td> 
  </tr> 
 </tbody> 
</table>

+++

### 其他

+++ **[!UICONTROL 进行API调用]**

此操作模块允许您对[!DNL Slack] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Slack]模块无法实现的数据流自动化。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Slack]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code>https://slack.com/api/</code>的路径。 示例：<code>/users/identity</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion]会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 基本URL]</td> 
   <td>选择要用于API调用的基本URL。</td> 
  </tr> 
 </tbody> 
</table>

+++

## 术语

在配置[!DNL Slack]模块时，以下术语可能很有用：

* **DM**： [!UICONTROL 直接消息]
* **即时消息**： [!UICONTROL 即时消息]
* **专用频道**：以前为[!UICONTROL 组]
* **直接消息**：以前为[!UICONTROL IM]
* **频道**： API文档中的[!UICONTROL 对话]，[!UICONTROL 应用程序中的]频道[!DNL Slack]。

