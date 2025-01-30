---
title: Google Forms模块
description: 通过 [!DNL Adobe Workfront Fusion Google Forms] 模块，您可以在Google Forms上监视、选择、添加、更新或删除响应。
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 1%

---

# [!DNL Google Forms]模块

[!DNL Adobe Workfront Fusion] [!DNL Google Forms]模块允许您监视、选择、添加、更新或删除您的[!DNL Google Forms]响应。

要将[!DNL Google Docs]与[!DNL Adobe Workfront Fusion]一起使用，需要具有[!DNL Google]帐户。 如果您还没有[!DNL Google]帐户，则可以在[!DNL Google]帐户帮助页面中创建一个帐户。

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

要使用[!DNL Google Forms]模块，您必须具有[!DNL Google]帐户。

## Google Forms API信息

Google Forms连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>2.0.10</td> 
  </tr>
 </tbody> 
 </table>

## 从表单创建电子表格

为了处理表单响应，必须创建响应中的电子表格。

1. 打开您的表单。
1. 转到 **[!UICONTROL Responses]** 选项卡。
1. 单击&#x200B;**[!UICONTROL Create Spreadsheet]**&#x200B;图标![电子表格图标](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png)。

1. 选择要创建新电子表格还是现有电子表格
1. 单击 **[!UICONTROL Create]**。

## [!DNL Google Forms]模块及其字段

配置[!DNL Google Forms]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Google Forms]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!UICONTROL Watch Responses]

查看表单以获取新响应。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>选择电子表格，其中包含您要监视新响应的表单中的响应。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Row with headers]</td> 
   <td>指定表的标题行。 默认行是<code>A1:Z1</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>指定您希望如何在输出中呈现值。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong> </p> <p>将根据单元格的格式在回复中计算和设置值的格式。 格式设置基于电子表格的区域设置，而不是请求用户的区域设置。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回<code>$1. 23</code>。</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>会计算值，但不在回复中设置格式。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回数字<code>1. 23</code>。</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>不计算值。 回复包括公式。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回<code>=A1</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Date and time render option]</td> 
   <td>选择您希望日期、时间和持续时间在输出中的表示方式。 如果[!UICONTROL Value Render Option]设置为[!UICONTROL Formatted Value]，则忽略此字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p> 设置[!DNL Workfront Fusion]在一个周期内处理的最大响应数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Add a Response]](#add-a-response)
* [[!UICONTROL Update a Response]](#update-a-response)
* [[!UICONTROL Delete a Response]](#delete-a-response)

#### [!UICONTROL Add a Response]

此模块会将新响应附加到表单电子表格的底部。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>选择包含要添加响应的工作表的电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>输入工作表列的所需值。</p> <p>对于格式正确的[!UICONTROL Timestamp]列，请使用以下值：</p><pre>formatDate（现在；DD/MM/YYYY HH：mm；UTC）</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> 用户输入的值不会进行解析，而是按原样存储。 </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>这些值会像用户在UI中键入值一样进行解析。 数字仍为数字，但字符串可能会转换为数字、日期或其他格式，这些规则与通过[!DNL Google Sheets] UI在单元格中输入文本时应用的规则相同。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Insert data option]</td> 
   <td> <p>指定在输入新数据时如何更改现有数据。 </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Overwrite]</strong> </p> <p>新数据将覆盖其写入区域中的现有数据。 将数据添加到工作表末尾会插入新的行或列，以便写入数据。</p> </li> 
     <li> <p><strong>[!UICONTROL Insert rows]</strong></p> <p>为新数据插入行。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a Response]

此模块将更新所选的响应。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>选择包含要更新响应的工作表的电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>输入或映射要更新的行号。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>在所需列中输入新值。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value input option]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> 用户输入的值不会进行解析，而是按原样存储。 </p> </li> 
     <li> <p><strong>[!UICONTROL User entered]</strong></p> <p>这些值会像用户在UI中键入值一样进行解析。 数字仍为数字，但字符串可能会转换为数字、日期或其他格式，这些规则与通过[!DNL Google Sheets] UI在单元格中输入文本时应用的规则相同。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a Response]

此模块删除所选的响应。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>选择包含您要删除响应的工作表的电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sheet]</td> 
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Row number]</p> </td> 
   <td> <p>输入或映射要删除的行数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL Search Responses]](#search-responses)
* [[!UICONTROL Search Responses (Advanced])](#search-responses-advanced)

#### [!UICONTROL Search Responses]

此模块会返回与给定条件匹配的响应。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>连接</td>
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>选择要搜索的表单。</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Sheet] </td>
   <td> <p>选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Column range]</td>
   <td> <p> 选择要搜索的列范围。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>定义要作为搜索响应依据的筛选器。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Sort Order] </td>
   <td> <p>选择是按升序还是降序对返回的响应进行排序。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Order By]</td>
   <td> <p> 选择要对返回的响应排序的列。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Value Render Option]</td> 
   <td> <p>指定您希望如何在输出中呈现值。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Formatted value]</strong></p> <p>将根据单元格的格式在回复中计算和设置值的格式。 格式设置基于电子表格的区域设置，而不是请求用户的区域设置。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回<code>$1. 23</code>。</p> </li> 
     <li> <p><strong>[!UICONTROL Unformatted value]</strong> </p> <p>会计算值，但不在回复中设置格式。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回数字<code>1. 23</code>。</p> </li> 
     <li> <p><strong>[!UICONTROL Formula]</strong> </p> <p>不计算值。 回复包括公式。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回<code>=A1</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL Date and time render option]</td>
    <td>选择您希望日期、时间和持续时间在输出中的表示方式。 如果[!UICONTROL Value Render]选项设置为“格式化值”，则忽略此字段。 </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL Maximum number of returned responses]</td>
   <td> <p> 设置[!DNL Workfront Fusion]在一个周期内返回的最大响应数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Responses (Advanced)]

此模块使用[[!DNL Google Charts Query Language]](https://developers.google.com/chart/interactive/docs/querylanguage)执行搜索。 此模块不返回行号。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>选择包含要搜索的工作表的电子表格。</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Sheet]</td>
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>使用<a href="https://developers.google.com/chart/interactive/docs/querylanguage">[!DNL Google Charts Query Language]</a>定义搜索查询。</p> <p>示例： <code>select * where C = "John"</code>检索C列为“John”的行的所有值。</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Maximum number of returned rows]</td>
   <td> <p> 设置[!DNL Workfront Fusion]在一个周期内返回的最大响应数。</p> </td> 
  </tr> 
 </tbody> 
</table>
