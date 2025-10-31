---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 将webhook添加到基本场景
description: Webhook（也称为即时触发器）是一种特定的触发器模块，它可以在每次进行更改时启动一个场景，而不是按给定的计划启动。
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
source-git-commit: 3a977d805c10fda7209b0634c6e32e818a980691
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# 将webhook添加到基本场景

Webhook（也称为即时触发器）是一种特定的触发器模块，它可以在每次进行更改时启动一个场景，而不是按给定的计划启动。

在本例中，您将添加一个webhook ，以便在将任何请求提交到特定请求队列后立即启动方案。 然后，场景将这些请求转换为项目。

此示例修改在[创建基本方案](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)中创建的方案。

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

## 先决条件

在执行此过程之前，您必须先创建[创建基本方案](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)中所述的方案。

## 添加和配置webhook


### 添加webhook模块

1. 在方案编辑器中打开方案。
1. 右键单击第一个模块，然后选择&#x200B;**删除模块**。

   模块被删除，留空占位符。

1. 单击空白模块，然后从应用程序列表中选择&#x200B;**Adobe Workfront**。
1. 选择&#x200B;**观看活动**。
1. 单击Webhook字段旁边的&#x200B;**添加**。
1. 在“记录类型”字段中，选择&#x200B;**问题**，以便模块会触发问题的更改。
1. 在“状态”字段中，选择&#x200B;**新建状态**。 这是用于筛选器的必填字段，本示例未涵盖该字段。
1. 在“记录来源”字段中，选择&#x200B;**仅新建记录**。 这允许场景在添加问题时触发，而不是在更新或删除问题时触发。
1. 单击&#x200B;**保存**&#x200B;以保存模块配置。

## 更新第二个模块

1. 打开方案。
1. 单击&#x200B;**转换对象**&#x200B;模块以将其打开。
1. 在问题ID字段中，删除黑色ID块。 该块为黑色，因为映射该块的模块不再可用。
1. 选择第一个模块(Watch Events)下的ID块以将其映射到第二个模块。
1. 单击&#x200B;**确定**。



### 测试和激活

1. 在方案编辑器的左下角单击&#x200B;**[!UICONTROL 运行一次]**。

   必须运行场景才能观察新请求。
1. 转到Fusion所连接的Workfront环境并添加问题。

   场景应该会运行。
1. 检查输出以确保方案按预期运行。
1. 如果您满意方案按预期工作，请单击屏幕左下角的&#x200B;**计划**&#x200B;切换开关至&#x200B;**开启**。

   这将激活方案。
1. 在Workfront Fusion中，单击左下角附近的&#x200B;**[!UICONTROL 保存]**&#x200B;以保存场景进度。
