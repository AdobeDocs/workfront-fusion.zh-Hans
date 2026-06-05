---
title: 重新触发特定场景执行
description: 您可以重新触发特定场景执行，以使用更新的场景Blueprint处理数据，或查看其数据流。
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 0c732add9c1ec75d7aed43bb7097bb1c95aa6408
workflow-type: tm+mt
source-wordcount: 523
ht-degree: 18%

---

# 重新触发特定场景执行

您可以重新触发特定场景执行，以使用更新的场景Blueprint处理数据，或查看其数据流。 当您重新触发执行时，场景将使用该执行的数据运行。

例如，如果您更新方案以添加操作（如创建问题），则可以重新触发在更新之前发生的执行。 更新的方案将使用原始方案的触发事件运行，但将包含更新的操作。 在此示例中，场景会在新执行期间创建一个问题。

重新触发适用于具有webhook触发器的方案和子方案。

在重新触发使用webhook的场景时，可以再次使用原始webhook事件，因此无需重新创建事件来重新触发场景。

使用链接方案时，也可以将重新触发应用于子方案。 子方案可使用从原始执行中的父方案发送的数据进行重触发，而无需重新触发父方案。

有关 Webhook 的更多信息，请参阅[即时触发器（Webhooks）](/help/workfront-fusion/references/modules/webhooks-reference.md)。

有关链接方案的详细信息，请参阅[链接多个方案](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)。

## 访问权限要求

+++ 展开可查看本文所述功能的访问权限要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 包</td> 
   <td> <p>任意 Adobe Workfront Workflow 包以及任意 Adobe Workfront 自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime 和 Select 包，且需额外购买 Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 许可证</td> 
   <td> <p>标准</p><p>工作版或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 重新触发执行

您可以从方案的图表、方案的历史记录区域或特定方案执行的页面重新触发方案执行。

### 从方案图重新触发执行

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择运行要重新触发的执行的方案。

   此时将打开方案的图表。
1. 在页面右侧的执行列表中找到要重新触发的执行。
1. 对该方案单击&#x200B;**重新触发程序**。

从关系图![重新触发程序](assets/retrigger-from-diagram.png)

### 从方案历史记录中重新触发执行

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择运行要重新触发的执行的方案。

   此时将打开方案的图表。

1. 单击方案名称正下方的&#x200B;**历史记录**&#x200B;选项卡。
1. 找到要重新触发的执行。 如有必要，您可以使用全文搜索来查找它。
1. 对该方案单击&#x200B;**重新触发程序**。

![从历史记录中重新触发程序](assets/retrigger-from-history.png)

### 从场景执行页面重新触发场景

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择运行要重新触发的执行的方案。

   此时将打开方案的图表。
1. 在页面右侧的执行列表中找到要重新触发的执行。
1. 单击执行以将其打开。
1. 在执行页面上，单击&#x200B;**重新触发程序**。


![执行中的重新触发程序](assets/retrigger-from-execution.png)






