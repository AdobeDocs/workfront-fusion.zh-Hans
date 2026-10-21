---
title: 常规函数
description: Adobe Workfront Fusion映射面板中提供了以下常规函数。
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
TQID: 'https://experienceleague.adobe.com/1IX25ZtrWVizi5gZJfFw-acnW5eIuXpGgcXgXW0T-Hw'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 8ea986eb6573bb49accfad312bb0796faa2642ab
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 5%
---
# 常规函数

## 变量

您可以使用这些常规变量来标识有关执行的详细信息：

* `executionId`：此方案执行的ID
* `scenarioId`：当前打开的场景的 ID
* `scenarioName`：当前正在运行的方案的名称
* `scenarioUrl`： Fusion用户界面中当前方案的链接
* `executionUrl`：指向Fusion用户界面中当前方案执行的链接
* `scenarioApiUrl`：当前方案的Fusion API URL
* `executionApiUrl`：当前执行详细信息的融合API URL
* `teamId`：拥有当前场景的Fusion团队的ID
* `organizationId`：与当前执行关联的Fusion组织的ID。 这不是Adobe IMS组织ID。
* `triggerTimestamp`：触发此执行的时间
* `operationsConsumed`：场景在该点已使用的操作次数

变量名称区分大小写。 例如，使用`scenarioUrl`，而不是`scenarioURL`。

您可以在映射的字段中使用这些变量，而无需构建URL或硬编码团队和组织ID。 例如，您可以在通知的映射文本字段中包含以下内容：

<pre><code>
Scenario: &#123;&#123;scenarioName&#125;&#125;
Open scenario: &#123;&#123;scenarioUrl&#125;&#125;
Open execution: &#123;&#123;executionUrl&#125;&#125;
Team: &#123;&#123;teamId&#125;&#125;
Organization: &#123;&#123;organizationId&#125;&#125;
</code></pre>

在使用这些变量时，请牢记以下几点：

* 当场景运行时，将解析值。 映射面板会列出变量，但不会预览其值。
* `scenarioUrl`和`executionUrl`链接到Fusion用户界面中的方案和执行。 `scenarioApiUrl`和`executionApiUrl`是API终结点URL，而不是指向Fusion页面的链接。
* API URL变量仅返回文本。 他们不会提出请求或提供身份验证凭据。 普通API身份验证和权限仍然适用。
* 链接不授予其他访问权限。 普通Fusion权限在此适用。
* 对于未保存到执行历史记录中的运行（如沙盒运行或在历史记录同步关闭的情况下运行），不会生成`executionUrl`。 生成的链接并不保证执行详细信息在您使用该链接时可用。
* 无法为模板或未保存的方案生成`scenarioUrl`。
* 如果无法生成URL，则变量没有值。

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

