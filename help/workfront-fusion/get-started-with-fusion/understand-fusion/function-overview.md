---
title: 函数概述
description: 在映射项目时，您可以使用函数创建简单或复杂的公式。
author: Becky
feature: Workfront Fusion
exl-id: e07730cb-52be-46db-a365-93cdbed1021c
source-git-commit: 6aad13e81c083754d7aad53dec103715bd6b8807
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 60%

---

# 函数概述

Workfront Fusion包含内置函数，可让您创建简单或复杂的公式。 这些函数涵盖了各种用例，包括用于数组、字符串、数字和来自之前模块的数据的函数。

此外，您可以创建自定义函数，然后场景可以使用这些函数转换和处理数据。

## 内置函数

在映射项目时，您可以使用函数创建简单或复杂的公式。可用的函数与 Excel 以及某些编程语言中的函数类似：

* 它们可用于处理通用逻辑、数学、文本、日期和数组。
* 它们允许您对项目值执行条件逻辑和转换，例如将文本转换为大写、裁剪文本、将日期转换为其他格式等。

### 函数选项卡概述

映射面板包含以下选项卡。每个选项卡均包含适用于该数据类型的函数与关键词。

| 函数类型 | 有关更多信息，请参阅： |
| --- | --- |
| **从其他模块映射**<br>![&#x200B;从其他模块映射](assets/toolbar-icon-functions-you-map-from-other-modules.png) | [将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md) |
| **常规函数**<br>![&#x200B;常规函数](assets/toolbar-icon-general-function.png) | [常规函数](/help/workfront-fusion/references/mapping-panel/functions/general-functions.md) |
| **数学函数**<br>![&#x200B;数学函数](assets/toolbar-icon-math-functions.png) | [数学函数](/help/workfront-fusion/references/mapping-panel/functions/math-functions.md) |
| **文本和二进制函数**<br>![&#x200B;字符串函数](assets/toolbar-icon-text-binary-functions.png) | [字符串函数](/help/workfront-fusion/references/mapping-panel/functions/string-functions.md) |
| **日期和时间** <br> ![日期和时间函数](assets/toolbar-icon-date-time-functions.png) | <ul><li>[日期和时间函数](/help/workfront-fusion/references/mapping-panel/functions/date-and-time-functions.md)</li><li>[日期和时间格式化标记](/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md)</li><li> [日期和时间解析标记](/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-parsing.md)</li></ul> |
| **用于处理数组的函数**<br> ![数组函数](assets/toolbar-icon-functions-for-arrays.png) | [数组函数](/help/workfront-fusion/references/mapping-panel/functions/array-functions.md) |

![函数工具栏](assets/functions-toolbar-350x189.png)

## 自定义函数

您可以在Fusion的“函数”区域中创建自定义函数。 然后，以Adobe App Builder模块的形式将这些函数添加到场景中。

由于自定义函数可通过Adobe App Builder使用，因此您的组织必须具有Adobe App Builder许可证才能使用它们。

有关自定义函数的信息和说明，请参阅使用自定义函数访问数据。
