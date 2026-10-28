---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 向基础场景添加 Webhook
description: Webhook（也称为即时触发器）是一种特定的触发器模块，它可以在每次进行更改时启动一个场景，而不是按给定的计划启动。
author: Becky
feature: Workfront Fusion
exl-id: 28ecca1f-a9c3-4b3d-95f5-73cb9a5dc4b9
TQID: https://experienceleague.adobe.com/V3cpVf8NzJdGjSZvPA0Hy0Uui-zSdd986plS1Us0oNI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
source-git-commit: 4cd8b43e9ce9a16aca16397ce140cdd2467bf7d4
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 13%
---
# 向基础场景添加 Webhook

Webhook（也称为即时触发器）是一种特定的触发器模块，它可以在每次进行更改时启动一个场景，而不是按给定的计划启动。

在本例中，您将添加一个webhook ，以便在将任何请求提交到特定请求队列后立即启动方案。 然后，场景将这些请求转换为项目。

此示例修改在[创建基本方案](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)中创建的方案。

>[!NOTE]
>
>Workfront Fusion正在将场景编辑器转换为新Experience。 在此过渡期间，经典体验和新体验均可用，您可以随时在它们之间切换。 我们建议使用新Experience。 有关详细信息，请参阅文章场景编辑器中的[新体验和经典体验](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)。

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

## 先决条件

在执行此过程之前，您必须先创建[创建基本方案](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)中所述的方案。

## 在新版Experience中添加和配置webhook（推荐）

* [添加webhook模块](#add-the-webhook-module)
* [更新第二个模块](#update-the-second-module)
* [测试和激活](#test-and-activate)

### 添加webhook模块

1. 在方案编辑器中打开方案。
1. 右键单击第一个模块并选择&#x200B;**[!UICONTROL 删除模块]**。

   模块被删除，留空占位符。

1. 单击空白模块以打开应用程序和服务列表。

   ![应用和服务选取器](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. 选择&#x200B;**Adobe Workfront**。
1. 选择&#x200B;**观看活动**。
1. 单击 Webhook 字段旁边的&#x200B;**添加**。
1. 在“记录类型”字段中，选择&#x200B;**问题**，以便模块会触发问题的更改。
1. 在“状态”字段中，选择&#x200B;**新建状态**。 这是用于筛选器的必填字段，本示例未涵盖该字段。
1. 在“记录来源”字段中，选择&#x200B;**仅新建记录**。 这允许场景在添加问题时触发，而不是在更新或删除问题时触发。
1. 单击&#x200B;**保存**&#x200B;以保存模块配置。

### 更新第二个模块

1. 打开方案。
1. 单击&#x200B;**转换对象**&#x200B;模块以将其打开。
1. 在问题ID字段中，删除黑色ID块。 该块为黑色，因为映射该块的模块不再可用。
1. 选择第一个模块(Watch Events)下的ID块以将其映射到第二个模块。
1. 单击&#x200B;**确定**。

### 测试和激活

1. 单击&#x200B;**[!UICONTROL 运行一次]**&#x200B;图标。

   运行一次在新版Experience中是仅用于图标的。 将鼠标悬停在该图标上可查看&#x200B;**[!UICONTROL 运行一次]**&#x200B;工具提示。

   ![运行方案按钮](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png)

   必须运行场景才能观察新请求。
1. 转到Fusion所连接的Workfront环境并添加问题。

   场景应该会运行。
1. 检查输出以确保方案按预期运行。
1. 如果您对方案按预期工作感到满意，请单击&#x200B;**计划**&#x200B;切换到&#x200B;**开启**。

   这将激活方案。

   ![计划切换](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/scheduling-new.png)

1. 单击“控件”区域中的&#x200B;**保存**&#x200B;图标![保存图标](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/save-icon-new.png)以保存方案进度。

## 在经典Experience中添加和配置webhook

* [添加webhook模块（经典）](#add-the-webhook-module-classic)
* [更新第二个模块(Classic)](#update-the-second-module-classic)
* [测试和激活(Classic)](#test-and-activate-classic)

### 添加webhook模块（经典）

1. 在方案编辑器中打开方案。
1. 右键单击第一个模块，然后选择&#x200B;**删除模块**。

   模块被删除，留空占位符。

1. 单击空白模块，然后从应用程序列表中选择&#x200B;**Adobe Workfront**。
1. 选择&#x200B;**观看活动**。
1. 单击 Webhook 字段旁边的&#x200B;**添加**。
1. 在“记录类型”字段中，选择&#x200B;**问题**，以便模块会触发问题的更改。
1. 在“状态”字段中，选择&#x200B;**新建状态**。 这是用于筛选器的必填字段，本示例未涵盖该字段。
1. 在“记录来源”字段中，选择&#x200B;**仅新建记录**。 这允许场景在添加问题时触发，而不是在更新或删除问题时触发。
1. 单击&#x200B;**保存**&#x200B;以保存模块配置。

### 更新第二个模块(Classic)

1. 打开方案。
1. 单击&#x200B;**转换对象**&#x200B;模块以将其打开。
1. 在问题ID字段中，删除黑色ID块。 该块为黑色，因为映射该块的模块不再可用。
1. 选择第一个模块(Watch Events)下的ID块以将其映射到第二个模块。
1. 单击&#x200B;**确定**。

### 测试和激活(Classic)

1. 在方案编辑器的左下角单击&#x200B;**[!UICONTROL 运行一次]**。

   必须运行场景才能观察新请求。
1. 转到Fusion所连接的Workfront环境并添加问题。

   场景应该会运行。
1. 检查输出以确保方案按预期运行。
1. 如果您满意方案按预期工作，请单击屏幕左下角的&#x200B;**计划**&#x200B;切换开关至&#x200B;**开启**。

   这将激活方案。
1. 在Workfront Fusion中，单击左下角附近的&#x200B;**[!UICONTROL 保存]**&#x200B;以保存场景进度。
