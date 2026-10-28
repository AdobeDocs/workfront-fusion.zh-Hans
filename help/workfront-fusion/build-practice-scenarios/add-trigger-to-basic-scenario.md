---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 向基础场景添加触发器模块
description: 了解如何添加触发器模块，以允许方案定期查找新请求并将它们转化为项目。
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
TQID: https://experienceleague.adobe.com/xepLecibr9U6FpQM0neDy15DbFGF55rR6gVYvo644H4
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
source-git-commit: 347280547bea92c0ee498da519495569a3cac661
workflow-type: tm+mt
source-wordcount: '1022'
ht-degree: 11%
---
# 向基础场景添加触发器模块

触发器模块位于方案的开头。 当给定服务发生更改时，这些模块将开始场景执行。 更改可以是创建新记录、删除记录、更新记录等。 您可以为开始场景的更改指定条件。

轮询模块在设定的时间间隔检查服务，并返回有关在该时间间隔内发生更改的信息。 如果没有任何更改，则触发器不会执行场景。

在此示例中，您将添加一个每15分钟运行一次的触发器模块，如果有任何请求已提交到特定队列，则会启动一个方案。 然后，场景将这些请求转换为项目。

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

## 在新版Experience中添加和配置触发器模块（推荐）

* [添加触发器模块](#add-the-trigger-module)
* [计划触发器模块](#schedule-the-trigger-module)
* [更新第二个模块](#update-the-second-module)
* [测试和激活](#test-and-activate)

### 添加触发器模块

1. 在方案编辑器中打开方案。
1. 右键单击第一个（搜索）模块并选择&#x200B;**[!UICONTROL 删除模块]**。

   模块被删除，留空占位符。

1. 单击空白模块以打开应用程序和服务列表。

   ![应用和服务选取器](/help/workfront-fusion/build-practice-scenarios/assets/new-connector-picker.png)

1. 选择&#x200B;**Adobe Workfront**。
1. 选择&#x200B;**监视记录**。
1. 确保模块使用与场景中其余模块相同的连接。
1. 在记录类型字段中，选择&#x200B;**问题**。
1. 在筛选器字段中，选择&#x200B;**仅新记录**。
1. 在输出框中，选择`ID`、`Name`和`Project ID`。
1. 单击&#x200B;**确定**&#x200B;以保存模块设置。

   出现“Choose where to start（选择开始位置）”窗口。

1. 从&#x200B;**开始选择**。

### 计划触发器模块

1. 单击Watch Record模块上的时钟图标。

   监视记录模块上的![时钟图标](assets/clock-icon-on-watch-record.png)

   将打开“计划”设置窗口。

1. 在“运行方案”字段中，选择&#x200B;**定期**。

1. 单击&#x200B;**确定**。

### 更新第二个模块

由于第一个模块已被替换，因此第二个模块必须映射到新的第一个模块。

1. 打开转换对象模块。
1. 在问题ID字段中，删除黑色ID块。 该块为黑色，因为映射该块的模块不再可用。
1. 选择第一个模块（观看记录）下的ID块，以将其映射到第二个模块。
1. 单击&#x200B;**确定**。

### 测试和激活

1. 转到Fusion所连接的Workfront环境并添加问题。
1. 单击&#x200B;**[!UICONTROL 运行一次]**&#x200B;图标。

   运行一次在新版Experience中是仅用于图标的。 将鼠标悬停在该图标上可查看&#x200B;**[!UICONTROL 运行一次]**&#x200B;工具提示。

   ![运行方案按钮](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png)

1. 检查输出以确保方案按预期运行。
1. 如果您对方案按预期工作感到满意，请单击&#x200B;**计划**&#x200B;切换到&#x200B;**开启**。

   这将激活方案。

   ![计划切换](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/scheduling-new.png)

1. 单击“控件”区域中的&#x200B;**保存**&#x200B;图标![保存图标](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/save-icon-new.png)以保存方案进度。

   >[!IMPORTANT]
   >
   >在磨练和测试场景时经常保存。

## 在经典Experience中添加和配置触发器模块

* [添加触发器模块(Classic)](#add-the-trigger-module-classic)
* [计划触发器模块(Classic)](#schedule-the-trigger-module-classic)
* [更新第二个模块(Classic)](#update-the-second-module-classic)
* [测试和激活(Classic)](#test-and-activate-classic)

### 添加触发器模块(Classic)

1. 在方案编辑器中打开方案。
1. 右键单击第一个（搜索）模块并选择&#x200B;**删除模块**。

   模块被删除，留空占位符。

1. 单击空白模块，然后从应用程序列表中选择&#x200B;**Adobe Workfront**。
1. 选择&#x200B;**监视记录**。
1. 确保模块使用与场景中其余模块相同的连接。
1. 在记录类型字段中，选择&#x200B;**问题**。
1. 在筛选器字段中，选择&#x200B;**仅新记录**。
1. 在输出框中，选择`ID`、`Name`和`Project ID`。
1. 单击&#x200B;**确定**&#x200B;以保存模块设置。

   出现“Choose where to start（选择开始位置）”窗口。

1. 从&#x200B;**开始选择**。

### 计划触发器模块(Classic)

1. 单击Watch Record模块上的时钟。

   将打开“计划”设置窗口。

1. 在“运行方案”字段中，选择&#x200B;**定期**。

1. 单击&#x200B;**确定**。

### 更新第二个模块(Classic)

由于第一个模块已被替换，因此第二个模块必须映射到新的第一个模块。

1. 打开转换对象模块。
1. 在问题ID字段中，删除黑色ID块。 该块为黑色，因为映射该块的模块不再可用。
1. 选择第一个模块（观看记录）下的ID块，以将其映射到第二个模块。
1. 单击&#x200B;**确定**。

### 测试和激活(Classic)

1. 转到Fusion所连接的Workfront环境并添加问题。
1. 在方案编辑器的左下角单击&#x200B;**[!UICONTROL 运行一次]**。
1. 检查输出以确保方案按预期运行。
1. 如果您满意方案按预期工作，请单击屏幕左下角的&#x200B;**计划**&#x200B;切换开关至&#x200B;**开启**。

   这将激活方案。
1. 在Workfront Fusion中，单击左下角附近的&#x200B;**[!UICONTROL 保存]**&#x200B;以保存场景进度。

   >[!IMPORTANT]
   >
   >在磨练和测试场景时经常保存。

## 资源

* 有关触发器模块的详细信息，请参阅文章模块概述中的[触发器模块](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules)。
