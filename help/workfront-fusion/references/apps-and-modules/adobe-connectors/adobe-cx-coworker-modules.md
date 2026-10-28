---
title: Adobe CX Enterprise Coworker模块
description: 使用Adobe Workfront Fusion中的Adobe CX Enterprise Coworker连接器向同事发送自然语言提示，并在场景中使用其响应。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 6efe84af0487893a3c33ba2bf6e3db5200f25446
workflow-type: tm+mt
source-wordcount: '1974'
ht-degree: 6%
---
# Adobe CX Enterprise Coworker模块

使用Adobe Workfront Fusion中的Adobe CX Enterprise Coworker连接器向同事发送自然语言提示，并在场景中使用其响应。 同事将解释您的请求，并且可以使用您帐户可用的工具来开展工作。

连接器提供两个模块：

* **[!UICONTROL 运行提示]**&#x200B;会启动新请求，默认情况下会等待结果。
* **[!UICONTROL 获取执行状态]**&#x200B;检查您之前启动的请求。

## 访问权限要求

<!-- BECKY CHECK ME: This table is copied from other Fusion connector articles. The source material does not list access requirements, but says you need an Adobe account that has access to Coworker. Confirm the requirements and whether Coworker needs its own license or entitlement. -->

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

## 先决条件

您必须拥有有权访问Adobe CX Enterprise Coworker的Adobe帐户。

## 将Adobe CX Enterprise Coworker连接到Workfront Fusion

使用Adobe帐户登录，该帐户有权访问同事以及您的请求所需的任何服务。

要创建连接，请执行以下操作：

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
      <tr>
        <td role="rowheader">客户端 ID</td>
        <td>
          <p>输入或映射此连接的可选覆盖。 否则，请使用此帐户类型的平台管理的clientId。 为专用的Co-worker帐户注册显示的Fusion回调URL。</p>
        </td>
      <tr>
        <td role="rowheader">客户端密码</td>
        <td>
          <p>输入或映射此连接的可选覆盖。 否则，使用此帐户类型的平台管理的clientSecret。 使用为配置的IMS环境颁发的凭据。</p>
        </td>
    </tbody>
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**。

如果您无法登录或使用所需的服务，请与您的管理员联系。

## Adobe CX Enterprise Coworker模块及其字段

>[!WARNING]
>
>切勿在提示中包含密码或其他凭据。

### 获取执行状态

此操作模块检查&#x200B;**[!UICONTROL 启动的任务当前状态。运行提示符]**。

此模块检查任务一次。 在任务完成之前，它不会启动新任务或持续检查。 如果结果仍在等待，请稍后再次检查。

>[!NOTE]
>
>请勿将任务ID转换为数字、对其舍入或重新格式化。 如果同事在没有任务ID的情况下立即应答了原始提示，则无需检查状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Include原始结果] <i>（可选，高级）</i></td> 
   <td> <p>此选项默认处于关闭状态。 在输出中包含完整的同事响应。 响应可能包含敏感信息。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>选择您在原始<b>[！UICONTROL运行提示]</b>执行中使用的相同连接。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL任务ID]</td> 
   <td> <p>映射<b>[！UICONTROL返回的任务ID运行提示]</b>。 与返回的内容完全相同，保留为文本。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 运行提示

该操作模块会向同事发送指令，例如总结文本或使用帐户可用的工具收集信息。

每次运行都会发送一次提示，并开始新的对话。 您无需选择AI模型或提供单独的AI提供程序密钥。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 连接]</td> 
   <td> <p>选择您的同事连接。 有关说明，请参阅本文中的<a href="#connect-adobe-cx-coworker-to-workfront-fusion" class="MCXref xref">将Adobe CX Enterprise Coworker连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL用户提示]</td> 
   <td> <p>输入您的说明。 您可以使用早期模块中的多行并映射信息。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL等待完成] <i>（可选，高级）</i></td> 
   <td> <p>此选项默认处于打开状态。 如果希望模块等待任务完成或需要注意，请启用此选项。 将其关闭以立即返回初始结果。</p><p>有关详细信息，请参阅本文中的<a href="#wait-for-completion">等待完成</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Include原始结果] <i>（可选，高级）</i></td> 
   <td> <p>此选项默认处于关闭状态。 如果您希望模块在输出中包含完整的同事响应，请启用此选项。 响应可能包含敏感信息。</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
> 除非出于特定目的需要完整响应，否则我们建议将&#x200B;**[!UICONTROL Include Raw result]**&#x200B;保留为关闭。 原始结果可能包含敏感信息，不能保证它们包含每个操作的完整记录。 在保存、共享原始结果或将其传递到其他服务之前，查看它包含的内容。

#### 等待完成

当&#x200B;**[!UICONTROL 等待完成]**&#x200B;处于打开状态时，模块会在五秒钟的等待之后检查任务。 如果任务仍在等待处理，模块将再等待五秒钟，然后再次检查。 每次检查都需要一段时间才能收到响应。 检查状态时不再发送提示。

当任务完成、失败、被取消或拒绝，或者需要您的输入或授权时，等待将停止。 如果Co-worker提供了立即的答案，则模块会返回该答案，而无需进一步检查。

当&#x200B;**[!UICONTROL 等待完成]**&#x200B;关闭时，模块返回第一个结果而不等待任务完成。 检查&#x200B;**[!UICONTROL 状态]**、**[!UICONTROL 已完成]**&#x200B;和&#x200B;**[!UICONTROL 需要注意]**&#x200B;以决定下一步要做什么。 当第一个结果到达时，任务可能已经完成。

等待受Fusion的模块超时限制。 如果模块超时或停止，则同事可以继续工作。 在这种情况下，您可能无法收到输出或任务ID。

若要完成更多工作，请关闭等待并保存初始&#x200B;**[!UICONTROL 任务ID]**，以便您稍后查看任务。 超时后不要再次自动运行提示。 第一个请求可能已在进行中，重复它可能会重复更改。


## 模块输出

两个模块均会在完成时返回以下信息，并且不会出现错误。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL任务ID]</td> 
   <td> <p>标识任务。 当同事提供即时答案而不创建任务时，此项为空。 将此值与<b>[！UICONTROL Get Execution Status]</b>一起使用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL上下文ID]</td> 
   <td> <p>标识对话。 它不是继续对话的输入。</p><p>有关详细信息，请参阅本文中的<a href="#use-previous-answers">使用以前的答案</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 状态]</td> 
   <td> <p>当前任务状态。 请参阅本文中的<a href="#task-states" class="MCXref xref">任务状态</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL已完成]</td> 
   <td> <p>当任务完成或同事提供即时答案时为True。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL需要注意]</td> 
   <td> <p>当同事需要输入或授权时为True。</p><p>有关详细信息，请参阅本文中的<a href="#requests-that-need-attention">需要注意的请求</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL最终助理文本]</td> 
   <td> <p>任务完成时的最终答案。 当任务处于待处理状态或需要注意时，此项为空。 已完成的响应也可能没有应答文本。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文本构件（可能包括中间文本）]</td> 
   <td> <p>工作期间返回的文本。 每个项目都可以包括工件ID、名称和文本。 这些项目不一定是最终答案。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL原始结果（选择加入）]</td> 
   <td> <p>完整响应。 仅当<b>[！UICONTROL Include Raw result]</b>处于打开状态时，才会包含此项。</p> </td> 
  </tr> 
 </tbody> 
</table>

使用&#x200B;**[!UICONTROL 最终助理文本]**&#x200B;作为答案，而不是组合所有文本项目。 工件可以包括进度描述或其他中间文本。

### 需要注意的请求

同事可能需要更多信息或授权才能继续。 发生此情况时，**[!UICONTROL 需要注意]**&#x200B;为true，**[!UICONTROL 已完成]**&#x200B;为false。 将结果路由到人，而不是将其视为已完成的工作。

这些模块无法回答后续问题或代表您批准操作。 **[!UICONTROL 获取执行状态]**&#x200B;可以检查任务状态是否已更改，但无法解析输入或授权请求。

### 使用上一个答案

每&#x200B;**[!UICONTROL 运行一次Prompt]**&#x200B;执行会启动一个新对话。 要引用之前的答案，请将相关问题和答案作为文本包含在新的提示中。 这提供了同事的上下文，但不会恢复上一个对话。

**[!UICONTROL 上下文ID]**&#x200B;标识与结果关联的对话。 您无法将其提供给这些模块以继续对话。

>[!IMPORTANT]
>
>**[!UICONTROL 已完成]**&#x200B;不保证请求的业务操作成功。 例如，Co-worker可能会通过说明所需的工具不可用来完成操作。 查看答案并验证任何所需的结果，然后再执行下一个操作。

### 任务状态

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"><code>submitted</code>, <code>working</code></td> 
   <td> <p>任务待处理。 <b>[！UICONTROL已完成]</b>为false。 <b>[！UICONTROL运行提示]</b>在等待时继续等待。 否则，请保存任务ID并稍后检查。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>completed</code></td> 
   <td> <p><b>[！UICONTROL已完成]</b>为true。 查看<b>[！UICONTROL最终助理文本]</b>和预期的结果。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>input-required</code>, <code>auth-required</code></td> 
   <td> <p>这个任务需要注意。 <b>[！UICONTROL已完成]</b>为false，<b>[！UICONTROL需要注意]</b>为true。 等待停止。 将结果传送给人工审核。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"><code>failed</code>, <code>canceled</code>, <code>rejected</code></td> 
   <td> <p>模块报告错误，而不是正常结果。</p> </td> 
  </tr> 
 </tbody> 
</table>

即使模块返回时没有出现错误，挂起的结果或需要注意的结果也不是成功完成的结果。

## 示例

### 汇总更新

1. 添加&#x200B;**[!UICONTROL 运行提示]**&#x200B;并选择您的连接。
1. 在&#x200B;**[!UICONTROL 用户提示]**&#x200B;字段中输入以下内容：

   ```text
   Summarize the following project update in three bullet points.
   Use only the supplied text; do not call tools or change any records.
   
   The planning workshop is complete. Two dependencies need confirmation.
   The team will review the delivery estimate on Friday.
   ```

1. 将&#x200B;**[!UICONTROL 等待完成]**&#x200B;保留为开启，并关闭&#x200B;**[!UICONTROL 包含原始结果]**。
1. 如果&#x200B;**[!UICONTROL 需要注意]**&#x200B;为true，则将结果路由给人工审核。 如果&#x200B;**[!UICONTROL 已完成]**&#x200B;为true，请将&#x200B;**[!UICONTROL 最终助理文本]**&#x200B;映射到您的下一步。

人工智能生成的措辞可能有所不同。 在准确性很重要的地方审查结果。

### 稍后检查较长的任务

1. 添加&#x200B;**[!UICONTROL 运行提示符]**，选择您的连接，然后输入指令。
1. 关闭&#x200B;**[!UICONTROL 等待完成]**。
1. 检查初始结果。

   * 如果任务已完成，则处理结果。
   * 如果任务需要引起注意，请将结果传送以供审查。
   * 如果任务处于挂起状态，请将&#x200B;**[!UICONTROL 任务ID]**&#x200B;保存为文本并记下您使用的连接。

1. 稍后，对该连接和任务ID使用&#x200B;**[!UICONTROL 获取执行状态]**。
1. 如果任务仍在等待处理，请在场景的限制内安排另一次检查。 完成时处理一次结果，并单独处理注意事项或错误。

不要再次运行原始提示只是为了检查其进度。

## 使用注意事项

* 同事可以使用您的帐户允许的工具并执行操作，包括对记录的更改。 使用受信任的提示和具有适当访问权限的帐户。
* 这些模块不提供限制单个工具的方法。 诸如“不更改任何内容”之类的说明描述了您的意图，但并非强制的只读模式。
* 可用的工具和技能因客户而异。 连接器不提供技能选择器或保证特定操作，例如创建历程或更新项目。 请勿假定需要批准的请求将在无人参与的情况下完成。
* 连接器将启动并检查同事请求。 它不会监视项目更改或自动将答案保存到其他应用程序。 根据需要向方案添加适当的触发器、存储和后续模块。
* 人工智能生成的答案可能不完整或不准确。 在使用重要结果做出更改或决策之前验证这些结果。
* 连接器不会自动重试失败的请求。 确保场景的错误处理不会重复出现结果不确定的提示。

## 故障排除

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">缺少必填字段</td> 
   <td> <p>选择连接并输入所需的提示或任务ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">登录失败或访问被拒绝</td> 
   <td> <p>再次登录，然后检查您的Adobe帐户是否有权访问同事和所需的服务。 如有需要，请联系您的管理员。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">未找到任务</td> 
   <td> <p>检查任务ID是否保持不变，以及您是否正在使用原始连接。 新任务可能无法立即显示。 稍后检查状态，而不是再次发送提示。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">状态检查失败</td> 
   <td> <p>如果错误包括已接受的任务ID，请使用<b>[！UICONTROL Get Execution Status]</b>调查该任务。 不要自动重新启动提示。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">运行提示超时或失去响应</td> 
   <td> <p>即使您没有收到其ID，任务也可能已开始。 在重复请求之前进行调查，以避免重复工作。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Fusion等待时超时</td> 
   <td> <p>同事可能还在工作。 如果您有任务的ID，请检查该任务。 对于将来的长时间任务，请关闭等待功能，然后先保存初始ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">同事或所需服务不可用</td> 
   <td> <p>与管理员共享显示的错误，不含凭据或敏感结果内容。</p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- BECKY CHECK ME: Confirm the exact module and field labels in the UI (Run a Prompt, Get Execution Status, User prompt, Wait for completion, Include raw result, Task ID, and the output item names). Also confirm that the module is listed under "Adobe CX Enterprise Coworker" in the app picker. -->
