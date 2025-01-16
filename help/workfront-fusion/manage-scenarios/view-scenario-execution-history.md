---
title: 查看并解决未完成的执行
description: '[!UICONTROL Incomplete executions]文件夹存储由于错误未能成功完成的场景执行。 可以手动或自动解决每个存储的不完整执行。'
author: Becky
feature: Workfront Fusion
exl-id: 974b32b4-d86a-48cd-a8d4-1ae2cf309b9b
source-git-commit: 3d06958b6f706f4f974230853fb6553232656fd3
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 0%

---

# 查看方案的执行历史记录

您可以显示有关场景的事件或执行的信息，也可以搜索场景的所有执行以获取特定数据。

场景执行表示场景的单次运行。

场景事件是对场景的修改，如编辑、激活或停用场景。

>[!NOTE]
>
>方案的历史记录会显示方案在过去30天内的所有事件和执行。

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

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 查看方案历史记录


### 在“历史记录”选项卡上查看方案历史记录

[!UICONTROL History]选项卡显示的详细信息多于[!UICONTROL Scenario detail]页面上可用的详细信息。 您还可以对[!UICONTROL History]选项卡上的执行进行过滤和排序。

1. 单击左侧面板中的&#x200B;**[!UICONTROL Scenario]**&#x200B;选项卡，然后单击方案。

   或

   如果您在方案编辑器中处理方案，请单击窗口左上角附近的左箭头![](assets/exit-editing-arrow.png)。

1. 单击方案名称附近的&#x200B;**历史记录**。
   ![历史记录选项卡](assets/history-tab.png)

   针对方案的每次执行都列出了以下详细信息：

   * 运行日期为&#x200B;**[!UICONTROL Started]**
   * 执行Id
   * **[!UICONTROL Status]** （成功或失败）
   * 运行&#x200B;**[!UICONTROL Duration]**
   * **[!UICONTROL Operations]**&#x200B;的数量
   * **[!UICONTROL Data Transfer]**&#x200B;的大小

   >[!NOTE]
   >
   >方案历史记录会在最近执行的方案旁边显示一个&#x200B;**正在处理**&#x200B;标记，同时将执行详细信息写入存储。 在场景执行后立即进行处理。 并且持续时间不应超过几分钟。 处理执行时，场景执行的详细信息可能不可见。

1. 要查看特定方案执行的详细信息，请单击最右侧的&#x200B;**详细信息**。 仅当执行有详细信息时，[!UICONTROL details]链接才可见。
1. 要查看事件，请打开&#x200B;**显示事件**。


### 在“方案详细信息”页面上查看方案历史记录


1. 单击左侧面板中的&#x200B;**[!UICONTROL Scenario]**&#x200B;选项卡，然后单击方案。

   或

   如果您在方案编辑器中处理方案，请单击窗口左上角附近的左箭头![](assets/exit-editing-arrow.png)。

1. 单击右侧面板中的&#x200B;**[!UICONTROL History]**&#x200B;选项卡。
1. （可选）有关所选方案运行的详细信息，请单击右侧面板中的执行。

   有关处理捆绑包的详细信息，请参阅[方案执行流程](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)

   >[!NOTE]
   >
   >* 方案历史记录会在最近执行的方案旁边显示一个&#x200B;**处理历史记录**&#x200B;标记，同时将执行详细信息写入存储。 在场景执行后立即进行处理。 并且持续时间不应超过几分钟。 处理执行时，场景执行的详细信息可能不可见。

1. 要查看事件，请单击&#x200B;**事件**&#x200B;选项卡。

## 筛选场景执行历史记录

您可以过滤执行历史记录以仅查看具有指定值的执行。

1. 打开方案的全页历史记录，如本文中[!UICONTROL History]选项卡](#view-scenario-history-on-the-history-tab)上的[查看方案执行历史记录中所述。
1. 单击要作为筛选依据的列标题中的[!UICONTROL filter]图标![](assets/fusion-scenario-filter-icon.png)。
1. 在[!UICONTROL filter]对话框中，输入要作为筛选依据的值。
1. 单击 **[!UICONTROL Save]**。

过滤器图标在有活动过滤器的列中呈橙色。

<!-- don't see how to do this
## Sort the scenario execution history

You can sort the scenario execution history.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-execution-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL Sort] icon in the header of the column you want to filter by.
1. Optional: To reverse the order of the sort, click the [!UICONTROL Sort] icon again.
-->

## 搜索场景的所有执行

1. 打开方案的全页历史记录，如本文中[!UICONTROL History]选项卡](#view-scenario-history-on-the-history-tab)上的[查看方案执行历史记录中所述。
1. 单击执行列表顶部的&#x200B;**[!UICONTROL Fulltext search]**。

   或

   键入&#x200B;**Ctrl+Shift+F** (Windows)或&#x200B;**Cmd+Shift+F** (Mac)
将打开[!UICONTROL Search in history]窗口。

1. （可选）要搜索包含特定文本的执行，请在&#x200B;**[!UICONTROL Search in history]**&#x200B;窗口的搜索栏中输入文本。

   要搜索精确文本，请用双引号将文本括起来（“示例”）。

   >[!INFO]
   >
   >**示例：**&#x200B;如果要查找创建特定项目的执行，请在[!UICONTROL Fulltext search]栏中输入项目ID。
   >
   >“625ef2ef0006036bd1794b6e52d737c5”

1. （可选）要按日期范围限制搜索，请在[!UICONTROL By date range]区域中选择所需搜索的开始和结束日期。

   >[!NOTE]
   >
   >* 执行仅可用于之前的30天。
   >
   >* [!DNL Workfront Fusion]存储webhook负载30天。 创建webhook有效负载超过30天后对其进行访问会导致错误“[!UICONTROL Failed to read file from storage.]”


1. （可选）要按状态限制搜索，请在&#x200B;**[!UICONTROL By status]**&#x200B;下拉列表中选择所需的状态。


   可用状态包括：

   * [!UICONTROL All]

   * [!UICONTROL Error]

   * [!UICONTROL Warning]

   * [!UICONTROL Success]

1. （可选）更改结果在&#x200B;**[!UICONTROL Sort by dates]**&#x200B;下拉列表中的显示顺序。

1. （可选）要复制场景执行ID，请单击&#x200B;**[!UICONTROL Copy execution ID]**&#x200B;图标 所需执行的行中的<img src="assets/copy-fusion-execution-id-icon.png">。

1. （可选）单击[!UICONTROL Fulltext search]的结果以检查包含该信息的方案模块输出包。
