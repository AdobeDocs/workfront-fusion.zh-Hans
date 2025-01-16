---
title: 数组函数
description: Adobe Workfront Fusion映射面板中提供了以下数组函数。
author: Becky
feature: Workfront Fusion
exl-id: 16c3915c-add1-4aab-a0e1-75fc590c42a6
source-git-commit: 2c732659f3f3e81e13b7b12a5df5bde19c0e0928
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# 数组函数

## [!UICONTROL join (array; separator)]

将数组的全部项串联到一个字符串中，在每个项之间使用指定的分隔符。

## [!UICONTROL length (array)]

返回数组中的项数。

## [!UICONTROL keys (object)]

返回给定对象或数组的属性的数组。

## [!UICONTROL slice (array; start; [end])]

返回仅包含选定项目的新数组。

## [!UICONTROL merge (array1; array2; ...)]

将一个或多个阵列合并到一个阵列中。

## [!UICONTROL contains (array; value)]

验证数组是否包含值。

## [!UICONTROL remove (array; value1; value2; ...)]

删除数组的参数中指定的值。 此函数仅对文本或数字的原始数组有效。

## [!UICONTROL add (array; value1; value2; ...)]

将参数中指定的值添加到数组中并返回该数组。

## [!UICONTROL map (complex array; key;[key for filtering];[possible values for filtering])]

返回包含复杂数组的值的原始数组。 此函数允许过滤值。 对键使用原始变量名称。

>[!BEGINSHADEBOX]

**示例：**

* `map(Emails[];email)`

  返回带有电子邮件的原始数组

* `map(Emails[];email;label;work;home)`

  返回带有标签等于工作或主页的原始数组

>[!ENDSHADEBOX]

有关详细信息，请参阅[映射数组或数组元素](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md)。

## 随机播放

## [!UICONTROL sort (array; [order]; [key])]

对数组的值进行排序。 `order`参数的有效值为：

* `asc`

  （默认） — 升序：类型“数字”为1、2、3、...。 A， B， C， a， b， c， ...表示文字

* `desc`

  降序： ...， 3， 2， 1表示类型“数字”。...， c， b， a， C， B， A代表文字。

* `asc ci`

  不区分大小写的升序：A、a、B、b、C、c...表示文本类型。

* `desc ci`

  不区分大小写降序： ...， C， c， B， b， A，用于类型“文本”。

使用`key`参数访问复杂对象内的属性。

对键使用原始变量名称。

要访问嵌套属性，请使用点表示法。

数组中的第一项是索引1。

>[!BEGINSHADEBOX]

**示例：**

* `sort(Contacts[];name)`

  按“name”属性以默认升序排序联系人数组

* `sort(Contacts[];desc;name)`

  按“name”属性降序排列联系人数组

* `sort(Contacts[];asc ci;name)`

  按“name”属性以不区分大小写的升序对联系人数组排序

* `sort(Emails[];sender.name)`

  按“sender.name”属性对电子邮件数组排序

>[!ENDSHADEBOX]

## [!UICONTROL reverse (array)]

数组的第一个元素成为最后一个元素，第二个元素成为倒数第二个元素，依此类推。

## [!UICONTROL flatten (array)]

创建一个新数组，其中所有子数组元素以递归方式连接到该数组，直至指定深度。

## [!UICONTROL distinct (array; [key])]

删除数组中的重复项。 使用“[!UICONTROL key]”参数访问复杂对象内的属性。 要访问嵌套属性，请使用点表示法。 数组中的第一项是索引1。

>[!BEGINSHADEBOX]

**示例：** `distinct(Contacts[];name)`

通过比较“name”属性，删除联系人数组中的重复项

>[!ENDSHADEBOX]

## toCollection

## toArray

此函数将一个集合转换为键值对的数组。

>[!BEGINSHADEBOX]

**示例：**

给定收藏集

`{ key1: "value1", key2: "value2:}`

函数

`toArray({ key1: "value1", key2: "value2:})`

返回键值对的数组

`[{ key1: "value1"}, { key2: "value2"}]`

>[!ENDSHADEBOX]

## [!UICONTROL arrayDifference [array1, array2, mode]]

返回两个数组之间的差值。

为`mode`参数输入以下值之一。

* `classic`：返回一个新数组，该数组包含`array2`中不存在的`array1`的所有元素。

* `symmetric`：返回两个数组不共用的元素数组。

  换言之，该函数返回的数组包含`array1`中不存在于`array2`中的所有元素，以及`array2`中不存在于`array1`中的所有元素。

>[!BEGINSHADEBOX]

**示例：**

给定以下数组：

```
myArray = [1,2,3,4,5]
```

```
yourArray = [3,4,5,6,7]
```

* `arrayDifference [myArray, yourArray, classic]`

  返回`[1,2]`

* `arrayDifference [yourArray, myArray, classic]`

  返回`[6,7]`

* `arrayDifference [myArray, yourArray, symmetric]`

  返回`[1,2,6,7]`

>[!ENDSHADEBOX]

## 删除重复项

## 关键字

## emptyarray
