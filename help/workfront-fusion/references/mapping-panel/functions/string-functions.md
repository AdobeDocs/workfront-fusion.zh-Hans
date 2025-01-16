---
title: 字符串函数
description: Adobe Workfront Fusion映射面板中提供了以下字符串函数。
author: Becky
feature: Workfront Fusion
exl-id: d3e49fce-85bc-4ee6-9a94-497a306e0c74
source-git-commit: 2c732659f3f3e81e13b7b12a5df5bde19c0e0928
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# 字符串函数

## [!UICONTROL length (text or buffer)]

返回文本字符串的长度（字符数）或二进制缓冲区的长度（缓冲区大小，以字节为单位）。

>[!BEGINSHADEBOX]

**示例：**

`length( hello )`

返回：5

>[!ENDSHADEBOX]

## [!UICONTROL lower (text)]

将文本字符串中的所有字母字符转换为小写。

>[!BEGINSHADEBOX]

**示例：**

`lower( Hello )`

返回： hello

>[!ENDSHADEBOX]

## [!UICONTROL capitalize (text)]

将文本字符串中的第一个字符转换为大写。

>[!BEGINSHADEBOX]

**示例：**

`capitalize( workfront )`

返回： [!DNL Workfront]

>[!ENDSHADEBOX]

## [!UICONTROL startcase (text)]

每个单词的首字母使用大写，其他字母使用小写。

>[!BEGINSHADEBOX]

**示例：**
`startcase( hello WORLD )`

返回： [!UICONTROL Hello World]

>[!ENDSHADEBOX]

## [!UICONTROL ascii (text; [remove diacritics])]

从文本字符串中删除所有非ascii字符。

>[!BEGINSHADEBOX]

**示例：**

* `ascii(` `Wěošrčkřfžrýoáníté` `)`

返回： [!DNL Workfront]

* `ascii(` `ěščřž` `;` `true` `)`

返回： [!UICONTROL escrz]

>[!ENDSHADEBOX]

## [!UICONTROL replace (text;search string; replacement string)]

将搜索字符串替换为新的字符串。

>[!BEGINSHADEBOX]

**示例：**

`replace( Hello World ; Hello ; Hi )`

返回： [!UICONTROL Hi World]

>[!ENDSHADEBOX]

正则表达式（包含在`/.../`中）可用作附加了标志（如`g`、`i`、`m`）的组合的搜索字符串：

>[!BEGINSHADEBOX]

**示例：**

![](assets/replace---1-350x31.png)

所有这些数字X X X X X都替换为X

>[!ENDSHADEBOX]

替换字符串可以包含以下特殊替换模式：

* `$&`插入匹配的子字符串。
* `$n`其中n是小于100的正整数，插入带括号的n个子匹配字符串。 这是1索引。

>[!BEGINSHADEBOX]

**示例：**

![](assets/variable-value-350x63.png)

返回：电话号码`+420777111222`

![](assets/variable-value---2-350x55.png)

返回：电话号码： `+420777111222`

>[!CAUTION]
>
>请勿在替换字符串参数中使用命名捕获组，如`/ is (?<number>\d+)/`。 这样做会导致错误。


>[!ENDSHADEBOX]

有关正则表达式的详细信息，请参阅[文本分析器](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/text-parser.md)。

## [!UICONTROL trim (text)]

删除文本开头或结尾的空格字符。

## [!UICONTROL upper (text)]

将文本字符串中的所有字母字符转换为大写。

>[!BEGINSHADEBOX]

**示例：**

`upper( Hello )`

返回： [!UICONTROL HELLO]

>[!ENDSHADEBOX]

## [!UICONTROL substring (text; start;end)]

返回文本字符串在“开始”位置和“结束”位置之间的部分。

>[!BEGINSHADEBOX]

**示例：**

* `substring( Hello ; 0 ; 3)`

  返回：帮助

* `substring( Hello ; 1 ; 3 )`

  返回： el

>[!ENDSHADEBOX]

## [!DNL indexOf (string; value; [start])]

返回指定值在字符串中第一次出现的位置。 如果搜索的值不存在，则此方法将返回“–1”。 起始值表示搜索在字符串中的开始位置。

>[!BEGINSHADEBOX]

**示例：**

* `indexOf( Workfront ; o )`

  返回： 1

* `indexOf( Workfront ; x )`

  返回： -1

* `indexOf( Workfront ; o ; 3 )`

  返回：6

>[!ENDSHADEBOX]

## [!UICONTROL toBinary (value)]

将任意值转换为二进制数据。

您还可以指定编码作为第二个参数，以将十六进制或base64的二进制转换应用于二进制数据。

>[!BEGINSHADEBOX]

**示例：**

* `toBinary( Workfront )`

  返回：57 6f 72 6b 66 72 6f 6e 74

* `toBinary( V29ya2Zyb250 ; base64 )`

  返回：57 6f 72 6b 66 72 6f 6e 74

>[!ENDSHADEBOX]

## [!UICONTROL toString (value)]

将任意值转换为字符串。

## [!UICONTROL encodeURL (text)]

将某些文本中的特殊字符编码为有效的URL地址。

## [!UICONTROL decodeURL (text)]

将URL中的特殊字符解码为文本。

>[!BEGINSHADEBOX]

**示例：**
`decodeURL( Automate%20your%20workflow )`

返回： [!UICONTROL Automate your workflow]

>[!ENDSHADEBOX]

## [!UICONTROL escapeHTML (text)]

转义文本中的所有HTML标签。

>[!BEGINSHADEBOX]

**示例：**

`escapeHTML( <b>Hello</b> )`

返回： `&lt;b&gt;Hello&lt;/b&gt;`

>[!ENDSHADEBOX]

## [!UICONTROL escapeMarkdown(text)]

转义文本中的所有Markdown标记。

>[!BEGINSHADEBOX]

**示例：**

`escapeMarkdown( # Header )`

返回： `&#35; Header`

>[!ENDSHADEBOX]

## [!UICONTROL stripHTML (text)]

从文本中删除所有HTML标签。

>[!BEGINSHADEBOX]

**示例：**

`stripHTML( <b>Hello</b> )`

返回： Hello

>[!ENDSHADEBOX]

## 包含（文本；搜索字符串）

验证文本是否包含搜索字符串。

>[!BEGINSHADEBOX]

**示例：**

* `contains( Hello World ; Hello )`

  返回： [!UICONTROL true]

* `contains( Hello World ; Bye )`

  返回： [!UICONTROL false]

>[!ENDSHADEBOX]

## [!UICONTROL split (text; separator)]

通过将字符串拆分为子字符串，将字符串拆分为字符串数组。

>[!BEGINSHADEBOX]

**示例：**

`split( John, George, Paul ; , )`

>[!ENDSHADEBOX]

## [!UICONTROL md5 (text)]

计算字符串的md5哈希值。

>[!BEGINSHADEBOX]

**示例：**

`md5( Workfront )`

返回： `1448bbbeaa7a9b8091d426999f1f666b`

>[!ENDSHADEBOX]

## [!UICONTROL sha1 (text; [encoding]; [key])]

计算字符串的sha1哈希。 如果指定了键参数，则返回sha1 HMAC哈希。 支持的编码：“hex”（默认）、“base64”或“latin1”。

>[!BEGINSHADEBOX]

**示例：**

`sha1( workfront )`

返回：b2b30b8ae1f9e5b40fbb0696eaabdbfd8d0c087f

>[!ENDSHADEBOX]

## [!UICONTROL sha256 (text; [encoding]; [key])]

计算字符串的sha256哈希。 如果指定了键参数，则返回sha256 HMAC哈希。 支持的编码：“hex”（默认）、“base64”或“latin1”。>

>[!BEGINSHADEBOX]

**示例：**

`sha256( workfront )`

返回：ed3d7397eec7b94453035b67ba4468c883ee3bedeb57137f7371f2e0cf5e2bbc

>[!ENDSHADEBOX]

## [!UICONTROL sha512 (text; [output encoding]; [key]; [key encoding])]

计算字符串的sha512哈希。 如果指定了键参数，则返回sha512 HMAC哈希。

支持的编码：

* &quot;[!UICONTROL hex]&quot; （默认）
* &quot;[!UICONTROL base64]&quot;
* &quot;[!UICONTROL latin1]&quot;

支持的密钥编码：

* &quot;[!UICONTROL text]&quot; （默认）
* &quot;[!UICONTROL hex]&quot;
* &quot;[!UICONTROL base64]&quot;或&quot;[!UICONTROL binary]&quot;

使用“[!UICONTROL binary]”密钥编码时，密钥必须是缓冲区，而不是字符串。

>[!BEGINSHADEBOX]

**示例：**

`sha512(workfront)`

返回：789ae41b9456357e4f27c6a09956a767abbb8d80b206003ffdd1e94dbc687cd119b85e1e19db58bb44b234493af35fd431639c0345aadf2cf7ec26e9f4a7fb19

>[!ENDSHADEBOX]

## [!UICONTROL base64 (text)]

将文本转换为base64。

>[!BEGINSHADEBOX]

**示例：**

`base64( workfront )`

返回：d29ya2Zyb250==

>[!ENDSHADEBOX]
