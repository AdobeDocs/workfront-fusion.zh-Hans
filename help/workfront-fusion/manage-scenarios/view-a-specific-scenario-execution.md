---
title: 查看特定场景执行
description: 您可以查看特定场景执行的详细信息，包括筛选和搜索场景事件。
author: Becky
feature: Workfront Fusion
exl-id: 34dd9836-9a1b-4ce2-b24e-ae769888a52a
source-git-commit: 42be02d6a59a5d7b8faccdcfe40e8b967153c6eb
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# 查看特定场景执行

您可以查看特定场景执行的详细信息，包括筛选和搜索场景事件。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何Adobe Workfront Workflow包和任何Adobe Workfront自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime和Select包，以及额外购买的Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>标准</p><p>工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果贵组织具有不包含Workfront Automation and Integration的Select或Prime Workfront包，则贵组织必须购买Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

+++

## 查看特定执行

您可以从方案的方案历史记录中查看执行。


1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡，然后单击方案。

   或

   如果您在方案编辑器中处理方案，请单击窗口左上角附近的左箭头![退出编辑箭头](assets/exit-editing-arrow.png)。

1. 单击方案名称附近的&#x200B;**历史记录**。
   ![历史记录选项卡](assets/history-tab.png)


1. 找到要查看的执行，然后单击该行最右侧的&#x200B;**详细信息**。 仅当执行有详细信息时，[!UICONTROL 详细信息]链接才可见。

   随即会打开场景图，并在右侧打开执行详细信息面板。

   为此执行生成输出的模块将标有绿色标题。

   未运行的模块将灰显。

1. 要查看模块中的输出，请单击模块附近的输出详细信息气泡。 气泡中的数字表示模块输出的捆绑数。

   ![模块附近的输出气泡](assets/output-bubble.png)

1. 要查看通过过滤器的包，请单击过滤器。 过滤器附近的数字表示通过过滤器的捆绑数。
1. 要在执行面板中搜索特定的模块或事件，请在&#x200B;**搜索执行事件**&#x200B;框中输入搜索词。 键入内容时，将显示结果。
1. 要按状态（如成功或警告）限制执行面板搜索结果，请单击&#x200B;**状态筛选器**&#x200B;下拉列表并选择状态。




>[!NOTE]
>
>要创建指向特定模块的链接，请在查看以下页面时将`?moduleId=<module-id>`添加到URL：
>
>* 方案编辑页面（URL以`/edit`结尾）
>* 特定场景执行（URL以`/logs/<log-id>`结尾）
>
>查看场景时，`<module-id>`引用模块标签旁边的数字。
>
>这在调试方案或复制模块配置时可能很有用。
