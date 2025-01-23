---
title: ServiceNow模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用 [!DNL ServiceNow]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 7b236869-bd83-4db5-a363-d6570f6e4aff
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 0%

---

# [!DNL ServiceNow]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL ServiceNow]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成] </p>
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

1. 开始配置第一个[!DNL ServiceNow]模块时，单击[!UICONTROL Connection]框旁边的&#x200B;**[!UICONTROL Add]**。
1. 输入以下内容：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td>输入新[!DNL ServiceNow]连接的名称</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Username]</p> </td> 
      <td>输入您的[!DNL ServiceNow]用户名。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Password]</p> </td> 
      <td>输入您的ServiceNow密码。</td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Instance]</p> </td> 
      <td> <p>输入您的[!DNL ServiceNow]帐户的地址，但不输入<code>https://</code>（通常为<code>&lt;company>.service-now.com</code>）。</p> </td> 
     </tr> 
    </tbody> 
   </table>

   <!--Markdown placeholder-->

## [!UICONTROL ServiceNow]模块及其字段

配置[!DNL ServiceNow]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL ServiceNow]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>如果在“[!UICONTROL Record type]”字段中选择了自定义记录，则加载自定义字段可能需要一些时间。
>
>如果没有自定义记录，则下拉列表将为空。

* [[!UICONTROL Watch records]](#watch-records)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Deactivate a User]](#deactivate-a-user)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Upload an attachment]](#upload-an-attachment)
* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Search for records]](#search-for-records)

### [!UICONTROL Watch records]

此触发器模块在创建或更新记录时激活方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>选择要监视的表是自定义表还是标准表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>选择要监视的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>选择要显示的值的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>选择您希望模块输出的字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>选择要监视新记录还是更新的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Custom API Call]

此操作模块允许您对[!DNL ServiceNow] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL ServiceNow]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> <p>键入您希望模块与之交互的Web服务器上的地址。</p> <p>您可以键入相对URL，这意味着您不必在开头包含协议（如<code>http://</code>）。 这向Web服务器表明交互正在服务器上发生。</p> <p>例如： <code>[!DNL /api/conversations].create</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Read a record]

此操作模块使用系统ID读取[!DNL ServiceNow]记录。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>输入或映射您希望模块读取的记录的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>选择您要读取的记录是在自定义表中还是在标准表中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>选择您希望模块读取的[!DNL ServiceNow]记录的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>选择要显示的值的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>选择您希望模块输出的字段。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Deactivate a User]

此操作模块使用系统ID在[!DNL ServiceNow]中停用用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User System ID]</td> 
   <td> 输入或映射要取消激活模块的用户的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Download an attachment]

此操作模块下载[!DNL ServiceNow]记录中的附件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment System ID]</td> 
   <td> 输入或映射您希望模块下载的附件的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Upload an attachment]

此操作模块将附件上传到[!DNL ServiceNow]记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table name]</td> 
   <td>输入或映射要上载附件的表的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>输入或映射要上载附件的系统的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File name]</td> 
   <td>输入或映射附件的名称</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File content]</td> 
   <td>输入或映射要上载的文件到[!DNL ServiceNow]。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Create a record]

此操作模块创建新的[!DNL ServiceNow]记录。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>选择要在自定义表还是标准表中创建记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>选择要模块创建的[!DNL ServiceNow]记录的类型。 然后，您可以填写此记录类型的可用字段。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update a record]

此操作模块创建新的[!DNL ServiceNow]记录。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record System ID]</td> 
   <td>输入或映射您希望模块更新的记录的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>选择要更新的记录是在自定义表中还是在标准表中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>选择要更新模块的[!DNL ServiceNow]记录的类型。 然后，您可以填写此记录类型的可用字段。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Delete a record]

此操作模块可删除事件或用户。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td>选择您要删除事件还是用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL System ID]</td> 
   <td>输入或映射您希望模块删除的记录的唯一[!DNL ServiceNow] ID。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search for records]

此模块使用您选择的标准搜索记录。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将ServiceNow帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-servicenow-to-workfront-fusion" class="MCXref xref">将[!DNL ServiceNow]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Table type]</td> 
   <td>选择要搜索的表是自定义表还是标准表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>选择要搜索的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Result set]</td> 
   <td>选择您希望模块返回符合条件的所有记录，还是只返回第一个符合条件的记录。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximal count of records]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search type]</td> 
   <td> <p>选择您希望模块执行的搜索类型</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Advanced query]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Query]</p> <p>输入自定义搜索查询。 有关[!DNL ServiceNow]自定义搜索查询的信息，请参阅<a href="https://docs.servicenow.com/bundle/orlando-platform-user-interface/page/use/common-ui-elements/reference/r_OpAvailableFiltersQueries.html">ServiceNow查询文档</a>。</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Simple]</strong> </p> 
      <ul> 
       <li> <p>[!UICONTROL Search Criteria]</p> <p>输入您希望模块搜索的条件。<!--For more information on setting up search filters, see <a href="." class="MCXref xref">Add a filter to a scenario in Adobe Workfront Fusion</a>.</p>--> </li> 
       <li> <p>[!UICONTROL Sort by]</p> <p>指示您希望模块按哪个字段对结果进行排序，以及应按升序还是降序对结果进行排序。</p> </li> 
      </ul> </li> 
    </ul> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Display]</td> 
   <td>选择要显示的值的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>选择您希望模块输出的字段。</td> 
  </tr> 
 </tbody> 
</table>
