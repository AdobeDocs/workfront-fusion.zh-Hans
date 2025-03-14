---
title: Salesforce模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Salesforce的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 3c7c03a7-67ea-4673-90b0-7d0506d9fa10
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '3042'
ht-degree: 0%

---

# [!DNL Salesforce]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Salesforce]的工作流，并将其连接到多个第三方应用程序和服务。

有关Salesforce连接器的视频介绍，请参阅：

* [Salesforce](https://video.tv.adobe.com/v/3427027/){target=_blank}

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

>[!NOTE]
>
>* 并非所有版本的[!DNL Salesforce]都具有API访问权限。 有关详细信息，请参阅[!DNL Salesforce]社区网站上有关具有API访问权限的[!DNL Salesforce]版本的信息。
>* 有关从[!DNL Salesforce] API返回的特定错误的信息，请参阅[!DNL Salesforce] API文档。 您还可以检查[!DNL Salesforce] API的状态以确定任何可能的服务中断。
>

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

## 先决条件

要使用[!DNL Salesforce]模块，您必须具有[!DNL Salesforce]帐户。

## Salesforce API信息

Salesforce连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> {{connection.instanceUrl}}</td>
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v62.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.15.14</td> 
  </tr>
 </tbody> 
 </table>

## 关于搜索[!DNL Salesforce]对象

在搜索对象时，您可以输入单个搜索词，也可以使用通配符和运算符创建更复杂的查询：

* 使用星号通配符(\*)代替零个或多个字符。 例如，搜索Ca\*会查找以Ca开头的项目
* 使用问号通配符(？) 作为单个字符的替代。 例如，搜索Jo？n将查找词为John或Joan但不包含Jon的项目
* 使用引号运算符(“ ”)查找精确匹配的短语。 例如：“星期一会议”

有关搜索可能性的更多信息，请参阅有关SOQL和SOSL的[!DNL Salesforce]开发人员文档。

## 创建与[!DNL Salesforce]的连接

要为您的[!DNL Salesforce]模块创建连接：

1. 在任意[!DNL Salesforce]模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[！UICONTROL连接名称]</td>
        <td>
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL环境]</td>
        <td>
          <p>选择是连接到生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL类型]</td>
        <td>
          <p>选择您是要连接到服务帐户还是个人帐户。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL客户端ID]</td>
        <td>输入您的Salesforce客户端ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL客户端密钥]</td>
        <td>输入您的Salesforce客户端密码。 </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL Sandbox]</td>
        <td>如果这是沙盒环境，则启用此选项。</td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL API版本]</td>
        <td>输入要使用的Salesforce API的版本。 默认版本为62.0。</td>
      </tr>
    </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。


## [!DNL Salesforce]模块及其字段

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

* [[!UICONTROL 观看字段]](#watch-a-field)
* [[!UICONTROL 观看记录]](#watch-for-records)
* [[!UICONTROL 观看出站消息]](#watch-outbound-messages)

#### [!UICONTROL 观看字段]

此触发器模块在[!DNL Salesforce]中更新字段时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL记录类型] </td> 
   <td> <p>选择记录类型，其中包含您希望模块监视的字段。 您必须选择在[!DNL Salesforce]设置中启用了[！UICONTROL字段历史记录]的记录类型。 有关详细信息，请参阅[!DNL Salesforce]文档中的<a href="https://help.salesforce.com/articleView?id=tracking_field_history.htm&amp;type=5">字段历史记录跟踪</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL字段]</td> 
   <td> <p>选择您希望模块关注更改的字段。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL限制]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大字段数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看记录]

此触发器模块在创建或更新对象中的记录时执行场景。 该模块返回与一个或多个记录关联的所有标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL类型] </td> 
   <td> <p>选择要模块监视的[!DNL Salesforce]记录的类型。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL记录字段]</td> 
   <td>选择您希望模块监视的字段。 可用字段取决于记录类型。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL最大记录数]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL监视]</td> 
   <td> <p>确定您希望方案仅监视所选类型的新记录，还是只监视所选类型的新记录以及该类型记录的所有其他更改。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看出站消息]

此触发器模块会在有人发送消息时执行场景。 该模块返回与一个或多个记录关联的所有标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

此模块需要一些额外的设置：

1. 转到[!DNL Salesforce]设置页面。

   要访问设置页面，请找到并单击[!DNL Salesforce]帐户右上角标记为“[!UICONTROL 设置]”的按钮。 从[!DNL Salesforce]设置页面中，找到左侧的“[!UICONTROL 快速查找/搜索]”栏。 搜索“[!UICONTROL 工作流规则]”。

1. 单击&#x200B;**[!UICONTROL 工作流规则]**。
1. 在显示的[!UICONTROL 工作流规则]页面上，单击&#x200B;**[!UICONTROL 新建规则]**，然后选择该规则将应用到的对象类型（例如，如果您正在监视对Opportunity记录的更新，则为“[!UICONTROL Opportunity]”）。
1. 单击&#x200B;**[!UICONTROL 下一步]**。
1. 设置规则名称、评估标准和规则条件，然后单击&#x200B;**[!UICONTROL 保存]**&#x200B;和&#x200B;**[!UICONTROL 下一步]**。

1. 单击&#x200B;**[!UICONTROL 完成]**。
1. 在新创建的工作流规则中，单击&#x200B;**[!UICONTROL 编辑]**。
1. 从&#x200B;**[!UICONTROL 添加工作流操作]**&#x200B;下拉列表中，选择&#x200B;**[!UICONTROL 新建出站消息]**。

1. 指定名称、描述、端点URL以及要包括在新出站消息中的字段，然后单击&#x200B;**[!UICONTROL 保存]**。

   **[!UICONTROL 终结点URL]**&#x200B;字段包含在[!DNL Workfront Fusion]中的[!DNL Salesforce] [!UICONTROL 出站消息]上提供的URL。

1. 配置以[!UICONTROL 出站消息]事件开头的方案。

1. 单击右下角的&#x200B;**&lt;/>**&#x200B;图标，并复制提供的URL。
1. 返回&#x200B;**[!UICONTROL 工作流规则]**&#x200B;页面，找到新创建的规则，然后单击&#x200B;**[!UICONTROL 激活]**。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Webhook]</td> 
   <td> <p>选择要用于监视传出消息的webhook。 要添加webhook，请单击<strong>[！UICONTROL添加]</strong>并输入webhook的名称和连接。</p> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[！UICONTROL Adobe Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL记录类型] </td> 
   <td> <p>选择您希望模块监视传出消息的[!DNL Salesforce]记录的类型。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL字段]</td> 
   <td> <p>选择您希望模块监视传出消息的字段。 可用字段取决于记录类型。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 创建记录]](#create-a-record)
* [[!UICONTROL 自定义API调用]](#custom-api-call)
* [[!UICONTROL 删除记录]](#delete-a-record)
* [[!UICONTROL 下载附件/文档]](#download-attachmentdocument)
* [[!UICONTROL 读取记录]](#read-a-record)
* [[!UICONTROL 上载附件/文档]](#upload-attachmentdocument)
* [上传文件](#upload-file)

#### [!UICONTROL 创建记录]

此操作模块在对象中创建新记录。

利用模块，可选择模块中可用的对象字段。 这减少了设置模块时必须滚动的字段数。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL记录类型] </p> </td> 
   <td> <p>选择要模块创建的[!DNL Salesforce]记录的类型。 根据[！UICONTROL记录类型]字段中选择的记录类型，字段将变为可用。 这些字段基于[!DNL Salesforce] API。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL选择要映射的字段]</td> 
   <td> <p>选择您希望模块在创建新记录时配置的字段。 必填字段位于列表顶部。 </p> <p>您选择的字段在此字段下打开。 您现在可以在这些字段中输入值。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义API调用]

此操作模块允许您对[!DNL Salesforce] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Salesforce]模块无法实现的数据流自动化。

模块返回以下内容：

* **[!UICONTROL 状态代码]** （数字）：这表示HTTP请求是成功还是失败。 这些是标准代码，您可以在互联网上查找。
* **[!UICONTROL 标头]** （对象）：与输出正文无关的响应/状态代码的更详细的上下文。 并非响应标头中显示的所有标头都是响应标头，因此某些标头可能对您没什么用。

  响应标头取决于您在配置模块时选择的HTTP请求。

* **[!UICONTROL Body]**（对象）：根据您在配置模块时选择的HTTP请求，您可能会收到一些返回的数据。 该数据(如来自[!UICONTROL GET]请求的数据)包含在此对象中。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL URL]</p> </td> 
   <td> <p>输入相对于<code> &lt;Instance URL&gt;/services/data/v46.0/</code>的路径。</p> <p>有关可用端点的列表，请参阅<a href="https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm">Salesforce REST API开发人员指南</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL方法]</p> </td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 例如，<code>{"Content-type":"application/json"}</code>。 Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。 例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除记录]

此操作模块删除对象中的现有记录。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL记录类型] </td> 
   <td> <p>选择要模块删除的[!DNL Salesforce]记录的类型。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL ID]</td> 
   <td> <p>输入或映射您希望模块删除的记录的唯一[!DNL Salesforce] ID。</p> <p>要获取ID，请在浏览器中打开[!DNL Salesforce]对象，并复制URL末尾处最后一个正斜杠(/)后面的文本。 例如： <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 下载附件/文档]

此操作模块从记录中下载文档或附件。

您可以指定记录的ID以及所需的下载类型。

模块会返回附件或文档的ID以及任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[！UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr>
    <td>[！UICONTROL下载类型]</td>
    <td> <p>指定要从Salesforce下载的文件类型。</p> 
     <ul> 
      <li>[！UICONTROL附件]</li> 
      <li>[！UICONTROL文档]</li> 
      <li>[！UICONTROL ContentDocument]（此文档已在[!DNL Saleforce CRM Content]或[!DNL Salesforce Files]中上载到库。）</li> 
     </ul> </td>
  </tr> 
  <tr>
    <td> <p>[！UICONTROL ID] / </p> <p>[！UICONTROL附件ID] / </p> <p>[！UICONTROL内容文档ID]</p> </td>
    <td> <p>输入或映射您希望模块下载的记录的唯一[!DNL Salesforce] ID。</p> <p>要获取ID，请在浏览器中打开[!DNL Salesforce]对象，并复制URL末尾处最后一个正斜杠(/)后面的文本。 例如： <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

此操作模块从[!DNL Salesforce]中的单个对象读取数据。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr>
    <td>[！UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr>
    <td>[！UICONTROL记录类型]</td>
    <td>选择您希望模块读取的[!DNL Salesforce]记录的类型。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL记录字段]</td>
    <td>选择您希望模块读取的字段。 您必须至少选择一个字段。</td>
  </tr> 
  <tr>
    <td>[！UICONTROL ID]</td>
    <td> <p>输入或映射您希望模块读取的记录的唯一[!DNL Salesforce] ID。</p> <p>要获取ID，请在浏览器中打开[!DNL Salesforce]对象，并复制URL末尾处最后一个正斜杠(/)后面的文本。 例如： <code>https://eu5.salesforce.com/&lt;object ID&gt;</code></p> </td>
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**示例：**&#x200B;以下API调用返回您[!DNL Salesforce]帐户中所有用户的列表：
>
>* **URL**： `query`
>
>* **方法**： [!UICONTROL GET]
>
>* **查询字符串**：
>
>* **键**： `q`
>
>* **值**： `SELECT Id, Name, CreatedDate, LastModifiedDate FROM User LIMIT 10`
>
>在&#x200B;**[!UICONTROL 包] > [!UICONTROL 正文] > [!UICONTROL 记录]**&#x200B;下的模块输出中可以找到搜索匹配项。
>
>在我们的示例中，返回了6个用户：
>
>![搜索匹配](/help/workfront-fusion/references/apps-and-modules/assets/matches-of-the-search-350x573.png)


#### [!UICONTROL 更新记录]

此操作模块编辑对象中的记录。

利用模块，可选择模块中可用的对象字段。 这减少了设置模块时必须滚动的字段数。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL ID]</td> 
   <td>输入或映射要更新的记录ID。</td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL记录类型] </p> </td> 
   <td> <p>选择要更新模块的[!DNL Salesforce]记录的类型。 根据在“记录类型”字段中选择的记录类型，字段变为可用。 这些字段基于[!DNL Salesforce] API。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL选择要映射的字段]</td> 
   <td> <p>选择您希望模块在创建新记录时配置的字段。 必填字段位于列表顶部。 </p> <p>您选择的字段在此字段下打开。 您现在可以在这些字段中输入值。</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL 上载附件/文档]

此操作模块上传文件并将其附加到您指定的记录，或上传文档。

模块会返回附件或文档的ID以及任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL上载类型]</td> 
   <td>选择您希望模块上载附件还是文档。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL ID]</td> 
   <td>输入或映射要向其上载附件的对象的ID。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件夹]</td> 
   <td>选择包含您希望模块上传的文件的文件夹。 </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Source File]</td> 
   <td>从上一个模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
 </tbody> 
</table>

#### 上传文件

此操作模块会将单个文件上传到Salesforce。



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL  Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文档链接]</td> 
   <td>选择是否应用内容文档链接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL linkedEntityId]</td> 
   <td>如果使用文档链接，请输入或映射链接对象的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL ShareType]</td> 
   <td>如果使用文档链接，请选择文件的权限。<ul><li><b>查看器权限</b><p>用户可以查看文件。</p></li><li><b>协作者权限</b><p>用户可以查看和编辑文件。</p></li><li><b>推断的权限</b><p>权限基于用户对相关记录（如库）的权限。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL可见性]</td> 
   <td>如果使用文档链接，请输入或映射文档的可见性。<ul><li><b>AllUsers</b><p>适用于所有具有权限的用户</p></li><li><b>InternalUsers</b><p>可供具有权限的内部用户使用。</p></li><li><b>共享用户</b><p>可供可以查看文件发布到的馈送的用户使用。</p></li></ul></td> 
  </tr>

### 搜索

#### [!UICONTROL 使用查询搜索]

此搜索模块在[!DNL Salesforce]中查找与您指定的搜索查询匹配的对象中的记录。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL搜索类型]</td> 
   <td> <p>选择您希望模块执行的搜索类型：</p> 
    <ul> 
     <li> <p>[！UICONTROL Simple]</p> </li> 
     <li> <p>[！UICONTROL使用SOSL(Salesforce对象搜索语言)]</p> </li> 
     <li> <p>[！UICONTROL使用SOQL(Salesforce对象查询语言)]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL类型] </p> </td> 
   <td> <p>如果您选择了简单搜索类型，请选择您希望模块搜索的[!DNL Salesforce]记录的类型。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL查询] / [！UICONTROL SOSL查询] / [！UICONTROL SOQL查询]</td> 
   <td> <p>输入要作为搜索依据的查询。</p> <p>有关SOSL的详细信息，请参阅[!DNL Salesforce]文档中的<a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_sosl.htm">Salesforce对象搜索语言(SOSL)</a>。</p> <p>有关SOQL的详细信息，请参阅[!DNL Salesforce]文档中的<a href="https://developer.salesforce.com/docs/atlas.en-us.soql_sosl.meta/soql_sosl/sforce_api_calls_soql.htm">Salesforce对象查询语言(SOQL)</a>。</p> <p>注意：请注意，参数<code>RETURNING </code>的值会影响模块的输出。 如果您使用<code>LIMIT</code>，[!DNL Fusion]将忽略[！UICONTROL最大记录计数]字段中的设置。 如果不设置任何限制，Fusion将插入值[！UICONTROL LIMIT = Maximum count of records]。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL最大记录数]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索]

此操作模块可检索符合给定条件的所有记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关将[!DNL Salesforce]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL  Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL类型]</td> 
   <td> <p>选择要搜索的对象类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL搜索条件]</td> 
   <td>选择要搜索的字段、要在查询中使用的运算符以及要在字段中搜索的值。 您可以使用AND或OR连接查询。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td>选择要包含在模块输出中的字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL结果集]</td> 
   <td>选择您希望模块返回所有匹配记录，还是仅返回第一个匹配记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL最大]</td> 
   <td>输入或映射您希望模块在每个方案执行周期中检索的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>
