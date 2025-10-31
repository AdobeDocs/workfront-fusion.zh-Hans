---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: errors
title: 配置抛出错误解决方法
description: 在某些情况下，您可能希望强制停止场景执行，然后进入“回滚”或“提交”阶段，或者停止路由处理，然后将其存储在查看队列中，并在Adobe Workfront Fusion中解决未完成的执行。
author: Becky
feature: Workfront Fusion
exl-id: 4bf2a6c7-16b2-4545-9adf-be3947a7017d
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# 配置`throw`错误解决方法

在某些情况下，您可能希望强制停止场景执行，然后进入“回滚”或“提交”阶段，或者停止路由处理，并可以选择将其存储在未完成执行的队列中。

目前，错误处理指令不能超出错误处理程序路由的范围，并且Adobe Workfront Fusion不提供可以让您轻松有条件地生成（抛出）错误的模块。

您可以使用以下解决方法来模拟`throw`错误功能。

有关未完成执行的信息，请参阅[在Adobe Workfront Fusion中查看和解决未完成的执行](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)。

有关错误处理指令的信息，请参阅Adobe Workfront Fusion中用于错误处理的[指令](/help/workfront-fusion/references/errors/directives-for-error-handling.md)。

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

## `throw`的解决方法

要有条件地引发错误，您可以配置模块，使其在操作期间故意失败。 一种方法是使用[!UICONTROL JSON] > [!UICONTROL 分析JSON]模块，该模块配置为可选地引发错误（在本例中为`BundleValidationError`）：

![JSON错误](assets/json-parse-json.png)

然后，可以将其中一个错误处理指令附加到错误处理路由：

* **回滚**：强制停止方案执行并执行回滚阶段。
* **提交**：强制停止方案执行并执行提交阶段。
* **忽略**：停止路由处理。
* **中断**：停止处理路由并将其存储在“未完成执行的队列”文件夹中。

以下示例显示了[!DNL Rollback]指令的使用：

![Rollback指令](assets/rollback-directive.png)
