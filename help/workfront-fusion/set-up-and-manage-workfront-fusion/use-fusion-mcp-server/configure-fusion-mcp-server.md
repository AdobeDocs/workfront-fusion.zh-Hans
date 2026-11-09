---
title: 配置Adobe Workfront Fusion MCP服务器
description: 将Adobe Workfront Fusion连接到与MCP兼容的AI代理平台或Co-worker（独立或Fusion右边栏中）。
source-git-commit: d5861015b3bb0e9c176fcf4fd71db426671764dd
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 7%
---

# 配置Adobe Workfront Fusion MCP服务器

Adobe Workfront Fusion MCP服务器允许您在受支持的AI代理平台上通过自然语言对话处理Fusion组织的场景、执行、连接、Webhook、数据存储等。

有关Adobe Workfront Fusion MCP服务器中可用工具的列表，请参阅[Adobe Workfront Fusion MCP服务器工具](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-fusion-mcp-server/fusion-mcp-server-tools.md)。

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

## 先决条件

在将Fusion连接到AI代理平台之前，您必须：

* 拥有活动的Adobe Workfront Fusion许可证并访问至少一个Fusion组织。
* 拥有Fusion用户角色和团队角色，这些角色可授予对要处理的数据的访问权限。
* 使用Adobe ID (Adobe Identity Management System， IMS)登录。
* 有权访问与MCP兼容的AI代理平台，或访问合作者。

## 支持的MCP应用程序

Fusion MCP服务器可与以下应用程序配合使用。

**聊天应用程序**

* 克洛德
* OpenAI ChatGPT
* Microsoft 365 Copilot

**开发人员工具**

* 人工克劳德码
* 光标
* GitHub Copilot
* VS代码
* OpenAI代码
* MCP检查器、 mcp-remote和使用本地回调的其他工具

**自动化和AI平台**

* Adobe Workfront Fusion
* Google顶点AI 搜索
* Glean
* 作家AI Studio
* Postman

### 限制

* 只有此部分列出的应用程序可以连接到Fusion MCP服务器。
* 如果桌面应用程序和命令行界面(CLI)在您自己的计算机(`localhost`)上接收到登录回调，则它们可以正常工作。
* 您无法添加自己的应用程序。 要请求对新应用程序的支持，请通过[fusiondev@adobe.com](mailto:fusiondev@adobe.com)联系Fusion团队。

<!-- BECKY CHECK ME: Other parts of this article might conflict with these limitations. See the comments in the important note below, in the section Connect Fusion to a custom MCP solution, and in the troubleshooting table. -->

>[!NOTE]
>
> Adobe当前不在Claude连接器目录或ChatGPT应用程序/插件目录中发布Workfront Fusion连接器。 若要将Fusion与Claude、ChatGPT或Microsoft Copilot一起使用，请按照本文所述通过URL将其添加为&#x200B;**自定义MCP服务器**。

本文逐步介绍的连接步骤：

* [Adobe同事](#use-fusion-with-coworker)： Fusion右边栏中的同事作为独立同事和同事
* [Claude](#connect-fusion-to-claude)：自定义连接器
* [ChatGPT](#connect-fusion-to-chatgpt)：自定义MCP服务器
* [自定义MCP解决方案](#connect-fusion-to-a-custom-mcp-solution)

>[!IMPORTANT]
>
>如果您使用不同的MCP兼容平台，请按照该平台的文档添加自定义MCP服务器。 当系统提示输入MCP服务器URL时，请输入：
>
>```
>https://mcp.fusion.adobe.com/mcp
>```

## 将Fusion与同事一起使用

同事是Adobe的人工智能代理。 Fusion内置于协同工作中，因此您无需输入MCP URL或注册OAuth应用程序。 您可以在以下两个位置使用Fusion的协同工作：

* 同事（独立）：与其他Adobe应用程序一起使用Fusion。
* Fusion右边栏中的同事：在Fusion UI内的面板中打开同事。

两者都使用相同的Fusion MCP工具、Adobe ID和Fusion权限。 “Read（读取）”或“Write（写入）”MCP工具设置同时适用于这两者。 破坏性操作（如删除、清除队列或覆盖）始终需要确认。

### 在同事中使用Fusion

1. 打开同事。 您可以在https://experience.adobe.com/#/coworker上找到它。
1. 打开&#x200B;**自定义项** > **集成**
1. 搜索或找到&#x200B;**fusion-mcp**&#x200B;并单击它。
1. 在打开的窗口中，单击&#x200B;**测试**。
1. 如果您有权访问多个Fusion组织，则将自动选择该组织。 如有必要，您可以稍后要求同事切换组织。

### 在Fusion右边栏中使用同事

在Fusion中，将在右边栏中打开同事

1. 登录到Workfront Fusion。
1. 单击右边栏中的&#x200B;**同事**&#x200B;图标。
1. 在面板中提问。

### 示例提示

* *显示过去24小时内无法执行的所有方案。*
* *列出本周创建或删除的所有方案，按最近使用的方案排序。*
* *此方案在做什么？*
* *为什么此执行失败？*

## 将Fusion连接到Claude

将Fusion添加为自定义连接器。

>[!NOTE]
>
> 在Claude Team/Enterprise中，您必须是所有者才能添加自定义连接器。 有关信息，请参阅Claude文档中的[使用远程MCP的自定义连接器入门](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)。

1. 登录到[克劳德](https://claude.ai)。
1. 在左侧菜单中，选择&#x200B;**自定义**。
1. 选择&#x200B;**连接器**。
1. 选择&#x200B;**+**，然后选择&#x200B;**添加自定义连接器**。
1. 输入名称（例如“Workfront Fusion”）和MCP服务器URL：

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

1. 单击&#x200B;**连接**。
1. 登录。 选择配置文件和Fusion组织。

对于Claude Code ，可以从命令行添加服务器：

```
claude mcp add --transport http fusion-mcp https://mcp.fusion.adobe.com/mcp
```

## 将Fusion连接到ChatGPT

将Fusion添加为自定义MCP服务器。

### ChatGPT桌面或代码

1. 在ChatGPT中，打开&#x200B;**设置**。
1. 单击&#x200B;**插件**。
1. 单击&#x200B;**添加服务器**。
1. 输入服务器的名称。
1. 对于类型，选择&#x200B;**可流式处理HTTP**。
1. 输入MCP服务器URL：

   ```
   https://mcp.fusion.adobe.com/mcp
   ```

1. 单击&#x200B;**保存**。
1. 为新服务器单击&#x200B;**身份验证**&#x200B;并登录。
1. 确保打开了服务器旁边的切换开关。

### Web上的ChatGPT

1. 登录到[ChatGPT](https://chatgpt.com)。
1. 转到[https://chatgpt.com/plugins](https://chatgpt.com/plugins)。 （可能需要在&#x200B;**设置**&#x200B;下启用开发人员模式；在商业/企业计划中，管理员必须允许自定义连接器。）
1. 单击&#x200B;**+**。
1. 输入&#x200B;**名称**。
1. 对于&#x200B;**连接**，请选择&#x200B;**服务器URL**&#x200B;并输入MCP服务器URL。
1. 将&#x200B;**Authentication**&#x200B;保留设置为&#x200B;**OAuth**。
1. 阅读风险消息并选中复选框。
1. 单击&#x200B;**创建**，然后使用您的登录。

## 切换到其他Fusion组织

您无需断开连接即可更改组织。 Fusion MCP服务器可以在会话中切换活动组织：

* _我拥有哪些Fusion组织？_
* _切换到1234组织。_

代理使用`fusion_orgs_list`和`fusion_orgs_set`。 交换机仅适用于当前对话/会话。 位于不同数据中心区域（例如，美国和欧盟）的组织均可通过同一MCP URL访问。

## 设置和身份验证疑难解答

| 问题 | 可能的原因 | 修复 |
| --- | --- | --- |
| 在Claude或ChatGPT目录中找不到Fusion连接器。 | Adobe不发布用于Fusion的目录连接器。 | 使用本文中的URL将Fusion添加为自定义MCP服务器。 |
| 无法在Claude或ChatGPT中添加自定义连接器。 | 您的计划限制所有者或管理员可以使用自定义连接器。 | 请让您的Claude或ChatGPT管理员添加连接器或允许自定义MCP服务器。 |
| 您已连接，但未看到任何数据，或者数据有误。 | 错误的Fusion组织处于活动状态。 | 要求代理列出您的组织并切换到正确的组织。 |
| 身份验证失败或连接停止工作。 | 会话过期或连接错误。 | 断开并重新连接服务器。 |
| 您看到一条消息，指出MCP访问被禁用。 | 您的Fusion组织的MCP访问已关闭。 | 请咨询Fusion管理员以启用它。 |
| 代理可以读取方案，但不能创建、运行、更新或删除方案。 | 写入MCP工具已禁用，或者您的团队角色不允许使用它。 | 要求您的Fusion管理员启用编写工具，或授予您所需的团队角色。 |
| 自定义应用程序身份验证被拒绝。 | 回调URL不在授权列表中。 | 要求您的管理员添加精确的回调URL。 |
| Fusion未列在Co-worker中，或Fusion右边栏中缺少Co-worker。 | 您的组织未启用该功能。 | 请与Fusion管理员联系。 |

## 常见问题

### 是否存在适用于Claude或ChatGPT的官方Fusion连接器？

目前不可以。 使用自定义MCP服务器URL。 Co-worker（独立版本和Fusion右边栏中的）已内置Fusion。

### 我可以使用多个Fusion组织吗？

可以。 您可以在对话期间切换活动组织，而无需重新连接。

### 代理可以代表我做什么？

代理使用您的Fusion角色和团队权限充当您的角色。 它不能访问Fusion中无法访问的任何内容。 破坏性操作需要明确确认。

### 代理是否看到我的连接密钥？

不可以。 连接和密钥工具返回元数据（名称、类型、范围、过期），而不是凭据或机密值。

