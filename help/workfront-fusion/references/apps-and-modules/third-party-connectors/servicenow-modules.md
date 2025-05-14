---
title: ServiceNow模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用 [!DNL ServiceNow]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
source-git-commit: 55418d9a25d44e107236898bb236e9daf9fe5bd1
workflow-type: tm+mt
source-wordcount: '1586'
ht-degree: 1%

---

# [!DNL ServiceNow]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL ServiceNow]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL ServiceNow]模块，您必须具有[!DNL ServiceNow]帐户。

## ServiceNow API信息

ServiceNow连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td>https://{{connection.instance}}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.5.13</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL ServiceNow]连接到[!DNL Workfront Fusion]

要为您的[!DNL ServiceNow]模块创建连接：

1. 开始配置第一个[!DNL ServiceNow]模块时，单击[!UICONTROL 连接]框旁边的&#x200B;**[!UICONTROL 添加]**。
1. 输入以下内容：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL连接名称]</p> </td> 
      <td>输入新[!DNL ServiceNow]连接的名称</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL环境]</p> </td> 
      <td>选择您要连接到生产环境还是非生产环境。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL密码]</p> </td> 
      <td>选择您是要连接到服务帐户还是个人帐户。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL用户名]</p> </td> 
      <td>输入您的[!DNL ServiceNow]用户名。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL密码]</p> </td> 
      <td>输入您的ServiceNow密码。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL实例]</p> </td> 
      <td> <p>输入您的[!DNL ServiceNow]帐户的地址，但不输入<code>https://</code>（通常为<code>&lt;company>.service-now.com</code>）。</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**继续**&#x200B;保存连接并返回模块。

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow]模块及其字段

配置[!DNL ServiceNow]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL ServiceNow]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* 如果在“[!UICONTROL 记录类型]”字段中选择了自定义记录，则加载自定义字段可能需要一些时间。
>
>* 如果没有自定义记录，“记录类型”字段下拉列表将为空。

### 触发器

#### [!UICONTROL 观看记录]

此触发器模块在创建或更新记录时激活方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL表类型]</td> 
   <td>选择要监视的表是自定义表还是标准表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择要监视的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示]</td> 
   <td>选择要显示的值的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td>选择您希望模块输出的字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL筛选器]</td> 
   <td>选择要监视新记录还是更新的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 创建记录]](#create-a-record)
* [[!UICONTROL 自定义API调用]](#custom-api-call)
* [[!UICONTROL 停用用户]](#deactivate-a-user)
* [[!UICONTROL 删除记录]](#delete-a-record)
* [[!UICONTROL 下载附件]](#download-an-attachment)
* [[!UICONTROL 读取记录]](#read-a-record)
* [[!UICONTROL 上载附件]](#upload-an-attachment)
* [[!UICONTROL 更新记录]](#update-a-record)

#### [!UICONTROL 创建记录]

此操作模块创建新的[!DNL ServiceNow]记录。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL表类型]</td> 
   <td>选择要在自定义表还是标准表中创建记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择要模块创建的[!DNL ServiceNow]记录的类型。 然后，您可以填写此记录类型的可用字段。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义API调用]

此操作模块允许您对[!DNL ServiceNow] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL ServiceNow]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL相对URL]</td> 
   <td> 输入相对于<code>https://&ltinstance_url&gt/api/</code>的路径。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
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

#### [!UICONTROL 停用用户]

此操作模块使用系统ID在[!DNL ServiceNow]中停用用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL用户系统ID]</td> 
   <td> 输入或映射要取消激活模块的用户的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除记录]

此操作模块可删除事件或用户。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择您要删除事件还是用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL系统ID]</td> 
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
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL附件系统ID]</td> 
   <td> 输入或映射您希望模块下载的附件的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

此操作模块使用系统ID读取[!DNL ServiceNow]记录。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录系统ID]</td> 
   <td>输入或映射您希望模块读取的记录的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL表类型]</td> 
   <td>选择您要读取的记录是在自定义表中还是在标准表中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择您希望模块读取的[!DNL ServiceNow]记录的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示]</td> 
   <td>选择要显示的值的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td>选择您希望模块输出的字段。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新记录]

此操作模块创建新的[!DNL ServiceNow]记录。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录系统ID]</td> 
   <td>输入或映射您希望模块更新的记录的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL表类型]</td> 
   <td>选择要更新的记录是在自定义表中还是在标准表中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
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
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL表名称]</td> 
   <td>输入或映射要上载附件的表的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL系统ID]</td> 
   <td>输入或映射要上载附件的项目的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL 搜索记录]

此模块使用您选择的标准搜索记录。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[！UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL表类型]</td> 
   <td>选择要搜索的表是自定义表还是标准表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择要搜索的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL结果集]</td> 
   <td>选择您希望模块返回符合条件的所有记录，还是只返回第一个符合条件的记录。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL最大记录数]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL搜索类型]</td> 
   <td> <p>选择您希望模块执行的搜索类型</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL高级查询]</strong> </p> 
      <ul> 
       <li> <p>[！UICONTROL搜索查询]</p> <p>输入自定义搜索查询。 有关[!DNL ServiceNow]自定义搜索查询的信息，请参阅<a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">ServiceNow查询文档</a>。</p> </li> 
      </ul> </li> 
     <li> <p><strong>[！UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[！UICONTROL搜索条件]</p> <p>输入您希望模块搜索的条件。 </li> 
       <li> <p>[！UICONTROL排序方式]</p> <p>指示您希望模块按哪个字段对结果进行排序，以及应按升序还是降序对结果进行排序。</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示]</td> 
   <td>选择要显示的值的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td>选择您希望模块输出的字段。</td> 
  </tr> 
 </tbody> 
</table>
