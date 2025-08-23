---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 将触发器模块添加到基本场景
description: 了解如何添加触发器模块，以允许方案定期查找新请求并将它们转化为项目。
author: Becky
feature: Workfront Fusion
exl-id: cd8ac958-b7a6-4536-89d8-c79a2f8940a6
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 1%

---

# 将触发器模块添加到基本场景

触发器模块位于方案的开头。 当给定服务发生更改时，这些模块将开始场景执行。 更改可以是创建新记录、删除记录、更新记录等。 您可以为开始场景的更改指定条件。

轮询模块在设定的时间间隔检查服务，并返回有关在该时间间隔内发生更改的信息。 如果没有任何更改，则触发器不会执行场景。

在此示例中，您将添加一个每15分钟运行一次的触发器模块，如果有任何请求已提交到特定队列，则会启动一个方案。 然后，场景将这些请求转换为项目。

此示例修改在[创建基本方案](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)中创建的方案。

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
   <td> <p>新增：标准</p><p>或</p><p>当前： [！UICONTROL Work]或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新：</p> <ul><li>[！UICONTROL Select]或[！UICONTROL Prime] Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li><li>[！UICONTROL Ultimate] Workfront计划：包括Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

在执行此过程之前，您必须先创建[创建基本方案](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)中所述的方案。

## 添加并配置触发器模块

### 添加触发器模块

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

### 计划触发器模块

1. 单击Watch Records模块的时钟。

   将打开“计划”设置窗口。

1. 在“运行方案”字段中，选择&#x200B;**定期**。

1. 单击&#x200B;**确定**。

### 更新第二个模块

由于第一个模块已被替换，因此第二个模块必须映射到新的第一个模块。

1. 打开转换对象模块。
1. 在问题ID字段中，删除黑色ID块。 该块为黑色，因为映射该块的模块不再可用。
1. 选择第一个模块（观察记录）下的ID块，以将其映射到第二个模块。
1. 单击&#x200B;**确定**。

### 测试和激活

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
