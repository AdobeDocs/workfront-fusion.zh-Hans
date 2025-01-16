---
title: HTTP请求方法
description: 在模块中配置API调用时，必须选择HTTP请求方法。 本文介绍了可用的方法，以及选择每种方法的原因。
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# HTTP请求方法

在模块中配置API调用时，必须选择HTTP请求方法。 本文介绍了可用的方法，以及选择每种方法的原因。

## HTTP方法

使用以下HTTP方法之一。

* **[!UICONTROL GET]**：根据您的参数从Web服务器中检索数据。 [!UICONTROL GET]请求指定资源的表示形式，并在成功时接收包含所请求内容的[!UICONTROL 200 OK]响应消息。
* **[!UICONTROL POST]**：根据您的参数向Web服务器发送数据。 [!UICONTROL POST]请求包括上载文件等操作。 多个[!UICONTROL POST]可能会产生与单个[!UICONTROL POST]不同的结果，因此，请小心不要无意中发送多个[!UICONTROL POST]。如果[!UICONTROL POST]成功，您将收到[!UICONTROL 200 OK]响应消息。
* **[!UICONTROL PUT]**：根据您的参数将数据发送到Web服务器中的位置。 [!UICONTROL PUT]请求包括上载文件等操作。 [!UICONTROL PUT]和[!UICONTROL POST]之间的区别在于PUT是幂等的，这意味着单个成功[!UICONTROL PUT]的结果与许多相同的[!UICONTROL PUT]的结果相同。如果PUT成功，您将收到200响应消息（通常为201或204）。
* **[!UICONTROL PATCH]**： （对于某些API调用模块不可用）根据您的参数对Web服务器上的资源应用部分修改。 [!UICONTROL PATCH]不是幂等的，这意味着多个[!UICONTROL PATCH]的结果可能会产生意外结果。 如果[!UICONTROL PATCH]成功，您将收到200响应消息（通常为204）。
* **[!UICONTROL DELETE]**：根据您的参数从Web服务器删除指定的资源（如果该资源存在）。 如果[!UICONTROL DELETE]成功，您将收到“200确定”响应消息。
