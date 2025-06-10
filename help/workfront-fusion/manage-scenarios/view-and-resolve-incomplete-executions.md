---
title: 查看并解决未完成的执行
description: '[!UICONTROL 未完成的执行]文件夹存储由于错误未成功完成的场景执行。 可以手动或自动解决每个存储的不完整执行。'
author: Becky
feature: Workfront Fusion
exl-id: 8891b4d7-a39a-4f14-8521-8c2ca186ca6e
source-git-commit: ad304117fb6e9d1320b8e50d71a162609dc6e6f4
workflow-type: tm+mt
source-wordcount: '649'
ht-degree: 5%

---

# 查看并解决未完成的执行

[!UICONTROL 未完成的执行]文件夹存储由于错误未成功完成的场景执行。 可以手动或自动解决每个存储的不完整执行。

>[!NOTE]
>
>默认情况下，不完整执行的存储被禁用。 要启用它，请在场景高级设置中启用[!UICONTROL 允许存储未完成的执行]选项。
>
>有关方案设置的详细信息，请参阅[配置方案设置](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)。

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
   <td> <p>新文档： [！UICONTROL Standard]</p><p>或</p><p>当前： [！UICONTROL Work]或更高版本</p> </td> 
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
   <p>新增：</p> <ul><li>[！UICONTROL Select]或[！UICONTROL Prime] [!DNL Workfront]计划：您的组织必须购买[!DNL Adobe Workfront Fusion]。</li><li>已包含[！UICONTROL Ultimate] [!DNL Workfront]计划： [!DNL Workfront Fusion]。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买[!DNL Adobe Workfront Fusion]。</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">访问级别配置*</td> 
   <td> 
     <p>您必须是组织的[!DNL Workfront Fusion]管理员。</p>
     <p>您必须是团队的[!DNL Workfront Fusion]管理员。</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 查看未完成的执行

如果模块在操作过程中遇到错误，则会将新的未完成执行添加到“未完成执行”文件夹。 每个不完整的执行都包含场景的Blueprint以及可以映射到失败模块的所有捆绑包。 通过单击场景详细信息页面上的[!UICONTROL 未完成的执行]选项卡，可以打开未完成的执行列表。

<!--

![Incomplete executions tab](assets/incomplete-executions-tab-350x102.png)

-->

有关详细信息，请参阅本文中导致不完整执行的[错误](#errors-resulting-into-incomplete-executions)。

>[!NOTE]
>
>每个组织未解决的执行文件夹当前的大小限制为500 MB。 如果贵组织超过此限制，您可能会看到以下错误：
>
>`"There is NOT ENOUGH SPACE to add a bundle to the IEQ. The reason is: Too many incomplete executions."`
>
>有关详细信息，请参阅配置方案设置一文中的[启用数据丢失](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss)。


## 从“未完成的执行”选项卡中解决未完成的执行

在存储新的未完成执行时，您可以按如下方式解决它：

1. 打开受影响的方案。
1. 单击&#x200B;**[!UICONTROL 未完成的执行]**&#x200B;选项卡。
1. 找到要解析的未完成执行，然后单击&#x200B;**[!UICONTROL 详细信息]**。
1. 打开模块的日志，其中显示了模块的所有操作。
1. 找到失败的操作，然后单击&#x200B;**[!UICONTROL 解决]**：

   ![解决按钮](assets/resolve-btn-350x188.png)



## 从“历史记录”选项卡中解决未完成的执行

如果您想在尝试解析未完成的执行之前查看所有模块操作的日志，可以从[!UICONTROL History]文件夹解析未完成执行：

1. 打开受影响的方案。
1. 单击&#x200B;**[!UICONTROL 历史记录]**&#x200B;选项卡。
1. 找到方案的失败执行，然后单击&#x200B;**[!UICONTROL 详细信息]**。
1. 打开模块的日志，其中显示了模块的所有操作。
1. 找到失败的操作，然后单击&#x200B;**[!UICONTROL 解决]**：

   ![解决按钮](assets/resolve-btn-350x188.png)

## 与未完成执行相关的选项

[!UICONTROL 场景设置]面板中的以下选项确定是否以及如何存储未完成的执行：

* 允许存储未完成的执行
* 顺序处理
* 启用数据丢失

有关这些选项的详细信息，请参阅[配置方案设置](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)。

## 导致执行不完整的错误

有几类错误会导致存储不完整的执行。 这些可能包括：

* 验证错误由不完整或错误的数据引起，主要原因是需要缺少项目才能成功处理通过模块的所有数据。
* 由于临时或长期连接故障（例如，在连接电子邮件或远程FTP服务器期间）导致最终目标不可用而发生错误。

如果场景中的第一个模块发生错误，则执行会立即停止，并且不会存储未完成的执行。

如果任何其他模块发生错误，并且没有附加错误处理程序路由，则会出现以下情况之一：

* 为以下错误类型存储具有自动重试的不完整执行记录：

   * `ConnectionError`
   * `RateLimitError`
   * `OutOfSpaceError`
   * `ModuleTimeoutError`

* 为以下错误类型存储了未完成的执行记录（没有自动重试）：

   * `DataError`
   * `InvalidConfigurationError`
   * `InvalidAccessTokenError`
   * `UnexpectedError`
   * `MaxFileSizeExceededError`
   * `MaxResultsExceededError`

* 如果错误类型不是上述类型，则执行失败。
