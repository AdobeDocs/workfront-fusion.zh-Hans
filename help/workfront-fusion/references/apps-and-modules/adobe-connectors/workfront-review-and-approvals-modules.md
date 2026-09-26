---
title: Adobe Workfront内容和审批模块
description: 通过Adobe Workfront的“内容和审批”模块，您可以获取审批详细信息、做出资产决策、添加或删除审批参与者、添加或更新审批阶段、锁定或解锁阶段以及进行自定义API调用。
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
    internal-label: Integrations
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
source-git-commit: 01689332f97c15b317e686d11a27cb4dc7e2e8bd
workflow-type: tm+mt
source-wordcount: '5202'
ht-degree: 11%
---
# Adobe Workfront统一审核和批准模块

使用Adobe Workfront统一审查和审批模块，您可以获取审批详细信息、做出资产决策、添加或删除审批参与者、添加或更新审批阶段、锁定或解锁阶段以及进行自定义API调用。

有关Workfront统一审阅和批准的信息，请参阅Workfront文档中的[统一审阅和批准概述](https://experienceleague.adobe.com/en/docs/workfront/using/review-and-approve-work/document-approvals-overview)。

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
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td>
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 先决条件

要访问Workfront内容和批准，您必须具备以下条件：

* 您必须使用支持Adobe云存储的Workfront版本。 如果贵组织尚未使用支持的版本，请联系您的Adobe客户代表。

## 连接到Adobe Workfront统一审查和批准


1. 在任意Adobe Workfront统一审查和批准模块中，单击“连接”字段旁边的&#x200B;**添加**。
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
          <p>选择 <b>Adobe Workfront 服务器到服务器连接</b>。</p>
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
          <p>输入您的实例名称，即您的域。</p><p>示例：如果您的 URL 为 <code>https://example.my.workfront.com</code>，请输入 <code>example</code>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 实例通道]</td>
        <td>
          <p>输入此连接要访问的环境类型。</p><p>示例：如果您的 URL 为 <code>https://example.my.workfront.com</code>，请输入 <code>my</code>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端 ID]</td>
        <td>请输入您的 Workfront 客户端 ID。 您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。 打开您要连接的特定应用程序即可查看客户端 ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的 Workfront 客户端密钥。 您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。 如果您的 Workfront OAuth2 应用程序没有客户端密钥，您可以重新生成一个。 有关操作说明，请参阅 Workfront 文档。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 范围]</td>
        <td>输入此连接所需的相关范围。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 主机前缀]</td>
        <td>在大多数情况下，此值应为 <code>origin</code>。
      </tr>
    </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

   如果您未登录Workfront统一审查和批准，您将被定向到登录屏幕。 登录后，您即可允许该连接。

## Adobe Workfront统一审核和批准模块

在您配置 Workfront 模块时，Workfront Fusion 会显示以下字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 Workfront 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。


![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)
* [搜索](#searches)
* [其他](#other)

### 操作

* [添加或更新参与者](#add-or-update-participants)
* [批量删除模板](#bulk-delete-templates)
* [创建模板](#create-a-template)
* [创建分组审批](#create-grouped-approval)
* [创建阶段](#create-stages)
* [锁定舞台](#lock-a-stage)
* [做出决定](#make-a-decision)
* [在舞台上做出决策](#make-a-decision-on-a-stage)
* [管理已分组审批的资源](#manage-assets-on-a-grouped-approval)
* [管理阶段参与者](#manage-stage-participants)
* [管理分组审批的阶段](#manage-stages-on-a-grouped-approval)
* [提醒舞台上的参与者](#remind-a-participant-on-a-stage)
* [提醒参与者](#remind-participant)
* [提醒未决定的参与者](#remind-undecided-participants)
* [提醒舞台上的未决定参与者](#remind-undecided-participants-on-a-stage)
* [解锁阶段](#unlock-a-stage)
* [更新阶段](#update-a-stage)
* [更新模板](#update-a-template)
* [更新所有阶段](#update-all-stages)
* [更新分组的审批（完整状态）](#update-grouped-approval-full-state)


#### 添加或更新参与者

该操作模块在批准时添加或更新默认阶段的参与者。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>文档 ID</p>
      </td>
      <td>输入或映射要为其添加或更新参与者的资源ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>将参与者添加到阶段</p>
      </td>
      <td>对于要将参与者添加到的每个阶段，单击<b>添加项</b>并进入阶段。<p> 然后，对于要添加到阶段的每个参与者，单击<b>添加项</b>并输入参与者详细信息。</p>
      <ul>
      <li><b>参与者ID</b><p>输入或映射参与者的ID。</p></li>
      <li><b>参与者类型</b><p>选择参与者是用户还是茶叶。</p></li>
      <li><b>参与者角色</b><p>选择参与者是批准者还是审阅者。</p></li>
      </ul> 
      </td> 
      </tr>
  </tbody>
</table>

#### 批量删除模板

此模块删除指定的审批模板。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>模板Id</p></td>
      <td>对于每个要删除的模板，单击<b>添加项</b>并输入模板ID。</td> 
      </tr>
  </tbody>
</table>

#### 创建模板

此操作模块创建一个审批模板

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>名称</p></td>
      <td>输入或映射模板的名称。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>公司 ID</p></td>
      <td>如果要将公司范围添加到模板，请输入或映射公司ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>阶段</p>
      </td>
      <td>对于要添加的每个阶段，单击<b>添加项</b>并输入阶段数据。<p>有关详细信息，请参阅本文中的<a href="#stages-fields" class="MCXref xref" >阶段字段</a>。 </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>共享对象为</p></td>
      <td>对于要与其共享模板的每个用户，单击<b>添加项</b>以及用户ID和所需的访问级别。</td> 
      </tr>
  </tbody>
</table>

#### 创建分组审批

此活动模块创建分组审批：一组文档版本，它们通过一个或多个审批路径一起移动，每个版本都按顺序排列阶段，并具有自己的参与者。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>名称</p></td>
      <td>输入或映射分组审批的显示名称。 名称必须介于1到255个字符之间。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>资源</p></td>
      <td>对于要包含在组中的每个文档版本，单击<b>添加项</b>并输入文档版本(DOCV) ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>路径</p></td>
      <td>对于要添加的每个批准路径，单击<b>添加项</b>并输入路径ID、名称和阶段。 每个路径都包含一系列有序的阶段。 对于每个阶段，在阶段字段中，单击<b>添加项</b>并输入以下数据：
      <ul>
      <li><b>阶段ID</b><p>输入由客户端分配的阶段标识符，该标识符在所有路径中是唯一的。 必须为字母数字，允许使用下划线或连字符，且不能超过64个字符。</p></li>
      <li><b>阶段名称</b><p>输入或映射舞台的名称。</p></li>
      <li><b>父阶段ID</b><p>对于要添加到阶段的每个父阶段，单击<b>添加项</b>并输入父ID。</p></li>
      <li><b>参加者</b><p>对于要添加到阶段的每个参与者，单击<b>添加项</b>并输入参与者详细信息。
      <ul>
      <li><b>参与者ID</b><p>输入或映射参与者的ID。</p></li>
      <li><b>参与者类型</b><p>选择参与者是用户还是团队。</p></li>
      <li><b>参与者角色</b><p>选择参与者是批准者还是审阅者。</p></li>
      </ul>
      </p></li>
      <li><b>截止日期</b><p>如果截止日期是特定日期，请输入或映射日期。</p></li>
      <li><b>距截止日期的工作日</b><p>如果截止日期在特定工作天数之后，请输入或映射天数。</p></li>
      <li><b>截止时间：小时</b><p>输入或映射截止日期(0-23)的当日时间。 与截止时间配对：分钟。</p></li>
      <li><b>截止时间：分钟</b><p>输入或映射截止日期(0-59)的小时制时间。 与截止时间：小时数配对。</p></li>
      <li><b>自定义消息</b><p>输入或映射阶段的自定义消息。</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>父对象标识</p></td>
      <td>输入或映射要与分组审批关联的Workfront父对象（例如，项目或任务）的ID。 如果使用此字段，则还必须输入对象代码。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>对象代码</p></td>
      <td>输入或映射父对象的Workfront对象类型代码（例如，<code>PROJ</code>或<code>TASK</code>）。 如果输入父对象ID，则此为必填字段。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>模板 ID</p></td>
      <td>（可选）输入或映射模板ID以在可跟踪性的分组审批中记录。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>输入或映射每个方案执行周期中您希望模块使用的最大结果数。</td> 
      </tr>
  </tbody>
</table>

#### 创建阶段

此操作模块使用给定的阶段数据创建批准。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要为其创建或更新阶段的资源的ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>阶段</p>
      </td>
      <td>对于要添加的每个阶段，单击<b>添加项</b>并输入阶段数据。<p>有关详细信息，请参阅本文中的<a href="#stages-fields" class="MCXref xref" >阶段字段</a>。 </p> </td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>模板 ID</p></td>
      <td>输入或映射要为其创建阶段的资源的ID。</td> 
      </tr>
  </tbody>
</table>

<!--
BECKY CHECK ME: The following block of Delete-prefixed Actions modules (Delete a decision on a stage, Delete a stage, Delete a template, Delete an approval, Delete decisions, Delete grouped approval, Delete participants) is not confirmed to be current in the live connector as of this update - status uncertain. Commented out for now; restore (and remove this comment) once confirmed, or delete for good if confirmed removed.

#### Delete a decision on a stage

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
   </tbody>
</table>


#### Delete a stage

This action module deletes the specified stage from the approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a stage from.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Stage ID</p></td>
      <td>Enter or map the ID of the stage that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete a template

This module deletes the specified approval template.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Template ID</p></td>
      <td>Enter or map the ID of the template that you want to delete.</td> 
      </tr>
  </tbody>
</table>

#### Delete an approval

This action module deletes the approval for the given document.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete an approval from.</td> 
      </tr>
  </tbody>
</table>

#### Delete decisions

This module removes the current user's decision from the specified stage. The current user is the user whose credentials are used in the connection used in this module.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the document that you want to delete a decision from.</td> 
      </tr>
  </tbody>
</table>

#### Delete grouped approval

This action module deletes a grouped approval, cascading to its child asset approvals and paths.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Group GUID</p></td>
      <td>Enter or map the GUID of the grouped approval that you want to delete.</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>Limit</p></td>
      <td>Enter or map the maximum number of results you want the module to work with during each scenario execution cycle.</td> 
      </tr>
  </tbody>
</table>

#### Delete participants

This action module deletes participants from an approval.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Connection</td>
      <td>For instructions on creating a connection to Adobe Workfront Unified Review and Approvals, see <a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >Connect to Adobe Workfront Unified Review and Approvals</a> in this article.</td>
    </tr>
     <tr>
      <td role="rowheader"><p>Document ID</p></td>
      <td>Enter or map the ID of the asset that you want to delete participants from.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant type</p>
      </td>
      <td>Select whether the participants is a user or a team.</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>Participant ID</p>
      </td>
      <td>Enter or map the ID of the participant.</td> 
      </tr>
  </tbody>
</table>
-->

#### 锁定舞台

此操作模块锁定指定的审批阶段并将阶段设置为不活动。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要锁定的资源的ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>阶段ID</p>
      </td>
      <td>输入或映射要锁定的阶段的ID。</td> 
      </tr>
  </tbody>
</table>

#### 做出决定

此操作模块将决策应用于审批或审批阶段。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要锁定的资源的ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>决定</p></td>
      <td>选择要应用于审批或阶段的决定。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>阶段ID</p>
      </td>
      <td>对于要将决策应用到的每个阶段，单击<b>添加项</b>并输入阶段ID。</td> 
      </tr>
  </tbody>
</table>

#### 在舞台上做出决策

此模块将决策应用于指定阶段。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要作出决策的文档ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>阶段ID</p></td>
      <td>输入或映射要对其做出决策的阶段的ID。</td> 
      </tr>
    <tr>
      <td role="rowheader"><p>决定</p></td>
      <td>选择要应用于此阶段的决策。</td> 
      </tr>
  </tbody>
</table>

#### 管理已分组审批的资源

该操作模块添加和/或删除分组审批的文档版本。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>已分组的批准ID</p></td>
      <td>输入或映射要管理资产的分组审批的GUID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>添加Assets</p></td>
      <td>对于要添加到该组的每个文档版本，单击<b>添加项</b>并输入文档版本(DOCV) ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>删除Assets</p></td>
      <td>对于要从组中移除的每个文档版本，单击<b>添加项</b>并输入文档版本(DOCV) ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>输入或映射每个方案执行周期中您希望模块使用的最大结果数。</td> 
      </tr>
  </tbody>
</table>

#### 管理阶段参与者

该操作模块在分组审批的特定阶段添加、更新和/或删除参与者。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>已分组的批准ID</p></td>
      <td>输入或映射分组审批的GUID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>阶段ID</p></td>
      <td>输入或映射要管理参与者的阶段的ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>添加参与者</p></td>
      <td>对于要添加到阶段的每个参与者，单击<b>添加项</b>并输入以下详细信息：
      <ul>
      <li><b>参与者类型</b><p>选择参与者是用户还是团队。</p></li>
      <li><b>参与者</b><p>输入或映射参与者的ID。</p></li>
      <li><b>角色</b><p>选择参与者是批准者还是审阅者。</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>更新参与者</p></td>
      <td>对于要在阶段中更新的每个参与者，单击<b>添加项</b>并输入以下详细信息：
      <ul>
      <li><b>参与者类型</b><p>选择参与者是用户还是团队。</p></li>
      <li><b>参与者</b><p>输入或映射参与者的ID。</p></li>
      <li><b>角色</b><p>选择参与者是批准者还是审阅者。</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>删除参与者</p></td>
      <td>对于要从阶段中删除的每个参与者，单击<b>添加项</b>并输入以下详细信息：
      <ul>
      <li><b>参与者类型</b><p>选择参与者是用户还是团队。</p></li>
      <li><b>参与者</b><p>输入或映射参与者的ID。</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>输入或映射每个方案执行周期中您希望模块使用的最大结果数。</td> 
      </tr>
  </tbody>
</table>

#### 管理分组审批的阶段

此操作模块在分组审批时添加、更新和/或删除阶段。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>已分组的批准ID</p></td>
      <td>输入或映射分组审批的GUID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>添加阶段</p></td>
      <td>对于要添加的每个阶段，单击<b>添加项</b>并输入以下详细信息：
      <ul>
      <li><b>阶段ID</b><p>输入或映射阶段的标识符。</p></li>
      <li><b>阶段名称</b><p>输入或映射舞台的名称。</p></li>
      <li><b>截止日期</b><p>如果截止日期是特定日期，请输入或映射日期。</p></li>
      <li><b>距截止日期的工作日</b><p>如果截止日期在特定工作天数之后，请输入或映射天数。</p></li>
      <li><b>自定义消息</b><p>输入或映射阶段的自定义消息。</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>更新暂存</p></td>
      <td>对于要更新的每个阶段，单击<b>添加项</b>并输入以下详细信息：
      <ul>
      <li><b>阶段ID</b><p>输入或映射要更新的阶段的ID。</p></li>
      <li><b>阶段名称</b><p>输入或映射舞台的名称。</p></li>
      <li><b>截止日期</b><p>如果截止日期是特定日期，请输入或映射日期。</p></li>
      <li><b>距截止日期的工作日</b><p>如果截止日期在特定工作天数之后，请输入或映射天数。</p></li>
      <li><b>自定义消息</b><p>输入或映射阶段的自定义消息。</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>删除阶段</p></td>
      <td>对于每个要删除的阶段，单击<b>添加项</b>并输入阶段ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>输入或映射每个方案执行周期中您希望模块使用的最大结果数。</td> 
      </tr>
  </tbody>
</table>

#### 提醒舞台上的参与者

此模块向特定阶段的特定参与者发送提醒。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要为其发送提醒的资源ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>阶段ID</p>
      </td>
      <td>输入或映射要为其发送提醒的阶段的ID。</td> 
      </tr>
    </tr>
     <tr>
      <td role="rowheader"><p>参与者ID</p></td>
      <td>输入或映射要向其发送提醒的参与者ID。</td> 
      </tr>
  </tbody>
</table>

#### 提醒参与者

此模块向指定的参与者发送提醒通知。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要为其发送提醒的资源ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>参与者ID</p>
      </td>
      <td>输入或映射要提醒的参与者ID。</td> 
      </tr>
      <tr>
      <td role="rowheader">
        <p>参与者类型</p>
      </td>
      <td>输入或映射要提醒的参与者类型。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>参与者角色</p>
      </td>
      <td>输入或映射要提醒的参与者的角色。</td> 
      </tr>
  </tbody>
</table>

#### 提醒未决定的参与者

此模块会向指定审批中所有未确定的参与者发送提醒通知。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要为其发送提醒的资源ID。</td> 
      </tr>
  </tbody>
</table>

#### 提醒舞台上的未决定参与者

此模块会向阶段中所有未确定的参与者发送提醒通知。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要为其发送提醒的资源ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>阶段ID</p>
      </td>
      <td>输入或映射要为其发送提醒的阶段的ID。</td> 
      </tr>
  </tbody>
</table>

#### 解锁阶段

此操作模块解锁指定的批准阶段并将阶段设置为活动状态。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要解锁的资产ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>阶段ID</p>
      </td>
      <td>输入或映射要锁定的阶段的ID。</td> 
      </tr>
  </tbody>
</table>


#### 更新阶段

此操作模块更新指定阶段上的字段。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要作出决策的文档ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>阶段ID</p></td>
      <td>输入或映射要对其做出决策的阶段的ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>阶段名称</p></td>
      <td>输入或映射模板的名称。</td> 
      </tr>
      <td role="rowheader">
        <p>其他字段</p>
      </td>
      <td>在阶段字段中输入数据。<p>有关详细信息，请参阅本文中的<a href="#stages-fields" class="MCXref xref" >阶段字段</a>。 </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>共享对象为</p></td>
      <td>对于要与其共享模板的每个用户，单击<b>添加项</b>以及用户ID和所需的访问级别。</td> 
      </tr>
  </tbody>
</table>

#### 更新模板

此模块会更新指定审批模板上的字段。



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>模板 ID</p></td>
      <td>输入或映射模板的名称。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>名称</p></td>
      <td>输入或映射要更新的模板的ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>公司 ID</p></td>
      <td>如果要将公司范围添加到模板，请输入或映射公司ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>阶段</p>
      </td>
      <td>对于要添加的每个阶段，单击<b>添加项</b>并输入阶段数据。<p>有关详细信息，请参阅本文中的<a href="#stages-fields" class="MCXref xref" >阶段字段</a>。 </p> </td> 
      </tr>
    <tr>
      <td role="rowheader"><p>共享对象为</p></td>
      <td>对于要与其共享模板的每个用户，单击<b>添加项</b>以及用户ID和所需的访问级别。</td> 
      </tr>
  </tbody>
</table>

#### 更新所有阶段

THis模块将现有审批的所有阶段替换为给定的阶段数据。 文档必须处于可编辑状态。



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射要为其更新阶段的资源的ID。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>阶段</p>
      </td>
      <td>对于要更新的每个阶段，单击<b>添加项</b>并输入阶段数据。<p>有关详细信息，请参阅本文中的<a href="#stages-fields" class="MCXref xref" >阶段字段</a>。 </p> </td> 
      </tr>
  </tbody>
</table>

#### 更新分组的审批（完整状态）

此操作模块对分组的审批应用完全状态更新。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>已分组的批准ID</p></td>
      <td>输入或映射要更新的分组审批的GUID。 例如：<code>9f8b60820000462ecf66c409d1248fa9</code>。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>路径</p></td>
      <td>对于希望分组审批具有的每个审批路径，单击<b>添加项</b>并输入路径ID、名称和阶段。 Fusion会根据当前状态协调这些路径，添加、更新和移除路径以匹配您发送的内容。 每个路径都包含一系列有序的阶段。 对于每个阶段，在阶段字段中，单击<b>添加项</b>并输入以下数据：
      <ul>
      <li><b>阶段ID</b><p>输入由客户端分配的阶段标识符，该标识符在所有路径中是唯一的。 必须为字母数字，允许使用下划线或连字符，且不能超过64个字符。</p></li>
      <li><b>阶段名称</b><p>输入或映射舞台的名称。</p></li>
      <li><b>父阶段ID</b><p>对于要添加到阶段的每个父阶段，单击<b>添加项</b>并输入父ID。</p></li>
      <li><b>参加者</b><p>对于要添加到阶段的每个参与者，单击<b>添加项</b>并输入参与者详细信息。
      <ul>
      <li><b>参与者ID</b><p>输入或映射参与者的ID。</p></li>
      <li><b>参与者类型</b><p>选择参与者是用户还是团队。</p></li>
      <li><b>参与者角色</b><p>选择参与者是批准者还是审阅者。</p></li>
      </ul>
      </p></li>
      <li><b>截止日期</b><p>如果截止日期是特定日期，请输入或映射日期。</p></li>
      <li><b>距截止日期的工作日</b><p>如果截止日期在特定工作天数之后，请输入或映射天数。</p></li>
      <li><b>截止时间：小时</b><p>输入或映射截止日期(0-23)的当日时间。 与截止时间配对：分钟。</p></li>
      <li><b>截止时间：分钟</b><p>输入或映射截止日期(0-59)的小时制时间。 与截止时间：小时数配对。</p></li>
      <li><b>自定义消息</b><p>输入或映射阶段的自定义消息。</p></li>
      </ul>
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>资源</p></td>
      <td>（可选）对于要包含该组的每个文档版本，单击<b>添加项</b>并输入文档版本(DOCV) ID。 如果忽略此字段，则当前资源将保持不变。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>幂等密钥</p></td>
      <td>（可选）输入或映射客户端提供的密钥（最多128个字符），使重试的请求安全。 如果再次发送相同的键，则模块不会再次应用更新。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>输入或映射每个方案执行周期中您希望模块使用的最大结果数。</td> 
      </tr>
  </tbody>
</table>

### 搜索

* [获取模板](#get-a-template)
* [获取审批详细信息](#get-approval-details)
* [在分组审批中获取审批](#get-approvals-in-a-grouped-approval)
* [获取分组的审批详细信息](#get-grouped-approval-details)
* [获取多个审批](#get-multiple-approvals)
* [获取建议的审批](#get-suggested-approvals)
* [获取建议的参与者](#get-suggested-participants)
* [列表机器人](#list-bots)
* [按父项列出分组的批准](#list-grouped-approvals-by-parent)
* [列表模板](#list-templates)
* [搜索AI品牌评论](#search-ai-brand-reviews)
* [搜索分组的批准](#search-grouped-approvals)


#### 获取模板

此模块返回指定的审批模板。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>模板 ID</p></td>
      <td>输入或映射您要为其获取建议审批参与者的文档ID。</td> 
      </tr>
       <tr>
         <td role="rowheader">
           返回模板的最大数量
         </td>
         <td>
              输入或映射每个方案执行周期中您希望模块返回的最大模板数。 
         </td>
       </tr>
  </tbody>
</table>

#### 获取审批详细信息

此搜索模块可检索资产的批准详细信息。



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>文档</p>
      </td>
      <td>输入或映射要检索其审批详细信息的资源的ID。</td> 
      </tr>
  </tbody>
</table>

#### 在分组审批中获取审批

此搜索模块会返回构成分组审批的单个资产审批。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>组GUID</p></td>
      <td>输入或映射要为其获取审批的分组审批的GUID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>文档版本数据</p></td>
      <td>选择是否将Redrock documentVersion记录附加到每个文档版本(DOCV)审批。 </td>
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>输入或映射每个方案执行周期中您希望模块使用的最大结果数。</td> 
      </tr>
  </tbody>
</table>

#### 获取分组的审批详细信息

此搜索模块按其GUID返回分组审批。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>组GUID</p></td>
      <td>输入或映射要获取其详细信息的分组审批的GUID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>输入或映射每个方案执行周期中您希望模块使用的最大结果数。</td> 
      </tr>
  </tbody>
</table>

#### 获取多个审批

此模块检索特定类型文档列表的审批详细信息。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档Id</p></td>
      <td>对于要检索其审批详细信息的每个文档，单击<b>添加项</b>并输入文档ID。</td> 
      </tr>
       <tr>
         <td role="rowheader">
           返回结果的最大数目
         </td>
         <td>
              输入或映射每个方案执行周期中您希望模块返回的最大结果数。 
         </td>
       </tr>
  </tbody>
</table>

#### 获取建议的审批

此模块返回来自先前文档版本的建议审批负载。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射您要获得建议审批的文档ID。</td> 
      </tr>
       <tr>
         <td role="rowheader">
           返回审批的最大数量
         </td>
         <td>
              输入或映射每个方案执行周期中您希望模块返回的最大审批数。 
         </td>
       </tr>
  </tbody>
</table>

#### 获取建议的参与者

此模块返回先前文档审批的审批参与者建议。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>文档 ID</p></td>
      <td>输入或映射您要为其获取建议审批参与者的文档ID。</td> 
      </tr>
       <tr>
         <td role="rowheader">
           返回的最大参与者数
         </td>
         <td>
              输入或映射每个方案执行周期中您希望模块返回的最大参与者数。 
         </td>
       </tr>
  </tbody>
</table>

#### 列表机器人

此模块返回分页的机器人帐户列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>页面</p></td>
      <td>输入或映射要返回的结果页。</td> 
      </tr>
       <tr>
         <td role="rowheader">
           返回结果的最大数目
         </td>
         <td>
              输入或映射每个方案执行周期中您希望模块返回的最大结果数。 
         </td>
       </tr>
  </tbody>
</table>

#### 按父项列出分组的批准

此搜索模块返回与Workfront父对象关联的分组批准。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>父级 ID</p></td>
      <td>输入或映射要为其获取分组审批的Workfront父对象（例如，项目或任务）的ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>对象代码</p></td>
      <td>（可选）输入或映射父对象的Workfront对象类型代码（例如，<code>PROJ</code>或<code>TASK</code>）。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>输入或映射每个方案执行周期中您希望模块使用的最大结果数。</td> 
      </tr>
  </tbody>
</table>

#### 列表模板

此模块返回当前用户可用的所有审批模板的列表。 当前用户是其凭据用于此模块中使用的连接的用户。



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
   </tbody>
</table>

#### 搜索AI品牌评论

此模块返回作为批准的一部分为文档版本生成的AI品牌审查结果。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>机器人用户标识</p></td>
      <td>输入或映射要搜索审阅的机器人的用户ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>父文档ID</p></td>
      <td>输入或映射要搜索审阅的父文档的ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>文档版本Id</p></td>
      <td>输入或映射要为其发送提醒的资源ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>阶段ID</p></td>
      <td>输入或映射阶段ID以将结果限制在批准的特定阶段。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>页面</p></td>
      <td>输入或映射页码以将结果限制到该页面。</td> 
      </tr>
       <tr>
         <td role="rowheader">
           返回审核的最大数量
         </td>
         <td>
              输入或映射您希望模块在每个方案执行周期中返回的最大审阅数。 
         </td>
       </tr>
  </tbody>
</table>

#### 搜索分组的批准

此搜索模块使用命名视图搜索分组的批准。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>视图</p></td>
      <td>（可选）选择或映射用于确定响应形状的命名视图。 目前，仅支持等待审批。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>（可选）输入或映射结果第一页的页面大小。 最大值为100，默认值为20。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>光标</p></td>
      <td>（可选）输入或映射上一个响应中的不透明光标，以获取下一页结果。 如果提供光标，则模块会忽略Limit字段。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>团队 ID</p></td>
      <td>（可选）对于您也希望按其匹配分组审批的每个团队（团队是参与者），单击<b>添加项</b>并输入团队ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>限制</p></td>
      <td>输入或映射每个方案执行周期中您希望模块使用的最大结果数。</td> 
      </tr>
  </tbody>
</table>

<!-- BECKY CHECK ME: the screenshot shows two separate fields both labeled "Limit" - an optional pagination page-size field (max 100, default 20, ignored if Cursor is set) and a required general execution-cycle limit, matching the Limit field used in every other module in this article. Confirm this isn't a UI labeling issue before publishing, and that both rows are needed/correctly distinguished. -->

### 其他

* [发起自定义 API 调用](#make-a-custom-api-call)
* [阶段字段](#stages-fields)


#### 发起自定义 API 调用

此模块对Adobe Workfront统一审查和批准API进行自定义API调用。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe Workfront统一审查和批准的连接的说明，请参阅本文中的<a href="#connect-to-adobe-workfront-unified-review-and-approvals" class="MCXref xref" >连接到Adobe Workfront统一审查和批准</a>。</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>相对路径</p>
      </td>
      <td>
        <p>输入相对于 <code>https://workfront.adobe.io</code> 的路径。 例如， <code>/unified-approvals/public/api/v1/approvals/&lt;ASSET_TYPE&gt;/&lt;ASSET_ID&gt;</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>方法</p>
      </td>
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。 有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">标头</td>
      <td>
        <p>以标准 JSON 对象的形式添加请求标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion 会自动添加授权标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 查询字符串]  </td>
      <td>
        <p>对于要添加到查询字符串的每个键/值对，单击<b>添加项</b>并输入键和值。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 正文]</td>
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>



#### 阶段字段

配置阶段时，以下字段可用。 并非所有字段都可用于所有模块。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">阶段名称</td>
      <td>输入或映射舞台的名称。</td>
    </tr>
     <tr>
      <td role="rowheader"><p>截止日期</p></td>
      <td>如果截止日期是特定日期，请输入或映射日期。</td> 
      </tr>
  </tbody>
     <tr>
      <td role="rowheader"><p>截止日期工作日</p></td>
      <td>如果截止日期在特定工作天数之后，请输入或映射天数。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>截止时间</p></td>
      <td>如果截止日期是特定时间，请输入或映射时间。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>参加者</p></td>
      <td>对于要添加到阶段的每个参与者，单击<b>添加项</b>并输入参与者详细信息。      
      <ul>
      <li><b>参与者ID</b><p>输入或映射参与者的ID。</p></li>
      <li><b>参与者类型</b><p>选择参与者是用户还是团队。</p></li>
      <li><b>参与者角色</b><p>选择参与者是批准者还是审阅者。</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>自动锁定已启用</p></td>
      <td>指定是否要自动锁定舞台。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>决策规则</p></td>
      <td>选择您是否希望该阶段仅需要一个决策。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>父ID/父阶段ID</p></td>
      <td>对于要添加到阶段的每个父阶段，单击<b>添加项</b>并输入父ID。</td> 
      </tr>
     <tr>
      <td role="rowheader"><p>触发器</p></td>
      <td>要为此批准阶段配置触发器，请单击<b>添加项</b>并输入触发器详细信息。      <ul>
      <li><b>类型</b><p>选择<b>激活</b></p></li>
      <li><b>当</b><p>选择是在创建批准时还是在其他阶段完成时触发该阶段。</p></li>
      <li><b>阶段</b><p>对于要添加到触发器的每个阶段，单击<b>添加项</b>并输入或映射阶段ID。</p></li>
      <li><b>决策</b><p>对于要添加到触发器的每个决策，单击<b>添加项</b>并输入或映射该决策。</p></li>
      </ul> 
      </td> 
      </tr>
     <tr>
      <td role="rowheader"><p>自定义消息</p></td>
      <td>输入或映射阶段的自定义消息。</td> 
      </tr>
</table>
