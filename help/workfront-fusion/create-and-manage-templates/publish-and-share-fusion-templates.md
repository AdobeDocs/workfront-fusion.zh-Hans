---
title: Publish和共享模板
description: 创建模板后，您的模板将可供所有团队成员使用。 如果要与团队外部的人员共享模板，则必须先发布该模板。
author: Becky
feature: Workfront Fusion
exl-id: 99a1227d-bff9-479f-b8b9-efcf7cea3708
source-git-commit: 7acc27ab2ce80b964b7f9fbb302816aa75964ab5
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 2%

---

# Publish和共享模板

创建模板后，您的模板将可供所有团队成员使用。 如果要与团队外部的人员共享模板，则必须先发布该模板。

有关创建模板的信息，请参阅[创建新模板](/help/workfront-fusion/create-and-manage-templates/create-new-fusion-templates.md)。

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
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

必须先创建模板，然后才能发布或共享。

## Publish模板

1. 在左侧导航面板中，单击&#x200B;**[!UICONTROL Templates]**。
1. 单击 **[!UICONTROL Team templates]** 选项卡。
1. 在要发布的模板行中单击&#x200B;**Publish**。

   或


   单击要发布的模板的名称，然后单击屏幕右上角的&#x200B;**[!UICONTROL Publish]**&#x200B;按钮。

## 共享[!DNL Workfront Fusion]模板

发布模板后，即可共享该模板。

1. 在左侧导航面板中，单击&#x200B;**[!UICONTROL Templates]**。
1. 单击 **[!UICONTROL Team templates]** 选项卡。
1. 单击要共享的模板名称以打开该模板。
1. 单击&#x200B;**已发布**&#x200B;选项卡以打开该版本的模板。
1. （视情况而定）如果您需要可共享链接，请单击&#x200B;**[!UICONTROL Share public link]**。

   >[!NOTE]
   >
   >尽管您可以共享此链接，但模板本身停留在[!UICONTROL Team templates]选项卡中并且不是公共的。

1. （视情况而定）如果您希望将模板公开，请单击&#x200B;**[!UICONTROL Request Approval]**&#x200B;以将其发送给管理员以供审批。

   >[!NOTE]
   >
   >* 模板获得批准后，即会公开。 [!UICONTROL Public templates]在所有[!DNL Workfront Fusion]用户的[!UICONTROL Public templates]选项卡中可见，无论组织或团队如何。
   >* 您的管理员不会收到通过电子邮件接收模板以进行审阅的通知。 如果批准情况紧急，请直接联系管理员。


## 模板状态

Fusion将不同的版本（“私有”、“已发布”和“已批准”）保存在模板页面的不同选项卡中。

可以使用以下状态：

* **[!UICONTROL Private]**：此模板仅对模板作者及其团队可见。
* **[!UICONTROL Published]**：此模板仅对模板作者及其团队可见。 您可以发送已发布的模板以供审批，并复制可共享链接。
* **[!UICONTROL Approved]**：此模板对[!UICONTROL Public templates]选项卡中的所有Workfront Fusion用户可见。 您可以通过单击屏幕右上角的[!UICONTROL Options]来复制可共享链接。

<!--You can also check the status from the [!UICONTROL Team templates] tab. If a template is published, it will have an icon to the right of the template name.

* **Eye icon**: The template is published, it is visible only for the team, and the approval request was not sent.
* **Yellow checkmark icon**: The template is published, it is visible only for the team, and the approval request was sent.
* **Green checkmark icon**: The template is published and public. It is visible for any Workfront Fusion user in the [!UICONTROL Public templates] tab. It is also still visible in the [!UICONTROL Team templates] tab, and the template author or their team member can still edit it.

Templates without icons have [!UICONTROL Private] status. They are not published and are visible only to the team.
-->
