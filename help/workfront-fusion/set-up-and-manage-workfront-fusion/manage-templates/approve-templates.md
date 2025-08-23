---
content-type: reference
title: 批准或取消批准模板
description: 本文介绍了如何批准或拒绝Fusion模板。
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: dafecd8b-96e5-46da-9ab6-15f0bc9b52a4
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---

# 批准或取消批准“公共”选项卡的模板

Adobe Workfront Fusion模板是预建方案，旨在自动化和简化各种工作流。 这些模板可帮助用户快速设置集成和自动化，而无需从头开始构建所有内容。

如果您是管理员，则可以在“公共模板”选项卡中选择是否应将某些模板与整个组织共享。

用户可以发送其为审批而创建的模板，以供在公共模板页面上共享。<!--do the have to be requested or can an admin just choose to approve?-->

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
  <col>
  <col>
  <tbody>
    <tr>
      <td role="rowheader">Adobe Workfront计划</td>
      <td><p>任何</p></td>
    </tr>
    <tr data-mc-conditions="">
      <td role="rowheader">Adobe Workfront许可证</td>
      <td><p>新增：标准</p><p>或</p><p>当前： [！UICONTROL Work]或更高版本</p></td>
    </tr>
    <tr>
      <td role="rowheader">Adobe Workfront Fusion许可证**</td>
      <td>
        <p>当前：无Workfront Fusion许可证要求。</p>
        <p>或</p>
        <p>旧版：任意</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">产品</td>
      <td>
        <p>新：</p>
        <ul>
          <li>[！UICONTROL Select]或[！UICONTROL Prime] Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li>
          <li>[！UICONTROL Ultimate] Workfront计划：包括Workfront Fusion。</li>
        </ul>
        <p>或</p>
        <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
      </td>
    </tr>
  </tbody>
</table>

<!--
For more detail about the information in this table, see [Access requirements in Workfront documentation](/help/quicksilver/administration-and-setup/add-users/access-levels-and-object-permissions/access-level-requirements-in-documentation.md). 

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md).-->

+++

## 批准或不批准Workfront Fusion模板

批准模板可使其在[!UICONTROL 公共模板]选项卡中可见并对所有用户可用。

不批准模板会将其从[!UICONTROL 公共模板]选项卡中删除，并使其仅对创建该模板的团队可用。

1. 在左侧导航面板中单击&#x200B;**[!UICONTROL 管理]**&#x200B;以打开[!UICONTROL 管理]区域。
1. 在左侧导航面板中单击&#x200B;**[!UICONTROL 模板]**。
1. 如果要批准模板，请单击模板右侧的&#x200B;**[!UICONTROL 批准]**。
1. 如果要取消批准模板，请单击模板右侧的&#x200B;**[!UICONTROL 取消批准]**。

>[!NOTE]
>
>如果您要批准之前已批准并编辑的模板，则第二次批准将覆盖原始模板。


## 模板状态

您可以在模板页面上的模板名称下查看状态。

可以使用以下状态：

* **[!UICONTROL 私有]**：此模板仅对模板作者及其团队可见。
* **[!UICONTROL 已发布]**：此模板仅对模板作者及其团队可见。 发布后，您可以根据需要发送模板以供审批。 您还可以复制可共享链接。
* **[!UICONTROL 已批准]**：此模板在[!UICONTROL 公共模板]选项卡中对所有Workfront Fusion用户可见。 您还可以通过单击屏幕右上角的[!UICONTROL 选项]来复制可共享链接。

您还可以从[!UICONTROL 团队模板]选项卡中检查状态。 如果模板已发布，则模板名称的右侧将显示一个图标。

* **眼睛图标**：模板已发布；该模板仅对团队可见；未发送审批请求。
* **黄色复选标记图标**：模板已发布；该模板仅对团队可见；它正在等待批准以添加到“公共模板”选项卡中。
* **绿色复选标记图标**：该模板在“公共模板”选项卡中可用，并且对于任何Workfront Fusion用户均可见。 它还在[!UICONTROL 团队模板]选项卡中可见。 模板作者或其团队成员仍可以编辑它。

没有图标的模板具有[!UICONTROL 私有]状态。 它们未发布，仅对团队可见。


<!--

## Questions about how this works

Editing

1. If an admin edits a template, do they have to publish again? ... Do they have to approve again?
1. What does publishing actually do?
1. Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
1. What is the admin approving? Does a user have to submit it for approval? 



What does "Publishing" mean?
What does "Approving" mean?
If an admin edits a template, do they have to publish again? ... Do they have to approve again?
Does a user have to submit for approval to share on the Public tab or can admin go through and approve/reject which ones they want? 
What is the admin approving? Does a user have to submit it for approval?

-->
