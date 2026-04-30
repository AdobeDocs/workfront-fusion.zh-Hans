---
title: 编辑Webhook
description: 您可以编辑Workfront和Workfront Planning连接器的现有Webhook。
author: Becky
feature: Workfront Fusion
source-git-commit: 2561c911b9b542a7b143fae745baf4e1de45be38
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 4%

---

# 编辑Webhook

您可以编辑现有的Webhook。 使用这些webhook的场景将使用新的配置，这样便无需创建新的webhook并将其手动分配给所有受影响的场景。

只能为以下连接器编辑Webhook：

* Workfront
* Workfront Planning

>[!IMPORTANT]
>
>更新webhook时，请考虑以下事项：
>
>* Workfront事件订阅会将编辑后的webhook视为新订阅。 对于以前的webhook配置，不会保留事件订阅历史记录，因为它被视为单独的事件订阅。
>* 从旧事件订阅切换到新事件订阅可能不会完全同步。 因此，可能会收到两次事件（如果新订阅在旧订阅停止之前开始运行）或错过事件（如果旧订阅在新订阅开始运行之前停止）。

## 编辑webhook

您可以从场景或Webhooks列表中编辑Webhook。

### 在场景中编辑webhook

>[!NOTE]
>
>此功能仅适用于具有Workfront或Workfront Planning即时触发器模块的方案。

1. 转到包含要编辑的webhook的场景。
1. 在方案的触发器模块中，单击Webhook字段旁边的下拉菜单，然后选择&#x200B;**编辑项**。

   将打开webhook的配置窗口，其中填充了现有配置。

1. 对webhook进行任何所需的编辑。
1. 点击&#x200B;**保存**&#x200B;以保存 Webhook 并返回模块。

### 从Webhook列表中编辑Webhook

1. 在左侧导航中，选择&#x200B;**Webhooks** ![Webhooks图标](assets/webhooks-icon.png)。
1. 单击要编辑的webhook旁边的复选框。
1. 在屏幕底部的蓝色横幅中，单击&#x200B;**编辑**。
1. 对webhook进行任何所需的编辑。
1. 单击&#x200B;**保存**&#x200B;以保存Webhook并返回Webhook列表。

