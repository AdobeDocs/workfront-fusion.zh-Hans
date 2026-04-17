---
title: 向场景添加AI提示
description: 您可以在场景中包含一个AI提示，该提示会连接到
author: Becky
feature: Workfront Fusion
exl-id: d0ac0d0b-e3a0-46de-801d-e53c1c4d63ff
source-git-commit: 3d957c219cdc5fed4fdf9b0649cab724fae21871
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 向场景添加AI提示

您可以使用与大型语言模型(LLM)结合使用的模型上下文协议(MCP)在场景中包含AI提示。 通过在MCP代理模块中配置这些工作流，您可以使用人工智能来设置高效、安全和灵活的工作流。

## 模型上下文协议概述

模型上下文协议(Model Context Protocol，MCP)是一种将AI语言模型与其他应用程序安全连接的方法。 您可以配置MCP服务器，以允许AI模型访问应用程序。 然后，您可以向AI模型发送提示，它可以从应用程序返回信息。

例如，您可以配置MCP服务器将AI模型与Gmail连接。 当您向大型语言模型发送提示“Give my last 5 emails from Gmail”时，它会解析该提示并将其发送到Gmail MPC服务器，然后服务器可以访问您的Gmail并返回电子邮件。

MCP代理模块允许您使用语言模型和MCP服务器处理用户提示。

## 在Fusion场景中使用MCP的好处

在场景中使用MCP具有以下优势：

* 在场景中使用MCP可减少思考操作的所有情况和可能变体的需要。 通过使用提示，您无需使用正则表达式或解析数据来解释这些变化。
* 可以使用从先前模块映射的元素或映射面板中的其他函数为提示提供上下文。
* 使用提示可以比使用特定模块构建场景更有效、更灵活，因为它可以在提示上使用推理并从可用上下文中选择最佳操作过程。
* 由于您配置了模块可以连接到的MCP服务器，因此您可以控制该服务器的安全性，并且可以确保安全性符合您组织的需要。

>[!NOTE]
>
>可用功能取决于MCP服务器中可用的工具，不受Fusion控制。

## 向场景添加AI提示

您可以使用MCP代理模块向方案添加AI提示。

有关说明，请参阅[MCP代理模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md)。
