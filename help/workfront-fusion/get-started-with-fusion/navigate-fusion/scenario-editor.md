---
title: 方案编辑器
description: 利用方案编辑器，可在可视化界面中创建和编辑方案。
author: Becky
feature: Workfront Fusion
exl-id: 47ccecf0-751c-4026-96a9-329c33cb6801
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 3%

---

# 方案编辑器

利用方案编辑器，可在可视化界面中创建和编辑方案。

![方案编辑器](assets/scenario-editor.jpg)

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证</td> 
   <td> <p>新增： [!UICONTROL Standard]</p><p>或</p><p>当前： [!UICONTROL Work]或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>[!UICONTROL Select] 或[!UICONTROL Prime] [!DNL Workfront]计划：您的组织必须购买[!DNL Adobe Workfront Fusion]。</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 计划： [!DNL Workfront Fusion]已包括在内。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买[!DNL Adobe Workfront Fusion]。</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">访问级别配置*</td> 
   <td> 
     <p>您必须是组织的[!DNL Workfront Fusion]管理员。</p>
     <p>您必须是团队的[!DNL Workfront Fusion]管理员。</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 打开方案编辑器并添加模块：

1. 单击左侧面板中的&#x200B;**[!UICONTROL Scenarios]** ![方案图标](assets/scenarios-icon.png)。
1. 单击问号图标![问号图标](assets/question-mark-full-size.png)，然后查找并单击要开始使用的应用程序或服务。 有关配置模块的详细信息，请参阅[配置模块](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)。

## 可用的方案编辑器操作

### 运行场景

| 操作 | 详细信息 |
|----------|----------|
| 测试运行场景 | 在激活方案之前，请验证方案是否按预期运行。 一旦激活，场景将根据其计划执行。 如果所有组件都未按预期运行，请参阅[添加错误处理](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md)以了解如何处理错误。 |

![运行方案按钮](assets/run-your-scenario.png)

### 正在调度

| 操作 | 详细信息 |
|----------|----------|
| 计划方案 | 默认情况下，场景每15分钟运行一次。 您可以通过定义激活方案运行的时间和频率来更改此设置。 融合场景可以计划为每5分钟运行一次。 有关详细信息，请参阅[计划方案](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。 |

![计划面板](assets/scheduling-scenario-editor.png)

### 控件

| 操作 | 详细信息 |
|----------|----------|
| 保存 | 保存场景后，三个点菜单下将显示一个新版本，以防您未来需要访问它。 以前保存的方案版本仅可用60天。 |
| 方案设置 | 方案设置面板包含方案的高级设置。 有关可用设置的详细信息，请参阅[配置方案设置](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)。 |
| 注释 | 记录方案。 其他用户可以在场景中查看这些注释。 |
| 自动对齐 | 自动对齐场景中的模块。 |
| 说明流程 | 查看显示数据如何流过场景的动画。 |
| 开发工具 | 使用Devtool，您可以检查场景的所有手动运行，查看所有执行的操作，并查看每个执行的API调用的详细信息。 您可以查看导致错误的模块、操作或单个响应，并使用该知识来优化场景。 有关详细信息，请参阅[调试方案](/help/workfront-fusion/manage-scenarios/debug-a-scenario.md)。 |
| 更多 | 在更多菜单中，您可以导入或导出Blueprint，并将方案恢复为以前的版本。 |

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
