---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 通过 Adobe Admin Console 向 Adobe Workfront Fusion 添加用户
description: You can add a user to the Adobe Admin Console and assign them to Adobe Workfront Fusion, or assign an existing user in the Adobe Admin Console to Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 7cb1c1a7-3c7a-459a-818f-d9cefcb9988b
source-git-commit: 6762806f17a0fc55531b647a84901b8ca572a997
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 20%

---

# 通过 Adobe Admin Console 向 Adobe Workfront Fusion 添加用户

You can add a user to the [!DNL Adobe Admin Console] and assign them to Adobe Workfront Fusion, or assign an existing user in the [!DNL Adobe Admin Console] to Workfront Fusion.

For a video describing Workfront Fusion in the [!DNL Adobe Admin Console], including how to add users, see [[!DNL Fusion] on Adobe IMS](https://video.tv.adobe.com/v/3412464/){target=_blank}.

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
  </tr>
   <tr> 
   <td role="rowheader">访问级别配置</td> 
   <td>You must be a Product Configuration Administrator of Adobe products for your organization.</td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++



## 先决条件

Before using the [!DNL Admin Console] for Workfront, you should receive a receive an email inviting you to the console.

* If you are new to [!DNL Adobe] and you have received an email telling you that you now have administer rights to manage [!DNL Adobe] software and services for your organization, click the button in the email to create an [!DNL Adobe] account and open the [!DNL Admin Console].

  或

  If you already have an Adobe account, go to the [[!DNL Adobe Admin Console] page](https://adminconsole.adobe.com).


## Add a new user to the [!DNL Adobe Admin Console] and Workfront Fusion

1. From the [[!DNL Adobe Admin Console] page](https://adminconsole.adobe.com/), select the **[!UICONTROL Products]** tab in the top navigation bar, and then select the **Workfront Fusion** product tile.

   ![Fusion in Admin Console](assets/fusion-product-admin-console.png)

1. In the list that displays, select the organization where you want to add a user.

   ![Fusion instance in Admin Console](assets/fusion-instances-admin-console.png)

1. In the list that displays, with the **[!UICONTROL Product Profiles]** tab selected, click the name of the Workfront Fusion [!UICONTROL Product Profile] link.

   >[!IMPORTANT]
   >
   > Do not make any changes to the [!UICONTROL Product Profile] itself.

1. With the **[!UICONTROL Users]** tab selected above the list, click **[!UICONTROL Add User]**.

1. In the **[!UICONTROL Add users to this product profile]** box, enter the email address or name of a user you want to add, then select the user in the list that appears.

1. 单击&#x200B;**[!UICONTROL 保存]**。

   The user is created in Workfront Fusion.

1. (Optional) Continue to [Change a user&#39;s access level in Workfront Fusion](#change-a-users-access-level-in-workfront-fusion).

## Change a user&#39;s access level in Workfront Fusion

* [Change a user&#39;s role to Admin](#change-a-users-role-to-admin)
* [Change a user&#39;s role to Member, Accountant, or App Developer](#change-a-users-role-to-member-accountant-or-app-developer)

### 将用户的角色更改为管理员

必须在[!DNL Adobe Admin Console]中为用户分配管理员角色。

1. 在您添加用户的Workfront Fusion [!UICONTROL 产品配置文件]页面上，选择&#x200B;**[!UICONTROL 管理员]**&#x200B;选项卡。

1. 单击&#x200B;**[!UICONTROL 添加管理员]**。

1. 在&#x200B;**[!UICONTROL 添加产品配置文件管理员]**&#x200B;框中，输入要成为管理员的用户的电子邮件地址或名称，然后在显示的列表中选择该用户。

1. 单击&#x200B;**[!UICONTROL 保存]**。

   用户现在是Workfront Fusion中的管理员。

### 将用户的角色更改为成员、会计或应用程序开发人员

在Workfront Fusion中处理成员、会计和应用程序开发人员角色。

有关说明，请参阅[查看或编辑用户角色](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md)。

## 将[!DNL Adobe Admin Console]中的现有用户分配给Workfront Fusion

您可以在Fusion中将现有用户添加到团队。 这在Fusion中处理。

有关说明，请参阅[将用户添加到团队](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md)。
