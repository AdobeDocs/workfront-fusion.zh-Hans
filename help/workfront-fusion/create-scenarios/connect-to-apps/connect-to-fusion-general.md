---
title: 创建连接 — 基本说明
description: Many Adobe Workfront Fusion connectors do not require custom configuration when creating a connection. This article describes the default connection creation process.
author: Becky
feature: Workfront Fusion
exl-id: e47ab4d9-6612-4d9a-a024-da508a8bbfb2
source-git-commit: bbd1ec27e52127c8814188612a1e8d5cfab0cd25
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 21%

---

# 创建连接 — 基本说明

Many Adobe Workfront Fusion connectors do not require custom configuration when creating a connection. This article describes the default connection creation process.

>[!NOTE]
>
>
>If Adobe Workfront Fusion doesn&#39;t offer an app for the web service you would like to use in your scenario, you can connect to the web service using Workfront Fusion HTTP and Webhooks modules, as explained in the following articles:
>
>* [Connect Adobe Workfront Fusion to a web service that uses API token authorization](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-wf-web-service-uses-api-token-auth.md)
>* [Configure a webhook for a web service without a connector](/help/workfront-fusion/create-scenarios/add-modules/receive-a-webhook-from-a-web-service.md)

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
   <td role="rowheader">Adobe Workfront Fusion 许可证</td> 
   <td>
   <p>基于操作：不需要 Workfront Fusion 许可证</p>
   <p>Connector-based (legacy): To connect to applications outside the Workfront family of products, you must have Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

有关 Adobe Workfront Fusion 许可证的详细信息，请参阅 [Adobe Workfront Fusion 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## Create a connection

To create a connection to a given application, you must be in a module for that application. For example, to create a connection to Workfront, you must be in a Workfront module.

To create a connection inside a Workfront Fusion module:

1. In any module for the given application, click **[!UICONTROL Add]** next to the [!UICONTROL Connection] box to open the **[!UICONTROL Create a connection]** panel.
1. (Optional) Change the default **[!UICONTROL Connection name]**.
1. In the Environment field, select whether this is a production or non-production environment.
1. In the Type field, select whether this is a service or personal account.
1. (Conditional) If the app requires advanced connection settings, such as an ID, key, or [!UICONTROL secret], enter that information.

   You may need to click **[!UICONTROL Show advanced settings]** to display the fields where you can enter this kind of information.

1. 单击&#x200B;**[!UICONTROL 继续]**。
1. In the sign-in window that displays, enter your credentials to log in to the app if you haven&#39;t already done so.
1. (Conditional) If an **[!UICONTROL Allow]** button displays, examine the actions that the connector will be able to take, then click the button to connect the app to Workfront Fusion.

   >[!NOTE]
   >
   >* The Environment and Type fields are for information only and do not change the functionality of the connection. This information appears in the Connections area of Fusion, allowing you to determine which connection to use for a given use case in your organization.
   >* 某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
   >
   >   例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。
