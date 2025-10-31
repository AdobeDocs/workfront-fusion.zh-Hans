---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 将筛选器添加到基本方案
description: 通过过滤器，您可以确保场景仅在满足某些条件时推进。
author: Becky
feature: Workfront Fusion
exl-id: 78ab27fe-e2dd-4b52-b986-77b4b7ea3b5e
source-git-commit: 3a977d805c10fda7209b0634c6e32e818a980691
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 1%

---

# 将筛选器添加到基本方案

通过过滤器，您可以确保场景仅在满足某些条件时推进。

在此示例中，您将向场景添加一个过滤器，该过滤器允许仅当请求已提交到特定请求队列时，才从请求创建新项目。

此示例修改在[创建基本方案](/help/workfront-fusion/build-practice-scenarios/create-basic-scenario.md)中创建的方案。

>[!NOTE]
>
>Workfront触发器模块包括过滤器，这些过滤器允许仅在满足某些条件时才启动方案。 但是，由于模块间过滤器用于每个非触发器和非Workfront用例，因此了解如何在模块之间使用过滤器非常重要。 此示例将模块间过滤器用于可能与模块内过滤器相符的功能。

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

## 添加筛选器

### 准备添加过滤器

1. 打开方案。
1. 单击第一个模块以将其打开。
1. 在&#x200B;**输出**&#x200B;区域，选择`Project`。
您现在应该已选择`ID`、`Name`和`Project`。
1. 单击确定以保存模块设置。
1. 打开Workfront。
1. 在Workfront中，找到表示Fusion场景将使用的请求队列的项目。

   此项目必须位于为Fusion连接设置的Workfront帐户中。

1. 在URL中记下项目ID。

   示例： https://\&lt;MyDomain\>.my.workfront.com/project/\&lt;ProjectID\>/tasks

### 添加并配置过滤器

1. 返回到方案编辑器中的方案。
1. 单击第一和第二模块之间的扳手图标![扳手图标](assets/wrench-icon.png)，然后选择&#x200B;**设置过滤器**。
1. 在标签字段中，输入此过滤器的标签，如“过滤请求队列”。
1. 在&#x200B;**Condition**&#x200B;区域的顶部字段中，映射第一个模块中的`projectID`。

   ![映射项目ID](assets/map-proj-id.png)
1. 将&#x200B;**Condition**&#x200B;运算符保留为Equal to。
1. 在&#x200B;**条件**&#x200B;区域的底部字段中，粘贴您从[准备添加筛选器](#prepare-to-add-the-filter)的项目URL中记录的项目ID。
1. 单击&#x200B;**确定**&#x200B;以保存筛选器设置。

### 测试和激活

1. 转到Fusion所连接到的Workfront环境，并将问题添加到您在筛选器中指定的项目。 将另一个问题添加到其他项目。
1. 在方案编辑器的左下角单击&#x200B;**[!UICONTROL 运行一次]**。
1. 检查输出以确保方案按预期运行。

   这两个问题都应该显示在第一个模块的输出中，但只有指定项目中的问题应该显示为第二个模块的输入。
1. 如果您满意方案按预期工作，请单击屏幕左下角的&#x200B;**计划**&#x200B;切换开关至&#x200B;**开启**。

   这将激活方案。
1. 在Workfront Fusion中，单击左下角附近的&#x200B;**[!UICONTROL 保存]**&#x200B;以保存场景进度。

   >[!IMPORTANT]
   >
   >在磨练和测试场景时经常保存。

## 资源

* 有关筛选器的详细信息，请参阅[将筛选器添加到方案](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md)。
