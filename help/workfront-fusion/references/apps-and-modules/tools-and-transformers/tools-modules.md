---
title: 工具
description: ' [!DNL Adobe Workfront Fusion Tools] 部分包含几个可增强方案的有用模块。'
author: Becky
feature: Workfront Fusion
exl-id: d9425f5b-4f4a-42da-9aca-1c1783be5fa7
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '2286'
ht-degree: 0%

---

# [!UICONTROL 工具]

[!DNL Adobe Workfront Fusion Tools]部分包含几个可以增强方案的有用模块。

[!UICONTROL 工具]模块可从应用列表或屏幕底部的[!UICONTROL 工具]图标![工具图标](/help/workfront-fusion/references/apps-and-modules/assets/tools-icon-small.png)中获取。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>无Workfront Fusion许可证要求</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## [!UICONTROL 工具]及其字段

* [触发器](#triggers)
* [操作](#actions)
* [汇总](#aggregators)
* [变压器](#transformers)

### 触发器

#### [!UICONTROL 基本触发器]

利用此模块，可创建自定义触发器并定义其输入捆绑包。

例如，您可以将此模块用于计划发送到指定电子邮件地址的联系人或任何其他列表（如[!UICONTROL 电子邮件] >[!UICONTROL 发送电子邮件]，或[!DNL Gmail] >[!UICONTROL 发送电子邮件]模块），或用作要在需要时触发的简单提醒。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL包]</td> 
   <td> <p>通过添加数组项创建自定义包。 对于要添加到捆绑包中的每个项目，单击<b>添加项目</b>并输入项目的名称和值。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 获取多个变量]](#get-multiple-variables)
* [[!UICONTROL 获取变量]](#get-variable)
* [[!UICONTROL 增量函数]](#increment-function)
* [[!UICONTROL 设置多个变量]](#set-multiple-variables)
* [[!UICONTROL 设置变量]](#set-variable)
* [[!UICONTROL 睡眠]](#sleep)

#### [!UICONTROL 获取多个变量]

此模块可检索先前由[!UICONTROL Set Variable]或[!UICONTROL Set Multiple Variables]模块创建的值。

此模块可以读取在场景中的任意位置设置的变量，即使该变量与[!UICONTROL 获取多个变量]模块所在的路由不同。 唯一的要求是，在[!UICONTROL 工具] > [!UICONTROL 获取多个变量]模块之前执行[!UICONTROL 工具] > [!UICONTROL 设置变量]或[!UICONTROL 工具] > [!UICONTROL 设置多个变量]模块。 有关模块执行顺序的详细信息，请参阅[添加路由器模块并配置路由](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)。

<table style="table-layout:auto">
    <tr>
        <td>[！UICONTROL Variables]</td>
        <td>对于您希望模块获取的每个变量，单击<b>添加项</b>并输入变量的名称。</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

**示例：**&#x200B;以下可能是对[!UICONTROL Set]/[!UICONTROL Get（多个）变量]模块的使用：

* 用于存储计算值以供以后使用，即使是在不同的路由中。 当该值在多个模块中使用，并且计算该值的公式过于复杂时，这将很有用。
* 调试公式。 如果模块中使用的公式似乎未提供正确的结果，请复制该公式并将其粘贴到您在相关模块之前插入的[!UICONTROL 设置变量]模块中。 在[!UICONTROL Set Variable]模块后断开模块连接并执行方案。 验证[!UICONTROL 设置变量]模块的输出，调整或简化公式，再次执行方案，并继续执行该操作，直到问题得到解决。

>[!ENDSHADEBOX]


#### [!UICONTROL 获取变量]

此模块可检索先前由[!UICONTROL 设置变量]或[!UICONTROL 设置多个变量]模块创建的值。

此模块可以读取在场景中任意位置设置的变量，即使该变量与[!UICONTROL Get Variable]模块所在的路由不同。 唯一要求是[!UICONTROL Tools] > [!UICONTROL Set Variable]或[!UICONTROL Tools] > [!UICONTROL Set Multiple Variables]模块在[!UICONTROL Tools] > [!UICONTROL Get Variable]模块之前执行。 有关模块执行顺序的详细信息，请参阅[添加路由器模块并配置路由](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量名称]</td> 
   <td> <p>映射您希望模块获取的变量的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 增量函数]

此模块会在每个周期或每个方案运行后返回一个以1递增的值。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL重置值]</td> 
   <td> <p>选择您希望模块重置值的时间。 当您希望值从第一个值开始时。</p> 
    <ul> 
     <li>[！UICONTROL After One cycle]</li> 
     <li>[！UICONTROL After one scenario run]</li> 
     <li>[！UICONTROL从不]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**

此模块可用于实现向组中的用户分配任务、商机、电子邮件等“循环调度”。 算法按照一定的合理顺序从一组中选取被分配人，通常从列表的顶部到底部。 当算法到达列表结尾时，它将向位于列表顶部的用户分配下一个分配，并继续向列表下方进行分配。

以下方案会在每个奇数方案运行后向第一个收件人发送电子邮件，并在每个偶数方案运行后向第二个收件人发送电子邮件。

![示例电子邮件](/help/workfront-fusion/references/apps-and-modules/assets/example-email.png)

要创建此方案，请执行以下操作：

1. 将模块的&#x200B;**[!UICONTROL 重置值]**&#x200B;字段设置为“从不”。
1. 为奇数值设置路由。 使用等于`1`的模数数学函数设置此路由的过滤器：

   ![奇数](/help/workfront-fusion/references/apps-and-modules/assets/odd.png)

**注意**：不要忘记将[!UICONTROL 等于]运算符从默认的[!UICONTROL 文本]运算符更改为[!UICONTROL 数值]运算符。

1. 使用等于`0`的模数数学函数为偶数设置路径：

增量函数在每次场景运行时都添加一个。 过滤器会检查增量并根据其值执行操作，以确保平均分配电子邮件。

>[!ENDSHADEBOX]

#### [!UICONTROL 设置多个变量]

此模块创建可由路由中的其他模块映射的变量。 此变量还可以映射到场景中任何路由的[!UICONTROL 获取变量]或[!UICONTROL 获取多个变量]模块。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Variables]</td> 
   <td>对于要添加的每个变量，单击<b>添加项</b>并输入变量的名称和值。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL变量生命周期] </td> 
   <td> <p>选择您希望变量保持有效的时长（保持相同的值）。</p> 
    <ul> 
     <li><strong>[！UICONTROL One cycle]</strong>：变量对一个周期有效。 当在一个场景运行中收到多个Webhook时，这非常有用，因为更多Webhook会创建更多周期。 </li> 
     <li><strong>[！UICONTROL One执行]</strong>：变量对一个方案执行有效。 一个执行可以包含一个或多个周期。</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 设置变量]

此模块创建一个可由路由中的其他模块映射的变量。 此变量还可以映射到场景中任何路由的[!UICONTROL 获取变量]或[!UICONTROL 获取多个变量]模块。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL变量名称] </td> 
   <td>输入变量名称。 在其他模块中映射变量时，将显示此名称。 </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL变量生命周期] </td> 
   <td> <p>选择您希望变量保持有效的时长（保持相同的值）。</p> 
    <ul> 
     <li><strong>[！UICONTROL One cycle]</strong>：变量对一个周期有效。 在收到一个场景运行中的多个Webhook时（更多Webhook =更多周期）非常有用。 </li> 
     <li><strong>[！UICONTROL One执行]</strong>：变量对一个方案执行有效。 一个执行可以包含一个或多个周期。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL变量值] </td> 
   <td>输入或映射变量的值。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 睡眠]

利用此模块，可将方案流延迟最多300秒（5分钟）。

例如，如果要降低[!DNL target]服务服务器负载或在发送批量短信或电子邮件时模拟人的行为，此函数可能很有用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[！UICONTROL延迟]</p> </td> 
   <td> <p>输入方案将暂停的秒数。</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!TIP]
>
>如果要暂停流量更长的时间段，我们建议您将方案拆分为两个方案：
>
>* 第一个方案将包含暂停前的部分。
>* 第二种方案将包含其后的部分。
>
>第一种情形最终会将所有必需的信息与当前时间戳一起存储在一个数据存储中。 第二种方案将定期检查数据存储中是否存在时间戳早于预期延迟的记录，检索记录，完成数据的处理，并从数据存储中删除记录。
>
><!--For more information on data stores, see [Data Stores in [!DNL Adobe Workfront Fusion]]().-->
>
>有关特定数据存储模块的详细信息，请参阅[[!UICONTROL 数据存储]模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md)。

### 汇总

* [[!UICONTROL 数值汇总]](#numeric-aggregator)
* [[!UICONTROL 表汇总]](#table-aggregator)
* [[!UICONTROL 文本汇总]](#text-aggregator)

#### [!UICONTROL 数值汇总]

利用此模块，可检索数值，然后应用其中一个选定的函数(SUM、AVG、COUNT、MAX、MIN)，并将结果返回一个捆绑包中。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[！UICONTROL Source module]</p> </td> 
   <td> <p>选择要从中聚合字段的模块。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL聚合函数]</p> </td> 
   <td> <p>选择要用于聚合值的函数。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL分组依据]</p> </td> 
   <td> <p>定义要按其分组聚合输出的表达式。 此表达式可以包含一个或多个映射项。 然后，使用此表达式的值将聚合的数据分成不同的组。 每个组输出为一个单独的捆绑，其中包含一个键（经过计算的表达式）和一个值（聚合值）。 在后续模块中，您可以将该键用作过滤器。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL在出现空聚合后停止处理]</td> 
   <td>启用此选项可在没有结果时停止方案。</td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL值]</p> </td> 
   <td> <p>输入或映射要聚合的值。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 表汇总]

此模块使用指定的列分隔符和行分隔符（允许您创建表）将接收捆绑的选定字段中的值合并到单个捆绑中。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[！UICONTROL Source module]</p> </td> 
   <td> <p>选择要从中聚合字段的模块。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL聚合字段]</td> 
   <td> <p> 从上面选择的模块中选择包含要聚合到一个捆绑包中的值的字段。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL列分隔符]</p> </td> 
   <td> <p>选择或输入分隔符类型，该分隔符将分隔结果捆绑中的字段值列。 如果选择[！UICONTROL其他]，请在分隔符字段中输入要将值分隔的字符。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL行分隔符]</p> </td> 
   <td> <p>选择或输入分隔符类型，该分隔符将分隔结果捆绑中的字段值行。 如果选择[！UICONTROL其他]，请在分隔符字段中输入要将值分隔的字符。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL分组依据]</p> </td> 
   <td> <p>定义要按其分组聚合输出的表达式。 此表达式可以包含一个或多个映射项。 随后，将使用此表达式的值将聚合的数据分成不同的组。 每个组输出为一个单独的捆绑，其中包含一个键（经过计算的表达式）和一个值（聚合值）。 在后续模块中，您可以将该键用作过滤器。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL在出现空聚合后停止处理]</td> 
   <td>选择此选项可在没有结果时停止方案。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 文本汇总]

此模块将来自所接收捆绑的选定字段的值合并到单个捆绑中。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[！UICONTROL Source module]</p> </td> 
   <td> <p>选择要从中聚合字段的模块。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL行分隔符]</p> </td> 
   <td> <p>选择或输入分隔符类型，该分隔符将分隔结果捆绑中的字段值行。 如果选择[！UICONTROL其他]，请在分隔符字段中输入要将值分隔的字符。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL分组依据]</p> </td> 
   <td> <p>定义包含一个或多个映射项的表达式。 聚合的数据用同一表达式的值在“组”下分隔。 每个组输出为一个单独的包，其中包含带有已计算表达式的键和聚合文本。 这样，您就可以在后续模块中将键用作过滤器。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL在出现空聚合后停止处理]</td> 
   <td>选择此选项可在没有结果时停止方案。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Text]</td> 
   <td> <p> 输入或映射您希望模块聚合的文本。</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**&#x200B;您可以使用文本聚合器将更多值（例如，客户名称或注释）插入到单个包中，并发送一封包含电子邮件正文或电子邮件主题中所有值的电子邮件。

>[!ENDSHADEBOX]

### 变压器

* [[!UICONTROL 撰写字符串]](#compose-a-string)
* [[!UICONTROL 转换文本的编码]](#convert-the-encoding-of-the-text)
* [[!UICONTROL 开关]](#switch)

#### [!UICONTROL 撰写字符串]

将任意值转换为字符串数据类型（文本）。 这样可简化映射（例如，映射二进制数据）的操作。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Text]</td> 
   <td> <p>输入或映射要转换为文本的数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 转换文本的编码]

将输入的输入文本（或二进制数据）转换为所选的编码。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[！UICONTROL输入数据]</p> </td> 
   <td> <p>输入或映射要转换的内容。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL输入数据代码页]</td> 
   <td> <p>选择输入数据的编码类型。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL输出数据代码页]</p> </td> 
   <td> <p>选择目标（输出）数据的编码类型。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 开关]

检查输入值是否与提供的值列表匹配。 根据结果返回输出。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[！UICONTROL输入]</p> </td> 
   <td> <p>输入要计算的表达式。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL使用正则表达式进行匹配]</td> 
   <td> <p>启用此选项可使用正则表达式。 模块根据正则表达式而不是精确匹配来确定案例。</p> 
    <div> 
     <p>正则表达式是一系列字符，其中每个字符要么是具有特殊意义的元字符，要么是具有字面含义的常规字符。 这些字符和元字符标识了可用于搜索文本的模式。 例如，如果要搜索名称，可设置正则表达式以搜索由两个以大写字母开头的连续单词组成的模式。 正则表达式是用于搜索和处理文本的强大工具。</p> 
     <p>有关正则表达式的讨论超出了本文的讨论范围。 我们建议使用以下资源：</p> 
     <ul> 
      <li>有关元字符的完整列表，请参阅MDN Web文档中的<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions">正则表达式</a>。</li> 
      <li>有关如何创建正则表达式的教程，我们建议<a href="https://regexone.com/">RegexOne</a>。</li> 
      <li>若要试验正则表达式，我们建议使用<a href="https://regex101.com/">正则表达式101</a>网站。 在左侧面板中选择ECMAScript (JavaScript) FLAVOR。</li> 
     </ul> 
    </div> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL用例] </td> 
   <td> 对于要添加的每个案例，单击<b>添加项目</b>并输入项目的模式和输出。 <p>如果输入包含输入到[！UICONTROL模式]字段的值，则会返回输入到[！UICONTROL输出]字段的值。</p> <p>如果输入与您在[！UICONTROL模式]字段中设置的任何值都不匹配，则会出现以下情况之一：</p> 
    <ul> 
     <li>返回[！UICONTROL Else]字段中的值</li> 
     <li>如果[！UICONTROL Else]字段中没有值，则不会返回任何输出。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL Else]</p> </td> 
   <td> <p>输入当不符合案例字段中设置的标准时返回的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>
