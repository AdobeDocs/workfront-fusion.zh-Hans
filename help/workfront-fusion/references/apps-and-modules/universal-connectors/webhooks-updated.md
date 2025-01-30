---
title: Webhook
description: webhook是由事件触发的HTTP调用。 您可以使用Webhook激活即时触发器模块。 任何连接到Internet并允许HTTP请求的应用程序都可以将Webhook发送到Adobe Workfront Fusion。
author: Becky
feature: Workfront Fusion
exl-id: 8e415378-e9c1-4b49-874b-6d38aba0c303
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1331'
ht-degree: 0%

---

# Webhook



<!--This information moved to the webhooks article in the create scenarios folders in the new repo-->

webhook是由事件触发的HTTP调用。 您可以使用Webhook激活即时触发器模块。 任何连接到Internet并允许HTTP请求的应用程序都可以将Webhook发送到Adobe Workfront Fusion。

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
   <p>当前：无Workfront Fusion许可证要求。</p>
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

## 在[!DNL Workfront Fusion]中使用webhook

>[!NOTE]
>
>要调用第三方webhook（传出webhook），请使用其中一个HTTP模块。 有关详细信息，请参阅[HTTP模块](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md#universal-connectors)。

要使用webhook将应用程序连接到[!DNL Workfront Fusion]，请执行以下操作：

1. 将&#x200B;**[!UICONTROL Webhooks]** >**[!UICONTROL Custom Webhook]**&#x200B;即时触发器模块添加到您的方案中。

1. 单击Webhook字段旁边的&#x200B;**[!UICONTROL Add]**，然后输入新webhook的名称。
1. （可选）单击&#x200B;**[!UICONTROL Advanced Settings]**。
1. 在&#x200B;**[!UICONTROL IP restrictions]**&#x200B;字段中，输入模块可以接受其数据的IP地址列表（以逗号分隔）。
1. 单击 **[!UICONTROL Save]**

创建webhook后，将显示唯一的URL。 这是webhook发送数据的地址。 Workfront Fusion会验证发送到此地址的数据，然后传递它以在场景中处理。

>[!NOTE]
>
>创建webhook后，您可以将其同时用于多个场景。

### 配置webhook的数据结构 {#configure-the-webhook-s-data-structure}

为了识别传入有效负载的数据结构，[!DNL Workfront Fusion]将解析您发送到所显示地址的示例数据。 您可以通过在服务或应用程序中进行更改来提供示例数据，该服务或应用程序会将该服务或应用程序调用webhook。 例如，您可以删除文件。

或者，您可以通过[!UICONTROL HTTP] > [!UICONTROL Make a request]模块发送示例数据：

1. 使用&#x200B;**[!UICONTROL HTTP]** > **[!UICONTROL Make a request]**&#x200B;模块创建新方案

1. 使用以下值配置模块：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"><p>[!UICONTROL URL] </p></td> 
      <td>输入webhook的URL。 您可以在用于设置webhook的[!UICONTROL Webhooks]模块中找到此URL。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Method] </td> 
      <td><p>[!UICONTROL POST]</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Body type]</td> 
      <td><p> [!UICONTROL Raw]</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Content type]</td> 
      <td><p> JSON (application/json)</p></td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Request content]</td> 
      <td><p>webhook中需要原始JSON</p></td> 
     </tr> 
    </tbody> 
   </table>

   ![新屏幕设置](/help/workfront-fusion/references/apps-and-modules/assets/new-scenario-set-up-like-this-350x446.png)

1. 在单独的浏览器选项卡或窗口中打开具有[!UICONTROL Webhooks]模块的方案。
1. 在webhooks模块中，单击&#x200B;**[!UICONTROL Redetermine data structure]**。

   您无需取消其他模块与Webhooks模块的链接。

1. 切换到具有[!UICONTROL HTTP]模块的方案并运行它。
1. 切换回使用Webhooks模块的场景。

   “[!UICONTROL Successfully determined]”消息表示模块已成功确定数据结构。

   ![已成功确定](/help/workfront-fusion/references/apps-and-modules/assets/successfully-determined-350x175.png)

1. 单击&#x200B;**[!UICONTROL OK]**&#x200B;保存数据结构。

   webhook的项目现在位于“映射”面板中，可用于场景中的后续模块。

## webhook队列

如果webhook收到数据，并且不存在需要该数据的活动场景，则数据存储在队列中。 激活场景后，它将按顺序处理队列中等待的所有包。

>[!IMPORTANT]
>
>Webhook队列在使用相同webhook的场景之间共享。 如果其中一个方案被禁用，则所有传入数据都将保留在队列中。

## 支持的传入数据格式

[!DNL Workfront Fusion]支持3种传入数据格式：[!UICONTROL Query String]、[!UICONTROL Form Data]和[!UICONTROL JSON]。

[!DNL Workfront Fusion]根据所选的数据结构验证所有传入数据。 然后，根据方案的设置，数据会存储在队列中以供处理，或者会立即进行处理。

如果数据的任何部分未通过验证，[!DNL Workfront Fusion]将返回400 HTTP状态代码，并在HTTP响应的正文中指定传入数据未通过验证检查的原因。 如果传入数据验证成功，Workfront Fusion将返回“[!UICONTROL 200 Accepted]”状态。

* [[!UICONTROL Query String]](#query-string)
* [[!UICONTROL Form Data]](#form-data)
* [[!UICONTROL JSON]](#json)

### [!UICONTROL Query String]

```
GET https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>?name=<yourname>&job=automate
```

### [!UICONTROL Form Data]

```
POST https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>

Content-Type: application/x-www-form-urlencoded

name=<yourname>&job=automate
```

#### 多部分表单数据

```
POST https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>


Content-Type: multipart/form-data; boundary=---generatedboundary

---generatedboundary

Content-Disposition: form-data; name="file"; filename="file.txt"


Content-Type: text/plain


Content of file.txt


---generatedboundary

Content-Disposition: form-data; name="name"

Workfront Fusion

---generatedboundary
```

为了接收使用`multipart/form-data`编码的文件，您必须使用包含嵌套字段`name`、`mime`和`data`的`collection`类型字段配置数据结构。 字段`name`是`text`类型，包含上载文件的名称。 `mime`是`text`类型并包含MIME格式的文件。 字段`data`是`buffer`类型，包含要传输文件的二进制数据。

有关MIME格式的详细信息，请参阅[MIME模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/mime.md)。

### [!UICONTROL JSON]

```
POST https://app.workfrontfusion.com/wh/<yourunique32characterslongstring>

Content-Type: application/json

{"name": "Workfront Fusion", "job": "automate"}
```

>[!TIP]
>
>如果要访问原始JSON，请在设置webhook时启用JSON传递。
>
>1. 单击&#x200B;**[!UICONTROL Add]**&#x200B;添加新的webhook。
>1. 单击 **[!UICONTROL Show advanced settings]**。
>1. 单击 **[!UICONTROL JSON pass-through]**。
>

## Webhook标题

要访问webhook的标头，请在设置webhook时启用Get请求标头。

1. 单击&#x200B;**[!UICONTROL Add]**&#x200B;添加新的webhook。
1. 单击 **[!UICONTROL Show advanced settings]**。
1. 单击 **[!UICONTROL Get request headers]**。

您可以使用`map()`和`get()`函数的组合提取特定的标头值。

>[!INFO]
>
>**示例：**
>
>以下示例显示了一个从`Headers[]`数组提取`authorization`标头值的公式。 该公式用在过滤器中，该过滤器将提取的值与给定文本进行比较，以仅在存在匹配项时传递Webhook。
>
>![设置筛选器](/help/workfront-fusion/references/apps-and-modules/assets/set-up-a-filter-350x169.png)
>
>有关使用给定键获取数组元素的更多信息，请参阅“映射数组”一文中的[使用给定键映射数组的元素](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md#map-an-arrays-element-with-a-given-key)。

## 响应Webhook

对webhook调用的默认响应是文本“已接受”。 响应将返回到在执行自定义Webhook模块期间调用webhook的应用程序。

* [测试对webhook的响应](#test-the-response-to-a-webhook)
* [HTML响应示例](#html-response-example)
* [重定向示例](#redirect-example)

### 测试对webhook的响应

1. 在您的方案中包含模块&#x200B;**[!UICONTROL Custom Webhook]**。
1. 将新的webhook添加到模块。
1. 将webhook URL复制到剪贴板。
1. 运行方案。

   [!UICONTROL Custom Webhook]模块上的闪电图标将变为旋转圆点。 这显示了模块现在正在等待webhook调用。

1. 打开一个新的浏览器窗口，将复制的URL粘贴到地址栏中，然后按&#x200B;**[!UICONTROL Enter]**。

   已触发[!UICONTROL Custom Webhook]模块，浏览器将显示一个新页面。

如果要自定义webhook的响应，请使用模块Webhook响应。

模块的配置包含两个字段：[!UICONTROL Status]和[!UICONTROL Body]。

* [!UICONTROL Status]字段包含HTTP响应状态代码，例如，2xx表示成功（例如，`200`表示正常），3xx表示重定向（例如，`307`表示临时重定向），4xx表示客户端错误（例如，`400`表示错误请求）等等。

* [!UICONTROL Body]字段包含webhook调用将接受的任何内容。 它可以是简单文本、HTML、XML、JSON等。

  >[!TIP]
  >
  >我们建议将`Content-Type`标头设置为相应的MIME类型：纯文本为`text/plain`，HTML为`text/html`，JSON为`application/json`，XML为`application/xml`，依此类推。 有关MIME类型的详细信息，请参阅[MIME模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/mime.md)。

发送响应的超时为40秒。 如果响应在该时段内不可用，Workfront Fusion将返回“200已接受”状态。

### HTML响应示例

>[!INFO]
>
>**示例：**
>
>按如下方式配置[!UICONTROL Webhook Response]模块：
>
><table style="table-layout:auto"> 
&gt; <col> 
&gt; <col> 
&gt; <tbody> 
&gt;  <tr> 
&gt;   <td role="rowheader">[!UICONTROL Status] </td> 
&gt;   <td> <p>2xx成功HTTP状态代码，例如200</p> </td> 
&gt;  </tr> 
&gt;  <tr> 
&gt;   <td role="rowheader">[!UICONTROL Body] </td> 
&gt;   <td> <p>HTML代码</p> </td> 
&gt;  </tr> 
&gt;  <tr> 
&gt;   <td role="rowheader"> <p>[!UICONTROL Custom headers]</p> </td> 
&gt;   <td> 
&gt;    <ul> 
&gt;     <li><strong>键</strong>： Content-type</li> 
&gt;     <li><strong>值</strong>： text/html</li> 
&gt;    </ul> </td> 
&gt;  </tr> 
&gt; </tbody> 
&gt;</table>
>
>![自定义标头](/help/workfront-fusion/references/apps-and-modules/assets/custom-headers-350x235.png)
>
>这将生成一个HTML响应，并在Web浏览器中显示：
>
>![HEML响应](/help/workfront-fusion/references/apps-and-modules/assets/html-response-350x70.png)

### 重定向示例

>[!INFO]
>
>**示例：**&#x200B;按如下方式配置[!UICONTROL Webhook Response]模块：
>
><table style="table-layout:auto"> 
&gt; <col> 
&gt; <col> 
&gt; <tbody> 
&gt;  <tr> 
&gt;   <td role="rowheader">[!UICONTROL Status] </td> 
&gt;   <td> <p>3xx重定向HTTP状态代码，例如303</p> </td> 
&gt;  </tr> 
&gt;  <tr> 
&gt;   <td role="rowheader"> <p>[!UICONTROL Custom headers]</p> </td> 
&gt;   <td> 
&gt;    <ul> 
&gt;     <li><strong>[!UICONTROL Key]</strong>：位置</li> 
&gt;     <li><strong>[!UICONTROL Value]</strong>：要重定向到的URL。</li> 
&gt;    </ul> </td> 
&gt;  </tr> 
&gt; </tbody> 
&gt;</table>
>
>![Webhook响应](/help/workfront-fusion/references/apps-and-modules/assets/webhook-response-350x279.png)

## Webhook停用

如果出现以下任一情况，Webhook将自动停用：

* webhook已超过5天未连接到任何场景
* webhook仅用于非活动场景，这些场景已非活动超过30天。

如果停用的Webhook未连接到任何场景并且已处于停用状态超过30天，则会自动删除和取消注册它们。


## 故障排除

### 映射面板中缺少项目

如果[!UICONTROL Webhooks] > [!UICONTROL Custom Webhook]模块之后的模块设置中的映射面板中缺少某些项，请单击&#x200B;**[!UICONTROL Webhooks]>[!UICONTROL Custom Webhook]**&#x200B;模块以打开其设置，然后单击&#x200B;**[!UICONTROL Re-determine data structure]**：

![重新确定数据结构](/help/workfront-fusion/references/apps-and-modules/assets/redetermine-data-structure-btn-350x195.png)

然后按照本文中[配置webhook的数据结构](#configure-the-webhook-s-data-structure)部分中描述的步骤进行操作。
