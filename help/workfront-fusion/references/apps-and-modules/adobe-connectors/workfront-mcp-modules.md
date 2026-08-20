---
title: Adobe Workfront MCP模块
description: 使用Adobe Workfront MCP模块，您可以向Adobe Workfront的MCP服务器发送纯英语提示，并让AI模型执行该请求。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 94492dbd382eee2f4e66e53d53a441ca82492bfb
workflow-type: tm+mt
source-wordcount: 841
ht-degree: 17%

---

# Adobe Workfront MCP模块

Adobe Workfront MCP连接器是Adobe Workfront自己的模型上下文协议(MCP)服务器的专用Fusion集成。 与典型连接器（每个模块执行一个固定操作）不同，此连接器具有一个接受开放式、纯英语指令并让AI模型决定需要哪些Workfront操作来完成它的模块。

例如，您可以输入提示“查找所有落后于计划的活动项目并总结其状态”，模块将返回合成答案，而不必将多个“获取”和“筛选”模块链接在一起。

您可以限制允许AI执行哪些Workfront操作，以便即使无人参与场景也可以保证不会执行任何意外的破坏性操作。

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
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 将Adobe Workfront MCP连接到Workfront Fusion

Adobe Workfront MCP连接器使用OAuth 2.0连接到Workfront。 与其他Workfront连接器不同，不需要填写手动连接字段，例如主机、客户端ID或客户端密钥。

要创建连接，请执行以下操作：

1. 在Adobe Workfront MCP模块中，单击连接字段旁边的&#x200B;**[!UICONTROL 添加]**。
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
          <p>输入此连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>选择您要连接到生产环境还是非生产环境。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>选择连接服务帐户还是个人帐户。</td>
      </tr>
    </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

   如果您尚未登录 Workfront，系统会将您引导至登录界面。 登录并批准访问权限。

系统会将您重定向回Workfront Fusion，并且新连接将在模块中可用。

>[!NOTE]
>
>首次使用时，该连接会自动向Workfront的MCP服务器注册自身，并会在您创建的每个后续连接中重复使用该注册。

## Adobe Workfront MCP模块及其字段

### 处理用户提示

该操作模块使用您指定的语言模型针对Workfront的MCP服务器处理一个简单的英语提示，并返回AI的答案。

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
  </tr>   <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-workfront-mcp-to-workfront-fusion" class="MCXref xref">将Adobe Workfront MCP连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>只读工具<i>（可选）</i></td> 
   <td> <p>限制允许AI调用哪些只读Workfront操作。 如果未选择工具，则允许使用所有只读工具。</p> </td> 
  </tr> 
  <tr> 
   <td>写入/删除工具<i>（可选）</i></td> 
   <td> <p>输入允许AI调用的写入或删除Workfront操作。 如果将此留空，则允许使用所有写入和删除工具。</p> <p>为了确保无人参与场景从不执行破坏性操作，我们建议将此字段保留设置为有意的空选择，而不是将其保留为不受限制。</p> </td> 
  </tr> 
  <tr> 
   <td>输入提示</td> 
   <td> <p>以纯英语输入或映射您希望AI执行的指令。</p> <p>示例：<i>查找分配给我的所有落后于计划的项目。</i></p> </td> 
  </tr>  </tbody> 
</table>

有关可以为只读工具和写入/删除工具字段选择的工具列表，请参阅Workfront文档中的[Adobe Workfront MCP服务器工具](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-tools)。

模块会返回以下信息，您可以在场景中的后续模块中映射这些信息：

* **响应**： AI的最终答案，以文本形式显示。
* **审核记录**：会话的记录，包括原始提示、开始和结束时间以及每次工具调用人工智能的详细信息，如工具名称、参数、是否成功、持续时间和输出。
* **摘要**：会话的总数，包括尝试的工具调用数、成功或失败的次数、总处理时间和总体状态。
