---
title: 使用内置函数映射项
description: 在映射项目时，您可以使用函数创建简单或复杂的公式。
author: Becky
feature: Workfront Fusion
exl-id: b9d7643e-febf-42e2-9ddc-8ec8eba98e7a
source-git-commit: 8de3e365ff7ff91f4b29fb8a298f3b846de0a980
workflow-type: tm+mt
source-wordcount: '717'
ht-degree: 23%

---

# 使用内置函数映射项

Workfront Fusion包含内置函数，可让您创建简单或复杂的公式。 这些函数涵盖了各种用例，包括用于数组、字符串、数字和来自之前模块的数据的函数。

此外，您可以创建自定义函数，然后场景可以使用这些函数转换和处理数据。

有关自定义函数的信息和说明，请参阅[使用自定义函数映射数据](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md)。

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
   <td role="rowheader">产品</td> 
   <td>
   <p><ul><li>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li><li>您必须拥有Adobe App Builder许可证才能使用自定义函数。</ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 使用内置函数映射数据

在映射项目时，您可以使用函数创建简单或复杂的公式。 可用的函数与 Excel 以及某些编程语言中的函数类似：

* 它们可用于处理通用逻辑、数学、文本、日期和数组。
* 它们允许您对项目值执行条件逻辑和转换，例如将文本转换为大写、裁剪文本、将日期转换为其他格式等。

### 在字段中插入函数

要将函数插入到字段中，请执行以下操作：

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要映射数据的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击要插入函数的字段。
1. 在映射面板中选择包含要插入的函数的选项卡。

   有关映射面板选项卡的信息，请参阅[函数概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md)
1. 单击函数名称。

   或

   将函数拖到字段中。
1. 配置函数参数。

   有关函数参数的说明，请将鼠标悬停在映射面板中的函数上。

   有关函数及其参数的详细信息，请参阅[函数引用下的文章：文章索引](/help/workfront-fusion/references/mapping-panel/functions/functions-toc.md)。

1. 继续配置模块，或单击&#x200B;**确定**。

>[!TIP]
>
>创建要在其他字段中重用的复杂公式时，可以单击包含该组合的字段，使用Cmd-A或Ctrl-A将其选中，然后将其复制并粘贴到其他字段中。


>[!BEGINSHADEBOX]

**示例：**&#x200B;某些数据类型会阻止用户输入超过一定数量的字符。 您可以使用子字符串函数将值限制为特定字符数。

在此示例中，子字符串函数将项目名称限制为50个字符。

![示例会议长度限制](assets/example-meet-length-restriction-350x184.png)

>[!ENDSHADEBOX]

### 嵌套函数

可以将函数相互嵌套。

>[!BEGINSHADEBOX]

**示例：**

在此示例中，子字符串函数将修剪后的项目名称限制为50个字符。

![已修剪的名称](assets/trimmed-name-under-50.png)

>[!ENDSHADEBOX]

嵌套函数：

1. 单击要在其中创建公式的字段。

   这将打开映射面板。

1. 单击要添加的第一个函数。 这是外部的函数。 如果存在以下示例，则这是`substring`函数。
1. 在该函数中，单击希望嵌套函数放置的位置。 在此示例中，嵌套函数将替换第一个参数。
1. 在映射面板中，单击嵌套函数。 在此示例中，这是`trim`函数。
1. 根据需要继续配置函数。
1. 继续配置模块，或单击&#x200B;**确定**。

### 使用[!DNL Google Sheets]函数

如果Workfront Fusion不提供您要使用的功能，但它由[!DNL Google Sheets]提供，您可以按照以下步骤使用它：

1. 在[!DNL Google Sheets]中，创建一个新的空电子表格。
1. 在Workfront Fusion中，打开您的场景。
1. 将&#x200B;**[!DNL Google Sheets]** >**[!UICONTROL 更新单元格]**&#x200B;模块添加到方案。

1. 配置模块：

   1. 在&#x200B;**[!UICONTROL 电子表格]**&#x200B;字段中选择新创建的电子表格。
   1. Insert your formula containing the [!DNL Google Sheets] function(s) into the **[!UICONTROL Value]** field.

      You can use the output of preceding modules as usual.

      ![Use Google Sheets functions](assets/exploit-google-sheet-functions-350x218.png)

1. Insert the **[!UICONTROL Google Sheets] >[!UICONTROL Get a cell]** module to obtain the calculated result.
1. Configure the module, using the same Cell ID that you used in step 4.

   ![Use Google Sheets functions](assets/exploit-google-sheet-functions-2-350x187.png)
