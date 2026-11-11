---
title: 查看和管理团队角色
description: 每个团队都有一个“角色”选项卡，您可以在其中查看团队的角色、创建自己的角色、选择每个角色包括的权限以及更新或删除角色。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: a3a6922afd713cd002cdf472c7ef62c1855b80d9
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 9%
---
# 查看和管理团队角色

您可以查看团队中可用的角色，创建自己的角色，并选择每个角色包含哪些权限。 您还可以更新和删除角色。

自定义角色具有以下优势：

* 每个团队成员只能访问其工作所需的权限，这降低了关键场景意外更改的风险。
* 自定义角色可以更好地匹配组织的工作方式，而不是让您的团队适应预定义角色。
* 您无需联系支持人员即可自行管理访问权限。

有关组织、团队和预定义团队角色的概述，请参阅[组织和团队概述](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/org-and-team-overview.md)。 有关预定义角色中包含的权限，请参阅[组织和团队角色](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md)。

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
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">访问级别配置</td> 
   <td> 
     <p>您在团队中必须具有<b>[！UICONTROL管理成员]</b>权限。 在预定义角色中，此权限包括在“团队管理员”和“组织所有者”角色中。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 谁可以管理团队角色

团队中具有&#x200B;**[!UICONTROL 管理成员]**&#x200B;权限的任何人都可以创建、更新、删除用户，并将用户分配给该团队中的角色。

* 组织所有者可以创建和管理所有团队中的角色。
* 组织管理员只能管理其所属的团队中的角色，并且他们具有&#x200B;**[!UICONTROL 管理成员]**&#x200B;权限。
* 团队管理员可以管理其团队中的角色。

## 创建或编辑角色

1. 在Fusion的左侧导航中，单击&#x200B;**团队概述**。
1. （视情况而定）如果您不在要查看其角色的团队的页面上，请单击页面顶部附近的&#x200B;**团队**&#x200B;下拉列表，然后选择正确的团队。
1. 打开&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡。

   选项卡列出了团队中可用的角色，包括预定义角色。 对于每个角色，该列表都显示了角色的名称及其权限摘要，如“无权限”、“成员”或“自定义· 19权限”。

1. 要创建角色，请单击&#x200B;**[!UICONTROL 创建角色]**。

   或

   要编辑角色，请在要编辑的角色的行中单击&#x200B;**[!UICONTROL 编辑]**。

   <!-- BECKY CHECK ME: The Edit button is available for the predefined roles as well as custom roles. Confirm the title of the edit page, whether you can rename the predefined roles, and what happens to users who already have the role. -->

1. 在&#x200B;**[!UICONTROL 角色名称]**&#x200B;字段中输入角色的名称。
1. 在&#x200B;**[!UICONTROL 角色模板]**&#x200B;下拉列表中，选择要从中开始的模板。

   模板设置角色的初始权限。 默认模板为&#x200B;**[!UICONTROL 查看器]**。

1. 在&#x200B;**[!UICONTROL 范围的权限]**&#x200B;区域，选择要让角色包含的权限。

   权限按区域分组，如&#x200B;**[!UICONTROL 自动化]**、**[!UICONTROL 连接]**&#x200B;和&#x200B;**[!UICONTROL 团队]**。 对于每个区域，您可以执行以下任一操作：

   * 若要一次设置某个区域中的所有权限，请单击该区域名称旁边的&#x200B;**[!UICONTROL 无访问权限]**、**[!UICONTROL 仅查看]**&#x200B;或&#x200B;**[!UICONTROL 完全访问]**。
   * 要选择特定权限，请选中或清除每个权限对应的复选框。

   有关权限的列表，请参阅本文中您可以包含在角色](#permissions-that-you-can-include-in-a-role)中的[权限。

   <!-- BECKY CHECK ME: Confirm the options in the Role template dropdown and what each one selects. Confirm exactly what No access, View only, and Full access select in each area (in the screenshot, View only selects the view permissions). Confirm whether there is a Description field, and whether there are areas below Team on the page (the screenshots end at Team). -->

1. 单击&#x200B;**[!UICONTROL 保存]**。 要关闭页面而不保存，请单击&#x200B;**[!UICONTROL 取消]**。
1. （可选）要删除角色，请单击&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡上角色行中的&#x200B;**[!UICONTROL 删除]**。

   <!-- BECKY CHECK ME: Confirm why the Delete button is unavailable (dimmed) for some roles, such as Team Operator, Team Member, and Team Admin in the screenshot, whether there is a confirmation prompt, and what happens to users who have the role. Update this step and add a note, if needed. -->

您创建的角色可在团队中使用。 您可以将其分配给团队成员。

### 可包含在角色中的权限

<table style="table-layout:auto">
 <col>
 <col>
 <thead>
  <tr>
   <th>区域</th>
   <th>权限</th>
  </tr>
 </thead>
 <tbody>
 <tr>
   <td role="rowheader">[！UICONTROL Automations]</td>
   <td>查看列表，查看详细信息，查看运行历史记录，管理通知，重置统计信息，运行一次，编辑计划，激活，停用，创建，编辑，发布，删除</td>
  </tr>
 <tr>
   <td role="rowheader">[！UICONTROL未完成的执行]</td>
   <td>查看，管理</td>
  </tr>
 <tr>
   <td role="rowheader">[！UICONTROL Webhooks]</td>
   <td>查看、查看队列、创建、编辑、管理队列、更改优先级、删除</td>
  </tr>
 <tr>
   <td role="rowheader">[！UICONTROL Connections]</td>
   <td>查看、创建、编辑、删除</td>
  </tr>
 <tr>
   <td role="rowheader">[！UICONTROL键]</td>
   <td>查看、创建、编辑、删除</td>
  </tr>
 <tr>
   <td role="rowheader">[！UICONTROL数据存储]</td>
   <td>查看列表，浏览记录，创建，编辑，删除</td>
  </tr>
 <tr>
   <td role="rowheader">[！UICONTROL数据结构]</td>
   <td>查看、创建、编辑、删除</td>
  </tr>
 <tr>
   <td role="rowheader">[！UICONTROL模板]</td>
   <td>查看列表，查看详细信息，创建，编辑，删除</td>
  </tr>
 <tr>
   <td role="rowheader">[！UICONTROL团队]</td>
   <td>查看团队、编辑团队设置、管理成员、删除团队</td>
  </tr>
 </tbody>
</table>

<!-- BECKY CHECK ME: Confirm that this list is complete, and add a description of what each permission allows, if needed. The list is taken from the Create role page, which may have more areas below Team. -->

## 将角色克隆到其他团队

您可以将一个团队中的角色复制到另一个团队，这样您就不必在每个团队中重新创建相同的角色。

1. 打开团队的&#x200B;**[!UICONTROL 角色]**&#x200B;选项卡，如本文中[创建或编辑角色](#create-or-edit-a-role)中所述。
1. 单击&#x200B;**[!UICONTROL 克隆到团队]**。

   将打开“**[!UICONTROL 将角色克隆到其他团队]**”页面。

1. 在&#x200B;**[!UICONTROL 目标团队]**&#x200B;下拉列表中，选择要将角色克隆到的团队。

   此时会出现一个表格，其中列出了当前团队中的角色。

1. 对于表中的每个角色，复查并设置以下内容：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[！UICONTROL Source role]</td> 
      <td> <p>当前团队中的角色及其权限摘要。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 操作]</td> 
      <td> <p>该怎么处理这个角色。 例如，<b>[！UICONTROL Copy to existing role]</b>将源角色的权限复制到目标团队中已存在的角色。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL目标]</td> 
      <td> <p>源角色复制到的目标团队中的角色。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL更改]</td> 
      <td> <p>目标角色是否不同于源角色。 例如，<b>[！UICONTROL已在同步]</b>意味着目标角色已具有与源角色相同的权限。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 用户]</td> 
      <td> <p>有关拥有角色的用户的信息。 例如，<b>[！UICONTROL没有匹配的用户]</b>表示没有要包括的用户。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL状态]</td> 
      <td> <p>克隆后角色的结果。</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 克隆]**。 要关闭页面而不克隆，请单击&#x200B;**[!UICONTROL 取消]**。

<!-- BECKY CHECK ME: The screenshot shows the Clone roles to another team page after a target team is selected. Confirm the options in the Action dropdown (for example, whether you can create a new role in the target team), the options in the Target dropdown, what the checkbox in the Users column does (for example, whether it also assigns the role to matching users in the target team) and what "matching users" means, what the Changes column shows when the roles differ, and what the Status column shows before and after you clone. -->

<!-- BECKY CHECK ME: Confirm whether the Target team dropdown lists all teams or only the teams that you can manage, and whether the Clone to team button is visible to everyone who can manage roles. -->

## 为用户分配角色

分配自定义角色的方式与分配预定义角色的方式相同。 有关说明，请参阅[将用户添加到团队](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md)和[查看或编辑用户角色](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md#view-or-edit-user-roles-for-a-team)。

<!-- BECKY CHECK ME: Confirm that custom roles appear in the role dropdowns in both of these procedures. -->

## 注意事项

* 组织权限层叠。 要授予某人在所有团队中执行操作的权限，请分配组织角色而不是创建团队角色。 有关详细信息，请参阅[组织和团队角色](/help/workfront-fusion/references/licenses-and-roles/organization-roles.md)。
* 您创建的角色属于一个团队。

<!-- BECKY CHECK ME: The Slack thread says that defining a role that is available in all teams was out of scope for the initial release. Confirm that a role belongs to a single team, and that you clone it to use it in another team. -->
