---
title: Microsoft Dynamics 365“财务与运营”单元
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Microsoft Dynamics 365 Finance and Operations的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 96f8d4f1-f97b-4da8-8d82-83cccb54ec68
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 0%

---

# [!DNL Microsoft Dynamics 365 Finance and Operations modules]

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Microsoft Dynamics 365]的工作流，并将其连接到多个第三方应用程序和服务。

>[!NOTE]
>
>[!DNL Microsoft Dynamics 365 Finance and Operations]连接器不支持[!DNL Dynamics 365]。
>
>对于Microsoft Dynamics 365模块，请参阅[[!DNL Microsoft Dynamics 365 modules]](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-dynamics-365-modules.md)。



有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 创建连接

要为Microsoft Dynamics 365 Finance and Operations模块创建连接，请执行以下操作：

1. 在任意Microsoft Dynamics 365 Finance and Operations模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL Add]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>选择是要创建标准Dynamics Finance and Operations连接，还是要使用授权代码创建连接。</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>输入您的Dynamics Finance和操作[!UICONTROL Client ID]。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>输入您的Dynamics Finance和操作[!UICONTROL Client Secret]。 </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Tenant ID]</td>
        <td>输入您的Dynamics Finance and Operations租户ID。</td>
        </tr>
        <tr>
        <td role="rowheader">资源</td>
        <td>输入Dynamics Finance and Operations帐户的URL(不带https://)</td>
        </tr>
      </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;保存连接并返回模块。



## Microsoft Dynamics 365“财务与运营”模块及其字段

>[!IMPORTANT]
>
>通过Dynamics 365 F&amp;O API提供的数据实体因实例而异。 如果您不确定哪些实体可以通过API访问，则使用“data”端点查看实例中的实体会很有用。 Dynamics 365 Finance and Operations中的“data”端点是用于访问OData服务的根URL。 此端点允许您使用标准OData协议与系统公开的各种数据实体进行交互。
>
>您可以使用自定义API调用模块检索这些实体。
>
><!--For more information -->



### 创建实体项

此操作模块在Microsoft Dynamics 365 Finance and Operations中创建一个新的实体项。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>有关将Microsoft Dynamics 365 Finance and Operations连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection" class="MCXref xref">创建连接</a>。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>输入或映射要创建的Dynamics Finance and Operations实体类型。</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
     <td> <p>输入或映射包含要包含在新实体项中的数据的JSON主体。</p> </td> 
  </tr> 
 </tbody> 
</table>



### 删除实体项

此操作模块会从Dynamics Finance and Operations中删除实体项。 项目由其主键字段标识。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>有关将Microsoft Dynamics 365 Finance and Operations连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection" class="MCXref xref">创建连接</a>。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>输入或映射要删除的Dynamics Finance and Operations实体类型。</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> 主键字段标识项目。 对于要提供的每个主键字段，单击<b>添加项</b>，然后输入或映射标识该项的唯一键和值。 </td> 
  </tr> 
 </tbody> 
</table>

### 进行自定义API调用

此操作模块对Dynamics Finance and Operations API进行自定义调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>有关将Microsoft Dynamics 365 Finance and Operations连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection" class="MCXref xref">创建连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>输入相对于Dynamics Finance and Operations URL的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 这会确定请求的内容类型。</p> <p>例如，<code> {"Content-type":"application/json"}</code></p> <p>注意：如果您收到错误并且难以确定其来源，请考虑根据[!DNL Workfront]文档修改标头。 如果自定义API调用返回422 HTTP请求错误，请尝试使用<code>"Content-Type":"text/plain"</code>标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query string]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> <p>提示：我们建议您通过JSON正文而不是查询参数发送信息。</p> </td> 
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



### 读取实体项

此操作模块从实体项返回数据。 项目由其主键字段标识。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>有关将Microsoft Dynamics 365 Finance and Operations连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection" class="MCXref xref">创建连接</a>。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>输入或映射要读取的Dynamics Finance and Operations实体类型。</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> 主键字段标识项目。 对于要提供的每个主键字段，单击<b>添加项</b>，然后输入或映射标识该项的唯一键和值。 </td> 
  </tr> 
 </tbody> 
</table>

### 更新实体项

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>有关将Microsoft Dynamics 365 Finance and Operations连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection" class="MCXref xref">创建连接</a>。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Entity]</td>
     <td>输入或映射要更新的Dynamics Finance and Operations实体类型。</td> 
  </tr>  
  <tr> 
    <td>[!UICONTROL Primary key fields]</td>
     <td> 主键字段标识项目。 对于要提供的每个主键字段，单击<b>添加项</b>，然后输入或映射标识该项的唯一键和值。 </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Body]</td>
     <td> <p>输入或映射包含要包含在新实体项中的数据的JSON主体。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

此搜索模块会根据您指定的条件返回结果。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将[!DNL Workfront]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Entity]</td> 
   <td>输入或映射要搜索的Dynamics Finance and Operations实体类型。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>输入搜索依据的字段、要在查询中使用的运算符以及要在字段中搜索的值。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort by]</td> 
   <td> <p>输入或映射要作为结果排序依据的字段。</p> </td> 
  </tr> 
 </tbody> 
</table>


<!--

### List All

This module lists all records for a given entity.  The item is identified by its Primary key fields.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
     <td>Choose the Dynamics Finance and Operations entity type that you want the module to list.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
     <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Watch Record

This trigger module starts a scenario when a record of the given type is created or updated.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
    <td> <p>For instructions about connecting Microsoft Dynamics 365 Finance and Operations to [!DNL Workfront Fusion], see <a href="#create-a-connection" class="MCXref xref">Create a connection</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of [!DNL Workfront] record that you want the module to watch.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to [!DNL Workfront] logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
 </tbody> 
</table>

-->
