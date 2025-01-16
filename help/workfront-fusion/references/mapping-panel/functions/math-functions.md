---
title: 数学函数
description: Adobe Workfront Fusion映射面板中提供了以下数学函数。
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# 数学函数

## [!UICONTROL average ([array of values]) average(value1; [value2], ...)]

返回特定数组中数值的平均值，或单独输入的数值的平均值。

## [!UICONTROL ceil (number)]

返回大于或等于指定数字的最小整数。

>[!BEGINSHADEBOX]

**示例：**

* `ceil(` `1.2` `)`

  返回2

* `ceil(` `4` `)`

  返回4

>[!ENDSHADEBOX]

## [!UICONTROL floor (number)]

返回小于或等于指定数字的最大整数。

>[!BEGINSHADEBOX]

**示例：**

* `floor(` `1.2` `)`

  返回1

* `floor(` `1.9` `)`

  返回1

* `floor(` `4` `)`

  返回4

>[!ENDSHADEBOX]

## [!UICONTROL max ([array of values]), max(value1;value2; ...)]

返回指定数组中的最大数或单独输入的数字中的最大数。

## [!UICONTROL min ([array of values]), min(value1; value2; ...)]

返回指定数组中的最小数字或单独输入数字中的最小数字。

## [!UICONTROL round (number)]

将数值舍入到最接近的整数。

>[!BEGINSHADEBOX]

**示例：**

* `round(` `1.2` `)`

  返回1

* `round(` `1.5` `)`

  返回2

* `round(` `1.7` `)`

  返回2

* `round(` `2` `)`

  返回2

>[!ENDSHADEBOX]

## [!UICONTROL sum ([array of values]), sum(value1; value2; ...)]

返回指定数组中的值的总和或单独输入的数字的总和。

## [!UICONTROL parseNumber (number; decimal separator)]

解析带有数字的字符串并返回数字。 例如， parseNumber(1 756,456；，)

## [!UICONTROL formatNumber (number; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

以请求的格式返回一个数字。 默认情况下，小数点为逗号(，)，千位分隔符为句点(.)。

>[!BEGINSHADEBOX]

**示例：**

`formatNumber( 123456789 ; 3 ; , ; . )`

返回123.456.789,000

>[!ENDSHADEBOX]
