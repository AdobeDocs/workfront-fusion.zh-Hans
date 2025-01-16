---
title: JWT模块
description: ' [!DNL Adobe Workfront Fusion] [!UICONTROL JWT]应用程序提供了一个模块，该模块根据提供的算法创建JWT令牌。'
author: Becky
feature: Workfront Fusion
exl-id: 380f60db-b2ec-411a-86ee-0d5699f19b41
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# [!UICONTROL JWT]模块

[!DNL Adobe Workfront Fusion] [!UICONTROL JWT]应用程序提供了一个模块，该模块基于提供的算法创建JWT令牌。

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
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成]，[!UICONTROL [!DNL Workfront Fusion]用于工作自动化]</p>
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

要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## JWT API信息

JWT连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
   <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.1.5</td> 
  </tr>
 </tbody> 
 </table>

## JWT模块及其字段

### 生成JWT

此模块基于所选算法生成JWT。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Algorithm]</td> 
   <td> <p>选择要生成JWT的算法。</p> <ul>
   <li><b>HS256</b>：使用SHA-256哈希算法的HMAC</li>
   <li><b>HS384</b>：使用SHA-384哈希算法的HMAC</li>
   <li><b>HS512</b>：使用SHA-512哈希算法的HMAC</li>
   <li><b>RS256</b>：使用SHA-256哈希算法的RSASSA-PKCS1-v1_5</li>
   <li><b>RS384</b>：使用SHA-384哈希算法的RSASSA-PKCS1-v1_5</li>
   <li><b>RS512</b>：使用SHA-512哈希算法的RSASSA-PKCS1-v1_5</li>
   <li><b>PS256</b>：使用SHA-256哈希算法的RSASSA-PSS（仅节点^6.12.0或&gt;=8.0.0）</li>
   <li><b>PS384</b>：使用SHA-384哈希算法的RSASSA-PSS（仅节点^6.12.0或&gt;=8.0.0）</li>
   <li><b>PS512</b>：使用SHA-512哈希算法的RSASSA-PSS（仅节点^6.12.0或&gt;=8.0.0）</li>
   <li><b>ES256</b>：使用P-256曲线和SHA-256哈希算法的ECDSA</li>
   <li><b>ES384</b>：使用P-384曲线和SHA-384哈希算法的ECDSA</li>
   <li><b>ES512</b>：使用P-521曲线和SHA-512哈希算法的ECDSA</li>
   </ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload] </td> 
   <td> <p>对于每个要添加的有效负荷项，单击<b>添加项</b>并输入该项的键和值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Options] </td> 
   <td> <p>对于要添加的每个选项项，单击<b>添加项</b>并输入该项的键和值。</p> <p>可以使用以下键：
   <ul>
   <li><b>算法</b>： （默认值： RS256）</li>
   <li><b>expiresIn</b>：以秒或描述时间跨度（例如，2天、10小时、7天）的字符串表示。 数值将解释为秒计数。 如果使用字符串，请确保提供时间单位（天、小时等），否则默认使用毫秒单位（120等于120毫秒）。</li>
   <li><b>notBefore</b>：以秒为单位或以描述时间范围（如2天、10小时、7天）的字符串表示。 数值将解释为秒计数。 如果使用字符串，请确保提供时间单位（天、小时等），否则默认使用毫秒单位（120等于120毫秒）。
</li>
   <li><b>受众</b></li>
   <li><b>发行者</b></li>
   <li><b>jwtid</b></li>
   <li><b>主题</b></li>
   <li><b>noTimestamp</b></li>
   <li><b>标题</b></li>
   <li><b>keyid</b></li>
   <li><b>mutatePayload</b>：如果<code>true</code>，则符号函数将直接修改有效负载对象。 如果在应用声明后但在将其编码为令牌之前需要原始引用有效负载，则可以使用此功能。</li>
   <li><b>allowInsecureKeySizes</b>：如果<code>true</code>，则允许模数低于2048的私钥用于RSA。</li>
   <li><b>allowInvalidAsymmetricKeyTypes</b>：如果<code>true</code>，则允许与指定算法不匹配的非对称密钥。 此选项仅用于向后兼容，应当避免。</li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>
