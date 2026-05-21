---
title: k队列
description: 许多服务都提供Webhook，以便在服务发生特定更改时即时发送通知。 即时触发器（也称为Webhook）可以使用这些事件开始场景。 事件在等待处理时进入webhook的队列，例如当场景已经在运行时。 您可以查看webhook的队列。
author: Becky
feature: Workfront Fusion
exl-id: 04aed0cb-e837-4c81-8eb1-113075d2ada8
TQID: https://experienceleague.adobe.com/FtTjoNtYNM9kuPDMaHa4883m13pLO2MRat5ohnjXuAM
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 29%

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

查看webhook的队列：

1. 单击左侧菜单中的&#x200B;**[!UICONTROL Webhooks]**。
1. 找到要查看其队列的Webhook。
1. 在“接收的事件”按钮中找到事件数。

   ![Webhook队列](assets/webhook-queue.png)

1. 单击按钮可查看有关队列中事件的详细信息。
