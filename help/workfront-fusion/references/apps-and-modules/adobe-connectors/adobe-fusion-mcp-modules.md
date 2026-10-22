---
title: Adobe Fusion MCP模块
description: 使用Adobe Fusion MCP模块，您可以向Adobe Fusion的MCP服务器发送简单的英语提示，并让AI模型执行该请求。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 06ba1c54288fff09f866bffa5c3fce7381c71ad2
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 14%
---
# Adobe Fusion MCP模块

Adobe Fusion MCP连接器向Adobe Fusion模型上下文协议(MCP)服务器发送一个纯英语提示。 AI模型解释您的请求并调用完成请求所需的Fusion工具。

该连接器仅适用于托管的Adobe Fusion MCP服务器。 不能将其指向其他MCP服务器。

有关Fusion场景中MCP的详细信息，请参阅[向场景添加AI提示](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md)。

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
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 将Adobe Fusion MCP连接到Workfront Fusion

您可以直接从Adobe Fusion MCP模块内部创建连接。

1. 在Adobe Fusion MCP模块中，单击&#x200B;**连接**&#x200B;字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 填写以下字段：

   <table style="table-layout:auto">
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">连接名称</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">环境</td>
        <td>
          <p>选择您要连接到生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">类型</td>
        <td>
          <p>选择连接服务帐户还是个人帐户。</p>
        </td>
      </tr>
    </tbody>
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**。

您将被重定向到Adobe的登录页面。 使用您的Adobe帐户登录并批准访问权限。 系统会将您重定向回Workfront Fusion，并且新连接将在模块中可用。

## Adobe Fusion MCP模块及其字段

### 处理用户提示

此操作模块向Adobe Fusion MCP服务器发送一个纯英文提示。 AI模型解释提示，调用完成提示所需的Fusion工具并返回结果。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>LLM键<i>（可选，高级）</i></td> 
   <td> <p>默认情况下，此模块使用Adobe托管人工智能处理您的提示，您无需选择键。</p> <p>若要改用您自己的AI提供程序，请选择一个现有的LLM密钥，或通过单击<b>添加</b>并输入以下信息创建一个新密钥：</p>
     <ul>
       <li><b>密钥名称</b>：输入新密钥的名称。</li>
       <li><b>LLM</b>：选择与此键关联的大型语言模型。 支持的提供商包括OpenAI、Anthropic和Amazon Bedrock。</li>
       <li><b>密钥</b>：输入或映射所选提供商的API密钥。</li>
       <li><b>模型</b>：选择键将使用的LLM模型。</li>
       <li><b>其他字段</b>：为LLM所需的任何其他字段输入值。</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将Adobe Fusion MCP连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-fusion-mcp-to-workfront-fusion" class="MCXref xref">将Adobe Fusion MCP连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>只读工具<i>（可选）</i></td> 
   <td> <p>选择特定的只读工具以限制AI。 如果未选择任何工具，则允许此类别中的所有只读工具。</p> </td> 
  </tr> 
  <tr> 
   <td>写入/删除工具<i>（可选）</i></td> 
   <td> <p>选择特定的写入或删除工具以限制AI。 如果未选择任何工具，则允许此类别中的所有写入和删除工具。</p> <p>为了确保无人参与场景从不执行破坏性操作，我们建议将此字段保留设置为有意的空选择，而不是将其保留为不受限制。</p> </td> 
  </tr> 
  <tr> 
   <td>输入提示</td> 
   <td> <p>以纯英语输入或映射您希望AI执行的指令。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 限制人工智能可调用的工具

您可以通过选择只读工具和写入/删除工具字段中的工具来限制AI可以调用的Fusion工具。

* 如果将字段留空，则AI可以调用该类别中的每个工具。
* 如果将这两个字段都留空，则AI可以调用Fusion MCP服务器上的每个工具。

要防止无人参与场景执行写入或删除操作，请在只读工具字段仅选择您要允许的工具，并在您熟悉AI调用的写入/删除工具字段中选择至少一个工具。

列表中的工具名称来自Fusion MCP服务器。

#### 模块如何处理您的提示

* 模块没有跟进。 如果你的提示不明确，AI会做出合理的假设，并在回应中予以说明，而不是问你一个问题。
* AI验证可通过使用工具更改的信息。
* 除了您的提示请求之外，AI不会执行任何写入或删除操作。
* 模块需要有效的连接。 没有一个人是行不通的。

#### 输出

模块会返回以下信息，您可以在场景中的后续模块中映射这些信息：

* **响应**： AI的最终答案，以文本形式显示。
* **审核记录**：会话的记录，包括调用的工具、它们的参数和结果以及计时。
* **摘要**：会话的总数，包括成功的工具调用数和最终状态。
