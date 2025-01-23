---
title: OpenAI (ChatGPT)模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用OpenAIT(ChatGPT)的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: c8138d82-fa5a-4e69-b3cb-aa232099cb33
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 0%

---

# [!DNL OpenAI (ChatGPT & DALL-E)]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL OpenAI (ChatGPT & DALL-E)]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
  <td> <p>[!UICONTROL Pro] 或更高</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
   <td> <p>[!UICONTROL Plan]， [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td> <p>[!UICONTROL [!DNL Workfront Fusion] 用于工作自动化和集成] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## 先决条件

要使用[!DNL OpenAI (ChatGPT & DALL-E)]模块，您必须具有[!DNL OpenAI]帐户，包括API密钥和组织ID。

## OpenAI （ChatGPT和DALL-E） API信息

OpenAI （ChatGPT和DALL-E）连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.11.1</td> 
  </tr>
 </tbody> 
 </table>

## 正在将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]

您可以直接从[!DNL OpenAI (ChatGPT & DALL-E)]模块内部创建与[!DNL OpenAI (ChatGPT & DALL-E)]帐户的连接。

1. 在任意[!DNL OpenAI (ChatGPT & DALL-E)]模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 输入以下信息：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>输入新连接的名称。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td>您可以在OpenAI用户设置中找到API密钥。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Organization ID] </td> 
      <td>您可以在OpenAI的“组织设置”页面上找到您的组织ID。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。


## [!DNL OpenAI (ChatGPT & DALL-E)]模块及其字段

配置[!DNL OpenAI (ChatGPT & DALL-E)]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL OpenAI (ChatGPT & DALL-E)]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 创建完成

>[!IMPORTANT]
>
>此模块已弃用。

<!--

This action module creates a completion for the provided prompt or chat.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> Enter or map the ID of the model to use. You can use the Get models module to see all of your available models. </td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Temperature]</td> 
   <td> This value must be between 0 and 2, and determines the randomness of the output. Higher values produce output that is more random, while lower values produce more focused output. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating completions in the <a href="https://platform.openai.com/docs/api-reference/completions/create" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### 创建审核

此操作模块确定文本是否违反OpenAI的内容策略。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL OpenAI (ChatGPT & DALL-E)]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> 对于要包含的每个文本示例，单击<b>添加项</b>并输入或映射文本。 包括整个文本示例。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> 输入或映射要使用的模型的ID。 您可以使用“获取模型”模块查看所有可用模型。 </td> 
  </tr> 
 </tbody> 
</table>

### 创建编辑

按照说明操作，此操作模块会返回您提供的提示的编辑版本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL OpenAI (ChatGPT & DALL-E)]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> 输入或映射要使用的模型的ID。 您可以使用“获取模型”模块查看所有可用模型。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input]</td> 
   <td> 输入或映射要编辑的文本。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Instruction]</td> 
   <td> 输入或映射编辑的说明。 示例：“修复拼写错误。” </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>有关此模块中可选高级设置的信息，请参阅<a href="https://platform.openai.com/docs/api-reference/edits/create" class="MCXref xref">OpenAI API文档</a>中有关创建编辑的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 创建嵌入

此操作模块创建一个表示输入文本的嵌入矢量。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL OpenAI (ChatGPT & DALL-E)]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> 输入或映射要使用的模型的ID。 您可以使用“获取模型”模块查看所有可用模型。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Input text to embed]</td> 
   <td> 输入或映射要嵌入的文本。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User ID]</td> 
   <td> 输入或映射表示最终用户的唯一标识符，这可以帮助OpenAI监控和检测滥用 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> 输入或映射每个方案执行周期中您希望模块使用的最大编辑次数。</td> 
  </tr> 
 </tbody> 
</table>

### 创建聊天完成

给定描述对话的消息列表，此操作模块将返回响应。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL OpenAI (ChatGPT & DALL-E)]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model]</td> 
   <td> 输入或映射要使用的模型的ID。 您可以使用“获取模型”模块查看所有可用模型。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>目前为止，消息描述了对话情况。 对于每个要添加的消息，单击<b>添加项</b>并填写以下内容：
   <ul>
   <li> <b>角色</b>：选择此消息的作者角色。</li>
   <li> <b>内容</b>：输入或映射此邮件的内容。</li>
   <li> <b>名称</b>：输入或映射此邮件的作者姓名。 名称可以包含大写和小写字母、数字和下划线。 名称的最大长度为64个字符。</li>
   </ul>
    </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>有关此模块中可选高级设置的信息，请参阅<a href="https://platform.openai.com/docs/api-reference/chat/create" class="MCXref xref">OpenAI API文档</a>中有关创建聊天完成的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Edit image

This action module makes edits or creates variations of existing images.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to create edits or variations of the image.
   <p>NOTE: Images must be a valid PNG file, less than 4MB, and square. If mask is not provided, the image must have transparency, which will be used as the mask.</p> 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Text description of desired image]</td> 
   <td> <p>If editing an image, enter or map a description of the edits you want to create. Maximum length is 1000 characters.</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating image edits or variations in the <a href="https://platform.openai.com/docs/api-reference/images/createEdit" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->

### 生成图像

此操作模块使用Dall-E模型生成或处理图像。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL OpenAI (ChatGPT & DALL-E)]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text description of the desire image]</td> 
   <td> 输入或映射所需图像的描述。 最大描述长度为1000个字符。 
 </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>有关此模块中可选高级设置的信息，请参阅<a href="https://platform.openai.com/docs/api-reference/images/create" class="MCXref xref">OpenAI API文档</a>中有关创建图像的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 获取模型

本模块列出并描述了OpenAI API中可用的各种模型。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL OpenAI (ChatGPT & DALL-E)]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> 选择是要获取所有模型的列表还是检索特定模型。
    <ul>
    <li><p><b>列出模型 </b></p><p>此操作列出当前可用的模型，并提供有关每个模型的基本信息，如所有者和可用性。</p></li>
    <li><p><b>检索模型 </b></p><p>输入或映射要检索的模型的ID。 </p></li>
   </ul>
 </td> 
  </tr>
 </tbody> 
</table>

### 进行自定义API调用

此操作模块向OpenAI API发出自定义HTTP请求。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL OpenAI (ChatGPT & DALL-E)]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>输入相对于<code>https://api.openai.com/v1/</code>的路径 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

<!--

### Manage Audio

This action modules converts audio to text.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your [!DNL OpenAI (ChatGPT & DALL-E)] account to Workfront Fusion, see <a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">Connecting [!DNL OpenAI (ChatGPT & DALL-E)] to [!DNL Workfront Fusion]</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> Select whether you want to transcribe the audio into the input language, or into English.
   <p>If transcribing into the input language, you can select the language in this module's advanced settings. </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Select a source file from a previous module, or map the source file's name and data.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> Enter or map the maximum number of edits you want the module to work with during each scenario execution cycle.</td> 
   <tr> 
   <td role="rowheader">[!UICONTROL Advanced settings]</td> 
   <td> <p>For information about the optional advanced settings in this module, see the information about creating transcriptions in the <a href="https://platform.openai.com/docs/api-reference/audio/createTranscription" class="MCXref xref">OpenAI API documentation</a>.</p> </td> 
  </tr> 
  </tr> 
 </tbody> 
</table>

-->

### 管理文件

此操作模块可列出、删除或检索文件或文件内容。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL OpenAI (ChatGPT & DALL-E)]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td> 选择要执行的操作。 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> 如果要删除文件，或者检索文件或文件内容，请输入或映射文件的ID。 
  </tr> 
</tbody>
</table>

### 管理微调

管理微调作业，根据您的特定培训数据定制模型。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL OpenAI (ChatGPT & DALL-E)]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connecting-openaichatgpt-to-workfront-fusion" class="MCXref xref">将[!DNL OpenAI (ChatGPT & DALL-E)]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select the operation]</td> 
   <td> 选择要执行的操作。
   <ul>
   <li><p>从数据集中微调模型</p><p>输入或映射所需图像的描述。</p>
     <li><p>获取有关微调作业的信息</p><p>输入或映射作业的ID。</p>
   <li><p>取消微调作业</p><p>输入或映射作业的ID。</p>
   <li><p>取消微调作业</p><p>输入或映射作业的ID。</p>
   <li><p>获取微调作业的状态更新</p><p>输入或映射作业的ID，然后选择是否要流式传输这些更新。</p>
   <li><p>删除微调模型</p><p>输入或映射要删除的模型的ID。</p>
 </ul> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td> 如果要删除文件，或者检索文件或文件内容，请输入或映射文件的ID。 
  </tr> 
</tbody>
