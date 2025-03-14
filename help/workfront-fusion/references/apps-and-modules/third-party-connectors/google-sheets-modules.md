---
title: Google Sheets模块
description: 为了将 [!DNL Google Sheets] 与 [!DNL Adobe Workfront Fusion],you need the [!UICONTROL Workfront Fusion Google Sheets] 扩展一起使用（可选，但是对于即时触发器是必需的）。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 80965570-2937-4ac8-97c0-54f7a813ec50
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '3957'
ht-degree: 0%

---

# [!DNL Google Sheets]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Google Sheets]的工作流，并将其连接到多个第三方应用程序和服务。

有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅[创建与 [!DNL Adobe Workfront Fusion] 的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

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

要使用[!UICONTROL Google工作表]模块，您必须具有[!UICONTROL Google]帐户。

## Google Sheets API信息

Google Sheets连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://sheets.googleapis.com/v4</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v4 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v2.5.7</td> 
  </tr>
 </tbody> 
 </table>

## Google Sheets模块及其字段

配置[!DNL Google Forms]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Google Sheets]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 触发器

#### [!UICONTROL 观察行]

从电子表格中新添加的行检索值。

模块仅检索之前未填充的新行。 触发器不会处理被覆盖的行。

>[!IMPORTANT]
>
>如果工作表包含空白行，则不会处理空白行之后的行。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择包含要监视的工作表的电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作表] </td> 
   <td> <p>选择要监视新行的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL表包含标头]</td> 
   <td> <p> 选择电子表格是否包含标题行。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL是]</strong> </p> <p>模块不会检索标题行作为输出数据。 </p> <p>输出中的变量名称由标头调用。</p> </li> 
     <li> <p><strong>[！UICONTROL编号]</strong> </p> <p>模块还会检索第一个表行</p> <p>输出中的变量名称称为A、B、C、D等。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL带有标题的行] </td> 
   <td> <p>输入标题行的范围。 例如，<code>A1:F1</code>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL第一个表行]</td> 
   <td> <p>输入表第一行的范围。 例如，<code>A1:F1</code>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL值渲染选项]</p> </td> 
   <td> <ul><li><p style="font-weight: bold;">[！UICONTROL格式的值]</p> <p>将根据单元格的格式在回复中计算值并设置其格式。 格式设置基于电子表格的区域设置，而不是请求用户的区域设置。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回<code>"$1.23"</code>。</p></li><li> <p style="font-weight: bold;">[！UICONTROL未格式化的值]</p> <p>系统会计算这些值，但不会在回复中设置格式。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回数字<code>"1.23"</code>。</p></li><li> <p style="font-weight: bold;">[！UICONTROL公式]</p> <p>不会计算值。 回复包括公式。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回<code>"=A1"</code>。</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL日期和时间渲染选项]</p> </td> 
   <td> <ul><li><p style="font-weight: bold;">[！UICONTROL序列号]</p> <p>日期、时间、日期时间和持续时间字段以“序列号”格式输出为两倍，由Lotus 1-2-3推广。 值的整数部分（小数点左侧）计算自1899年12月30日以来的天数。 小数部分（小数的右侧）将时间计为一天中的小数。 例如，1900年1月1日中午是2.5， 2 ，因为是在1899年12月30日后的2天， 0.5 ，因为中午是半天。 1900年2月1日下午3点将为33:625。这正确地将1900年视为非闰年。</p> </li><li><p style="font-weight: bold;">[！UICONTROL格式字符串]</p> <p>日期、时间、日期时间和持续时间字段以其给定的数字格式（取决于电子表格的区域设置）作为字符串输出。</p></li><ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制] </td> 
   <td> <p>设置[!DNL Workfront Fusion]在一个执行周期内可处理的最大结果数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 添加行]](#add-a-row)
* [[!UICONTROL 添加工作表]](#add-a-sheet)
* [[!UICONTROL 清除单元格]](#clear-a-cell)
* [[!UICONTROL 清除行]](#clear-a-row)
* [[!UICONTROL 创建电子表格]](#create-a-spreadsheet)
* [[!UICONTROL 删除行]](#delete-a-row)
* [[!UICONTROL 删除工作表]](#delete-a-sheet)
* [[!UICONTROL 获取单元格]](#get-a-cell)
* [[!UICONTROL 进行API调用]](#make-an-api-call)
* [[!UICONTROL 更新单元格]](#update-a-cell)
* [[!UICONTROL 更新行]](#update-a-row)

#### [!UICONTROL 添加行]

此模块用于在工作表中添加行。

配置[!DNL Google Sheets]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Google Sheets]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL模式]</td> 
   <td> <p>选择您要手动还是通过映射选择电子表格和工作表。</p> <p>注意：手动映射很有用，例如，在[!DNL Workfront Fusion]方案中创建新电子表格时，而您希望将数据直接添加到方案中新建的电子表格中。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择[!DNL Google]电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>选择要向其添加行的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL列范围]</td> 
   <td>选择要使用的列范围。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL表包含标头]</td> 
   <td> <p> 选择电子表格是否包含标题行。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL是]</strong> </p> <p>模块不会检索标题行作为输出数据。 </p> <p>输出中的变量名称由标头调用。</p> </li> 
     <li> <p><strong>[！UICONTROL编号]</strong> </p> <p>模块还会检索第一个表行</p> <p>输出中的变量名称称为A、B、C、D等。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Values] </td> 
   <td> <p>在要添加的行中输入或映射所需的单元格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL值输入选项]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[！UICONTROL用户已进入]</strong></p> <p>这些值会像用户在UI中键入值一样进行解析。 数字仍为数字，但字符串可能会转换为数字、日期或其他格式，这些规则与通过[!DNL Google Sheets] UI在单元格中输入文本时应用的规则相同。</p> </li> 
     <li> <p><strong>[！UICONTROL Raw]</strong> </p> <p> 用户输入的值不会进行解析，并且会在输入时进行存储。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Insert data option]</td> 
   <td> <p>指定在输入新数据时如何更改现有数据。 </p> 
    <ul> 
     <li> <p><strong>[！UICONTROL插入行]</strong></p> <p>为新数据插入行。</p> </li> 
     <li> <p><strong>[！UICONTROL覆盖]</strong> </p> <p>新数据将覆盖其写入区域中的现有数据。 将数据添加到工作表末尾会插入新的行或列，以便写入数据。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 添加工作表]

在选定电子表格中创建新工作表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择要添加工作表的Google电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL属性]</td> 
   <td> 
    <ul> 
     <li> <p style="font-weight: bold;">[！UICONTROL标题]</p> <p>输入新工作表的名称。</p> </li> 
     <li> <p style="font-weight: bold;">[！UICONTROL索引]</p> <p>输入工作表位置。 缺省值为0（将页面放在第一位）。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 清除单元格]

从指定的单元格中删除值。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择包含要从中清除单元格的工作表的Google电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>选择要从中清除单元格的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL单元格] </td> 
   <td> <p>输入或映射要清除的单元格的ID。 示例： <code>A5</code>。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 清除行]

从指定行中删除值。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择包含要从中清除行的工作表的[!DNL Google]电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p> 选择要从中清除数据的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL行号]</td> 
   <td> <p>输入要从中清除数据的行的编号。 示例： <code> 23</code>。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建电子表格]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL标题] </td> 
   <td> <p>输入新电子表格的名称。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL区域设置]</td> 
   <td> <p>使用以下格式之一输入电子表格的区域设置：</p> 
    <ul> 
     <li>ISO 639-1语言代码，例如 <code>en</code></li> 
     <li>ISO 639-2语言代码，例如<code>haw</code>（如果没有639-1代码）</li> 
     <li>ISO语言代码和国家/地区代码的组合，例如 <code>en_US</code></li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL重新计算间隔]</td> 
   <td> <p>重新计算volatile函数前等待的时间：</p> <ul><li><p style="font-weight: bold;">[！UICONTROL更改时]</p> <p>在每次更改时更新易失性函数。</p></li><li> <p style="font-weight: bold;">[！UICONTROL更改时每分钟]</p> <p>易失性函数在每次更改时和每分钟都会更新。</p></li> <li><p style="font-weight: bold;">[！UICONTROL更改时和每小时]</p> <p>易失性函数会在每次更改时每小时更新一次。</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL时区]</td> 
   <td> <p> 选择电子表格的时区。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL数字格式]</td> 
   <td> <p>选择电子表格中所有单元格的默认格式。</p> <p><strong>[！UICONTROL Text]</strong>：文本格式。 示例： <code>1000. 12</code></p> <p><strong>[！UICONTROL Number]</strong>：数字格式。 示例： <code>1,000.12</code></p> <p><strong>[！UICONTROL百分比]</strong>：格式百分比。 示例： <code>10. 12%</code></p> <p><strong>[！UICONTROL货币]</strong>：货币格式。 示例： <code>$1,000.12</code></p> <p><strong>[！UICONTROL日期]</strong>：日期格式。 示例： <code>9/26/2008</code></p> <p><strong>[！UICONTROL时间]</strong>：时间格式。 示例： <code>3:59:00 PM</code></p> <p><strong>[！UICONTROL日期时间]</strong>：日期和时间格式。 示例： <code>9/26/08 15:59:00</code> </p> <p><strong>[！UICONTROL Scientific]</strong>：科学数字格式。 示例： <code>1. 01E+03</code></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>对于要添加到电子表格的每个工作表，单击<strong>[！UICONTROL添加项]</strong>并输入或映射工作表的标题以及工作表的索引。 索引0表示第一个工作表。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除行]

删除指定的行。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择包含您要从中删除行的工作表的Google电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>电子表格 </td> 
   <td> <p>选择要从中删除行的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>行号</td> 
   <td> <p>输入要删除的行号。 示例： <code>23</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除工作表]

删除特定工作表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择[!DNL Google]电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>选择要删除的工作表。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取单元格]

从选定的单元格中检索值。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择[!DNL Google]电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>选择包含要从中检索数据的单元格的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL单元格] </td> 
   <td> <p>输入要从中检索数据的单元格的ID。 示例： <code>A6</code></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL值渲染选项]</td> 
   <td> <ul><li><p style="font-weight: bold;">[！UICONTROL格式的值]</p> <p>将根据单元格的格式在回复中计算值并设置其格式。 格式设置基于电子表格的区域设置，而不是请求用户的区域设置。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回<code>"$1.23"</code>。</p></li><li> <p style="font-weight: bold;">[！UICONTROL未格式化的值]</p> <p>系统会计算这些值，但不会在回复中设置格式。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回数字<code>"1.23"</code>。</p></li><li> <p style="font-weight: bold;">[！UICONTROL公式]</p> <p>不会计算值。 回复包括公式。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回<code>"=A1"</code>。</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[!DNL Date and time render option]</td> 
   <td> <ul><li><p style="font-weight: bold;">[!DNL Serial number]</p> <p>日期、时间、日期时间和持续时间字段以“序列号”格式输出为两倍，由Lotus 1-2-3推广。 值的整数部分（小数点左侧）计算自1899年12月30日以来的天数。 小数部分（小数的右侧）将时间计为一天中的小数。 例如，1900年1月1日中午是2.5， 2 ，因为是在1899年12月30日后的2天， 0.5 ，因为中午是半天。 1900年2月1日下午3点将为33:625。这正确地将1900年视为非闰年。</p></li><li> <p style="font-weight: bold;">[!DNL Formatted string]</p> <p>日期、时间、日期时间和持续时间字段以其给定的数字格式（取决于电子表格的区域设置）作为字符串输出。</p> </li><ul></td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 进行API调用]

此操作模块允许您执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将Google Sheets帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL URL]</p> </td> 
   <td>输入相对于<code>https://sheets.googleapis.com/v4/</code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL方法]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 例如，<code>{"Content-type":"application/json"}</code>。 [!DNL Workfront Fusion]为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串]</td> 
   <td> <p> 以标准JSON对象的形式添加API调用的查询。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：   <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新单元格]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择[!DNL Google]电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>选择要更新单元格的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL单元格] </td> 
   <td> <p>输入要更新的单元格的ID。 示例： <code>A5</code></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL值]</td> 
   <td> <p>输入单元格的新值。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL值输入选项]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[！UICONTROL用户已进入]</strong></p> <p>这些值会像用户在UI中键入值一样进行解析。 数字仍为数字，但字符串可能会转换为数字、日期或其他格式，这些规则与通过[!DNL Google Sheets] UI在单元格中输入文本时应用的规则相同。</p> </li> 
     <li> <p><strong>[！UICONTROL Raw]</strong> </p> <p> 用户输入的值不会进行解析，并且会在输入时进行存储。 </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新行]

此模块允许您更改选定行中的单元格内容。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL模式]</td> 
   <td> <p>选择您要手动还是通过映射选择电子表格和工作表。</p> <p>注意：例如，在[！UICONTROL Workfront Fusion]场景中创建新电子表格，并且您希望将数据直接添加到场景中新创建的电子表格时，手动映射很有用。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择[!DNL Google]电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>选择要在其中更新行的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL行号]</td> 
   <td> <p> 输入要更新的行号。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL表包含标头]</td> 
   <td> <p> 选择电子表格是否包含标题行。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL是]</strong> </p> <p>模块不会检索标题行作为输出数据。 </p> <p>输出中的变量名称由标头调用。</p> </li> 
     <li> <p><strong>[！UICONTROL编号]</strong> </p> <p>模块还会检索第一个表行</p> <p>输出中的变量名称称为A、B、C、D等。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Values] </td> 
   <td> <p>输入值或将值映射到要更改（更新）的行的所需单元格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL值输入选项]</td> 
   <td> 
    <ul> 
     <li> <p><strong>[！UICONTROL用户已进入]</strong></p> <p>这些值会像用户在UI中键入值一样进行解析。 数字仍为数字，但字符串可能会转换为数字、日期或其他格式，这些规则与通过[!DNL Google Sheets] UI在单元格中输入文本时应用的规则相同。</p> </li> 
     <li> <p><strong>[！UICONTROL Raw]</strong> </p> <p> 用户输入的值不会进行解析，并且会在输入时进行存储。 </p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL 获取范围值]](#get-range-values)
* [[!UICONTROL 列表工作表]](#list-sheets)
* [[!UICONTROL 搜索行]](#search-rows)
* [[!UICONTROL 搜索行（高级）]](#search-rows-advanced)

#### [!UICONTROL 获取范围值]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择[!DNL Google]电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>选择要从中获取范围内容的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL范围] </td> 
   <td> <p>输入要获取的范围。 示例： <code>A1:D25</code>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL表包含标头]</td> 
   <td> <p>如果工作表具有标题行，请选中此框</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL带有标题的行]</td> 
   <td>输入表标题的范围。 示例<code>A1:F1</code>。 如果将字段留空，[!DNL Workfront Fusion]会将指定范围的第一行视为标头。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL值渲染选项]</td> 
   <td> <ul><li><p style="font-weight: bold;">[！UICONTROL格式的值]</p> <p>将根据单元格的格式在回复中计算值并设置其格式。 格式设置基于电子表格的区域设置，而不是请求用户的区域设置。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回<code>"$1.23"</code>。</p></li><li> <p style="font-weight: bold;">[！UICONTROL未格式化的值]</p> <p>系统会计算这些值，但不会在回复中设置格式。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回数字<code>"1.23"</code>。</p></li><li> <p style="font-weight: bold;">[！UICONTROL公式]</p> <p>不会计算值。 回复包括公式。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回<code>"=A1"</code>。</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL日期和时间渲染选项]</td> 
   <td> <ul><li><p style="font-weight: bold;">[！UICONTROL序列号]</p> <p>日期、时间、日期时间和持续时间字段以“序列号”格式输出为两倍，由Lotus 1-2-3推广。 值的整数部分（小数点左侧）计算自1899年12月30日以来的天数。 小数部分（小数的右侧）将时间计为一天中的小数。 例如，1900年1月1日中午是2.5， 2 ，因为是在1899年12月30日后的2天， 0.5 ，因为中午是半天。 1900年2月1日下午3点将为33:625。这正确地将1900年视为非闰年。</p> </li><li><p style="font-weight: bold;">[！UICONTROL格式字符串]</p> <p>日期、时间、日期时间和持续时间字段以其给定的数字格式（取决于电子表格的区域设置）作为字符串输出。</p></li><ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列表工作表]

此模块返回电子表格中所有工作表的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择包含要列出工作表的[!DNL Google]电子表格。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索行]

使用过滤器选项搜索行。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将Google Sheets帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择[!DNL Google]电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>选择要在其中搜索行的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL表包含标头]</td> 
   <td> <p> 选择电子表格是否包含标题行。 如果选择了[！UICONTROL是]选项，则模块不会检索标头行作为输出数据，并且输出中的变量名称随后由标头调用。 如果选择了[！UICONTROL否]选项，则模块还会检索第一个表行，然后输出中的变量名称将仅称为A、B、C、D等。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL列范围]</td> 
   <td>选择要使用的列范围。 示例： <code>A-F</code></td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL筛选器]</td> 
   <td> <p>设置要用于搜索行的筛选器。</p> <!--<p>For more information about filters, see <a href="/help/workfront-fusion/create-scenarios/add-modules/" class="MCXref xref">Add a filter to a scenario in [!UICONTROL Adobe Workfront Fusion]</a>.</p>--> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL排序顺序]</td> 
   <td>选择是要升序排序还是降序排序。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Order by]</td> 
   <td>选择要作为排序依据的列。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL值渲染选项]</td> 
   <td> <ul><li><p style="font-weight: bold;">[！UICONTROL格式的值]</p> <p>将根据单元格的格式在回复中计算值并设置其格式。 格式设置基于电子表格的区域设置，而不是请求用户的区域设置。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回<code>"$1.23"</code>。</p></li><li> <p style="font-weight: bold;">[！UICONTROL未格式化的值]</p> <p>系统会计算这些值，但不会在回复中设置格式。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回数字<code>"1.23"</code>。</p></li><li> <p style="font-weight: bold;">[！UICONTROL公式]</p> <p>不会计算值。 回复包括公式。 例如，如果<code>A1</code>是<code>1.23</code>，<code>A2</code>是<code>=A1</code>并且格式为货币，则<code>A2</code>将返回<code>"=A1"</code>。</p> </li><ul></td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL日期和时间渲染选项]</td> 
   <td> <ul><li><p style="font-weight: bold;">[！UICONTROL序列号]</p> <p>日期、时间、日期时间和持续时间字段以“序列号”格式输出为两倍，由Lotus 1-2-3推广。 值的整数部分（小数点左侧）计算自1899年12月30日以来的天数。 小数部分（小数的右侧）将时间计为一天中的小数。 例如，1900年1月1日中午是2.5， 2 ，因为是在1899年12月30日后的2天， 0.5 ，因为中午是半天。 1900年2月1日下午3点将为33:625。这正确地将1900年视为非闰年。</p> </li><li><p style="font-weight: bold;">[！UICONTROL格式字符串]</p> <p>日期、时间、日期时间和持续时间字段以其给定的数字格式（取决于电子表格的区域设置）作为字符串输出。</p></li><ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL返回的最大行数]</td> 
   <td>设置[!DNL Workfront Fusion]在一个执行周期内返回的最大行数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索行（高级）]

返回与给定条件匹配的结果。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Sheets]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Spreadsheet] </td> 
   <td> <p>选择包含要搜索的工作表的Google电子表格。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL工作表] </td> 
   <td> <p>选择包含要搜索的行的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Query]</td> 
   <td> <p>使用[!DNL Google Charts Query Language]。 示例： <code>select * where B = "John"</code></p> <p>有关[!DNL Google Charts Query Language]的详细信息，请参阅[!DNL Google]文档中的<a href="https://developers.google.com/chart/interactive/docs/querylanguage">查询语言引用</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 使用限制

如果发生错误`429: RESOURCE_EXHAUSTED`，则表示您已超出API速率限制。

[!DNL Google Sheets] API限制每个项目每100秒500个请求，每个用户每100秒100个请求。 对读取和写入的限制将单独进行跟踪。 没有每日使用量限制。

有关更多详细信息，请访问[developers.google.com/sheets/api/limits](https://developers.google.com/sheets/api/limits)。

## 提示和技巧

* [从 [!DNL Google] 工作表中获取空单元格](#get-empty-cells-from-a-google-sheet)
* [在工作表中添加按钮以运行方案](#add-a-button-in-a-sheet-to-run-a-scenario)

### 从[!DNL Google Sheet]获取空单元格

若要获取空单元格，您可以使用[!UICONTROL 搜索行（高级）]模块。 使用此公式可获取空列。

```
select * where E is null
```

其中，“E”是列，“is null”是条件。 您可以使用Google查询语言创建更高级的查询。 有关详细信息，请参阅Google文档中的[Google查询Lang](https://developers.google.com/chart/interactive/docs/querylanguage)。

### 在工作表中添加按钮以运行方案

1. 在[!DNL Workfront Fusion]中，在场景中插入&#x200B;**[!UICONTROL Webhook]** > **[!UICONTROL 自定义Webhook]**&#x200B;模块并对其进行配置。 有关说明，请参阅[Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)。

1. 复制webhook的URL。
1. 执行方案。
1. 在Google工作表中，从主菜单栏中选择&#x200B;**[!UICONTROL 插入]** > **[!UICONTROL 绘图]**...。

1. 在[!UICONTROL 绘图]窗口中，单击窗口顶部附近的&#x200B;**[!UICONTROL 文本框]**&#x200B;图标![文本框](/help/workfront-fusion/references/apps-and-modules/assets/text-box.png)。
1. 设计一个按钮，然后单击右上角的&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;按钮：
1. 该按钮即放置在您的工作表中。 单击按钮右上角的三个垂直圆点：
1. 选择&#x200B;**[!UICONTROL 分配脚本……]。菜单中的**。
1. 输入脚本（函数）的名称，如`runScenario`，然后单击&#x200B;**[!UICONTROL 确定]**：
1. 从主菜单栏中选择&#x200B;**[!UICONTROL 工具]** > **[!UICONTROL 脚本编辑器]**。

1. 插入以下代码：

   * 函数的名称必须对应于您在步骤9中指定的名称。
   * 将URL替换为您在步骤2中复制的webhook URL。

     ```
     function runScenario() {
     UrlFetchApp.fetch("&lt;webhook you copied>");
     }
     ```

1. 按&#x200B;**[!UICONTROL Ctrl+S]**&#x200B;保存脚本文件，输入项目名称，然后单击&#x200B;**[!UICONTROL 确定]**。

1. 切换回[!DNL Google Sheets]并单击新按钮。
1. 向脚本授予所需的授权：
1. 在[!DNL Workfront Fusion]中，验证方案是否已成功执行。

## 在电子表格中存储日期

如果在没有任何格式的电子表格中存储日期值，则该日期值会在电子表格中显示为ISO 8601格式的文本。 但是，使用不了解此文本的日期的[!DNL Google Sheets]公式或函数（示例：公式`=A1+10`）显示以下错误：

![错误](/help/workfront-fusion/references/apps-and-modules/assets/mceclip6-350x87.png)

为了帮助[!DNL Google Sheets]了解日期，请使用`formatDate`函数设置其格式。 传递给函数的正确格式（作为第二个参数）取决于电子表格的区域设置设置。

有关此函数的更多信息，请参阅日期和时间函数一文中的[[!UICONTROL formatDate] (date； format； [timezone])](/help/workfront-fusion/references/mapping-panel/functions/date-and-time-functions.md#formatdate-date-format-timezone)。

要确定正确的格式，请执行以下操作：

1. 在Google Sheets中，从主菜单中选择&#x200B;**[!UICONTROL 文件]** > **[!UICONTROL 电子表格]**&#x200B;设置以验证和设置区域设置。

1. 验证或设置正确的区域设置后，从主菜单中选择&#x200B;**[!UICONTROL 格式]** > **[!UICONTROL 数字]**&#x200B;来确定相应的日期和时间格式。 格式显示在日期时间菜单项旁边：

1. 要撰写应传递到[!UICONTROL formatDate()]函数的正确格式，请参阅[令牌列表以了解日期和时间格式](/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md)。

>[!BEGINSHADEBOX]

**示例：**

对于`MM/DD/YYYY HH:mm:ss`格式（适用于美国区域设置）：

![区域设置时间公式](/help/workfront-fusion/references/apps-and-modules/assets/locale-time-350x83.png)

>[!ENDSHADEBOX]

## 正在利用[!DNL Google Sheets]功能

要使用Google Sheets中的内置函数，您可以对其进行利用。 有关详细信息，请参阅“使用函数映射项”一文中的[使用 [!DNL Google Sheets] 函数](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md#use-google-sheets-functions)。

## 阻止[!DNL Google Sheets]将数字更改为日期

如果用作文本的字符串被解释为[!DNL Google]工作表中的日期，您可以将此数字预设置为纯文本格式以防止出现这种情况。 例如，如果您键入1-2019，打算将其解释为文本，Google可能会将其解释为日期。

1. 在[!DNL Google Sheets]中，突出显示包含数字的列或单元格。
1. 单击&#x200B;**[!UICONTROL 格式]** > **[!UICONTROL 数字]** > **[!UICONTROL 纯文本]**。

[!DNL Workfront Fusion]中的另一种解决方法是在数字前键入撇号(&#39;)，例如，&#39;1-2019或&#39;1/47。 从[!DNL Workfront Fusion]发送数据后，单元格中不显示撇号。
