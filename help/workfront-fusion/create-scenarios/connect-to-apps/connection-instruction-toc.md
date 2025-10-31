---
title: 创建连接
description: 连接必须遵循它所连接的应用程序或Web服务的API所设置的要求。 因此，设置连接的说明因应用程序或Web服务而异。 本文可帮助您识别和查找有关将Adobe Workfront Fusion连接到所选应用程序或Web服务的说明。
author: Becky
feature: Workfront Fusion
exl-id: 281403a6-6f88-4976-8a10-1d0848ef9b35
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---

# 创建连接

连接必须遵循它所连接的应用程序或Web服务的API所设置的要求。 因此，设置连接的说明因应用程序或Web服务而异。 本文可帮助您识别和查找有关将Adobe Workfront Fusion连接到所选应用程序或Web服务的说明。

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

## 连接到不需要配置的应用程序或Web服务

在大多数情况下，您可以使用模块创建几乎没有或没有额外信息的连接。 Workfront Fusion会自动处理身份验证。

有关创建无特殊注意事项的连接的说明，请参阅[创建连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)。

## 连接到Adobe应用程序或服务

要连接到Adobe应用程序或服务，您可能需要Adobe Admin Console中的信息，例如您的组织ID或技术帐户ID。

您还可以使用Adobe Authenticator模块通过单个连接连接到任何Adobe API。 这允许您更轻松地连接到尚未拥有专用Fusion连接器的Adobe产品。

有关具体说明，请参阅连接器的[文章](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-adobe-products)。

## 连接到[!DNL Microsoft]应用或Web服务

Workfront Fusion中的大多数[!DNL Microsoft]应用都允许您创建无额外信息的连接。

以下情况需要在创建连接时执行额外的步骤：

* 使用Microsoft Dynamics 365模块。

  有关说明，请参阅[Microsoft Dynamics 365模块](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md)。

* 使用HTTP模块连接到Microsoft Graph API

  有关说明，请参阅[调用MS Graph REST API](/help/workfront-fusion/create-scenarios/connect-to-apps/call-the-ms-graph-rest-api.md)。

## 连接到[!DNL Google]应用或Web服务

根据您使用的[!DNL Google]帐户类型，连接到[!DNL Google]应用的进程可能会有所不同。 此外，在连接到Workfront Fusion时，[!DNL Google]安全措施可能需要额外的配置。

有关更多信息，请参阅：

* [使用自定义OAuth客户端将Adobe Workfront Fusion连接到Google Services](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)
* [使用更新的安全措施将Adobe Workfront Fusion连接到Google服务](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-google-with-new-security-measures.md)

## 需要其他配置的其他应用程序

某些应用程序和服务不遵循Workfront Fusion连接的基本配置。 您可以在文章中找到有关连接这些应用程序的说明。

有关具体说明，请参阅连接器的[文章](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#connectors-for-third-party-applications)。
