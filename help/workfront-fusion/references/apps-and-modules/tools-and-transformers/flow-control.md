---
title: 流量控制
description: 创建或编辑场景时，您可以配置设置以控制数据流经场景的方式。
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: ce2f13866fef97b5687991dfcf5d9579a5e539e4
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# 流量控制

创建或编辑场景时，您可以配置设置以控制数据流经场景的方式。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
  <td> <p>[!UICONTROL Pro] 或更高</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
   <td> <p>[!UICONTROL Plan]， [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前许可证要求：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成]，[!UICONTROL [!DNL Workfront Fusion]用于工作自动化]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Adobe Workfront]计划，则您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[!UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## 中继器

您可以使用[!UICONTROL Repeater]模块重复指定次数的任务。 [!UICONTROL Repeater]模块逐个生成包。

例如，您可以通过将&#x200B;**[!UICONTROL Email]>[!UICONTROL Send me an email]**&#x200B;模块连接到[!UICONTROL Repeater]模块，使用[!UICONTROL Repeater]模块发送主题为“Hello 1”、“Hello 2”等的五封电子邮件。

要使用[!UICONTROL Repeater]模块：

1. 单击屏幕底部的[!UICONTROL Flow Control]图标![](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif)，然后在显示的菜单中单击&#x200B;**[!UICONTROL Repeater]**。
1. 单击[!UICONTROL Repeater]捆绑包，然后在显示的框中单击&#x200B;**[!UICONTROL Connect automatically]**。
1. 在出现的[!UICONTROL Flow Control]框中，键入要在&#x200B;**[!UICONTROL Repeats]**&#x200B;框中输入的重复（输出包）数。

   在我们的电子邮件示例中，您将键入5。

   ![](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   每次重复时，该项的值将按在&#x200B;**[!UICONTROL Step]**&#x200B;字段中指定的值增加，您可以通过选择&#x200B;**[!UICONTROL Show advanced settings]**&#x200B;来查看该字段。 默认情况下，此数字为1。

1. 单击&#x200B;**[!UICONTROL OK]**&#x200B;以关闭&#x200B;**[!UICONTROL Flow Control]**&#x200B;框。

1. 单击连接到[!UICONTROL Repeater]模块的应用或服务模块。
1. 在出现的框中，键入要重复的信息。

   在我们的电子邮件示例中，您需要在[!UICONTROL Subject]框中键入Hello，然后从中继器模块映射`i`。

   ![](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)

| 项 | 描述 |
|---|---|
| [!UICONTROL Initial value] | 输入或映射您希望模块在第一个迭代中设置为`i`的数字。 默认值为1。 |
| [!UICONTROL Repeats] | 输入或映射您希望模块重复执行的次数。 此数字必须大于或等于0，并且小于或等于10,000。 |
| [!UICONTROL Step] | 这是模块增加`i`值所依据的数字。 默认值为1。 |

{style="table-layout:auto"}

>[!NOTE]
>
>重复次数不是由`i`的值确定的，因为它在编程中处于循环中。 模块将重复[!UICONTROL Repeats]字段中指示的次数。 值`i`随[!DNL repeater]模块的每个迭代而更改，可以映射到以后的模块。 上面的示例将`i`的值映射到Hello消息中，从而生成显示“Hello 1”、“Hello 2”等的消息。

## [!UICONTROL Iterator]

[!UICONTROL Iterator]是一种特殊类型的模块，可将数组转换为一系列捆绑包。 在[!UICONTROL Iterator]模块输出中，每个数组项都将是一个单独的捆绑包。 有关详细信息，请参阅[迭代器模块](/help/workfront-fusion/references/modules/iterator-module.md)。

## 数组汇总

数组聚合器是一种特殊类型的模块，允许将多个捆绑合并为一个捆绑包。 有关详细信息，请参阅[聚合器模块](/help/workfront-fusion/references/modules/aggregator-module.md)。

## [!UICONTROL Router]

[!UICONTROL Router]模块允许您将流量分支为多条路由，并以不同的方式处理每条路由中的数据。 [!UICONTROL Router]模块收到捆绑包后，会按照路由附加到[!UICONTROL Router]模块的顺序将其转发到每个连接的路由。 有关详细信息，请参阅 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)中的[路由器模块。

<!--
<div>
<h2>Directives</h2>
<p>The error handling directives allow you to control how your scenario reacts to errors. For more information, see <a href="/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md" class="MCXref xref">Advanced error handling in Adobe Workfront Fusion</a> and <a href="/help/workfront-fusion/references/errors/directives-for-error-handling.md" class="MCXref xref">Directives for error handling in Adobe Workfront Fusion</a>.</p>
</div>
-->
