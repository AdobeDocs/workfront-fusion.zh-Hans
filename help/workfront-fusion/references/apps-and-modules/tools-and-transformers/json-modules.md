---
title: JSON 模块
description: Adobe Workfront Fusion JSON应用程序提供了用于处理JSON格式的数据的模块，以便Adobe Workfront Fusion可以进一步处理数据内容或创建新的JSON内容。
author: Becky
feature: Workfront Fusion
exl-id: f8b281c5-bb63-4412-98c5-d82f45f8eafc
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# [!UICONTROL JSON]模块

[!DNL Adobe Workfront Fusion] [!UICONTROL JSON]应用程序提供了用于处理JSON格式数据的模块，以便[!DNL Adobe Workfront Fusion]可以进一步处理数据内容或创建新的JSON内容。

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

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 解析JSON时的注意事项

* [数据结构](#data-structure)
* [收藏集与数组](#collection-vs-array)

### 数据结构

数据结构描述了JSON数据的组织方式，并能够将各个JSON项目映射到场景中的其他模块。 如果不提供数据结构，则可以手动执行模块，[!DNL Workfront Fusion]将从提供的JSON构建结构：

1. 将[!UICONTROL 分析JSON]模块添加到方案。
1. 在&#x200B;**[!UICONTROL JSON字符串]**&#x200B;字段中，输入要从中构建数据结构的JSON。
1. 不要将其他模块连接到[!UICONTROL 解析JSON]模块。 由于[!DNL Workfront Fusion]尚不了解JSON数据的结构，因此尚无法将[!UICONTROL 解析JSON]模块中的数据映射到方案中的其他模块。
1. 手动运行方案。 这允许[!UICONTROL 解析JSON]模块从您提供的JSON中识别JSON结构。
1. 您现在可以连接以下模块。 现在，可以映射解析JSON模块中的项目。

有关详细信息，请参阅[!UICONTROL Adobe Workfront Fusion][&#128279;](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md)中的数据结构。

### 收藏集与数组

如果JSON字符串字段包含集合`{ ... }`，则输出是包含集合项的单个捆绑。

>[!BEGINSHADEBOX]

**示例：**

```
{
    "name" : "Peter",

    "ID" : 1>}
```


![JSON收藏集](/help/workfront-fusion/references/apps-and-modules/assets/json-collection.png)

>[!ENDSHADEBOX]

如果JSON字符串字段包含数组`[ ... ]`，则输出是一系列捆绑包。 每个包都包含数组的一个元素。

>[!BEGINSHADEBOX]

**示例：**

```
[
  {
    "name" : "Peter",
    "ID" : 1
  },

  {
    "name" : "Mike",
    "ID" : 2
  }
]
```

![JSON数组](/help/workfront-fusion/references/apps-and-modules/assets/json-array.png)

>[!ENDSHADEBOX]

## [!UICONTROL JSON]模块及其字段

配置[!DNL JSON]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除了这些以外，还可能会显示其他JSON字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [将JSON转换为XML](#convert-json-to-xml)
* [解析JSON](#parse-json)
* [创建JSON](#create-json)
* [转换JSON](#transform-json)

### 汇总

#### [!UICONTROL 聚合到JSON]

此聚合器模块将上一个模块的输出聚合到JSON中。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module] </td> 
   <td> <p>选择用于输出要汇总到JSON的数据的模块。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>选择要用于创建JSON的数据结构。 数据结构决定了此模块中可用的其他字段。 有关详细信息，请参阅本文中的<a href="#data-structure" class="MCXref xref">数据结构</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 缩进]</td> 
   <td> <p> 选择是要使用制表符、两个空格还是四个空格缩进JSON。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 分组依据]</td> 
   <td>定义要按其分组聚合输出的表达式。 此表达式可以包含一个或多个映射项。 然后，使用此表达式的值将聚合的数据分成不同的组。 每个组输出为一个单独的捆绑，其中包含一个键（经过计算的表达式）和一个值（聚合文本）。 在后续模块中，您可以将该键用作过滤器。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 在出现空聚合后停止处理]</td> 
   <td>启用此选项可在没有结果时停止方案。</td> 
  </tr> 
 </tbody> 
</table>

### 变压器

* [将JSON转换为XML](#convert-json-to-xml)
* [创建JSON](#create-json)
* [解析JSON](#parse-json)
* [转换JSON](#transform-json)

#### [!UICONTROL 将JSON转换为XML]

此操作模块将JSON字符串转换为XML。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>输入或映射要转换为XML的JSON。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建JSON]

此操作模块从数据结构创建JSON。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">数据结构</td> 
   <td> <p>选择要用于创建JSON的数据结构。 有关详细信息，请参阅本文中的<a href="#data-structure" class="MCXref xref">数据结构</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">缩进</td> 
   <td> <p>选择要用于此JSON的缩进。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 解析JSON]

此操作模块将JSON字符串解析为数据结构，允许您访问JSON字符串中的数据。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Data structure]</td> 
   <td> <p>选择要用于创建JSON的数据结构。 有关详细信息，请参阅本文中的<a href="#data-structure" class="MCXref xref">数据结构</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON string] </td> 
   <td> <p>输入或映射要解析的JSON。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 转换JSON]

此操作模块将对象转换为JSON字符串。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">缩进</td> 
   <td> <p>选择要用于此JSON的缩进。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 对象]</td> 
   <td> <p>输入或映射要转换为JSON的对象。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 将数据记录转换为JSON

>[!BEGINSHADEBOX]

**示例：**&#x200B;以下示例说明如何将数据记录从[!DNL Google Sheets]转换为JSON格式：

1. 将[!DNL Google Sheets] > [!UICONTROL 选择方案中的行]模块以获取数据。 设置模块以从[!DNL Google]电子表格中检索行。 将&#x200B;**[!UICONTROL 返回的最大行数]**&#x200B;设置为一个较小的数字，但大于一个以用于测试目的（例如，3）。 执行[!DNL Google Sheets]模块，方法是右键单击该模块并选择“**[!UICONTROL 仅运行此模块]**”。 验证模块的输出。

1. 在[!DNL Google Sheets]模块之后连接[!UICONTROL 数组汇总]模块。 在模块设置的&#x200B;**[!UICONTROL Source节点]**&#x200B;字段中选择[!DNL Google Sheets]模块。 请暂时保留其他字段。

1. 在[!UICONTROL 数组聚合器]模块之后连接[!UICONTROL JSON] > [!UICONTROL 创建JSON]模块。 模块设置需要一个描述JSON格式的数据结构。 单击&#x200B;**[!UICONTROL 添加]**&#x200B;以打开数据结构设置。 创建此数据结构的最简单方法是自动从JSON示例生成它。 单击&#x200B;**[!UICONTROL 生成器]**&#x200B;并将您的JSON示例粘贴到&#x200B;**[!UICONTROL 示例数据]**&#x200B;字段：

   **示例：**

   ```
   {
   "books": [
   {
   "id": "ID",
   "title": "Title",
   "author": "Author"
   }
   ]
   }
   ```

1. 单击&#x200B;**[!UICONTROL 保存]**。 数据结构中的[!UICONTROL Specification]字段现在包含生成的结构。
1. 将数据结构的名称更改为更具体的名称，然后单击&#x200B;**[!UICONTROL 保存]**。 与root数组属性对应的字段在JSON模块的设置中显示为可映射字段。

1. 单击该字段旁边的&#x200B;**[!UICONTROL 映射]**&#x200B;按钮，并将Array聚合器输出中的`Array[]`项映射到它。

1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;以关闭[!UICONTROL JSON]模块的设置。

1. 打开[!UICONTROL 数组汇总]模块的设置。 将&#x200B;**[!UICONTROL Target结构]**&#x200B;从[!UICONTROL Custom]更改为与根数组属性对应的[!UICONTROL JSON]模块的字段。 将[!DNL Google Sheets]模块中的项映射到相应的字段。

1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;以关闭[!UICONTROL 数组汇总]模块的设置。

1. 运行方案。

   [!UICONTROL JSON]模块输出正确的JSON格式。

1. 打开[!DNL Google Sheets]模块的设置，并增加[!UICONTROL 返回的最大行数]数值，使其大于电子表格中的行数，以便处理所有数据。

>[!ENDSHADEBOX]

## 故障排除

### 无法映射来自[!UICONTROL 分析JSON]模块的数据

确保JSON内容正确映射到[!UICONTROL 解析JSON]模块，并且数据结构已正确定义。 有关详细信息，请参阅本文中的[将数据记录转换为JSON](#transforming-data-records-to-json)。

### 在JSON中使用条件语句时，模块失败

在JSON中使用条件语句（如`if`）时，请将引号放在条件语句之外。

>[!BEGINSHADEBOX]

**示例：**

JSON中的![引号](/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png)

>[!ENDSHADEBOX]
