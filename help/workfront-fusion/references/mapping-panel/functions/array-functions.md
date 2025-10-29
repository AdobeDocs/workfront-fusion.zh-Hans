---
title: 数组函数
description: Adobe Workfront Fusion映射面板中提供了以下数组函数。
author: Becky
feature: Workfront Fusion
exl-id: 16c3915c-add1-4aab-a0e1-75fc590c42a6
source-git-commit: 9b61a3b18df1f755cc7ccc28889564e4bcb6cda0
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 0%

---

# 数组函数

## [!UICONTROL 联接（数组；分隔符）]

将数组的全部项串联到一个字符串中，在每个项之间使用指定的分隔符。

## [!UICONTROL 长度（数组）]

返回数组中的项数。

## [!UICONTROL 键（对象）]

返回给定对象或数组的属性的数组。

## [!UICONTROL 片（数组；开始；[结束]）]

返回仅包含选定项目的新数组。

## [!UICONTROL 合并(array1； array2； ...)]

将一个或多个阵列合并到一个阵列中。

## [!UICONTROL 包含（数组；值）]

验证数组是否包含值。

## [!UICONTROL 移除（数组；值1；值2； ...）]

删除数组的参数中指定的值。 此函数仅对文本或数字的原始数组有效。

## [!UICONTROL 添加（数组；值1；值2； ...）]

将参数中指定的值添加到数组中并返回该数组。

## [!UICONTROL 映射（复数数组；键；[用于筛选的键]；[用于筛选的可能值]）]

返回包含复杂数组的值的原始数组。 此函数允许过滤值。 对键使用原始变量名称。

>[!BEGINSHADEBOX]

**示例：**

* `map(Emails[];email)`

  返回带有电子邮件的原始数组

* `map(Emails[];email;label;work)`

  返回带有标签等于工作的电子邮件的原始数组

>[!ENDSHADEBOX]

有关详细信息，请参阅[映射数组或数组元素](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md)。

## 随机播放

## [!UICONTROL 排序（数组；[顺序]；[键]）]

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

## [!UICONTROL 反向（数组）]

数组的第一个元素成为最后一个元素，第二个元素成为倒数第二个元素，依此类推。

## [!UICONTROL 平面化（数组）]

创建一个新数组，其中所有子数组元素以递归方式连接到该数组，直至指定深度。

## [!UICONTROL distinct （数组；[键]）]

删除数组中的重复项。 使用“[!UICONTROL key]”参数访问复杂对象内的属性。 要访问嵌套属性，请使用点表示法。 数组中的第一项是索引1。

>[!BEGINSHADEBOX]

**示例：** `distinct(Contacts[];name)`

通过比较“name”属性，删除联系人数组中的重复项

>[!ENDSHADEBOX]

## toCollection

* 此函数接受一个包含键值对的数组，并将其转换为一个集合。 函数有3个参数：

* （数组）包含键值对
* （字符串）用作键的字段的名称
* （字符串）要用作值的字段的名称

>[!BEGINSHADEBOX]

示例：

给定数组：

```
[{"name":"Bob", "age":22}, {"name":"Tim", "age":23}]
```

和参数

```
{{toCollection(6.array; "name"; "age")}}
```

函数返回

```
{
    "Bob": 22,
    "Tim": 23
}
```

>[!ENDSHADEBOX]

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

## [!UICONTROL arrayDifference [array1， array2， mode]]

返回两个数组之间的差值。

为`mode`参数输入以下值之一。

* `classic`：返回一个新数组，该数组包含`array1`中不存在的`array2`的所有元素。

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
