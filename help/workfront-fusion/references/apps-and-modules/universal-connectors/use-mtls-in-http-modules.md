---
title: 在 Adobe Workfront Fusion 的 HTTP 模块中使用双向 TLS
description: 您可以在Adobe Workfront Fusion HTTP模块中使用双方TLS，允许信息交易双方验证对方的身份。
author: Becky
feature: Workfront Fusion
exl-id: 1e0b4c3b-9a0b-491d-aaf2-0011d8386abe
source-git-commit: 6a4bf090e7804f0b2b9ca6eefbb7490d1c35b6ce
workflow-type: tm+mt
source-wordcount: '866'
ht-degree: 16%

---

# 在 Adobe Workfront Fusion 的 HTTP 模块中使用双向 TLS

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
   <p>基于连接器（旧版）：Workfront Fusion for Work Automation and Integration </p>
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

## 提供您的Workfront Fusion公共证书

当您使用HTTP请求连接到Web服务时，Web服务通常需要Workfront Fusion公共证书来进行验证。 这允许Web服务将HTTP请求中提供的证书与文件上的证书进行比较，以确保证书位于Web服务的允许列表上。

有关将Adobe Workfront Fusion公共证书上传到Web服务的说明，请参阅Web服务的文档。

>[!NOTE]
>
>除了证书之外，您可能需要提供其他信息。 有关Web服务需要什么的信息，请参阅Web服务的API文档。

您可以使用以下链接下载Workfront Fusion公共证书。 列入允许列表要查找数据中心，请参阅组织的“为Fusion配置IP地址”一文中的[识别数据中心](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)。

### 2026年证书

>[!IMPORTANT]
>
>* 这些Workfront Fusion公共证书的过期日期各不相同，具体取决于您的集群。 请查看下图以查看您的过期时间。 过期后，您需要向Web服务上传新证书。 我们建议您：
>
>   * 记下过期日期，并设置一个提醒，提醒您自己将证书上传到您的Web服务。
>   * 将此页加入书签以轻松查找新证书。
>
>* 这些是非通配符mTLS证书。

| 数据中心 | 下载链接 | 日期有效 |
| --- | --- | --- |
| 美国AWS数据中心 | [下载Workfront Fusion US证书2026](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-us-mtls-certificate-2026.pem) | 2026年1月29日至2027年3月2日 |
| US Azure群集 | [下载Workfront Fusion US Azure证书2026](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-az-mtls-certificate.pem) | 2025年9月21日至2026年10月23日 |
| 欧盟AWS数据中心 | [下载Workfront Fusion EU证书2026](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-eu-mtls-certificate-2026.pem) | 2026年1月29日至2027年3月2日 |
| EU Azure群集 | [下载Workfront Fusion EU Azure证书2026](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2026-certs/fusion-prod-eu-az-mtls-certificate-2026.pem) | 2026年2月4日至2027年3月8日 |


### 2025年证书

>[!IMPORTANT]
>
>* 我们建议安装2026年的证书，如上所示。
>* 这些Workfront Fusion公共证书将在&#x200B;**2026年4月4日**（美国和EU）或&#x200B;**2025年11月25日**(Azure)过期。 您的证书过期后，您需要向Web服务上传新证书。 我们建议您：
>
>   * 记下过期日期，并设置一个提醒，提醒您自己将证书上传到您的Web服务。
>   * 将此页加入书签以轻松查找新证书。
>
>* 这些是非通配符mTLS证书。

| 数据中心 | 下载链接 | 日期有效 |
| --- | --- | --- |
| 美国数据中心 | [下载Workfront Fusion US证书2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-us-mtls-certificate.pem) | 2025年3月3日至2026年4月4日 |
| 欧盟数据中心 | [下载Workfront Fusion EU证书2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-eu-mtls-certificate.pem) | 2025年3月3日至2026年4月4日 |
| Azure群集 | [下载Workfront Fusion Azure证书2025](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/2025-certs/fusion-prod-az-mtls-certificate.pem) | 2024年10月24日至2025年11月25日 |

<!--

### Certificates for 2024

>[!IMPORTANT]
>
>* We recommend installing the certificates for 2025, available above.
>* These Workfront Fusion public certificates expire on **May 7, 2025**. After yours expires you will need to upload a new certificate to the web service. We recommend that you:
>
>   * Make note of the expiration date and set a reminder for yourself to upload the certificate to your web service.
>   * Bookmark this page to easily find the new certificates.
>
>* These are non-wildcard mTLS certificates.

| Datacenter | Download link | Dates valid |
|---|---|---|
| US Datacenter | [Download Workfront Fusion Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-us-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |
| EU Datacenter | [Download Workfront Fusion EU Certificate 2024](/help/workfront-fusion/references/apps-and-modules/universal-connectors/assets/fusion-prod-eu-mtls-certificate.pem) | April 5, 2024 to May 7, 2025 |

-->

## 在Workfront Fusion HTTP模块中启用双向TLS

所有Workfront Fusion [!UICONTROL HTTP]请求模块都可以选择启用双向TLS。

要在[!UICONTROL HTTP]请求模块中启用双向TLS，请执行以下操作：

1. 向方案添加[!UICONTROL HTTP]请求模块。
1. 开始配置模块。

   有关配置[!UICONTROL HTTP]请求模块的说明，请参阅[通用连接器](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)下的相应文章。

1. 在模块底部附近启用&#x200B;**[!UICONTROL 显示高级设置]**。
1. 启用&#x200B;**[!UICONTROL 使用双向TLS]**。
