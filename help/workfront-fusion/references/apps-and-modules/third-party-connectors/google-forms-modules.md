---
title: Google Forms模块
description: 通过 [!DNL Adobe Workfront Fusion Google Forms] 模块，您可以在Google Forms上监视、选择、添加、更新或删除响应。
author: Becky
feature: Workfront Fusion
exl-id: dc017957-c0f8-4206-916f-21ccda346fb9
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1415'
ht-degree: 0%

---

# [!DNL Google Forms]模块

Adobe Workfront Fusion [!DNL Google Forms]模块允许您监视、选择、添加、更新或删除您的[!DNL Google Forms]响应。

要将[!DNL Google Docs]与Adobe Workfront Fusion结合使用，必须具有[!DNL Google]帐户。 如果您还没有[!DNL Google]帐户，则可以在[!DNL Google]帐户帮助页面中创建一个帐户。

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

要处理表单响应，必须先创建响应电子表格。

1. 打开您的表单。
1. 转到&#x200B;**[!UICONTROL 响应]**&#x200B;选项卡。
1. 单击&#x200B;**[!UICONTROL 创建电子表格]**&#x200B;图标![电子表格图标](/help/workfront-fusion/references/apps-and-modules/assets/spreadsheet-icon.png)。

1. 选择要创建新电子表格还是现有电子表格
1. 单击&#x200B;**[!UICONTROL 创建]**。

## [!DNL Google Forms]模块及其字段

在配置[!DNL Google Forms]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Google Forms]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!UICONTROL 观看回应]

查看表单以获取新响应。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>选择电子表格，其中包含您要监视新响应的表单中的响应。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作表]</td> 
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 带有标题的行]</td> 
   <td>指定表的标题行。 默认行是<code>A1:Z1</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 值渲染选项]</td> 
   <td> <p>指定您希望如何在输出中呈现值。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 格式化的值]</strong> </p> <p>将根据单元格的格式在回复中计算和设置值的格式。 格式设置基于电子表格的区域设置，而不是请求用户的区域设置。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回<code>$1. 23</code>。</p> </li> 
     <li> <p><strong>[!UICONTROL 未格式化的值]</strong> </p> <p>会计算值，但不在回复中设置格式。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回数字<code>1. 23</code>。</p> </li> 
     <li> <p><strong>[!UICONTROL 公式]</strong> </p> <p>不计算值。 回复包括公式。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回<code>=A1</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 日期和时间渲染选项]</td> 
   <td>选择您希望日期、时间和持续时间在输出中的表示方式。 如果[!UICONTROL Value Render Option]设置为[!UICONTROL Formatted Value]，则会忽略此字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p> 设置Workfront Fusion在一个周期内处理的最大响应数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 添加响应]](#add-a-response)
* [[!UICONTROL 删除响应]](#delete-a-response)
* [[!UICONTROL 更新响应]](#update-a-response)

#### [!UICONTROL 添加响应]

此模块会将新响应附加到表单电子表格的底部。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>选择包含要添加响应的工作表的电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作表]</td> 
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>输入工作表列的所需值。 列基于工作表可用。</p> <p>对于[!UICONTROL Timestamp]列，请使用以下值：</p><pre>formatDate（现在；DD/MM/YYYY HH：mm；UTC）</pre> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 值输入选项]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> 用户输入的值不会进行解析，而是按原样存储。 </p> </li> 
     <li> <p><strong>[!UICONTROL 用户已进入]</strong></p> <p>这些值会像用户在UI中键入值一样进行解析。 数字仍为数字，但字符串可能会转换为数字、日期或其他格式，这些规则与通过[!DNL Google Sheets] UI在单元格中输入文本时应用的规则相同。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Insert data option]</td> 
   <td> <p>指定在输入新数据时如何更改现有数据。 </p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 覆盖]</strong> </p> <p>新数据将覆盖其写入区域中的现有数据。 将数据添加到工作表末尾会插入新的行或列，以便写入数据。</p> </li> 
     <li> <p><strong>[!UICONTROL 插入行]</strong></p> <p>为新数据插入行。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除响应]

此模块删除所选的响应。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>选择包含您要删除响应的工作表的电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作表]</td> 
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 行号]</p> </td> 
   <td> <p>输入或映射要删除的行数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新响应]

此模块将更新所选的响应。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Spreadsheet]</td> 
   <td> <p>选择包含要更新响应的工作表的电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作表]</td> 
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 行号]</p> </td> 
   <td> <p>输入或映射要更新的行号。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>为所需列输入新值。 列基于工作表可用。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 值输入选项]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[!UICONTROL Raw]</strong> </p> <p> 用户输入的值不会进行解析，而是按原样存储。 </p> </li> 
     <li> <p><strong>[!UICONTROL 用户已进入]</strong></p> <p>这些值会像用户在UI中键入值一样进行解析。 数字仍为数字，但字符串可能会转换为数字、日期或其他格式，这些规则与通过[!DNL Google Sheets] UI在单元格中输入文本时应用的规则相同。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL 搜索响应]](#search-responses)
* [[!UICONTROL 搜索响应（高级]）](#search-responses-advanced)

#### [!UICONTROL 搜索响应]

此模块会返回与给定条件匹配的响应。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
    <td>连接</td>
   <td> <p>有关将[!DNL Google]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>选择要搜索的表单。</p> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL 工作表] </td>
   <td> <p>选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL 列范围]</td>
   <td> <p> 选择要搜索的列范围。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 筛选器]</td> 
   <td> <p>定义要作为搜索响应依据的筛选器。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL 排序顺序] </td>
   <td> <p>选择是按升序还是降序对返回的响应进行排序。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
    <td>[!UICONTROL Order By]</td>
   <td> <p> 选择要对返回的响应排序的列。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 值渲染选项]</td> 
   <td> <p>指定您希望如何在输出中呈现值。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 格式的值]</strong></p> <p>将根据单元格的格式在回复中计算和设置值的格式。 格式设置基于电子表格的区域设置，而不是请求用户的区域设置。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回<code>$1. 23</code>。</p> </li> 
     <li> <p><strong>[!UICONTROL 未格式化的值]</strong> </p> <p>会计算值，但不在回复中设置格式。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回数字<code>1. 23</code>。</p> </li> 
     <li> <p><strong>[!UICONTROL 公式]</strong> </p> <p>不计算值。 回复包括公式。 例如，如果<code>A1</code>是<code>1. 23</code>，<code>A2 </code>是<code>=A1</code>并且格式为货币，则<code>A2</code>返回<code>=A1</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions="">
    <td>[!UICONTROL 日期和时间渲染选项]</td>
    <td>选择您希望日期、时间和持续时间在输出中的表示方式。 如果[!UICONTROL Value Render]选项设置为“格式化的值”，则忽略此字段。 </td>
  </tr> 
  <tr>
    <td role="rowheader">[!UICONTROL 返回的最大响应数]</td>
   <td> <p> 设置Workfront Fusion在一个周期内返回的最大响应数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索响应（高级）]

此模块使用[[!DNL Google Charts Query Language]](https://developers.google.com/chart/interactive/docs/querylanguage)执行搜索。 此模块不返回行号。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Google]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL Spreadsheet]</td>
   <td> <p>选择包含要搜索的工作表的电子表格。</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL 工作表]</td>
   <td> <p> 选择包含表单响应的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>使用<a href="https://developers.google.com/chart/interactive/docs/querylanguage">[!DNL Google Charts Query Language]</a>定义搜索查询。</p> <p>示例： <code>select * where C = "John"</code>检索C列为“John”的行的所有值。</p> </td> 
  </tr> 
  <tr>
    <td>[!UICONTROL 返回的最大行数]</td>
   <td> <p> 设置Workfront Fusion在一个周期内返回的最大响应数。</p> </td> 
  </tr> 
 </tbody> 
</table>
