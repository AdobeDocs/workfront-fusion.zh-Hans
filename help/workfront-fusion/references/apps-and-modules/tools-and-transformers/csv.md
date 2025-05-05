---
title: CSV
description: 通过Adobe Workfront Fusion CSV模块，您可以创建CSV文件，并根据收到的文本值或文件解析CSV文本。
author: Becky
feature: Workfront Fusion
exl-id: bc6d5ddc-93c3-437b-8537-5bece1351c1d
source-git-commit: 5971b2210eaac8f8a75fd7a4aac5a9f7954d27ef
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# CSV

[!DNL Adobe Workfront Fusion] [!UICONTROL CSV]模块允许您创建CSV文件，并从接收的文本值或文件解析CSV文本。

由于这是转换器，因此这些模块不需要连接。

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
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## [!UICONTROL Create CSV]

[!UICONTROL Create CSV]聚合器允许您根据收到的文本值创建csv文本。

有关聚合器的详细信息，请参阅[聚合器模块](/help/workfront-fusion/references/modules/aggregator-module.md)。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>选择用于输出要用于创建CSV的字段的模块。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Aggregated Fields]</td>
        <td>从可用字段列表中选择要聚合的字段。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Include headers in the first row]</td>
        <td>选择此选项以在结果中包含标头。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Group by]</td>
        <td>输入筛选条件以将结果分组。 例如，输入日期。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Stop processing after an empty aggregation]</td>
        <td>选择此选项可在没有结果时停止方案。</td>
    </tr>
</table>

## [!UICONTROL Create CSV (advanced)]

[!UICONTROL Create CSV (advanced)]聚合器允许您根据收到的文本值创建CSV文本。 它采用一种数据结构，该数据结构定义生成的CSV文件中的CSV列。 定义后，列将作为字段显示在CSV模块设置中，并可映射到场景中的后续模块。

有关聚合器的详细信息，请参阅[聚合器模块](/help/workfront-fusion/references/modules/aggregator-module.md)。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
        <td>选择用于输出要用于创建CSV的字段的模块。</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data Structure]</td> 
   <td> <p>选择数据结构，以您希望的方式聚合字段。 定义数据结构后，您可以将项目映射到相应的字段。</p> <p>有关详细信息，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">数据结构</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include headers in the first row] </td> 
   <td>选择此选项以在结果中包含标头。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group by] </td> 
   <td>输入筛选条件以将结果分组。 例如，输入日期。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stop processing after an empty aggregation] </td> 
   <td>选择此选项可在没有结果时停止方案。 </td> 
  </tr> 
 </tbody> 
</table>


>[!BEGINSHADEBOX]

**示例**：

此示例说明如何将Google联系人导出到CSV文件，该文件具有名为“全名”和“电子邮件”的两列。 [!UICONTROL Google Contacts] > [!UICONTROL Get contacts from a group]模块中的输出包具有以下结构。 电子邮件地址存储在<code>[!UICONTROL Emails[]]中</code> 项，它是一个集合数组，每个集合包含两个项：<code>标签</code> 和<code>电子邮件</code>.
![正在转换](/help/workfront-fusion/references/apps-and-modules/assets/transforming-350x546.png)

简单[!DNL Create CSV]模块提供了一个与捆绑包的顶级项目对应的复选框列表。 如果尝试选择<code>全名</code> 和<code>封电子邮件</code> 项，[!UICONTROL Create CSV]模块会生成以下输出，这可能不是您想要的：

```
"emails","fullName"
"[object Object]","Shon Winer"
"[object Object]","Lizeth Fulmore"
"[object Object]","Hilario Gullatt"
"[object Object]","Abby Eisenbarth"
```

因为项目<code>全名</code> 为简单类型“文本”，按预期导出。 项目<code>电子邮件</code>将复杂类型Array of Collections导出为[对象Object]，这是默认情况下Collections和Arrays转换为文本的方式。

有关详细信息，请参阅[项目数据类型](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md)。


导出<code>电子邮件的内容 </code><code>电子邮件[]的第一个集合的项目</code> 数组，您必须使用[!UICONTROL Create CSV (advanced)]模块。 利用此模块，可定义CSV文件的单独列并将项目映射到这些列，包括嵌套列。

1. 在方案中插入模块[!UICONTROL Create CSV (advanced)]。
1. 单击[!UICONTROL Data structure]字段旁边的<strong>[!UICONTROL Add]</strong>按钮以创建新的数据结构。
1. 输入数据结构的名称，然后单击<strong>[!UICONTROL Add item]</strong>以添加各个列。 要导出两列：“全名”和“电子邮件”，生成的数据结构将如下所示：

   ![Google联系人输出](/help/workfront-fusion/references/apps-and-modules/assets/google-contacts-350x524.png)

1. 定义数据结构后，[!UICONTROL Create CSV (advanced)]模块的配置中将显示与每个单独列对应的字段，以便映射项目。 从<code>[!UICONTROL Emails[]]中获取第一项</code> 数组并映射其项<code>电子邮件 </code>至字段/列电子邮件：

   ![创建CSV高级模块](/help/workfront-fusion/references/apps-and-modules/assets/create-csv-advanced-350x308.png)

1. 执行方案。 因为项目<code>电子邮件[1]：电子邮件</code> 映射到列“电子邮件”的简单类型文本，它可正确导出。

```
"Full Name","Email"
"Shon Winer","Shon@Winer.com"
"Lizeth Fulmore","Lizeth@Fulmore.com"
"Hilario Gullatt","Hilario@Gullatt.com"
"Abby Eisenbarth","Abby@Eisenbarth.com"
```

>[!ENDSHADEBOX]

## [!UICONTROL Parse CSV]

[!UICONTROL Parse CSV]转换器允许您从接收的文本值或文件解析CSV文本。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Number of columns]</td> 
   <td>指定CSV文件中的列数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV contains headers]</td> 
   <td> <p>如果CSV文本的第一行包含标题，请选择此选项。</p> <p>注意：模块不使用这些标头标记输出中的列。 相反，此字段可确保标头不会包含在输出数据中。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL delimiterType]</td> 
   <td> <p>选择CSV文件的分隔符。 分隔符是指示分隔值或字段之间的边界的文本字符。</p> 
    <ul> 
     <li>[!UICONTROL Comma]</li> 
     <li>[!UICONTROL Tab]</li> 
     <li> <p>[!UICONTROL Other]</p> <p>如果选择[!UICONTROL Other]，请输入CSV文件用于分隔值的分隔符字符。 必须只输入一个字符。<br></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Preserve quotes inside unquoted field]</td> 
   <td>启用此选项可保留引号。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CSV]</td> 
   <td>输入或映射要解析的CSV文件。<p>注意： <p>如果数据为二进制形式（通常来自文件），则必须使用“toString()”函数将二进制数据转换为[!UICONTROL String]：</p><p><img src="/help/workfront-fusion/references/apps-and-modules/assets/parse-csv-350x123.png"></p></p></td> 
  </tr> 
 </tbody> 
</table>
