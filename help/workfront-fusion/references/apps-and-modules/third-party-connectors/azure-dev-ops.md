---
title: Azure DevOps模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用 [!DNL Azure DevOps]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 0%

---

# [!DNL Azure DevOps]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Azure DevOps]的工作流，并将其连接到多个第三方应用程序和服务。

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

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

要使用[!DNL Azure DevOps]模块，您必须具有[!DNL Azure] DevOps帐户。

## [!DNL Azure DevOps] API信息

Azure DevOps连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## 将[!DNL Azure DevOps]连接到[!DNL Workfront Fusion] {#connect-azure-devops-to-workfront-fusion}

1. 将[!DNL Azure DevOps]模块添加到您的方案。
1. 单击[!UICONTROL 连接]字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 在[!UICONTROL 连接类型]字段中，选择&#x200B;**[!DNL Azure DevOps]**。

   >[!IMPORTANT]
   >
   >[!UICONTROL [!DNL Azure DevOps] （请求所有范围）]连接类型不久将被弃用。 因此，我们不建议使用它。

1. 填写以下字段：

   <table style="table-layout:auto">
        <tr>
            <td>[!UICONTROL 连接名称]</td>
            <td>输入正在创建的连接的名称。</td>
        </tr>
      <tr>
            <td>[!UICONTROL 组织]</td>
            <td>输入您创建了[!DNL Azure DevOps]应用程序的组织的名称。</td>
        </tr>
    </table>

1. 要输入Azure DevOps应用程序ID或客户端密钥，请单击<b>显示高级设置</b>，然后在打开的字段中输入它们。
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;完成连接设置并继续创建方案。

## [!UICONTROL Azure DevOps]模块及其字段

配置[!DNL Azure DevOps]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Azure DevOps]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!UICONTROL 关注工作项]

此即时触发器模块在[!UICONTROL Azure DevOps]中添加、更新或删除记录时执行方案。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>为模块选择或添加webhook。</p> <p>有关触发器模块中Webhook的详细信息，请参阅<a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">即时触发器(Webhook)</a>。</p> <p>有关如何创建Webhook的信息，请参阅<a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref">Webhook</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [创建记录](#create-a-record)
* [自定义API调用](#custom-api-call)
* [下载附件](#download-an-attachment)
* [链接工作项](#link-work-items)
* [读取记录](#read-record)
* [更新工作项](#update-a-work-item)
* [[!UICONTROL 上载附件]](#upload-an-attachment)

#### [!UICONTROL 创建记录]

此操作模块创建新项目或工作项。

模块输出新创建的工作项的对象ID，或新创建项目的URL和状态代码。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择您要创建工作项还是项目。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 项目]</strong> </p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL 名称]</strong>：输入或映射新项目的名称。</p> </li> 
       <li> <p><strong>[!UICONTROL 描述]</strong>：输入或映射新项目的描述。 </p> </li> 
       <li> <p><strong>[!UICONTROL 可见性]</strong>：选择您希望项目是公共项目还是专用项目。 用户必须已登录您的组织，并且必须已被授予项目访问权限，才能与专用项目交互。 公共项目对未登录到您的组织的用户可见。</p> </li> 
       <li> <p><strong>[!UICONTROL 版本控制]</strong>：选择您希望项目使用[!DNL Git]还是[!UICONTROL Team Foundation版本控制(TFCV)]进行版本控制。</p> </li> 
       <li> <p><strong>[!UICONTROL 工作项进程]</strong>：选择要用于项目的工作进程。 选项有[!UICONTROL Basic]、[!UICONTROL Scrum]、[!UICONTROL 功能成熟度模型集成(CMMI)]和[!UICONTROL Agile]。</p> <p>有关[!DNL Azure DevOps]进程的详细信息，请参阅[!DNL Azure DevOps]文档中的<a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&amp;tabs=basic-process">默认进程和进程模板</a>。</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL 工作项]</strong> </p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL 项目]</strong>：选择要创建工作项的项目。</p> </li> 
       <li> <p><strong>[!UICONTROL 工作项类型]</strong>：选择要创建的工作项类型。</p> </li> 
       <li> <p><strong>[!UICONTROL 其他字段]</strong>：在这些字段中，输入您希望工作项具有的给定属性值。 可用字段取决于工作项类型。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义API调用]

此操作模块允许您对[!DNL Azure DevOps] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Azure DevOps]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 基本URL]</td> 
   <td> <p>选择或映射用于连接到[!DNL Azure DevOps]帐户的基本URL</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 相对URL]</td> 
   <td> <p>输入为此API调用要连接的相对URL。</p> <p><b>示例： </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL API版本]</td> 
   <td>选择或映射要为此API调用连接到的[!DNL Azure DevOps] API的版本。 如果未选择版本，[!DNL Workfront Fusion]将连接到[!DNL Azure DevOps] API版本5.1。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
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

#### [!UICONTROL 下载附件]

此操作模块下载附件。

模块将返回附件的文件内容。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 附件URL]</td> 
   <td> <p>输入或映射要下载的附件的URL。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 链接工作项]

此操作模块链接两个工作项并定义它们之间的关系。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作项ID]</td> 
   <td>输入或映射要链接其他工作项的主工作项的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 链接的工作项ID]</td> 
   <td>输入或映射要链接到主工作项的工作项的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 链接类型]</td> 
   <td> <p>定义要链接的工作项之间的关系。</p> <p>有关详细信息，请参阅[!UICONTROL Azure DevOps]文档中的<a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops">链接类型参考指南</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>输入或映射注释的文本。 这对于解释链接的推理或意图很有用。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

此操作模块从[!DNL Azure DevOps]中的单个记录读取数据。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择您要读取项目还是工作项</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 项目]</strong>：选择要读取的项目。</p> </li> 
     <li> <p><strong>[!UICONTROL 工作项]</strong>：选择包含要读取的工作项的项目，然后选择该工作项类型。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要包含在此模块的输出捆绑包中的信息。 可用字段取决于工作项类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射要读取的记录的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新工作项]

该操作模块使用其ID更新现有工作项。

模块返回已更新工作项的ID。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目]</td> 
   <td>选择包含要更新的工作项的项目。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作项类型]</td> 
   <td> <p>选择要更新的工作项的类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 其他字段]</td> 
   <td>在每个字段中，输入您希望工作项具有的给定属性值。 可用字段取决于工作项类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作项ID]</td> 
   <td>输入或映射要更新的工作项的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上载附件]

此操作模块上传文件并将其附加到工作项。

模块会返回附件的附件ID和下载URL。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目] </td> 
   <td> <p>选择要上载附件的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作项ID]</td> 
   <td> <p>输入或映射要上载附件的工作项的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>输入要添加到上载附件的注释文本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file] </td> 
   <td>从以前的模块中选择源文件，或者输入或映射源文件的名称和内容。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL 列出工作项]

此操作模块检索[!DNL Azure DevOps]项目中特定类型的所有工作项。

模块返回主工作项和任何关联字段的ID，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Azure DevOps]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref">将[!DNL Azure DevOps]连接到[!UICONTROL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 项目]</td> 
   <td>选择要从中检索工作项的项目。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 工作项类型]</td> 
   <td> <p>选择要检索的工作项类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td>选择要显示在模块输出中的属性。 可用字段取决于您要检索的工作项的类型。 您必须至少选择一个属性。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射[!DNL Workfront Fusion]在一个执行周期内返回的最大工作项数。</td> 
  </tr> 
 </tbody> 
</table>
