---
title: Adobe Experience Manager MCP模块
description: 使用Adobe Experience Manager MCP模块，您可以向Adobe Experience Manager的MCP服务器发送纯英语提示，并让AI模型执行该请求。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 4c23409465b4be9fd10ff6938a750bc662ba2fe4
workflow-type: tm+mt
source-wordcount: 1020
ht-degree: 11%

---

# Adobe Experience Manager MCP模块

Adobe Experience Manager MCP连接器是Adobe Experience Manager自己的模型上下文协议(MCP)服务器的专用Fusion集成。 与典型连接器不同（每个模块执行一个固定操作），该连接器具有一个模块，用于接受开放式的纯英语指令，并允许AI模型决定需要哪些Adobe Experience Manager操作才能完成该指令，可跨站点、数字资产、内容片段、文件夹、内容存储库和内容人工智能等区域执行此操作。

此连接器专用于Adobe Experience Manager自己的MCP服务器。 它不支持其他不相关的MCP服务器。 对于连接器，您可以改为指向任何MCP服务器，请使用MCP代理连接器。

有关MCP代理连接器的信息，请参阅[MCP代理模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/model-context-protocol-mcp-connector.md)。

>[!NOTE]
>
>此模块中的响应是人工智能生成的，有时可能不完美，即使有了所有可用的保护措施。 此模块适用于人工无法实时查看每次运行的自动化功能，但无法保证您从传统Adobe Experience Manager模块中会获得的确定性行为。

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
   <td role="rowheader">Adobe Workfront Fusion 许可证</td> 
   <td>
   <p>基于操作：适用于拥有基于操作的许可证的组织</p>
   <p>基于连接器（旧版）：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

有关 Adobe Workfront Fusion 许可证的详细信息，请参阅 [Adobe Workfront Fusion 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

* 您必须拥有Adobe Experience Manager帐户才能使用此模块。

## 将Adobe Experience Manager MCP连接到Workfront Fusion {#connect-adobe-experience-manager-mcp-to-workfront-fusion}

Adobe Experience Manager MCP连接器使用OAuth连接到Adobe Experience Manager。 没有可手动填写的连接字段，例如用户名、密码或API密钥。

要创建连接，请执行以下操作：

1. 在Adobe Experience Manager MCP模块中，单击连接字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 选择您要连接到生产环境还是非生产环境。
1. 选择您是连接到服务帐户还是个人帐户
1. 单击&#x200B;**继续**。

   您将被重定向到Adobe的登录页面。
1. 在Adobe登录页面上，登录并批准访问权限。

系统会将您重定向回Workfront Fusion，并且新连接将在模块中可用。

## Adobe Experience Manager MCP模块及其字段

目前，Adobe Experience Manager MCP连接器只有一个模块。

### 处理用户提示

该操作模块向Adobe Experience Manager的MCP服务器发送一个纯英文指令，并返回AI的答案。

此模块的每次运行都是一个独立的执行，类似于发送电子邮件而不是进行实时对话。 AI无法再提出后续问题并等待您的答复。 相反，它会做出最佳判断，并返回完整的答案。 如果您的提示模棱两可，人工智能会声明它所做的任何假设都是其答案的一部分，而不是停下来要求您澄清。

>[!IMPORTANT]
>
>此模块仅在您的提示实际请求写入或删除操作时才执行写入或删除操作。 它不会采取任何您未请求的额外操作，即使是在它执行您未请求的其他操作时。

由于每次运行都是独立的，因此模块本身没有先前运行的内存。 要创建跨越多次运行的多圈对话体验，请存储上一个问题和答案。 您可以对此使用数据存储区，然后将该历史记录作为文本包含在下一个提示的开头处，然后是新问题。

有关数据存储的信息，请参阅[数据存储](/help/workfront-fusion/create-scenarios/data-stores/data-store-overview.md)。

<table style="table-layout:auto"> 
 <col/>
 <col/>
 <tbody>
  <tr>
   <td role="rowheader">LLM键<i>（可选，高级）</i></td>
   <td><p>默认情况下，此模块使用Adobe自己的AI服务处理您的提示，您无需选择键。</p><p>若要改用您自己的AI提供程序，请选择一个现有的LLM密钥，或通过单击<b>添加</b>并输入以下信息创建一个新密钥：</p>
    <ul>
     <li><b>密钥名称</b>：输入新密钥的名称。</li>
     <li><b>LLM</b>：选择与此键关联的大型语言模型。 支持的提供商包括OpenAI、Anthropic Claude和Amazon Bedrock。</li>
     <li><b>密钥</b>：输入或映射所选提供商的API密钥。</li>
     <li><b>模型</b>：选择键将使用的LLM模型。</li>
     <li><b>其他字段</b>：为LLM所需的任何其他字段输入值。</li>
    </ul>
   </td>
  </tr>
  <tr>
   <td role="rowheader">连接</td>
   <td><p>有关将Adobe Experience Manager帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-mcp-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager MCP连接到Workfront Fusion</a>。</p></td>
  </tr>
  <tr>
   <td role="rowheader">用户提示</td>
   <td><p>以纯英语输入或映射您希望AI执行的指令。</p><p>示例：<i>在营销文件夹中查找90天内未更新的所有资产。</i></p></td>
  </tr>
  <tr>
   <td role="rowheader">只读工具<i>（可选）</i></td>
   <td><p>限制允许AI调用哪些只读Adobe Experience Manager操作 — 仅查找某些内容（例如查找资源或读取页面内容）的操作，并且绝不更改任何内容。</p><p>如果此字段留空，则允许所有只读操作。</p></td>
  </tr>
  <tr>
   <td role="rowheader">写入/删除工具<i>（可选）</i></td>
   <td><p>限制允许AI调用哪些写入或删除Adobe Experience Manager操作 — 即更改某些内容的操作，如更新页面、发布内容或删除资源。</p><p>如果此字段留空，则允许执行所有写入和删除操作。 为了确保无人参与场景从不执行破坏性操作，我们建议将此字段保留设置为有意的空选择，而不是将其保留为不受限制。</p></td>
  </tr>
 </tbody>
</table>

该模块会以文本形式返回AI的最终答案，并记录产生该答案时发生了什么情况，包括调用了哪些工具、每次调用是否成功以及处理耗时多长。
