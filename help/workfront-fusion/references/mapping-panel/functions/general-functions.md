---
title: 常规函数
description: Adobe Workfront Fusion映射面板中提供了以下常规函数。
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: 2c732659f3f3e81e13b7b12a5df5bde19c0e0928
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 常规函数

## [!UICONTROL get (object or array; path)]

返回对象或数组的值路径。 要访问嵌套对象，请使用点表示法。 数组中的第一项是索引1。

>[!BEGINSHADEBOX]

**示例：**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (expression; value1; value2)]

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

## [!UICONTROL ifempty (value1; value2)]

如果此值不为空，则返回`value1`；否则返回`value2`。

>[!BEGINSHADEBOX]

**示例：**

* `ifempty(` `A` `;` `B`

  返回

* `ifempty(` `unknown` `;` `B`

  返回B

* `ifempty(` `""` `;` `B`

  返回B

>[!ENDSHADEBOX]

## [!UICONTROL switch (expression; value1; result1; [value2; result2; ...]; [else])]

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

## [!UICONTROL omit(object; key1; [key2; ...])]

省略对象的给定键并返回其余键。

>[!BEGINSHADEBOX]

**示例：**

`omit(`用户`;`密码`)`

返回用户信息（不包括密码）的集合。

>[!ENDSHADEBOX]

## [!UICONTROL pick(object; key1; [key2; ...])]

仅从对象中选取给定的键。

>[!BEGINSHADEBOX]

**示例：**

`pick(`用户`;`密码`;`电子邮件`)`

仅返回用户的密码和电子邮件地址的集合。

>[!ENDSHADEBOX]

## mergeCollections(collection1； collection2)

通过组合键值对合并两个收藏集。 如果两个收藏集包含相同的键，则来自第二个收藏集的值将覆盖来自第一个收藏集的值。
