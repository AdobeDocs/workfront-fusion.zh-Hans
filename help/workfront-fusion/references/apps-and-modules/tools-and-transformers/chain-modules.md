---
title: 链模块
description: 使用这些模块，您可以将场景链接在一起，使一个调用另一个。
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
exl-id: 21429f94-fe4c-4ccc-a8c0-d7573657fecc
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 1%

---

# 链模块

使用“链”模块，可以将一个方案连接到另一个方案。

<!--This article will be about the specific module configuration-->

有关计划链接方案的说明，请参阅[将多个方案链接在一起](/help/workfront-fusion/create-scenarios/plan-a-scenario/chain-scenarios.md)。


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



## 链模块及其字段

### 触发器

#### 从父项接收数据

此模块是子方案中的触发模块，由调用父方案中的子方案模块触发。 它接收来自父方案的数据，可以在子方案中处理这些数据。

配置从父模块接收数据：

1. 要使用现有数据结构，请在数据结构字段中，选择将用于方案输入数据的数据结构。

   或

   若要创建新的数据结构以用作方案的输入数据，请单击“数据结构”字段旁边的&#x200B;**添加**&#x200B;并创建数据结构。

   有关创建数据结构的说明，请参阅[数据结构](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md)。

1. 单击&#x200B;**确定**&#x200B;以保存模块。

### 操作

#### 调用子方案

此模块位于父方案中。 这些字段反映了在子方案中的“从父模块接收数据”中设置的数据结构。

>[!NOTE]
>
>* 您可以选择现有的子方案，也可以通过此模块创建新子方案。
>* 您可以在创建子方案时创建数据结构。

配置“调用子方案”模块

1. 将“调用子方案”模块添加到方案中。
1. 要使用现有的子方案，请在链字段中，选择要调用的子方案。

   或

   要创建新的子方案，请单击“链”字段旁边的“添加”。 子方案会显示在单独的窗口中，其中已放置从父模块接收数据和从父模块返回响应。

   在子方案的触发器模块中配置的字段显示在调用子方案模块中。

1. 在调用子方案模块中输入或映射要传递给子方案的信息。
1. （视情况而定）如果希望父方案继续执行，而不等待子方案的响应，请启用&#x200B;**触发并忘记**&#x200B;选项。
1. 单击&#x200B;**确定**&#x200B;以保存模块。

>[!NOTE]
>
>如果为此模块创建新的子方案，子方案将在单独的浏览器窗口中打开，允许您同时查看和配置父方案和子方案。

#### 将响应返回至父级

这是子方案中的，并将选定结构中的数据发送至父方案。 您可以在父方案的后续模块中映射此数据。

如果您的子方案有多个路由，我们建议将此模块添加到始终在任何其他路由之后运行和执行的路由中。

要配置添加响应程序模块，请执行以下操作：

1. 要使用现有的数据结构，请在数据结构字段中，选择将用于子方案返回给父方案的数据的数据结构。

   或

   要为数据创建新的数据结构，请单击“数据结构”字段旁边的&#x200B;**添加**&#x200B;并创建数据结构。

   有关创建数据结构的说明，请参阅[数据结构](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md)。

1. 单击&#x200B;**确定**&#x200B;以保存模块。
