---
title: Workfront Proof模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用 [!DNL Workfront Proof]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Workfront Proof, Digital Content and Documents
exl-id: 9e556ae5-e672-4872-9c40-8c8e5f0305be
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '2668'
ht-degree: 0%

---

# [!DNL Workfront Proof]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Workfront Proof]的工作流，并将其连接到多个第三方应用程序和服务。

如果您需要执行[!DNL Workfront]内或[!DNL Workfront Proof]中校对当前不支持的任务，例如根据某些事件更新校对和搜索校对的收件人，这将很有用。

[!DNL Workfront Proof]连接器不计入您的组织可用的活动应用程序数量。 所有方案，即使它们仅使用[!DNL Workfront Proof]应用程序，也会计入贵组织的方案总数。

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

## Workfront Proof信息

Workfront Proof连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v21.3.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.8.92</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Workfront Proof]连接到[!DNL Workfront Fusion]

您可以在[!DNL Workfront Fusion]模块内直接创建与[!DNL Workfront Proof]帐户的连接。

1. 在任意[!DNL Workfront Fusion]模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;[!UICONTROL **添加**]

2. 填写以下字段：

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Connection name]</p>
                </td>
                <td>输入连接的名称</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Environment]</td>
                <td>选择此环境是生产环境，还是非生产环境，如预览或沙盒。</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Type]</td>
                <td>选择这是服务帐户还是个人帐户。</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Email / Username]</td>
                <td>输入[!DNL Workfront Proof]帐户的用户名。</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Password]</td>
                <td>输入[!DNL Workfront Proof]帐户的密码。</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Tenant ID]</td>
                <td><strong>注意</strong>：不使用BYOK的客户必须将此字段留空。 <p>输入此帐户的租户ID。 如果您在查找租户ID时需要帮助，请联系Workfront客户支持。</p></td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Domain Extension]</td>
                <td>输入用于访问帐户的URL的扩展名。 <p>示例： <code>com</code>或 <code>eu</code></p></td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Production, Preview, or Custom Environment]</td>
                <td>要连接的生产、预览或自定义环境。</td>
            </tr>
        </tbody>
    </table>


3. 单击&#x200B;[!UICONTROL **继续**]&#x200B;保存连接并返回模块

## [!DNL Workfront Proof]模块及其字段

配置[!DNL Workfront Proof]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Workfront Proof]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

* [观看PDF摘要](#watch-for-pdf-summary)
* [[!UICONTROL Watch Proof Activity]](#watch-proof-activity)
* [观看校样](#watch-proofs)

#### [!UICONTROL Watch for PDF Summary]

当有人为校对创建PDF摘要时，此即时触发模块会执行场景。

此模块中需要webhook。

模块返回与验证关联的所有标准字段，以及连接访问的任何自定义字段和值。 它还为PDF摘要创建新的事件订阅，并输出有效负载中发送的`pdf_url`属性中的内容。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Webhook name]</td> 
   <td>输入或映射新webhook的名称</td> 
  </tr> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Proof Activity]

此触发器模块执行对验证验证执行指定活动时的场景。

模块返回与验证关联的所有标准字段，以及连接访问的任何自定义字段和值。 它还为PDF摘要创建新的事件订阅，并输出有效负载中发送的`pdf_url`属性中的内容。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Activity type]</td> 
   <td>选择您是要观看任何新决策（包括验证状态更改），还是只观看整体验证状态更改。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Limit]</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch Proofs]

当有人创建验证或做出决策时，此计划触发器模块执行场景。

该模块会返回一个列表，列出在指定的时间段内找到的所有记录及其类型。 它还会返回您指定的字段值。 如果模块发现对验证做出了决策，则会在单独的字段中包含之前值和当前值。 您可以在场景的后续模块中映射此信息。

此操作在您指定的定期计划间隔内进行。

您必须具有足够权限才能访问[!DNL Workfront Proof]中的证明或验证，才能检索此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td>选择您是要监视新验证，还是要监视新的总体验证决策。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">限制</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">每页项目数</td> 
   <td> <p>要分页结果，请输入或映射应在结果每页上显示的返回结果数。 此数字必须小于或等于100。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Create Proof]](#create-proof)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Download Proof]](#download-proof)
* [[!UICONTROL Read a Record]](#read-a-record)
* [[!UICONTROL Request PDF Summary]](#request-pdf-summary)
* [[!UICONTROL Update Proof]](#update-proof)
* [[!UICONTROL Upload File]](#upload-file)

#### [!UICONTROL Create Proof]

<!--Cannot test Jan 2025-->

此操作模块在[!DNL Workfront Proof]中创建新验证或新版本的验证。

您可以为新验证指定参数，如果要创建新版本，请指定源验证。

模块返回新验证或验证版本的ID。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Type]</td> 
   <td> <p>指定您希望创建的验证具有基本工作流还是[!UICONTROL Automated Workflow]。</p> <p>然后，填写为您选择的验证类型显示的字段。 例如，如果您选择[!UICONTROL Automated Workflow]，请填写<strong>[!UICONTROL Workflow Stages]</strong>字段以配置阶段。</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Allow original file to be downloaded]</td> 
   <td>选择是否允许下载从中创建校对的原始文件。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Classic Proof Viewer]</td> 
   <td>选择是否使用经典校样查看器。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Combine all files into single proof]</td> 
   <td>启用此选项可将所有文件合并到单个多页验证中。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create a new proof version]</td> 
   <td>如果希望模块创建现有校对的新版本，请选择此选项。 然后在显示的<strong>[!UICONTROL Existing Proof ID]</strong>字段中，映射或输入验证的唯一ID。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link Label]</td> 
   <td>输入或映射自定义验证链接的标签。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Custom Link URL]</td> 
   <td>输入或映射自定义链接的URL。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>键入以下数字之一，以指示要将以下哪些默认电子邮件通知设置用于已创建的验证。
    <ul>
     <li><strong>1</strong> — 所有新评论和回复</li>
     <li><strong>2</strong> — 回复我的评论</li>
     <li><strong>3</strong> — 每日摘要</li>
     <li><strong>4</strong> — 每小时摘要</li>
     <li><strong>5</strong> — 仅决策</li>
     <li><strong>9</strong> — 已禁用</li>
    </ul></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Excel Summary]</td> 
   <td>选择是否要禁用将验证评论下载到Excel文件的功能。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable PDF Summary]</td> 
   <td>选择是否要禁用将校对注释下载到PDF文件的功能。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>选择是否要为此验证禁用订阅电子邮件。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Embed Player]</td> 
   <td>选择是否要为此验证启用嵌入的播放器。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>选择是否允许非参与者订阅验证。<br>如果选择此选项，还可以为订阅者选择“默认角色”，如本表所述。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>选择是否要启用订阅电子邮件验证。 如果启用此项，订阅者必须单击电子邮件中的链接才能访问验证。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>选择您希望创建的校对隐藏还是显示团队URL。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Hash] <span style="font-weight: normal;">或</span> [!UICONTROL File Hashes]</td> 
   <td>添加要从中创建验证的一个或多个文件的ID。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL File Names]</td> 
   <td>为创建的验证添加一个或多个文件名这是必填字段。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>指定您是否希望在做出所有必需的决策后锁定创建的验证。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Notify recipients about this proof]</td> 
   <td>选择一个选项，以指示您是否希望在创建验证时通知收件人。&gt;</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof name]</td> 
   <td>为创建的验证键入名称。这是必填字段。 使用管道符号(|)为多个校样分隔名称。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof owner ID]</td> 
   <td>输入或映射验证所有者的ID。 如果此字段留空，则验证所有者将设置为当前用户。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Reference ID]</td> 
   <td>输入验证的参考ID。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require electronic signature]</td> 
   <td>选择您是否希望要求决定证明的任何人提交电子签名。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>指定您是否希望创建的验证需要登录。 </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Resolution ID]</td> 
   <td>输入要用于校对的分辨率ID。 有关分辨率ID的列表，请参阅[!DNL Workfront Proof] <a href="https://api.proofhq.com/home/objects/soapworkflowproofobject.html">API文档</a>。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL SWF]</td> 
   <td>输入SWF验证的类型。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Show] [项目]</td> 
   <td>对于每个项目，选择是否要将其显示在验证中。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Workspace ID]</td> 
   <td>输入要在其中创建验证的工作区的ID。 </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Recipients]</td> 
   <td>为创建的验证添加所需收件人的电子邮件地址。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>指定您希望创建的验证的截止日期。 使用以下日期格式：</p> <p><code>YYYY-MM-DD hh:mm</code></p> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL Custom API Call]

此操作模块允许您对[!DNL Workfront Proof] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Workfront Proof]模块无法实现的数据流自动化。

模块会返回状态代码、标题和正文。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Method]</td> 
   <td>为API调用设置操作。 有关可用操作，请参阅<a href="https://api.proofhq.com/">验证API文档</a>。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Body (XML)]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**示例：**
>
>![验证API模块示例](/help/workfront-fusion/references/apps-and-modules/assets/wfp-api-module-example-350x586.png)

#### [!UICONTROL Download Proof]

此操作模块下载您使用其ID识别的特定验证的源文件。

您指定校样的ID。

模块会返回用于创建验证的源文件的内容。您可以在场景的后续模块中映射此信息。

您必须具有足够的权限才能访问[!DNL Workfront Proof]中的记录以检索此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>键入在[!UICONTROL Proof Details]页面上找到的验证的唯一ID。  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a Record]

此操作模块从[!DNL Workfront Proof]中的单个验证中读取数据。

您可以指定校样的ID以及您想要从校样中获得的信息。

模块会返回您为验证选择的字段的值及其类型。 您可以在场景的后续模块中映射此信息。

您必须具有足够的权限才能访问[!DNL Workfront Proof]中的记录以检索此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td>选择您要读取校样、校样评论还是校样审阅者。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL ID]</td> 
   <td>输入或映射您希望模块读取的记录的唯一[!DNL Workfront Proof] ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Request PDF Summary]

此操作模块请求[!DNL Workfront Proof]中特定证明的PDF摘要。

您指定校样的ID。

该模块返回PDF摘要信息。 您可以在场景的后续模块中映射此信息。

您必须具有足够的权限才能访问[!DNL Workfront Proof]中的记录以检索此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>输入您要为其请求PDF摘要的验证的唯一[!DNL Workfront Proof] ID。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Callback URL]</td> 
   <td>输入或映射要发送PDF摘要的URL。</td> 
  </tr> 
 </tbody> 
</table>

##### 可能存在的错误

* **错误**：“[!UICONTROL You do not have privilege to perform this request. The stage must contain at least one recipient.]”
* **解决方案**：确保您不是唯一一个分配到工作流阶段的人。 必须为工作流的阶段分配另一个用户。

#### [!UICONTROL Update Proof]

此操作模块更新[!DNL Workfront Proof]中的现有校对。

您可以指定校样的ID和记录类型以及要包含在输出中的字段。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

您必须具有足够的权限才能访问[!DNL Workfront Proof]中的记录以检索此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID]</td> 
   <td> <p>键入在[!UICONTROL Proof Details]页面上找到的验证的唯一ID。 </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Deadline]</td> 
   <td> <p>指定您希望创建的验证的截止日期。 使用日期格式<code>YYYY-MM-DD hh:mm</code>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default email notifications for subscribers]</td> 
   <td>选择您希望为创建的验证使用的以下默认电子邮件通知设置之一。
    <ul>
     <li> [!UICONTROL All new comments and replies]</li>
     <li>[!UICONTROL Replies to my comments]</li>
     <li>[!UICONTROL Daily summary]</li>
     <li> [!UICONTROL Hourly summary]</li>
     <li> [!UICONTROL Decisions only]</li>
     <li> [!UICONTROL Disabled]</li>
    </ul></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Default Role]</td> 
   <td>选择验证的默认角色。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Disable Subscription Email]</td> 
   <td>选择是否要为此验证禁用订阅电子邮件。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions]</td> 
   <td>选择是否允许非参与者订阅验证。<br>如果选择此选项，还可以在[!UICONTROL Default Role]字段中选择选项。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Subscriptions Validation]</td> 
   <td>选择是否要启用订阅电子邮件验证。 如果启用此项，订阅者必须单击电子邮件中的链接才能访问验证。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Enable Team URL]</td> 
   <td>选择您希望创建的校对隐藏还是显示团队URL。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Lock proof when all required decisions are made]</td> 
   <td>指定您是否希望在做出所有必需的决策后锁定创建的验证。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Message]</td> 
   <td>输入或映射要与校样一起显示的消息。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof ID] </td> 
   <td>输入或映射要更新的校对ID。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Proof Name]</td> 
   <td>输入或映射要更新的校对的名称。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Require login]</td> 
   <td> <p>指定您是否希望创建的验证需要登录。 </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show Versions Like]</td> 
   <td>选择是否要显示此校对的其他版本的链接。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>输入或映射验证的主题</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload File]

此操作模块上传文件以便与[!DNL Workfront Proof]中的[!UICONTROL Create Proof]模块一起使用。

模块会返回已上传文件的哈希ID。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL List Workflow Templates]](#list-workflow-templates)
* [[!UICONTROL Search]](#search)

#### [!UICONTROL List Workflow Templates]

此搜索模块列出了所有可用的工作流模板。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Limit]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大模板数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search]

此搜索模块在[!DNL Workfront Proof]中查找与您指定的搜索查询匹配的对象中的记录。

如果正在搜索验证，模块将返回验证的ID。 如果正在搜索收件人，则它会返回收件人的用户ID、电子邮件、名称、位置和电子邮件别名。您可以将此信息映射到场景中的后续模块。

您必须具有足够的权限才能访问[!DNL Workfront Proof]中的记录以检索此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!DNL Connection]</td> 
   <td> <p>有关将[!DNL Workfront Proof]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Search for]</td> 
   <td> <p>选择要模块搜索的记录类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Proof]</strong> </p> <p>输入要搜索的校对的校对名称。</p> </li> 
     <li> <p><strong>[!UICONTROL Recipient]</strong> </p> <p>输入要搜索的收件人的电子邮件地址。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Result Set]</td> 
   <td>指示模块将搜索<strong>[!UICONTROL All Matching Records]</strong>还是仅搜索<strong>[!UICONTROL First Matching Record]</strong>。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sort By]</td> 
   <td>选择要作为结果排序依据的字段。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Sorting Direction]</td> 
   <td> <p>选择要按升序或降序对结果进行排序。</p> </td> 
  </tr> 
 </tbody> 
</table>

