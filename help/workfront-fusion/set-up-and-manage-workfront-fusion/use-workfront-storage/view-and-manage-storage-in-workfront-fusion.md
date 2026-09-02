---
title: 在Workfront Fusion中查看和管理存储
description: 存储区域列出了可用的存储库，并允许您浏览文件夹和文件。
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: a2632cb3184cd555555136288e78ab1e05e4ea9d
workflow-type: tm+mt
source-wordcount: 330
ht-degree: 1%

---

# 在Workfront Fusion中查看和管理存储

Workfront Fusion中的存储区域允许您查看Adobe云存储中的存储库并与之交互。

有关存储的概述，请参阅[存储概述](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md)。

>[!TIP]
>
>必须先初始化存储，然后才能查看存储库。 有关说明，请参阅[初始化存储](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md)。

## 查看存储库、文件夹和文件

1. 在Workfront Fusion中，单击左侧导航栏中的&#x200B;**存储**。
此时将打开存储库列表。

   如果只有一个可用存储库，则直接打开存储库。

1. 单击任意存储库上的&#x200B;**打开**&#x200B;以浏览其内容。

   打开存储库会显示存储库中的文件夹。
1. 单击文件夹以将其打开并显示其“文件”。
1. 要通过文件夹结构向后导航，请单击痕迹导航。


>[!NOTE]
>
>空文件夹显示消息： *“此文件夹为空”*

## 管理多个存储连接

一个团队可以有多个Adobe Storage连接。

1. 在Workfront Fusion中，单击左侧导航栏中的&#x200B;**存储**。
如果存在多个连接，“存储”页面的顶部将显示选项卡，标记每个连接的名称。
1. 要切换到其他连接的存储库，请单击该连接的选项卡。

如果连接无效（如令牌过期且无法刷新），则连接会被自动过滤掉，并且不会显示为选项卡。 Fusion的计划令牌刷新可保持连接自动有效。

## 文件信息

表中的每个文件都显示：

| 列 | 描述 |
| -------- | ------------- |
| **名称** | 带有文档图标的文件名。 |
| **类型** | 文件扩展名徽章，如PNG、PDF或JPG。 |
| **大小** | 文件大小。 如果文件最近上传，而后端仍在处理该文件，则显示&#x200B;*“正在处理……”*。 |
| **已创建** | 创建日期。 |

存在多个版本时，文件还会显示&#x200B;**版本徽章**（例如，`v2`、`v3`）。

## 表控件

* **搜索/筛选器**：使用全局搜索栏按名称筛选文件。
* **排序**：单击列标题进行排序。
* **分页**：每页选择10、25、50或100个项目。 默认值为25。
