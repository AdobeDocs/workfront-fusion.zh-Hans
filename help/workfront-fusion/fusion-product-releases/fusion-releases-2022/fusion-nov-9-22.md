---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: Workfront Fusion 发行活动：2022 年 11 月 7 日当周
description: 本页介绍了2022年11月7日这一周在Adobe Workfront Fusion中所做的所有增强。
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9d58abd0-1fe7-43c8-a1ea-2fadea738590
TQID: https://experienceleague.adobe.com/iigr0fKWxXA-DvvPZVjZvIQ3s-dW6XUBWgMYaxoGZRs
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 25%

---

# Workfront Fusion 发行活动：2022 年 11 月 7 日当周

**Webhook队列优化**

Fusion的webhook队列已在此版本中进行了优化。 现在，接受webhook的服务与排队和其他进程是分开的。 此更改使Fusion能够以更快、更一致的速率处理webhook队列。

在实施此更改期间，我们能够更好地了解已排队webhook事件的预期日志处理时间。 Fusion的webhook查看器页面不应超过1分钟。

要查看当前排队的webhook事件，请在左侧导航中导航到Webhook。 分子中具有数字的卡车图标表示该webhook的队列事件。 单击卡车图标以查看已排队的事件。


**现在将停用或删除未使用的Webhook**

我们对Workfront Fusion处理未使用Webhook的方式进行了一些更改。 现在，如果以下任一情况适用，则会自动停用wWebhook：

* webhook已超过5天未连接到任何场景。
* Webhook 仅用于处于非活动状态的场景，并且这些场景已超过 30 天未活动。

如停用的 Webhook 未连接至任何场景且停用超过 30 天，将会自动删除并注销。
