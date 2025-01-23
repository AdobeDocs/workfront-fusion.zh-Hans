---
title: Microsoft Dynamics 365模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Microsoft Dynamics 365的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 16ae173b-10ce-481d-8f6c-1df0e65f7c0e
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1548'
ht-degree: 0%

---

# [!DNL Microsoft Dynamics 365 modules]

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Microsoft Dynamics 365]的工作流，并将其连接到多个第三方应用程序和服务。

>[!NOTE]
>
>[!DNL Microsoft Dynamics 365]连接器不支持[!DNL Dynamics Finance and Operations]。

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

要使用[!DNL Microsoft Dynamics] 365，您必须具有[!DNL Microsoft Dynamics 365]帐户。

## 将Microsoft Dynamics 365连接到Workfront Fusion

您可以直接从[!DNL Microsoft Dynamics 365]模块内部创建与[!DNL Microsoft Dynamics 365]帐户的连接。

>[!NOTE]
>
>某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
>
>例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。

1. 在任意[!DNL Microsoft Dynamics 365]模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 输入连接的名称。
1. 在&#x200B;**[!UICONTROL Resource]**&#x200B;字段中，输入[!DNL Dynamics 365]帐户的地址，但不输入`https://`。
1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。

>[!NOTE]
>
>在[!DNL Microsoft Azure]门户中注册[!DNL Workfront Fusion]时，请使用以下重定向URI：
>
>* `https://app.workfrontfusion.com/oauth/cb/workfront-microsoft-dynamics2`


## [!DNL Microsoft Dynamics 365]模块及其字段

配置[!DNL Microsoft Dynamics 365]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Microsoft Dynamics 365]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Watch Records (Scheduled)]](#watch-records-scheduled)
* [[!UICONTROL Watch Records (Real Time)]](#watch-records-real-time)
* [[!UICONTROL Create Record]](#create-record)
* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Delete Record]](#delete-record)
* [[!UICONTROL Read Records]](#read-records)
* [[!UICONTROL Update Record]](#update-record)
* [[!UICONTROL Search Records]](#search-records)

### [!UICONTROL Watch Records (Scheduled)]

当您指定的对象中的记录在[!DNL Dynamics 365]中上次计划运行之后创建或更新时，此计划触发器模块会执行一个方案。

模块输出指示找到的记录是新的还是更新的（如果它在时段内既添加又更新，则标记为新）。 您可以在场景的后续模块中映射此信息。

此操作在您指定的定期计划间隔内进行。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Include]</td> 
   <td>选择您希望模块监视<strong>[!UICONTROL Only new records]</strong>、<strong>[!UICONTROL Updated records only]</strong>还是<strong>[!UICONTROL New records and all changes]</strong>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>选择您希望方案监视的[!UICONTROL Microsoft Dynamics 365]记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max Records]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Watch Records (Real Time)]

此即时触发器模块在[!DNL Dynamics 365]中创建或更新您指定的记录（对象）时执行方案。

此模块中需要webhook。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>选择要用于此模块的webhook。 </p> <p>要添加新的webhook，请执行以下操作：</p> 
    <ol> 
     <li value="1"> <p>单击Webhook字段右侧的<strong>[!UICONTROL Add]</strong></p> </li> 
     <li value="2"> <p>在<strong>[!UICONTROL Webhook]</strong>名称字段中，为webhook键入一个描述性名称。</p> </li> 
     <li value="3"> <p>在<strong>[!UICONTROL Connection]</strong>字段中，选择要使用的连接</p> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </li> 
     <li value="4"> <p>单击<strong>[!UICONTROL Save]</strong>以保存webhook并返回模块。</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Create Record]

此操作模块创建一个实体，如约会或任务。

指定有关要创建的图元的信息。

模块会返回新实体的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>选择您希望模块创建的实体类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select Fields to Map]</td> 
   <td>选择创建记录时要包含其值的字段。 可用字段取决于实体类型。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Property fields]</td> 
   <td> 这些是您选择的字段。 输入您希望记录具有的给定属性值。 </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Make an API Call]

此操作模块允许您对[!DNL Microsoft Dynamics 365] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Microsoft Dynamics 365]模块无法实现的数据流自动化。

模块会返回有关状态代码、标题和正文的信息。 您可以在场景的后续模块中映射此信息。

要了解更多信息，请参阅有关使用[!DNL Dynamics 365 Customer Engagement Web API]的[!DNL Microsoft]文档。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>输入相对于<code>&lt;Instance URL>/api/data/v9.1/</code>的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> <p>中的更多信息</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 为您添加授权标头。</p> </td> 
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

### [!UICONTROL Delete Record]

此操作模块删除实体。

指定实体的ID。

模块会返回实体的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td> <p>选择要让模块删除的实体类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>输入或映射您希望模块删除的记录的唯一[!DNL Microsoft Dynamics 365] ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Read Records]

此操作模块从[!DNL Microsoft Dynamics 365]中的单个实体读取数据。

指定实体的ID。

模块会返回实体的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>选择您希望模块读取的实体类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射您希望模块读取的记录的唯一[!DNL Microsoft Dynamics 365] ID。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Update Record]

此操作模块可更新实体。

指定实体的ID。

该模块会返回更新记录的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>选择要更新模块的实体类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select Fields to Map]</td> 
   <td>选择创建记录时要包含其值的字段。 可用字段取决于实体类型。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Property fields]</td> 
   <td>这些是您选择的字段。 输入您希望记录具有的给定属性值。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射您希望模块更新的记录的唯一[!DNL Microsoft Dynamics] 365 ID。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Search Records]

此搜索模块在[!DNL Microsoft Dynamics 365]中查找与您指定的搜索查询匹配的对象中的记录。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Entity Type]</td> 
   <td>选择要更新模块的实体类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filters]</td> 
   <td> <p>选择要用于此搜索的过滤器。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Standard Filters]</strong> </p> <p>选择字段和运算符，然后输入或映射要搜索的值，从而设置过滤器。 您可以在过滤器中使用AND或OR规则。</p> </li> 
     <li> <p><strong>[!UICONTROL Query Functions]</strong> </p> <p>输入要用于搜索的[!DNL Dynamics 365] Web API查询函数。 </p> <p>有关查询函数的更多信息，请参阅[!DNL Microsoft]文档中的<a href="https://docs.microsoft.com/en-us/dynamics365/customer-engagement/web-api/queryfunctions?view=dynamics-ce-odata-9">Web API查询函数引用</a>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort]</td> 
   <td> <p>指定项目的返回顺序。 您可以添加多个排序。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Field]</strong> </p> <p>指定要作为结果排序依据的字段。</p> </li> 
     <li> <p><strong>[!UICONTROL Direction]</strong> </p> <p>指定排序方向（升序或降序）。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max Records]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>
