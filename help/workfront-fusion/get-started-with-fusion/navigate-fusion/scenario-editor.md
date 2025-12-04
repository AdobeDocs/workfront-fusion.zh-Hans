---
title: 方案编辑器
description: 利用方案编辑器，可在可视化界面中创建和编辑方案。
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: f968b9141173725160cea36575ad4e02a09a5e3f
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 16%

---

# 方案编辑器

利用方案编辑器，可在可视化界面中创建和编辑方案。

![方案编辑器](assets/scenario-editor.jpg)

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

## 打开方案编辑器并添加模块：

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]** ![方案图标](assets/scenarios-icon.png)。
1. 单击问号图标![问号图标](assets/question-mark-full-size.png)，然后查找并单击要开始使用的应用程序或服务。 有关配置模块的详细信息，请参阅[配置模块](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)。

## 可用的方案编辑器操作

### 运行场景

| 操作 | 详细信息 |
|----------|----------|
| 测试运行场景 | 在激活方案之前，请验证方案是否按预期运行。 一旦激活，场景将根据其计划执行。 如果所有组件都未按预期运行，请参阅[添加错误处理](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md)以了解如何处理错误。 |

![运行方案按钮](assets/run-your-scenario.png)

### 日程计划

| 操作 | 详细信息 |
|----------|----------|
| 计划方案 | 默认情况下，场景每15分钟运行一次。 您可以通过定义激活方案运行的时间和频率来更改此设置。 融合场景可以计划为每5分钟运行一次。 有关详细信息，请参阅[计划方案](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。 |

![计划面板](assets/scheduling-scenario-editor.png)

### 控件

您可能需要单击“控件”区域中的三个点图标来查看其中的某些控件。

| 操作 | 详细信息 |
|----------|----------|
| 进行保存 <p>![保存图标](assets/save-icon.png)</p> | 保存场景后，三个点菜单下将显示一个新版本，以防您未来需要访问它。 以前保存的方案版本仅可用60天。 |
| 方案设置 <p>![方案设置图标](assets/scenario-settings-icon.png)</p> | 方案设置面板包含方案的高级设置。 有关可用设置的详细信息，请参阅[配置方案设置](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)。 |
| 注释  <p>![注释图标](assets/notes-icon.png)</p> | 记录方案。 其他用户可以在场景中查看这些注释。 |
| 自动对齐 <p>![自动对齐图标](assets/auto-align-icon.png)</p> | 自动对齐场景中的模块。 |
| 搜索模块![搜索模块](assets/search-modules-icon.png)  </p> | 输入搜索词以查找模块，然后单击要带到该模块的搜索结果。 您可以按模块名称、ID、类型或应用程序进行搜索。 |
| 说明流程  <p>![说明流程图标](assets/explain-flow-icon.png) </p> | 查看动画，其中移动圆点显示数据如何在场景中流动。 |
| DevTool <p>![DevTool图标](assets/devtool-icon.png)</p> | 使用DevTool，您可以检查场景的所有手动运行，查看所有执行的操作，并查看执行的每个API调用的详细信息。 您可以查看导致错误的模块、操作或单个响应，并使用该知识来优化场景。 有关详细信息，请参阅[调试方案](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md)。 |
| 导出Blueprint  <p>![导出Bluepring图标](assets/export-blueprint-icon.png) </p> | 导出当前方案的蓝图。 |
| 导入Blueprint  <p>![导入Blueprint图标](assets/import-blueprint-icon.png) </p> | 导入之前导出的方案Blueprint。 |
| 以前的版本  <p>![上一版本图标](assets//previous-version-icon.png) </p> | 查看此方案的先前版本。 |

![控制面板](assets/controls-editor-scenario.png)

### 工具

| 操作 | 详细信息 |
|----------|----------|
| 流量控制 | 配置设置以控制数据流经的方式。 有关详细信息，[查看所需的链接]。 |
| 工具 | 工具部分包含几个可以增强方案的有用模块。 有关详细信息，[查看所需的链接]。 |
| 文本分析器 | 使用文本解析器工具解析文本，以供在其他方案模块中使用。 文本解析器不需要连接。 有关详细信息，[查看所需的链接]。 |

![工具面板](assets/tools-scenario-editor.png)

### 收藏夹

您可以使用“收藏夹”图标添加常用模块。

![收藏夹面板](assets/favorites-scenario-editor.png)
