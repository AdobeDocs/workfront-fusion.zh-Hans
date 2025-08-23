---
title: Microsoft Office 365日历
description: 在Adobe Workfront Fusion场景中，您可以自动使用Microsoft Office 365日历的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: fdecf740-e735-4569-b1a2-7c25c751ba42
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2044'
ht-degree: 0%

---

# [!DNL Microsoft Office 365 Calendar]

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Microsoft Office 365 Calendar]的工作流，并将其连接到多个第三方应用程序和服务。

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

## 先决条件

要使用[!DNL Microsoft Office 365 Calendar]模块，您必须具有[!DNL Microsoft Office 365 Calendar]帐户。

## Microsoft Office 365日历API信息

Microsoft Office 365日历连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## 正在将[!DNL Office 365 Calendar]服务连接到Workfront Fusion

有关将[!DNL Office 365 Calendar]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
>
>例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。

## [!DNL Microsoft Office 365 Calendar]模块及其字段

在配置[!DNL Microsoft Office 365 Calendar]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Microsoft Office 365 Calendar]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [活动](#event)
* [日程表](#calendar)
* [其他](#other)

### 活动

* [[!UICONTROL 创建事件]](#create-an-event)
* [[!UICONTROL 删除事件]](#delete-an-event)
* [[!UICONTROL 获取事件]](#get-an-event)
* [[!UICONTROL 搜索事件]](#search-events)
* [[!UICONTROL 更新事件]](#update-an-event)
* [[!UICONTROL 观看活动]](#watch-events)

#### [!UICONTROL 创建事件]

此操作模块将创建新事件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 主题]</td> 
   <td> <p>输入或映射已创建事件的标题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 开始日期]</td> 
   <td> 输入事件在合并日期和时间表示法中开始时的单个时间点。 使用格式<code>{date}T{time}</code>；例如，<code>2017-08-29T04:00:00.0000000</code>。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 结束日期]</td> 
   <td> 输入事件以组合日期和时间表示结束时的单一时间点。 使用格式<code>{date}T{time}</code>；例如，<code>2017-08-29T04:00:00.0000000</code>。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 提醒时间]</td> 
   <td>选择是否要激活此事件的提醒。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 提醒]</td> 
   <td>输入或映射提醒触发时事件开始前的分钟数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 重要性]</td> 
   <td> <p>选择此事件的重要性。</p> 
    <ul> 
     <li>[!UICONTROL 低]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL 高]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 敏感度] </td> 
   <td> <p>选择此事件的敏感度。</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>收件人看到“[!UICONTROL 请将其视为个人]”消息。</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>收件人看到“[!UICONTROL 请将其视为私人]”消息。 收件人的收件箱规则不会转发或重定向此事件。</p> </li> 
     <li> <p><strong>[!UICONTROL 机密]</strong> </p> <p>收件人看到“[!UICONTROL 请将其视为机密]”消息。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 正文内容类型]</td> 
   <td>选择正文内容是纯文本还是HTML。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 正文内容]</td> 
   <td>输入或映射与事件关联的消息正文。 它可以采用HTML或文本格式（如上面[!UICONTROL 正文内容类型]字段中所指定）。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 位置]</td> 
   <td> <p>输入或映射事件位置详细信息。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">已请求[!UICONTROL 响应]</td> 
   <td>选择<strong>[!UICONTROL 是]</strong>以请求被邀请者发送对活动邀请的响应。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 显示为]</td> 
   <td> <p>选择您希望向查看您的日历的人员显示事件的方式。</p> 
    <ul> 
     <li>[!UICONTROL 自由]</li> 
     <li>[!UICONTROL 暂定]</li> 
     <li>[!UICONTROL 忙]</li> 
     <li>[!UICONTROL 外出]</li> 
     <li>[!UICONTROL 在其他位置工作]</li> 
     <li>[!UICONTROL 未知]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 与会者]</p> </td> 
   <td> <p>对于每个要邀请的与会者，单击“<b>添加项目</b>”并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 名称]</strong> </p> <p>输入或映射与会者的姓名。</p> </li> 
     <li> <p><strong>[!UICONTROL 电子邮件]</strong> </p> <p>输入或映射与会者的电子邮件地址。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 类别]</td> 
   <td>对于您希望事件在日历中显示为的每个类别，单击<b>添加项目</b>，然后输入或映射该类别。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除事件]

此操作模块删除现有事件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 事件ID]</td> 
   <td> <p>输入或映射要删除的事件的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取事件]

此操作模块可检索指定事件的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 事件ID]</td> 
   <td> <p>输入或映射要检索其详细信息的事件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索事件]

在选定日历中创建、更新、删除、开始或结束事件时，此搜索模块会检索该事件的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日历组ID]</td> 
   <td>选择包含要监视其活动的日历的[!UICONTROL 日历组]。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日历]</td> 
   <td> <p>选择要监视的特定日历。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 筛选器]</td> 
   <td> <p>设置筛选条件以筛选结果。 您可以按以下属性进行筛选：</p> 
    <ul> 
     <li>[!UICONTROL 主题]</li> 
     <li>[!UICONTROL 事件ID]</li> 
     <li>[!UICONTROL 创建日期时间]</li> 
     <li>[!UICONTROL 上次修改日期时间]</li> 
     <li>[!UICONTROL 正文预览]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td> <p>选择您希望对结果进行排序的方式。</p> 
    <ul> 
     <li><strong>[!UICONTROL 主题]</strong>，升序或降序</li> 
     <li><strong>[!UICONTROL 创建日期时间]</strong>，升序或降序</li> 
     <li><strong>[!UICONTROL 上次修改日期时间]</strong>，升序或降序</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入一个场景执行周期内Workfront Fusion应返回的最大事件数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新事件]

此操作模块更新现有事件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 事件ID]</td> 
   <td>输入、映射或选择要更新的事件ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 主题]</td> 
   <td> <p>输入或映射事件的新标题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 开始日期]</td> 
   <td> 输入事件在合并日期和时间表示法中开始时的单个时间点。 使用格式<code>{date}T{time}</code>；例如，<code>2017-08-29T04:00:00.0000000</code>。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 结束日期]</td> 
   <td> 输入事件以组合日期和时间表示结束时的单一时间点。 使用格式<code>({date}T{time}</code>；例如，<code>2017-08-29T04:00:00.0000000</code>。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 提醒时间]</td> 
   <td>选择是否要激活此事件的提醒。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 提醒]</td> 
   <td>输入或映射提醒触发时事件开始前的分钟数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 重要性]</td> 
   <td> <p>选择此事件的重要性。</p> 
    <ul> 
     <li>[!UICONTROL 低]</li> 
     <li>[!UICONTROL Medium]</li> 
     <li>[!UICONTROL 高]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 敏感度] </td> 
   <td> <p>选择此事件的敏感度。</p> 
    <ul> 
     <li><strong>[!UICONTROL Normal]</strong> </li> 
     <li> <p><strong>[!UICONTROL Personal]</strong> </p> <p>收件人看到“[!UICONTROL 请将其视为个人]”消息。</p> </li> 
     <li> <p><strong>[!UICONTROL Private]</strong> </p> <p>收件人看到“[!UICONTROL 请将其视为私人]”消息。 收件人的收件箱规则不会转发或重定向此事件。</p> </li> 
     <li> <p><strong>[!UICONTROL 机密]</strong> </p> <p>收件人看到“[!UICONTROL 请将其视为机密]”消息。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 正文内容类型]</td> 
   <td>选择与事件关联的消息正文内容是纯文本还是HTML。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 正文内容]</td> 
   <td>输入或映射与事件关联的消息正文。 它可以采用HTML或文本格式（如上面[!UICONTROL 正文内容类型]字段中所指定）。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 位置]</td> 
   <td> <p>输入事件位置详细信息。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">已请求[!UICONTROL 响应]</td> 
   <td>选择<strong>[!UICONTROL 是]</strong>以请求被邀请者发送对活动邀请的响应。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 显示为]</td> 
   <td> <p>选择您希望向查看您的日历的人员显示事件的方式。</p> 
    <ul> 
     <li>[!UICONTROL 自由]</li> 
     <li>[!UICONTROL 暂定]</li> 
     <li>[!UICONTROL 忙]</li> 
     <li>[!UICONTROL 外出]</li> 
     <li>[!UICONTROL 在其他位置工作]</li> 
     <li>[!DNL Unknown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 与会者]</p> </td> 
   <td> <p>添加活动参与者。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 名称]</strong> </p> <p>输入与会者的姓名。</p> </li> 
     <li> <p><strong>[!UICONTROL 电子邮件]</strong> </p> <p>输入与会者的电子邮件地址。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 类别]</td> 
   <td>输入或映射您希望事件在日历中显示为的类别。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看活动]

在选定日历中创建、更新、删除、开始或结束事件时，此触发器模块会检索该事件的详细信息。

>[!NOTE]
>
>要监视某个事件系列的已删除事件，请在[!UICONTROL 监视事件]字段中选择[!UICONTROL 按更新时间]。 此模块不会监视已删除的单个事件或删除的事件系列。


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 监视事件]</td> 
   <td> <p>选择您希望如何观看活动。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL ，按创建时间]</strong> </p> <p>留意新活动。</p> </li> 
     <li> <p><strong>[!UICONTROL ，按更新时间]</strong> </p> <p>观看更新的活动。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日历组ID]</td> 
   <td>选择包含要监视其活动的日历的[!UICONTROL 日历组]。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日历]</td> 
   <td> <p>选择要监视的特定日历。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 筛选器]</td> 
   <td>设置筛选条件以按主题、事件ID或正文筛选结果。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入Workfront Fusion在一个场景执行周期内应返回的最大消息数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 日程表

* [[!UICONTROL 创建日历]](#create-a-calendar)
* [[!UICONTROL 删除日历]](#delete-a-calendar)
* [[!UICONTROL 获取日历]](#get-a-calendar)
* [[!UICONTROL 列出日历]](#list-calendars)
* [[!UICONTROL 更新日历]](#update-a-calendar)



#### [!UICONTROL 创建日历]

此操作模块在您的Office 365帐户中创建新日历。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日历名称]</td> 
   <td> <p>输入新日历的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除日历]

此操作模块删除现有日历。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日历ID]</td> 
   <td>输入要删除的日历的[!UICONTROL 日历] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取日历]

此操作模块可检索有关单个日历的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日历ID]</td> 
   <td> <p>输入或映射要检索其详细信息的日历ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出日历]

此搜索模块可检索所有经过身份验证的用户日历的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日历组ID]</td> 
   <td>选择包含要列出的日历的[!UICONTROL 日历组]。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入Workfront Fusion应在一个方案执行周期内返回的最大日历数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新日历]

此操作模块编辑现有日历。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日历ID]</td> 
   <td>输入要更新的日历的[!UICONTROL 日历ID]。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 新日历名称]</td> 
   <td> <p>输入日历的新名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

#### [!UICONTROL 进行API调用]

此模块允许您执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>输入相对于<code>https://graph.microsoft.com</code>的路径。 示例：<code> /v1.0/me/events</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 方法]</p> </td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 例如：<code>{"Content-type":"application/json"}</code>。Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p> 以标准JSON对象的形式添加API调用的查询。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：   <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
