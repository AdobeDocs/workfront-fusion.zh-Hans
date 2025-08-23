---
title: Datadog模块
description: 在Adobe Workfront Fusion场景中，您可以自动执行使用Datadog的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 1%

---

# [!DNL Datadog]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Datadog]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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
   <p>新：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

要使用[!DNL Datadog]模块，您必须具有[!DNL Datadog]帐户。

## Datadog API信息

Datadog连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>1.0.11</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Datadog]连接到Workfront Fusion {#connect-datadog-to-workfront-fusion}

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

您可以直接从[!DNL Datadog]Datadog[!UICONTROL 模块内创建与]帐户的连接。

1. 在任意[!UICONTROL Datadog]模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
1. 按如下方式填写模块的字段：

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL 连接名称]</td> 
      <td> <p> 输入连接的名称。</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>选择此连接是用于生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>选择您是要连接到服务帐户还是个人帐户。</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL 域] </td> 
      <td> <p>选择要连接的域（美国或欧盟）。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API密钥位置] </td> 
      <td> <p>选择是在标头中还是在查询字符串中包含API密钥。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td> <p> 输入您的[!DNL Datadog] API密钥。 </p> <p>有关检索API密钥的说明，请参阅本文中的<a href="#retrieve-your-api-key-and-application-key" class="MCXref xref">检索API密钥和应用程序密钥</a>。</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Datadog]模块及其字段

在配置[!DNL Datadog]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Datadog]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Datadog]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">将[!DNL Datadog]连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 使用专用域]</td> 
   <td>一些需要大量传入流量的Datadog API端点在其专用域上运行。 选中此框以使用专用域进行API调用。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code>https://api.datadoghq.com/api/</code>的路径。 示例： <code> /v1/org</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
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
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Datadog]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-datadog-to-workfront-fusion" class="MCXref xref">将[!DNL Datadog]连接到Workfront Fusion</a>。</p> </td> 
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
   <td role="rowheader">[!UICONTROL 间隔]</td> 
   <td> 如果度量的类型为“比率”或“计数”，则定义相应的时间间隔。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 点]</td> 
   <td><p>添加与量度相关的点数。</p> <p>这是JSON点数组。 每个点的格式如下： <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>注释：  <p>时间戳必须以秒为单位。</p> <p>时间戳必须为最新。 当前被定义为将来不超过10分钟或过去不超过1小时。</p> <p> 数值格式应为浮点值。</p> </p> <p>此字段必须包含至少1个项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 主机]</td> 
   <td>输入生成度量的主机的名称。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标记]</td> 
   <td> 对于要添加到量度的每个标记，单击<b>添加项</b>并输入标记的值。</td> 
  </tr> 
 </tbody> 
</table>
