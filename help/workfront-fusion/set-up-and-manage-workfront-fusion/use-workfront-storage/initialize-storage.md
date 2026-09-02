---
title: 初始化存储
description: 当用户首次导航到Storage时，他们会看到一个初始化屏幕，该屏幕会代表团队创建到Adobe Storage的安全连接。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 216
ht-degree: 0%

---

# 在Workfront Fusion中初始化存储

必须先初始化Fusion Storage区域，然后才能在Adobe云存储中查看存储库、文件夹和文件。

有关存储的概述，请参阅[存储概述](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md)。

## 初始化存储

1. 在Workfront Fusion中，单击左侧导航栏中的&#x200B;**存储**。
1. 单击&#x200B;**初始化存储**。

Fusion会代表团队自动创建到Adobe Storage的安全连接。

建立连接后，Fusion将加载团队的存储库。

## 初始化疑难解答

| 消息 | 原因 | 用户应该做什么 |
| -------- | -------- | ------------------------ |
| **访问受限** | 组织未载入Adobe IMS。 | 联系组织管理员以完成IMS载入。 |
| **组织不匹配** | 用户已登录到其他非Fusion中选择的Adobe组织。 | 注销，然后使用正确的Adobe IMS组织重新登录。 |
| **访问被拒绝** | 用户的帐户没有所需的权限，或者Adobe Storage对组织不可用。 | 向组织管理员验证帐户权限。 解析后，单击&#x200B;**重试**。 |
| **未找到存储** | 已建立连接，但未找到存储库。 | 验证是否已为组织配置Adobe存储。 验证后，单击&#x200B;**加载存储**&#x200B;重试。 |
