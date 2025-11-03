---
title: Cvent模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Cvent的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: b7e16180-1db8-4aff-bb7b-69ca98194b00
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1129'
ht-degree: 1%

---

# [!DNL Cvent]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Cvent]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何Adobe Workfront Workflow包和任何Adobe Workfront自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime和Select包，以及额外购买的Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>标准</p><p>工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证</td> 
   <td>
   <p>基于操作：不需要Workfront Fusion许可证</p>
   <p>基于连接器（旧版）：用于工作自动化和集成的Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果贵组织具有不包含Workfront Automation and Integration的Select或Prime Workfront包，则贵组织必须购买Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

要使用[!DNL Cvent]模块，您必须具有[!DNL Cvent]帐户。

## Cvent API信息

Cvent连接器使用以下功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> V200611.ASMX </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.7.14</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Cvent]连接到Adobe Workfront Fusion {#connect-cvent-to-adobe-workfront-fusion}

>[!NOTE]
>
>[!DNL Cvent]模块通过[!UICONTROL SOAP] API工作。 要创建与[!DNL Cvent]的连接，您必须确保以下各项：
>
>* 您有[!UICONTROL SOAP]访问[!DNL Cvent] API的权限。
>* Workfront Fusion IP地址已添加到您组织的允许列表。
>
>  有关Workfront Fusion IP地址的列表，请参阅组织的允许列表中的[为Fusion配置IP地址](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)


您可以在[!DNL Cvent]模块内直接创建与[!DNL Cvent]帐户的连接。

1. 在任意[!DNL Cvent]模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
1. 选择要连接的区域。

   * [!UICONTROL 北美]
   * [!UICONTROL 欧洲]
   * [!UICONTROL 沙盒]

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Cvent]模块及其字段

在配置[!DNL Cvent]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Cvent]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)
* [搜索](#searches)

### 操作

* [[!UICONTROL 自定义API调用]](#create-meeting-request)
* [[!UICONTROL 读取记录]](#read-a-record)
* [[!UICONTROL 注册被邀请者]](#register-invitee)
* [[!UICONTROL 添加被邀请者]](#add-invitee)
* [[!UICONTROL 删除联系人]](#delete-contact)
* [[!UICONTROL 更新联系人]](#update-contact)
* [[!UICONTROL 创建会议请求]](#create-meeting-request)

#### [!UICONTROL 自定义API调用]

此操作模块允许您对[!DNL Cvent] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Cvent]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

模块返回a状态代码，以及API调用的标头和正文。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Cvent]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Cvent]连接到Adobe Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">操作</td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">正文(XML)</td> 
   <td> <p>输入或映射API调用的正文。 必须只包含XML。 模块将自动包含身份验证标头。 </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

此操作模块读取有关特定记录的信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Cvent]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Cvent]连接到Adobe Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL记录类型]</p> </td> 
   <td>选择要读取的记录的项目类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL联系人] / [！UICONTROL事件] / [！UICONTROL邀请者ID]</td> 
   <td> <p>输入或映射要读取的项目的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出]</td> 
   <td> <p>选择要包含在模块输出中的字段。 根据您选择的项目类型，字段可用。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 注册被邀请者]

此操作模块为事件注册被邀请者。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Cvent]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Cvent]连接到Adobe Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>被邀请者ID</p> </td> 
   <td> <p>输入或映射要注册事件的被邀请者的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">事件ID</td> 
   <td> <p>输入或映射要为其注册被邀请人的事件的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 添加被邀请者]

此操作模块邀请联系人参加活动。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Cvent]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Cvent]连接到Adobe Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL联系人ID]</p> </td> 
   <td> <p>输入或映射要添加到事件的联系人ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL事件ID]</td> 
   <td> <p>输入或映射您要将联系人添加到的事件的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除联系人]

此操作模块删除Cvent中的单个联系人。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Cvent]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Cvent]连接到Adobe Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL联系人ID]</td> 
   <td> <p>输入或映射要删除的联系人的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新联系人]

此操作模块使用其ID更新现有联系人。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Cvent]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Cvent]连接到Adobe Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL联系人ID]</p> </td> 
   <td> <p>输入或映射要更新的联系人ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL字段]</td> 
   <td> <p>选择要为其输入信息的字段，然后为这些字段填写所需的值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL自定义字段]</td> 
   <td> <p>选择要为其输入信息的字段，然后为这些字段填写所需的值。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建会议请求]

此操作模块会将会议请求添加到您的帐户。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Cvent]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Cvent]连接到Adobe Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL表单ID]</p> </td> 
   <td> <p>输入或映射要用于创建新会议请求的表单ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL会议请求字段]</td> 
   <td> <p>选择要为其输入信息的会议请求字段，然后填写这些字段的所需值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL事件请求字段]</td> 
   <td> <p>选择您要为其输入信息的事件请求字段，然后填写这些字段的所需值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL RFP请求字段]</td> 
   <td> <p>选择要为其输入信息的建议请求字段，然后填写这些字段的所需值。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL 列出记录]

此搜索模块可检索有关特定类型的所有记录的信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Connection]</p> </td> 
   <td> <p>有关将[!DNL Cvent]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref">将[!DNL Cvent]连接到Adobe Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL记录类型]</p> </td> 
   <td> <p>选择要列出的记录类型。</p> 
    <ul> 
     <li> <p>[!DNL Cvent]帐户中的所有事件</p> </li> 
     <li> <p>事件的所有会话</p> </li> 
     <li> <p>某个活动的所有被邀请者</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL事件ID]</td> 
   <td> <p>如果您要列出被邀请者或会话，请输入或映射与这些被邀请者或会话关联的事件ID。</p> </td> 
  </tr> 
 </tbody> 
</table>
