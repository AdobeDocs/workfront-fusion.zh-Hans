---
name: add-mini-tocs
description: ""
source-git-commit: 4ec81401b5a76edd620b9779414ee578966b4315
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 0%

---


# 添加迷你目录

扫描Markdown文件，并在每个具有直接子标题的合格标题下插入一个小型目录。

## 工作流

1. 读取目标文件。
2. 识别`##`级别或更高级别的每个标题，这些标题至少有一个直接子标题（更深一个`#`级别）。
3. 对于每个此类父标题，仅构建指向其直接子标题的链接的项目符号列表。
4. 在第一个子标题的前面，在父标题之后的任何介绍性文本后面插入列表。
5. 如果该位置已存在迷你TOC，请将其与该部分中当前的子标题进行比较。 如果列表已过期（缺少条目、多余条目或不正确的链接），请将其替换为更新的列表。 如果已经匹配，则跳过。
6. 编写更新的文件。

## 范围

- **从不**&#x200B;在`#`文章标题下创建迷你目录。 迷你目录仅添加在`##`标题和更深的标题下。
- `##`标题获取其`###`直接子项的列表。
- `###`标题获取其`####`直接子项的列表。
- 等等，以更深层次地了解。

## 链接格式

列表中的每个条目都使用此精确格式：

```
* [Heading text](#anchor)
```

### 锚点生成规则

将标题文本转换为锚点，如下所示：

1. 小写全部文本。
2. 删除任何非字母、数字、空格或连字符的字符。
3. 将空格替换为连字符。
4. 删除任何反撇号形式的代码格式（将文本保留在其中）。

示例： `### Create or edit a function` → `#create-or-edit-a-function`

## 嵌套规则

- 每个列表中仅链接&#x200B;**直接子项**（比父项深一层）。
- 请勿在同一列表中包含孙辈或较深的标题。
- 如果这些儿童标题本身有孩子，他们会在标题下方插入自己的迷你目录。

**示例结构：**

```
## Manage a package          ← parent: gets a list of ### headings
### Functions                ← child of ##, parent of ####: gets a list of #### headings
#### Create a function       ← child of ###
#### Delete a function       ← child of ###
### Variables                ← child of ##
### History                  ← child of ##
```

结果位于：

在`## Manage a package`下：

```
* [Functions](#functions)
* [Variables](#variables)
* [History](#history)
```

在`### Functions`下：

```
* [Create a function](#create-a-function)
* [Delete a function](#delete-a-function)
```

## 投放

在第一个子标题的前面插入迷你目录列表。 如果在父标题和第一个子标题之间有介绍性文本，则列表将紧跟在该文本之后，位于第一个子标题的正上方。 在迷你目录列表前后始终包含空白行。

## 跳过的内容

- `#`标题（文章标题）：请勿在此添加迷你目录。
- 只有一个直接子项的父标题：跳过 — 单个项目列表不添加导航值。
- 没有子标题的部分：跳过。
