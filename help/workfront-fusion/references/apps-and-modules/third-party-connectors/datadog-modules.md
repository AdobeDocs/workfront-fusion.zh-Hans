---
title: Datadog 模块
description: 在Adobe Workfront Fusion场景中，您可以自动执行使用Datadog的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
TQID: https://experienceleague.adobe.com/DM-90ye4UKybFarHch-ubk4vOt4Ofh69EBXTmAO-Hmw
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 959
ht-degree: 47%

---

# [!DNL Datadog] 模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL Datadog] 的工作流，并将其连接到多个第三方应用程序和服务。

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

## 先决条件

要使用 [!DNL Datadog] 模块，您必须拥有一个 [!DNL Datadog] 帐户。

## Datadog API信息

Datadog连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>1.0.11</td> 
  </tr>
 </tbody> 
 </table>

## 将 [!DNL Datadog] 连接到 Workfront Fusion {#connect-datadog-to-workfront-fusion}

### 检索API密钥和应用程序密钥 {#retrieve-your-api-key-and-application-key}

要将您的[!DNL Datadog]帐户连接到Workfront Fusion，您需要从[!DNL Datadog]帐户检索API密钥和应用程序密钥。

1. 登录到您的[!DNL Datadog]帐户。
1. 在左侧导航面板中，单击&#x200B;**[!UICONTROL 集成]**，然后单击&#x200B;**[!UICONTROL API]**。
1. 在主屏幕上，单击&#x200B;**[!UICONTROL API密钥]**。
1. 将鼠标悬停在紫色栏上以显示API密钥。
1. 将API密钥复制到安全位置。
1. 在主屏幕上，单击&#x200B;**[!UICONTROL 应用程序键]**。
1. 将鼠标悬停在紫色栏上以显示应用程序密钥。
1. 将应用程序密钥复制到安全位置。

### 在Workfront Fusion中创建与[!DNL Datadog]的连接

您可以直接从[!UICONTROL Datadog]模块内创建与[!DNL Datadog]帐户的连接。

1. 在任意[!UICONTROL Datadog]模块中，单击[!UICONTROL 连接]字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 按如下方式填写模块的字段：

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[！UICONTROL连接名称]</td> 
      <td> <p> 输入连接名称。</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>选择此连接是用于生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>选择连接服务帐户还是个人帐户。</td>
        </tr>
     <tr> 
      <td role="rowheader">[！UICONTROL域] </td> 
      <td> <p>选择要连接的域（美国或欧盟）。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL API密钥位置] </td> 
      <td> <p>选择是在标头中还是在查询字符串中包含API密钥。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL API Key]</td> 
      <td> <p> 输入您的[!DNL Datadog] API密钥。 </p> <p>有关检索API密钥的说明，请参阅本文中的<a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">检索API密钥和应用程序密钥</a>。</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Datadog] 模块及其字段

在您配置 [!DNL Datadog] 模块时，Workfront Fusion 会显示以下字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Datadog] 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 操作

* [[!UICONTROL 进行API调用]](#make-an-api-call)
* [[!UICONTROL 发布时序点]](#post-timeseries-points)

#### [!UICONTROL 进行API调用]

此操作模块允许您执行自定义API调用。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将 [!DNL Datadog] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">将 [!DNL Datadog] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL使用专用域]</td> 
   <td>一些需要大量传入流量的Datadog API端点在其专用域上运行。 选中此框以使用专用域进行API调用。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于 <code>https://api.datadoghq.com/api/</code> 的路径。 示例： <code> /v1/org</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。 有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
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

**示例：**&#x200B;以下API调用返回您[!DNL Datadog]帐户中的所有仪表板：

URL： `/v1/dashboard`

方法： `GET`

![Datadog API调用示例](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-example.png)

结果可以在模块的“输出”中找到，位于“包”>“正文”>“功能板”下。

在我们的示例中，返回了3个仪表板：

![Datadog API响应](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-response-example.png)

#### [!UICONTROL 发布时序点]

此模块允许您发布可在[!DNL Datadog]的仪表板上绘制的时间系列数据。

压缩有效负载的限制为3.2 MB (3200000)，解压缩有效负载的限制为62 MB (62914560)。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将 [!DNL Datadog] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">将 [!DNL Datadog] 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 类型]</td> 
   <td> 选择要使用的量度类型。 
   <ul>
   <li>计量</li>
   <li>费率</li>
   <li>计数</li>
   </ul>
   </td> 
  <tr> 
   <td role="rowheader">[！UICONTROL间隔]</td> 
   <td> 如果度量的类型为“比率”或“计数”，则定义相应的时间间隔。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL点]</td> 
   <td><p>添加与量度相关的点数。</p> <p>这是JSON点数组。 每个点的格式如下： <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>注意：  <p>时间戳必须以秒为单位。</p> <p>时间戳必须为最新。 当前被定义为将来不超过10分钟或过去不超过1小时。</p> <p> 数值格式应为浮点值。</p> </p> <p>此字段必须包含至少1个项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL主机]</td> 
   <td>输入生成度量的主机的名称。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标记]</td> 
   <td> 对于要添加到量度的每个标记，单击<b>添加项</b>并输入标记的值。</td> 
  </tr> 
 </tbody> 
</table>
