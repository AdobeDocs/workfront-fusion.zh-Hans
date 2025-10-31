---
title: 创建连接 — 基本说明
description: 许多Adobe Workfront Fusion连接器在创建连接时不需要自定义配置。 本文介绍了默认连接创建过程。
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# 创建连接 — 基本说明

许多Adobe Workfront Fusion连接器在创建连接时不需要自定义配置。 本文介绍了默认连接创建过程。

>[!NOTE]
>
>
>如果Adobe Workfront Fusion不为您要在场景中使用的Web服务提供应用程序，则可使用Workfront Fusion HTTP和Webhooks模块连接到Web服务，如以下文章所述：
>
>* [将Adobe Workfront Fusion连接到使用API令牌授权的Web服务](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [为没有连接器的Web服务配置webhook](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

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
   <td role="rowheader">Adobe Workfront Fusion许可证</td> 
   <td>
   <p>基于操作：不需要Workfront Fusion许可证</p>
   <p>基于连接器（旧版）：要连接到Workfront产品系列之外的应用程序，您必须具有Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 创建连接

要创建与给定应用程序的连接，您必须处于该应用程序的模块中。 例如，要创建与Workfront的连接，您必须在Workfront模块中。

要在Workfront Fusion模块中创建连接，请执行以下操作：

1. 在给定应用程序的任意模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;框旁边的[!UICONTROL 添加]以打开&#x200B;**[!UICONTROL 创建连接]**&#x200B;面板。
1. （可选）更改默认&#x200B;**[!UICONTROL 连接名称]**。
1. 在环境字段中，选择是生产环境还是非生产环境。
1. 在“类型”字段中，选择此帐户是服务帐户还是个人帐户。
1. （有条件）如果应用程序需要高级连接设置（如ID、密钥或[!UICONTROL 密钥]），请输入该信息。

   您可能需要单击&#x200B;**[!UICONTROL 显示高级设置]**&#x200B;以显示可在其中输入此类信息的字段。

1. 单击&#x200B;**[!UICONTROL 继续]**。
1. 在显示的登录窗口中，输入您的凭据以登录应用程序（如果尚未登录）。
1. （视情况而定）如果显示&#x200B;**[!UICONTROL 允许]**&#x200B;按钮，请检查连接器能够执行的操作，然后单击按钮以将应用程序连接到Workfront Fusion。

   >[!NOTE]
   >
   >* “环境”和“类型”字段仅供参考，不会更改连接的功能。 此信息显示在Fusion的“连接”区域中，允许您确定要在组织中的给定用例中使用的连接。
   >* 某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
   >
   >   例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。
