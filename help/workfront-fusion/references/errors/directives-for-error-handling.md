---
content-type: reference
title: 用于错误处理的指令
description: 本文介绍了可用于在Adobe Workfront Fusion场景中处理错误的指令。
author: Becky
feature: Workfront Fusion
exl-id: d7b0141f-d99d-4ab7-a60f-ed552a76f05d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 15%

---

# 用于错误处理的指令

错误处理指令允许您选择场景遇到错误时发生的操作。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> 新增：标准<p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Adobe Workfront Fusion]许可证</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新：</p> <ul><li>[！UICONTROL Select]或[！UICONTROL Prime] Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li><li>[！UICONTROL Ultimate] Workfront计划：包括Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>


要了解您拥有的计划、许可证类型或访问权限，请联系您的Workfront管理员。

有关Adobe Workfront Adobe Workfront Fusion的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 用于错误处理的指令

Workfront Fusion中提供了以下错误处理指令。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>回滚</p> <p> <img src="assets/rollback.png"> </p> </td> 
   <td> <ul><li><p>场景执行立即停止。</li><li>将在所有模块上启动回滚阶段，以尝试将所有模块恢复到其初始状态。 </li><li>不处理后续模块。</p></li><li> <p>在大多数情况下，在场景设置下指定的连续错误数后，将停用场景。 有关详细信息，请参阅<a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors" class="MCXref xref">连续错误数</a>。</p> </li><li><p>场景执行状态被标记为“错误”。</p></li></ul> <p><b>注意</b>：如果未将错误处理程序路由附加到模块，并且未选中[！UICONTROL场景设置]下的<a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions" class="MCXref xref">允许存储不完整的执行</a>允许存储不完整的执行设置，则这是默认行为。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>提交</p> <p> <img src="assets/commit.png"> </p> </td> 
   <td> <ul><li><p>场景执行立即停止。</li><li>提交阶段在所有模块上启动。 </li><li>不处理后续模块。</p></li><li> <p>将忽略所有未处理的包。</p> </li><li><p>场景执行状态标记为“成功”。 </p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>恢复</p> <p> <img src="assets/resume.png"> </p> </td> 
   <td> <ul><li><p>指定替代输出并将其提供给遇到错误的模块。</p> </li><li><p>随后处理模块。</p></li><li> <p>场景执行状态标记为“成功”。</p></li></ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>忽略</p> <p> <img src="assets/ignore.png"> </p> </td> 
   <td><ul><li> <p>该错误被忽略。</li><li> 不处理后续模块。</p> </li><li><p>如果存在未处理的捆绑包，则场景执行会正常继续进行。</p> </li><li><p>场景执行状态标记为“成功”。</p> </li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>间断</p> <p> <img src="assets/break.png"> </p> </td> 
   <td><ul><li> <p>场景执行的状态存储在未完成执行的队列中，在该队列中可以手动解决错误。有关详细信息，请参阅<a href="/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md" class="MCXref xref">查看并解决未完成的执行</a>。</p> <p>不过，也有一些例外。 有关详细信息，请参阅配置场景设置<a href="/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow" class="MCXref xref">一文中的</a>允许存储不完整的执行</a>。</p></li><li> <p>不处理后续模块。</p></li><li> <p>如果存在未处理的捆绑包，则场景执行会正常继续进行。</p> </li><li><p>禁用[！UICONTROL自动完成执行]选项后，场景执行状态将标记为“警告”。</p></li></ul> <p>有关详细信息，请参阅本文中的<a href="#break" class="MCXref xref">[！UICONTROL Break]</a>部分</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>重试</p> <p> <img src="assets/retry.png"> </p> </td> 
   <td> <p>在某些情况下，当失败原因可能随时间推移而推移时，重新执行失败模块可能会很有用。</p> <p>Workfront Fusion当前不提供Retry指令，但可以使用多种变通方法来模拟其功能。 有关详细信息，请参阅<a href="/help/workfront-fusion/create-scenarios/config-error-handling/retry.md" class="MCXref xref">重试错误处理</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>* 错误处理指令不能在错误处理路由之外使用。
>* Workfront Fusion目前不提供使您能够轻松有条件地生成（抛出）错误的Throw模块，不过可以采取替代措施来模拟其功能。
>
>  有关详细信息，请参阅[配置`throw`错误解决方法](/help/workfront-fusion/create-scenarios/config-error-handling/throw.md)。

## 资源

* 有关回滚和回滚阶段的信息，请参阅方案执行、循环和阶段一文中的[回滚](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#rollback)。
* 有关提交阶段的信息，请参阅方案执行、循环和阶段一文中的[提交](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md#commit)。
