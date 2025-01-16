---
title: 日期和时间函数
description: 以下日期和时间函数在Adobe Workfront Fusion映射面板中可用。
author: Becky
feature: Workfront Fusion
exl-id: 92813dac-4bf0-4681-9b71-7bd2e92a89a4
source-git-commit: 2c732659f3f3e81e13b7b12a5df5bde19c0e0928
workflow-type: tm+mt
source-wordcount: '1773'
ht-degree: 1%

---

# 日期和时间函数

## 变量

### 现在

获取YYYY-MM-DD-hh:mm:ss格式的当前时间。

### 时间戳

以Unix时间戳形式获取当前时间。

## 函数

### [!UICONTROL addSeconds (date; number)]

将给定秒数添加到日期后返回新日期。 要减去秒数，请输入一个负数。

>[!BEGINSHADEBOX]

**示例：**

* `addSeconds(2016-12-08T15:55:57.536Z;2)`

  返回2016-12-08T15:55:59.536Z

* `addSeconds(2016-12-08T15:55:57.536Z;-2)`

  返回2016-12-08T15:55:55.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addMinutes (date; number)] {#addminutes-date-number}

将给定分钟数添加到日期后返回新日期。 要减去分钟，请输入一个负数。

>[!BEGINSHADEBOX]

**示例：**

* `addMinutes(2016-12-08T15:55:57.536Z;2)`

  返回2016-12-08T15:57:57.536Z

* `addMinutes(2016-12-08T15:55:57.536Z;-2)`

  返回2016-12-08T15:53:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addHours (date; number)] {#addhours-date-number}

将给定小时数添加到日期后返回新日期。 要减去小时数，请输入负数。

>[!BEGINSHADEBOX]

**示例：**

* `addHours(2016-12-08T15:55:57.536Z; 2)`

  返回2016-12-08T17:55:57.536Z

* `addHours(2016-12-08T15:55:57.536Z;-2)`

  返回2016-12-08T13:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addDays (date; number)] {#adddays-date-number}

将给定天数添加到日期后返回新日期。 要减去天数，请输入一个负数。

>[!BEGINSHADEBOX]

**示例：**

* `addDays(2016-12-08T15:55:57.536Z;2)`

  返回2016-12-10T15:55:57.536Z

* `addDays(2016-12-08T15:55:57.536Z;-2)`

  返回2016-12-6T15:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addMonths (date; number)]

向日期添加指定月份数后，返回新日期。 要减去月份，请输入负数。

>[!BEGINSHADEBOX]

**示例：**

* `addMonths(2016-08-08T15:55:57.536Z;2)`

  返回2016-10-08T15:55:57.536Z

* `addMonths(2016-08-08T15:55:57.536Z;-2)`

  返回2016-06-08T15:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL addYears (date; number)]

将给定年数添加到日期后返回新日期。 要减去年数，请输入一个负数。

>[!BEGINSHADEBOX]

**示例：**

* `addYears(2016-08-08T15:55:57.536Z;2)`

  返回2018-08-08T15:55:57.536Z

* `addYears(2016-12-08T15:55:57.536Z; -2)`

  返回2014-08-08T15:55:57.536Z

>[!ENDSHADEBOX]

### [!UICONTROL setSecond (date; number)]

此函数使用参数中指定的秒数返回新日期。

指定从0到59的数字。 如果数字超出该范围，则函数返回前一分钟（对于负数）或后续分钟（对于正数）的秒数。

如果您需要指定超出范围的数字，我们建议您使用[!UICONTROL  addSeconds]，如上文[addSeconds (date； number)](#addseconds-date-number)部分所述。

>[!BEGINSHADEBOX]

**示例：**

* `setSecond(2015-10-07T11:36:39.138Z;10)`

  返回2015-10-07T11:36:10.138Z

* `setSecond(2015-10-07T11:36:39.138Z; 6)`

  返回2015-10-07T11:37:01.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setMinute (date; number)]

此函数使用参数中指定的分钟数返回一个新日期。

指定从0到59的数字。 如果数字超出该范围，此函数将返回上一小时（对于负数）或后续小时（对于正数）的分钟数。

如果您需要指定超出范围的数字，我们建议您使用addMinutes，如上文[addMinutes (date； number)](#addminutes-date-number)中所述。

>[!BEGINSHADEBOX]

**示例：**

* `setMinute(2015-10-07T11:36:39.138Z;10)`

  返回2015-10-07T11:10:39.138Z

* `setMinute(2015-10-07T11:36:39.138Z;61)`

  返回2015-10-07T12:01:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setHour (date; number)]

此函数使用参数中指定的小时数返回一个新日期。

指定从0到23的数字。 如果数字在此范围之外，此函数将返回前一日（对于负数）或后续日（对于正数）的小时数。

如果您需要指定超出范围的数字，我们建议您使用addHours，如[addHours (date； number)](#addhours-date-number)中所述。

>[!BEGINSHADEBOX]

**示例：**

* `setHour(2015-08-07T11:36:39.138Z;6)`

  返回2015-08-07T06:36:39.138Z

* `setHour(2015-08-07T11:36:39.138;-6)`

  返回2015-08-06T18:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setDay (date; number/name of the day in English)]

此函数使用参数中指定的日期返回一个新日期。

您可以使用此函数设置星期几，星期日为1，星期六为7。 如果指定从1到7的数字，则结果日期在当前（星期日到星期六）周内。 如果此数字超出该范围，则此函数返回上一周（对于负数）或后续周（对于正数）中的某天。

如果您需要指定超出此范围的数字，我们建议您使用addDays，如上文[addDays (date； number)](#adddays-date-number)中所述。

>[!BEGINSHADEBOX]

**示例：**

* `setDay(2018-06-27T11:36:39.138Z;Monday)`

  返回2018-06-25T11:36:39.138Z

* `setDay(2018-06-27T11:36:39.138Z;1)`

  返回2018-06-24T11:36:39.138Z

* `setDay(2018-06-27T11:36:39.138Z;7)`

  返回2018-06-30T11:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setDate (date; number)]

此函数返回一个新日期，其中包含在参数中指定的月份日期。

指定从1到31的数字。 如果数字在此范围之外，此函数将返回上个月中的一天（对于负数）或后续的月份（对于正数）。

>[!BEGINSHADEBOX]

**示例：**

* `setDate(2015-08-07T11:36:39.138Z;5)`

  返回2015-08-05T11:36:39.138Z

* `setDate(2015-08-07T11:36:39.138Z;32)`

  返回2015-09-01T11:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setMonth (date; number/name of the month in English)]

此函数使用参数中指定的月份返回一个新日期。

指定从1到12的数字。 如果数字超出此范围，此函数返回上一年（对于负数）或后续年（对于正数）中的月。

>[!BEGINSHADEBOX]

**示例：**

* `setMonth(2015-08-07T11:36:39.138Z;5)`

  返回2015-05-07T11:36:39.138Z

* `setMonth(2015-08-07T11:36:39.138Z;17)`

  返回2016-05-07T11:36:39.138Z

* `setMonth(2015-08-07T11:36:39.138Z;january)`

  返回2015-01-07T12:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL setYear (date; number)]

返回具有参数中指定的年份的新日期。

>[!BEGINSHADEBOX]

**示例：**

* `setYear(2015-08-07T11:36:39.138Z;2017)`

  返回2017-08-07T11:36:39.138Z

>[!ENDSHADEBOX]

### [!UICONTROL formatDate (date; format; [timezone])]

当您有日期值（如`12-10-2021 20:30`）且要将其格式化为文本值（如`Dec 10, 2021 8:30 PM`）时，请使用此函数。

例如，当您需要在同一场景中将一个应用程序或Web服务的日期格式更改为连接的应用程序或Web服务的日期格式时，这将很有用。

有关详细信息，请参阅文章[项目数据类型](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md)中的日期和文本。

#### 参数

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>参数</th> 
   <th>预期的数据类型* </th> 
   <th>作用</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL date] </td> 
   <td>日期 </td> 
   <td> <p>将日期值转换为文本值。 </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL format] </td> 
   <td>文本 </td> 
   <td> <p>允许您使用日期/时间格式令牌指定格式。 有关详细信息，请参阅日期和时间格式的<a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">令牌</a>。</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>示例： </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL timezone] </td> 
   <td>文本 </td> 
   <td> <p>（可选）用于指定用于转换的时区。 </p> <p>有关可识别时区的列表，请参阅Wikipedia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones"> tz数据库时区列表</a>中的“TZ数据库名称”列。 函数仅将此列中列出的值识别为有效时区。 将忽略任何其他值，并改为使用配置文件中指定的方案时区。 </p> <p>如果忽略此参数，将应用用户档案设置中指定的方案时区。 </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>示例： </b></span></span><code>Europe/Prague</code>， <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

如果提供了其他类型，则应用类型强制。 有关详细信息，请参阅[类型强制](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md)。

#### 返回值和类型

`formatDate`函数根据指定的格式和时区返回给定日期值的文本表示形式。 数据类型为文本。

>[!BEGINSHADEBOX]

**示例：**&#x200B;在这些示例中，方案和Web时区都设置为`Europe/Prague`。

![](assets/date&time-functions-examples-350x61.png)

* `formatDate(1. Date created;MM/DD/YYYY)`

  返回10/01/2018

* `formatDate(1. Date created; YYYY-MM-DD hh:mm A)`

  返回2018-10-01 09:32 AM

* `formatDate(1. Date created;DD.MM.YYYY HH:mm;UTC)`

  返回01.10.2018 07:32

* `formatDate(now;DD.MM.YYYY HH:mm)`

  返回19.03.2019 15:30

>[!ENDSHADEBOX]

### [!UICONTROL parseDate (text; format; [timezone])]

当您具有表示日期（如`12-10-2019 20:30`或`Aug 18, 2019 10:00 AM`）的文本值，并且要将其转换（解析）为日期值（二进制计算机可读表示法）时，请使用此函数。 有关详细信息，请参阅文章[项目数据类型](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md)中的日期和文本。

#### 参数

第二列指示预期类型。 如果提供了其他类型，则应用类型强制。 有关详细信息，请参阅[类型强制](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md)。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>参数</th> 
   <th>预期的数据类型* </th> 
   <th>作用</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL text] </td> 
   <td>文本 </td> 
   <td> <p>将日期值转换为文本值。 </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL format] </td> 
   <td>文本 </td> 
   <td> <p>允许您使用日期/时间格式令牌指定格式。 有关详细信息，请参阅日期和时间格式的<a href="/help/workfront-fusion/references/mapping-panel/functions/tokens-for-date-and-time-formatting.md" class="MCXref xref">令牌</a>。</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>示例： </b></span></span><code>DD.MM.YYYY HH:mm</code> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL timezone] </td> 
   <td>文本 </td> 
   <td> <p>（可选）用于指定用于转换的时区。 </p> <p>有关可识别时区的列表，请参阅Wikipedia <a href="https://en.wikipedia.org/wiki/List_of_tz_database_time_zones"> tz数据库时区列表</a>中的“TZ数据库名称”列。 函数仅将此列中列出的值识别为有效时区。 将忽略任何其他值，并改为使用配置文件中指定的方案时区。 </p> <p>如果忽略此参数，将应用用户档案设置中指定的方案时区。</p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b>示例： </b></span></span><code>Europe/Prague</code>， <code>UTC</code></p> </td> 
  </tr> 
 </tbody> 
</table>

如果提供了其他类型，则应用类型强制。 有关详细信息，请参阅[类型强制](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md)。

#### 返回值和类型

此函数根据指定的格式和时区将文本字符串转换为日期。 值的数据类型是Date。

>[!BEGINSHADEBOX]

**示例：**&#x200B;在以下示例中，返回的Date值是根据ISO 8601表示的，但结果的数据类型为Date。

* `parseDate(2016-12-28;YYYY-MM-DD)`

  返回2016-12-28T00:00:00.000Z

* `parseDate(2016-12-28 16:03;YYYY-MM-DD HH:mm)`

  返回2016-12-28T16:03:00.000Z

* `parseDate(2016-12-28 04:03 pm; YYYY-MM-DD hh:mm a)`

  返回2016-12-28T16:03:06.000Z

* `parseDate(1482940986;X)`

  返回2016-12-28T16:03:06.000Z

>[!ENDSHADEBOX]

### [!UICONTROL dateDifference (Date1; Date2; Unit)]

返回表示两个日期之差的数字，以指定的单位表示。

从Date1减去Date2。

为`unit`参数使用以下时间值之一：

* 毫秒
* 秒
* 分钟
* 小时
* 天
* 星期
* 月

如果未指定单位，此函数将返回毫秒之差。

>[!BEGINSHADEBOX]

**示例：**

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z)`

  返回`600,000`

* `dateDifference(2021-05-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;hours)`

  返回`4`

* `dateDifference2021-06-11T18:10:00.000Z;2021-05-11T18:00:00.000Z;months)`

  返回`1`

>[!ENDSHADEBOX]

### 其他示例

#### 如何计算月中每周的第n天

此部分针对[!DNL Exceljet]网页中的[!DNL Workfront Fusion]进行改编，该网页介绍了如何获取一个月中的第n天。

如果您需要计算与每月第n天对应的日期（例如，第一个星期二、第三个星期五等），可以使用以下公式：

![](assets/date&time-functions-calc-nth-day-350x31.png)

```
{{addDays(setDate(1.date; 1); 1.n * 7 - formatDate(addDays(setDate(1.date; 1); "-" + 1.dow); "E"))}}
```

公式包含以下项：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>1.n</code> </td> 
   <td> <p> 第n天：</p> 
    <ul> 
     <li><code>1</code> （第1个星期二）</li> 
     <li><code>2</code> 第2个星期二</li> 
     <li><code>3</code> 第3个星期二，以此类推</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>2.dow</code> </td> 
   <td> <p> 每周时间：</p> 
    <ul> 
     <li><code>1</code> 表示星期一</li> 
     <li><code>2</code> 表示星期二</li> 
     <li><code>3</code> 表示星期三</li> 
     <li><code>4</code> 表示周四</li> 
     <li><code>5</code> 表示星期五</li> 
     <li><code>6</code> 表示星期六</li> 
     <li><code>7</code> 表示星期日</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td><code>1.date</code> </td> 
   <td> <p> 日期决定月份。 要计算当前月份中每周的第n天，请使用<code>now</code>变量。</p> </td> 
  </tr> 
 </tbody> 
</table>

如果您只想计算一个特定情况，例如，每逢星期三，则可以用相应的数字替换公式中的项`1.n`和`2.dow`。 对于当月的第二个星期三，您将使用以下值：

* `1.n` = `2`
* `1.dow` = `3`
* `1.date` = `now`

![](assets/nth-day-variable-value-350x33.png)

#### 说明：

* `setDate(now;1)`返回当月的第一个月
* `formatDate(....;E)`返回星期几(1， 2， ... 6)

### 如何计算日期之间的天数

一种方法是使用以下表达式：

![](assets/calculate-days-between-dates-350x68.png)

```
{{round((2.value - 1.value) / 1000 / 60 / 60 / 24)}}
```

>[!NOTE]
>
>* `D1`和`D2`的值必须为Date类型值。 如果它们是字符串类型值（例如，20.10.2018），请使用`parseDate()`函数将它们转换为日期类型值。
>
>* `round()`函数用于日期之一在夏令时时间段内，而另一个日期不在夏令时时间段内的情况。 在这些情况下，小时数差等于或少于一小时。 对于非整数结果，可以将其除以24。 你损失了一个小时的夏令时。 将其扁平化以便没有百分比

#### 如何计算每月的最后一天/毫秒

例如，当您在搜索模块中指定日期范围时，如果该范围跨越整个前一个月为一个关闭间隔（该间隔包含其两个限制点），则需要计算当月的最后一天。

2019-09-01 ≤ D ≤ 2019-09-30

下面的公式显示了一种计算上个月最后一天的方法：

![](assets/last-day-prev-month.png)

```
{{addDays(setDate(now; 1); -1)}}
```

在某些情况下，您不仅需要计算每月的最后一天，还需要计算每月的最后一毫秒：

2019-09-01T00:00:00.000Z ≤ D ≤ 2019-09-30T23:59:59.999Z

此公式显示了一种计算上个月最后一毫秒的方法：

![](assets/last-millisecond-prev-month-350x45.png)

```
{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD"; "UTC") - 1; "x")}}
```

如果需要结果以使用时区设置，请忽略UTC参数：

![](assets/omit-utc-argument-350x45.png)

`{{parseDate(parseDate(formatDate(now; "YYYYMM01"); "YYYYMMDD") - 1; "x")}}`

但是，最好改用半开间隔（排除其限制点之一的间隔），指定下个月的第一天，并将“小于或等于”运算符替换为“小于”，如下所示：

`2019-09-01 ≤ D < 2019-10-01`

`2019-09-01T00:00:00.000Z ≤ D < 2019-10-01T00:00:00.000Z`
