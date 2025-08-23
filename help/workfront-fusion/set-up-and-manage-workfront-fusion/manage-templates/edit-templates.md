---
content-type: reference
title: 编辑模板
description: 本文介绍了如何编辑Fusion模板。
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 473dba8b-faa4-432f-9357-c2146e86b261
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# 编辑模板

Adobe Workfront Fusion模板是预建方案，旨在自动化和简化各种工作流。 这些模板可帮助您快速设置集成和自动化，而无需从头开始构建所有内容。

如果您是管理员，则有权查看、修改、重命名、发布、批准和删除其他人创建的模板。

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

For information on Adobe Workfront Fusion licenses, see [Adobe Workfront Fusion licenses](../../workfront-fusion/get-started/license-automation-vs-integration.md). -->

+++

## 以管理员身份编辑Workfront Fusion模板

1. 在左侧导航面板中单击&#x200B;**[!UICONTROL 管理]**&#x200B;以打开[!UICONTROL 管理]区域。
1. 单击左侧导航面板中的&#x200B;**[!UICONTROL 所有模板]**。
1. 单击要编辑的模板右侧的&#x200B;**[!UICONTROL 详细信息]**。
1. （可选）通过单击右上角的&#x200B;**选项**&#x200B;并选择&#x200B;**重命名**&#x200B;来重命名模板。
1. （可选）要更改模板的语言，请单击&#x200B;**[!UICONTROL 创建新模板]** ![方案设置图标](assets/fusion-scenario-settings-icon.png)，然后从“语言”下拉列表中选择语言。

   >[!IMPORTANT]
   >
   >语言选择对应于系统设置中可用的语言，仅涉及公共模板的名称及其描述。 保存模板后，无法更改模板语言。

1. （可选）要编辑模板说明，请单击&#x200B;**[!UICONTROL 设置模板]** ![方案设置图标](assets/fusion-scenario-settings-icon.png)，然后输入说明。
1. 使用与创建标准方案相同的方式添加或编辑应用程序、模块和工具。

   若要向模块添加上下文帮助，请参阅本文中的[设置[!UICONTROL 向导]功能](#set-up-wizard-functionality)。

   <!--For more information on building a scenario, see [Create a scenario in Adobe Workfront Fusion](../../../workfront-fusion/scenarios/create-a-scenario.md).-->

   >[!NOTE]
   >
   >如果您的模板包含需要添加连接、凭据或其他隐私敏感信息的模块，则不会与模板用户共享此信息。

1. （可选）单击&#x200B;**[!UICONTROL 运行一次]**&#x200B;以测试模板。
1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;图标![保存图标](assets/save-icon.png)。


## 设置[!UICONTROL 向导]功能

[!DNL Workfront Fusion template] [!UICONTROL 向导]允许您向模板的将来用户提供与模块中使用的特定字段相关的说明或信息。

1. 单击添加到模板的模块以查看模块的字段。
1. 找到要添加[!UICONTROL 向导]信息的字段，并在该字段下方启用&#x200B;**[!UICONTROL 在向导]**&#x200B;中使用。
1. 在[!UICONTROL 帮助]字段中输入您希望用户可见的信息。
1. （可选）要允许用户在使用模板时查看此文本，请启用&#x200B;**[!UICONTROL 使用作为默认值]**。
1. 对要为其提供信息的每个字段重复步骤2 - 4。
1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;以保存更改并关闭模块。

发布过程与标准用户的情况相同。 有关信息，请参阅[发布和共享模板](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md)部分以了解更多详细信息。

## 模板状态

您可以在模板页面上的模板名称下查看状态。

可以使用以下状态：

* **[!UICONTROL 私有]**：此模板仅对模板作者及其团队可见。
* **[!UICONTROL 已发布]**：此模板仅对模板作者及其团队可见。 发布后，您可以根据需要发送模板以供审批。 您还可以复制可共享链接。
* **[!UICONTROL 已批准]**：此模板在[!UICONTROL 公共模板]选项卡中对所有Workfront Fusion用户可见。 您还可以通过单击屏幕右上角的[!UICONTROL 选项]来复制可共享链接。

您还可以从[!UICONTROL 团队模板]选项卡中检查状态。 如果模板已发布，则模板名称的右侧将显示一个图标。

* **眼睛图标**：模板已发布；该模板对团队可见。
* **黄色复选标记图标**：模板已发布；该模板仅对团队可见；它正在等待批准以添加到“公共模板”选项卡中。
* **绿色复选标记图标**：该模板在“公共模板”选项卡中可用，并且对于任何Workfront Fusion用户均可见。 它还在[!UICONTROL 团队模板]选项卡中可见。 模板作者或其团队成员仍可以编辑它。

没有图标的模板具有[!UICONTROL 私有]状态。 它们未发布，仅对团队可见。

## 查找模板的SVG信息

1. 在左侧导航面板中单击&#x200B;**[!UICONTROL 管理]**&#x200B;以打开[!UICONTROL 管理]区域。
1. 在左侧导航面板中单击&#x200B;**[!UICONTROL 模板]**。
1. 单击要为其查找信息的模板。
1. 单击右上角的&#x200B;**选项**。
1. 选择&#x200B;*SVG关系图*。

在这里，您可以查看SVG图表和SVG代码。
