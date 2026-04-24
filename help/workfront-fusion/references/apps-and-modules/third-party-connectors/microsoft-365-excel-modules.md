---
title: Microsoft Office 365 Excel模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Microsoft 365 Excel的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 059bc82b-f1bc-4b92-a44b-51c1daf14f08
source-git-commit: 03f4556d7f903689c85cba966ad875973037a2ba
workflow-type: tm+mt
source-wordcount: '2699'
ht-degree: 18%

---

# [!DNL Microsoft Office 365 Excel] 模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL Microsoft 365 Excel] 的工作流，并将其连接到多个第三方应用程序和服务。

有关创建场景的说明，请参阅[创建场景：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)中的相关文章。

有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的相关文章。

## 访问权限要求

+++ 展开可查看本文所述功能的访问权限要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 包</td> 
   <td> <p>任意 Adobe Workfront Workflow 包以及任意 Adobe Workfront 自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime 和 Select 包，且需额外购买 Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 许可证</td> 
   <td> <p>标准</p><p>工作版或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 许可证</td> 
   <td>
   <p>基于操作：不需要 Workfront Fusion 许可证</p>
   <p>基于连接器（旧版）：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

有关 Adobe Workfront Fusion 许可证的详细信息，请参阅 [Adobe Workfront Fusion 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

要使用[!DNL Microsoft office 365 Excel]，您必须拥有Microsoft帐户。

## Microsoft Office 365 Excel API信息

Microsoft Office 365 Excel连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td> https://graph.microsoft.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 版本</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v2.0.16</td> 
  </tr>
 </tbody> 
 </table>



## 正在将[!DNL Office 365 Excel]服务连接到Workfront Fusion

有关将[!DNL Office 365 Excel]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
>
>例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。

## [!DNL Microsoft Office 365 Excel] 模块及其字段

在您配置 [!DNL Microsoft 365 Excel] 模块时，Workfront Fusion 会显示以下字段。除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Microsoft 365 Excel] 字段。模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [工作簿](#workbook)
* [工作表](#worksheet)
* [表](#table)
* [其他](#other)

### 工作簿

* [下载工作簿](#download-a-workbook)
* [搜索工作簿](#search-workbooks)
* [Watch工作簿](#watch-workbooks)

#### [!UICONTROL 下载工作簿]

此操作模块下载指定Excel工作簿的内容。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Download a workbook]</td> 
   <td> <p>Select how you want to identify the workbook for the module to download.</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL，通过手动输入ID]</strong> </p> <p>在[！UICONTROL工作簿ID]字段中，输入或映射您希望模块下载的特定工作簿的ID。</p> </li> 
     <li> <p>通过从路径中选择<strong>[！UICONTROL]</strong> </p> <p>在[！UICONTROL工作簿]字段中，选择要让模块下载的工作簿，包括不在根文件夹中的路径。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索工作簿]

此操作模块搜索[!DNL Excel]工作簿。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹]</td> 
   <td> <p>选择要搜索工作簿的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 筛选条件]</p> </td> 
   <td> <p>您可以设置过滤器，以仅搜索符合您选择标准的工作簿。</p> <p>对于每个筛选条件，请输入要评估的字段、运算符以及筛选条件应允许的值。您可以通过添加AND或OR规则来使用多个过滤器。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大工作表数。</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL 观看工作簿]

此触发器模块在创建工作簿时启动方案。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文件夹]</td> 
   <td> <p>选择要监视新工作簿的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 筛选条件]</p> </td> 
   <td> <p>您可以将过滤器设置为仅监视符合所选条件的工作簿。</p> <p>对于每个筛选条件，请输入要评估的字段、运算符以及筛选条件应允许的值。您可以通过添加AND或OR规则来使用多个过滤器。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大工作簿数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 工作表

* [[!UICONTROL 添加工作表]](#add-a-worksheet)
* [[!UICONTROL 添加工作表行]](#add-a-worksheet-row)
* [[!UICONTROL 删除工作表行]](#delete-a-worksheet-row)
* [[!UICONTROL 列出工作表行]](#list-worksheet-rows)
* [[!UICONTROL 列出工作表]](#list-worksheets)
* [[!UICONTROL 更新工作表行]](#update-a-worksheet-row)
* [[!UICONTROL 监视工作表行]](#watch-worksheet-rows)

#### [!UICONTROL 添加工作表]

此操作模块在所选工作簿中创建新工作表。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>选择要添加工作表的工作簿，包括工作簿不在根目录中的路径。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 名称] </td>
   <td> <p>输入或映射新工作表的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 添加工作表行]

This action module adds a new row to the selected worksheet.

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>选择包含要添加行的工作表的工作簿，包括路径（如果工作簿不在根目录中）。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作表] </td>
   <td> <p>选择要添加行的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL要输入的值的类型]</p> </td> 
   <td> <p>选择要输入工作表的值的类型。 </p> 
    <ul> 
     <li> <p><strong>[！UICONTROL公式]</strong> </p> <p> Excel尝试计算指定的表达式。 公式中的函数名称为英文。 示例： <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[！UICONTROL公式本地]</strong> </p> <p>Excel尝试计算指定的表达式。 The function names are in the language of your Excel application. Example: <code>=SUM(A1, 1.5)</code> vs <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[！UICONTROL值]</strong> </p> <p>Excel不计算该值。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL Row]</td>
    <td>对于每个列，输入您希望该列在新行中的值。</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除工作表行]

此操作模块从工作表中删除一行。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>选择包含您要删除的行的工作表的工作簿。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作表]</td>
   <td> <p> 选择包含要删除的行的工作表。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL行ID]</td>
   <td>输入或映射要删除的行的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出工作表行]

此操作模块检索指定工作表中的行列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>选择包含工作表的工作簿，该工作表包含您要列出的行，如果工作簿不在根目录中，请包含路径。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作表] </td>
   <td> <p>选择包含要列出的行的工作表。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 限制]</td>
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大工作表行数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出工作表]

此操作模块检索指定工作簿中的工作表列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>选择包含您希望模块列出的工作表的工作簿。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 限制]</td>
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大工作表数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新工作表行]

此操作模块可更新现有的工作表行。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>选择包含要更新的行的工作表的工作簿。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作表] </td>
   <td> <p>选择包含要更新的行的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL要输入的值的类型]</p> </td> 
   <td> <p>选择要输入工作表的值的类型。 </p> 
    <ul> 
     <li> <p><strong>[！UICONTROL公式]</strong> </p> <p> Excel尝试计算指定的表达式。 公式中的函数名称为英文。 示例： <code>[!DNL =SUM(A1:A10)]</code></p> </li> 
     <li> <p><strong>[！UICONTROL公式本地]</strong> </p> <p>Excel tries to evaluate the specified expression. The function names are in the language of your Excel application. Example: <code>=SUM(A1, 1.5)</code> vs <code>=SUMME(A1; 1,5)</code></p> </li> 
     <li> <p><strong>[！UICONTROL值]</strong> </p> <p>Excel不计算该值。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL行ID]</td> 
   <td>选择要更新的行的编号。</td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL Row]</td>
    <td>对于每个列，输入您希望该列在新行中的值。</td>
    </tr> 
 </tbody> 
</table>

#### [!UICONTROL 监视工作表行]

此触发器模块会在工作表中添加新行时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>Select the workbook that contains the worksheet you want to watch for new rows.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[！UICONTROL工作表] </td>
   <td> <p>Select the Excel sheet that you want to watch for new rows.</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[！UICONTROL跳过空行] </td>
   <td> <p>启用此选项不会返回工作表中空行的包。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 限制]</td>
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大工作表行数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 表

* [[!UICONTROL 添加表]](#add-a-table)
* [[!UICONTROL 添加表格行]](#add-a-table-row)
* [[!UICONTROL 删除表]](#delete-a-table)
* [[!UICONTROL 获取表]](#get-a-table)
* [[!UICONTROL 列出表行]](#list-table-rows)
* [[!UICONTROL 列出表]](#list-tables)
* [[!UICONTROL 更新表]](#update-a-table)
* [[!UICONTROL 监视表行]](#watch-table-rows)

#### [!UICONTROL 添加表]

此操作模块会在Excel工作表中创建一个表元素。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作簿] </td> 
   <td> <p>选择包含要添加表的工作表的工作簿。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作表] </td> 
   <td> <p>选择要添加表的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Has headers]</td> 
   <td> <p>启用此选项可将第一行定义为表标题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL地址]</p> </td> 
   <td> <p>通过指示左上单元格和右下单元格来设置表的大小。 示例： <code>A1:C10</code>创建了一个包含3列和10行的表。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 添加表格行]

此操作模块修改现有表。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>Select the workbook that contains the table where you want to add a row.</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作表] </td>
   <td> <p>选择包含要添加行的表的工作表。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL表]</td>
   <td>选择要添加行的表。</td> 
  </tr> 
  <tr>
    <td role="rowheader" >[！UICONTROL Row]</td>
    <td>对于每个列，输入您希望该列在新行中的值。</td>
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL行ID]</p> </td> 
   <td> <p>要在表格上的特定位置添加行，请输入或映射行号。 模块在此行之后插入新行。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除表]

此操作模块从[!DNL Excel]工作表中删除指定的表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Delete a table]</td> 
   <td> <p>Select how you want to identify the table that you want to delete.</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>Enter or map the ID of the workbook that contains the table you want to delete, then enter or map the ID of the worksheet that contains the table.</p> <p>在[！UICONTROL表名称]字段中，输入或映射要删除的表的名称。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要删除表的工作簿和工作表，然后选择该表。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取表]

此操作模块检索指定表的元数据。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader"> 
     <p >[!UICONTROL 连接]</p>
   </td> 
   <td> 
     <p>有关将Office 365帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p>
     </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL获取表]</td> 
   <td> <p>Select how you want to identify the table that you want to retrieve.</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>Enter or map the ID of the workbook that contains the table you want to retrieve, then enter or map the ID of the worksheet that contains the table.</p> <p>In the [!UICONTROL Table Name] field, enter or map the name of the table you want to retrieve.</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要检索的表的工作簿和工作表，然后选择该表。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出表行]

此搜索模块检索工作簿中所有表行的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>选择包含要列出行的表的工作簿。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作表] </td>
   <td> <p>选择包含要列出行的表的工作表</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL表] </td>
   <td> <p>选择包含要列出的行的表。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 限制]</td>
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大表行数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出表]

此搜索模块检索所有表对象的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr>
    <td role="rowheader" >[！UICONTROL工作簿] </td>
   <td> <p>选择包含要列出的表的工作簿。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作表] </td>
   <td> <p>选择包含要列出的表的工作表</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 限制]</td>
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大表数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新表]

此操作模块更新现有的表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Update a table]</td> 
   <td> <p>Select how you want to identify the table that you want to update.</p> 
    <ul> 
     <li> <p><strong>Enter manually</strong> </p> <p>In the [!UICONTROL Workbook ID] field, enter or map the ID of the workbook that contains the table you want to update.</p> <p>在[！UICONTROL表名]字段中，输入或映射要更新的表名。</p> </li> 
     <li> <p><strong>[！UICONTROL从列表中选择]</strong> </p> <p>选择包含要更新的表的工作簿和工作表，然后选择该表。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 名称]</td> 
   <td> <p>如果要重命名表，请输入或映射表的新名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Show Headers]</td> 
   <td> <p>启用此选项以显示更新表的标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示总计]</td> 
   <td>启用此选项以显示表的总值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL样式]</td> 
   <td>为新表选择样式。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 监视表行]

在向表中添加新行时，此触发器将启动一个方案。

>[!NOTE]
>
>The table here refers to the embedded table element in the Workbook. Not the entire table (workbook/sheet).

![Embedded table](/help/workfront-fusion/references/apps-and-modules/assets/embedded-table-350x420.png)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL工作簿]</p> </td> 
   <td> <p>选择包含要监视的表的工作簿。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[！UICONTROL工作表] </td>
   <td> <p> 选择包含要监视的表的工作表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL表]</p> </td> 
   <td> <p>选择要监视的表。</p> </td> 
  </tr> 
  <tr> 
    <td role="rowheader" >[!UICONTROL 限制]</td>
   <td> <p>Enter or map the maximum number of rows you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

* [[!UICONTROL 进行API调用]](#make-an-api-call)
* [[!UICONTROL 检索数据]](#retrieve-data)

#### [!UICONTROL 进行API调用]

此操作模块允许您进行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于 <code>https://graph.microsoft.com</code> 的路径。示例：<code> /v1.0/me/drive/root/children</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   td&gt; <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 正文]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：   <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>">  
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 检索数据]

此操作从定义的工作表范围中检索数据，并为每行返回一个捆绑。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 连接]</p> </td> 
   <td> <p>有关将[!DNL Office 365]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作簿] </td> 
   <td> <p>选择包含要检索的数据的工作簿。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作表] </td> 
   <td> <p>Select the worksheet that contains the data you want to retrieve.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Range] </td> 
   <td> <p>Specify the area of the sheet you want to retrieve data from by indicating the top left and bottom right cells. 示例： <code>A1:D10</code></p> </td> 
  </tr> 
 </tbody> 
</table>
