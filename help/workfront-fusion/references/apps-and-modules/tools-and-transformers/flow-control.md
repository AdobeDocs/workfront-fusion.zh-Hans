---
title: 流量控制
description: 创建或编辑场景时，您可以配置设置以控制数据流经场景的方式。
author: Becky
feature: Workfront Fusion
exl-id: b3aed366-c399-44fa-8967-54ecb8647d96
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---

# 流量控制

创建或编辑场景时，您可以配置设置以控制数据流经场景的方式。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何Adobe Workfront Workflow包和任何Adobe Workfront自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime和Select包，以及额外购买的Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>标准</p><p>工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果贵组织具有不包含Workfront Automation and Integration的Select或Prime Workfront包，则贵组织必须购买Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

+++



## 中继器

您可以使用[!UICONTROL 中继器]模块按指定次数重复执行任务。 [!UICONTROL 中继器]模块逐个生成包。


<table>
    <tr>
        <td>[!UICONTROL 初始值]</td>
        <td>输入或映射您希望模块在第一迭代中的值。 默认值为 1。</td>
    </tr>
    <tr>
        <td>[!UICONTROL 重复]</td>
        <td>输入或映射您希望模块重复执行的次数。 此数字必须大于或等于0，并且小于或等于10,000。</td>
    </tr>
    <tr>
        <td>[!UICONTROL 步骤]</td>
        <td>这是模块增加值所依据的数字。 默认值为 1。</td>
    </tr>
</table>

>[!BEGINSHADEBOX]

例如，您可以通过将[!UICONTROL 电子邮件] >**[!UICONTROL 向我发送电子邮件]模块连接到[!UICONTROL 中继器]**&#x200B;模块，使用[!UICONTROL 中继器]模块发送主题为“Hello 1”、“Hello 2”等的五封电子邮件。

1. 单击屏幕底部的[!UICONTROL 流量控制]图标![流量控制图标](/help/workfront-fusion/references/apps-and-modules/assets/flow-control-icon.gif)，然后在显示的菜单中单击&#x200B;**[!UICONTROL 中继器]**。
1. 单击[!UICONTROL 中继器]模块，然后在显示的框中单击&#x200B;**[!UICONTROL 自动连接]**。

   此时会打开中继器模块。

1. 在&#x200B;**[!UICONTROL 重复]**&#x200B;字段中，输入您希望模块产生的重复（输出捆绑）数。

   在本例中，您将输入5。

   ![中继器](/help/workfront-fusion/references/apps-and-modules/assets/repeater-2-350x207.png)

   每次重复时，该项的值将增加在&#x200B;**[!UICONTROL 步骤]**&#x200B;字段中指定的值，您可以通过选择&#x200B;**[!UICONTROL 显示高级设置]**&#x200B;来查看该字段。 默认情况下，此数字为1。

1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;以关闭&#x200B;**[!UICONTROL 流量控制]**&#x200B;框。

1. 单击连接到[!UICONTROL 中继器]模块的应用或服务模块。
1. 在出现的框中，键入要重复的信息。

   在我们的电子邮件示例中，您可以在[!UICONTROL 主题]框中键入Hello，然后从中继器模块映射`i`。

   ![中继器](/help/workfront-fusion/references/apps-and-modules/assets/repeater-3-350x207.png)



>[!NOTE]
>
>重复次数不是由`i`的值确定的，因为它在编程中处于循环中。 模块将重复[!UICONTROL 重复]字段中指示的次数。 值`i`随[!DNL repeater]模块的每个迭代而更改，可以映射到以后的模块。 上面的示例将`i`的值映射到Hello消息中，从而生成显示“Hello 1”、“Hello 2”等的消息。

>[!ENDSHADEBOX]

## [!UICONTROL 迭代器]

[!UICONTROL 迭代器]是一种将数组转换为一系列捆绑的特殊模块类型。 在[!UICONTROL 迭代器]模块输出中，每个数组项都将是一个单独的捆绑包。 有关详细信息，请参阅[迭代器模块](/help/workfront-fusion/references/modules/iterator-module.md)。

## 数组汇总

数组聚合器是一种特殊类型的模块，允许将多个捆绑合并为一个捆绑包。 有关详细信息，请参阅[聚合器模块](/help/workfront-fusion/references/modules/aggregator-module.md)。

## [!UICONTROL 路由器]

[!UICONTROL 路由器]模块允许您将流量分为多条路由，并以不同的方式处理每条路由中的数据。 一旦[!UICONTROL 路由器]模块收到捆绑包，它会按照路由连接到[!UICONTROL 路由器]模块的顺序将其转发到每个连接的路由。 有关详细信息，请参阅Adobe Workfront Fusion中的[路由器模块](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)。

## 指令

利用错误处理指令，可控制场景对错误的反应方式。

有关错误处理指令的信息，请参阅[错误处理指令](/help/workfront-fusion/references/errors/directives-for-error-handling.md)。

