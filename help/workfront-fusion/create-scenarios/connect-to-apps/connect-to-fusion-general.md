---
title: 创建连接 — 基本说明
description: 许多 [!DNL Adobe Workfront Fusion] 连接器在创建连接时不需要自定义配置。 本文介绍了默认连接创建过程。
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 1%

---

# 创建连接 — 基本说明

许多[!DNL Adobe Workfront Fusion]连接器在创建连接时不需要自定义配置。 本文介绍了默认连接创建过程。

>[!NOTE]
>
>
>如果Adobe Workfront Fusion不为您要在场景中使用的Web服务提供应用程序，则可使用[!DNL Workfront Fusion] HTTP和Webhooks模块连接到Web服务，如以下文章所述：
>
>* [将Adobe Workfront Fusion连接到使用API令牌授权的Web服务](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [为没有连接器的Web服务配置webhook](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront计划：包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 创建连接

要在[!DNL Workfront Fusion]模块内创建连接，请执行以下操作：

1. 单击[!UICONTROL Connection]框旁的&#x200B;**[!UICONTROL Add]**&#x200B;以打开&#x200B;**[!UICONTROL Create a connection]**&#x200B;面板。
1. （可选）更改默认&#x200B;**[!UICONTROL Connection name]**。
1. （有条件）如果应用程序需要高级连接设置（如ID、键或[!UICONTROL secret]），请输入该信息。

   您可能需要单击&#x200B;**[!UICONTROL Show advanced settings]**&#x200B;以显示可在其中输入此类信息的字段。

1. 单击 **[!UICONTROL Continue]**。
1. 在显示的登录窗口中，输入您的凭据以登录应用程序（如果尚未登录）。
1. （视情况而定）如果显示&#x200B;**[!UICONTROL Allow]**&#x200B;按钮，请检查连接器能够执行的操作，然后单击按钮以将应用程序连接到[!DNL Workfront Fusion]。

   >[!NOTE]
   >
   >某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
   >
   >例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。
