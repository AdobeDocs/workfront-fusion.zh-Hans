---
title: 在Adobe Workfront Fusion的HTTP模块中使用双向TLS
description: 您可以在Adobe Workfront Fusion HTTP模块中使用双方TLS，允许信息交易双方验证对方的身份。
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 0%

---

# 在[!DNL Adobe Workfront Fusion]的HTTP模块中使用双向TLS

>[!NOTE]
>
>除了Adobe Workfront许可证之外，Adobe Workfront Fusion还需要[!DNL Adobe Workfront Fusion]许可证。

## 双向TLS概述

通过Internet发送数据时，确保数据到达或来自正确位置，并且只有目标收件人才能阅读这些数据非常重要。 启用TLS后，客户端（请求信息的计算机）使用证书来验证服务器的身份（提供信息的计算机）。 这样可以建立安全的HTTP连接。

双向TLS允许此身份确认双向进行。 当服务器向客户端发送其证书以验证其身份时，它还会请求客户端的证书。 这可确保服务器不会将信息发送给会滥用该信息的站点或用户。

>[!INFO]
>
>**示例：**
>
>* **TLS**：当有人在浏览器中键入“MyGreatBank.com”时，他们希望确保自己将转到“我的伟大银行”，而不是一个可能滥用或出售其银行信息的网站。 他们还想确保自己的银行账户信息被加密。
>
>   当浏览器（客户端）连接到MyGreatBank.com （服务器）时，TLS需要来自MyGreatBank.com的证书来验证其身份。 证书由证书颁发机构（如[!DNL DigiCert]或[!DNL Thawte]）提供。 由于浏览器信任证书颁发机构，因此允许连接。
>
>* **双方TLS**： MySoftware.com是一个软件客户端，它需要来自MyGreatBank.com API的信息。 MyGreatBank仅允许受信任的客户连接到其服务器。 因此，除了常规TLS验证MyGreatBank.com的标识外，TLS/证书颁发机构进程还将验证MySoftware.com的请求。

## 访问要求

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
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Adobe Workfront]计划，则您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[!UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

&#42;要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

&#42;&#42;有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)

## 提供您的[!DNL Workfront Fusion]公共证书


当您使用HTTP请求连接到Web服务时，Web服务通常需要[!DNL Workfront Fusion]公共证书才能进行验证。 这允许Web服务将HTTP请求中提供的证书与文件上的证书进行比较，以确保证书位于Web服务的允许列表上。

有关将[!DNL Adobe Workfront Fusion]公共证书上载到Web服务的说明，请参阅Web服务的文档。

>[!NOTE]
>
>除了证书之外，您可能需要提供其他信息。 有关Web服务需要什么的信息，请参阅Web服务的API文档。

您可以使用以下链接下载Workfront Fusion公共证书：

### 2023年4月23日至2024年5月7日证书

>[!IMPORTANT]
>
>* 这[!DNL Workfront Fusion]个公共证书将于2025年5月7日到期。 您的证书过期后，您需要向Web服务上传新证书。 我们建议您：
>
>   * 记下过期日期，并设置一个提醒，提醒您自己将证书上传到您的Web服务。
>   * 将此页加入书签以轻松查找新证书。
>
>* 这些是非通配符mTLS证书。

* [下载 [!DNL Workfront Fusion] 证书2023](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem)
* [下载 [!DNL Workfront Fusion] EU证书2023](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem)

  在欧盟使用

<!--

### Certificates for November 14, 2022 - July 15, 2023

>[!IMPORTANT]
>
>* These [!DNL Workfront Fusion] public certificates expire on July 15, 2023.
>* These are wildcard mTLS certificates.

* [Download [!DNL Workfront Fusion] Certificate 2023](https://cdn.experience.workfront.com/Documentation/Workfront+Fusion+2.0+public+certificates/app_workfrontfusion_com-jul-15-2023+updated.cer)
* [Download [!DNL Workfront Fusion] EU Certificate 2023](https://cdn.experience.workfront.com/Documentation/Workfront+Fusion/app-eu_workfrontfusion_com-jul-15-2023.cer)

   For use in the EU 

   -->

## 在[!DNL Workfront Fusion] HTTP模块中启用双向TLS

所有[!DNL Workfront Fusion] [!UICONTROL HTTP]请求模块都可以选择启用双向TLS。

要在[!UICONTROL HTTP]请求模块中启用双向TLS，请执行以下操作：

1. 将[!UICONTROL HTTP]请求模块添加到您的方案。
1. 开始配置模块。

   <!--For instructions on configuring an [!UICONTROL HTTP] request module, see the appropriate article under [[!UICONTROL Universal connectors] modules](/help/workfront-fusion/references/apps-and-modules/universal-connectors/).-->

1. 在模块底部附近启用&#x200B;**[!UICONTROL Show advanced settings]**。
1. 启用&#x200B;**[!UICONTROL Use Mutual TLS]**。
