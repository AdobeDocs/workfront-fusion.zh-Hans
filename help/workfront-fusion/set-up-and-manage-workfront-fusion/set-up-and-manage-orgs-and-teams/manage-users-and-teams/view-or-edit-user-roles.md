---
title: 管理组织中的Adobe Workfront Fusion用户
description: 管理组织中的Adobe Workfront Fusion用户
author: Becky
feature: Workfront Fusion
exl-id: 32c221fa-856b-4921-9fa6-5e60f2aa08cd
source-git-commit: 3f9390d8947ef2666336c1a4cc6eab8d174849d5
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 18%

---

# 查看或编辑用户角色

Adobe Workfront Fusion管理员可以管理Workfront Fusion中的用户角色。


>[!NOTE]
>
>如果贵组织当前正在迁移到Adobe Admin Console，则您无法在Workfront中管理用户（添加或删除用户）。 迁移完成后，您可以在Adobe Admin Console中执行这些操作。

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
   <td role="rowheader">访问级别配置</td> 
   <td> 
     <p>您必须是组织的Workfront Fusion管理员。</p>
     <p>您必须是团队的Workfront Fusion管理员。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 查看或编辑组织的用户角色

Adobe Workfront Fusion管理员可以查看和更新组织的用户角色。

1. 以Workfront Fusion管理员身份登录时，在左侧导航中选择&#x200B;**[!UICONTROL 所有用户]**。
1. 在要查看的用户行中单击&#x200B;**[!UICONTROL 详细信息]**。
1. （可选）要更新组织中用户的角色，请在要更改用户角色的组织行中单击&#x200B;**[!DNL Role]**&#x200B;列中的下拉菜单，然后选择新角色。

### 添加或更改组织所有者时的注意事项

您的组织可以有多个所有者。

将用户分配给所有者角色或从所有者角色分配用户时，请考虑以下事项。

* 只有责任人才能分配责任人角色，或将另一个角色分配给当前责任人。
* 只有管理员可以升级到所有者。
* 如果只有一个所有者，则无法更改或删除该所有者角色。
* 如果只有一个“所有者”，则在组织中有其他用户时，无法删除该“所有者”。
* 为管理员分配所有者角色后，他们会自动成为组织内所有团队的管理员。
* 当所有者被分配给另一个角色时，该用户会自动成为所有团队中的团队成员。
* 创建新团队后，所有所有者都会被自动分配为团队管理员。

## 查看或编辑团队的用户角色

Adobe Workfront Fusion管理员和团队管理员可以查看和更新用户角色。

1. 以Workfront Fusion管理员身份登录时，在左侧导航中选择&#x200B;**[!UICONTROL 所有用户]**。
1. 在要查看的用户行中单击&#x200B;**[!UICONTROL 详细信息]**。
1. 在包含要查看或编辑用户角色的团队的组织行中，单击&#x200B;**[!DNL Role]**&#x200B;列中的“团队”图标。
1. （可选）要更新团队中用户的角色，请单击团队中要更改用户角色的行&#x200B;**[!DNL Role]**&#x200B;列中的下拉列表，然后选择新角色。
