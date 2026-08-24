---
title: Azure DevOps 模块
description: 在 Adobe Workfront Fusion 场景中，您可以自动化使用  [!DNL Azure DevOps] 的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
TQID: https://experienceleague.adobe.com/RFI6MFgF-C1Cnn0bvjOLVf3qahyRblEp4dtypNrxqzE
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 0b7298ce53bf59695ce52cb46cb8d25b6ede5fc8
workflow-type: tm+mt
source-wordcount: 2646
ht-degree: 23%

---

# [!DNL Azure DevOps] 模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL Azure DevOps] 的工作流，并将其连接到多个第三方应用程序和服务。

有关创建场景的说明，请参阅[创建场景：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)中的相关文章。

有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的相关文章。

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
   <p>基于操作：适用于拥有基于操作的许可证的组织</p>
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

## 先决条件

要使用[!DNL Azure DevOps]模块，您必须具有[!DNL Azure] DevOps帐户。

## [!DNL Azure DevOps] API信息

Azure DevOps连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 版本</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## 将 [!DNL Azure DevOps] 连接到 Workfront Fusion {#connect-azure-devops-to-workfront-fusion}

* [使用EntraApp将Azure DevOps连接到Workfront Fusion](#connect-azure-devops-to-workfront-fusion-using-entraapp)
* [使用服务主体将Azure DevOps连接到Workfront Fusion](#connect-azure-devops-to-workfront-fusion-using-a-service-principal)

### 使用EntraApp将Azure DevOps连接到Workfront Fusion

1. 将[!DNL Azure DevOps]模块添加到您的方案。
1. 单击[!UICONTROL 连接]字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 在[!UICONTROL 连接类型]字段中，选择要使用的连接类型。

   >[!NOTE]
   >
   >[!UICONTROL [!DNL Azure DevOps] (EntraApp)]允许您请求连接的所有作用域。

1. 填写以下字段：

   <table style="table-layout:auto">
      <tr>
            <td>[!UICONTROL 连接名称]</td>
            <td>输入正在创建的连接的名称。</td>
      </tr>
      <tr>
            <td>[！UICONTROL组织]</td>
            <td>输入您创建了[!DNL Azure DevOps]应用程序的组织的名称。</td>
      </tr>
      <tr>
            <td>[！UICONTROL应用程序ID]</td>
            <td>输入要连接的DevOps应用程序的ID。</td>
      </tr>
      <tr>
            <td>[!UICONTROL 客户端密钥]</td>
            <td>为要连接的DevOps应用程序输入客户端密码。</td>
      </tr>
      <tr>
            <td>[！UICONTROL请求所有作用域]</td>
            <td>如果您使用[!DNL Azure DevOps] (EntraApp)连接类型，请启用此选项以请求连接的所有作用域。</td>
      </tr>
   </table>

1. 要输入Azure DevOps应用程序ID或客户端密钥，请单击<b>显示高级设置</b>，然后在打开的字段中输入它们。
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;完成连接设置并继续创建方案。

### 使用服务主体将Azure DevOps连接到Workfront Fusion

您可以创建使用服务主体（应用程序API连接）而不是个人帐户的连接。 当您希望连接作为应用程序或服务标识而不是作为特定人员运行时，这将很有用。 例如，如果某人离开公司或更改密码，则集成不会中断，这可能会很有用。

此连接类型适用于所有Azure DevOps模块。

>[!NOTE]
>
>服务主体身份验证不支持每个Azure DevOps功能。 少数管理员级别的操作（如管理用户许可证）仍需要个人帐户连接。 如果仅对工作项、展示板、存储库或管道需要此身份验证，请使用服务主体身份验证。

* [使用服务主体将Azure DevOps连接到Workfront Fusion的先决条件](#prerequisites-to-connecting-azure-devops-to-workfront-fusion-using-a-service-principal)
* [在Microsoft Entra ID中创建应用程序注册](#create-the-app-registration-in-microsoft-entra-id)
* [创建客户端密码](#create-a-client-secret)
* [收集您的连接详细信息](#collect-your-connection-details)
* [将服务主体添加到您的Azure DevOps组织](#add-the-service-principal-to-your-azure-devops-organization)
* [创建连接](#create-the-connection)

#### 使用服务主体将Azure DevOps连接到Workfront Fusion的先决条件

要创建此连接，您需要满足以下条件：

* 在Microsoft Entra ID中&#x200B;**全局管理员**&#x200B;或&#x200B;**应用程序管理员**&#x200B;访问权限，以注册应用程序。 如果您没有此访问权限，请让您的IT或身份团队中的某人为您完成该步骤。
* 在您的Azure DevOps组织中&#x200B;**项目集合管理员**&#x200B;访问权限，以将服务主体添加为成员。 此人通常与管理Microsoft Entra ID的人不同。
* Azure DevOps组织的名称。 您可以在Azure DevOps URL中找到此项： `dev.azure.com/<your organization name>`。

#### 在Microsoft Entra ID中创建应用程序注册

1. 登录到[!DNL Microsoft Entra]管理中心。
1. 转到&#x200B;**[!UICONTROL 应用注册]** > **[!UICONTROL 新注册]**。
1. 为应用程序提供一个清晰且可识别的名称。 例如：`Workfront Fusion Azure DevOps Integration`。
1. 将&#x200B;**[!UICONTROL 重定向URI]**&#x200B;保留为空。 此连接不涉及通过浏览器登录。
1. 选择&#x200B;**[!UICONTROL 注册]**。
1. 继续[创建客户端密钥](#create-a-client-secret)。

#### 创建客户端密码

1. 在新应用注册中，转到&#x200B;**[!UICONTROL 证书和密钥]**。
1. 选择&#x200B;**[!UICONTROL 新客户端密钥]**，添加说明，并选择有效期。
1. 选择&#x200B;**[!UICONTROL 添加]**。
1. 立即复制密码的&#x200B;**[!UICONTROL 值]**。 它只显示一次。 如果您在复制它之前导航离开，则必须创建一个新路径。
1. 继续[收集您的连接详细信息](#collect-your-connection-details)。

#### 收集您的连接详细信息

1. 在应用程序注册的&#x200B;**[!UICONTROL 概述]**&#x200B;页面中，注意以下值。 在模块中创建连接时输入这些参数。

   <table style="table-layout:auto">
    <col>
    <col>
    <tbody>
     <tr>
      <td role="rowheader">[！UICONTROL租户ID]</td>
      <td>在概述页面上，标记为<b>目录（租户） ID</b>。</td>
      </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 客户端 ID]</td>
      <td>在概述页面上，标记为<b>应用程序（客户端） ID</b>。</td>
     </tr>
     <tr>
      <td role="rowheader">[!UICONTROL 客户端密钥]</td>
      <td>您在<a href="#create-a-client-secret" class="MCXref xref">中创建客户端密钥</a>中复制的值。</td>
     </tr>
     <tr>
      <td role="rowheader">[！UICONTROL组织]</td>
      <td>您的Azure DevOps组织名称。 例如，如果URL是<code>dev.azure.com/yourorg</code>，请输入<code>yourorg</code>。</td>
     </tr>
    </tbody>
   </table>

   >[!NOTE]
   >
   >您可以跳过应用程序注册的&#x200B;**API权限**&#x200B;区域。 如果在此处添加Azure DevOps，则只有&#x200B;**委派权限**&#x200B;可用。 **应用程序权限**&#x200B;显示为灰色。 这是正常情况，因为Azure DevOps不支持以这种方式授予访问权限。 相反，在下一部分中，访问权限将直接在Azure DevOps中授予。

1. 继续[将服务主体添加到您的Azure DevOps组织](#add-the-service-principal-to-your-azure-devops-organization)。

#### 将服务主体添加到您的Azure DevOps组织

在Microsoft Entra ID中注册应用程序只会创建其标识。 它尚未授予应用程序访问Azure DevOps数据的任何权限。 此过程授予该访问权限。

1. 登录到Azure DevOps组织，网址为`dev.azure.com/<your organization name>`。
1. 选择左下角的&#x200B;**[!UICONTROL 组织设置]**，然后选择&#x200B;**[!UICONTROL 用户]**。
1. 选择&#x200B;**[!UICONTROL 添加用户]**。
1. 在搜索框中，按应用程序的显示名称（您在注册应用程序时为其提供的名称）进行搜索。 请勿按客户端ID进行搜索。
1. 选择访问级别：

   * **[!UICONTROL Basic]**&#x200B;通常足以读写工作项、展示板和存储库。
   * 如果您的工作流需要在设置过程中浏览可用进程，例如Agile、Scrum或自定义模板，请改为将服务主体添加到&#x200B;**[!UICONTROL 项目集合管理员]**&#x200B;组。 这是更高级别的访问权限，因此仅在您需要此功能时才授予此访问权限。

1. 按照贵组织的常规访问惯例，将服务主体分配给所需的一个或多个特定项目。
1. 选择&#x200B;**[!UICONTROL 添加]**。
1. 继续[创建连接](#create-the-connection)。

#### 创建连接

1. 在模块的连接设置屏幕中，选择&#x200B;**[!UICONTROL 服务主体]**&#x200B;连接类型。
1. 输入以下内容：

   * [!UICONTROL 租户ID]
   * [!UICONTROL 客户端ID]
   * [!UICONTROL 客户端密码]
   * [!UICONTROL 组织]

1. 保存连接。

   如果一切设置正确，连接验证成功。

## [!UICONTROL Azure DevOps]模块及其字段

在您配置 [!DNL Azure DevOps] 模块时，Workfront Fusion 会显示以下字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Azure DevOps] 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!UICONTROL 关注工作项]

此即时触发器模块在[!UICONTROL Azure DevOps]中添加、更新或删除记录时执行方案。

该模块会返回与记录关联的所有标准字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>为模块选择或添加webhook。</p> <p>有关触发器模块中Webhook的详细信息，请参阅<a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">即时触发器(Webhook)</a>。</p> <p>有关如何创建Webhook的信息，请参阅<a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhook</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [创建记录](#create-a-record)
* [自定义API调用](#custom-api-call)
* [下载附件](#download-an-attachment)
* [链接工作项](#link-work-items)
* [读取记录](#read-record)
* [更新工作项](#update-a-work-item)
* [[!UICONTROL 上载附件]](#upload-an-attachment)

#### [!UICONTROL 创建记录]

此操作模块创建新项目或工作项。

模块输出新创建的工作项的对象ID，或新创建项目的URL和状态代码。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择您要创建工作项还是项目。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL项目]</strong> </p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p><strong>[！UICONTROL名称]</strong>：输入或映射新项目的名称。</p> </li> 
       <li> <p><strong>[！UICONTROL描述]</strong>：输入或映射新项目的描述。 </p> </li> 
       <li> <p><strong>[！UICONTROL可见性]</strong>：选择您希望项目是公共项目还是专用项目。 用户必须已登录您的组织，并且必须已被授予项目访问权限，才能与专用项目交互。 公共项目对未登录到您的组织的用户可见。</p> </li> 
       <li> <p><strong>[！UICONTROL版本控制]</strong>：选择您希望项目使用[!DNL Git]还是[！UICONTROL Team Foundation版本控制(TFCV)]进行版本控制。</p> </li> 
       <li> <p><strong>[！UICONTROL工作项进程]</strong>：选择要用于项目的工作进程。 选项有[！UICONTROL Basic]、[！UICONTROL Scrum]、[！UICONTROL功能成熟度模型集成(CMMI)]和[！UICONTROL Agile]。</p> <p>有关[!DNL Azure DevOps]进程的详细信息，请参阅[!DNL Azure DevOps]文档中的<a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&amp;tabs=basic-process">默认进程和进程模板</a>。</p> </li> 
      </ul> </li> 
     <li> <p><strong>[！UICONTROL工作项]</strong> </p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p><strong>[！UICONTROL项目]</strong>：选择要创建工作项的项目。</p> </li> 
       <li> <p><strong>[！UICONTROL工作项类型]</strong>：选择要创建的工作项类型。</p> </li> 
       <li> <p><strong>[！UICONTROL其他字段]</strong>：在这些字段中，输入您希望工作项具有的给定属性值。 可用字段取决于工作项类型。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义 API 调用]

此操作模块允许您向 [!DNL Azure DevOps] API 发起自定义的已经过身份认证的调用。 通过这种方式，您可以构建其他 [!DNL Azure DevOps] 模块无法实现的数据流自动化。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL基本URL]</td> 
   <td> <p>选择或映射用于连接到[!DNL Azure DevOps]帐户的基本URL</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL相对URL]</td> 
   <td> <p>输入为此API调用要连接的相对URL。</p> <p><b>示例： </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL API 版本]</td> 
   <td>选择或映射要为此API调用连接到的[!DNL Azure DevOps] API的版本。 如果未选择版本，则Workfront Fusion将连接到[!DNL Azure DevOps] API版本5.1。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。 有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 正文]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 下载附件]

此操作模块下载附件。

模块将返回附件的文件内容。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL附件URL]</td> 
   <td> <p>输入或映射要下载的附件的URL。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 链接工作项]

此操作模块链接两个工作项并定义它们之间的关系。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作项ID]</td> 
   <td>输入或映射要链接其他工作项的主工作项的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL链接的工作项ID]</td> 
   <td>输入或映射要链接到主工作项的工作项的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL链接类型]</td> 
   <td> <p>定义要链接的工作项之间的关系。</p> <p>有关详细信息，请参阅[！UICONTROL Azure DevOps]文档中的<a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">链接类型参考指南</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Comment]</td> 
   <td>输入或映射注释的文本。 这对于解释链接的推理或意图很有用。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

此操作模块从[!DNL Azure DevOps]中的单个记录读取数据。

您需要指定记录的 ID。

该模块会返回记录的 ID 及其关联字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择您要读取项目还是工作项</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL项目]</strong>：选择要读取的项目。</p> </li> 
     <li> <p><strong>[！UICONTROL工作项]</strong>：选择包含要读取的工作项的项目，然后选择该工作项类型。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要包含在此模块输出捆绑包中的信息。 可用字段取决于工作项类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射要读取的记录的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新工作项]

该操作模块使用其ID更新现有工作项。

模块返回已更新工作项的ID。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL项目]</td> 
   <td>选择包含要更新的工作项的项目。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作项类型]</td> 
   <td> <p>选择要更新的工作项的类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL其他字段]</td> 
   <td>在每个字段中，输入您希望工作项具有的给定属性值。 可用字段取决于工作项类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作项ID]</td> 
   <td>输入或映射要更新的工作项的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上载附件]

此操作模块上传文件并将其附加到工作项。

模块会返回附件的附件ID和下载URL。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL项目] </td> 
   <td> <p>选择要上载附件的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作项ID]</td> 
   <td> <p>输入或映射要上载附件的工作项的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Comment]</td> 
   <td>输入要添加到上载附件的注释文本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 来源文件] </td> 
   <td>从以前的模块中选择源文件，或者输入或映射源文件的名称和内容。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL 列出工作项]

此操作模块检索[!DNL Azure DevOps]项目中特定类型的所有工作项。

模块返回主工作项和任何关联字段的ID，以及连接访问的任何自定义字段和值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL项目]</td> 
   <td>选择要从中检索工作项的项目。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL工作项类型]</td> 
   <td> <p>选择要检索的工作项类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要显示在模块输出中的属性。 可用字段取决于您要检索的工作项的类型。 您必须至少选择一个属性。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射Workfront Fusion在一个执行周期内返回的最大工作项数。</td> 
  </tr> 
 </tbody> 
</table>
