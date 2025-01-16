---
title: Google日历模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Google Calendar的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 6e514204-cd8e-4f30-bbbb-b8fbe48fc670
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '3312'
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

* [活动](#events)
* [日程表](#calendars)
* [访问控制规则](#access-control-rules)
* [迭代器（已弃用）](#iterators-deprecated)
* [其他](#other)

### 活动

* [[!UICONTROL Watch events]](#watch-events)
* [[!UICONTROL Search events]](#search-events)
* [[!UICONTROL Get an event]](#get-an-event)
* [[!UICONTROL Create an event]](#create-an-event)
* [[!UICONTROL Update an event]](#update-an-event)
* [[!UICONTROL Delete an event]](#delete-an-event)


#### [!UICONTROL Watch events]

此触发器模块执行在您指定的日历中添加、更新、删除、启动或结束新事件的场景。 该模块返回与一个或多个记录关联的所有标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>选择您希望模块使用的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Watch Events]</td> 
   <td> <p>选择要按“创建日期”、“更新日期”、“开始日期”或“结束日期”监视事件。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show deleted events]</td> 
   <td> <p>启用此选项可包含已删除的事件。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Query] </td> 
   <td> <p>输入要搜索的文本。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p> 设置[!DNL Workfront Fusion]在一个周期内处理的最大事件数（每个方案运行的重复次数）。 如果该值设置得过高，则可能会中断与给定第三方服务的连接（超时）。 [!DNL Workfront Fusion]对此没有影响。 我们建议您设置较低的值，并为最大循环数定义较高的值，或者更频繁地运行方案。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search events]

此操作模块在选定日历中搜索事件。

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
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>选择要搜索的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Start date]</td> 
   <td> <p> 输入或映射事件开始的日期。 此模块还会检索在此日期之前开始的、在输入的开始日期仍然发生的事件。 </p> <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> 输入或映射事件结束的日期。 </p> <p> 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </td> 
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
   <td>[!UICONTROL Limit]</td> 
   <td> <p>设置在一个执行周期内返回的最大事件数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an event]

此操作模块返回指定日历中单个事件的元数据。

指定日历和事件。

该模块会返回事件的ID和所有关联的字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>输入或映射包含要获取的事件的日历的ID。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>输入要获取的现有[!DNL Google Calendar]事件的事件ID。</p> </td> 
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
   <td>[!UICONTROL Create an Event]</td> 
   <td> <p>选择您希望如何创建事件。</p> 
    <ul> 
     <li><b>[!UICONTROL In Detail]</b><p>利用此选项，可更详细地介绍该事件。<br></p></li> 
     <li><b>[!UICONTROL Quickly]</b><p>您只需选择日历并输入事件名称即可。 您可以在名称中包含时间和地点详细信息，然后[!DNL Google Calendar]将为该时间和地点安排该事件。</p></li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
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
   <td> <p>如果这是全天事件，请输入事件的起始日期。 </p> <p>有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制转换。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL End date]</td> 
   <td> <p> 如果这是全天事件，请输入事件的结束日期。 </p> <p>有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制转换。</p> </td> 
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
   <td> <p>添加事件提醒。 对于每个提醒，选择要用于提醒的方法，并定义要提醒的事件之前的时长（以分钟为单位）。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attendees]</td> 
   <td>将与会者添加到活动。 为每位与会者输入或映射其姓名和电子邮件地址。</td> 
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
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar] </td> 
   <td> <p>选择要使用的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID] </td> 
   <td> <p>输入先前创建的[!DNL Google Calendar]事件中要更新的事件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

您可以通过在所需字段中输入新值来更新事件信息。 有关各个字段的详细信息，请参阅[[!UICONTROL Create an event]](#create-an-event)。

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
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>选择包含要删除的事件的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Event ID]</td> 
   <td> <p> 输入您要删除的先前创建的[!DNL Google Calendar]事件的事件ID。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notification about the event deletion]</td> 
   <td>选择您希望向所有来宾、未使用[!DNL Google Calendar]的来宾或任何人发送有关事件删除的通知。</td> 
  </tr> 
 </tbody> 
</table>

### 日程表

* [[!UICONTROL List calendars]](#list-calendars)
* [[!UICONTROL Get a calendar]](#get-a-calendar)
* [[!UICONTROL Create a calendar]](#create-a-calendar)
* [[!UICONTROL Update a calendar]](#update-a-calendar)
* [[!UICONTROL Delete a calendar]](#delete-a-calendar)
* [[!UICONTROL Clear a calendar]](#clear-a-calendar)

#### [!UICONTROL List calendars]

此操作模块返回用户日历列表中的日历。

模块会返回日历的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Minimum access role]</td> 
   <td> <p>选择用户的最低访问角色。 模块会根据此最小访问角色返回日历。</p> 
    <ul> 
     <li><strong>[!UICONTROL Free Busy Reader]</strong>：用户可以读取忙/闲信息。 </li> 
     <li><strong>[!UICONTROL Owner]</strong>：用户可以读取和修改事件，并且可以访问控制列表。 </li> 
     <li><strong>[!UICONTROL Reader]</strong>：用户可以读取非私有事件。 </li> 
     <li><strong>[!UICONTROL Writer]</strong>：用户可以读取和修改事件。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show hidden calendars]</td> 
   <td>启用此选项可在模块返回的列表中包含隐藏的日历。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>设置在一个执行周期内返回的最大日历数[!DNL Workfront Fusion]。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get a calendar]

此操作模块可检索日历。

您可以指定要检索的日历ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>选择要检索的日历。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a calendar]

此操作模块将创建新日历。

指定日历的名称。

模块会返回日历的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name]</td> 
   <td> <p> 输入新日历的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a calendar]

此操作模块更新日历。

您可以指定要更新的日历的ID。

模块会返回日历的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>选择要更新的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar name]</td> 
   <td> <p> 输入日历的新名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a calendar]

此操作模块删除日历。

指定要删除的日历的ID。

模块会返回日历的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>输入或映射要删除的日历的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clear a calendar]

此操作模块将从帐户的主日历中删除所有事件。

您可以指定连接到包含要清除的日历的帐户的连接。

模块会返回日历的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
 </tbody> 
</table>

### 访问控制规则

* [[!UICONTROL List access control rules]](#list-access-control-rules)
* [[!UICONTROL Get an access control rule]](#get-an-access-control-rule)
* [[!UICONTROL Create an access control rule]](#create-an-access-control-rule)
* [[!UICONTROL Update an access control rule]](#update-an-access-control-rule)
* [[!UICONTROL Delete an access control rule]](#delete-an-access-control-rule)

#### [!UICONTROL List access control rules]

此操作模块返回日历上访问控制列表中的规则。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>选择包含要检索的访问控制规则的日历。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>设置在一个执行周期内返回的最大结果数[!DNL Workfront Fusion]。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get an access control rule]

此操作模块返回访问控制规则的元数据。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Calendar ID]</td> 
   <td> <p>选择包含要检索的访问控制规则的日历。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Access control rule ID]</td> 
   <td>选择要检索的访问控制规则。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create an access control rule]

此操作模块将创建新的访问控制规则。

指定日历的名称。

该模块会返回访问控制规则的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>选择要创建访问控制规则的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Role]</td> 
   <td> <p>选择要分配给访问规则的角色。 </p> 
    <ul> 
     <li><strong>[!UICONTROL Free Busy Reader]</strong>：用户可以读取忙/闲信息。 </li> 
     <li><strong>[!UICONTROL Owner]</strong>：用户可以读取和修改事件，并且可以访问控制列表。 </li> 
     <li><strong>[!UICONTROL Reader]</strong>：用户可以读取非私有事件。 </li> 
     <li><strong>[!UICONTROL Writer]</strong>：用户可以读取和修改事件。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type]</td> 
   <td> <p>选择范围的类型。 </p> 
    <ul> 
     <li><strong>[!UICONTROL Default]</strong>：公共范围。 这是默认值。 </li> 
     <li><strong>[!UICONTROL User]</strong>：将范围限制为单个用户。 </li> 
     <li><strong>[!UICONTROL Group]</strong>：将范围限制为组。 </li> 
     <li><strong>[!UICONTROL Domain]</strong>：将范围限制为域。 </li> 
    </ul> <p>注意：授予[!UICONTROL Default]或公共范围的权限适用于任何经过身份验证或未经过身份验证的用户。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Value]</td> 
   <td>根据范围类型，输入用户或组的电子邮件地址，或域的名称。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notifications]</td> 
   <td> <p>启用此选项可发送有关访问更改的通知。 </p> <p>注意：访问删除时没有通知。 </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update an access control rule]

此操作模块可更新访问控制规则。

指定日历的名称。

该模块会返回访问控制规则的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>选择包含要更新的访问控制规则的日历。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Access control rule ID]</td> 
   <td>选择要更新的访问控制规则。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Role]</td> 
   <td> <p>选择要分配给访问规则的角色。 </p> 
    <ul> 
     <li><strong>[!UICONTROL None]</strong>：此角色不提供访问权限。</li> 
     <li><strong>[!UICONTROL Free Busy Reader]</strong>：用户可以读取忙/闲信息。 </li> 
     <li><strong>[!UICONTROL Owner]</strong>：用户可以读取和修改事件，并且可以访问控制列表。 </li> 
     <li><strong>[!UICONTROL Reader]</strong>：用户可以读取非私有事件。 </li> 
     <li><strong>[!UICONTROL Writer]</strong>：用户可以读取和修改事件。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Send notifications]</td> 
   <td> <p>启用此选项可发送有关访问更改的通知。 </p> <p>注意：访问删除时没有通知。 </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an access control rule]

此操作模块删除访问控制规则。

指定日历的名称。

该模块会返回访问控制规则的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendar ID]</td> 
   <td> <p>选择或映射包含要删除的访问控制规则的日历的ID。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Access control rule ID]</td> 
   <td>选择或映射要删除的访问控制规则的ID。</td> 
  </tr> 
 </tbody> 
</table>

### 迭代器（已弃用）

已弃用[!UICONTROL iterate attachments]和[!UICONTROL iterate attendees]模块。 若要迭代附件或与会者，请使用[!UICONTROL Flow Control] > [!UICONTROL Iterator]模块。 有关详细信息，请参阅[迭代器模块](/help/workfront-fusion/references/modules/iterator-module.md)

### 其他

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Get Free/Busy Information]](#get-freebusy-information)

#### [!UICONTROL Make an API Call]

此模块允许您执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google Calendar]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td>输入相对于<code>https://www.googleapis.com/calendar</code>的路径。 示例： <code>/v3/users/me/calendarList</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。例如，<code>{"Content-type":"application/json"}</code>。 [!DNL Workfront Fusion]为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p> 以标准JSON对象的形式添加API调用的查询。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：   <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Free/Busy Information]

此操作模块返回一组日历的空闲和忙碌信息。

模块会返回日历的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

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
   <td>[!UICONTROL Minimum time]</td> 
   <td> <p> 输入要检索其信息的间隔的开始。</p> <p> 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum time]</td> 
   <td> <p> 输入要检索其信息的间隔的结束。 </p> <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Calendars]</td> 
   <td> <p>对于要从中检索信息的每个日历，单击<strong>添加</strong>并输入或映射日历ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 在事件之前触发方案

借助标准[!DNL Google Calendar]电子邮件提醒和[!UICONTROL Webhooks] >[!UICONTROL Custom mailhook]模块，您可以在事件之前的指定时间触发方案。

1. 使用[!UICONTROL Google Calendar] >[!UICONTROL Update an event]模块向活动添加电子邮件提醒：

   ![](/help/workfront-fusion/references/apps-and-modules/assets/trigger-scen-before-event-350x209.png)

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

      ![](/help/workfront-fusion/references/apps-and-modules/assets/confirmation-code-350x252.png)

   1. 在Gmail中，将确认代码粘贴到编辑框中，然后单击&#x200B;**[!UICONTROL Verify]**：

      ![](/help/workfront-fusion/references/apps-and-modules/assets/paste-code-350x46.png)

   1. 打开&#x200B;**[!UICONTROL Filters and Blocked Addresses]**&#x200B;选项卡。
   1. 单击 **[!UICONTROL Create a new filter]**。
   1. 为来自`     calendar-notification@google.com`的所有电子邮件设置过滤器，然后单击&#x200B;**[!UICONTROL Create a filter]**：
   1. 选择&#x200B;**[!UICONTROL Forward it to]**&#x200B;并从列表中选择邮件挂接的电子邮件地址。
   1. 单击&#x200B;**[!UICONTROL Create filter]**&#x200B;以创建筛选器。

1. （可选）在[!DNL Workfront Fusion]中，将[!UICONTROL Text parser] > [!UICONTROL Match pattern]模块添加到[!UICONTROL Webhooks] >[!UICONTROL Custom mailhook]模块之后，以分析电子邮件的HTML代码以获取您需要的任何信息。

   例如，您可以按如下方式配置模块，以获取事件的ID：

   *模式*： `<meta itemprop="eventId/googleCalendar" content="(?<evenitID>.*?)"/>`

   *文本*：从[!UICONTROL Webhooks] >[!UICONTROL Custom mailhook]模块输出的`HTML content`项。
