---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 通过Adobe Admin Console将用户添加到Adobe Workfront Fusion
description: 您可以将用户添加到Adobe Admin Console并将其分配给Adobe Workfront Fusion，或将Adobe Admin Console中的现有用户分配给Workfront Fusion。
author: Becky
feature: Workfront Fusion
exl-id: 7cb1c1a7-3c7a-459a-818f-d9cefcb9988b
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 2%

---

# 通过Adobe Admin Console将用户添加到Adobe Workfront Fusion

您可以将用户添加到[!DNL Adobe Admin Console]并将其分配给[!DNL Adobe Workfront Fusion]，或将[!DNL Adobe Admin Console]中的现有用户分配给[!DNL Workfront Fusion]。

有关描述[!DNL Adobe Admin Console]中的[!DNL Workfront Fusion]的视频（包括如何添加用户），请参阅Adobe IMS[&#128279;](https://video.tv.adobe.com/v/3412464/){target=_blank}上的[!DNL Fusion] 。



您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 计划*</td> 
   <td> <p>[!UICONTROL Pro] 或更高</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td> 
   <td> <p>[!UICONTROL Plan]， [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前许可证要求：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Adobe Workfront]计划，则贵组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[!UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td> 
  </tr>
   <tr> 
   <td role="rowheader">[!DNL Adobe] 管理员权限</td> 
   <td>对于您的组织，您必须是[!UICONTROL Product Configuration Administrator]个产品（共[!DNL Adobe]个）。</td> 
  </tr>
  </tbody> 
</table>

&#42;要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

&#42;&#42;有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。



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


## 先决条件

在使用[!DNL Workfront]的[!DNL Admin Console]之前，您应该会收到一封邀请您加入控制台的电子邮件。

1. 如果您是[!DNL Adobe]的新用户，并且已收到一封电子邮件，告知您现在拥有管理贵组织的[!DNL Adobe]软件和服务的管理权限，请单击电子邮件中的按钮以创建[!DNL Adobe]帐户并打开[!DNL Admin Console]。

   或

   如果您已有Adobe帐户，请转到[[!DNL Adobe Admin Console] 页面](https://adminconsole.adobe.com)。


## 向[!DNL Adobe Admin Console]和[!DNL Workfront Fusion]添加新用户

1. 从[[!DNL Adobe Admin Console] 页面](https://adminconsole.adobe.com/)中，选择顶部导航栏中的&#x200B;**[!UICONTROL Products]**&#x200B;选项卡，然后选择&#x200B;**[!DNL Workfront Fusion]**&#x200B;产品拼贴。

   Admin Console![&#128279;](assets/fusion-product-admin-console.png)中的Fusion

1. 在显示的列表中，选择要添加用户的组织。

   Admin Console![&#128279;](assets/fusion-instances-admin-console.png)中的Fusion实例

1. 在显示的列表中，选择&#x200B;**[!UICONTROL Product Profiles]**&#x200B;选项卡，单击[!DNL Workfront Fusion] [!UICONTROL Product Profile]链接的名称。

   >[!IMPORTANT]
   >
   > 不要对[!UICONTROL Product Profile]本身进行任何更改。

1. 在列表上方选择&#x200B;**[!UICONTROL Users]**&#x200B;选项卡后，单击&#x200B;**[!UICONTROL Add User]**。

1. 在&#x200B;**[!UICONTROL Add users to this product profile]**&#x200B;框中，输入要添加的用户的电子邮件地址或名称，然后在显示的列表中选择该用户。

1. 单击 **[!UICONTROL Save]**。

   已在[!DNL Workfront Fusion]中创建用户。

1. （可选）继续[在 [!DNL Workfront Fusion]](#change-a-users-access-level-in-workfront-fusion)中更改用户的访问级别

## 在Workfront Fusion中更改用户的访问级别

* [将用户的角色更改为管理员](#change-a-users-role-to-admin)
* [将用户的角色更改为成员、会计或应用程序开发人员](#change-a-users-role-to-member-accountant-or-app-developer)

### 将用户的角色更改为管理员

必须在[!DNL Adobe Admin Console]中为用户分配管理员角色。

1. 在添加用户的[!DNL Workfront Fusion] [!UICONTROL Product Profile]页面上，选择&#x200B;**[!UICONTROL Admins]**&#x200B;选项卡。

1. 单击 **[!UICONTROL Add Admin]**。

1. 在&#x200B;**[!UICONTROL Add product profile administrators]**&#x200B;框中，输入要成为管理员的用户的电子邮件地址或名称，然后在显示的列表中选择该用户。

1. 单击 **[!UICONTROL Save]**。

   该用户现在是[!DNL Workfront Fusion]中的管理员。

### 将用户的角色更改为成员、会计或应用程序开发人员

在Workfront Fusion中处理成员、会计和应用程序开发人员角色。

有关说明，请参阅[查看或编辑用户角色](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/manage-users-and-teams/view-or-edit-user-roles.md)。

## 将[!DNL Adobe Admin Console]中的现有用户分配给[!DNL Workfront Fusion]

您可以在Fusion中将现有用户添加到团队。 这在Fusion中处理。

有关说明，请参阅[将用户添加到团队](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/add-a-user-to-a-team.md)。
