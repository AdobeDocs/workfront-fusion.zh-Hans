---
title: 数学函数
description: Adobe Workfront Fusion映射面板中提供了以下数学函数。
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
TQID: https://experienceleague.adobe.com/a0WYFvPFBnXOvKS9ndQ-TD5xSvJz2bCbUbDY5VnXW0w
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 404
ht-degree: 6%

---

# 数学函数

## [!UICONTROL 平均值（[个值数组]）平均值(value1； [value2]， ...)]

返回特定数组中数值的平均值，或单独输入的数值的平均值。

## [!UICONTROL ceil （数字）]

返回大于或等于指定数字的最小整数。

>[!BEGINSHADEBOX]

**示例：**

* `ceil(` `1.2` `)`

  返回2

* `ceil(` `4` `)`

  返回4

>[!ENDSHADEBOX]

## [!UICONTROL 楼层（数字）]

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

## [!UICONTROL 最大值（[个值数组]），最大值(value1；value2； ...)]

返回指定数组中的最大数或单独输入的数字中的最大数。

## [!UICONTROL 分钟（[个值数组]），最小值(value1； value2； ...)]

返回指定数组中的最小数字或单独输入数字中的最小数字。

## [!UICONTROL 轮（数字）]

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

## [!UICONTROL sum （[个值数组]）， sum(value1； value2； ...)]

返回指定数组中的值的总和或单独输入的数字的总和。

## [!UICONTROL parseNumber （数字；小数分隔符）]

解析带有数字的字符串并返回数字。 例如， parseNumber(1 756,456；，)

## [!UICONTROL formatNumber (number； decimalPOINTS； [decimalSeparator]；[thousandsSeparator])]

以请求的格式返回一个数字。 默认情况下，小数点为逗号(，)，千位分隔符为句点(.)。

>[!BEGINSHADEBOX]

**示例：**

`formatNumber( 123456789 ; 3 ; , ; . )`

返回123.456.789,000

>[!ENDSHADEBOX]

### [!UICONTROL abs（号码）]

[!BADGE 新！]{type=Informative}

返回某数字的绝对值。

>[!BEGINSHADEBOX]

**示例：**

* `abs(-3.14)`

  返回3.14
* `abs(3.14)`

  返回3.14


### [!UICONTROL div(number1； number2； ...)]

[!BADGE 新！]{type=Informative}

以指定的顺序除以所有数字。

>[!BEGINSHADEBOX]

**示例：**

* `div(10; 2)`

  返回5
* `div(100; 5; 4)`

  返回5


### [!UICONTROL ln（数字）]

[!BADGE 新！]{type=Informative}

返回该数的自然对数。


>[!BEGINSHADEBOX]

**示例：**

* `ln(1)`

  返回0
* `ln(2.718281828)`

  返回1


### [!UICONTROL log(number1； number2)]

[!BADGE 新！]{type=Informative}

返回以`number1`为底的`number2`的对数。

>[!BEGINSHADEBOX]

**示例：**

* `log(10; 100)`

  返回2
* `log(2; 8)`

  返回3


### [!UICONTROL number(string)]

[!BADGE 新！]{type=Informative}

将字符串转换为数字。

>[!BEGINSHADEBOX]

**示例：**

* `number("3.14")`

  返回3.14
* `number("42")`

  返回42


### [!UICONTROL power(number； power)]

[!BADGE 新！]{type=Informative}

返回提升为指定次幂的数字。

>[!BEGINSHADEBOX]

**示例：**

* `power(2; 3)`

  返回8
* `power(4; 0.5)`

  返回2


### [!UICONTROL prod(number1； number2； ...)]

[!BADGE 新！]{type=Informative}

将提供的所有数字相乘。

>[!BEGINSHADEBOX]

**示例：**

* `prod(2; 3; 4)`

  返回24
* `prod(5; 5)`

  返回25


### [!UICONTROL sortAscNum(number1； number2； ...)]

[!BADGE 新！]{type=Informative}

返回提供的按升序排序的数字。

>[!BEGINSHADEBOX]

**示例：**

* `sortAscNum(3; 1; 2)`

  返回\[1， 2， 3]
* `sortAscNum(5; 3; 4)`

  返回\[3， 4， 5]


### [!UICONTROL sortDescNum(number1； number2； ...)]

[!BADGE 新！]{type=Informative}

返回提供的按降序排序的数字。

>[!BEGINSHADEBOX]

**示例：**

* `sortDescNum(3; 1; 2)`

  返回\[3， 2， 1]
* `sortDescNum(5; 3; 4)`

  返回\[5， 4， 3]


### [!UICONTROL sqrt(number)]

[!BADGE 新！]{type=Informative}

返回一个数的平方根。

>[!BEGINSHADEBOX]

**示例：**

* `sqrt(9)`

  返回3
* `sqrt(4)`

  返回2


### [!UICONTROL sub(number1； number2； ...)]

[!BADGE 新！]{type=Informative}

按提供的顺序减去所有数字。

>[!BEGINSHADEBOX]

**示例：**

* `sub(10; 3; 2)`

  返回5
* `sub(20; 5)`

  返回15
