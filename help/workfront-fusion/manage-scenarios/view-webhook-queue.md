---
title: k队列
description: 许多服务都提供Webhook，以便在服务发生特定更改时即时发送通知。 即时触发器（也称为Webhook）可以使用这些事件开始场景。 事件在等待处理时进入webhook的队列，例如当场景已经在运行时。 您可以查看webhook的队列。
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
TQID: 'https://experienceleague.adobe.com/FtTjoNtYNM9kuPDMaHa4883m13pLO2MRat5ohnjXuAM'
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 1c28e4007e3e9d6503618482002e506f9393ee57
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 16%
---
# 查看webhook的队列

许多服务都提供Webhook，以便在服务发生特定更改时即时发送通知。 即时触发器（也称为Webhook）可以使用这些事件开始场景。 事件在等待处理时进入webhook的队列，例如当场景已经在运行时。 您可以查看webhook的队列。

传入的webhook数据始终存储在队列中，无论您在场景设置面板中如何设置“数据是机密的”选项。 在场景中处理数据后，将从队列中永久删除该数据。

有关 Webhook 的更多信息，请参阅[即时触发器（Webhooks）](/help/workfront-fusion/references/modules/webhooks-reference.md)。

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

## 查看webhook的队列

来自传入webhook的所有消息都存储在webhook的队列中。

如果某个方案当前具有队列，则该方案中会显示一条横幅：

![队列横幅](assets/queue-banner.png)

webhook的队列页面具有与&#x200B;**[!UICONTROL 方案]**&#x200B;和&#x200B;**[!UICONTROL Webhook]**&#x200B;列表相同的布局。

>[!NOTE]
>
>搜索和排序仅适用于当前加载到表中的事件，而不适用于整个队列。 要包含更多事件，请首先加载其他事件。

要查看和管理webhook的队列，请执行以下操作：

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Webhooks]**。
1. 找到要查看其队列的Webhook。
1. 找到事件数“队列已满”列。

   ![Webhook队列](assets/webhook-queue.png)

1. 单击&#x200B;**操作**&#x200B;按钮可查看有关队列中事件的详细信息。

   webhook的队列页面将打开。 该页面在表中列出了队列中的事件，这些事件具有以下列： **[!UICONTROL ID]**、**[!UICONTROL 创建于]**、**[!UICONTROL 大小]**&#x200B;和&#x200B;**[!UICONTROL 详细信息]**。

1. （可选）要筛选表中的事件，请在表上方的&#x200B;**[!UICONTROL 搜索]**&#x200B;字段中输入文本。
1. （可选）要对事件进行排序，请单击&#x200B;**[!UICONTROL ID]**、**[!UICONTROL 创建于]**&#x200B;或&#x200B;**[!UICONTROL Size]**&#x200B;列标题。
1. （可选）要更改每个页面上显示的事件数，请在页面底部的&#x200B;**[!UICONTROL 显示]**&#x200B;下拉列表中选择一个数字。
1. （可选）若要在事件页面之间移动，请单击页面底部的&#x200B;**[!UICONTROL First]**、**[!UICONTROL Previous]**、**[!UICONTROL Next]**&#x200B;或&#x200B;**[!UICONTROL Last]**。

   当队列只有一页事件时，这些按钮不可用。

1. （可选）要查看事件的有效负载，请单击该事件行中的&#x200B;**[!UICONTROL 详细信息]**。

   这将打开详细信息对话框，并显示事件的有效负载。

1. （可选）要删除事件，请执行以下操作：

   1. 通过执行以下操作之一，Select要删除的事件：

      * Select中每个要选择的事件旁边的复选框。
      * Select **[!UICONTROL Select all]**&#x200B;复选框可选择整个队列，而不仅仅是当前加载的事件。 然后，您可以清除要从选定范围中排除的任何事件的复选框。

   1. 在靠近屏幕底部的栏中，单击&#x200B;**删除**。
