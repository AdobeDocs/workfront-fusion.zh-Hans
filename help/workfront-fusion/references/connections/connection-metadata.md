---
title: 连接元数据
description: Fusion使用元数据来标识连接的重要属性。
author: Becky
feature: Workfront Fusion
exl-id: b41fbe8c-30fa-49d0-8a24-3535642b97ae
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---

# 连接元数据

Fusion使用元数据来标识连接的重要属性。

创建新连接时可以设置连接元数据。 这些属性位于用于设置连接的同一对话框中：

![连接元数据](assets/connection-metadata-setup.png)

Fusion用户可以从“连接”区域查看和编辑连接。

连接区域中的![连接元数据](assets/connections-area-metadata.png)

## 环境类型

生产和非生产系统均可使用Fusion连接。 您可以标记连接所连接的环境类型，这有助于保护生产环境。

与其他连接元数据一样，环境类型仅用于提供信息。 用户负责准确地设置此属性，并在场景中使用与正确环境的连接。

## 身份验证类型

Fusion连接可用于服务帐户和个人帐户。 当场景自动变为Fusion时，使用服务帐户进行身份验证。 个人帐户是基于特定人员的身份验证。 使用的身份验证类型取决于方案的要求。 个人帐户应用于自动用户操作。 例如，如果Fusion场景自动批准特定人员，则身份验证类型应该适用于该人员。 否则，Fusion将充当Fusion，并且类型应为服务帐户。

与其他连接元数据一样，身份验证类型仅用于提供信息。 用户负责准确地设置此属性，并在场景中使用正确的连接类型。

有关身份验证类型的详细信息，请参阅Adobe身份验证指南中的[身份验证](https://developer.adobe.com/developer-console/docs/guides/authentication/)。

## 资源

* 有关管理连接元数据的说明，请参阅[管理连接](/help/workfront-fusion/create-scenarios/connect-to-apps/manage-connections.md)。
