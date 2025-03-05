---
title: Adobe Acrobat Sign模块
description: 使用 [!DNL Adobe Acrobat Sign] 模块，您可以基于 [!DNL Adobe] Acrobat Sign帐户中的事件启动 [!DNL Adobe Workfront Fusion] 方案，创建、读取或更新协议和其他记录，使用您设置的条件搜索记录以及上传文档。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0ef9d40e-8ad6-434e-8fa0-076920ff29ea
source-git-commit: 85cd8dbf70dff220f593fa669b447bf5df2a21a2
workflow-type: tm+mt
source-wordcount: '6666'
ht-degree: 0%

---

# [!DNL Adobe Acrobat Sign]模块

通过[!DNL Adobe Acrobat Sign]模块，您可以基于[!DNL Adobe Acrobat Sign]帐户中的事件启动[!DNL Adobe Workfront Fusion]方案，创建、读取或更新协议和其他记录，使用您设置的条件搜索记录以及上传文档。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
  <td> <p>[！UICONTROL Pro]或更高版本</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
   <td> <p>[！UICONTROL计划]，[！UICONTROL工作]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前许可证要求：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[！UICONTROL [!DNL Workfront Fusion] for Work Automation and Integration] </p>
   </td>  
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[！UICONTROL Select]或[！UICONTROL Prime] [!DNL Adobe Workfront]计划，则贵组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[！UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## [!DNL Adobe Acrobat Sign] API信息

Adobe Acrobat Sign连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v6 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.35.1</td> 
  </tr>
 </tbody> 
</table>


## [!DNL Adobe Acrobat Sign]连接器使用建议

[!DNL Adobe Sign]应用程序使[!DNL Fusion]中的自动化eSignature业务流程更加简单和强大。

[!DNL Adobe Sign]的新用户应密切注意与更新协议相关的一些限制。 协议通常在启动后不会更改。 我们建议[!DNL Adobe Sign]的新用户侧重于使用协议创建模块创建新协议。 这将使[!DNL Fusion]自动化更容易，并且更好地用于[!DNL Adobe Sign]。

[!DNL Adobe Sign]协议需要一个字段来处理。 有多种方法可用于执行此操作，但最简单、最常见的方法是上传临时文档，然后将该文档映射到您的协议。

![Adobe Sign建议](/help/workfront-fusion/references/apps-and-modules/assets/adobe-sign-recommendations-350x168.png)

## [!DNL Adobe Acrobat Sign]模块及其字段

配置[!DNL Adobe Acrobat Sign]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Adobe Acrobat Sign]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

<!--
* [Watch for agreements](#watch-for-agreements) 
* [Watch for events](#watch-for-events)
-->

+++ **[!UICONTROL 关注协议]**

此触发器模块会在创建或更新协议时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
<td>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL筛选器]</td> 
   <td>选择要监视新记录、更新记录还是两者。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型] </td> 
   <td>选择您希望记录监视的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查找文本]</td> 
   <td> <p>输入要搜索的搜索词。 模块会返回包含这些术语作为字段值的记录。</p> <p>有关在[!DNL Adobe Acrobat Sign]中搜索字段的更多信息，请参阅<a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">Adobe Sign搜索中的“文本搜索的工作原理” — 其工作方式</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL返回的最大协议数]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 观看活动]**

当您选择的事件发生时，此触发器模块会启动一个方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td>选择要使用的webhook，或单击<b>[！UICONTROL添加]</b>并填写以下字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Webhook名称]</td> 
   <td> <p>输入webhook的名称</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL范围]</td> 
   <td> 
    <ul> 
     <li> <p>[！UICONTROL帐户]</p> </li> 
     <li> <p>[！UICONTROL组]</p> </li> 
     <li> <p>[！UICONTROL用户]</p> </li> 
     <li> <p>[！UICONTROL资源]</p> <p>如果选择[！UICONTROL资源]，请输入资源ID和资源类型。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资源级别]</td> 
   <td> <p>选择要监视的资源类型。</p> 
    <ul> 
     <li> <p>[！UICONTROL协议]</p> </li> 
     <li> <p>[！UICONTROL小组件]</p> </li> 
     <li> <p>[！UICONTROL兆符号]</p> </li> 
     <li> <p>[！UICONTROL库文档]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Webhook订阅事件]</td> 
   <td>选择您希望模块监视的[!DNL Adobe Sign]事件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL应用程序显示名称]</td> 
   <td>用于创建webhook的应用程序的显示名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL应用程序名称]</td> 
   <td>用于创建webhook的应用程序的显示名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL问题通知电子邮件]</td> 
   <td> <p>此设置仅适用于管理员帐户</p> <p>对于要向其发送问题通知电子邮件的每个电子邮件地址，单击<b>[！UICONTROL添加]</b>并输入电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Agreement条件参数]</td> 
   <td>如果要添加任何条件参数，请在要添加参数的记录类型上选择<b>[！UICONTROL是]</b>，然后在要启用的任何参数上选择<b>[！UICONTROL是]</b>。</td> 
  </tr> 
 </tbody> 
</table>

+++

### 操作

<!--
* [Create a record](#create-a-record) 
* [Create an agreement](#create-an-agreement) 
* [Create related records](#create-related-records) 
* [Custom API Call](#custom-api-call) 
* [List records](#list-records) 
* [Read a record](#read-a-record) 
* [Read related records](#read-related-records) 
* [Update a record](#update-a-record) 
* [Update related record](#update-related-record) 
* [Upload document](#upload-document)
-->

+++ **[!UICONTROL 创建记录]**

此操作模块创建选定类型的新记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td>以标准JSON对象的形式添加请求的标头。 例如， <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td> <p>选择要创建的记录类型。</p> 
    <ul> 
     <li> <p><b>[！UICONTROL组]</b> </p> </li> 
     <li> <p><b>[！UICONTROL库文档]</b> </p> </li> 
     <li> <p><b>[！UICONTROL用户]</b> </p> </li> 
     <li> <p><b>[！UICONTROL Web窗体] ([！UICONTROL Widget])</b> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL组信息]</td> 
   <td> <p>输入或映射组的[！UICONTROL名称]和[！UICONTROL ID]，并指示此组是否为帐户的默认组。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL库文档信息]</td> 
   <td> <p>填写以下字段：</p> 
    <ul> 
     <li> <p><b>[！UICONTROL要发送的文件]</b> </p> <p>对于每个要添加的文件，单击<b>[！UICONTROL添加项]</b>并填写相应的字段。</p> 
      <ul> 
       <li><b>[！UICONTROL临时文档ID]</b> <p>输入临时文档的ID</p> </li> 
       <li> <p><b>[！UICONTROL URL文件传输]</b> </p> <p>填写以下字段：</p> 
        <ul> 
         <li> <p><b>[！UICONTROL Mime-Type]</b> </p> <p>输入原始文件的mime类型。 多用途Internet邮件扩展(MIME)类型是允许软件识别在Internet上共享的不同类型数据的标签。 Web服务器和浏览器使用MIME类型来确定应该对文件执行的操作。 例如，在浏览器中处理MIME类型为<code>text/html</code>的文件的方式与MIME类型为<code>image/jpeg</code>的文件的方式不同。</p> </li> 
         <li> <p><b>[！UICONTROL名称]</b> </p> <p>输入文件的名称。</p> </li> 
         <li> <p><b>[！UICONTROL URL]</b> </p> <p>输入要发送的文件的URL。</p> </li> 
        </ul> </li> 
       <li> <p><b>[！UICONTROL Notarize]</b> </p> <p>选择是否需要对此文档进行公证。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL库模板名称]</b> </p> <p>输入或映射库模板的名称</p> </li> 
     <li> <p><b>[！UICONTROL共享模式]</b> </p> <p>指定应该有权访问库文档的人员。</p> </li> 
     <li> <p><b>[！UICONTROL库文档状态]</b> </p> <p>选择文档处于创作状态还是活动状态。</p> </li> 
     <li> <p><b>[！UICONTROL库模板类型]</b> </p> <p>对于每个要使用的库模板类型，单击<b>[！UICONTROL添加项]</b>并选择模板类型。</p> </li> 
     <li> <p><b>[！UICONTROL上次事件日期]</b> </p> <p>输入库文档上发生事件的最后日期。</p> <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </li> 
     <li> <p><b>[！UICONTROL库文档状态]</b> </p> <p>选择库文档的状态。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL用户信息]</td> 
   <td> <p>填写以下字段：</p> 
    <ul> 
     <li> <p><b>[！UICONTROL电子邮件]</b> </p> <p>输入用户的电子邮件地址。</p> </li> 
     <li> <p><b>[！UICONTROL是帐户管理员]</b> </p> <p>如果创建的用户是帐户管理员，请选中此选项。</p> </li> 
     <li> <p><b>[！UICONTROL用户ID]</b> </p> <p>输入用户的唯一ID</p> </li> 
     <li> <p><b>[！UICONTROL帐户ID]</b> </p> <p>输入与此用户关联的[!DNL Adobe Acrobat Sign]帐户的唯一ID。</p> </li> 
     <li> <p><b>[！UICONTROL名字]</b> </p> <p>输入用户的名字。</p> </li> 
     <li> <p><b>[！UICONTROL姓氏]</b> </p> <p>输入用户的姓氏</p> </li> 
     <li> <p><b>[！UICONTROL公司]</b> </p> <p>输入用户的公司名称。</p> </li> 
     <li> <p><b>[！UICONTROL首字母]</b> </p> <p>输入用户的首字母。</p> </li> 
     <li> <p><b>[！UICONTROL区域设置]</b> </p> <p>输入用户的区域设置。 这会确定UI的语言。 </p> </li> 
     <li> <p><b>[！UICONTROL Phone]</b> </p> <p>输入用户的电话号码</p> </li> 
     <li> <p><b>主要组ID</b> </p> <p>输入将新用户添加到其中的组。 如果未输入任何内容，则用户将被添加到帐户的默认组中。</p> </li> 
     <li> <p><b>[！UICONTROL作业标题]</b> </p> <p>输入用户的工作标题。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Web窗体信息]</td> 
   <td> <p>填写以下字段</p> 
    <ul> 
     <li> <p><b>[！UICONTROL文件信息]</b> </p> <p>对于每个要添加到Web表单的文件，单击“添加”并填写以下字段：</p> 
      <ul> 
       <li> <p>[！UICONTROL文件类型]</p> <p>[！UICONTROL文档]</p> </li> 
       <li> <p>[！UICONTROL临时文档]</p> </li> 
       <li> <p>[！UICONTROL URL文件信息]</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL Web窗体名称]</b> </p> <p>输入Web窗体的名称。 此名称用于标识位置（如电子邮件和网站）中的Web窗体。</p> </li> 
     <li> <p><b>[！UICONTROL Web窗体状态]</b> </p> <p>选择应创建新Web窗体的状态。</p> </li> 
     <li> <p><b>[！UICONTROL Web窗体参与者集信息]</b> </p> 
      <ul> 
       <li> <p><b>[！UICONTROL成员信息]</b> </p> <p>对于要添加到参与者集的每个成员，单击<b>[！UICONTROL添加项]</b>。 </p> 
        <ul> 
         <li> <p><b>[！UICONTROL电子邮件]</b> </p> <p>将此选项留空。</p> </li> 
         <li> <p><b>[！UICONTROL安全选项]</b> </p> <p>如果要添加用于验证此用户的安全选项，请选择<b>[！UICONTROL是]</b>，然后选择该安全选项并填写它所需的任何字段。</p> </li> 
        </ul> </li> 
       <li> <p><b>[！UICONTROL角色]</b> </p> <p>选择角色。 此参与者集的所有成员共享角色。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL Web窗体附加参与者集信息]</b> </p> 
      <ul> 
       <li> <p><b>[！UICONTROL成员信息]</b> </p> <p>对于要添加到参与者集的每个成员，单击<b>[！UICONTROL添加项]</b>。</p> 
        <ul> 
         <li> <p><b>[！UICONTROL电子邮件]</b> </p> <p>将此选项留空。</p> </li> 
         <li> <p><b>[！UICONTROL安全选项]</b> </p> <p>如果要添加用于验证此用户的安全选项，请选择<b>[！UICONTROL是]</b>，然后选择该安全选项并填写它所需的任何字段。</p> </li> 
        </ul> </li> 
       <li> <p><b>[！UICONTROL角色]</b> </p> </li> 
       <li> <p><b>[！UICONTROL Web窗体参与者ID] </b> </p> <p>输入Web窗体参与者的标识。</p> </li> 
       <li> <p><b>[！UICONTROL顺序]</b> </p> <p>指定此参与者集应与Web窗体交互的顺序。 例如，顺序值为1的参与者组必须首先运行，2必须运行下一步，依此类推。 订单编号必须以一个开头，且系列中没有间隙。 </p> </li> 
       <li> <p><b>[！UICONTROL提供程序参与者集信息]</b> </p> <p>如果参与者未知，请输入提供者是否必须提供参与者的详细信息，然后输入包含未知参与者所需详细信息的消息。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL身份验证失败信息]</b> </p> <p>如果要为用户提供失败或错误页面，请选择<b>[！UICONTROL是]</b>，然后填写以下字段：</p> 
      <ul> 
       <li> <p><b>[！UICONTROL URL]</b> </p> <p>输入错误页面的URL</p> </li> 
       <li> <p><b>[！UICONTROL解帧]</b> </p> <p>如果希望错误页面显示在Web窗体中，请启用此选项</p> </li> 
       <li> <p><b>[！UICONTROL延迟]</b> </p> <p>输入将用户重定向到错误页面之前的延迟（以秒为单位）。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL CC信息]</b> </p> <p>对于您希望在签署Web窗体上的最终协议时收到电子邮件的每个电子邮件地址，单击<b>[！UICONTROL添加项]</b>并输入电子邮件地址。</p> </li> 
     <li> <p><b>[！UICONTROL完成信息]</b> </p> <p style="font-style: normal;">如果要为用户提供成功页面，请选择<b>[！UICONTROL是]</b>，然后填写以下字段：</p> 
      <ul> 
       <li> <p><b>[！UICONTROL URL]</b> </p> <p>输入成功页面的URL</p> </li> 
       <li> <p><b>[！UICONTROL解帧]</b> </p> <p>如果希望成功页面显示在Web窗体中，请启用此选项</p> </li> 
       <li> <p><b>[！UICONTROL延迟]</b> </p> <p>输入在将用户重定向到成功页面之前的延迟（以秒为单位）。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL组ID]</b> </p> <p>输入Web窗体所属的组的ID。 如果未输入任何内容，则Web窗体属于帐户用户的主要组。</p> </li> 
     <li> <p><b>[！UICONTROL上次事件日期]</b> </p> <p>输入Web窗体上发生最后事件的日期。 使用格式<code>yyyy-MM-dd'T'HH:mm:ssZ</code>。</p> </li> 
     <li> <p><b>[！UICONTROL区域设置]</b> </p> <p>输入用户的区域设置。 这会确定UI的语言。 </p> </li> 
     <li> <p><b>[！UICONTROL安全选项]n</b> </p> <p>输入用于保护文档的密码。 您必须单独将此密码传达给任何相关方。</p> </li> 
     <li> <p><b>[！UICONTROL保险存储信息]</b> </p> <p>如果您的帐户设置为单据电子仓库，并且每个协议都启用了选项，则可以启用此选项以电子仓库此协议。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 创建协议]**

该操作模块将创建一个协议，发送它以供签名，并返回协议ID。

>[!NOTE]
>
>我们建议上载文档以作为临时文档签名，然后将其映射到[!UICONTROL 创建协议]模块中的[!UICONTROL 要发送的文件]字段。 有关示例，请参阅本文中的“上传文档”。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
<td>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a></td>  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td>以标准JSON对象的形式添加请求的标头。 例如， <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">要发送的[！UICONTROL文件]</td> 
   <td> <p>对于要包含在协议中的每个项目，单击<b>[！UICONTROL添加项目]</b>并填写以下字段：</p> 
    <ul> 
     <li> <p><b>[！UICONTROL文件类型]</b> </p> 
      <ul> 
       <li> <p><b>[！UICONTROL文档]</b> </p> <p>填写以下字段：</p> 
        <ul> 
         <li> <p><b>[！UICONTROL创建日期]</b> </p> <p>以<code>yyyy-MM-dd'T'HH:mm:ssZ</code>格式输入或映射文档创建日期。 例如，<code>2016-02-25T18:46:19Z</code>表示UTC时间。</p> </li> 
         <li> <p><b>[！UICONTROL ID]</b> </p> <p>输入或映射文档的ID。</p> </li> 
         <li> <p><b>[！UICONTROL标签]</b> </p> <p>输入或映射文件的唯一标签。 对于自定义工作流，这会将文件映射到工作流定义中对应的文件元素。 在自定义工作流协议创建请求中，必须指定此项。</p> </li> 
         <li> <p><b>[！UICONTROL页数]</b> </p> <p>输入或映射文档中的页数。</p> </li> 
         <li> <p><b>[！UICONTROL Mime-Type]</b> </p> <p>输入或映射原始文件的mime类型。 多用途Internet邮件扩展(MIME)类型是允许软件识别在Internet上共享的不同类型数据的标签。 Web服务器和浏览器使用MIME类型来确定应该对文件执行的操作。 例如，在浏览器中处理MIME类型为<code>text/html</code>的文件的方式与MIME类型为<code>image/jpeg</code>的文件的方式不同。</p> </li> 
         <li> <p><b>[！UICONTROL名称]</b> </p> <p>输入或映射文档的名称。<br></p> </li> 
        </ul> </li> 
       <li> <p><b>[！UICONTROL库文档ID]</b> </p> <p>输入库文档的ID</p> </li> 
       <li> <p><b>[！UICONTROL临时文档ID]</b> </p> <p>输入临时文档的ID</p> </li> 
       <li> <p><b>[！UICONTROL URL文件传输]</b> </p> <p>填写以下字段：</p> 
        <ul> 
         <li> <p><b>[！UICONTROL Mime-Type]</b> </p> <p>输入原始文件的mime类型。 多用途Internet邮件扩展(MIME)类型是允许软件识别在Internet上共享的不同类型数据的标签。 Web服务器和浏览器使用MIME类型来确定应该对文件执行的操作。 例如，在浏览器中处理MIME类型为<code>text/html</code>的文件的方式与MIME类型为<code>image/jpeg</code>的文件的方式不同。</p> </li> 
         <li> <p><b>[！UICONTROL名称]</b> </p> <p>输入文件的名称。</p> </li> 
         <li> <p><b>[！UICONTROL URL]</b> </p> <p>输入要发送的文件的URL。</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL标签]</b> </p> <p>输入文件的标签。</p> </li> 
     <li> <p><b>[！UICONTROL Notarize]</b> </p> <p>启用此选项以指示文件必须经过公证。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL协议名称]</td> 
   <td>输入新协议的名称。 此名称用于标识电子邮件和网站等位置中的协议。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL参与者集信息]</td> 
   <td> <p>对于要添加的每个参与者集，单击<b>[！UICONTROL添加项]</b>并填写以下字段。</p> 
    <ul> 
     <li> <p><b>[！UICONTROL成员]</b> </p> <p>对于要添加到参与者集的每个人，单击<b>[！UICONTROL添加项]</b>并输入此人的电子邮件地址。</p> </li> 
     <li> <p><b>[！UICONTROL顺序]</b> </p> <p>指定此参与者集签署协议的顺序。 例如，订单值为1的参与者组必须首先签名，2则必须先签名，依此类推。 订单编号必须以一个开头，且系列中没有间隙。 </p> </li> 
     <li> <p><b>[！UICONTROL角色]</b> </p> <p>为此参与者集选择角色。 集合中的所有参与者都将获得此角色。</p> </li> 
     <li> <p><b>[！UICONTROL ID]</b> </p> <p>输入或映射此参与者集的ID。</p> </li> 
     <li> <p><b>[！UICONTROL标签]</b> </p> <p>输入或映射参与者集的唯一标签。 对于自定义工作流，参与集中指定的标签应将其映射到自定义工作流中的参与步骤。</p> </li> 
     <li> <p><b>[！UICONTROL名称]</b> </p> <p>输入参与者集的名称。 此名称在协议中必须是唯一的。</p> </li> 
     <li> <p><b>[！UICONTROL私人消息]</b> </p> <p>输入或映射此参与者集的消息。 集合中的所有参与者都会收到此消息。</p> </li> 
     <li> <p><b>[！UICONTROL可见页面]</b> </p> <p>如果为此协议启用了有限文档可见性，请指定对此参与者集可见的文件。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL签名类型]</td> 
   <td> <p>选择协议所需的签名类型。</p> 
    <ul> 
     <li> <p><b>[！UICONTROL电子签名]</b> </p> <p>协议必须以电子方式签署。</p> </li> 
     <li> <p>已写入<b>[！UICONTROL]</b> </p> <p>必须手动签署协议，并且必须扫描和上传已签署的协议。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL状态]</td> 
   <td> <p>选择此协议的状态。</p> 
    <ul> 
     <li> <p><b>[！UICONTROL创作]</b> </p> <p>您仍然可以编辑或向此协议添加字段。</p> </li> 
     <li> <p><b>[！UICONTROL草稿]</b> </p> <p>您可以在发送此协议之前对其进行增量构建。</p> </li> 
     <li> <p><b>[！UICONTROL正在处理]</b> </p> <p>此协议将立即发送。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL CCs]</td> 
   <td> <p>您可以将此协议发送给不需要签名的相关方，如利益相关者。 他们在签署过程开始时收到一封电子邮件，在收到最后签名时收到另一封电子邮件。 他们还会收到PDF的协议副本。 </p> <p>对于要抄送此协议的每个人员，请单击<b>[！UICONTROL添加项]</b>并填写以下字段：</p> 
    <ul> 
     <li> <p><b>[！UICONTROL电子邮件]</b> </p> <p>输入或映射要抄送协议的电子邮件地址。</p> </li> 
     <li> <p><b>[！UICONTROL标签]</b> </p> <p>输入或映射此电子邮件地址的标签，如工作流描述中所示</p> </li> 
     <li> <p><b>[！UICONTROL可见页面]</b> </p> </li> 
     <li> <p>如果为此协议启用了有限文档可见性，请指定对此参与者集可见的文件。 </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Email option]</td> 
   <td> <p>对于每种类型的电子邮件，选择该类型的电子邮件是发送给所有参与者还是不发送给任何参与者。</p> 
    <ul> 
     <li> <p><b>[！UICONTROL完成电子邮件]</b> </p> <p>在此协议完成、取消、过期或拒绝时发送电子邮件。</p> </li> 
     <li> <p><b>[！UICONTROL外部测试版电子邮件]</b> </p> <p>委派或替换此协议时发送电子邮件。</p> </li> 
     <li> <p><b>[！UICONTROL协议启动电子邮件]</b> </p> <p>在创建此协议或请求对此协议执行操作时发送电子邮件。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL外部ID]</td> 
   <td> <p>输入或映射此协议的ID。 您可以在创建协议时指定此项，并使用该项在后面的模块或查询中查找协议。</p> <p>注意：外部ID值通过API对所有参与者可见，因此不应将其用于包含敏感令牌。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL合并字段信息]</td> 
   <td> <p>对于协议中要为其放置默认值的每个字段，单击<b>[！UICONTROL添加项]</b>并输入默认值和字段名称。</p> <p>可编辑字段的值将显示给签名者。对于只读字段，提供的值在签名过程中将不可编辑。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL公证信息]</td> 
   <td> <p>填写以下字段：</p> 
    <ul> 
     <li> <p><b>[！UICONTROL约会]</b> </p> <p>输入或映射约会的建议时间和日期以将此协议公证。</p> </li> 
     <li> <p><b>[！UICONTROL注释]</b> </p> <p>输入或映射要包括的有关公证会话的任何注释。</p> </li> 
     <li> <p><b>[！UICONTROL付款]</b> </p> <p>选择由协议签名者还是发送者支付公证员。</p> </li> 
     <li> <p><b>[！UICONTROL公证类型]</b> </p> <p>选择公证人的类型</p> 
      <ul> 
       <li> <p>[！UICONTROL Provider notary]</p> <p>公证员由公证员提供商提供。</p> </li> 
       <li> <p>[！UICONTROL BYON NOTARY]</p> <p>公证人由客户提供。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Post sign选项]</td> 
   <td> <p>选择是否希望在签署协议后将签名者定向到成功页面。 如果选择<b>[！UICONTROL是]</b>，请填写以下字段：</p> 
    <ul> 
     <li> <p><b>[！UICONTROL重定向延迟]</b> </p> <p>输入或映射一个数字，该数字表示将签名者重定向到成功页面之前的秒数。 如果此值大于0，则用户将首先看到标准的[!DNL Adobe Sign]成功消息，然后在延迟后将被重定向到您的成功页面。</p> </li> 
     <li> <p><b>[！UICONTROL重定向URL]</b> </p> <p>输入或映射一个可公开访问的URL，在成功完成签名过程后，用户将发送到该URL。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Security option]</td> 
   <td> <p>输入或映射用于保护PDF文档的辅助密码。 </p> <p>重要提示： [!DNL Adobe Sign]绝不会共享此密码，因此您必须单独将它传达给任何相关方。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL保险存储信息]</td> 
   <td>如果您的帐户设置为单据电子仓库，并且每个协议都启用了选项，则可以启用此选项以电子仓库此协议。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 创建相关记录]**

此操作模块会创建链接到所选模块的记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择要与创建的记录关联的原始记录的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL协议]/[！UICONTROL库文档]/[！UICONTROL用户]/[！UICONTROL小组件ID]</td> 
   <td>输入或映射要与创建的记录关联的对象的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL协议相关字段]</td> 
   <td> <p>选择要创建的相关字段的类型</p> 
    <ul> 
     <li> <p><b>[！UICONTROL表单字段]</b> </p> <p>输入包含要创建的字段的模板的模板ID</p> </li> 
     <li> <p><b>[！UICONTROL提醒]</b> </p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p><b>[！UICONTROL收件人参与者ID]</b> </p> <p>对于每个希望接收提醒的参与者，单击[！UICONTROL添加项目]，然后输入参与者的ID。</p> </li> 
       <li> <p><b>[！UICONTROL状态]</b> </p> <p>对于新记录，状态必须为[！UICONTROL Active]。</p> </li> 
       <li> <p><b>[！UICONTROL第一个提醒延迟]</b> </p> <p>输入发送第一个提醒前的延迟小时数。 允许的最小值为1小时，最大值不能超过协议创建和协议到期时间（以小时为单位）的差异。 如果未设置此延迟，则第一次提醒将基于频率。</p> </li> 
       <li> <p><b>[！UICONTROL提醒频率]</b> </p> <p>设置您希望发送提醒的频率。 如果未提供发送频率，则提醒将发送一次。</p> </li> 
       <li> <p><b>[！UICONTROL上次发送日期]</b> </p> <p>此字段由系统设置。</p> </li> 
       <li> <p><b>[！UICONTROL下一个发送日期]</b> </p> <p>此字段必须为空或设置为[！UICONTROL ONCE]。</p> </li> 
       <li> <p><b>[！UICONTROL注释]</b> </p> <p>输入要包含在提醒中的注释。 这有助于告诉参与者需要其参与的原因。</p> </li> 
       <li> <p><b>[！UICONTROL开始提醒计数器，来自]</b> </p> <p>选择是否根据协议创建时间（协议可用时）发送提醒。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL签名者身份报告]</b> </p> <p>输入用于保护PDF文档的密码。</p> </li> 
     <li> <p><b>[！UICONTROL视图]</b> </p> <p>输入以下字段</p> 
      <ul> 
       <li> <p><b>[！UICONTROL名称]</b> </p> <p>选择要创建的视图的名称。</p> </li> 
       <li> <p><b>[！UICONTROL自动登录用户]</b> </p> <p>选择<b>[！UICONTROL是]</b>以自动将用户登录到返回的URL。</p> </li> 
       <li> <p><b>[！UICONTROL框架父项]</b> </p> <p>输入或映射以逗号分隔的父域URL列表，其中返回的URL可能为iframed。 如果留空，则[!DNL Adobe Acrobat Sign]页面在iframe中不可查看。</p> </li> 
       <li> <p><b>[！UICONTROL区域设置]</b> </p> <p>输入您要创建视图的语言。 </p> </li> 
       <li> <p><b>[！UICONTROL无Chrome标志]</b> </p> <p>选择<b>[！UICONTROL是]</b>以显示没有导航页眉或页脚的嵌入页面。</p> </li> 
       <li> <p><b>[！UICONTROL可以编辑文件]</b> </p> <p>如果希望通过添加或删除文件来编辑文件上载部分，请选择<b>[！UICONTROL是]</b>。 这不是一种访问控制机制。 默认值为[！UICONTROL是]。</p> </li> 
       <li> <p><b>[！UICONTROL库文档]</b> </p> <p>如果希望库文档链接可见，请选择<b>[！UICONTROL是]</b>。 默认值为[！UICONTROL是]。</p> </li> 
       <li> <p><b>[！UICONTROL本地文件]</b> </p> <p>如果希望显示本地文件上载按钮，请选择<b>[！UICONTROL是]</b>。 默认值为[！UICONTROL是]。</p> </li> 
       <li> <p><b>[！UICONTROL Web连接器]</b> </p> <p>如果希望链接附加来自Web源的文档，请选择<b>[！UICONTROL是]</b>。 默认值为“是”。</p> </li> 
       <li> <p><b>[！UICONTROL为预览选定项]</b> </p> <p>选择<b>[！UICONTROL是]</b>以将撰写页面设置为创作模式。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL成员共享]</b> </p> <p>对于要与其共享协议的每个成员，单击<b>[！UICONTROL添加项]</b>并输入成员的电子邮件地址和给该成员的消息。</p> </li> 
     <li> <p>[！UICONTROL委派参与者集]</p> 
      <ul> 
       <li> <p><b>[！UICONTROL参与者集ID]</b> </p> <p>输入参与者集的ID</p> </li> 
       <li> <p><b>[！UICONTROL成员信息]</b> </p> <p>对于每个要添加的成员，单击[！UICONTROL添加项]，然后输入该成员的电子邮件地址和电话信息。</p> </li> 
       <li> <p><b>[！UICONTROL私人消息]</b> </p> <p>输入消息。 参与者集的所有成员都会收到此消息。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL库视图信息]</td> 
   <td> <p>填写以下字段：</p> 
    <ul> 
     <li> <p><b>[！UICONTROL名称]</b> </p> <p>输入库模板的名称。 此名称在电子邮件和网站中使用。</p> </li> 
     <li> <p><b>[！UICONTROL自动登录用户]</b> </p> <p>选择<b>[！UICONTROL是]</b>以自动将用户登录到返回的URL。</p> </li> 
     <li> <p><b>[！UICONTROL框架父]</b> </p> <p>输入或映射以逗号分隔的父域URL列表，其中返回的URL可能为iframed。 如果留空，则[!DNL Adobe Acrobat Sign]页面在iframe中不可查看。</p> </li> 
     <li> <p><b>[！UICONTROL区域设置]</b> </p> <p>输入您要创建视图的语言。 </p> </li> 
     <li> <p><b>[！UICONTROL无Chrome标志]</b> </p> <p>选择<b>[！UICONTROL是]</b>以显示没有导航页眉或页脚的嵌入页面。</p> </li> 
     <li> <p><b>[！UICONTROL发送视图配置]</b> </p> <p>如果要配置[！UICONTROL Send]视图，请选择<b>[！UICONTROL是]</b>，然后填写以下字段。</p> 
      <ul> 
       <li> <p><b>[！UICONTROL协议名称]</b> </p> <p>在合成页面上输入或映射库文档的协议名称。</p> </li> 
       <li> <p><b>[！UICONTROL可以编辑文件]</b> </p> <p>如果希望通过添加或删除文件来编辑文件上载部分，请选择<b>[！UICONTROL是]</b>。 这不是一种访问控制机制。 默认值为[！UICONTROL是]。</p> </li> 
       <li> <p><b>[！UICONTROL本地文件]</b> </p> <p>如果希望库文档链接可见，请选择<b>[！UICONTROL是]</b>。 默认值为[！UICONTROL是]。</p> </li> 
       <li> <p><b>[！UICONTROL Web连接器]</b> </p> <p>如果希望链接附加来自Web源的文档，请选择<b>[！UICONTROL是]</b>。 默认值为[！UICONTROL是]。</p> </li> 
       <li> <p><b>已选择预览</b> </p> <p>选择<b>[！UICONTROL是]</b>以将撰写页面设置为创作模式。</p> </li> 
      </ul> <p> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL用户视图信息]</td> 
   <td> <p>填写以下字段</p> 
    <ul> 
     <li> <p><b>[！UICONTROL名称]</b> </p> <p>选择请求的用户视图的名称。</p> </li> 
     <li> <p><b>[！UICONTROL自动登录用户]</b> </p> <p>选择<b>[！UICONTROL是]</b>以自动将用户登录。 选择<b>[！UICONTROL否]</b>需要凭据。 默认值为[！UICONTROL否]。</p> </li> 
     <li> <p><b>[！UICONTROL框架父]</b> </p> <p>输入或映射以逗号分隔的父域URL列表，其中返回的URL可能为iframed。 如果留空，则[!DNL Adobe Acrobat Sign]页面在iframe中不可查看。</p> </li> 
     <li> <p><b>无Chrome标志</b> </p> <p>选择<b>[！UICONTROL是]</b>以显示没有导航页眉或页脚的嵌入页面。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL小组件相关字段]</td> 
   <td> <p>选择要创建的相关记录。</p> 
    <ul> 
     <li> <p>[！UICONTROL视图]</p> <p>填写以下字段。</p> 
      <ul> 
       <li> <p><b>[！UICONTROL名称]</b> </p> <p>选择请求的Web窗体视图的名称</p> </li> 
       <li> <p><b>[！UICONTROL自动登录用户]</b> </p> <p>选择<b>[！UICONTROL是]</b>以自动将用户登录。 选择<b>[！UICONTROL否]</b>需要凭据。 默认值为[！UICONTROL否]。</p> </li> 
       <li> <p><b>[！UICONTROL框架父]</b> </p> <p>输入或映射以逗号分隔的父域URL列表，其中返回的URL可能为iframed。 如果留空，则[!DNL Adobe Acrobat Sign]页面在iframe中不可查看。</p> </li> 
       <li> <p><b>[！UICONTROL区域设置]</b> </p> <p>输入您要创建视图的语言。 </p> </li> 
       <li> <p><b>[！UICONTROL无Chrome标志]</b> </p> <p>选择<b>[！UICONTROL是]</b>以显示没有导航页眉或页脚的嵌入页面。</p> </li> 
       <li> <p>[！UICONTROL个性化签名视图配置]</p> <p>如果要配置个性化的签名视图，请选择<b>[！UICONTROL是]</b>并填写以下字段：</p> 
        <ul> 
         <li> <p><b>[！UICONTROL电子邮件]</b> </p> <p>输入接收新创建的Web表单的人员的电子邮件地址</p> </li> 
         <li> <p><b>[！UICONTROL注释]</b> </p> <p>输入描述API调用方如何建立签名者身份的注释。 此信息显示在[!DNL Adobe Acrobat Sign]审核跟踪中。</p> </li> 
         <li> <p><b>[！UICONTROL过期]</b> </p> <p>输入此Web窗体个性化的到期日期。 </p> <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </li> 
         <li> <p><b>[！UICONTROL可重用]</b> </p> <p>如果希望目标签名者能够多次签署表单，请选择<b>[！UICONTROL是]</b>。</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL成员共享]</b> </p> <p>对于要与其共享协议的每个成员，单击<b>[！UICONTROL添加项]</b>并输入成员的电子邮件地址和给该成员的消息。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 自定义API调用]**
此模块允许您执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL URL]</p> </td> 
   <td> <p>输入相对路径 <code>https://api.[region].adobesign.com/api/rest/v6/</code></p> <p>注意：有关可用端点的列表，请参阅[!DNL Adobe Sign] API参考。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL方法]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串] </td> 
   <td> <p>输入请求查询字符串。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL上传临时文档]</td> 
   <td> <p>如果要上载临时文档，请输入要上载文档的源文件。</p> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 列出记录]**

此操作模块列出帐户有权访问的选定类型的所有记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择要检索相关记录的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL区域设置]</td> 
   <td> <p>输入用户的区域设置。 这会确定UI的语言。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL外部ID]</td> 
   <td>为要返回的协议输入或映射外部ID（在[!DNL Adobe Acrobat Sign]之外分配的ID）。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL组ID]</td> 
   <td>输入与要列出的记录关联的组的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示隐藏项（记录）]</td> 
   <td>如果要在结果中包括隐藏的记录，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Cursor] / [！UICONTROL开始索引]</td> 
   <td> <p>输入模块应返回的第一条记录的编号。 </p> <p>注意：此字段与[！UICONTROL返回记录的最大数量]字段组合使用分页。 例如，如果[！UICONTROL Maximum number of returned events]为100，而[！UICONTROL Start index]为101，则模块将返回记录101-200，或返回结果的第二页。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL返回的最大记录数]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> <p>注意：此字段与[！UICONTROL Cursor]或[！UICONTROL Start Index]字段组合使用以进行分页。 例如，如果[！UICONTROL Maximum number of returned events]为100，而[！UICONTROL Start index]为101，则模块将返回记录101-200，或返回结果的第二页。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL父域URL]</td> 
   <td> <p>输入或映射以逗号分隔的父域URL列表，其中返回的URL可能为iframed。 如果留空，则[!DNL Adobe Acrobat Sign]页面在iframe中不可查看。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 读取记录]**

此操作模块从单个记录中检索信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择要检索相关记录的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录ID]</td> 
   <td>输入或映射要检索的记录的ID。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 读取相关记录]**

阅读与单个记录相关的其他信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择要检索相关记录的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录ID]（示例：[！UICONTROL帐户ID]）</td> 
   <td>输入或映射要检索相关记录的记录ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL其他字段]</td> 
   <td>根据记录类型和相关字段在特定字段中输入信息。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 更新记录]**

此操作模块更新[!DNL Adobe Acrobat Sign]中的单个记录。

>[!IMPORTANT]
>
>* 作为最佳实践，如果您预期协议会有重大变化，我们建议您创建一个新协议，而不是更新现有协议。
>* 某些更新包含必填字段。 在配置更新时，请务必填写所有必填字段。 [!DNL Workfront Fusion]模块中的必填字段以粗体显示。
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录ID] </td> 
   <td>输入或映射要更新的记录ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择要更新的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL其他字段]</td> 
   <td> <p>根据记录类型和相关字段在特定字段中输入信息。</p> 
    <ul> 
     <li> <p><b>[！UICONTROL协议]</b> </p> <p>作为最佳实践，如果您预期协议会有重大变化，我们建议您创建一个新协议，而不是更新现有协议。</p> </li> 
     <li> <p><b>[！UICONTROL库文档]</b> </p> <p>选择要更新的字段，然后填写所选字段：</p> 
      <ul> 
       <li> <p><b>[！UICONTROL状态]</b> </p> <p>为库文档选择新状态。</p> </li> 
       <li> <p><b>[！UICONTROL名称]</b> </p> <p>输入或映射库模板的名称</p> </li> 
       <li> <p><b>[！UICONTROL共享模式]</b> </p> <p>指定应该有权访问库文档的人员。</p> </li> 
       <li> <p><b>[！UICONTROL库模板类型]</b> </p> <p>对于每个要使用的库模板类型，单击<b>[！UICONTROL添加项]</b>并选择模板类型。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL用户]</b> </p> <p>选择要更新的字段，然后填写所选字段：</p> 
      <ul> 
       <li> <p><b>[！UICONTROL名字]</b> </p> <p>输入用户的名字。</p> </li> 
       <li> <p><b>[！UICONTROL姓氏]</b> </p> <p>输入用户的姓氏</p> </li> 
       <li> <p><b>[！UICONTROL公司]</b> </p> <p>输入用户的公司名称。</p> </li> 
       <li> <p><b>[！UICONTROL Phone]</b> </p> <p>输入用户的电话号码</p> </li> 
       <li> <p><b>[！UICONTROL主组ID]</b> </p> <p>输入将新用户添加到其中的组。 如果未输入任何内容，则用户将被添加到帐户的默认组中。</p> </li> 
       <li> <p><b>[！UICONTROL作业标题]</b> </p> <p>输入用户的工作标题。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL Web窗体] （[！UICONTROL小组件]）</b> </p> <p>根据记录类型和相关字段在特定字段中输入信息。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 更新相关记录]**

此操作模块更新与特定对象相关的记录。

>[!IMPORTANT]
>
>* 作为最佳实践，如果您预期协议会有重大变化，我们建议您创建一个新协议，而不是更新现有协议。
>* 某些更新包含必填字段。 在配置更新时，请务必填写所有必填字段。 [!DNL Workfront Fusion]模块中的必填字段以粗体显示。
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录类型]</td> 
   <td>选择与相关字段关联的记录的记录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL协议]/[！UICONTROL库文档]/[！UICONTROL用户]/[！UICONTROL小组件ID]</td> 
   <td>输入或映射要与创建的记录关联的对象的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL其他字段]</td> 
   <td> <p>根据记录类型和相关字段在特定字段中输入信息。</p> 
    <ul> 
     <li> <p><b>[！UICONTROL协议]</b> </p> <p>作为最佳实践，如果您预期协议会有重大变化，我们建议您创建一个新协议，而不是更新现有协议。</p> </li> 
     <li> <p><b>[！UICONTROL库文档]</b> </p> <p>选择要更新的字段，然后填写所选字段：</p> 
      <ul> 
       <li> <p><b>[！UICONTROL状态]</b> </p> <p>为库文档选择新状态。</p> </li> 
       <li> <p><b>[！UICONTROL注释]</b> </p> <p>输入或映射注释的文本。</p> </li> 
       <li> <p><b>[！UICONTROL可见性]</b> </p> <p>选择是显示还是显示库文档。</p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL用户]</b> </p> <p>选择要更新的字段，然后填写所选字段：</p> 
      <ul> 
       <li> <p><b>[！UICONTROL组信息列表]</b> </p> <p>填写以下字段</p> 
        <ul> 
         <li> <p><b>[！UICONTROL状态]</b> </p> <p>为用户选择新状态。</p> </li> 
         <li> <p><b>[！UICONTROL ID]</b> </p> <p>输入组的唯一ID</p> </li> 
         <li> <p><b>[！UICONTROL是组管理员]</b> </p> <p>选择<b>[！UICONTROL是]</b>以将此用户设为组管理员。</p> </li> 
         <li> <p><b>是主要组</b> </p> <p>选择<b>[！UICONTROL是]</b>将此组更新到用户的主组。</p> </li> 
         <li> <p><b>[！UICONTROL创建日期]</b> </p> <p>输入创建组的日期。</p> <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override="">在[！UICONTROL Adobe Workfront Fusion]中键入强制转换</a>。</p> </li> 
         <li> <p><b>[！UICONTROL名称]</b> </p> <p>输入或映射组的名称。</p> </li> 
         <li> <p><b>[！UICONTROL库文档创建可见]</b> </p> <p>这些设置确定用户是否可以创建库文档</p> 
          <ul> 
           <li> <p>[！UICONTROL值]</p> <p>允许</p> </li> 
           <li> <p>[！UICONTROL已继承]</p> <p>从组或帐户继承组设置</p> </li> 
          </ul> </li> 
         <li> <p><b>[！UICONTROL发送限制到工作流]</b> </p> <p>这些设置确定用户是否只能使用工作流创建协议。</p> 
          <ul> 
           <li> <p>[！UICONTROL值]</p> <p>允许</p> </li> 
           <li> <p>[！UICONTROL已继承]</p> <p>从组或帐户继承组设置</p> </li> 
          </ul> </li> 
         <li> <p><b>[！UICONTROL用户可以发送]</b> </p> 
          <ul> 
           <li> <p>[！UICONTROL值]</p> <p>允许</p> </li> 
           <li> <p>[！UICONTROL已继承]</p> <p>从组或帐户继承组设置</p> </li> 
          </ul> </li> 
        </ul> </li> 
      </ul> 
      <ul> 
       <li> <p><b>[！UICONTROL状态]</b> </p> <p>选择用户的新状态，然后输入有关要激活或取消激活用户的原因的注释。</p> </li> 
       <li> <p><b>[！UICONTROL区域设置]</b> </p> <p>输入用户的区域设置。 这会确定UI的语言。 </p> </li> 
      </ul> </li> 
     <li> <p><b>[！UICONTROL Web窗体] （[！UICONTROL小组件]）</b> </p> <p>根据记录类型和相关字段在特定字段中输入信息。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 上载文档]**

上载临时文档。 临时文档在上传后7天内都可用。

>[!NOTE]
>
>我们建议上传文档以作为临时文档签名，然后在创建协议模块中将其映射到要发送的文件字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL记录ID]</td> 
   <td>输入或映射要更新的记录ID</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL MIME类型]</td> 
   <td>输入原始文件的mime类型。 多用途Internet邮件扩展(MIME)类型是允许软件识别在Internet上共享的不同类型数据的标签。 Web服务器和浏览器使用MIME类型来确定应该对文件执行的操作。 例如，在浏览器中处理MIME类型为<code>text/html</code>的文件的方式与MIME类型为<code>image/jpeg</code>的文件的方式不同。</td> 
  </tr> 
 </tbody> 
</table>

**示例：**&#x200B;在此工作流中，要签名的文档(以前从Workfront下载)作为临时文档上传。

(/help/workfront-fusion/references/apps-and-modules/assets/sign-example-1-350x308.png)

[!UICONTROL 上载文档]模块为文档提供了[!DNL Adobe Acrobat Sign] ID，可在以后的模块中引用。 创建协议后，上传文档的ID包含在[!UICONTROL 要发送的文件]字段中。

![签名示例](/help/workfront-fusion/references/apps-and-modules/assets/sign-example-2-350x356.png)

+++

### 搜索

+++ **[!UICONTROL 搜索协议]**

此搜索模块根据您提供的条件搜索协议。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Acrobat Sign]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文本筛选器]</td> 
   <td> <p>在协议元数据中搜索文本。 </p> 
    <ul> 
     <li> <p><b>[！UICONTROL查找文本]</b> </p> <p>输入要在协议元数据中查找的文本。 每个单词都被视为单独的文本项。 </p> </li> 
     <li> <p><b>[！UICONTROL在]</b>中查找文本 </p> <p>选择要在其中查找文本的元数据字段。 如果未选择任何内容，则模块将搜索所有元数据。</p> </li> 
    </ul> <p>模块会返回包含任何选定字段中所输入文本的任何协议。 示例：输入“Spring campaign”并选择“Title”和“Note”选项会返回在“Title”或“Note”中带有“Spring”或“Campaign”字样的任何协议。</p> <p>有关在[!DNL Adobe Acrobat Sign]中搜索字段的更多信息，请参阅<a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">[!DNL Adobe Sign]搜索中的“文本搜索的工作方式” — 其工作方式</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL创建日期]</td> 
   <td>选择日期。 模块仅返回创建日期与此条件匹配的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL过期日期]</td> 
   <td>选择日期。 模块仅返回过期日期与此条件匹配的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[！UICONTROL修改日期]</p> </td> 
   <td>选择日期。 模块仅返回修改日期与此条件匹配的记录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL外部ID]</td> 
   <td> <p> 外部ID是发件人分配给协议的ID，可以是任何形式，但通常采用“&lt;groupID&gt;：&lt;ID&gt;”的形式。</p> <p>对于要添加的每个外部ID，单击<b>[！UICONTROL添加]</b>并输入或映射外部ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL组ID]</td> 
   <td> <p>组ID是创建组时分配的标识符。</p> <p>对于要添加的每个外部ID，单击<b>[！UICONTROL添加]</b>并输入或映射外部ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资产ID]</td> 
   <td> <p>这是分配给特定协议的ID。 </p> <p>对于要添加的每个外部ID，单击<b>[！UICONTROL添加]</b>并输入或映射外部ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL父ID]</td> 
   <td> <p>这是分配给协议父对象的ID。 </p> <p>对于要添加的每个外部ID，单击<b>[！UICONTROL添加]</b>并输入或映射外部ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL参与者电子邮件]</td> 
   <td> <p>参与者的电子邮件地址。 </p> <p>对于要添加的每个外部ID，单击<b>[！UICONTROL添加]</b>并输入或映射外部ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL角色]</td> 
   <td>选择要将返回的结果包括在内的角色。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL排序方式]</td> 
   <td>如果要让模块对结果进行排序，请选择要作为结果排序依据的字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL排序顺序]r</td> 
   <td>如果要让模块对结果进行排序，请选择是要升序排序还是降序排序。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL状态]</td> 
   <td>选择要将返回的结果包括在内的状态。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL类型]</td> 
   <td>选择要将返回的结果包括在内的协议类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Subtypes]</td> 
   <td>选择要将返回的结果包括在内的协议子类型。 只有库模板协议具有子类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL用户ID]</td> 
   <td> <p>与共享协议的用户的用户ID。</p> <p>对于每个要添加的用户ID，单击<b>[！UICONTROL添加]</b>并输入或映射用户ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL可见性]</td> 
   <td>选择您希望返回的结果包含的可见性级别。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL开始索引]</td> 
   <td> <p>输入要返回的第一个结果的位置。 将此参数与[！UICONTROL返回的最大结果数]结合使用，以对结果进行分页</p> <p>示例：如果一次返回100个结果，请输入100以返回结果100-200。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL返回结果的最大数目]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++
