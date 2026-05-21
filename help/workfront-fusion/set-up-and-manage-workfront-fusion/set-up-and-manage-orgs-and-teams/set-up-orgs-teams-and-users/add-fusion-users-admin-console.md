---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: get-started-with-workfront-fusion-2-0
title: 通过 Adobe Admin Console 向 Adobe Workfront Fusion 添加用户
description: 您可以将用户添加到Adobe Admin Console并将其分配给Adobe Workfront Fusion，或将Adobe Admin Console中的现有用户分配给Workfront Fusion。
author: Becky
feature: Workfront Fusion
exl-id: 7cb1c1a7-3c7a-459a-818f-d9cefcb9988b
TQID: https://experienceleague.adobe.com/jo9dNX5czLlg7Wi4iFBR6FlOM-fmM-i3zoEhh5sgsqc
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 607
ht-degree: 20%

---

# 通过 Adobe Admin Console 向 Adobe Workfront Fusion 添加用户

您可以将用户添加到[!DNL Adobe Admin Console]并将他们分配给Adobe Workfront Fusion，或将[!DNL Adobe Admin Console]中的现有用户分配给Workfront Fusion。

有关描述[!DNL Adobe Admin Console]中的Workfront Fusion的视频（包括如何添加用户），请参阅Adobe IMS[&#128279;](https://video.tv.adobe.com/v/3412464/){target=_blank}上的[!DNL Fusion] 。

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
   <td>您必须是贵组织的Adobe产品的产品配置管理员。</td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++



## 先决条件

在使用[!DNL Admin Console] for Workfront之前，您应该会收到一封邀请您加入控制台的电子邮件。

* 如果您是[!DNL Adobe]的新用户，并且已收到一封电子邮件，告知您现在拥有管理贵组织的[!DNL Adobe]软件和服务的管理权限，请单击电子邮件中的按钮以创建[!DNL Adobe]帐户并打开[!DNL Admin Console]。

  或

  如果您已经拥有Adobe帐户，请转到[[!DNL Adobe Admin Console] 页面](https://adminconsole.adobe.com)。


## 向[!DNL Adobe Admin Console]和Workfront Fusion添加新用户

1. 从[[!DNL Adobe Admin Console] 页面](https://adminconsole.adobe.com/)中，选择顶部导航栏中的&#x200B;**[!UICONTROL 产品]**&#x200B;选项卡，然后选择&#x200B;**Workfront Fusion**&#x200B;产品拼贴。

   Admin Console中的![Fusion](assets/fusion-product-admin-console.png)

1. 在显示的列表中，选择要添加用户的组织。

   Admin Console中的![Fusion实例](assets/fusion-instances-admin-console.png)

1. 在显示的列表中，选择&#x200B;**[!UICONTROL 产品配置文件]**&#x200B;选项卡，单击Workfront Fusion [!UICONTROL 产品配置文件]链接的名称。

   >[!IMPORTANT]
   >
   > 不要对[!UICONTROL 产品配置文件]本身进行任何更改。

1. 在列表上方选择&#x200B;**[!UICONTROL 用户]**&#x200B;选项卡，单击&#x200B;**[!UICONTROL 添加用户]**。

1. 在&#x200B;**[!UICONTROL 将用户添加到此产品配置文件]**&#x200B;框中，输入要添加的用户的电子邮件地址或名称，然后在显示的列表中选择该用户。

1. 单击&#x200B;**[!UICONTROL 保存]**。

   将在Workfront Fusion中创建用户。

1. （可选）继续在Workfront Fusion[&#128279;](#change-a-users-access-level-in-workfront-fusion)中更改用户的访问级别。

## 在Workfront Fusion中更改用户的访问级别

* [将用户的角色更改为管理员](#change-a-users-role-to-admin)
* [将用户的角色更改为成员、会计或应用程序开发人员](#change-a-users-role-to-member-accountant-or-app-developer)

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
