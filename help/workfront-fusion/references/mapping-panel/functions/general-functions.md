---
title: 常规函数
description: Adobe Workfront Fusion映射面板中提供了以下常规函数。
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: e11e581c092ebba343a0f2d6943ecbe4d0fe4c87
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 7%

---

# 常规函数

## 变量

您可以使用这些常规变量来标识有关执行的详细信息：

* `executionID`：此方案执行的ID
* `triggerTimestamp`：触发此执行的时间
* `scenarioID`：当前打开的场景的 ID
* `operationsConsumed`：场景在该点已使用的操作次数

## [!UICONTROL get （对象或数组；路径）]

返回对象或数组的值路径。 要访问嵌套对象，请使用点表示法。 数组中的第一项是索引1。

>[!BEGINSHADEBOX]

**示例：**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if （表达式；值1；值2）]

如果表达式计算为true，则返回`value1`；否则，返回`value2`。

若要创建if语句（仅当两个或更多表达式被计算为true时才返回值），请使用`and`关键字。

要合并`if`语句，请使用`and`和`or`运算符。

![和运算符](assets/and-in-if-statement.png)

>[!BEGINSHADEBOX]

**示例：**

* `if( 1 = 1 ; A ; B )`

  返回

* `if( 1 = 2 ; A ; B )`

  返回B

* `if( 1 = 2 and 1 = 2 ; A ; B )`

  返回B

>[!ENDSHADEBOX]

## [!UICONTROL ifempty （值1；值2）]

如果此值不为空，则返回`value1`；否则返回`value2`。

>[!BEGINSHADEBOX]

**示例：**

* `ifempty(` `A` `;` `B` )

  返回

* `ifempty(` `unknown` `;` `B` )

  返回B

* `ifempty(` `""` `;` `B` )

  返回B

>[!ENDSHADEBOX]

## [!UICONTROL switch （表达式；值1；结果1；[值2；结果2； ...]；[else]）]

根据值列表计算一个值（称为表达式）；返回与第一个匹配值对应的结果。 要包含`else`值，请将其添加到最终表达式或值之后。

>[!BEGINSHADEBOX]

**示例：**

* `switch( B ; A ; 1 ; B ; 2 ; C ; 3 )`

  返回2

* `switch( C ; A ; 1 ; B ; 2 ; C ; 3 )`

  返回3

* `switch( X ; A ; 1 ; B ; 2 ; C ; 3 ; 4 )`

  返回4

  在此函数中，4是在未应用表达式时要返回的值（`else`值）。

>[!ENDSHADEBOX]

## [!UICONTROL 省略（对象；键1；[键2； ...]）]

省略对象的给定键并返回其余键。

>[!BEGINSHADEBOX]

**示例：**

`omit(`用户`;`密码`)`

返回用户信息（不包括密码）的集合。

>[!ENDSHADEBOX]

## [!UICONTROL pick(object； key1； [key2； ...])]

仅从对象中选取给定的键。

>[!BEGINSHADEBOX]

**示例：**

`pick(`用户`;`密码`;`电子邮件`)`

仅返回用户的密码和电子邮件地址的集合。

>[!ENDSHADEBOX]

## mergeCollections(collection1； collection2)

通过组合键值对合并两个收藏集。 如果两个收藏集包含相同的键，则来自第二个收藏集的值将覆盖来自第一个收藏集的值。

### [!UICONTROL isBlank(value)]

如果值为`null`或空字符串，则返回`true`，否则返回`false`。 与`ifEmpty`不同，此函数不将数字`0`或仅包含空格的字符串视为空白。

>[!BEGINSHADEBOX]

**示例：**

* `isBlank("")     `

  返回true
* `isBlank(null)   `

  返回true
* `isBlank("Hello")`

  返回false
* `isBlank(0)      `

  返回false
* `isBlank(" ")    `

  返回false

>[!ENDSHADEBOX]


### [!UICONTROL in(value； value1； value2； ...)]

如果值与提供的值之一（严格相等，无类型强制）相等，则返回`true`。

>[!BEGINSHADEBOX]

**示例：**

* `in("B"; "A"; "B"; "C")`

  返回true
* `in("D"; "A"; "B"; "C")`

  返回false
* `in(2; 1; 2; 3)        `

  返回true
* `in("2"; 1; 2; 3)      `

  返回false

>[!ENDSHADEBOX]

### [!UICONTROL ifin(value； value1； value2； ...； trueExpression； falseExpression)]

如果值与提供的任何匹配值匹配，则返回`trueExpression`，否则返回`falseExpression`。 至少需要3个参数（值、一个匹配值以及trueExpression + falseExpression）。

>[!BEGINSHADEBOX]

**示例：**

* `ifin("B"; "A"; "B"; "yes"; "no")`

  返回yes
* `ifin("D"; "A"; "B"; "yes"; "no")`

  返回否
* `ifin("X"; "X"; "found"; "not found")`

  找到退货

>[!ENDSHADEBOX]

### [!UICONTROL case(indexNumber； value1； value2； ...)]

返回由索引号（从1开始）指定的位置的值。 如果索引超出范围或为0，则返回`null`。

>[!BEGINSHADEBOX]

**示例：**

* `case(1; "Sun"; "Mon"; "Tue")`

  返回Sun
* `case(2; "Sun"; "Mon"; "Tue")`

  返回星期一
* `case(3; "Sun"; "Mon"; "Tue")`

  返回星期二
* `case(5; "a"; "b")           `

  返回空值

>[!NOTE]
>
>我们建议使用此项来获取日期的日期名称：
>`case(dayOfWeek(date); "Sun"; "Mon"; "Tue"; "Wed"; "Thu"; "Fri"; "Sat")`

>[!ENDSHADEBOX]

