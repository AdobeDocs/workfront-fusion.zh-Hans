---
title: 工作人员池
description: 工作进程池是专用于一个或多个特定组织的Workfront Fusion处理资源数量。 所有Fusion操作和处理都发生在组织分配的工作进程池的上下文中。
author: Becky
feature: Workfront Fusion
source-git-commit: bb94083eb9f58dc3ae9f94a59288da43317b567b
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# 工作人员池

工作线程池是专用于特定组织的一系列Workfront Fusion处理资源。 所有Fusion操作和处理都发生在组织分配的工作进程池的上下文中。

工作池使您的方案能够更高效地运行，并消除了与其他组织竞争获得Fusion处理容量的机会。

## 工作线程池概述

工作线程池是一种并行处理场景执行的方法。 每个工作线程池都与：

* 多名工作人员。
* 执行队列。

执行场景时，场景会传递到工作池的执行队列中。 池中的工作进程不断从执行池中提取任务并并行处理它们。

如果执行队列深度增加，并且正在使用所有现有工作进程，则Workfront Fusion将通过添加更多工作进程来自动缩放池。 这种扩展是动态的，并且是事件驱动的，这意味着无需您或您的组织采取任何操作，容量便会根据实时负载来获取或订立合同。

Workfront Fusion团队会持续监控池的利用率和扩展行为，并可以查看阈值或模式以确保随着使用率的增长保持性能的一致性。
