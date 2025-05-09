---
title: Google日历模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Google Calendar的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: 160e503adeca5404e18fd0cba9f475fee8510a48
workflow-type: tm+mt
source-wordcount: '2315'
ht-degree: 0%

---

# [!DNL Google Calendar]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!UICONTROL Google Calendar]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL Google Calendar]模块，您必须具有[!DNL Google]帐户。

## Google日历API信息

Google Calendar连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://www.googleapis.com/calendar/v3</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v5.4.5</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Calendar]模块及其字段

配置[!DNL Google Calendar]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Google Calendar]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [触发器](#triggers)
* [操作](#actions)
* [迭代器](#iterators)

### 触发器

* [观看活动](#watch-events)
* [观看活动（即时）](#watch-events-instant)

#### 观看活动

此触发器模块执行在您指定的日历中添加、更新、删除、启动或结束新事件的场景。 该模块返回与一个或多个记录关联的所有标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe的连接[!DNL Workfront Fusion] — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>选择您希望模块使用的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch]</td> 
   <td> <p>选择是只观看新活动，还是观看新活动和所有更改。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>启用此选项可包含已删除的事件。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>输入要返回结果的文本。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> 设置[!DNL Workfront Fusion]在一个周期内处理的最大事件数（每个方案运行的重复次数）。 如果该值设置得过高，则可能会中断与给定第三方服务的连接（超时）。 [!DNL Workfront Fusion]对此没有影响。 我们建议您设置较低的值，并为最大循环数定义较高的值，或者更频繁地运行方案。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 观看活动（即时）

此触发器模块使用mailhook创建电子邮件地址，您可以将其用作事件的邀请者。 模块会根据邀请电子邮件地址参加的事件启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Mailhook] </td> 
   <td> <p>选择要用于此模块的mailhook。 要创建新的邮件挂钩，请单击<b>添加</b>，然后输入要用于邮件挂钩的连接。</p><p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe的连接[!DNL Workfront Fusion] — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of events]</td> 
   <td> <p> 设置[!DNL Workfront Fusion]在一个周期内处理的最大事件数（每个方案运行的重复次数）。 如果该值设置得过高，则可能会中断与给定第三方服务的连接（超时）。 [!DNL Workfront Fusion]对此没有影响。 我们建议您设置较低的值，并为最大循环数定义较高的值，或者更频繁地运行方案。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [创建日历](#create-a-calendar)
* [创建事件](#create-an-event)
* [删除事件](#delete-an-event)
* [获取事件](#get-events)
* [更新事件](#update-an-event)

#### 创建日历

此操作模块将创建与帐户关联的日历。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe的连接[!DNL Workfront Fusion] — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color] </td> 
   <td> <p>选择要与日历关联的颜色。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name] </td> 
   <td> <p>输入或映射新日历的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an event]

此操作模块创建一个事件。

您可以指定事件的日历和参数。

模块会返回事件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>有关将[!DNL Google Calendar]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>选择要显示事件的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Color]</td> 
   <td>选择事件在日历上显示的颜色。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> 输入或映射事件的名称。 </p> <p>注意：如果您在[!UICONTROL Create an event]字段中选择了[!UICONTROL Quick add]，则可以包含事件的日期和时间，并且[!DNL Workfront Fusion]将为该日期和时间创建事件。 示例： <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>。 如果您选择了[!UICONTROL Quick add]，但未在事件名称中包含日期和时间，则事件将从当前时间创建，并持续一小时。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>如果事件是全天事件（不需要开始和结束时间），则启用此选项。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>输入或映射事件的开始日期和时间。 </p> <p>有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> 输入或映射事件的结束日期和时间。 </p> <p>有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>输入或映射事件的描述。 此字段支持HTML。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>在文本表单中输入事件的位置。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>启用此选项可使用默认提醒设置。 如果您在[!UICONTROL Reminder]字段中设置了自定义提醒，此值将设置为“否”。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>添加事件提醒。 对于要添加的每个提醒，单击<b>添加项</b>，然后选择要用于提醒的方法，并定义要提醒的事件之前的时长（以分钟为单位）。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>将与会者添加到活动。 对于每个与会者，单击<b>添加与会者</b>，然后输入或映射其姓名和电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>选择您希望查看您的日历的人员在此活动期间将您视为“忙碌”或“可用”。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>选择此事件的可见性。 </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>该事件具有您在日历设置中设置的可见性。</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>与该日历共享的任何人都可以查看此事件。</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>只有与会者才能看到此活动。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>选择是将有关创建新事件的通知发送给所有来宾、非[!DNL Google Calendar]来宾还是不发送给任何人。</p> <p>提示：我们建议仅在迁移用例中使用[!UICONTROL None]选项。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>如果希望来宾能够修改此事件，请启用此选项。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>添加要应用于此事件的任何周期性规则。 每个规则都需要一个包含[!UICONTROL RRULE]、[!UICONTROL EXRULE]、[!UICONTROL RDATE]和[!UICONTROL EXDATE]行的定期事件列表。 请注意，此字段不允许有[!UICONTROL DTSTART]和[!UICONTROL DTEND]行；事件开始和结束时间在开始和结束字段中指定。 对于单个事件或定期事件的实例，将忽略此字段。 有关详细信息，请参阅<a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an event]

此操作模块删除事件。

请指定日历和事件ID。

模块会返回事件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe的连接[!DNL Workfront Fusion] — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>选择包含要删除的事件的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> 输入您要删除的先前创建的[!DNL Google Calendar]事件的事件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get events]

此模块根据您指定的标准检索有关选定日历中的事件的信息。

指定搜索的日历和参数。

模块会返回事件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>有关将[!DNL Google Calendar]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar]</td> 
   <td> <p>选择要为其检索事件的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> 输入或映射事件开始的日期。 此模块还会检索在此日期之前开始的、在输入的开始日期仍然发生的事件。 </p> <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> 输入或映射事件结束的日期。 </p> <p> 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Single events]</td> 
   <td> <p> 启用此选项可将定期事件视为单个实例。 例如，如果您有一个每周会议并且启用了此选项，模块会将每周的会议作为单独事件返回。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query]</td> 
   <td> <p>输入或映射要作为搜索依据的搜索词。 </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Order by]</td> 
   <td> <p>选择结果中返回的事件的顺序。</p> 
    <ul> 
     <li><strong>[!UICONTROL Start Time]</strong>：按开始日期和时间排序（升序）。 这仅在查询单个事件时可用。</li> 
     <li><strong>[!UICONTROL Updated Time]</strong>：按上次修改时间排序（升序）。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mazimum number of returned events]</td> 
   <td> <p>设置在一个执行周期内返回的最大事件数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an event]

此操作模块更改现有事件。

请指定日历和事件ID。

模块会返回事件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe的连接[!DNL Workfront Fusion] — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>选择要使用的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>输入先前创建的[!DNL Google Calendar]事件中要更新的事件ID。</p> </td> 
  </tr>   <tr> 
   <td>[!UICONTROL Event name]</td> 
   <td> <p> 输入或映射事件的名称。 </p> <p>注意：如果您在[!UICONTROL Create an event]字段中选择了[!UICONTROL Quick add]，则可以包含事件的日期和时间，并且[!DNL Workfront Fusion]将为该日期和时间创建事件。 示例： <code>Appointment at Capitol Hill on June 3rd 10am-10:25am</code>。 如果您选择了[!UICONTROL Quick add]，但未在事件名称中包含日期和时间，则事件将从当前时间创建，并持续一小时。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL All day event]</td> 
   <td>如果事件是全天事件（不需要开始和结束时间），则启用此选项。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p>输入或映射事件的开始日期和时间。 </p> <p>有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> 输入或映射事件的结束日期和时间。 </p> <p>有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Description]</td> 
   <td>输入或映射事件的描述。 此字段支持HTML。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Location]</td> 
   <td>在文本表单中输入事件的位置。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Use the default reminder settings for this event]</td> 
   <td>启用此选项可使用默认提醒设置。 如果您在[!UICONTROL Reminder]字段中设置了自定义提醒，此值将设置为“否”。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reminder] </td> 
   <td> <p>添加事件提醒。 对于要添加的每个提醒，单击<b>添加项</b>，然后选择要用于提醒的方法，并定义要提醒的事件之前的时长（以分钟为单位）。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>将与会者添加到活动。 对于每个与会者，单击<b>添加与会者</b>，然后输入或映射其姓名和电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show me as]</td> 
   <td>选择您希望查看您的日历的人员在此活动期间将您视为“忙碌”或“可用”。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Visibility] </td> 
   <td> <p>选择此事件的可见性。 </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Default]</b></p> <p>该事件具有您在日历设置中设置的可见性。</p> </li> 
     <li> <p><b>[!UICONTROL Public]</b></p> <p>与该日历共享的任何人都可以查看此事件。</p> </li> 
     <li> <p><b>[!UICONTROL Private]</b></p> <p>只有与会者才能看到此活动。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event creation]</td> 
   <td> <p>选择是将有关创建新事件的通知发送给所有来宾、非[!DNL Google Calendar]来宾还是不发送给任何人。</p> <p>提示：我们建议仅在迁移用例中使用[!UICONTROL None]选项。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Guests can modify the event]</td> 
   <td> <p>如果希望来宾能够修改此事件，请启用此选项。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Recurrence]</td> 
   <td>添加要应用于此事件的任何周期性规则。 每个规则都需要一个包含[!UICONTROL RRULE]、[!UICONTROL EXRULE]、[!UICONTROL RDATE]和[!UICONTROL EXDATE]行的定期事件列表。 请注意，此字段不允许有[!UICONTROL DTSTART]和[!UICONTROL DTEND]行；事件开始和结束时间在开始和结束字段中指定。 对于单个事件或定期事件的实例，将忽略此字段。 有关详细信息，请参阅<a href="https://tools.ietf.org/html/rfc5545#section-3.8.5">RFC5545</a>。</td> 
  </tr>

</tbody> 
</table>

### 迭代器

#### 迭代附件

此操作模块循环访问事件的附件，并将每个附件输出到单独的捆绑包中。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> 在此方案中选择输出包含要迭代的附件的事件的模块。 </td> 
  </tr> 
 </tbody> 
</table>

#### 迭代与会者

此操作模块针对某项活动循环访问与会者，并将每个与会者输出为一个单独的组合。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> 在此方案中选择输出包含要迭代的参与者的事件的模块。 </td> 
  </tr> 
 </tbody> 
</table>





## 在事件之前触发方案

借助标准[!DNL Google Calendar]电子邮件提醒和[!UICONTROL Webhooks] >[!UICONTROL Custom mailhook]模块，您可以在事件之前的指定时间触发方案。

1. 使用[!UICONTROL Google Calendar] >[!UICONTROL Update an event]模块向活动添加电子邮件提醒：

   ![在事件之前触发方案](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

1. 创建以[!UICONTROL Webhooks] >[!UICONTROL Custom mailhook]模块开头的新方案。

   1. 复制mailhook的电子邮件地址。
   1. 保存场景并执行它。

1. 在[!DNL Gmail]中，将[!DNL Google Calendar]电子邮件提醒重定向到邮件挂接的电子邮件地址：

   1. 打开您的&#x200B;**[!UICONTROL [!DNL Gmail] settings]**。
   1. 打开&#x200B;**[!UICONTROL Forwarding and POP/IMAP]**&#x200B;选项卡。
   1. 单击&#x200B;**[!UICONTROL Add a forwarding address].**
   1. 粘贴复制的邮件挂接的电子邮件地址，单击&#x200B;**[!UICONTROL Next]**，在弹出窗口中按&#x200B;**[!UICONTROL Proceed]**&#x200B;进行确认，然后单击&#x200B;**[!UICONTROL OK]**。

   1. 在[!DNL Workfront Fusion]中，切换到应通过接收确认电子邮件完成其执行的新方案。
   1. 单击模块上方的气泡以检查模块的输出。
   1. 展开`Text`项目并复制确认代码：

      ![确认码](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. 在Gmail中，将确认代码粘贴到编辑框中，然后单击&#x200B;**[!UICONTROL Verify]**：

      ![粘贴代码](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. 打开&#x200B;**[!UICONTROL Filters and Blocked Addresses]**&#x200B;选项卡。
   1. 单击 **[!UICONTROL Create a new filter]**。
   1. 为来自`     calendar-notification@google.com`的所有电子邮件设置过滤器，然后单击&#x200B;**[!UICONTROL Create a filter]**：
   1. 选择&#x200B;**[!UICONTROL Forward it to]**&#x200B;并从列表中选择邮件挂接的电子邮件地址。
   1. 单击&#x200B;**[!UICONTROL Create filter]**&#x200B;以创建筛选器。

1. （可选）在[!DNL Workfront Fusion]中，在[!UICONTROL Webhooks] >[!UICONTROL Custom mailhook]模块之后添加[!UICONTROL Text parser] > [!UICONTROL Match pattern]模块，以分析电子邮件的HTML代码以获取您需要的任何信息。

   例如，您可以按如下方式配置模块，以获取事件的ID：

   *模式*： `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *文本*：从[!UICONTROL Webhooks] >[!UICONTROL Custom mailhook]模块输出的`HTML content`项。
