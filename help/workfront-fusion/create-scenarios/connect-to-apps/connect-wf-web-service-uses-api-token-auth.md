---
title: 将Adobe Workfront Fusion连接到使用API令牌授权的Web服务
description: 某些服务不允许集成解决方案(如Adobe Workfront Fusion)创建可在场景中轻松使用的应用程序。
author: Becky
feature: Workfront Fusion
exl-id: 4a8ac816-52de-41e8-96d7-1c8cde2ebe32
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 0%

---

# 将Adobe Workfront Fusion连接到使用API令牌授权的Web服务

某些服务不允许集成解决方案(如Adobe Workfront Fusion)创建可在场景中轻松使用的应用程序。

此情况的解决方法是使用HTTP >发出请求模块，将所需的服务（应用程序）连接到Workfront Fusion。

本文介绍如何使用API密钥/API令牌将几乎任何Web服务连接到Workfront Fusion。

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

## 连接到使用API令牌的Web服务

对于大多数Web服务，通过API令牌连接服务的过程都相似。

1. 在Web服务的网站上创建一个应用程序，如本文中的[创建新应用程序并获取API令牌](#create-a-new-application-and-obtain-the-api-token)部分所述。
1. 获取API密钥或API令牌。
1. 添加Workfront Fusion的HTTP >向方案生成请求模块。
1. 根据Web服务的API文档设置模块并运行方案，如本文中的[设置HTTP模块](#set-up-the-http-module)部分中所述。

>[!NOTE]
>
>此示例连接到Pushover通知服务。

## 创建新应用程序并获取API令牌

>[!NOTE]
>
>Web服务可通过多种不同的方式创建和分发API密钥或API令牌。 有关获取所需Web服务的API密钥和令牌的说明，请转至该服务的网站并搜索“API密钥”或“API令牌”。
>
>我们仅包括有关获取Pushover API密钥的说明，以作为您可能找到的内容的示例。

1. 登录到您的Pushover帐户。
1. 单击页面底部的&#x200B;**创建应用程序/API令牌**。
1. 填写应用程序信息，然后单击&#x200B;**创建应用程序**。
1. 将提供的API令牌存储在安全位置。 您需要它才能使Workfront Fusion HTTP >发出请求模块连接到所需的Web服务（在本例中为Pushover）。

## 设置HTTP模块

要将Web服务连接到Workfront Fusion场景，您需要使用HTTP >在场景中生成请求模块，并根据Web服务的API文档设置模块。

1. 添加HTTP >向方案发出请求模块。
1. 要使用Workfront Fusion推送消息，请按照以下方式设置HTTP模块。

   >[!NOTE]
   >
   >这些模块设置对应于Pushover Web服务API文档。 其他Web服务的设置可能不同。 例如，API令牌可以插入到标头中，而不是插入到正文字段中。

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> URL</td> 
      <td> <p><code>https://api.pushover.net/1/messages.json</code> </p> <p>URL字段包含您可以在Web服务的API文档中找到的端点。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> 方法</td> 
      <td> <p><code>POST</code> </p> <p>使用的方法取决于对应的端点。 推送消息的Pushover端点使用POST方法。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 标头</p> </td> 
      <td> <p>某些Web服务可能使用标头来指定API令牌身份验证或其他参数。 在我们的示例中并非如此，因为推送消息的Pushover端点对所有请求类型都使用Body（见下文）。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 查询字符串</p> </td> 
      <td> <p>某些Web服务可以使用查询字符串指定其他参数。 在我们的示例中，情况并非如此，因为Pushover Web服务对所有请求类型都使用Body（见下文）。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 正文类型</p> </td> 
      <td> <p><code>Raw</code> </p> <p>此设置允许您在下方的内容类型字段中选择JSON内容类型。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 内容类型</p> </td> 
      <td> <p><code>JSON (application/json)</code> </p> <p>JSON是Pushover应用程序所需的内容类型。 这可能与其他Web服务不同。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> 请求内容</p> </td> 
      <td> <p>以JSON格式输入正文请求内容。 您可以使用JSON &gt;创建JSON模块，如本文中的<a href="#map-the-json-body-using-the-json--create-json-module" class="MCXref xref">使用JSON &gt;创建JSON模块</a>映射JSON主体中所述。 或者，也可以手动输入JSON内容，如<a href="#enter-the-json-body-manually" class="MCXref xref">在本文章中手动输入JSON正文</a>中所述。</p> <p>有关该Web服务所需的参数，请参阅Web服务的API文档。</p> </td>

   </tr> 
    </tbody> 
   </table>

## 手动输入JSON正文

以JSON格式指定参数和值。

>[!BEGINSHADEBOX]

**示例：**

```
{"user":"12345c2ecu1hq42ypqzhswbyam34",
"token":"123459evz8aepwtxydndydgyumbfx",
"message":"Hello World!",
"title":"The Push Notification"}
```

>[!ENDSHADEBOX]

此示例包括以下信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p> 用户</p> </td> 
   <td> <p>您的用户密钥。 这可以在您的Pushover功能板中找到。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> 令牌 </td> 
   <td> <p>您生成的API令牌/API密钥创建了Pushover应用程序。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> message </td> 
   <td> <p>发送到设备的推送通知的文本内容。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> 标题 </td> 
   <td> <p>（可选）消息的标题。 如果未输入值，则使用您应用程序的名称。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 使用JSON >创建JSON模块映射JSON主体

创建JSON模块使指定JSON更加容易。 它还允许您动态定义值。

有关JSON模块的详细信息，请参阅[JSON模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/json-modules.md)。

1. 输入或映射要从中创建JSON的值。

   ![JSON值](/help/workfront-fusion/create-scenarios/connect-to-apps/assets/json-values-350x288.png)

1. 将JSON >创建JSON模块连接到HTTP >发出请求模块。
1. 将JSON字符串从创建JSON模块映射到“HTTP”>“发出请求”模块中的“请求内容”字段。

运行场景时，推送通知将发送到已在Pushover帐户中注册的设备。
