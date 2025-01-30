---
title: 创建新模板
description: 您可以在 [!DNL Adobe] Workfront Fusion中创建新场景模板。
author: Becky
feature: Workfront Fusion
exl-id: 9cb9bd04-e9ae-4162-a1b9-d71566582b7a
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# 创建新模板

您可以在[!DNL Adobe] Workfront Fusion中创建新场景模板。

>[!TIP]
>
>创建新模板之前，您可以检查[!UICONTROL Public templates]选项卡，以确保要创建的模板尚不可用。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证</td> 
   <td> <p>新增： [!UICONTROL Standard]</p><p>或</p><p>当前： [!UICONTROL Work]或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>[!UICONTROL Select] 或[!UICONTROL Prime] [!DNL Workfront]计划：您的组织必须购买[!DNL Adobe Workfront Fusion]。</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 计划： [!DNL Workfront Fusion]已包括在内。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买[!DNL Adobe Workfront Fusion]。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 创建新模板

您可以在一个与构建方案类似的过程中构建模板。 Fusion管理员还可以从现有方案创建模板。

* [构建模板](#build-a-template)
* [从场景创建模板](#create-a-template-from-a-scenario)

### 构建模板

1. 在左侧导航面板中单击&#x200B;**[!UICONTROL Templates]** ![模板图标](assets/templates-icon.png)。
1. 单击右上角的&#x200B;**[!UICONTROL Create a new template]**。
1. （可选）通过替换左上角的默认&#x200B;**[!UICONTROL New template name]**&#x200B;来重命名模板。
1. （可选）要更改模板的语言，请单击&#x200B;**[!UICONTROL Set up a template]** ![方案设置图标](assets/scenario-settings-icon.png)，然后从“语言”下拉列表中选择语言。

   >[!IMPORTANT]
   >
   >语言选择对应于系统设置中可用的语言，仅涉及公共模板的名称及其描述。 保存模板后，无法更改模板语言。

1. （可选）要输入模板的说明，请单击&#x200B;**[!UICONTROL Set up a template]** ![方案设置图标](assets/scenario-settings-icon.png)并输入说明。
1. 使用与将模块添加到方案相同的流程添加应用程序、模块和工具。

   有关说明，请参阅[添加模块](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md)下的文章。

   若要向模块添加上下文帮助，请参阅本文中的[设置向导功能](#set-up-wizard-functionality)。

   有关构建方案的详细信息，请参阅用于创建方案的[工作流](/help/workfront-fusion/create-scenarios/plan-a-scenario/create-a-scenario-workflow.md)。

   >[!NOTE]
   >
   >如果您的模板包含需要添加连接、凭据或其他隐私敏感信息的模块，则不会与模板用户共享此信息。

1. （可选）单击&#x200B;**[!UICONTROL Run once]**&#x200B;以测试您的模板。
1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;图标![保存图标](assets/save-icon.png)以保存模板。

保存模板后，您的团队成员将能够看到该模板。 如果您希望可以在团队外部访问模板，则必须提交请求以批准和发布模板。 该请求将发送到Adobe Workfront Fusion团队以供审批。 在模板获得批准后，您团队之外的其他人可以访问该模板。

有关发布模板的信息，请参阅[Publish和共享 [!DNL Adobe Workfront Fusion] 模板](/help/workfront-fusion/create-and-manage-templates/publish-and-share-fusion-templates.md)。

### 从场景创建模板

>[!NOTE]
>
>您必须是Fusion管理员才能从场景创建模板。

1. 单击左侧面板中的&#x200B;**[!UICONTROL Scenarios]**&#x200B;选项卡。
1. 选择要从中创建模板的方案。
1. 单击页面右上角附近的&#x200B;**管理员**&#x200B;下拉菜单。
1. 选择&#x200B;**克隆作为模板**。

   方案将被复制到新模板页面中。
1. （可选）通过替换左上角的默认&#x200B;**[!UICONTROL New template name]**&#x200B;来重命名模板。
1. （可选）要更改模板的语言，请单击&#x200B;**[!UICONTROL Set up a template]** ![方案设置图标](assets/scenario-settings-icon.png)，然后从“语言”下拉列表中选择语言。

   >[!IMPORTANT]
   >
   >语言选择对应于系统设置中可用的语言，仅涉及公共模板的名称及其描述。 保存模板后，无法更改模板语言。

1. （可选）要输入模板的说明，请单击&#x200B;**[!UICONTROL Set up a template]** ![方案设置图标](assets/scenario-settings-icon.png)并输入说明。
1. 使用与将模块添加到方案相同的流程，根据需要编辑应用程序、模块和工具。

   有关说明，请参阅[添加模块](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md)下的文章。

   若要向模块添加上下文帮助，请参阅本文中的[设置[!UICONTROL Wizard]功能](#set-up-wizard-functionality)。

   >[!NOTE]
   >
   >如果您的模板包含需要添加连接、凭据或其他隐私敏感信息的模块，则不会与模板用户共享此信息。

1. （可选）单击&#x200B;**[!UICONTROL Run once]**&#x200B;以测试您的模板。
1. 单击&#x200B;**[!UICONTROL Save]**&#x200B;图标![保存图标](assets/save-icon.png)。

## 设置[!UICONTROL Wizard]功能 {#set-up-wizard-functionality}

[!DNL Workfront Fusion template] [!UICONTROL Wizard]允许您向模板的将来用户提供与模块中使用的特定字段相关的说明或信息。

1. 创建模板时，单击添加到模板的模块以查看模块的字段。
1. 找到要添加[!UICONTROL Wizard]信息的字段，并为该字段启用&#x200B;**[!UICONTROL Use in Wizard]**。
1. 在[!UICONTROL Help]字段中输入您希望用户可见的信息。
1. （可选）要允许用户在使用模板时查看此文本，请启用&#x200B;**[!UICONTROL Use as default value]**。
1. 对要为其提供信息的每个字段重复步骤2 - 4。
1. 单击&#x200B;**[!UICONTROL OK]**&#x200B;以保存更改并关闭模块。
