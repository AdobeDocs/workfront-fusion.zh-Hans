---
title: 模型上下文协议(MCP)模块
description: 模型上下文协议(MCP)模块允许您使用MCP处理用户提示。
author: Becky
feature: Workfront Fusion
source-git-commit: d8ae176db714d2b9f041b74a62e8276171745c4b
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---

# 模型上下文协议(MCP)模块

模型上下文协议(Model Context Protocol，MCP)是一种将AI语言模型与其他应用程序安全连接的方法。 您可以配置MCP服务器，以允许AI模型访问应用程序。 然后，您可以向AI模型发送提示，它可以从应用程序返回信息。

例如，您可以配置MCP服务器将AI模型与Gmail连接。 当您发送提示“Give my last 5 emails from Gmail”时，它可以访问您的Gmail并返回电子邮件。

模型上下文协议(MCP)模块允许您使用语言模型和MCP服务器处理用户提示。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求</p>
   <p>或</p>
   <p>旧版：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 模型上下文协议模块及其字段

配置MCP模块时，[!DNL Adobe Workfront Fusion]显示下面列出的字段。 模块中的粗体标题表示必填字段。

### 进程用户提示

该操作模块使用您指定的语言模型和MCP服务器来处理提示。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL大语言模型(LLM)键]</td> 
   <td> <p>输入或映射要用于此提示的大型语言模型的API密钥。 </p> <p>目前，仅支持Anthropic API密钥。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL MCP服务器]</td> 
   <td> <p>对于要用于此提示的每个MCP服务器，单击<b>添加项</b>并输入服务器的名称和主机。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入提示]</td> 
   <td> <p>输入或映射大语言模型的提示。 </p> </td> 
  </tr> 
 </tbody> 
</table>
