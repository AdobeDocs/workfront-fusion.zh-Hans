---
name: release-notes-formatter
description: 格式化并验证Workfront发行说明，确保一致性、正确结构和正确链接。 仅用于产品版本目录中的发行说明文件，或者用户提及发行说明、产品版本或季度版本时。 不适用于操作方法文章或常规文档。
source-git-commit: 4d32e8aab5b3b8a12dbc23e61f517fc4fd6dc9e5
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 2%

---


# 发行说明格式化程序

在`help/quicksilver/product-announcements/product-releases/`目录中格式化并验证Adobe Workfront发行说明。

## 页面类型

从文件路径和内容中标识页面类型：

| 页面类型 | 文件模式 | 模板 |
|-----------|-------------|----------|
| **概述** | `{YY}-q{N}-release-overview.md` | 请参阅。#overview-page-template |
| **产品区域** | `{YY}-q{N}-{area}.md` | 请参阅。#product-area-page-template |
| **计划** | `planning-release-activity-{YY}-q{N}.md` | 类似于产品区域 |
| **外观** | `look-and-feel-updates-{YY}-q{N}.md` | 请参阅。#look-and-feel-page-template |

## 格式化工作流

### 步骤1：验证Frontmatter

所有发行说明页面的必填字段：

```yaml
---
title: <descriptive title>
description: <matches or summarizes the title>
author: <author name>
feature: Product Announcements
recommendations: noDisplay, noCatalog
exl-id: <existing UUID — never generate or change>
---
```

规则：
- `feature`必须刚好`Product Announcements`
- `recommendations`必须刚好`noDisplay, noCatalog`
- 从不创建`exl-id` — 仅包含已存在的一个
- 不要将`draft: Probably`添加到实际页面（仅限模板）

### 步骤2：按页面类型验证结构

#### 产品区域页面

1. **H1**： `{Written Quarter} {Area} enhancements`
   - 示例：`# Second Quarter 2026 Administrator enhancements`
   - 季度必须写成：“第一季度”、“第二季度”、“第三季度”、“第四季度”

2. **简介段落**：说明区域以及概览的链接
   - 必须链接到&#x200B;**正确季度的**&#x200B;概览文件
   - 常见错误：链接到上一季度（例如，`26-q1`而不是`26-q2`）

3. 每个功能&#x200B;**H2**：将功能标题作为标题
   - **最新功能在前** — 最新的发行说明必须作为介绍段落之后的第一个H2显示
   - 较旧的功能将按反时间顺序列出

4. 在每个H2之后&#x200B;**日期标注块**：

```markdown
>[!NOTE]
>
>Preview: {Month Day, Year}
>Production fast release: {Month Day, Year}
>Production for everyone: {Month Day, Year}
```

5. **正文**：功能描述，然后链接到帮助文档

#### 概述页面

1. **H1**： `{Written Quarter} release overview`

2. **在计划发行月份介绍段落**

3. 带有发布计划表的&#x200B;**`>[!IMPORTANT]`块**

4. **H2`Adobe Workfront enhancements`**，包含锚点链接的项目符号列表：

```markdown
* [Administrator enhancements](#administrator-enhancements)
* [Document enhancements](#document-enhancements)
```

5. 带有HTML功能表的每个产品区域&#x200B;**H3**（请参阅。claude/commands/_release-notes-formatter-reference.md#overview-feature-table）
   - 在每个表中，**最新功能排在前** — 最新行显示在表的顶部（标题行之后）

6. **尾随部分** (H2)：其他区域的发行说明、桌面校对查看器更新、公告、API版本、维护更新、培训更新

### 步骤3：验证链接

- 产品区域页面中的&#x200B;**概述链接**：必须指向同一季度
   - 正确： `26-q2-release-activity/26-q2-release-overview.md`
   - 错误： `26-q1-release-activity/26-q1-release-overview.md`
- 概览中的&#x200B;**锚点链接**：必须匹配H3 ID（小写、连字符）
- 概览表中的&#x200B;**功能链接**：必须使用`class="MCXref xref" xrefformat="{para}"`
- **帮助文档链接**：必须以`/help/quicksilver/`开头

### 步骤4：验证日期

- 格式： `{Month} {Day}, {Year}`（例如，“2026年3月12日”）
- 将`TBD`用于未知日期
- 产品区域页面`>[!NOTE]`块中的日期必须与相应的概述表行匹配
- 预览日期应早于生产日期

### 步骤5：常见修复

设置格式时应用以下修复：

| 问题 | 修复 |
|-------|-----|
| 概述链接季度错误 | 更新以匹配文件自己的季度 |
| 缺少`>[!NOTE]`日期块 | 在H2功能标题后添加块 |
| 日期格式不一致 | 标准化为`Month Day, Year` |
| `>[!NOTE]`前缺少空白行 | 添加空白行 |
| 编号说明行中的额外空格 | 修剪尾随空格 |
| 产品区域页面中的HTML | 保留为Markdown（HTML仅适用于概览表） |
| 缺少`exl-id` | 将其排除 — 不生成一个 |

### 步骤6：更新目录

每当您创建&#x200B;**新**&#x200B;发行说明页面（概述或产品区域）时，请将其添加到同一更改中的`help/quicksilver/TOC.md`。 不在目录中的页面将不会显示在已发布的导航中，即使概述表格中的链接指向该页面也是如此。

添加的位置：

- 目录在标题下每季度有一个节，如`* 2026 Q3 Release {#release-26-q3}`。 如果季度标题尚不存在（新季度的第一页），请将其添加到上一季度的上方，这样最新季度就会位于最上方。
- 在该季度标题下，按以下顺序列出页面：
   1. 首先&#x200B;**概述** (`Third Quarter 2026 release overview`)。
   2. **产品区域页面**&#x200B;按区域名称（管理员、文档、企业运营、项目、报表、请求）的字母顺序排列。
   3. **其他增强功能**&#x200B;最后进行（始终在按字母顺序排列的产品区域之后）。

每个TOC条目都是一个使用页面标题和绝对存储库路径的Markdown链接：

```markdown
      * [Third Quarter 2026 Documents enhancements](/help/quicksilver/product-announcements/product-releases/26-q3-release-activity/26-q3-documents.md)
```

将缩进（六个空格）与周围的条目匹配。 将页面H1逐字用作链接文本 — 例如`Documents enhancements`、`Requesting enhancements`（不是`Requests`） — 以便TOC标签与之前的季度匹配。

要避免的常见错误：

- 创建产品区域页面，而不将其添加到目录。
- 从新的产品区域页面链接到其他季度的概述（步骤3）。
- 在上一个季度的标题下插入新季度的页面。

## 文件命名约定

| 类型 | 模式 | 示例 |
|------|---------|---------|
| 概述 | `{YY}-q{N}-release-overview.md` | `26-q2-release-overview.md` |
| 产品区域 | `{YY}-q{N}-{area-slug}.md` | `26-q2-admin-and-setup.md` |
| 目录 | `{YY}-q{N}-release-activity/` | `26-q2-release-activity/` |

标准区域概要： `admin-and-setup`、`documents`、`projects`、`reports`、`requests`、`other`

## 季度映射

| 季度 | 书面形式 | Months |
|---------|-------------|--------|
| Q1 | 第一季度 | 1月3日 |
| Q2 | 第二季度 | 4月6日 |
| Q3 | 第三季度 | 7月9日 |
| Q4 | 第四季度 | 10月至12月 |

季度产量报告通常会在当季最后一个月的第二个整周的周四发布。

## 验证核对清单

查看发行说明文件时，请验证：

- [ ] Frontmatter的所有必填字段都具有正确的值
- [ ] H1与页面类型格式匹配
- [ ]概述链接指向正确的季度
- [ ]每个功能都有一个`>[!NOTE]`日期块（产品区域页面）
- [ ]日期格式一致(`Month Day, Year`)
- [ 概述中的]功能表行与产品区域页面内容匹配
- [ ]没有断开的内部链接
- [ 概述中的]个锚点链接与H3节ID匹配
- [ ]功能以最新先的方式排序（包括产品区域页面和概述表）
- [ ]个新发行说明页面在`help/quicksilver/TOC.md`中按正确的季度列出，概览在前，产品区域按字母顺序（其他在后）排列

## 其他资源

- 有关完整的HTML模板和示例，请参阅。claude/commands/_release-notes-formatter-reference.md
