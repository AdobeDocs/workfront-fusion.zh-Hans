---
title: 工作人员池
description: 工作进程池是专用于一个或多个特定组织的Workfront Fusion处理资源数量。 所有Fusion操作和处理都发生在组织分配的工作进程池的上下文中。
author: Becky
feature: Workfront Fusion
exl-id: 8bf508a8-d1f9-455f-af89-62f688289137
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: b800142d824927e5765eed50a831731e6b5d9925
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 19%
---
# 工作人员池

工作线程池是专用于特定组织的一系列Workfront Fusion处理资源。 所有Fusion操作和处理都发生在组织分配的工作进程池的上下文中。

工作池使您的方案能够更高效地运行，并消除了与其他组织竞争获得Fusion处理容量的机会。

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
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 工作线程池概述

工作线程池是一种并行处理场景执行的方法。 每个工作线程池都与：

* 多名工作人员。
* 执行队列。

执行场景时，场景会传递到工作池的执行队列中。 池中的工作进程不断从执行池中提取任务并并行处理它们。

如果执行队列深度增加，并且正在使用所有现有工作进程，则Workfront Fusion将通过添加更多工作进程来自动缩放池。 这种扩展是动态的，并且是事件驱动的，这意味着无需您或您的组织采取任何操作，容量便会根据实时负载来获取或订立合同。

Workfront Fusion团队会持续监控池的利用率和扩展行为，并可以查看阈值或模式以确保随着使用率的增长保持性能的一致性。

## 重命名工作线程池

组织所有者和管理员可以重命名分配给其组织的工作者池。 默认情况下，每个池都会显示系统生成的名称。 您可以为池提供一个自定义名称，如`Marketing EU`或`High-volume integrations`，然后根据需要随时更改它。

重命名池只会更改其标记方式。 方案、执行和池容量不受影响。 新名称会出现在显示池的任何位置，例如将方案分配给池时。

>[!NOTE]
>
>仅当为您的组织分配了多个辅助进程池时，才会显示&#x200B;**[!UICONTROL 辅助进程池]**&#x200B;选项卡。 如果贵组织只有一个Worker池或使用共享池，则不会显示选项卡。

要重命名工作线程池，请执行以下操作：

1. 在左侧导航中，单击&#x200B;**组织概述**
1. 单击页面顶部附近的&#x200B;**[!UICONTROL 工作线程池]**&#x200B;选项卡。

   选项卡列出了每个池并显示为其分配了多少方案。

1. 单击要重命名的池旁边的&#x200B;**[!UICONTROL 重命名]**。
1. 在打开的面板中，输入新名称。
1. 单击&#x200B;**保存**。
