---
title: Adobe Workfront模块
description: 您可以使用Adobe Workfront Fusion Adobe Workfront连接器在Workfront中自动执行流程。 如果您拥有Workfront Fusion for Work Automation and Integration许可证，则还可以使用它连接到第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 93c27cf6-38b0-466c-87bb-926c4817eae7
source-git-commit: d2c873ffec406ae343fbcc72246688dec0bd1eab
workflow-type: tm+mt
source-wordcount: '7373'
ht-degree: 2%

---

# Adobe Workfront模块

>[!IMPORTANT]
>
>本文包含有关2025年10月22日发布的Workfront连接器新版本的说明。 此新连接器反映了对Workfront API所做的更改。
>
>新连接器将标记为“Workfront”，之前可用的连接器将标记为“Workfront（旧版）”。
>
>我们建议：
>
>* 在创建或更新场景时使用新连接器。
>* 将现有模块升级到新连接器。
>
>有关升级现有模块的说明，请参阅将模块升级到新版本一文中的[将Workfront模块升级到新版本](/help/workfront-fusion/manage-scenarios/update-module-to-new-version.md)。
>
>有关为何有时需要新连接器的信息，请参阅[Fusion中的API概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/api-overview.md)。

您可以使用Adobe Workfront Fusion Adobe Workfront连接器在Workfront中自动执行流程。 您还可以将Workfront连接到其他应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。 有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。


>[!NOTE]
>
>* 如果您的组织使用旧版许可包（基于连接器），则必须具有Workfront Fusion for Work Automation and Integration许可证才能连接到第三方应用程序和服务。 Workfront连接器不会计入您的组织可用的活动应用程序数量。 所有方案，即使它们仅使用Workfront应用程序，也会计入贵组织的方案总数。

+++

## 将Workfront连接到Workfront Fusion

Workfront连接器使用OAuth 2.0连接到Workfront。

您可以直接在Workfront Fusion模块内创建与Workfront帐户的连接。

* [使用客户端ID和客户端密钥连接到Workfront](#connect-to-workfront-using-client-id-and-client-secret)
* [使用服务器到服务器连接连接到Workfront](#connect-to-workfront-using-a-server-to-server-connection)

### 使用客户端ID和客户端密钥连接到Workfront

1. 在任意Adobe Workfront模块中，单击连接字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接类型]</td>
        <td>
          <p>选择<b>Adobe Workfront身份验证连接</b>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端ID]</td>
        <td>输入您的Workfront客户端ID。 您可以在Workfront中“设置”区域的“OAuth2应用程序”区域找到此代码。 打开要连接的特定应用程序以查看客户端ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的Workfront客户端密码。 您可以在Workfront中“设置”区域的“OAuth2应用程序”区域找到此代码。 如果您的Workfront中的OAuth2应用程序没有客户端密钥，则可以生成另一个密钥。 有关说明，请参阅Workfront文档。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 身份验证URL]</td>
        <td>此值可保留为默认值，也可以输入Workfront实例的URL，后跟<code>/integrations/oauth2</code>。 <p>示例： <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 主机前缀]</td>
        <td>在大多数情况下，此值应为<code>origin</code>。
      </tr>
    </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

   如果您未登录Workfront，则会引导您进入登录屏幕。 登录后，您可以允许连接。

>[!NOTE]
>
>* 到Workfront API的OAuth 2.0连接不再依赖API密钥。
>* 要创建与Workfront沙盒环境的连接，您必须在该环境中创建一个OAuth2应用程序，然后在您的连接中使用由该应用程序生成的客户端ID和客户端密钥。

### 使用服务器到服务器连接连接到Workfront

1. 在任意Adobe Workfront模块中，单击连接字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接类型]</td>
        <td>
          <p>选择<b>Adobe Workfront服务器到服务器连接</b>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 实例名称]</td>
        <td>
          <p>输入实例的名称，也称为域。</p><p>示例：如果您的URL是<code>https://example.my.workfront.com</code>，请输入<code>example</code>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 实例通道]</td>
        <td>
          <p>输入此连接将连接的环境类型。</p><p>示例：如果您的URL是<code>https://example.my.workfront.com</code>，请输入<code>my</code>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端ID]</td>
        <td>输入您的Workfront客户端ID。 您可以在Workfront中“设置”区域的“OAuth2应用程序”区域找到此代码。 打开要连接的特定应用程序以查看客户端ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的Workfront客户端密码。 您可以在Workfront中“设置”区域的“OAuth2应用程序”区域找到此代码。 如果您的Workfront中的OAuth2应用程序没有客户端密钥，则可以生成另一个密钥。 有关说明，请参阅Workfront文档。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 范围]</td>
        <td>输入此连接的任何适用范围。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 主机前缀]</td>
        <td>在大多数情况下，此值应为<code>origin</code>。
      </tr>
    </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

   如果您未登录Workfront，则会引导您进入登录屏幕。 登录后，您可以允许连接。

>[!NOTE]
>
>* 到Workfront API的OAuth 2.0连接不再依赖API密钥。
>* 要创建与Workfront沙盒环境的连接，您必须在该环境中创建一个OAuth2应用程序，然后在您的连接中使用由该应用程序生成的客户端ID和客户端密钥。

## Workfront模块及其字段

配置Workfront模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Workfront字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。


![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>* 如果您在Workfront模块中未看到最新字段，这可能是因为缓存问题。 等待一小时，然后重试。
>* 来自Adobe Workfront的HTTP 429状态代码不应导致停用，而是会在场景中触发短暂的执行暂停。

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

<!--
* [Watch Events](#watch-events) 
* [Watch Record](#watch-record) 
* [Watch Field](#watch-field)
-->

+++ **[!UICONTROL 观看活动]**

在Workfront中添加、更新或删除特定类型的对象时，此触发器模块会实时执行场景

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

1. 单击&#x200B;**[!UICONTROL Webhook]**&#x200B;框右侧的&#x200B;**添加**。

1. 在显示的&#x200B;**[!UICONTROL 添加挂接]**&#x200B;框中配置webhook。

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Webhook名称]</td> 
      <td>输入webhook的名称</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Connection]</td> 
      <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 记录类型]</td> 
      <td>选择要模块观看的Workfront记录类型。</td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 状态]</td> 
      <td>选择您要观察旧状态还是新状态。<ul><li><p><b>[!UICONTROL 新状态]</b></p><p>当记录将<b>更改为</b>给定值时触发方案。</p><p>例如，如果状态设置为[!UICONTROL New State]，而过滤器设置为[!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress]，则webhook会在[!UICONTROL Status]更改为[!UICONTROL In Progress]时触发场景，而不管状态之前是什么。 </p></li><li><p><b>[!UICONTROL 旧状态]</b></p><p>当记录从<b>更改</b>给定值时触发方案。</p><p>例如，如果状态设置为[!UICONTROL Old State]，而过滤器设置为[!UICONTROL Status] [!UICONTROL Equals] [!UICONTROL In Progress]，则当[!UICONTROL Status]当前为[!UICONTROL In Progress]的状态更改为其他状态时，webhook会触发一个场景。 </p></li></ul></td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL 事件过滤器]</p> </td> 
      <td> <p>您可以设置过滤器，以仅监视符合您选择标准的记录。</p> <p>对于每个筛选器，输入希望筛选器计算的字段、运算符以及希望筛选器允许的值。 通过添加AND规则，您可以使用多个过滤器。</p> <p><b>注意</b>：您无法编辑现有Workfront Webhook中的筛选器。 要为Workfront活动订阅设置其他筛选器，请删除当前webhook并创建一个新筛选器。</p> <p>有关事件过滤器的详细信息，请参阅本文中的Workfront &gt; [!UICONTROL 监视事件]模块中的<a href="#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">事件订阅过滤器</a>。</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td>排除由此连接产生的事件</td> 
      <td>启用此选项可排除使用此触发器模块使用的同一连接器创建或更新的事件。 这可以防止场景触发自身，导致其在无休止循环中重复的情况。<p><b>注意</b>： Assignment记录类型不包括此选项。</p></td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL 记录源]</td> 
      <td>
       <p>选择您希望方案仅观看[!UICONTROL 新记录]、[!UICONTROL 仅更新记录]、[!UICONTROL 新记录和更新记录]还是[!DNL Deleted Records Only]。</p>
       <p><b>注意</b>：如果您选择[!UICONTROL 新建和更新的记录]，webhook创建将创建2个事件订阅（针对同一webhook地址）。</p>
       </td> 
     </tr> 
    </tbody> 
   </table>



   <!--Markdown 0032 placeholder-->

创建webhook后，您可以查看事件所发往的端点地址。

有关详细信息，请参阅Workfront文档事件订阅API一文中的[事件负载示例](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-api#examples-of-event-payloads)部分。

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

+++

+++ **[!UICONTROL 监视字段]**

当您指定的字段更新时，此触发器模块会执行场景。 该模块会返回指定字段的旧值和新值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择要模块观看的Workfront记录类型。</p> <p>例如，如果希望每次更新任务中的记录字段时都开始执行方案，请选择[!UICONTROL Task]。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 字段]</td> 
   <td>选择您希望模块关注更新的字段。 这些字段反映了Workfront管理员为跟踪而设置的字段。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 输出]</td> 
   <td>选择要包含在此模块的输出捆绑包中的对象字段。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 限制]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

+++

+++ **[!UICONTROL 观看记录]**

此触发器模块执行特定类型的对象添加、更新或同时添加和更新的方案。 该模块返回与一个或多个记录关联的所有标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

在输出中，模块指示每个记录是新的还是更新的。

自上次运行场景以来添加和更新的记录将作为新记录返回。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 筛选器]</td> 
   <td> <p>选择您希望方案仅观看[!UICONTROL 新记录]、[!UICONTROL 仅更新记录]还是[!UICONTROL 新记录和更新记录]。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择要模块观看的Workfront记录类型。</p> <p>例如，如果您要在每次创建新项目时启动方案，请选择[!UICONTROL 项目]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 参考]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的引用字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的集合字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 可选过滤器]</td> 
   <td> <p>（高级）键入API代码字符串以定义任何其他将细化标准的参数或代码。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

+++


### 操作

<!--
* [Convert object](#convert-object) 
* [Create a record (attaching custom forms)](#create-a-record-attaching-custom-forms) 
* [Create a record](#create-a-record) 
* [Custom API Call](#custom-api-call) 
* [Delete Record](#delete-record) 
* [Download Document](#download-document) 
* [Misc Action](#misc-action) 
* [Read a Record](#read-a-record) 
* [Update Record](#update-record) 
* [Upload Document](#upload-document)
-->

+++ **[!UICONTROL 转换对象]**

此操作模块进行以下转换之一：

* 将问题转化为项目
* 将问题转化为任务
* 将任务转换为项目

>[!NOTE]
>
>自2024年7月起，转化对象时可包含自定义表单。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 对象类型]</td> 
   <td> <p>选择要转换的对象类型。 这是转换之前对象的类型。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 转换为]</td> 
   <td>选择要将其转换为的对象。 这是转换后对象的类型。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL &lt;对象&gt; ID]</td> 
   <td> <p>输入对象的ID。 </p> <p>注意：输入对象的ID时，可以开始键入对象的名称，然后从列表中选择该对象。 然后，模块在字段中输入相应的ID。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 模板ID]</td> 
   <td> <p>如果要转换为项目，请选择要用于项目的模板ID。</p> <p>注意：输入对象的ID时，可以开始键入对象的名称，然后从列表中选择该对象。 然后，模块在字段中输入相应的ID。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 自定义表单]</td> 
   <td>选择要添加到新转换的对象中的任何自定义表单，然后输入自定义表单字段的值。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Options]</td> 
   <td> <p>在转换对象时启用所需的任意选项。 选项是否可用取决于您要转换到的对象或从哪个对象转换。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 复制本机字段]</td> 
   <td> <p>启用此选项可将任何本地字段从原始对象复制到新对象。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 复制自定义表单]</td> 
   <td> <p>启用此选项可将任何本地字段从原始对象复制到新对象。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 创建记录]** 

此操作模块可在Workfront中创建对象，如项目、任务或问题，并允许您向新对象添加自定义表单。 利用模块，可选择模块中可用的对象字段。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

确保提供最小数量的输入字段。 例如，如果您要创建问题，则需要在“项目ID”字段中提供有效的父项目ID，以指示问题应存在于Workfront中的位置。 您可以使用映射面板从场景中的其他模块映射此信息，也可以通过键入名称，然后从列表中选择该名称来手动输入该信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择您希望模块创建的Workfront记录类型。</p> <p>例如，如果要创建项目，请从下拉列表中选择[!UICONTROL 项目] 。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 选择要映射的字段]</td> 
   <td> <p>选择可用于数据输入的字段。 这样，您就无需滚动浏览不需要的字段即可使用这些字段。 然后，您可以在这些字段中输入或映射数据。</p> <p>对于自定义表单中的字段，请使用<b>[!UICONTROL 附加自定义表单]</b>字段。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 附加自定义表单]</td> 
   <td>选择要添加到新对象的任何自定义表单，选择要为其输入值的字段，然后输入或映射这些字段的值。</td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

>[!NOTE]
>
>* 输入对象的ID时，可以开始键入对象的名称，然后从列表中选择该对象。 然后，模块在字段中输入相应的ID。
>* 输入自定义字段或[!UICONTROL Note]对象的文本（注释或回复）时，您可以使用[!UICONTROL 注释文本]字段中的HTML标记创建富文本，如粗体或斜体文本。
>



>[!NOTE]
>
>创建的用户处于停用和待审批状态。 如果您的组织已迁移到Adobe Admin Console，并且在几分钟内未删除未决批准徽章，则可以批准该用户。
>
>* **解析单个用户**
>
>      您可以解析“用户”列表中的单个用户。
>
>      1. 在“用户”列表中选择一个或多个用户。
>      1. 单击列表标题中的三个圆点菜单。
>      1. 选择&#x200B;**批准**。
>      1. 几分钟后，刷新页面。
>
>* **解析在大型批次中添加的用户**
>
>   要解决批量添加的用户，可以直接将批量用户添加到Adobe Admin Console。
>
>   有关说明，请参阅[管理多个用户 | 在Adobe文档中批量CSV上传](https://helpx.adobe.com/cn/enterprise/using/bulk-upload-users.html)。

+++

<!--

+++ **[!UICONTROL Create Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Create a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module creates an object, such as a project, task, or issue in Workfront. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  record and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

Make sure you provide the minimum number of input fields. For example, if you want to create an issue, you need to provide a valid parent project ID in the Project ID field to indicate where the issue should live in Workfront. You can use the mapping panel to map this information from another module in your scenario, or you can enter it manually by typing in the name and then selecting it from the list.

This module does not attach custom forms when creating the object. To attach custom forms while creating an object, use the [!UICONTROL Create a record (attaching custom forms)] module.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to create.</p> <p>For example, if you want to create a Project, select [!UICONTROL Project] from the dropdown list.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL 自定义API调用]**

通过此操作模块，您可以对Workfront API进行经过身份验证的自定义调用。 这样，您可以创建其他Workfront模块无法实现的数据流自动化。

模块返回以下信息：

* **[!UICONTROL 状态代码]** （数字）：这表示HTTP请求是成功还是失败。 这些是标准代码，您可以在互联网上查找。
* **[!UICONTROL 标头]** （对象）：与输出正文无关的响应/状态代码的更详细的上下文。 并非响应标头中显示的所有标头都是响应标头，因此某些标头可能对您没什么用。

  响应标头取决于您在配置模块时选择的HTTP请求。

* **[!UICONTROL Body]**（对象）：根据您在配置模块时选择的HTTP请求，您可能会收到一些返回的数据。 该数据(例如来自GET请求的数据)包含在此对象中。

您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>输入相对于<code> https://&lt;WORKFRONT_DOMAIN&gt;/attask/api/&lt;API_VERSION&gt;/</code>的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API版本]</td> 
   <td>选择您希望模块使用的Workfront API的版本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅Adobe Workfront Fusion中的<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 这会确定请求的内容类型。</p> <p>例如，<code> {"Content-type":"application/json"}</code></p> <p>注意：如果您收到错误并且难以确定其来源，请考虑根据Workfront文档修改标头。 如果自定义API调用返回422 HTTP请求错误，请尝试使用<code>"Content-Type":"text/plain"</code>标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> <p>提示：我们建议您通过JSON正文而不是查询参数发送信息。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

+++

+++ **[!UICONTROL 删除记录]**

此操作模块可删除对象，如Workfront中的项目、任务或问题。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 强制删除]</td> 
   <td>启用此选项以确保删除记录，即使Workfront UI会请求确认删除。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 异步删除]</td> 
   <td>启用此选项以允许异步删除模块。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>ID</td> 
   <td> <p>输入您希望模块删除的记录的唯一Workfront ID。</p> <p>要获取ID，请在浏览器中打开Workfront对象，并复制URL末尾处“ID=”后的文本。 例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td>选择要让模块删除的Workfront记录类型。</td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

>[!NOTE]
>
>我们建议采用以下方案配置，以避免因异步操作而无法删除记录。
>
>1. 同步删除记录。
>1. 将错误处理添加到删除记录模块以忽略由40秒超时导致的错误。


+++

+++ **[!UICONTROL 下载文档]**

此操作模块可从Workfront下载文档。

您指定记录的ID。

该模块返回文档的内容、文件名、文件扩展名和文件大小。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文档ID]</td> 
   <td> <p>映射或手动输入您希望模块下载的文档的唯一Workfront ID。</p> <p>要获取ID，请在浏览器中打开Workfront对象，并复制URL末尾处“ID=”后的文本。 例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

+++

### **获取预签名文件URL**

此操作模块获取预签名的文件URL，以后可由其他API使用。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文档ID]</td> 
   <td> <p>映射或手动输入您要为其获取预签名URL的文档的唯一Workfront ID。</p> <p>要获取ID，请在浏览器中打开Workfront对象，并复制URL末尾处“ID=”后的文本。 例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL URL过期时间]</td> 
   <td> <p>输入或映射此URL过期前存在的分钟数。 默认值为1分钟。</p><p>要更改此值，必须由Workfront Fusion团队启用此参数。 如果未启用，则无论您输入的数字如何，该值都将保持1分钟。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++ **[!UICONTROL 其他操作]**

通过此操作模块，您可以对API执行操作。

>[!NOTE]
>
>自2024年7月起，`convertToProject`操作包括字段`copyCategories`。 当设置为`TRUE`时，所有自定义表单都将包含在问题所转换到的项目中。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择您希望模块与之交互的Workfront记录类型。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 操作]</td> 
   <td> <p>选择要模块执行的操作。</p> <p>根据您选择的[!UICONTROL 记录类型]和[!UICONTROL 操作]，您可能需要填写其他字段。 这两个设置的某些组合可能只需要记录ID，而其他设置（如<strong>[!UICONTROL 记录类型的Project]</strong>和<strong>[!UICONTROL 操作]</strong>的[!UICONTROL 附加模板]）需要其他信息（如对象ID和模板ID）。</p><p>有关某些操作可用的选项，请参阅本文中的<a href="#misc-action-options" class="MCXref xref">其他操作选项</a>。</p> <p>有关各个字段的详细信息，请参阅<a href="http://developer.workfront.com/">Workfront开发人员文档</a>。 <p><strong>注意</strong>：开发人员文档网站仅包含通过API版本14传递的信息，但仍包含可供API调用使用的有用信息。 </p> 
    <ol> 
     <li value="1"> <p>从Workfront开发人员文档页面的左侧导航中选择记录类型。 以下类型有自己的页面：</p> 
      <ul> 
       <li> <p>[!UICONTROL 项目]</p> </li> 
       <li> <p>[!UICONTROL 任务]</p> </li> 
       <li> <p>[!UICONTROL Issues]</p> </li> 
       <li> <p>[!UICONTROL 用户]</p> </li> 
       <li> <p>[!UICONTROL 文档]</p> </li> 
      </ul> <p>对于所有其他记录类型，请选择<b>[!UICONTROL Other objects and endpoints]</b>，然后在按字母顺序排序的页面上查找该记录类型。</p> </li> 
     <li value="2"> <p>在相应记录类型的页面上，搜索操作（Ctrl-F或Cmd-F）。</p> </li> 
     <li value="3"> <p>查看所选操作下可用字段的描述。</p> </li> 
    </ol> <p>注释：  <p>通过Workfront [!UICONTROL 杂项操作]模块创建验证时，最佳实践为创建不包含任何高级选项的验证，然后使用[!DNL Workfront Proof] SOAP API更新验证。</p><p>有关使用Workfront API（此模块使用它）创建验证的更多信息，请参阅<a href="https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/tips-troubleshooting-apis/api-create-proof-options-json" class="MCXref xref">通过Adobe Workfront API创建验证时添加高级验证选项</a></p> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td>输入或映射您希望模块与之交互的记录的唯一Workfront ID。<p>要获取ID，请在浏览器中打开Workfront对象，并复制URL末尾处“ID=”后的文本。 例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p></td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

#### 其他操作选项

##### 任务

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>操作</th> 
   <th>选项</th> 
  </tr> 
  <tr> 
   <td>复制</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignations</li>
   <li>clearConstraints</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>清除财务数据</p></li>
   <li>clearpermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>清除提醒通知</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>移动</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignations</li>
   <li>clearDocuments</li>
   <li>clearConstraints</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>清除财务数据</p></li>
   <li>clearpermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>清除提醒通知</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

##### 问题

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>操作</th> 
   <th>选项</th> 
  </tr> 
  <tr> 
   <td>复制</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignations</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearpermissions</li>
   <li>clearProgress</li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>转换为任务</td> 
   <td>
   <ul>
   <li>preserveIssue<p>保留原来的问题，并将其解决方案与此任务绑定</p></li>
   <li>preservePrimaryContact<p>允许问题的主要联系人访问此任务</p></li>
   <li>preserveCompletionDate<p>保留问题的计划完成日期</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>转换至项目</td> 
   <td>
   <ul>
   <li>preserveIssue<p>保留原来的问题，并将其解决方案与此任务绑定</p></li>
   <li>preservePrimaryContact<p>允许问题的主要联系人访问此任务</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



##### 项目

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <th>操作</th> 
   <th>选项</th> 
  </tr> 
  <tr> 
   <td>复制</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignations</li>
   <li>clearCustomData</li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>清除财务数据</p></li>
   <li>clearpermissions</li>
   <li>clearPredecessors</li>
   <li>clearProgress</li>
   <li>clearTimedNotifications<p>清除提醒通知</p></li>
   </ul>
   </td> 
  </tr> 
  <tr> 
   <td>附加模板/另存为模板</td> 
   <td>
   <ul>
   <li>clearApprovers</li>
   <li>clearAssignations</li>
   <li>clearBillingRates</li>
   <li>clearConstraints</li>
   <li>clearDeliverable<p>清除目标</p></li>
   <li>clearDocuments</li>
   <li>clearExpenses</li>
   <li>clearFinancials<p>清除财务数据</p></li>
   <li>clearHourTypes</li>
   <li>Clearisssetup<p>清除队列属性和问题设置</p></li>
   <li>clearPredecessors</li>
   <li>clearrisks</li>
   <li>clearSharingOptions</li>
   <li>clearTimedNotifications<p>清除提醒通知</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



+++

+++ **[!UICONTROL 读取记录]**

此操作模块从单个记录中检索数据。

您指定记录的ID。 您还可以指定希望模块读取哪些相关记录。

例如，如果模块正在读取的记录是项目，则可以指定希望读取项目的任务。

模块会从您指定的输出字段中返回一个数据数组。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 记录类型]</td>

<td>选择要让模块读取的Workfront对象类型。</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 输出]</td>

<td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 输出自定义表单]</td>
     <td> <p>选择要包含在此模块输出捆绑包中的自定义表单，然后从要包含在输出中的自定义表单中选择特定字段。</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 引用]</td>
   <td>选择要包含在输出中的任何引用字段。</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL 收藏集]</td>
   <td>选择要包含在输出中的任何引用字段。</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>输入您希望模块读取的记录的唯一Workfront ID。</p> <p>要获取ID，请在浏览器中打开Workfront对象，并复制URL末尾处“ID=”后的文本。 例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

+++

<!--

+++ **[!UICONTROL Read a Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Read a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module retrieves data from a single record.

You specify the ID of the record. You can also specify which related records you want the module to read.

For example, if the record that the module is reading is a project, you can specify that you want the project's tasks read.

The module returns an array of data from the output fields you specified.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td>[!UICONTROL Connection]</td>
    <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Record Type]</td>
  
   <td>Choose the Workfront object type that you want the module to read.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Outputs]</td>
  
   <td> <p>Select the information you want included in the output bundle for this module.</p> </td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL References]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL Collections]</td>
   <td>Select any reference fields that you want to include in the output.</td> 
  </tr> 
  <tr> 
    <td>[!UICONTROL ID]</td>
   <td> <p>Enter the unique Workfront ID of the record that you want the module to read.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++

-->

+++ **更新事件有效负载版本**

Workfront最近发布了其事件订阅服务的新版本。 新版本不是对Workfront API的更改，而是对事件订阅功能的更改。 此操作模块会更新用于此方案的事件有效负载版本。

有关新的事件订阅版本的详细信息，请参阅Workfront文档中的[事件订阅版本控制](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning)

有关在事件订阅升级期间保留Workfront Fusion方案的资源（包括网络研讨会录像），请参阅[在事件订阅V2升级期间保留Fusion方案](https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182)。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 版本]</td> 
   <td> 选择要用于此有效负载的事件订阅的版本。 </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **更新记录**


此操作模块可更新对象，如项目、任务或问题。 利用模块，可选择模块中可用的对象字段。

您指定记录的ID。

模块会返回对象的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>输入您希望模块更新的记录的唯一Workfront ID。</p> <p>要获取ID，请在浏览器中打开Workfront对象，并复制URL末尾处“ID=”后的文本。 例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>选择要更新模块的Workfront记录类型。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>选择可用于数据输入的字段。 这样，您就无需滚动浏览不需要的字段即可使用这些字段。 然后，您可以在这些字段中输入或映射数据。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Attach Custom Form]</td> 
   <td>选择您想在新记录上提供字段值的自定义表单。 选择表单后，为该表单上的字段输入数据。<p> 要为要在此模块中附加的表单提供字段值，请在要映射的字段部分中包含自定义表单ID 。</td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

>[!NOTE]
>
> 输入自定义字段或[!UICONTROL Note]对象的文本（注释或回复）时，您可以使用[!UICONTROL 注释文本]字段中的HTML标记创建富文本，如粗体或斜体文本。


+++

<!--

+++ **[!UICONTROL Update Record (Legacy)]**

>[!IMPORTANT]
>
>This module has been replaced with the Update a record module. We recommend using that module in new scenarios.
>Existing scenarios that use this module will continue to function as expected. This module will be removed from the module selector in May 2025.

This action module updates an object, such as a project, task, or issue. The module allows you to select which of the object's fields are available in the module.

You specify the ID of the record.

The module returns the ID of the  object and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL ID]</td> 
   <td> <p>Enter the unique Workfront ID of the record that you want the module to update.</p> <p>To get the ID, open the Workfront object in your browser and copy the text at the end of the URL after "ID=." For example: https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr> 
   <td>[!DNL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to update.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!DNL Select fields to map]</td> 
   <td>Select the fields that you want available for data input. This allows you to use these fields without having to scroll through the ones you don't need. You can then enter or map data into these fields.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

>[!NOTE]
>
>* When entering the ID of an object, you can begin typing the name of the object, then select it from the list. The module then enters the appropriate ID into the field.
>* When entering the text for a custom field or a [!UICONTROL Note] object (Comment or reply), you can use HTML tags in the [!UICONTROL Note Text] field to create rich text, such as bold or italic text.

+++

-->

+++ **[!UICONTROL 上载文档]**

此操作模块可将文档上传到Workfront对象，如项目、任务或问题。 此模块会以块形式上传文档，从而使Workfront的上传过程更加顺畅。

此模块可以处理比旧版模块更大的文件，是使用Ultimate Workfront包分阶段向组织推出的一部分。

您可以指定文档的位置、要上传的文件以及文件的新名称（可选）。

模块会返回文档的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 相关记录ID]</td> 
   <td>输入要将文档上传到的记录的唯一Workfront ID。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 相关记录类型]</td> 
   <td>选择您希望模块上传文档的Workfront记录类型。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 文件夹ID]</td> 
   <td>根据相关记录的类型，您可能需要输入或映射文件夹ID。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

查看可在每个Workfront模块[可用的](#workfront-object-types-available-for-each-workfront-module)Workfront对象类型中使用此模块的Workfront对象类型列表。

+++

<!--

+++ **[!UICONTROL Upload Document (Legacy)]**

This action module uploads a document to a Workfront object, such as a project, task, or issue. It uploads the entire document at once. 

You specify the location for the document, the file you want to upload, and an optional new name for the file.

The module returns the ID of the document and any associated fields, along with any custom fields and values that the connection accesses. You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Related Record ID]</td> 
   <td>Enter the unique Workfront ID of the record to which you want to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Related Record Type]</td> 
   <td>Select the type of Workfront record where you want the module to upload the document.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder ID]</td> 
   <td>Depending on the type of related record, you may need to enter or map a folder ID.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Select a source file from a previous module, or map the source file's name and data.</p> </td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).


+++
-->

### 搜索

<!--
* [Read Related Records](#read-related-records) 
* [Search](#search)
-->

+++ **[!UICONTROL 读取相关记录]**

此搜索模块读取与指定的搜索查询相匹配的记录（在特定父对象中）。

您可以指定要包含在输出中的字段。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择要读取其关联记录的父记录(Workfront对象)的类型。</p> <p>请参阅本文中每个Workfront模块<a href="#object-types-available-for-each-workfront-search-module" class="MCXref xref">可用的</a>Workfront对象类型中，可使用此模块的Workfront对象类型列表。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 父记录ID]</td> 
   <td> <p>输入或映射要读取其关联记录的父记录的ID。</p> <p>要获取ID，请在浏览器中打开Workfront对象，并复制URL末尾处“ID=”后的文本。 例如：https://my.workfront.com/project/view?ID=<i>5e43010c03286a2a555e1d0a75d6a86e</i></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 收藏集]</td> 
   <td>选择或映射您希望模块读取的子记录类型。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在此模块的输出捆绑包中的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 搜索]**

此搜索模块在Workfront中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择要模块搜索的Workfront记录类型。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 自定义表单列表]</td> 
   <td> <p>至少选择一个自定义表单。 这些自定义表单中的字段可用于搜索查询。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 结果集]</td> 
   <td>选择一个选项，以指定您希望模块获得符合您的搜索条件的第一个结果还是所有符合该条件的结果。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 最大]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 搜索条件字段]</td> 
   <td> <p>选择要用于搜索条件的字段。 随后，这些字段将显示在搜索条件下拉列表中。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 搜索条件]</td> 
   <td> <p>输入搜索依据的字段、要在查询中使用的运算符以及要在字段中搜索的值。</p> <p>注意：请勿在您的搜索条件中使用<code>username </code>。 若在Workfront的API查询中包含<code>username </code>，则会将用户记录到Workfront中，搜索将不会成功。</p> <p>注意： <code>In</code>和<code>NotIn</code>使用数组。 输入的格式应为数组。</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在此模块输出中的字段。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 引用]</td> 
   <td>选择要包含在搜索中的任何引用字段。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 收藏集]</td> 
   <td>选择要添加到搜索的任何收藏集。</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 搜索（旧版）]**

>[!IMPORTANT]
>
>此模块已替换为搜索记录模块。 我们建议在新场景中使用该模块。
>&#x200B;>使用此模块的现有方案将继续按预期运行。 此模块将于2025年5月从模块选择器中移除。

此搜索模块在Workfront中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>有关将Workfront应用程序连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将Workfront连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 记录类型]</td> 
   <td> <p>选择要模块搜索的Workfront记录类型。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 结果集]</td> 
   <td>选择一个选项，以指定您希望模块获得符合您的搜索条件的第一个结果还是所有符合该条件的结果。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 最大]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 搜索条件字段]</td> 
   <td> <p>选择要用于搜索条件的字段。 随后，这些字段将显示在搜索条件下拉列表中。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 搜索条件]</td> 
   <td> <p>输入搜索依据的字段、要在查询中使用的运算符以及要在字段中搜索的值。</p> <p>注意：请勿在您的搜索条件中使用<code>username </code>。 若在Workfront的API查询中包含<code>username </code>，则会将用户记录到Workfront中，搜索将不会成功。</p> <p>注意： <code>In</code>和<code>NotIn</code>使用数组。 输入的格式应为数组。</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 输出]</td> 
   <td> <p>选择要包含在此模块输出中的字段。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 引用]</td> 
   <td>选择要包含在搜索中的任何引用字段。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL 收藏集]</td> 
   <td>选择要添加到搜索的任何收藏集。</td> 
  </tr> 
 </tbody> 
</table>

+++

<!--not visible Jan 6, 2025

+++ **[!UICONTROL Search (Legacy)]**

This search module looks for records in an object in Workfront that match the search query you specify.

You can map this information in subsequent modules in the scenario.

When you are configuring this module, the following fields display.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
   <td> <p>For instructions about connecting your Workfront app to Workfront Fusion, see <a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">Connect Workfront to Workfront Fusion</a> in this article.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Record Type]</td> 
   <td> <p>Select the type of Workfront record that you want the module to search for.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Result Set]</td> 
   <td>Select an option to specify whether you want the module to get the first result that matches your search criteria or all the results that match it.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximal]</td> 
   <td> <p>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search criteria]</td> 
   <td> <p>Enter the field that you want to search by, the operator you want to use in your query, and the value that you are searching for in the field.</p> <p>Note: Do not use <code>username </code>in your search criteria. Including <code>username </code>in an API query to Workfront logs the user into Workfront, and the search will not be successful.</p> <p>Note: <code>In</code> and <code>NotIn</code>work with arrays. The inputs should be in array format.</p></td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Outputs]</td> 
   <td> <p>Select the fields that you want to include in the output for this module.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL References]</td> 
   <td>Select any reference fields that you want to include in the search.</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Collections]</td> 
   <td>Select any collections that you want to add to the search.</td> 
  </tr> 
 </tbody> 
</table>

See a list of the Workfront object types for which you can use this module in [Workfront object types available for each Workfront module](#workfront-object-types-available-for-each-workfront-module).

+++-->

## 适用于每个Workfront模块的Workfront对象类型

<!-- [Object types available for each Workfront trigger module](#object-types-available-for-each-workfront-trigger-module) 
* [Object types available for each Workfront action module](#object-types-available-for-each-workfront-action-module) 
* [Object types available for each Workfront search module](#object-types-available-for-each-workfront-search-module)-->

+++**每个Workfront触发器模块可用的对象类型**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col>         
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL 监视记录]</th> 
   <th>[!UICONTROL 监视字段]</th> 
   <th>[!UICONTROL 监视活动]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>审批流程</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>任务分配</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>基准</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> 账单记录 </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>计费费率</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>公司</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>功能板</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档文件夹</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>文档请求</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>文档版本</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>费用</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>费用类型</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>组</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>Hour</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>小时数类型</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>问题</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>开发周期</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>工作角色</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>日志条目</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑路径</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>注释</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>注释标签</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>组合</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目群</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目用户</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>校样审批</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>保留时间* </td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>报表</td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>风险</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险类型</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>步骤审批者</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>任务</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>团队</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>模板任务</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>时间表</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>用户</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>更新</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**每个Workfront操作模块可用的对象类型**

>[!NOTE]
>
>[!UICONTROL 下载文档]模块未包含在此表中，因为Workfront对象类型不是其配置的一部分。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL 创建记录]</th> 
   <th>[!UICONTROL 更新记录]</th> 
   <th>[!UICONTROL 删除记录]</th> 
   <th>[!UICONTROL 上传文档]</th> 
   <th>[!UICONTROL 读取记录]</th> 
   <th>[!UICONTROL 自定义API调用]</th> 
   <th>[!UICONTROL 杂项操作]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>审批流程</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>任务分配</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>基准</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
   <tr> 
   <td>账单记录</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>计费费率</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>公司</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档文件夹</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档版本</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>汇率</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>费用</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>费用类型</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>外部文档</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>组</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Hour</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>小时数类型</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>问题</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>开发周期</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>工作角色</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>日志条目</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>里程碑</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑路径</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>注释</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>注释标签</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>组合</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目群</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目用户</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>保留时间* </td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险类型</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>步骤审批者</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>任务</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>团队</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板任务</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>时间表</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>用户</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>更新</td> 
   <td> </td> 
   <td>✓</td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**每个Workfront搜索模块可用的对象类型**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th> </th> 
   <th>[!UICONTROL 搜索]</th> 
   <th>[!UICONTROL 读取相关记录]</th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>审批流程</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>任务分配</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>账单记录</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>计费费率</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>公司</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档文件夹</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>文档版本</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>费用</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>费用类型</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>组</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>Hour</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>小时数类型</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>问题</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>开发周期</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>工作角色</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>日志条目</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>里程碑路径</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>注释</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>注释标签</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>组合</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目群</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>项目</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>项目用户</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>保留时间* </td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>风险类型</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>步骤审批者</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>任务</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>团队</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>模板任务</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td>时间表</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>用户</td> 
   <td>✓</td> 
   <td>✓</td> 
  </tr> 
  <tr> 
   <td>用户委托</td> 
   <td>✓</td> 
   <td> </td> 
  </tr> 
 </tbody> 
</table>

我们建议您仔细检查，以确保它按您预期的方式运行。

+++

## Workfront > [!UICONTROL 观看活动]模块中的活动订阅筛选器

>[!NOTE]
>
>* 我们强烈建议在您的[!UICONTROL 观看活动]模块中使用活动订阅过滤器。
>
>* Workfront最近发布了其事件订阅服务的新版本。 新版本不是对Workfront API的更改，而是对事件订阅功能的更改。 此操作模块会更新用于此方案的事件有效负载版本。
>
>   有关新的事件订阅版本的详细信息，请参阅Workfront文档中的[事件订阅版本控制](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-versioning)
>
>   有关在事件订阅升级期间保留Workfront Fusion方案的资源（包括网络研讨会录像），请参阅[在事件订阅V2升级期间保留Fusion方案(https://experienceleaguecommunities.adobe.com/t5/workfront-discussions/event-follow-up-preserving-your-fusion-scenarios-during-the/td-p/754182)]。

Workfront [!UICONTROL 观看活动]模块根据在Workfront API中创建活动订阅的webhook触发场景。 事件订阅是一组数据，用于确定哪些事件发送到webhook。 例如，如果您设置了[!UICONTROL 监视事件]模块来监视问题，则事件订阅仅发送与问题相关的事件。

通过使用事件订阅过滤器，Fusion用户可以创建更适合其用例的事件订阅。 例如，您可以在Workfront API中设置事件订阅，以便仅将特定项目中的问题发送到webhook，从而确保[!UICONTROL 关注事件]模块将仅触发该项目中的问题。 创建更窄触发器的功能通过减少无关触发器的数量而改进了方案设计。

这与在Workfront Fusion场景中设置过滤器不同。 如果没有事件订阅过滤器，您的webhook将接收与您选择的对象类型相关的所有事件。 这些事件中的大多数与方案无关，必须先将其过滤掉，方案才能继续。

在Workfront >关注事件过滤器中可以使用以下运算符：

* 等于
* 不等于
* 大于
* 小于
* 大于或等于
* 小于或等于
* 包含
* 已存在
   * 此运算符不需要值，并且值字段不存在。
* 不存在
   * 此运算符不需要值，并且值字段不存在。
* 已更改
   * 此运算符不需要值，并且值字段不存在。
   * 此运算符忽略状态字段。
   * 使用`Changed`时，在&#x200B;**记录来源**&#x200B;字段中选择&#x200B;**仅更新事件**。

>[!IMPORTANT]
>
>您无法编辑现有Workfront Webhook中的筛选器。 要为Workfront活动订阅设置其他筛选器，请删除当前webhook并创建一个新筛选器。

>[!INFO]
>
>**示例：**&#x200B;考虑处理分配给特定用户Ana的新问题的方案。
>
>### 使用事件订阅过滤器过滤事件（推荐）
>
>使用事件过滤器，您可以设置webhook以在创建问题时将问题分配给Ana时触发场景。 Ana具有userID b378489d8f7cd3cee0539260720a84b7。
>
>![事件筛选器](/help/workfront-fusion/references/apps-and-modules/assets/event-filter-watch-events-350x277.png)
>
>如果一天内创建100个问题，但只有两个问题分配给Ana，则该场景将执行两次。
>
>### 筛选场景中的事件（不推荐）
>
>要筛选事件以便仅处理分配给Ana的问题，您可以在[!UICONTROL 关注事件]模块之后创建筛选器。
>
>![没有事件筛选器](/help/workfront-fusion/references/apps-and-modules/assets/watch-events-non-event-filter-350x206.png)
>
>如果一天内创建100个问题，但只有两个问题分配给Ana，则该场景将执行100次。 98个执行将在过滤器处停止，但触发器模块仍在使用数据并对所有执行执行执行操作。

有关Workfront活动订阅的详细信息，请参阅[常见问题解答 — 活动订阅](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/adobe-workfront-api/event-subscriptions/event-subs-faq)。

有关Webhook的详细信息，请参阅Adobe Workfront Fusion中的[即时触发器(Webhook)](/help/workfront-fusion/references/modules/webhooks-reference.md)

有关场景中过滤器的详细信息，请参阅[将过滤器添加到场景](/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md)。
