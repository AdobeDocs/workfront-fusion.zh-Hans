---
title: 在Adobe Workfront Fusion的HTTP模块中使用双向TLS
description: 您可以在Adobe Workfront Fusion HTTP模块中使用双方TLS，允许信息交易双方验证对方的身份。
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 89017451c8e0b821616adda861222127e100a08d
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# 在[!DNL Adobe Workfront Fusion]的HTTP模块中使用双向TLS

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

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求</p>
   <p>或</p>
   <p>旧版：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 提供您的[!DNL Workfront Fusion]公共证书

当您使用HTTP请求连接到Web服务时，Web服务通常需要[!DNL Workfront Fusion]公共证书才能进行验证。 这允许Web服务将HTTP请求中提供的证书与文件上的证书进行比较，以确保证书位于Web服务的允许列表上。

有关将[!DNL Adobe Workfront Fusion]公共证书上载到Web服务的说明，请参阅Web服务的文档。

>[!NOTE]
>
>除了证书之外，您可能需要提供其他信息。 有关Web服务需要什么的信息，请参阅Web服务的API文档。

您可以使用以下链接下载Workfront Fusion公共证书。 列入允许列表要查找数据中心，请参阅组织的“为Fusion配置IP地址”一文中的[识别数据中心](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)。

### 2025年证书

>[!IMPORTANT]
>
>* 这些[!DNL Workfront Fusion]公共证书将在&#x200B;**2026年4月4日**（美国和EU）或&#x200B;**2025年11月25日**(Azure)过期。 您的证书过期后，您需要向Web服务上传新证书。 我们建议您：
>
>   * 记下过期日期，并设置一个提醒，提醒您自己将证书上传到您的Web服务。
>   * 将此页加入书签以轻松查找新证书。
>
>* 这些是非通配符mTLS证书。

| 数据中心 | 下载链接 | 日期有效 |
|---|---|---|
| 美国数据中心 | [下载 [!DNL Workfront Fusion] 美国证书2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-us-mtls-certificate.pem) | 2025年3月3日至2026年4月4日 |
| 欧盟数据中心 | [下载 [!DNL Workfront Fusion] EU证书2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-eu-mtls-certificate.pem) | 2025年3月3日至2026年4月4日 |
| Azure群集 | [下载 [!DNL Workfront Fusion] Azure证书2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-az-mtls-certificate.pem) | 2024年10月24日至2025年11月25日 |

<!--

### Certificates for 2024

>[!IMPORTANT]
>
>* We recommend installing the certificates for 2025, available above.
>* These [!DNL Workfront Fusion] public certificates expire on **May 7, 2025**. After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
|---|---|---|
| US Datacenter | [Download [!DNL Workfront Fusion] Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |
| EU Datacenter | [Download [!DNL Workfront Fusion] EU Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |

-->

## 在[!DNL Workfront Fusion] HTTP模块中启用双向TLS

所有[!DNL Workfront Fusion] [!UICONTROL HTTP]请求模块都可以选择启用双向TLS。

要在[!UICONTROL HTTP]请求模块中启用双向TLS，请执行以下操作：

1. 向方案添加[!UICONTROL HTTP]请求模块。
1. 开始配置模块。

   有关配置[!UICONTROL HTTP]请求模块的说明，请参阅[通用连接器](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)下的相应文章。

1. 在模块底部附近启用&#x200B;**[!UICONTROL 显示高级设置]**。
1. 启用&#x200B;**[!UICONTROL 使用双向TLS]**。
