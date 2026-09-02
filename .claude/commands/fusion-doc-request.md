---
name: fusion-doc-request
description: 处理来自#fusion-documentation Slack模板的Fusion文档请求 — 更新此存储库中的相关Fusion文档文章，然后在产品文档Workfront项目中创建匹配任务，并在自定义表单中填写功能描述和带格式的发行说明。 当用户共享Fusion功能的Slack文档请求线程/消息时，或者针对某个功能显示“请更新并创建任务”之类的内容时，可使用。
source-git-commit: e354c51f13bd4f15172de068cac9720bd097eb8d
workflow-type: tm+mt
source-wordcount: '859'
ht-degree: 0%

---


# Fusion文档请求

处理`#fusion-documentation` Slack渠道中发布的循环“来自{person}的新文档请求”模式：读取请求，更新文档，然后在用于此类先前请求的同一Workfront自定义表单上创建跟踪任务。

这是与`fusion-release-notes`技能不同的工作流。 此技能可更新参考文章并创建Workfront任务；它不会在此存储库中创建或更新每周Fusion发行说明页面，即使请求显示“需要公告：是”。 仅当用户单独请求每周发行说明时，才使用`fusion-release-notes`。

## 步骤1：获取请求详细信息

如果给定Slack链接，则从URL中解析`channel_id`和`message_ts`并获取线程（`slack_get_thread_replies`或`slack_read_thread`，具体取决于所连接的Slack MCP工具 — 如果其中一个失败，则尝试同时获取这两个线程）。 保留线程的永久链接/URL — 在步骤3中需要它。

此环境中的Slack连接不稳定（令牌已过期，会在会话期间断开连接）。 如果获取失败：
- 重试一次。
- 如果仍然失败，请明确告知用户获取失败，并要求用户直接粘贴请求内容。 不要猜测内容，也不要轻言放弃。

请求模板包含以下字段 — 提取每个字段：

* **功能标题**
* **描述**
* **要添加到文档的点** *（有时存在 — 请求者希望包含的特定部分/详细信息；如果给定，则将其视为必需部分，而不是可选部分）*
* **预计发行日期**
* **需要公告** *(是/否 — 仅供参考；请参阅上面的说明。 不要对此字段执行操作。)*

如果请求链接到具有完整规范的Confluence Wiki页面，请在编写文档之前获取该页面(`get_wiki_content`)。 不要只依赖Slack摘要来了解技术详细信息（确切的字段名称、步骤、UI标签） — 在链接时从Wiki规范中提取技术详细信息。

## 第2步：更新文档

在此存储库中查找相关的现有文章（查看相关模块名称、UI标签或设置名称 — 不要猜测文件）。 根据文章的现有结构、标题级别和住宅样式，更新它们以反映更改。

* 请勿发明不在Slack请求或链接的Wiki规范中的技术详细信息（确切字段名称、权限范围、配置步骤）。 如果某些内容未确认，请将其内联标记为HTML评论（例如`<!-- BECKY CHECK ME: confirm the exact permission scope before publishing -->`），而不是猜测 — 从不将其标记为可见标注。 它不得在已发布的页面上呈现。
* 如果这需要全新的文章文件（不仅仅是对现有文章文件的编辑），请遵循此存储库的常规规则：前端内容中不存在虚构的`exl-id`/`TQID`，请将新页面电连到相关目录，并在创建文件后将该文件转换为CRLF/no-BOM（`Write`工具默认为LF）。

## 步骤3：创建Workfront任务

项目： **产品文档任务 — 用于需要消息传送的开发问题**。 使用`insights_find_id_by_name` （实体`project`）解析其ID，而不是对其进行硬编码，以防其发生更改 — 请参阅下面的已知值以了解最后一个解析的ID。

任务字段：

| 字段 | 价值 |
|---|---|
| `name` | `Becky - {Feature Title}` |
| `projectID` | 从上面的项目查找中 |
| `assignedToID` | 当前用户，来自`insights_get_current_user` |
| `categoryID` | 产品文档自定义表单ID — 请参阅下面的已知值。 如果不清楚，请对此项目中任何最近的同级任务查询`task.task_categoryID`以进行确认。 |
| `description` | **完成Slack消息文本**（请求模板中的所有字段，而非转述），后跟指向Slack对话的链接 |
| `DE:Release notes` | 带格式的发行说明，请参阅下面的格式 |
| `DE:Preview Date Known` | `Yes`，默认 |
| `DE:Preview Date` | 默认情况下，请求的&#x200B;**预计发布日期** |
| 产品/区域 | 选择`Fusion` （产品文档表单上的枚举字段；如果名称不清楚，请使用`insights_search_fields`确认确切的字段名称） |

将预览日期字段设置为同一创建调用的一部分 — 请勿将其留待以后或等待询问。 如果用户稍后提供不同的日期，或指出日期实际上尚不知道，请相应地更新，但默认每次都填写日期。

`DE:Release notes`字段的发行说明格式。 始终以`***FUSION***`在其自己的行中开头，然后是空白行，然后是标题 — 这将标记注释概览，使其归属于Fusion（与核心Workfront相反）：

```markdown
***FUSION***

## {Feature Title}

{Description of what changed and why it matters, in second person. A sentence or two is enough for a simple change - use multiple paragraphs and/or a bulleted list for anything with several parts or steps, the same way a full weekly release note would.}

For more information, see [{Article title}](/help/workfront-fusion/{path-to-article}.md).
```

在创建调用之前，使用`workfront://tools/create-any-object`调用`read_workflow_docs` — 此调用设置自定义字段和枚举值(`DE:Preview Date Known`)，根据MCP服务器的规则需要它。

## 第4步：确认返回用户

简而言之，报告：

* 您更改了哪些doc文件以及添加了哪些内容。
* 任务名称和URL。
* 您设置的确切字段值，包括预览日期字段。
* 您未完全放心的任何内容 — 例如，Slack无法访问，您仅使用粘贴的文本工作，目标文档文章不明确，或者源资料中没有技术细节，标记而不被猜到。

## 已知值（来自以前的运行）

确认这些事件仍会解决，而不是假设它们是永久性的：

* 项目“产品文档任务 — 适用于需要消息传送的开发问题”映射到ID `5e69583f00236b9f767c3e3944100ee4`
* 产品文档自定义表单(`categoryID`)为`5d7275b9000514604bd969d418725843`
* 使用的自定义字段： `DE:Release notes`、`DE:Preview Date Known`、`DE:Preview Date`
