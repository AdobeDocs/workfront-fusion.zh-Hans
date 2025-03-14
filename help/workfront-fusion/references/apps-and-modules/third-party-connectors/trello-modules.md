---
title: 网格模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用Trello的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 5df5cd2b-ad4c-4a02-9d0c-7cee35232f93
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '5217'
ht-degree: 0%

---

# [!UICONTROL 网格]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!UICONTROL Trello]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL Trello]模块，您必须具有[!UICONTROL Trello]帐户。

## Trello API信息

Trello连接器使用以下功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://api.trello.com/1</td>
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v4.12.37</td> 
  </tr>
 </tbody> 
 </table>

## 将[!UICONTROL Trello]连接到[!DNL Workfront Fusion]

有关将[!UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅[创建与 [!DNL Adobe Workfront Fusion] 的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!UICONTROL Trello]模块及其字段

配置[!UICONTROL Trello]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 此外，根据应用程序或服务中的访问级别等因素，还可能会显示其他[!UICONTROL 网格]字段。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [展示板](#boards)
* [列表](#lists)
* [信息卡](#cards)
* [成员](#members)
* [核对清单](#checklists)
* [标签](#labels)
* [评论](#comments)

### 展示板

+++ **[!UICONTROL 存档或取消存档讨论区]**

此操作模块可关闭（存档）或重新打开（取消存档）您指定的讨论区。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL展示板ID]</td> 
   <td> <p> 输入或映射要关闭或重新打开的主板的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL存档或取消存档]</td> 
   <td> <p> 选择要关闭（存档）还是重新打开（取消存档）展示板。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 将成员分配给讨论区]**

此操作模块会将成员分配给您指定的展示板。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL展示板ID]</td> 
   <td> <p> 选择要添加成员的讨论区。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL电子邮件地址]</td> 
   <td> <p> 输入或映射要添加到讨论区的成员的电子邮件地址。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL成员类型]</p> </td> 
   <td> <p>选择您希望新成员成为的成员类型。</p> 
    <ul> 
     <li><strong>[！UICONTROL管理员]</strong>：讨论区管理员可以对讨论区执行任何讨论区操作。</li> 
     <li><strong>[！UICONTROL Normal]</strong>：普通成员只是讨论区的成员。</li> 
     <li><strong>[！UICONTROL观察者]</strong>：观察者是对讨论区具有只读访问权限的成员。 <br>观察者仅适用于具有[！UICONTROL Trello Business Class]的团队。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL全名]</td> 
   <td> <p> 输入或映射要添加到展示板的用户的全名。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 创建讨论区]**

此操作模块使用选定的设置创建新展示板。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL名称] </td> 
   <td> <p>输入或映射新讨论区的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL描述]</td> 
   <td> <p>根据需要输入或映射讨论区描述。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL组织ID]</p> </td> 
   <td> <p>输入或映射组织的ID。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL权限级别]</p> </td> 
   <td> <p>董事会在每个权限级别都有不同的投票和注释规则。 例如，如果您的讨论区是[！UICONTROL Private]，并且您将投票和注释规则设置为[！UICONTROL All]，则会收到错误。 </p> <p>每个权限级别的投票和评论仅限以下组：</p> 
    <ul> 
     <li><strong>[！UICONTROL Private]</strong>： 
      成员、成员和观察员</li> 
     <li><strong>[！UICONTROL对于组织]</strong>： 
      成员、成员和观察员、组织成员</li> 
     <li><strong>[！UICONTROL Public]</strong>： 
      成员、成员和观察员、组织成员、所有</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Voting]</p> </td> 
   <td> <p>选择一个选项，以指定可以在该讨论区投票的人员。 有关权限级别的投票限制，请参阅[！UICONTROL权限级别]字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Comments]</p> </td> 
   <td> <p>选择一个选项，以指定可以对此讨论区的信息卡进行评论的人员。 有关对权限级别的限制的注释，请参阅[！UICONTROL权限级别]字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL邀请]</p> </td> 
   <td> <p>选择谁可以邀请其他人加入此讨论区。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Self-join]</p> </td> 
   <td> <p>选择团队成员是否可以自己加入讨论区，或者必须邀请他们。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL默认标签]</p> </td> 
   <td> <p>选择是否为新展示板使用默认标签集。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL默认列表]</p> </td> 
   <td> <p>选择是否将默认列表集添加到展示板([！UICONTROL To Do]、[！UICONTROL Doing]、[！UICONTROL Done])。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL展示板源ID]</p> </td> 
   <td> <p>选择或映射要复制到新展示板中的展示板ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL卡盖]</p> </td> 
   <td> <p>如果要为展示板启用卡盖，请选择<strong>[！UICONTROL是]</strong>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL背景]</p> </td> 
   <td> <p>选择背景或自定义背景的颜色。</p> <p>注意：自定义背景仅适用于[！UICONTROL Trello Gold and Business Class]订阅者。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL背景ID]</td> 
   <td> <p> 如果已在[！UICONTROL背景]字段中选择使用自定义背景，请输入或映射要使用的背景的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL卡老化]</p> </td> 
   <td> <p>选择两种信息卡老化模式。 </p> 
    <ul> 
     <li><strong>[！UICONTROL海盗模式]</strong>：信息卡会随着年龄增长而撕裂、变黄和破裂，就像旧海盗地图一样。</li> 
     <li><strong>[！UICONTROL常规模式]</strong>：卡片会随着年龄增长而逐渐变透明。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 编辑讨论区]**

此操作模块编辑现有展示板的设置。

>[!SUCCESS]
>
><table style="table-layout:auto">
<col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL展示板ID]</p> </td> 
   <td> <p>输入或映射您希望模块创建的讨论区的唯一[！UICONTROL Trello] ID。 您可以使用其他模块（如监视板模块）检索展示板ID</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/watch-boards.png"> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL新名称]</td> 
   <td> <p> 输入或映射展示板的新名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL新描述]</td> 
   <td> <p> 输入或映射新的讨论区描述。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL组织ID]</p> </td> 
   <td> <p>输入或映射您希望模块编辑的讨论区的唯一[！UICONTROL Trello] ID。  </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL订阅] </td> 
   <td> <p>选择一个选项，以指定拥有此模块使用的连接的用户是否订阅了展示板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL权限级别]</p> </td> 
   <td> <p>董事会在每个权限级别都有不同的投票和注释规则。 例如：如果您的讨论区是[！UICONTROL Private]，并且您将投票和注释规则设置为[！UICONTROL All]，则会收到错误。 </p> <p>每个权限级别的投票和评论仅限以下组：</p> 
    <ul> 
     <li><strong>[！UICONTROL Private]</strong>： 
      成员、成员和观察员</li> 
     <li><strong>[！UICONTROL对于组织]</strong>： 
      成员、成员和观察员、组织成员</li> 
     <li><strong>[！UICONTROL Public]</strong>： 
      成员、成员和观察员、组织成员、所有</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Voting]</p> </td> 
   <td> <p>选择一个选项，以指定可以在该讨论区投票的人员。 有关权限级别的投票限制，请参阅[！UICONTROL权限级别]字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Comments]</p> </td> 
   <td> <p>选择一个选项，以指定可以对此讨论区的信息卡进行评论的人员。 有关对权限级别的限制的注释，请参阅[！UICONTROL权限级别]字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL邀请] </td> 
   <td> <p>选择谁可以邀请人员加入此讨论区。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Self-join]</td> 
   <td> <p> 选择团队成员是否可以自己加入讨论区，或者必须邀请他们。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL卡盖]</td> 
   <td> <p> 选择是否应在此展示板上显示卡盖。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL背景] </td> 
   <td> <p>选择背景或自定义背景的颜色。</p> <p>注意：自定义背景仅适用于[！UICONTROL Trello Gold and Business Class]订阅者。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL背景ID]</td> 
   <td> <p> 如果已在[！UICONTROL背景]字段中选择使用自定义背景，请输入或映射要使用的背景的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL卡老化]</p> </td> 
   <td> <p>选择两种信息卡老化模式。 </p> 
    <ul> 
     <li><strong>[！UICONTROL海盗模式]</strong>：信息卡会随着年龄增长而撕裂、变黄和破裂，就像旧海盗地图一样。</li> 
     <li><strong>[！UICONTROL常规模式]</strong>：卡片会随着年龄增长而逐渐变透明。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL日历信息源已启用]</td> 
   <td> <p> 选择是否启用日历馈送。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL &lt;颜色&gt;标签名称]</td> 
   <td> <p> 为所需的颜色标签指定一个名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL存档] </td> 
   <td> <p>选择一个选项以指示是否要存档（关闭）展示板。 </p> </td> 
  </tr> 
 </tbody> 
</table>


+++

+++ **[!UICONTROL 获取讨论区]**

此操作模块可检索讨论区的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL展示板ID]</p> </td> 
   <td> <p>输入或映射要检索相关信息的展示板的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!DNL Search for Boards]**

此搜索模块可检索有关您指定的主板的信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Query] </td> 
   <td> <p>输入或映射要获取相关信息的展示板的名称（或部分名称）。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL返回展示板的最大数量]</td> 
   <td> <p> 输入在一个执行周期内将返回的最大展示板数[!DNL Workfront Fusion]。 此值必须小于或等于1000。</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Partial] </p> </td> 
   <td> <p>默认情况下，此模块会搜索成员内容，以查找与查询中每个单词完全匹配的内容。 启用[！UICONTROL Partial]后，模块会查找以查询中任意单词开头的内容。</p> <p> 例如，如果您使用“development”一词来查找标题为“My Development Status Report”（我的开发状态报告）的展示板，则默认情况下需要搜索整个词。 如果您启用了[！UICONTROL Partial]，则可以搜索“dev”，但不能搜索“velopment”。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Boards] </td> 
   <td> <p>输入“我的”，或映射以逗号分隔的展示板ID列表。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 从讨论区中取消分配成员]**

此操作模块从展示板中删除成员。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL展示板ID]</td> 
   <td> <p> 输入（映射或选择）要从其中移除用户的展示板的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL成员] </td> 
   <td> <p>选择要从展示板中移除的成员。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 观看讨论区]**

此触发器模块在添加新展示板后开始执行场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制] </td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块返回的最大展示板数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 列表

+++ **[!UICONTROL 创建列表]**

此操作模块会在您指定的展示板上创建一个列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL展示板ID]</td> 
   <td> <p> 输入或映射要创建列表的展示板的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL名称] </td> 
   <td> <p>输入或映射新列表的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL位置] </td> 
   <td> <p>选择是将列表添加到顶部还是将其附加到卡片的底部。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL复制列表]</td> 
   <td> <p> 如果要复制列表，请选择您要如何输入要复制的列表的ID。</p> 
    <ul> 
     <li> <p><strong>手动输入</strong> </p> <p>在<strong>[！UICONTROL列表ID]</strong>字段中，输入或映射要复制的列表的ID。<br></p> </li> 
     <li> <p><strong>选择</strong> </p> <p>选择包含要复制的列表的主板，然后选择该列表。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 编辑列表]**

此操作模块编辑现有列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL列表ID]</td> 
   <td> <p> 输入或映射要更新的列表的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL名称] </td> 
   <td> <p>输入或映射列表的新名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL展示板ID]</td> 
   <td> <p> 映射或选择要移动列表的展示板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL位置] </td> 
   <td> <p>选择是将列表添加到顶部还是将其附加到卡片的底部。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL已订阅]</td> 
   <td> <p>如果要将活动成员订阅到列表，请启用此选项。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 获取列表]**

此操作模块可检索有关特定列表的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL列表ID]</p> </td> 
   <td> <p>输入或映射要检索其相关信息的列表的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 观看卡片移至列表]**

将信息卡移动到特定列表时，此触发器模块将激活。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Board]</td> 
   <td>选择包含您要监视卡片列表的展示板。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL列表]</td> 
   <td>选择要监视卡片的列表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制] </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 信息卡

+++ **[!UICONTROL 添加附件]**

此操作模块将一个附件添加到选定的信息卡。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入卡片ID]</td> 
   <td> <p> 选择您希望如何输入要向其添加附件的卡的ID。</p> 
    <ul> 
     <li> <p><strong>手动输入</strong> </p> <p>在<strong>[！UICONTROL卡片ID]</strong>字段中，输入或映射要向其添加附件的卡片ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要向其添加附件的卡的主板，然后选择包含该卡的列表，然后选择该卡。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL附件类型]</p> </td> 
   <td> <p>选择是要直接上载文件，还是要提供文件的URL。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL文件]</strong> </p> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </li> 
     <li> <p><strong>[！UICONTROL URL]</strong> </p> <p>输入文件的URL，并提供附件的名称。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 存档或取消存档卡片]**

此操作模块存档或将信息卡发送回展示板。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL卡ID]</td> 
   <td> <p> 输入或映射要存档或发回展示板的卡片ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL存档或取消存档]</td> 
   <td> <p> 选择是要关闭卡片（存档）还是将其发送回展示板（取消存档）。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 创建信息卡]**

此操作模块在选定列表中创建一个信息卡。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入列表ID]</td> 
   <td> <p> 选择您希望如何输入要添加信息卡的列表的ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL列表ID]</strong>字段中，输入或映射要添加卡片的列表的ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要添加卡片的列表的主板，然后选择列表。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL标签] </td> 
   <td> <p>对于要添加到卡片中的每个标签，单击<b>添加项</b>并输入标签的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL成员]</td> 
   <td>对于要添加到卡片中的每个成员，单击<b>添加项</b>并输入成员的ID。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL名称] </td> 
   <td> <p>输入新卡的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL描述]</p> </td> 
   <td> <p>输入卡的说明。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL位置] </td> 
   <td> <p>选择是将信息卡添加到顶部还是将信息卡附加到列表的底部。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL到期日期]</td> 
   <td> <p> 输入信息卡的到期日期。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL到期结束]</td> 
   <td> <p> 启用此选项以在到期日期将信息卡标记为完成。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件URL]</td> 
   <td> <p>输入或映射要作为附件添加到信息卡的文件的URL。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Source file]</p> </td> 
   <td> <p>输入或映射要作为附件添加到卡片上的文件信息。 从上一个模块中选择一个文件，或映射文件的名称和数据</p> 
     <p>注意：每个附件有10 MB的文件上传限制。 但是，[！UICONTROL Business Class]和[！UICONTROL Trello Gold]成员在每个附件中的文件上传限制为250 MB。</p> 
     </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL复制卡]</td> 
   <td> <p> 如果要创建新信息卡作为现有信息卡的副本，请选择您要如何输入要复制的信息的卡ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL卡片ID]</strong>字段中，输入或映射要复制的卡片ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要复制的信息卡的主板，然后选择包含该信息卡的列表，然后选择该信息卡。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 编辑卡片]**

此操作模块编辑现有信息卡。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入卡片ID]</td> 
   <td> <p> 选择您要如何输入要编辑的卡片ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL卡片ID]</strong>字段中，输入或映射要编辑的卡片ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要编辑的信息卡的主板，然后选择包含该信息卡的列表，然后选择该信息卡。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL新名称]</td> 
   <td> <p>输入或映射卡的新名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL新描述]</p> </td> 
   <td> <p>输入或映射卡的新描述。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL移动卡片]</p> </td> 
   <td> <p>选择展示板或展示板，并列出您要移动卡的位置。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL标签] </td> 
   <td> <p>对于要添加到卡片中的每个标签，单击<b>添加项</b>并输入标签的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL位置] </td> 
   <td> <p>选择是将信息卡添加到列表顶部还是将信息卡附加到列表底部。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL到期日期]</td> 
   <td> <p> 输入信息卡的到期日期。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL到期结束]</td> 
   <td> <p> 启用此选项以在到期日期将信息卡标记为完成。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL成员] </td> 
   <td> <p>对于每个要添加到卡片的成员，单击<b>添加项</b>并输入或映射成员的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL附件封面ID]</p> </td> 
   <td> <p>输入或映射您希望卡用作封面的图像附件的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL订阅] </td> 
   <td> <p>选择是否应订阅该卡。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL存档] </td> 
   <td> <p>选择一个选项以指示是否要存档（关闭）卡片。 </p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 获取信息卡]**

此操作模块可检索选定信息卡的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL展示板ID]</td> 
   <td> <p>输入包含要检索其详细信息的卡的主板的ID。 这允许您查看展示板自定义字段的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入卡片ID]</td> 
   <td> <p> 选择您要如何输入用于检索其详细信息的卡的ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL卡片ID]</strong>字段中，输入或映射要检索其详细信息的卡片ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要检索其详细信息的信息卡的主板，选择包含该信息卡的列表，然后选择该信息卡。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 搜索卡片]**

此操作模块返回与搜索查询匹配的卡片。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Board] </td> 
   <td> <p>选择要搜索的主板。 如果未选择展示板，则将搜索所有展示板。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Query]</p> </td> 
   <td> <p>输入搜索查询。 您可以使用以下搜索运算符来优化搜索：</p> 
    <ul> 
     <li><code><strong>-operator</strong></code> <p>您可以将“ — ”添加到任何运算符以进行负面搜索，例如<code>[!UICONTROL -has:members]</code>来搜索未分配任何成员的卡片。</p> </li> 
     <li><code><strong>@name</strong></code> <p>返回分配给成员的卡片。 您也可以使用<code>member:</code>。 使用<code>@me</code>仅包含您的卡片。</p> </li> 
     <li><code><strong>#label</strong></code> <p>返回标记的卡片。 您也可以使用<code>label:</code>。 例如，<code>label:"FIX IT"</code>将返回标签为“FIX IT”的卡片。</p> </li> 
     <li><code><strong>board:id</strong></code> <p>返回特定展示板中的卡片。 例如，<code>board:Trello</code>将返回展示板名称中带有[！UICONTROL Trello]的展示板上的卡片。</p> </li> 
     <li><code><strong>list:name</strong></code> <p>返回列表中名为“name”的卡片。</p> </li> 
     <li><code><strong>has:attachments</strong></code> <p>返回带有附件的卡片。 <code>has</code>：运算符也可以与其他属性（如<code>has:description</code>、<code>has:cover</code>、<code>has:members</code>或<code>has:stickers</code>）一起使用。</p> </li> 
     <li><code><strong>due:day</strong></code> <p>返回24小时内到期的卡片。 <code>due:</code>运算符也可以与其他时间范围一起使用，如<code>due:week</code>、<code>due:month</code>或<code>due:overdue</code>。 您还可以搜索特定的日期范围。 例如，向搜索添加<code>due:14</code>将包含未来14天到期的卡片。</p> </li> 
     <li><code><strong>created:day</strong></code> <p>返回过去24小时内创建的卡片。 <code> created:</code>运算符还可以与其他时间范围（如<code>created:week</code>或<code>created:month</code>）一起使用。 您还可以搜索特定的日期范围。 例如，将<code>created:14</code>添加到搜索包括最近14天创建的卡片。</p> </li> 
     <li><code><strong>edited:day</strong></code> <p>返回过去24小时内编辑的卡片。 <code>edited:</code>运算符也可以与其他时间范围一起使用，如<code>edited:week</code>或<code>edited:month</code>。 您还可以搜索特定的日期范围。 例如，将<code>edited:21</code>添加到搜索包括过去21天内编辑的卡片。</p> </li> 
     <li><code><strong>description:</strong>, <strong>checklist:</strong>, <strong>comment:</strong>, and <strong>name:</strong></code> <p>返回与信息卡描述、核对清单、注释或名称文本匹配的信息卡。 例如，<code>comment:"FIX IT"</code>将在注释中返回带有“FIX IT”的卡片。</p> </li> 
     <li><code><strong>is:open</strong> and <strong>is:archived</strong></code> <p>返回打开或存档的卡片。 如果未指定，则[！UICONTROL Trello]会返回这两种类型。</p> </li> 
     <li><code><strong>is:starred</strong> </code> <p>仅包括星形展示板上的信息卡。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL返回的信息卡最大数量]</td> 
   <td> <p> 输入或映射您希望[!DNL Workfront Fusion]在一个执行周期内返回的最大卡片数。 此值必须小于或等于1000。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Partial] </td> 
   <td> <p>默认情况下，此模块会搜索成员内容，以查找与查询中每个单词完全匹配的内容。 启用[！UICONTROL Partial]后，模块会查找以查询中任意单词开头的内容。</p> <p> 例如，如果您使用“development”一词来查找标题为“My Development Status Report”（我的开发状态报告）的展示板，则默认情况下需要搜索整个词。 如果您启用了[！UICONTROL Partial]，则可以搜索“dev”，但不能搜索“velopment”。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL卡片] </td> 
   <td> <p>要搜索特定信息卡，请单击<b>添加项目</b>并添加该信息卡的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 看卡片]**

此触发器模块会在添加新信息卡后启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL观察对象]</td> 
   <td> <p>选择要监视卡的位置。</p> 
    <ul> 
     <li><strong>[！UICONTROL所有卡片]</strong> </li> 
     <li> <p>特定展示板上的<strong>卡片</strong> </p> <p>选择要监视卡片的讨论区</p> </li> 
     <li> <p><strong>[！UICONTROL卡片位于特定列表]</strong> </p> <p>选择包含要监视卡片列表的展示板，然后选择列表。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制] </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 成员

+++ **[!UICONTROL 向信息卡添加成员]**

此操作模块将指定的成员添加到指定的信息卡。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL输入卡片ID和成员ID]</p> </td> 
   <td> <p>选择您希望如何输入卡片ID和成员ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>输入或映射<strong>[！UICONTROL卡ID]</strong>和<strong>[！UICONTROL成员ID]</strong>。</p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要向其添加成员的卡片的展示板，然后选择包含该卡片的列表、卡片本身以及要添加到卡片中的成员。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 将成员分配给讨论区]**

请参阅[讨论区](#boards)下的“[!UICONTROL 将成员分配给讨论区]”。

+++

+++ **[!UICONTROL 搜索成员]**

此操作模块检索有关[!UICONTROL Trello]成员的信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Query] </td> 
   <td> <p>输入要查找的用户的名称或用户名。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Partial] </td> 
   <td> <p>默认情况下，此模块会搜索成员内容，以查找与查询中每个单词完全匹配的内容。 启用[！UICONTROL Partial]后，模块会查找以查询中任意单词开头的内容。</p> <p> 例如，如果您使用“development”一词来查找标题为“My Development Status Report”（我的开发状态报告）的展示板，则默认情况下需要搜索整个词。 如果您启用了[！UICONTROL Partial]，则可以搜索“dev”，但不能搜索“velopment”。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL返回成员的最大数目]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 从讨论区中取消分配成员]**

请参阅[讨论区](#boards)下的“[!UICONTROL 从讨论区中取消分配成员]”。

+++

### 核对清单

+++ **[!UICONTROL 创建清单]**

此操作模块在选定的信息卡上创建核对清单。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入卡片ID]</td> 
   <td> <p> 选择您要如何输入要添加核对清单的卡的ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL卡ID]</strong>字段中，输入或映射要添加清单的卡ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要在其中添加清单的卡的主板，然后选择包含该卡的列表，然后选择该卡。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL名称] </td> 
   <td> <p>输入或映射清单的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL位置] </td> 
   <td> <p>选择是将清单添加到顶部还是将清单附加到卡片底部。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL输入核对清单ID]</p> </td> 
   <td> <p>如果通过复制现有清单来创建清单，请输入要复制的源清单的ID或将该ID映射到新清单中。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 创建清单项目]**

此操作模块会将项目添加到特定核对清单。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入核对清单ID]</td> 
   <td> <p> 如果通过复制现有清单来创建新的清单，请选择您要如何输入要添加项目的清单ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL清单ID]</strong>字段中，输入或映射要添加清单的卡ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要在其中添加清单的卡的主板，然后选择包含该卡的列表，然后选择清单。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL项名称]</p> </td> 
   <td> <p>输入或映射新项目的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL位置]</p> </td> 
   <td> <p>选择是将项目添加到清单顶部还是将[！UICONTROL append]添加到清单底部。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL已选中]</p> </td> 
   <td> <p>如果要将项目添加为已选中，则启用此选项。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 编辑清单项目]**

此操作模块可编辑现有核对清单。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入卡片ID和清单项目ID]</td> 
   <td> <p> 选择您要如何输入卡的ID以及要在其中编辑项目的核对清单。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL清单ID]</strong>字段中，输入或映射要添加清单的卡ID。</p> <p>在<strong>[！UICONTROL清单项目ID]</strong>字段中，输入或映射清单的ID。</p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要在其中添加清单的卡的主板，然后选择包含该卡的列表，然后选择清单。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL核对清单ID]</td> 
   <td>选择或映射要将清单项目移动到的清单。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL项名称]</p> </td> 
   <td> <p>输入或映射新项目的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL位置]</p> </td> 
   <td> <p>选择是将项目添加到清单顶部还是附加到清单底部。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL状态]</p> </td> 
   <td> <p>选择清单项目是完整的还是不完整的。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 标签

+++ **[!UICONTROL 向卡片添加标签]**

此操作模块向选定的信息卡添加标签。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入卡片ID]</td> 
   <td> <p> 选择您要如何输入要添加核对清单的卡的ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL卡ID]</strong>字段中，输入或映射要添加清单的卡ID。 在<strong>[！UICONTROL标签ID]</strong>字段中，输入或映射要添加标签的ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要在其中添加清单的卡的主板，然后选择包含该卡的列表，然后选择该卡。 </p> <p>选择要添加到卡片的标签。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

### 评论

+++ **[!UICONTROL 在信息卡中创建评论]**

此操作模块向选定的信息卡添加评论。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入卡片ID]</td> 
   <td> <p> 选择您希望如何输入要添加注释的卡片ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL卡片ID]</strong>字段中，输入或映射要添加注释的卡片ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要在其中添加注释的卡片的展示板，然后选择包含该卡片的列表，然后选择该卡片。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Comment] </td> 
   <td> <p>输入或映射要添加到选定信息卡的注释。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 在信息卡中列出评论]**

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入卡片ID]</td> 
   <td> <p> 选择您希望如何输入要添加注释的卡片ID。</p> 
    <ul> 
     <li> <p><strong>[！UICONTROL手动输入]</strong> </p> <p>在<strong>[！UICONTROL卡片ID]</strong>字段中，输入或映射要添加注释的卡片ID。<br></p> </li> 
     <li> <p><strong>[！UICONTROL Select]</strong> </p> <p>选择包含要在其中添加注释的卡片的展示板，然后选择包含该卡片的列表，然后选择该卡片。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL返回的最大评论数]</td> 
   <td> <p> 输入在一个执行周期内[!DNL Workfront Fusion]将返回的最大注释数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL始自] </td> 
   <td> <p>设置创建评论时段的开始日期。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Before] </td> 
   <td> <p>设置创建评论时段的结束日期。 有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL 观看评论]**

此触发器模块会在添加评论时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将您的[！UICONTROL Trello]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL观察对象]</td> 
   <td> <p>选择要监视注释的位置。</p> 
    <ul> 
     <li><strong>[！UICONTROL所有卡片]随处</strong> </li> 
     <li> <p><strong>[！UICONTROL板]</strong> </p> <p>选择要监视其评论的讨论区</p> </li> 
     <li> <p><strong>[！UICONTROL列表]</strong> </p> <p>选择包含要监视其注释的列表的展示板，然后选择列表。</p> </li> 
     <li><strong>[！UICONTROL卡]</strong> </li> 
     <li>选择包含要监视其注释的信息卡的主板，然后选择包含该信息卡的列表，然后选择该信息卡。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制] </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中返回的最大注释数。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

## [!UICONTROL 网格]对象ID

* [如何在 [!DNL Trello]中查找信息卡的ID或短链接](#how-to-find-the-id-or-the-shortlink-of-a-card-in-trello)
* [如何在 [!DNL Trello]中查找其他对象的ID](#how-to-find-ids-of-other-objects-in-trello)

### 如何在[!DNL Trello]中查找信息卡的ID或短链接

如果要编辑信息卡或创建新评论，您需要知道信息卡或其短链接的ID。 您可以从[!UICONTROL 新卡片]触发器的输出获取此信息。 通过打开信息卡并单击[!UICONTROL 共享]按钮，也可以获取信息卡的短链接。 可以在`https://trello.com/c/`之后URL末尾的[!UICONTROL 链接此信息卡]框中找到短链接。

![共享和更多](/help/workfront-fusion/references/apps-and-modules/assets/share-and-more-350x575.png)

### 如何在[!DNL Trello]中查找其他对象的ID

讨论区、列表和评论ID只能使用触发器获取。 [!DNL `trello.com`]网站不显示这些ID。
