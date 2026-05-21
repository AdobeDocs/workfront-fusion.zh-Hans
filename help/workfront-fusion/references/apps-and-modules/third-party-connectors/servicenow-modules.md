---
title: ServiceNow 模块
description: 在 Adobe Workfront Fusion 场景中，您可以自动化使用  [!DNL ServiceNow] 的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
TQID: https://experienceleague.adobe.com/cIq5yfUbJsb3v8DbVjWv7hCP6kOkTbGmGouBirjETpo
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 1643
ht-degree: 43%

---

# [!DNL ServiceNow] 模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL ServiceNow] 的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用 [!DNL ServiceNow] 模块，您必须拥有一个 [!DNL ServiceNow] 帐户。

## ServiceNow API信息

ServiceNow连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td><pre><code>https://&#123;&#123;connection.instance&#125;&#125;/api</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## 将 [!DNL ServiceNow] 连接到 Workfront Fusion

要为您的 [!DNL ServiceNow] 模块创建连接：

1. 开始配置第一个[!DNL ServiceNow]模块时，单击[!UICONTROL 连接]框旁边的&#x200B;**[!UICONTROL 添加]**。
1. 输入以下内容：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 连接名称]</p> </td> 
      <td>输入新[!DNL ServiceNow]连接的名称。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 环境]</p> </td> 
      <td>选择您要连接到生产环境还是非生产环境。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 密码]</p> </td> 
      <td>选择连接服务帐户还是个人帐户。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 用户名]</p> </td> 
      <td>输入您的[!DNL ServiceNow]用户名。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 密码]</p> </td> 
      <td>输入您的ServiceNow密码。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 实例]</p> </td> 
      <td> <p>输入您的[!DNL ServiceNow]帐户的地址，但不输入<code>https://</code>（通常为<code>&lt;company>.service-now.com</code>）。</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 点击&#x200B;**继续**&#x200B;保存连接并返回模块。

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow]模块及其字段

在您配置 [!DNL ServiceNow] 模块时，Workfront Fusion 会显示以下字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL ServiceNow] 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* 如果在“[!UICONTROL 记录类型]”字段中选择了自定义记录，则加载自定义字段可能需要一些时间。
>
>* 如果没有自定义记录，“记录类型”字段下拉列表将为空。

### 触发器

#### [!UICONTROL 监控记录]

此触发器模块在创建或更新记录时激活方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 表类型]</td> 
   <td>选择要监视的表是自定义表还是标准表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td>选择要监视的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 显示]</td> 
   <td>选择要显示的值的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择您希望模块输出的字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 筛选条件]</td> 
   <td>选择要监视新记录还是更新的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 创建记录]](#create-a-record)
* [[!UICONTROL 自定义 API 调用]](#custom-api-call)
* [[!UICONTROL 停用用户]](#deactivate-a-user)
* [[!UICONTROL 删除记录]](#delete-a-record)
* [[!UICONTROL 下载附件]](#download-an-attachment)
* [[!UICONTROL 读取记录]](#read-a-record)
* [[!UICONTROL 上载附件]](#upload-an-attachment)
* [[!UICONTROL 更新记录]](#update-a-record)

#### [!UICONTROL 创建记录]

此操作模块创建新的[!DNL ServiceNow]记录。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 表类型]</td> 
   <td>选择要在自定义表还是标准表中创建记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td>选择要模块创建的[!DNL ServiceNow]记录的类型。 然后，您可以填写此记录类型的可用字段。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义 API 调用]

此操作模块允许您向 [!DNL ServiceNow] API 发起自定义的已经过身份认证的调用。 通过这种方式，您可以构建其他 [!DNL ServiceNow] 模块无法实现的数据流自动化。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 相对URL]</td> 
   <td> 输入相对于 <code>https://&ltinstance_url&gt/api/</code> 的路径。 </td> 
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

#### [!UICONTROL 停用用户]

此操作模块使用系统ID在[!DNL ServiceNow]中停用用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 用户系统ID]</td> 
   <td> 输入或映射要取消激活模块的用户的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除记录]

此操作模块可删除事件或用户。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td>选择您要删除事件还是用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 系统ID]</td> 
   <td>输入或映射您希望模块删除的记录的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 下载附件]

此操作模块下载[!DNL ServiceNow]记录中的附件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 附件系统ID]</td> 
   <td> 输入或映射您希望模块下载的附件的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

此操作模块使用系统ID读取[!DNL ServiceNow]记录。

该模块会返回与记录关联的所有标准字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录系统ID]</td> 
   <td>输入或映射您希望模块读取的记录的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 表类型]</td> 
   <td>选择您要读取的记录是在自定义表中还是在标准表中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td>选择您希望模块读取的[!DNL ServiceNow]记录的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 显示]</td> 
   <td>选择要显示的值的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择您希望模块输出的字段。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新记录]

此操作模块创建新的[!DNL ServiceNow]记录。

在配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录系统ID]</td> 
   <td>输入或映射您希望模块更新的记录的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 表类型]</td> 
   <td>选择要更新的记录是在自定义表中还是在标准表中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td>选择要更新模块的[!DNL ServiceNow]记录的类型。 然后，您可以填写此记录类型的可用字段。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上载附件]

此操作模块将附件上传到[!DNL ServiceNow]记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 表名称]</td> 
   <td>输入或映射要上载附件的表的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 系统ID]</td> 
   <td>输入或映射要上载附件的项目的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 来源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL 搜索记录]

此模块使用您选择的标准搜索记录。

该模块会返回与记录关联的所有标准字段，以及连接可访问的任何自定义字段及其值。 您可以在场景后续的模块中映射这些信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将ServiceNow帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 表类型]</td> 
   <td>选择要搜索的表是自定义表还是标准表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td>选择要搜索的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 结果集]</td> 
   <td>选择您希望模块返回符合条件的所有记录，还是只返回第一个符合条件的记录。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 最大记录数]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 搜索类型]</td> 
   <td> <p>选择您希望模块执行的搜索类型</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 高级查询]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL 搜索查询]</p> <p>输入自定义搜索查询。 有关[!DNL ServiceNow]自定义搜索查询的信息，请参阅<a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">ServiceNow查询文档</a>。</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL 搜索条件]</p> <p>输入您希望模块搜索的条件。 </li> 
       <li> <p>[!UICONTROL 排序方式]</p> <p>指示您希望模块按哪个字段对结果进行排序，以及应按升序还是降序对结果进行排序。</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 显示]</td> 
   <td>选择要显示的值的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择您希望模块输出的字段。</td> 
  </tr> 
 </tbody> 
</table>
