---
title: Microsoft Dynamics 365模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Microsoft Dynamics 365的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 16ae173b-10ce-481d-8f6c-1df0e65f7c0e
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1810'
ht-degree: 0%

---

# [!DNL Microsoft Dynamics 365 modules]

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Microsoft Dynamics 365]的工作流，并将其连接到多个第三方应用程序和服务。

>[!NOTE]
>
>[!DNL Microsoft Dynamics 365]连接器不支持[!DNL Dynamics Finance and Operations]。
>
>有关[!DNL Microsoft Dynamics 365 Finance and Operations]连接器的信息，请参阅[[!DNL Microsoft Dynamics 365 Finance and Operations] 模块](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/dynamics-finance-operations-modules.md)。

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

要使用[!DNL Microsoft Dynamics] 365，您必须具有[!DNL Microsoft Dynamics 365]帐户。

## 将Microsoft Dynamics 365连接到Workfront Fusion

您可以直接从[!DNL Microsoft Dynamics 365]模块内部创建与[!DNL Microsoft Dynamics 365]帐户的连接。

>[!NOTE]
>
>某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
>
>例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。

1. 在任意[!DNL Microsoft Dynamics 365]模块中，单击[!UICONTROL 连接]字段旁边的&#x200B;**[!UICONTROL 添加]**。


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
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL环境]</td>
          <td>选择您要连接到生产环境还是非生产环境。</td>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL类型]</td>
          <td>选择您是要连接到服务帐户还是个人帐户。</td>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL客户端ID]<p>（可选）</p></td>
          <td>输入您的[!DNL Microsoft Dynamics] [！UICONTROL客户端ID]。</td>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL客户端密钥]<p>（可选）</p></td>
          <td>输入您的[!DNL Microsoft Dynamics] [！UICONTROL客户端密钥]。
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL身份验证URL]</td>
          <td>输入您的Workfront实例将用于对此连接进行身份验证的URL。 <p>默认值为<code>https://oauth.my.workfront.com/integrations/oauth2</code>。</p>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL资源]</td>
          <td>输入您的[!DNL Dynamics 365]帐户的地址，不包括<code>>https://</code>。</p>
        </tr>
      </tbody>
    </table>
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

>[!NOTE]
>
>在[!DNL Microsoft Azure]门户中注册[!DNL Workfront Fusion]时，请使用以下重定向URI：
>
>* `https://app.workfrontfusion.com/oauth/cb/workfront-microsoft-dynamics2`


## [!DNL Microsoft Dynamics 365]模块及其字段

配置[!DNL Microsoft Dynamics 365]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Microsoft Dynamics 365]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

* [[!UICONTROL 观看记录（实时）]](#watch-records-real-time)
* [[!UICONTROL 观看记录（已计划）]](#watch-records-scheduled)

#### [!UICONTROL 观看记录（实时）]

此即时触发器模块在[!DNL Dynamics 365]中创建或更新您指定的记录（对象）时执行方案。

此模块中需要webhook。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td> <p>选择要用于此模块的webhook。 </p> <p>要添加新的webhook，请执行以下操作：</p> 
    <ol> 
     <li value="1"> <p>单击Webhook字段右侧的<strong>[！UICONTROL Add]</strong></p> </li> 
     <li value="2"> <p>在<strong>[！UICONTROL Webhook]</strong>名称字段中，为webhook键入一个描述性名称。</p> </li> 
     <li value="3"> <p>在<strong>[！UICONTROL连接]</strong>字段中，选择要使用的连接</p> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </li> 
     <li value="4"> <p>单击<strong>[！UICONTROL保存]</strong>以保存webhook并返回模块。</p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看记录（已计划）]

此计划触发器模块执行一个方案，即指定对象中的记录是在此方案上次计划运行之后创建或更新的。

模块的输出指示它找到的记录是新的还是更新的。 如果记录是在该时间段内添加和更新的，则作为新记录返回。

此操作在您指定的定期计划间隔内进行。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> "
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Include]</td> 
   <td>选择您希望模块仅观看<strong>[！UICONTROL新记录]</strong>、<strong>[！UICONTROL仅更新记录]</strong>还是<strong>[！UICONTROL新记录和更新记录]</strong>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL实体类型]</td> 
   <td>选择要让方案关注的[！UICONTROL Microsoft Dynamics 365]记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。 基于所选实体类型，字段可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL最大记录数]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 创建记录]](#create-record)
* [[!UICONTROL 进行API调用]](#make-an-api-call)
* [[!UICONTROL 删除记录]](#delete-record)
* [[!UICONTROL 读取记录]](#read-records)
* [[!UICONTROL 更新记录]](#update-record)


#### [!UICONTROL 创建记录]

此操作模块创建一个实体，如约会或任务。

指定有关要创建的图元的信息。

模块会返回新实体的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL实体类型]</td> 
   <td>选择您希望模块创建的实体类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择要映射的字段]</td> 
   <td>选择创建记录时要包含其值的字段。 可用字段取决于实体类型。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL属性字段]</td> 
   <td> 这些是您选择的字段。 输入您希望记录具有的给定属性值。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除记录]

此操作模块删除实体。

指定实体的ID。

模块会返回实体的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL实体类型]</td> 
   <td> <p>选择要让模块删除的实体类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL ID]</td> 
   <td> <p>输入或映射您希望模块删除的记录的唯一[!DNL Microsoft Dynamics 365] ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 进行API调用]

此操作模块允许您对[!DNL Microsoft Dynamics 365] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Microsoft Dynamics 365]模块无法实现的数据流自动化。

模块会返回有关状态代码、标题和正文的信息。 您可以在场景的后续模块中映射此信息。

要了解更多信息，请参阅有关使用[!DNL Dynamics 365 Customer Engagement Web API]的[!DNL Microsoft]文档。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL URL]</td> 
   <td> <p>输入相对于<code>&lt;Instance URL>/api/data/v9.1/</code>的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> <p>中的更多信息</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 为您添加授权标头。</p> </td> 
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

#### [!UICONTROL 读取记录]

此操作模块从[!DNL Microsoft Dynamics 365]中的单个实体读取数据。

指定实体的ID。

模块会返回实体的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL实体类型]</td> 
   <td>选择您希望模块读取的实体类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL ID]</td> 
   <td>输入或映射您希望模块读取的记录的唯一[!DNL Microsoft Dynamics 365] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新记录]

此操作模块可更新实体。

指定实体的ID。

该模块会返回更新记录的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL实体类型]</td> 
   <td>选择要更新模块的实体类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择要映射的字段]</td> 
   <td>选择创建记录时要包含其值的字段。 可用字段取决于实体类型。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL属性字段]</td> 
   <td>这些是您选择的字段。 输入您希望记录具有的给定属性值。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL ID]</td> 
   <td>输入或映射您希望模块更新的记录的唯一[!DNL Microsoft Dynamics] 365 ID。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL 搜索记录]

此搜索模块在[!DNL Microsoft Dynamics 365]中查找与您指定的搜索查询匹配的对象中的记录。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
  <td> <p>有关将[!DNL Microsoft Dynamics 365]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-microsoft-dynamics-365-to-workfront-fusion" class="MCXref xref">将[!DNL Microsoft Dynamics 365]连接到[!DNL Workfront Fusion]</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL实体类型]</td> 
   <td>选择要更新模块的实体类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL过滤器]</td> 
   <td> <p>选择要用于此搜索的过滤器。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL标准筛选器]</strong> </p> <p>选择字段和运算符，然后输入或映射要搜索的值，从而设置过滤器。 您可以在过滤器中使用AND或OR规则。</p> </li> 
     <li> <p><strong>[！UICONTROL查询函数]</strong> </p> <p>输入要用于搜索的[!DNL Dynamics 365] Web API查询函数。 </p> <p>有关查询函数的更多信息，请参阅[!DNL Microsoft]文档中的<a href="https://docs.microsoft.com/en-us/dynamics365/customer-engagement/web-api/queryfunctions?view=dynamics-ce-odata-9">Web API查询函数引用</a>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL排序]</td> 
   <td> <p>指定项目的返回顺序。 您可以添加多个排序。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL字段]</strong> </p> <p>指定要作为结果排序依据的字段。</p> </li> 
     <li> <p><strong>[！UICONTROL方向]</strong> </p> <p>指定排序方向（升序或降序）。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL最大记录数]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>
