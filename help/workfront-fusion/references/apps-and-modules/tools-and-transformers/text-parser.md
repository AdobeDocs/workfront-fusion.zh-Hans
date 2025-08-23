---
title: 文本分析器
description: 您可以使用文本解析器工具来解析文本，以供在其他Adobe Workfront Fusion场景模块中使用。 文本解析器不需要连接。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 885d714e-fc09-41a2-89dc-ebe29a355e43
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 0%

---

# [!UICONTROL 文本分析器]

您可以使用[!UICONTROL 文本分析器工具]来分析文本，以供在其他Adobe Workfront Fusion方案模块中使用。 [!UICONTROL 文本分析器]不需要连接。

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
   <p>无Workfront Fusion许可证要求</p>
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

## 文本分析器API信息

文本解析器连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v2</td> 
  </tr>
 </tbody> 
 </table>

## [!UICONTROL 文本分析器]模块及其字段

在配置[!UICONTROL 文本分析器]模块时，Adobe Workfront Fusion将显示以下列出的字段。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 变压器

* [[!UICONTROL 从HTML获取元素]](#get-elements-from-html)
* [[!UICONTROL 从文本中获取元素]](#get-elements-from-text)
* [[!UICONTROL HTML至文本]](#html-to-text)
* [[!UICONTROL 匹配模式]](#match-pattern)
* [[!UICONTROL Replace]](#replace)

#### [!UICONTROL 从HTML获取元素]

从HTML代码中检索所需的元素。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 即使模块找不到匹配项，仍继续执行路由]</td> 
   <td> <p>启用此选项以确保模块在未返回任何结果时不会停止场景。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 元素类型]</td> 
   <td> <p> 选择要从HTML代码中检索的元素类型。 </p> 
    <ul> 
     <li>[!UICONTROL 图像]</li> 
     <li>[!UICONTROL 链接]</li> 
     <li>[!UICONTROL iFrame元素]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>输入或映射要从中检索指定元素类型的HTML代码。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 从文本中获取元素]

根据给定的模式解析文本中的元素。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 输入文本]</td> 
   <td> <p>输入或映射要分析的文本。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 模式]</td> 
   <td> <p>选择反映要从文本中解析的元素的图案。</p> <p>要输入自定义正则表达式，请从列表中选择自定义，然后在自定义正则表达式字段中输入自定义表达式。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 忽略重复发生次数]</td> 
   <td> <p>选中此框可忽略文本元素的重复出现次数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL HTML至文本]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL HTML] </td> 
   <td> <p>输入要转换为纯文本的HTML代码。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 换行符] </td> 
   <td> <p>选择换行符（换行符）的类型。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 大写标题]</p> </td> 
   <td> <p>启用此选项可将标题标记中包含的文本（如&lt;h2&gt; &lt;/h2&gt;）转换为大写文本。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 匹配模式]

[!UICONTROL 匹配模式]模块允许您从给定文本中查找和提取与搜索模式匹配的字符串元素。 此模块使用正则表达式（也称为正则表达式或正则表达式）。

正则表达式是一系列字符，其中每个字符要么是具有特殊意义的元字符，要么是具有字面含义的常规字符。 这些字符和元字符标识了可用于搜索文本的模式。 例如，如果要搜索名称，可设置正则表达式以搜索由两个以大写字母开头的连续单词组成的模式。 正则表达式是用于搜索和处理文本的强大工具。

有关正则表达式的讨论超出了本文的讨论范围。 我们建议使用以下资源：

* 有关元字符的完整列表，请参阅MDN Web文档中的[正则表达式](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)。
* 有关如何创建正则表达式的教程，我们建议[RegexOne](https://regexone.com/)。
* 若要试验正则表达式，我们建议使用[正则表达式101](https://regex101.com/)网站。 在左侧面板中选择ECMAScript (JavaScript) FLAVOR。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 模式] </td> 
   <td> <p>输入正则表达式模式。 </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>示例： </b></span></span> <code>[+-]?(\d+(\.\d+)?|\.\d+)([eE][+-]?\d+)?</code>提取所提供文本中的所有数字。</p> <p>注释：  <p>模式应至少包含一个位于括号<code>()</code>中的捕获组。 如果模式不包含任何捕获组，则输出包为空。</p> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 全局匹配]</td> 
   <td> <p>启用此选项以检索文本中的所有匹配项。 每个匹配项都在单独的捆绑包中输出。 如果禁用此选项，则模块将仅检索第一个条目。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 区分大小写]</td> 
   <td> <p> 启用此选项可让此模块将文本视为区分大小写。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Multiline] </td> 
   <td> <p>启用此选项可确保开始和结束元字符（<code>^</code>和<code>$</code>）匹配每行的开始或结束，而不只是整个输入字符串的开始或结束。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 单行]</td> 
   <td>启用此选项以确保句点(.)与换行符(<code>\n</code>)匹配。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 即使模块未返回任何结果，仍继续执行路由]</td> 
   <td> <p>启用此选项以确保模块在未返回任何结果时不会停止场景。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text] </td> 
   <td> <p>输入或映射要与模式匹配的文本。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Replace]

在输入的文本中搜索指定的值或正则表达式，并将结果替换为新的值。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 模式] </td> 
   <td> <p>输入搜索词。 您也可以使用正则表达式。 有关正则表达式的更多详细信息，请参阅<a href="#match-pattern" class="MCXref xref">[!UICONTROL 匹配模式]</a>模块。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 新值]</td> 
   <td> <p> 输入您要替换搜索词的值。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 全局匹配]</td> 
   <td> <p>启用此选项以检索文本中的所有匹配项。 每个匹配项都在单独的捆绑包中输出。 如果禁用此选项，则模块将仅检索第一个条目。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 区分大小写]</td> 
   <td> <p> 启用此选项可让此模块将文本视为区分大小写。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Multiline] </td> 
   <td> <p>启用此选项可确保开始和结束元字符（<code>^</code>和<code>$</code>）匹配每行的开始或结束，而不只是整个输入字符串的开始或结束。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 单行]</td> 
   <td>启用此选项以确保句点(.)与换行符(<code>\n</code>)匹配。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Text] </td> 
   <td> <p>输入要搜索的文本。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 数据擦除

数据抓取（有时称为网页抓取、数据提取或网页收集）是从网站收集数据，并将其存储在本地数据库或电子表格中的过程。 如果要从网站中刮取数据，并且不熟悉正则表达式，则可以使用数据刮取工具。

如果数据抓取工具提供REST API，则可以通过我们的通用[[!UICONTROL HTTP]模块](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)和[Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)模块连接到该工具。

## 文本解析器故障排除

如果无法获取文本解析器来生成任何输出，请使用此信息。

>[!BEGINSHADEBOX]

示例：

该模块应解析文件文档“filename.docx”的文件类型，文件扩展名从DOCX到PDF再到CSV。

在这种情况下，您可以选择使用的表达式是[!DNL \..+]

此正则表达式通常会导致完全匹配。

但是，在文本解析器中实施此表达式不会导致匹配：

![没有匹配项](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-you-dont-get-a-match-350x365.png)

原因在于“i”仅显示每个匹配的匹配数，因此在本例中，我们有2个匹配，因此“i”后面有一个数值1和2。 用例是，如果您需要仅匹配或传递第二个匹配值的过滤器中的数据，则可以指定由数值表示的值。

![匹配](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-matches-350x355.png)

为了能够获取所需的匹配值，以便在要解析的部分中添加括号（例如，从“filename.docx”中提取 — 仅从“docx”中提取），根据我们用于此案例的正则表达式，应在\上应用括号。(.+)

这会捕获DOCX，将其放入组中，然后保留“。” 别想了。

![获取匹配项](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-get-matches-350x592.png)

在下图所示的输出中，捕获组将匹配任何字符（行终止符除外）。

![输出](/help/workfront-fusion/references/apps-and-modules/assets/text-parser-output-350x389.png)

另一个同时包含正则表达式的解决方法是使用替换函数

`{{replace("abcdefghijklmno pqr stuvw xyz.docx"; "/.\./"; ".")}}`

然后将`abcdefghijklmno pqr stuvw xyz.docx`替换为您的实际文件名变量。

>[!ENDSHADEBOX]
