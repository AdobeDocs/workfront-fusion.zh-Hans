---
title: 设置通知选项
description: 在团队级别设置电子邮件通知选项。
author: Becky
feature: Workfront Fusion
exl-id: 570a09fc-01a9-4952-8a2b-8bfdd86d0bd8
TQID: https://experienceleague.adobe.com/-HytP4gfrhiiSn-dg5ndg1YC6NTMC-NURYzSFgO5kIo
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 90a58033e240271b88d01b9daef9763f38264056
workflow-type: tm+mt
source-wordcount: 665
ht-degree: 13%

---

# 设置通知选项

在您的组织使用Adobe Unified Shell时，您通过Adobe通知区域接收通知。

如果贵组织尚未迁移到Adobe Unified Shell，您可以选择团队收到的通知。 在团队级别设置通知。

您可以控制发送通知的用途：

* 警告时通知： Fusion在场景执行记录警告时发送通知。
* 出错时通知：当场景执行失败时，Fusion会发送通知。
* 禁用场景时通知：当场景自动停用（例如，出现太多连续错误后）时，Fusion会发送通知。

您可以在团队或方案级别设置通知。 方案级别的通知将覆盖在团队级别设置的通知。 也就是说，如果场景设置直接与团队设置冲突，则遵循场景设置。 团队通知设置会显示该设置是否存在任何覆盖。

默认情况下，Workfront Fusion中会启用所有通知类型。

>[!IMPORTANT]
>
>要从Workfront Fusion接收任何通知，必须在Adobe CX Enterprise通知设置中启用Fusion通知。 您可以通过单击屏幕右上角的通知铃铛并单击设置图标来访问这些设置。

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
  <tr data-mc-conditions=""> 
   <td role="rowheader">角色</td> 
   <td> 
     <p>您必须是要为其调整通知设置的Fusion组织和团队的成员。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 查看和管理团队级别的通知设置

1. 在Workfront Fusion中，单击左侧导航栏中的&#x200B;**团队概述**。
1. 单击&#x200B;**通知选项**&#x200B;选项卡。

   此时将打开“通知”选项列表。 如果存在任何覆盖，则该设置旁边会显示覆盖的数量。

1. （视情况而定）如果有任何覆盖，要查看哪些场景覆盖团队通知设置，请单击该设置的三个点菜单。

   您可以单击此菜单中的某个方案直接转到该方案。

   ![覆盖方案菜单](assets/view-notification-override.png)

1. 要恢复通知类型的默认设置，请参阅此文章中的[恢复通知默认设置](#restore-notification-defaults)。

对“通知”选项列表所做的更改将自动保存。

## 设置方案级通知设置

单个方案的通知设置在该方案的“方案设置”面板中进行设置。

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要添加过滤器的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击方案底部的[!UICONTROL 方案设置]图标![方案设置图标](assets/scenario-settings-icon.png)。
1. 在“方案设置”面板中，单击面板底部的&#x200B;**显示高级设置**。
1. 根据需要调整&#x200B;**警告时通知**、**错误时通知**&#x200B;和&#x200B;**方案禁用时通知**&#x200B;设置。
1. 单击&#x200B;**确定**&#x200B;保存并退出方案设置。

## 恢复通知默认值

您可以从“通知选项”选项卡将团队通知设置恢复为默认值。 这会将通知选项设置为已启用，并删除该通知类型的所有方案通知覆盖。

如果通知类型当前设置为默认值，则&#x200B;**还原为默认值**&#x200B;图标不可见。

1. 在Workfront Fusion中，单击左侧导航栏中的&#x200B;**团队概述**。
1. 单击&#x200B;**通知选项**&#x200B;选项卡。

   此时将打开“通知”选项列表。 如果通知类型当前未设置为默认值，则该通知类型将显示还原为默认图标。

   ![还原为默认可见](assets/restore-notification-defaults.png)

1. 要恢复该通知类型的默认设置，包括任何方案覆盖，请单击&#x200B;**重置为默认值**&#x200B;图标![重置为该通知类型的默认值](assets/restore-default-icon.png)。

对“通知”选项列表所做的更改将自动保存。

<!--

## Set notification options

If your organization is not on the Adobe Unified Shell, you can set notification settings directly in Fusion.

Email notification options are set on the team level.

1. In the left navigation panel, click **[!UICONTROL Team]**
1. Select the **[!UICONTROL Notification Options]** tab.
1. Enable the notifications that you want the team to receive.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">'[!UICONTROL Warning in scenario run]'</td> 
      <td> <p>Receive an email when there is a warning in a scenario run</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Errors in scenario run]</td> 
      <td>Receive an email when there is an error in a scenario run.</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Scenario deactivation]</p> </td> 
      <td><p>Receive an email when a scenario deactivates.</p><p>In some cases, a scenario might be deactivated by the Workfront Fusion engineering team because the scenario is causing performance or other issues. In these cases, you do not receive notifications in Workfront Fusion. </p></td>

</tr>
</tbody>
</table>

Changes to notification options save automatically.

-->
