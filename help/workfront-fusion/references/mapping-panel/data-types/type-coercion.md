---
title: 强制键入
description: 本文档介绍Adobe Workfront Fusion在收到预期和意外数据格式的值时的行为方式。
author: Becky
feature: Workfront Fusion
exl-id: a8bdd36d-c01f-4019-a3ea-fb185101500e
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 5%

---

# 强制键入

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">Adobe Workfront计划*</td> 
   <td> <p>[!DNL Pro] 或更高</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证*</td> 
   <td> <p>[!UICONTROL 计划]，[!UICONTROL 工作]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion]许可证**</td> 
   <td>
   <p>当前许可证要求：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] Adobe Workfront计划，则贵组织必须购买Adobe Workfront Fusion以及Adobe Workfront，才能使用本文中所述的功能。 Workfront Fusion包含在[!UICONTROL Ultimate] Workfront计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买Adobe Workfront Fusion和Adobe Workfront，才能使用本文中所述的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有的计划、许可证类型或访问权限，请联系您的Workfront管理员。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

### 强制键入

本文档介绍Adobe Workfront Fusion在收到预期和意外数据格式的值时的行为方式。

<table style="table-layout:auto">
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>预期</th> 
   <th>已收到</th> 
   <th> <p>描述</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>数组 </td> 
   <td>数组 </td> 
   <td> <p>此值将保持不变。</p> </td> 
  </tr> 
  <tr> 
   <td>数组 </td> 
   <td>其他 </td> 
   <td> <p>如果收到的值不是数组类型，则Workfront Fusion将创建一个数组，第一个（也是唯一的）元素将是收到的值。</p> </td> 
  </tr> 
  <tr> 
   <td>布尔 </td> 
   <td>布尔 </td> 
   <td> <p>此值将保持不变。</p> </td> 
  </tr> 
  <tr> 
   <td>布尔 </td> 
   <td>数字 </td> 
   <td> <p>即使值为0，该值也会转换为逻辑“是”。</p> </td> 
  </tr> 
  <tr> 
   <td>布尔 </td> 
   <td>文本 </td> 
   <td> <p>如果该值等于false或为空，则会将其转换为逻辑否。 否则，它将转换为逻辑“是”。</p> </td> 
  </tr> 
  <tr> 
   <td>布尔 </td> 
   <td>其他 </td> 
   <td> <p>只要收到的值存在（不为null），该值就会转换为逻辑“是”。</p> </td> 
  </tr> 
  <tr> 
   <td>缓冲 </td> 
   <td>缓冲 </td> 
   <td> <p>只有在代码页符合预期时，才会传递未更改的值。 如果代码页不同，Workfront Fusion将尝试将收到的值转换为请求的代码页。 如果不支持此转换，Workfront Fusion将返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>缓冲 </td> 
   <td>布尔 </td> 
   <td> <p>按照上述步骤将值转换为文本(true/false)，然后转换为二进制数据，以转换为文本。</p> </td> 
  </tr> 
  <tr> 
   <td>缓冲 </td> 
   <td>日期 </td> 
   <td> <p>值将转换为ISO 8601文本，然后按照上述转换为文本的步骤转换为二进制数据。</p> </td> 
  </tr> 
  <tr> 
   <td>缓冲 </td> 
   <td>数字 </td> 
   <td> <p>按照上述步骤将值转换为文本，然后转换为二进制数据，以转换为文本。</p> </td> 
  </tr> 
  <tr> 
   <td>缓冲 </td> 
   <td>文本 </td> 
   <td> <p>该值将转换为二进制数据，并按预期进行编码。 如果未指定预期的编码，将使用utf8编码。</p> </td> 
  </tr> 
  <tr> 
   <td>缓冲 </td> 
   <td>其他 </td> 
   <td> <p>Workfront Fusion返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>收藏集 </td> 
   <td>收藏集 </td> 
   <td> <p>此值将保持不变。</p> </td> 
  </tr> 
  <tr> 
   <td>收藏集 </td> 
   <td>其他 </td> 
   <td> <p>Workfront Fusion返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>日期 </td> 
   <td>日期 </td> 
   <td> <p>此值将保持不变。</p> </td> 
  </tr> 
  <tr> 
   <td>日期 </td> 
   <td>文本 </td> 
   <td> <p>Workfront Fusion将尝试将文本转换为日期。 如果转换失败，将返回验证错误。 日期必须包含日、月和年。 日期可能包含时间和时区。 默认时区基于您的设置。 示例：</p> <p><code>2016-06-20T17:26:44.356Z</code> </p> <p><code>2016-06-20 19:26:44 GMT+02:00</code> </p> <p><code>2016-06-20 19:26+0200</code> </p> <p><code>2016-06-20 17:26:44</code> </p> <p><code>2016-06-20</code> </p> <p><code>2016/06/20 17:26:44</code> </p> <p><code>2016/06/20 19:26:44+02:00</code> </p> <p><code>2016/06/20 17:26</code> </p> <p><code>2016/06/20 5:26 PM</code> </p> <p><code>2016/06/20</code> </p> <p><code>06/20/2016 17:26:44</code> </p> <p><code>06/20/2016 19:26:44+02:00</code> </p> <p><code>06/20/2016 17:26</code> </p> <p><code>06/20/2016 5:26 PM</code> </p> <p><code>06/20/2016</code> </p> <p><code>20.6.2016 17:26:44</code> </p> <p><code>20.6.2016 19:26:44+02:00</code> </p> <p><code>20.6.2016 17:26</code> </p> <p><code>20.6.2016</code> </p> </td> 
  </tr> 
  <tr> 
   <td>日期 </td> 
   <td>其他 </td> 
   <td> <p>Workfront Fusion返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>数字 </td> 
   <td>数字 </td> 
   <td> <p>此值将保持不变。</p> </td> 
  </tr> 
  <tr> 
   <td>数字 </td> 
   <td>文本 </td> 
   <td> <p>Workfront Fusion将尝试将文本转换为数字。 如果转换失败，将返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>数字 </td> 
   <td>其他 </td> 
   <td> <p>Workfront Fusion返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>文本 </td> 
   <td>文本 </td> 
   <td> <p>此值将保持不变。</p> </td> 
  </tr> 
  <tr> 
   <td>文本 </td> 
   <td>数组 </td> 
   <td> <p>如果给定的数组支持转换为文本，则将转换值。 否则，Workfront Fusion将返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>文本 </td> 
   <td>布尔 </td> 
   <td> <p>该值将转换为文本(true/false)。</p> </td> 
  </tr> 
  <tr> 
   <td>文本 </td> 
   <td>缓冲 </td> 
   <td> <p>如果为二进制数据指定了文本编码，该值将转换为文本。 否则，Workfront Fusion将返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>文本 </td> 
   <td>日期 </td> 
   <td> <p>值将转换为ISO 8601文本。</p> </td> 
  </tr> 
  <tr> 
   <td>文本 </td> 
   <td>数字 </td> 
   <td> <p>该值将转换为文本。</p> </td> 
  </tr> 
  <tr> 
   <td>文本 </td> 
   <td>其他 </td> 
   <td> <p>Workfront Fusion返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>时间 </td> 
   <td>时间 </td> 
   <td> <p>此值将保持不变。</p> </td> 
  </tr> 
  <tr> 
   <td>时间 </td> 
   <td>文本 </td> 
   <td> <p>Workfront Fusion将尝试将时间转换为<code>hours:minutes:seconds</code>格式。 如果转换失败，将返回验证错误。</p> </td> 
  </tr> 
  <tr> 
   <td>时间 </td> 
   <td>其他 </td> 
   <td> <p>Workfront Fusion返回验证错误。</p> </td> 
  </tr> 
 </tbody> 
</table>
