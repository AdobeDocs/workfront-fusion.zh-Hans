---
title: Adobe Firefly Creative生产MCP模块
description: 使用Adobe Firefly Creative生产MCP模块，您可以从Workfront Fusion场景发送自然语言提示，并让AI模型使用您选择的Firefly Creative生产工具。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: ee2719b9b3452b9203f2d0f4a550c87ff8a3b433
workflow-type: tm+mt
source-wordcount: '2087'
ht-degree: 5%
---
# Adobe Firefly Creative生产MCP模块

使用Adobe Workfront Fusion中的Adobe Firefly Creative Production MCP连接器，通过Firefly Creative Production tools处理自然语言请求。

连接器会发现通过连接的Firefly模型上下文协议(MCP)服务器可用的工具。 您可以选择模块可用于请求的工具。 根据Adobe帐户可用的工具以及在模块中选择的工具，请求可以执行以下操作：

* 发现工作流和操作。
* 编写并验证工作流。
* 提交运行并检查其进度。
* 检索输出URL。
* 当服务器的工具支持时，保存可编辑的工作流草稿。

此连接器面向Firefly Creative生产环境。 它不是Firefly主板连接器，也不是每个Creative Cloud应用程序的常规连接器。

有关Fusion场景中MCP的详细信息，请参阅[向场景添加AI提示](/help/workfront-fusion/create-scenarios/add-modules/add-an-ai-prompt-to-your-scenario.md)。

<!-- BECKY CHECK ME: The request asks you to confirm the customer-facing name of the connector, its beta or release status, its availability, its access requirements, and screenshots with the product and engineering owners before publication. Confirm each item, and add a beta note at the top of the article if the connector is released as a beta. -->

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
   <p>您还必须具有Adobe Firefly Creative生产访问权限，如本文中<a href="#prerequisites">先决条件</a>中所述。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 先决条件

在使用Adobe Firefly Creative生产MCP模块之前，您必须具备以下条件：

* 在启用此连接器的环境中访问Adobe Workfront Fusion。
* 具有所请求操作所需的Firefly Creative生产访问权限的Adobe帐户。
* 运行工作流所需的任何积分或权利。
* 由Fusion管理员配置的Adobe托管AI访问权限，或者您在模块的高级设置中选择的受支持LLM密钥。

Firefly授权和LLM凭据有不同的用途。 选择LLM键不会授予对Firefly工具的访问权限。

## 将Adobe Firefly Creative Production MCP连接到Workfront Fusion

1. 将&#x200B;**[!UICONTROL Adobe Firefly Creative Production MCP]** > **[!UICONTROL 处理用户提示]**&#x200B;添加到您的方案。
1. 单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 在&#x200B;**[!UICONTROL 创建连接]**&#x200B;窗口中，填写以下字段：

   <table style="table-layout:auto">
    <col>
    <col>
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
          <p>Select（无论您是连接到生产环境还是非生产环境）。</p>
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
1. 遵循授权流程，使用相应的Adobe帐户登录，并授权访问。
1. 返回到模块并查看为连接加载的工具。

Workfront Fusion处理OAuth客户端注册和令牌管理。 您不输入访问令牌、客户端ID、客户端密钥或API密钥。 您的管理员必须完成此流的设置，然后才能连接。

如果授权失败或看不到所需的工具，请与管理员确认您的访问权限和环境的配置。

<!-- BECKY CHECK ME: The Environment and Type fields are described the same way as in the Adobe Fusion MCP connection. The screenshot shows only the selected values (Production and Service account). Confirm the available options for each field, and whether a personal account is supported. -->

## Adobe Firefly Creative生产MCP模块及其字段

### 处理用户提示

此操作模块使用您允许的选定LLM和Firefly Creative生产工具处理您的提示。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL LLM键] <i>（可选，高级）</i></td> 
   <td> <p>将此字段留空以使用Fusion管理员配置的Adobe托管AI。 若要改用您自己的密钥，请选择一个现有的OpenAI、Anthropic或Amazon Bedrock密钥，或单击<b>[!UICONTROL 添加]</b>创建一个密钥。</p><p>您的Firefly登录与LLM凭据不同。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>模块用于发现和调用工具的Adobe Firefly Creative生产连接。 有关说明，请参阅本文中的<a href="#connect-adobe-firefly-creative-production-mcp-to-workfront-fusion" class="MCXref xref">将Adobe Firefly Creative生产MCP连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 只读工具] <i>（可选）</i></td> 
   <td> <p>Select服务器标识为只读的工具。 要选择当前列出的每个工具，请选择<b>Select全部</b>。</p><p>列出的工具数会显示在字段的标签中。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 写入/删除工具] <i>（可选）</i></td> 
   <td> <p>Select服务器未标识为只读的工具。 这些操作可以更改数据或运行工作流。 要选择当前列出的每个工具，请选择<b>Select全部</b>。</p><p>列出的工具数会显示在字段的标签中。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 其他工具（未知权限）] <i>（可选）</i></td> 
   <td> <p>Select工具没有可识别的只读注释。 仅当此类工具可用时，才会显示此字段。 在启用这些工具之前，请查看其行为方式。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 输入提示]</td> 
   <td> <p>描述所需的工作流发现、构成或执行。 最大长度为10,000个JavaScript字符串单位。 有些字符（包括许多表情符号）被计为两个单位。</p><p>在需要时显式请求执行或发布。 运行工作流可能会冲减积分。 异步运行可能会在运行完成之前返回批次ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

选择&#x200B;**[!UICONTROL 显示高级设置]**&#x200B;时，将显示&#x200B;**[!UICONTROL LLM键]**&#x200B;字段。

<!-- BECKY CHECK ME: The screenshot does not show the Other tools (unknown permissions) field, because it appears only when the server returns tools without a read-only annotation. Confirm its label, and confirm the order of the fields. Also confirm that the tool lists are not required. -->

工具列表因服务器的可用性和帐户的访问权限而异。 工具数量会显示在每个选择器的标签中。

#### Select此模块可以使用的工具

* 模块只能使用您选择的工具。
* 如果将某个类别留空，则模块将无法使用该类别中的工具。
* 如果您将所有类别都留空，则模块无需任何工具即可处理提示。 它无法访问每个工具。
* **[!UICONTROL Select all]**&#x200B;选择当前在该类别中列出的所有工具。 它不会自动包含稍后添加的工具。
* 如果选定的工具不可用或移动到其他类别，请再次打开模块并查看您的选择。

>[!NOTE]
>
>服务器的注释有助于对工具进行分类，但它们不保证权限。 仅启用场景所需的工具。

#### 输出

模块在&#x200B;**[!UICONTROL 数据]**&#x200B;下返回以下信息。 您可以在场景中的后续模块中映射它。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 响应] (<code>data.response</code>)</td> 
   <td> <p>最终文本响应。 其内容取决于提示和工具结果。 不保证为URL或结构化JSON。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 审核跟踪] (<code>data.auditTrail</code>)</td> 
   <td> <p>有关如何处理提示和工具调用的详细信息，包括其参数、结果、时间和成功信息。 根据您组织的数据处理要求处理这些详细信息。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 摘要] (<code>data.summary</code>)</td> 
   <td> <p>工具调用的次数、处理时间和执行状态。 查看摘要、响应和审核跟踪，包括任何<code>partial_success</code>结果。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL LLM用法] (<code>data.usage</code>)</td> 
   <td> <p>可选。 观察到LLM响应中的令牌总使用量。 这不是Firefly服务器中的提供商计费、Firefly信用消耗或Fusion无法观察的LLM活动。</p> </td> 
  </tr> 
 </tbody> 
</table>

##### LLM使用情况字段

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td><code>status</code></td> 
   <td> <p>下列选项之一：</p><ul><li><code>complete</code>：所有主令牌计数涵盖每个观察到的请求。</li><li><code>partial</code>：缺少某些使用情况信息。</li><li><code>unavailable</code>：发现了请求，但未报告任何可用的使用情况。</li><li><code>not_applicable</code>：未观察到任何LLM请求。</li></ul> </td> 
  </tr> 
  <tr> 
   <td><code>llmRequests</code></td> 
   <td> <p>运行时观察到的LLM请求数。</p> </td> 
  </tr> 
  <tr> 
   <td><code>requestsWithUsage</code></td> 
   <td> <p>观察到的具有可用令牌使用情况信息的请求数。</p> </td> 
  </tr> 
  <tr> 
   <td><code>inputTokens</code>, <code>outputTokens</code>, <code>totalTokens</code></td> 
   <td> <p>总计数。 如果任何观察到的请求未报告该计数，或者没有观察到的请求，则每个计数为<code>null</code>。 报告的零保持为零。</p> </td> 
  </tr> 
  <tr> 
   <td><code>cacheReadInputTokens</code>, <code>cacheWriteInputTokens</code></td> 
   <td> <p>缓存令牌的可选计数。 如果没有请求报告数字，则忽略这些字段。 如果只有某些请求报告了一个数字，则它们为<code>null</code>；如果每个请求都报告一个数字，则它们为数字。 请勿将这些计数添加到总计中。</p> </td> 
  </tr> 
 </tbody> 
</table>

当缓存字段为`null`时，主使用状态可以是`complete`。 使用状态与执行状态无关。 如果运行时不提供使用情况信息，则使用情况集合不存在，而不是显示零。

## 模块运行方式

* **某些操作是异步执行的。** 请求可以在输出可用之前返回批次ID。 对于较长的作业，请使用单独的运行来提交请求，并在稍后检查其状态，并在它们之间保存批次ID。 对于此设计，请勿依赖仅包含URL的响应。
* **错误生成模块错误。** 授权、验证和失败的运行时处理可能会产生模块错误，而不是输出捆绑包。 使用Fusion错误处理路由。
* **响应未证明成功。** 即使某些操作失败，模块仍会返回响应。 在依赖响应之前，请查看摘要、审核追踪和工具结果。
* **输出URL不是下载的文件。** 连接器会返回文本和工具结果，而不是二进制文件。 要将文件导入Fusion，请添加用于下载URL的HTTP模块。
* **运行工作流可以使用积分。** 图像生成和工作流执行可能会消耗积分。 确认适用于您帐户的使用和权利。 LLM令牌使用情况不是Firefly账单或信用报告。
* **提示指令不能保证单次运行。** 提示中的说明（例如仅提交一个批次）不能保证请求只被处理一次。 控制场景中的重试和重复请求。
* **处理具有限制。** 除了场景的执行限制之外，处理还具有工具、迭代和输出长度限制。 请勿假定模块可不受限制地轮询。

## 示例

### 无需运行工作流即可发现工作流

Select提供发现工作流所需的只读工具，然后输入以下提示：

```text
List the Firefly Creative Production workflows available to my account.
Summarize what each workflow does and what inputs it requires.
Do not create, modify, submit, or publish anything.
```

### 请求一个图像

Select您编写或选择工作流、验证工作流、提交工作流、检查工作流进度和检索输出时需要使用的工具。 工具名称和可用性可能有所不同。 然后，输入如下所示的提示：

```text
Generate one photorealistic image of a black dog on a sunny windowsill.
Submit one generation batch only and check that same batch for completion
within the available execution limits. Do not publish or submit another
generation.

On success, return only the actual downloadable image URL as plain text,
without Markdown, quotes, labels, or explanation. Never invent a URL or
return a workflow or status-page URL instead.

If the run fails or times out, report the failure honestly instead of
returning a URL. Do not generate another image to recover.
```

### 通过Workfront任务更新生成图像

在此示例中，以`/firefly `开头的任务更新会触发图像生成。 Fusion会下载结果，将其上载到任务，并添加完成更新。

该场景使用以下流程： Workfront任务更新>命令过滤器>读取任务> Firefly MCP > HTTP下载> Workfront文档上传>完成更新。

1. 将&#x200B;**[!UICONTROL Workfront]** > **[!UICONTROL 观看活动]**&#x200B;添加到方案中。 为&#x200B;**[!UICONTROL Note]**&#x200B;记录类型、**[!UICONTROL 新状态]**&#x200B;事件和&#x200B;**[!UICONTROL 仅新记录]**&#x200B;配置它。
1. 添加要求`newState.noteText`以`/firefly `开头且`newState.taskID`非空的筛选器。
1. 添加使用`newState.taskID`读取任务的模块。
1. 添加&#x200B;**[!UICONTROL Adobe Firefly Creative生产MCP]** > **[!UICONTROL 处理用户提示]**&#x200B;模块。 传递请求和Firefly所需的任何任务上下文。 将映射文本视为请求的内容，而不是视为更改方案规则的权限。
1. 检查Firefly结果。 仅当生成成功并且响应是可下载图像的有效允许的URL时才继续。
1. 添加用于下载文件的HTTP模块。 请勿将您的Workfront凭据发送到资源主机。 验证预期的主机、内容类型和大小。
1. 使用原始`newState.taskID`添加一个模块，以便将下载的文件名和二进制数据上载到任务中。
1. 上传成功后，添加一个模块以在任务上创建完成更新。 不要用`/firefly`开始更新，因为筛选器将匹配它。

例如，用户向任务中添加以下更新：

```text
/firefly Generate one photorealistic image of a black dog on a sunny windowsill.
```

然后，请求者可以在任务的“文档”区域查看已上传的草稿。 用户应先查看图像，然后再发布任何内容。

对于生产使用，请使用原始注释的ID来保留每个请求，并具有适用于并发运行的重复保护。 保存已提交批次的ID，因此，重试或超时会恢复状态检查，而不是提交另一代。

<!-- BECKY CHECK ME: The example scenario is from the request's draft. Confirm the module names and field labels (Watch Events, Note, New state, New Record Only, and the task, document upload, and update modules) against the current Workfront connector, and add a screenshot of the scenario if one is available. -->

## 故障排除

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">工作流仍在运行</td> 
   <td> <p>有些创意操作是异步执行的。 对于较长的作业，请在一次运行中提交请求，并在以后的运行中检查状态。 在两次运行之间保存批次ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">模块报告错误</td> 
   <td> <p>授权、验证和失败的运行时处理可能会产生模块错误。 向场景添加Fusion错误处理路由。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">模块返回响应，但某些操作失败</td> 
   <td> <p>查看摘要、审核追踪和工具结果。 仅响应不会显示图像已生成或已上传。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">有一个URL，但Fusion中没有文件</td> 
   <td> <p>连接器不下载文件。 添加下载URL的HTTP模块。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">所选工具不可用</td> 
   <td> <p>打开模块，刷新可用的工具，然后更新您的选择。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">运行工作流所需的时间超过一个模块</td> 
   <td> <p>除了场景的执行限制之外，处理还具有工具、迭代和输出长度限制。 将工作拆分为多个运行，并保存批次ID。</p> </td> 
  </tr> 
 </tbody> 
</table>
