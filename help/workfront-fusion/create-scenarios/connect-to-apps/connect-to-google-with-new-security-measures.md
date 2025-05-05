---
title: 使用更新的安全措施将Adobe Workfront Fusion连接到Google服务
description: Google对用户使用其API的方式引入了限制。 本文介绍了如何将Adobe Workfront Fusion连接到Google，并说明了这些更新安全措施。
author: Becky
feature: Workfront Fusion
exl-id: eac7ba26-664e-464c-b05c-8c2ebf407fb3
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# 使用更新的安全措施将Adobe Workfront Fusion连接到Google服务

Google对用户使用其API的方式引入了限制。 本文介绍了如何将Adobe Workfront Fusion连接到Google，并说明了这些更新安全措施。

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
   <p>当前：无Workfront Fusion许可证要求</p>
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

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## Google服务限制

自2020年6月1日起，Google对用户使用其API的方式引入了限制。 这些安全措施可保护Google用户免遭在Google上泄露或滥用其个人数据。

这些限制与Gmail和Google Drive应用程序相关。

有关这些限制的详细信息，请参阅[Google API服务用户数据策略](https://developers.google.com/terms/api-services-user-data-policy#additional_requirements_for_specific_api_scopes)中的“特定API范围的其他要求”

要访问受限范围，连接的服务(Adobe Workfront Fusion或通过API访问用户数据的任何其他服务)必须经过验证，并且必须拥有评估书来证明服务在使用数据方面的安全性和透明度。 Workfront Fusion符合Google对访问受限作用域的所有要求。 但是，Workfront Fusion中的大多数第三方连接服务没有评估书，因此不符合Google条款。 因此，Workfront Fusion不允许将数据发送到这些服务。

## Google服务限制的例外

有一些例外情况可能会将数据发送到没有评估书的未经批准的第三方服务，而不违反任何新限制。 这些控件的不同之处在于，Google Workspace与Workfront Fusion OAuth客户端以及Google Workspace与另一个OAuth客户端或@gmail.com和@googlemail.com。

* [Google Workspace与Workfront Fusion OAuth客户端](#google-workspace-with-workfront-fusion-oauth-client)
* [Google Workspace与其他OAuth客户端](#google-workspace-with-another-oauth-client)
* [@gmail.com和@googlemail.com](#gmailcom-and-googlemailcom)

### Google Workspace与Workfront Fusion OAuth客户端

Workfront Fusion使用域范围的安装异常。 全域安装适用于Google Workspace用户，允许用户集成未经批准的服务，没有任何限制。 如果您是Google Workspace用户，则无需执行任何其他步骤，可以直接连接到未批准的服务。

### Google Workspace与其他OAuth客户端

更喜欢使用自己的OAuth客户端而不是Workfront Fusion OAuth客户端的Google Workspace用户可以通过内部使用方法连接到Google服务。 此选项适用于高级用户。 有关说明，请参阅[使用自定义OAuth客户端将Adobe Workfront Fusion连接到Google服务](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)。

### @gmail.com和@googlemail.com {#gmailcom-and-googlemailcom}

通过@gmail.com或@googlemail.com访问Google服务的用户可以通过个人使用方法连接到Google服务。 此选项适用于高级用户。 有关说明，请参阅[使用自定义OAuth客户端将Adobe Workfront Fusion连接到Google服务](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)。

## 常见问题解答

* [Adobe Workfront Fusion中的哪些应用程序会受到影响？](#what-apps-in-adobe-workfront-fusion-are-affected)
* [我是否拥有Google Workspace帐户？](#do-i-have-a-g-suite-account)
* [如果我是@gmail.com或@googlemail.com用户，我应该怎么做？](#what-should-i-do-if-im-gmailcom-or-googlemailcom-user)
* [如果我是Google Workspace用户，该怎么办？](#what-should-i-do-if-im-a-g-suite-user)

### Adobe Workfront Fusion中的哪些应用程序会受到影响？ {#what-apps-in-adobe-workfront-fusion-are-affected}

Google Drive、Gmail和Email（已连接到Gmail帐户）。

### 我是否拥有Google Workspace帐户？ {#do-i-have-a-g-suite-account}

如果您的电子邮件地址以@gmail.com或@googlemail.com结尾，则您的帐户不是Google Workspace帐户。 如果您的Google帐户以自定义域(如@my-company.com)结尾，则它是Google Workspace帐户。

### 如果我是@gmail.com或@googlemail.com用户，该怎么办？ {#what-should-i-do-if-im-gmailcom-or-googlemailcom-user}

这些新限制仅适用于集成Google Drive或Gmail的情况。 如果要连接到Google Drive或Gmail，您可以

* 切换到Google Workspace

  或

* 创建自定义OAuth客户端。 此选项适用于高级用户。

  有关说明，请参阅[使用自定义OAuth客户端将Adobe Workfront Fusion连接到Google服务](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md)。

如果您要集成Google Drive或Gmail以外的任何其他服务，则这些限制不适用。

### 如果我是Google Workspace用户，该怎么办？ {#what-should-i-do-if-im-a-g-suite-user}

无需执行任何操作。
