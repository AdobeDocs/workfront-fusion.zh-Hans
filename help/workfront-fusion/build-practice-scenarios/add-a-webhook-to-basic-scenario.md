---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 将webhook添加到基本场景
description: Webhook（也称为即时触发器）是一种特定的触发器模块，它可以在每次进行更改时启动一个场景，而不是按给定的计划启动。
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 1%

---

# 将webhook添加到基本场景

Webhook（也称为即时触发器）是一种特定的触发器模块，它可以在每次进行更改时启动一个场景，而不是按给定的计划启动。

在本例中，您将添加一个webhook ，以便在将任何请求提交到特定请求队列后立即启动方案。 然后，场景将这些请求转换为项目。

此示例修改在[创建基本方案](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)中创建的方案。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证</td> 
   <td> <p>新增： [!UICONTROL Standard]</p><p>或</p><p>当前： [!UICONTROL Work]或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>[!UICONTROL Select] 或[!UICONTROL Prime] [!DNL Workfront]计划：您的组织必须购买[!DNL Adobe Workfront Fusion]。</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 计划： [!DNL Workfront Fusion]已包括在内。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买[!DNL Adobe Workfront Fusion]。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

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

1. 单击方案编辑器左下角的&#x200B;**[!UICONTROL Run once]**。

   必须运行场景才能观察新请求。
1. 转到Fusion所连接的Workfront环境并添加问题。

   场景应该会运行。
1. 检查输出以确保方案按预期运行。
1. 如果您满意方案按预期工作，请单击屏幕左下角的&#x200B;**计划**&#x200B;切换开关至&#x200B;**开启**。

   这将激活方案。
1. 在[!DNL Workfront Fusion]中，单击左下角附近的&#x200B;**[!UICONTROL Save]**&#x200B;以保存方案进度。
