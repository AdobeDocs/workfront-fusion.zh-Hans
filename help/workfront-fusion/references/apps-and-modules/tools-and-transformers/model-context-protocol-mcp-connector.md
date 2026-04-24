---
title: 模型上下文协议(MCP)模块
description: 模型上下文协议(MCP)模块允许您使用MCP处理用户提示。
author: Becky
feature: Workfront Fusion
hide: true
exl-id: 748055ad-d305-4513-9a5c-9c970b74a96e
source-git-commit: 80f2d078cd624424f23bd007e852f49643fec7f3
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 18%

---

# MCP代理模块

<!--SET UP REDIRECTS-->

模型上下文协议(Model Context Protocol，MCP)是一种将AI语言模型与其他应用程序安全连接的方法。 您可以配置MCP服务器，以允许AI模型访问应用程序。 然后，您可以向AI模型发送提示，它可以从应用程序返回信息。

例如，您可以配置MCP服务器将AI模型与Gmail连接。 当您发送提示“Give my last 5 emails from Gmail”时，它可以访问您的Gmail并返回电子邮件。

模型上下文协议(MCP)模块允许您使用语言模型和MCP服务器处理用户提示。

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

## 先决条件

* 您必须已配置要连接的任何MCP服务器。
* 必须具有指向所选LLM（大语言模型）的LLM密钥。

## 模型上下文协议模块及其字段

### 进程用户提示

该操作模块使用您指定的语言模型和MCP服务器来处理提示。

>[!NOTE]
>
>此模块必须返回对象。 它不会返回字符串或数字等输出。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>LLM键</td> 
   <td> 选择现有的LLM密钥，或单击<b>添加</b>并输入以下信息以创建新密钥： 
     <ul>
       <li><b>密钥名称</b>：输入新密钥的名称。</li>
       <li><b>LLM</b>：选择与此键关联的大型语言模型。</li>
       <li><b>密钥</b>：输入或映射选定模型的API密钥。</li>
       <li><b>模型</b>：选择键将使用的LLM模型。</li>
       <li><b>最大令牌数</b>：输入或映射LLM在其响应中可以生成的最大令牌数。<p>一个令牌通常等于四个字符，或者一个英文单词的0.75。 “Hello world”将等于两个令牌，“Authentication”将等于一到两个令牌。</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>MCP服务器</td> 
   <td> <p>对于要连接的每个MCP服务器，单击<b>添加</b>并输入以下信息： </p> 
     <ul>
       <li><b>连接</b>：选择Fusion将用于连接到MCP服务器的连接。</li>
       <li><b>MCP服务器主机</b>：输入MCP服务器的URL。</li>
       <li><b>MCP服务器名称</b>：输入或映射此MCP服务器的名称。</li>
       <li><b>标头</b>：添加任何适用的标头。</li>
       <li><b>MCP服务器类型</b>：选择服务器类型。</li>
      </ul>
    </td> 
  </tr> 
  <tr> 
   <td>输入提示 </td> 
   <td> <p>输入或映射要处理的提示。</p> </td> 
  </tr> 
 </tbody> 
</table>


