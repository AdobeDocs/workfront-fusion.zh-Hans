---
title: Microsoft Teams模块
description: 在Adobe Workfront Fusion场景中，您可以自动化使用团队的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
source-git-commit: f5b49cca308fad01167aed27e4716a3d630cb026
workflow-type: tm+mt
source-wordcount: '3642'
ht-degree: 2%

---

# Microsoft Teams模块

<!-- ADD REDIRECTS -->

在Adobe Workfront Fusion场景中，您可以自动使用Microsoft Teams的工作流，并将其连接到多个第三方应用程序和服务。

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

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

要使用Microsoft Teams模块，您必须拥有能够在模块中执行操作的Microsoft Teams帐户。

## 将Microsoft Teams服务连接到Workfront Fusion

有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅[创建与Adobe Workfront Fusion的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
>
>例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。

## Microsoft Teams模块及其字段

配置Microsoft Teams模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Microsoft Teams字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [团队](#team)
* [渠道](#channel)
* [消息](#message)
* [成员](#member)
* [在线会议](#online-meeting)
* [其他](#other)

### 团队

* [从组创建团队](#create-a-team-from-a-group)
* [创建Office 365组](#create-an-office-365-group)
* [删除团队或组](#delete-a-team-or-group)
* [获取团队](#get-a-team)
* [列出所有团队和组](#list-all-teams-and-groups)
* [列出加入的团队](#list-joined-teams)
* [更新团队](#update-a-team)
* [观看团队](#watch-teams)

#### 从组创建团队

此操作模块从现有Microsoft Office 365组创建一个团队，并为新团队配置设置。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">组 ID</td> 
   <td> <p>选择要从中创建团队的组。</p> 
   </tr> 
  <tr> 
   <td role="rowheader">允许成员创建和更新渠道</td> 
   <td>选择是否要允许成员创建和更新渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许成员删除渠道</td> 
   <td>选择是否要允许成员删除渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许成员添加和删除应用程序</td> 
   <td>选择是否要允许成员添加和删除应用程序。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许成员创建、更新和移除选项卡</td> 
   <td>选择是否要允许成员创建、更新和移除选项卡。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许成员创建和移除连接器</td> 
   <td>选择是否要允许成员创建和移除连接器。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许用户编辑其消息</td> 
   <td>选择是否要允许用户编辑其消息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许用户删除其消息</td> 
   <td>选择是否要允许用户删除其消息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许所有者删除消息</td> 
   <td>选择是否要允许所有者删除任何消息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许@team次提及</td> 
   <td>选择是否要允许@team次提及。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许@channel次提及</td> 
   <td>选择是否要允许@channel次提及。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许Giphy</td> 
   <td>选择是否要允许此团队使用Giphy。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许使用贴纸和米姆</td> 
   <td>选择是否允许用户包含标签和备忘录。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许自定义迷因</td> 
   <td>选择是否要允许用户包含自定义模组。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许来宾创建和更新渠道</td> 
   <td>选择是否要允许来宾创建和更新频道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">允许来宾删除频道</td> 
   <td>选择是否要允许来宾删除频道。</td> 
  </tr> 
 </tbody> 
</table>

#### 创建Office 365组

此操作模块在Microsoft Office 365中创建组。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">显示名称</td> 
   <td> <p>输入或映射此组在其通讯簿中显示的名称。</p> 
   </tr> 
  <tr> 
   <td role="rowheader">组的别名</td> 
   <td>输入或映射此组的电子邮件别名。 您可以包含小写字母、数字和下划线。 对于Office 365组类型，这将是组的电子邮件别名([别名]@[您的域].onmicrosoft.com)。 对于“安全组”类型，别名将用作昵称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">组类型</td> 
   <td>选择是创建Office 365组还是创建安全组。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">描述</td> 
   <td>输入或映射此组的描述。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">已启用安全性</td> 
   <td>如果要启用组的安全性，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">所有者</td> 
   <td>选择此组的所有者。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">成员</td> 
   <td>选择此组的成员。</td> 
  </tr> 
 </tbody> 
</table>

#### 删除团队或组

此操作模块删除指定的团队或组。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">组 ID</td> 
   <td> <p>输入或映射要删除的组的ID。</p> 
   </tr> 
 </tbody> 
</table>

#### 获取团队

此模块检索指定的Microsoft团队或Office 365组的属性和关系。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">组 ID</td> 
   <td> <p>输入或映射要检索其详细信息的组的ID。</p> 
   </tr> 
 </tbody> 
</table>

#### 列出所有团队和组

本模块列出了Microsoft Teams中的所有团队以及与组织关联的Office 365组。 您可以进行筛选，以仅返回符合指定条件的结果。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">筛选条件</td> 
   <td> <p>您可以将过滤器设置为仅返回符合所选标准的团队和组。</p> <p>对于每个筛选器，输入希望筛选器计算的字段、运算符以及希望筛选器允许的值。 您可以通过添加AND或OR规则来使用多个过滤器。</p> </td> 
   </tr> 
  <tr> 
   <td>返回结果的最大数目</td> 
   <td>设置Workfront Fusion在一个执行周期中返回的最大团队或组数。</td> 
  </tr> 
 </tbody> 
</table>


#### 列出加入的团队

此操作模块列出了与该模块中使用的连接相关联的用户已加入的团队。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>返回结果的最大数目</td> 
   <td>设置Workfront Fusion在一个执行周期中返回的最大团队或组数。</td> 
  </tr> 
 </tbody> 
</table>

#### 更新团队

此操作模块可更新Microsoft Teams或Office 365组中指定团队的属性。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">显示名称</td> 
   <td> <p>输入或映射此组在其通讯簿中显示的名称。</p> 
   </tr> 
  <tr> 
   <td role="rowheader">组的别名</td> 
   <td>输入或映射此组的电子邮件别名。 您可以包含小写字母、数字和下划线。 对于Office 365组类型，这将是组的电子邮件别名([别名]@[您的域].onmicrosoft.com)。 对于“安全”组类型，别名将用作昵称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">描述</td> 
   <td>输入或映射此组的描述。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">已启用安全性</td> 
   <td>如果要启用组的安全性，请启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">可见性</td> 
   <td>指定Office 365组的可见性。</td> 
  </tr> 
 </tbody> 
</table>

#### 观看团队

此触发器模块在创建团队后启动方案。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">筛选条件</td> 
   <td> <p>您可以将过滤器设置为仅监视符合您选择标准的团队和组。</p> <p>对于每个筛选器，输入希望筛选器计算的字段、运算符以及希望筛选器允许的值。 您可以通过添加AND或OR规则来使用多个过滤器。</p> </td> 
   </tr> 
  <tr> 
   <td>返回结果的最大数目</td> 
   <td>设置Workfront Fusion在一个执行周期中返回的最大团队或组数。</td> 
  </tr> 
 </tbody> 
</table>

### 渠道

* [创建渠道](#create-a-channel)
* [删除渠道](#delete-a-channel)
* [获取渠道](#get-a-channel)
* [列出渠道](#list-channels)
* [更新渠道](#update-a-channel)

#### 创建渠道

此操作模块为指定的团队创建新渠道。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">团队 ID</td> 
   <td> <p>在Microsoft Teams中选择要为其创建渠道的团队。</p> </td> 
   </tr> 
  <tr> 
   <td>渠道名称</td> 
   <td>输入或映射新渠道的名称。</td> 
  </tr> 
  <tr> 
   <td>描述</td> 
   <td>输入或映射新渠道的说明。</td> 
  </tr> 
 </tbody> 
</table>

#### 删除渠道

此操作模块会从Microsoft团队中删除指定的渠道。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">团队 ID</td> 
   <td> <p>在Microsoft Teams中输入或映射要从其中删除渠道的团队ID。</p> </td> 
   </tr> 
  <tr> 
   <td>渠道ID</td> 
   <td>输入或映射要删除的渠道的ID。</td> 
  </tr> 
  </tbody> 
</table>

#### 获取渠道

此模块检索渠道的属性和关系。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">团队 ID</td> 
   <td> <p>在Microsoft Teams中输入或映射拥有您要检索其详细信息的渠道的团队的ID。</p> </td> 
   </tr> 
  <tr> 
   <td>渠道ID</td> 
   <td>输入或映射要检索其详细信息的渠道ID。</td> 
  </tr> 
  </tbody> 
</table>

#### 列出渠道

此模块列出Microsoft Teams中指定团队拥有的渠道。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">团队 ID</td> 
   <td> <p>在Microsoft Teams中选择要为其列出渠道的团队。</p> </td> 
   </tr> 
  <tr> 
   <td>返回结果的最大数目</td> 
   <td>设置Workfront Fusion在一个执行周期内返回的最大通道数。</td> 
  </tr> 
  </tbody> 
</table>

#### 更新渠道

此操作模块更新指定渠道的说明。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">团队 ID</td> 
   <td> <p>在Microsoft Teams中选择拥有要更新的渠道的团队。</p> </td> 
   </tr> 
  <tr> 
   <td>渠道名称</td> 
   <td>输入或映射要更新的渠道的名称。</td> 
  </tr> 
  <tr> 
   <td>描述</td> 
   <td>输入或映射渠道的新描述。</td> 
  </tr> 
 </tbody> 
</table>

### 消息

* [回复渠道消息](#reply-to-a-channel-message)
* [发送消息](#send-a-message)
* [Watch消息](#watch-messages)
* [观看新回复](#watch-new-replies)

#### 回复渠道消息

此操作模块在指定渠道中创建对消息的回复。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">团队 ID</td> 
   <td> <p>选择Microsoft Teams中拥有包含要回复的消息频道的团队。</p> </td> 
   </tr> 
  <tr> 
   <td>渠道ID</td> 
   <td>选择包含要回复的消息的频道。</td> 
  </tr> 
  <tr> 
   <td>消息ID</td> 
   <td>输入或映射要回复的消息的ID。</td> 
  </tr> 
  <tr> 
   <td>内容类型</td> 
   <td>选择您要以纯文本还是HTML格式发送消息。</td> 
  </tr> 
  <tr> 
   <td>回复消息</td> 
   <td>输入或映射要发送的回复消息的正文。</td> 
  </tr> 
 </tbody> 
</table>

#### 发送消息

该操作模块会将消息发送到团队的渠道或聊天。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">消息类型/td&gt; 
   <td> <p>选择发送频道消息还是聊天消息。</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">团队 ID</td> 
   <td> <p>如果您向某个渠道发送消息，请输入或映射Microsoft Teams中负责您要将消息发送到的渠道的团队ID。</p> </td> 
   </tr> 
  <tr> 
   <td>渠道ID</td> 
   <td>如果要向某个渠道发送消息，请输入或映射要向其发送消息的渠道的ID。</td> 
  </tr> 
  <tr> 
   <td>创建新聊天</td> 
   <td>如果要发送聊天消息，请选择是否要创建新聊天。
   <ul><li><b>是</b><p>选择您要进行一对一聊天还是群组聊天，然后选择要包含在聊天中的成员。 您必须选择与此模块使用的连接关联的用户，一对一聊天必须仅包含该用户和一个其他用户。</p><p>如果要创建群组聊天，可以在“主题”字段中设置主题。</p>
   <li><b>否</b><p>输入或映射要向其发送消息的渠道所属团队的ID，然后输入或映射该渠道的ID。</td> 
  </tr> 
  <tr> 
   <td>消息</td> 
   <td>输入或映射要发送的邮件正文。</td> 
  </tr> 
  <tr> 
   <td>内容类型</td> 
   <td>选择您要以纯文本还是HTML格式发送消息。</td> 
  </tr> 
 </tbody> 
</table>

#### Watch消息

此触发器模块会在消息发送到团队的渠道或聊天时启动场景。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">要观看的消息类型</td> 
   <td> <p>选择您要观看频道消息还是聊天消息。</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">团队 ID</td> 
   <td> <p>如果您正在观看渠道消息，请选择Microsoft Teams中拥有您观看消息的渠道的团队。</p> </td> 
   </tr> 
  <tr> 
   <td>渠道ID</td> 
   <td>如果要监视渠道消息，请选择要监视消息的渠道。</td> 
  </tr> 
  <tr> 
   <td>聊天Id</td> 
   <td>如果您正在观看聊天消息，请选择要观看消息的聊天。</td> 
  </tr> 
  <tr> 
   <td>最大返回消息数</td> 
   <td>设置Workfront Fusion在一个执行周期内返回的最大消息数。</td> 
  </tr> 
 </tbody> 
</table>

#### 观看新回复

此触发器模块会在指定消息收到新回复时启动方案。

此模块不适用于个人帐户。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">团队 ID</td> 
   <td> <p>选择Microsoft Teams中拥有您监视回复的渠道的团队。</p> </td> 
   </tr> 
  <tr> 
   <td>渠道ID</td> 
   <td>选择要监视回复的频道。</td> 
  </tr> 
  <tr> 
   <td>消息ID</td> 
   <td>选择要查看回复的聊天。</td> 
  </tr> 
  <tr> 
   <td>返回回复的最大数量</td> 
   <td>设置Workfront Fusion在一个执行周期内返回的最大回复数。</td> 
  </tr> 
 </tbody> 
</table>

### 成员

* [添加成员](#add-a-member)
* [将成员添加到组](#add-a-member-to-a-group)

#### 添加成员

此操作模块会将一个成员添加到Microsoft Teams。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">成员名称</td> 
   <td> <p>输入或映射要添加到Microsoft Teams的成员名称。</p> </td> 
   </tr> 
  <tr> 
   <td>密码</td> 
   <td>输入或映射成员的密码。</td> 
  </tr> 
 </tbody> 
</table>

#### 将成员添加到组

此操作模块向Office 365组添加一个成员。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">组 ID</td> 
   <td> <p>选择要向其添加成员的组。</p> </td> 
   </tr> 
  <tr> 
   <td>成员ID</td> 
   <td>选择要添加到组的成员。</td> 
  </tr> 
 </tbody> 
</table>

### 在线会议

* [创建联机会议](#create-an-online-meeting)
* [删除联机会议](#delete-an-online-meeting)
* [获取联机会议](#get-an-online-meeting)
* [更新联机会议](#update-an-online-meeting)

#### 创建联机会议

此操作模块创建一个与用户日历上的事件无关联的独立会议。 此会议不会显示在用户的日历中。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">主题</td> 
   <td>输入或映射此会议的主题。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">开始日期和时间</td> 
   <td>输入或映射您希望会议开始的日期和时间。 有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">结束日期和时间</td> 
   <td>输入或映射希望会议结束的日期和时间。 有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许的演示者</td> 
   <td>选择允许在此会议中显示的组。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">出席者</td> 
   <td>对于要添加到会议的每个与会者，单击<b>添加项目</b>并选择与会者的姓名和角色。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许与会者启用他们的摄像头</td> 
   <td>选择是否允许与会者启用他们自己的摄像头。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许与会者启用其麦克风</td> 
   <td>选择是否允许与会者启用自己的麦克风。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许会议聊天</td> 
   <td>选择是要启用、禁用会议聊天，还是要限制会议呼叫的持续时间</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许团队反应</td> 
   <td>选择是否要为此会议启用Teams反应。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">跟帖 ID</td> 
   <td>输入或映射与此会议关联的执行绪的ID。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">消息ID</td> 
   <td>输入或映射与此会议关联的邮件的ID。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">回复链消息ID</td> 
   <td>输入或映射与此会议关联的回复链的ID。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">宣布进入和退出</td> 
   <td>选择是否希望在与会者进入或退出时宣布会议。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">范围</td> 
   <td>选择可绕过大厅等待的与会者组。 这些与会者将直接参加会议。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">启用拨入用户绕过大厅</td> 
   <td>选择是否允许拨入用户绕过大厅。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">自动录制</td> 
   <td>选择是否要自动录制会议。</td> 
   </tr> 
   </tbody> 
</table>

#### 删除联机会议

此操作模块删除具有指定ID的在线会议。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">会议Id</td> 
   <td> <p>输入或映射要删除的会议的ID。</p> </td> 
   </tr> 
 </tbody> 
</table>

#### 获取联机会议

此操作模块使用指定的ID检索联机会议的详细信息。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">会议Id</td> 
   <td> <p>输入或映射要检索其详细信息的会议ID。</p> </td> 
   </tr> 
 </tbody> 
</table>

#### 更新联机会议

此操作模块使用指定的ID更新联机会议。



<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">会议Id</td> 
   <td>输入或映射要更新的会议ID。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">主题</td> 
   <td>输入或映射此会议的主题。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">开始日期和时间</td> 
   <td>输入或映射您希望会议开始的日期和时间。 有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">结束日期和时间</td> 
   <td>输入或映射希望会议结束的日期和时间。 有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许的演示者</td> 
   <td>选择允许在此会议中显示的组。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">出席者</td> 
   <td>对于要添加到会议的每个与会者，单击<b>添加项目</b>并选择与会者的姓名和角色。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许与会者启用他们的摄像头</td> 
   <td>选择是否允许与会者启用他们自己的摄像头。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许与会者启用其麦克风</td> 
   <td>选择是否允许与会者启用自己的麦克风。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许会议聊天</td> 
   <td>选择是要启用、禁用会议聊天，还是要限制会议呼叫的持续时间</td> 
   </tr> 
   <tr> 
   <td role="rowheader">允许团队反应</td> 
   <td>选择是否要为此会议启用Teams反应。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">跟帖 ID</td> 
   <td>输入或映射与此会议关联的执行绪的ID。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">消息ID</td> 
   <td>输入或映射与此会议关联的邮件的ID。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">回复链消息ID</td> 
   <td>输入或映射与此会议关联的回复链的ID。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">宣布进入和退出</td> 
   <td>选择是否希望在与会者进入或退出时宣布会议。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">范围</td> 
   <td>选择可绕过大厅等待的与会者组。 这些与会者将直接参加会议。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">启用拨入用户绕过大厅</td> 
   <td>选择是否允许拨入用户绕过大厅。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">自动录制</td> 
   <td>选择是否要自动录制会议。</td> 
   </tr> 
   </tbody> 
</table>

### 其他

* [检查用户是否存在](#check-presence-of-users)
* [进行自定义API调用](#make-a-custom-api-call)
* [搜索用户](#search-users)

#### 检查用户是否存在

此操作模块检查选定的用户是否出现在Microsoft Teams上。

此模块不支持个人帐户。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">用户ID</td> 
   <td> <p>选择要检查其是否存在的用户。</p> </td> 
   </tr> 
 </tbody> 
</table>

#### 进行自定义API调用

此操作模块向Microsoft Teams API发出自定义请求。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL URL]</td> 
   <td>输入相对于<code>https://graph.microsoft.com</code>的路径。 示例：<code> /v1.0/groups</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
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

#### 搜索用户

此模块使用您指定的条件搜索用户。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接 </td> 
   <td> <p>有关将Microsoft Teams帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">筛选条件</td> 
   <td> <p>您可以将过滤器设置为仅返回符合所选标准的用户。</p> <p>对于每个筛选器，输入希望筛选器计算的字段、运算符以及希望筛选器允许的值。 您可以通过添加AND或OR规则来使用多个过滤器。</p> </td> 
   </tr> 
  <tr> 
   <td>返回结果的最大数目</td> 
   <td>设置Workfront Fusion在一个执行周期中返回的最大团队或组数。</td> 
  </tr> 
 </tbody> 
</table>



