---
name: fusion-release-notes
description: 创建一个新的Workfront Fusion每周发行说明页面，并将其链接到发行活动概述页面和目录。 当用户想要编写、添加或草稿新的Fusion发行说明或每周发行页面，或者请求为发行记录新的Fusion功能时使用。 请勿在product-announcements/product-releases中使用Workfront (Quicksilver)发行说明 — 针对这些内容使用release-notes-formatter。
source-git-commit: 59a8d8ee83906bc16fc627bd348accc4e588cf9b
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 1%

---


# Fusion发行说明

在`help/workfront-fusion/fusion-product-releases/`中新建一个每周Adobe Workfront **Fusion**&#x200B;发行说明页面，并将其从发布活动概述页面和`help/workfront-fusion/TOC.md`这两个位置链接起来，以便可发现该页面。

此系统不同于`release-notes-formatter`技能处理的Quicksilver （核心Workfront）发行说明：

| | Fusion发行说明（此技能） | Quicksilver发行说明(`release-notes-formatter`) |
|---|---|---|
| 节奏 | 每周 | 每季度 |
| 目录 | `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/` | `help/quicksilver/product-announcements/product-releases/` |
| 按功能日期标注 | 否 — 页面标题包含周 | 是 — 每个功能`>[!NOTE]`块 |
| 索引页 | `fusion-release-activity.md` （按年/月） | `{YY}-q{N}-release-overview.md`（按季度） |

## 步骤1：收集特征

询问用户（如果尚未提供）一周的文档功能/更改列表，以及每项功能/更改列表：

- 简短的功能标题
- 简单描述哪些内容发生了变化以及它为什么重要
- 链接到的帮助文章（验证路径是否存在 — 请勿猜测）
- 是需要用户/管理员操作还是弃用（需要`>[!IMPORTANT]`标注）

## 第2步：确定文件名和日期

- 查找文档记录的那一周的星期一（或发布日期），并在不明确时与用户确认。
- 文件路径： `help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md`
  - `{M}`和`{D}`没有&#x200B;**前导零**： `fusion-2026-7-20.md`，而不是`fusion-2026-07-20.md`。
  - 如果year文件夹尚不存在，请创建它。
- 在创建新页面之前，请检查该周的页面是否已存在。

## 第3步：编写页面

### Frontmatter

```yaml
---
title: Workfront Fusion release activity Week of {Month} {Day}, {Year}
description: Workfront Fusion release activity Week of {Month} {Day}, {Year}
author: {Author}
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
---
```

规则：
- `title`和`description`相同。
- 始终在日期(`July 20, 2026`)中包含逗号，即使某些旧页面会忽略该逗号 — 请勿复制该不一致内容。
- **每个新页面使用`hidefromtoc: true`。 不添加`exl-id`或`TQID`。** 发布页面后，稍后会分配这些权限；而发明一个权限是错误的。 （自2026年年中以后的页面都遵循此模式 — 如果您需要查看示例，请参阅`_fusion-release-notes-reference.md`。）

### 正文

```markdown
# Workfront Fusion release activity: Week of {Month} {Day}, {Year}

This page describes all enhancements made in Adobe Workfront Fusion the week of {Month} {Day}, {Year}.

For a list of all recent changes, see [Adobe Workfront Fusion release activity](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md).

For a list of recent bug fixes in Workfront Fusion, see the [Workfront Maintenance Updates](https://experienceleague.adobe.com/en/docs/workfront-known-issues/releases/current-updates) page and check for any updates labeled Workfront Fusion Maintenance Update.

## {Feature title}

Feature description paragraph(s) — what changed, why, and how it affects existing scenarios/configurations if relevant.

For more information, see [{Help article title}](/help/workfront-fusion/{path-to-article}.md).

## {Next feature title}

...
```

注意：
- 每个功能各一个H2，按用户给它们的顺序（页面中没有强制的最新排序 — 只有一周）。
- 每个功能没有`>[!NOTE]`日期标注 — 页面标题已经包含日期。
- 如果某个功能需要执行操作或属于重大更改/弃用，请直接在H2下方的描述前添加`>[!IMPORTANT]`标注：

  ```markdown
  ## {Feature title}
  
  >[!IMPORTANT]
  >
  >**Action Required: {short summary of what the user must do and by when}**
  >
  >{Details of the requirement.}
  
  {Regular description paragraph(s).}
  ```

- 每个功能都应以“有关详细信息，请参阅[...]”结尾 相关帮助文章的链接。 验证链接目标是否存在于存储库中。

## 步骤4：将页面添加到概览索引

编辑`help/workfront-fusion/fusion-product-releases/fusion-release-activity.md`：

- 查找`## Fusion releases in {current year}`部分（它是&#x200B;**非**，包装在`+++`可折叠的块中 — 仅折叠过去的年份）。
- 直接在年份标题下查找或创建版本月份的`### {Month} {Year}`标题。
  - 如果月份标题尚不存在，请将它在上个月&#x200B;**以上**&#x200B;添加（最新月份在前）。
- 将新页面添加为该月标题下的&#x200B;**第一个**&#x200B;项目符号（最新的一周优先）：

  ```markdown
  * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- 如果这是新年的第一个版本，请在上一年的标题上方添加新的`## Fusion releases in {YYYY}`标题，并将&#x200B;*previous*&#x200B;年的部分包装在`+++ **Click to open**` / `+++`可折叠块中（如果尚未包装）。

## 步骤5：将页面添加到目录

编辑`help/workfront-fusion/TOC.md`：

- 查找当前年份的`* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}`，嵌套在`* Fusion release activity {#fusion-release-activity}`下。
- 将新页面添加为该标题下的&#x200B;**first**&#x200B;条目（最新的最先），匹配现有缩进（8个空格）：

  ```markdown
        * [Workfront Fusion release activity: Week of {Month} {Day}, {Year}](/help/workfront-fusion/fusion-product-releases/fusion-releases-{YYYY}/fusion-{YYYY}-{M}-{D}.md)
  ```

- 如果当前年份的标题尚不存在，请在上一年标题上方添加`* Fusion releases - {YYYY} {#fusion-releases-{YYYY}}`。
- **不要**&#x200B;将`{hide-from-toc}`前缀添加到新条目 — 仅用于旧条目过期后退出可见导航的条目（请参阅下面的已知不一致）。

### 要观察的已知不一致（不复制）

- 几个2026年初的目录条目错误地嵌套在`Fusion releases - 2025`标题下，即使页面本身是2026年版本。 添加新条目时，请始终仔细检查它是否落在与&#x200B;**它自己的年份**&#x200B;匹配的标题下，而不是在上一个条目所在的位置。
- 一些较旧的页面标题/H1在年份之前省略逗号（`July 13 2026`而不是`July 13, 2026`）。 在新页面中始终使用逗号。

## 步骤6：最终核对表

- [ ]文件是在正确的路径创建的，且日期中没有前导零
- [ ] Frontmatter使用`hidefromtoc: true`，不是虚构的`exl-id`/`TQID`
- [ ]标题/描述匹配，日期包含逗号
- [ ]每个功能都有一个说明和经过验证的“了解更多信息”链接
- [ ]需要操作/弃用功能具有`>[!IMPORTANT]`标注
- [ ]新页面已添加为`fusion-release-activity.md`中的最新条目，位于正确的年/月下
- [ ]新页面已添加为`TOC.md`中正确年份标题下的最新条目
- [ ]根据需要创建的新年/月标题，前一年折叠在`fusion-release-activity.md`中

## 其他资源

有关完整有效示例（简单的多功能周，以及具有`>[!IMPORTANT]`操作必需标注的周），请参阅`.claude/commands/_fusion-release-notes-reference.md`。
