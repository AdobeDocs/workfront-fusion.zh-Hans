---
title: Fusion组织和团队概述
description: 通过Adobe Workfront Fusion的“组织”和“团队”功能，企业可以控制对Fusion中场景和其他功能的访问。
author: Becky
feature: Workfront Fusion
exl-id: 44e6de2a-b2d3-410d-abc3-10facd258495
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 1%

---

# [!DNL Adobe Workfront Fusion]组织和团队概述

通过[!DNL Adobe Workfront Fusion]的“组织”和“团队”功能，企业可以控制对Fusion中场景和其他功能的访问。

组织是Adobe Workfront Fusion中的最大实体。 例如，您的Fusion组织可能代表您整个公司的Fusion帐户。

团队是组织内的较小组，可共享Fusion资源，如方案、连接和模板。

## 组织

[!DNL Workfront Fusion]用户属于某个组织。

在将用户添加到团队之前，必须先将用户添加到组织。

### 组织角色

用户在组织中具有以下角色之一：

* **[!UICONTROL Owner]**：所有者拥有组织中可用的所有权限。
* **[!UICONTROL Admin]**：管理员可以为组织创建和管理团队和用户，还可以批准模板。
* **[!UICONTROL Member]**：成员可以使用[!DNL Workfront Fusion]，但无法进行组织更改。
* **[!UICONTROL Accountant]**：会计师可以在组织仪表板上看到许可证信息，但无法执行任何操作。
* **[!UICONTROL App Developer]**：此角色的功能当前不可用，并且将在不久的将来可用。 我们建议目前不要将用户分配给此角色。

有关每个组织角色中用户可以执行的特定操作的信息，请参阅[组织和团队角色](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md)。

## 团队

团队是共享对特定资源的访问权限的用户组。 这些资源可能包括：

* 方案
* 连接
* Webhook
* 键
* 数据存储
* 数据结构
* 电子邮件通知设置

>[!NOTE]
>
>由于团队共享资源，因此有时一个团队仅有一个成员会很有用。 例如，培训用户可能会创建与其个人[!DNL Workfront]帐户的连接。 任何团队成员也将能够连接到单个[!DNL Workfront]帐户。 在这种情况下，我们建议用户成为培训团队的唯一成员。

组织可以拥有所需数量的团队，并且用户可能属于一个或多个团队。

用户可以从左侧导航面板的下拉列表中选择其团队。 用户只能看到其所属的团队。 选择团队将允许用户访问该团队的资源。

### 团队角色

用户在其每个团队中具有以下角色之一：

* **[!UICONTROL Team Admin]**：管理员可以添加、删除或更改团队成员的角色。 他们还可以执行对其他团队角色可用的任何操作。
* **[!UICONTROL Team Member]**：团队成员角色允许用户创建和执行方案。
* **[!UICONTROL Team Monitoring]**： [!UICONTROL monitoring]角色允许用户访问方案的执行信息，但他们无法设计方案或更改其“活动”状态。
* **[!UICONTROL Team Operator]**： [!UICONTROL operator]角色允许用户查看执行数据并更改方案的“活动”状态。
* **[!UICONTROL Team Restricted Member]**：此角色的功能当前不可用，并且将在不久的将来可用。 我们建议目前不要将用户分配给此角色。

有关每个团队角色中用户可以执行的特定操作的信息，请参阅[组织和团队角色](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md)。
