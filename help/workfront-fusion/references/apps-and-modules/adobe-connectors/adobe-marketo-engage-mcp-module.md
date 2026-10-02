---
title: Adobe Marketo Engage MCP模块
description: Adobe Marketo Engage MCP模块允许您向Adobe Marketo Engage的MCP（模型上下文协议）服务器发送自然语言提示。
author: Becky
feature: Workfront Fusion
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
    internal-label: APIs
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
  - id: e14a7f57-c82c-4874-a495-5d036cbbdc3d
    internal-label: Resource management
subfeature_v2:
  - id: b70a979b-965d-47a9-a360-e7ec2a19b8c1
    internal-label: Digital content and documents
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 9e08c421a53c7ca499715fa8e32be6c10fbde1d9
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 9%
---
# Adobe Marketo Engage MCP模块

Adobe Marketo Engage MCP模块允许您使用人工智能模型向Adobe Marketo Engage的MCP（模型上下文协议）服务器发送自然语言提示，以解释请求并调用Marketo自己的工具来完成请求。 与每个模块执行一项固定操作（如“创建商机”）的传统Marketo连接器不同，此连接器具有一个接受纯英语开放式指令的模块，并允许AI决定需要哪些Marketo操作来满足该指令。

此连接器专门用于Marketo Engage自己的MCP服务器

若要连接到其他应用程序的MCP，请参阅[向方案添加AI提示](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md)。

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

* 您必须拥有Adobe Marketo Engage帐户和有效的Marketo实例。

## 将Adobe Marketo Engage MCP连接到Workfront Fusion {#connect-adobe-marketo-engage-mcp-to-workfront-fusion}

您可以直接在Adobe Marketo Engage MCP模块内创建与Marketo实例的连接。

1. 在Adobe Marketo Engage MCP模块中，单击&#x200B;**连接**&#x200B;字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>
          <p>选择您要连接到生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>
          <p>选择连接服务帐户还是个人帐户。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端 ID]</td>
        <td>
          <p>输入在Marketo LaunchPoint中创建的Marketo REST API服务的客户端ID。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>
          <p>输入Marketo LaunchPoint中创建的Marketo REST API服务的客户端密钥。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL Munchkin ID]</td>
        <td>
          <p>输入您的Marketo实例的Munchkin ID（例如，'123-ABC-456'）。 Munchkin ID显示在Marketo中的<b>管理员→Munchkin</b>下。</p>
        </td>
      </tr>
    </tbody>
   </table>

1. 单击&#x200B;**继续**&#x200B;以创建连接并返回模块。

>[!IMPORTANT]
>
> * 使用具有场景所需的最低角色和权限的专用仅限API的Marketo用户，而不是重用管理员帐户。
> * 创建连接不会验证凭据。 Fusion会在不进行测试调用的情况下保存它们，因此即使值错误或键入错误，连接似乎也可以成功创建。 如果凭据不正确，则在模块首次尝试访问Marketo或工具列表加载失败时，通常会稍后显示失败。

## 模块：“处理用户提示”

这是连接器提供的唯一模块。 场景通过以下方式使用它：

1. **连接** — 上面创建的Marketo连接。
2. **输入提示** — 用纯英文输入说明（例如，“查找上周添加到Spring网络研讨会列表中的每个潜在客户，并告诉我哪些潜在客户未设置公司名称”）。
3. **工具**（可选） — 如下所述。 这些字段仅在选择连接后显示。
4. **LLM键**（可选，高级） — 如下所述。

它以文本形式返回AI的最终答案，并包含生成该答案时发生的行为的完整审计追踪。

## Adobe Marketo Engage MCP模块及其字段

### 处理用户提示

该操作模块向Adobe Marketo Engage的MCP服务器发送一个纯英文指令，并返回人工智能的响应。

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
   <td><p>有关将Marketo帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-marketo-engage-mcp-to-workfront-fusion" class="MCXref xref">将Adobe Marketo Engage MCP连接到Workfront Fusion</a>。</p></td>
  </tr>
  <tr>
   <td role="rowheader">用户提示</td>
   <td><p>以纯英语输入或映射您希望AI执行的指令。</p><p>示例：<i>查找过去7天内添加到春季网络研讨会列表的所有潜在客户，并总结哪些行业最常见。</i></p></td>
  </tr>
 </tbody>
</table>

### 模块输出

输出是包含以下内容的单个包：

* 响应：人工智能的最终答案，作为文本。 您可以将此数据映射到后续模块。
* 审核记录：运行的详细记录，包括会话ID、原始提示、开始和结束时间、总持续时间、总体状态、最终响应以及工具调用列表。 每个工具调用条目记录了Marketo工具运行的时间、参数、输出、开始和结束时间及持续时间、是否成功以及在序列中的顺序。
* 摘要：同一运行浓缩为计数：工具调用总数、成功调用、失败调用、处理时间和状态。

### AI模型

默认情况下，该模块自动使用Adobe自己的托管AI服务，无需输入密钥或凭据。

您可以改为选择特定的LLM密钥来使用OpenAI、Anthropic Claude或Amazon Bedrock（如果贵组织拥有具有其中一种帐户的帐户）。

### 选择允许AI执行的Marketo操作

选择连接后，模块会询问Marketo MCP服务器它提供了哪些工具，并将这些工具显示为多选列表，其中每个列表显示了它包含多少工具：

* 只读工具：仅查找某些内容且从不更改任何内容的操作，例如查找潜在客户、列出营销活动成员或读取项目的详细信息。
* 撰写/删除工具：更改某些内容的操作，如创建或更新潜在客户、将某人添加到列表、激活营销活动或批准或发送电子邮件。
* 其他工具：第三个列表，仅当Marketo服务器提供其未标记为只读或未标记为只读的工具时显示。 它们单独显示，而不是假定为安全或不安全。 如果服务器对所有内容进行标记，则此列表不会显示。

如果未选择工具，则AI可以使用所有工具。 您可以将列表限制为特定操作。 例如，只选择2个特定的“写入”操作，而保留“只读”状态，这意味着AI可以自由查找它所需的任何内容，但只能进行这2种特定类型的更改。 将列表留空表示允许该类别中的所有操作。 限制AI需要主动选择要在该类别中允许的特定操作。 这样，您可以确保AI不会对实时营销数据采取意想不到的破坏性操作，同时仍让其能够自由收集信息。

由于列表是从Marketo服务器实时读取的，因此显示的确切工具可能会随着Adobe更新该服务器而更改。

### 无持久对话历史记录

此模块的每次运行都是一个独立执行。 AI不能问后续问题并等待答复。 相反，它必须做出最佳判断，一次性给出完整的最终答案。 如果请求模棱两可，AI将做出合理假设，将该假设作为答案的一部分陈述，然后继续。 它不会停止并要求用户进行澄清，因为它无法在单次运行中收到回复。

此外，AI还被指示通过工具调用来验证事实，而不是依赖内存，因为Marketo数据在上次运行后可能已发生更改。

AI只会在提示实际请求写入、更新或删除操作时执行操作。 它不会采取未请求的操作，包括激活或停用营销活动、创建或删除潜在客户和列表、批准或发送电子邮件，即使在它执行了用户曾要求的其他操作的同一运行中也是如此。

因为每次运行都是独立的，所以人工智能没有以前单独运行的记忆。 一种场景，想要多转、类似聊天的体验需要将该历史记录明确提供为新提示的一部分，例如将以前的问题和答案存储在Fusion的数据存储中，或者在模块之间传递，并在新提示开始时将其作为文本包含，随后添加新问题。 没有自动记住先前运行的会话或对话ID。

## 示例提示

您可以使用如下提示：

* *列出过去7天内加入“第3季度产品发布”计划的潜在客户，并总结他们来自哪些行业。*
* *检查“欢迎系列”智能营销活动当前是否处于活动状态，并告诉我有多少人在活动中。*
* *查找定价页面上使用的表单，并告诉我哪些字段标记为必填字段。*
* *将电子邮件为`jane@example.com`的潜在客户添加到“VIP客户”静态列表。*
* *在“春季新闻稿”计划中总结每封电子邮件的性能。*

<!--

## What a content writer should NOT claim

* Connection form: Do not describe the connection as an OAuth or "sign in with Adobe" flow. It is not one. It is three credential fields that the user copies out of Marketo's LaunchPoint and Munchkin admin pages. Screenshots or steps borrowed from the AEM MCP connector docs would be wrong here.
* Credential validation: Do not imply that the connection form validates the credentials. It saves them without testing them.
* Module scope: This is not a substitute for individual Marketo action modules. It is a single, flexible AI-driven module, not a set of deterministic single-purpose modules.
* Reliability: Results are AI-generated and can occasionally be imperfect, even with every safeguard above in place. This is appropriate for automation where a human is not reviewing every single run in real time, but it is not a guarantee of 100% deterministic behavior the way a traditional Marketo module is. This deserves extra emphasis for Marketo specifically, because a write action here can email real customers or alter real lead records.
* Tool restrictions: The read/write tool split limits what categories of Marketo actions the AI can take. It is not a way to sandbox or limit what the AI is capable of reasoning about or discussing in its answer text.
* Tool naming: Do not name specific Marketo MCP tools or actions unless they are verified against the live tool list. This document intentionally describes capability areas, such as leads, lists, campaigns, programs, emails, forms, snippets, and bulk operations, rather than exact tool names, since the server's exact tool set may evolve.
* API limits: Do not state Marketo API rate limits, quotas, or daily call caps as if this connector defines them. Any such limit comes from the user's own Marketo subscription and REST API allowance; verify with the Marketo team before publishing numbers.

## Reference links used while compiling this

* Adobe Marketo Engage MCP server (developer documentation):
  https://experienceleague.adobe.com/en/docs/marketo-developer/marketo/mcp-server

  -->
