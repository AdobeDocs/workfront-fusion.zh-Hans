---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: 管理锁定的方案
description: 管理 [!DNL Adobe Workfront Fusion]中的锁定方案
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 1%

---

# 管理锁定的方案

在某些情况下，某个方案可能会暂时锁定在[!DNL Workfront Fusion]中。 锁定方案将在2-4小时内自动解锁。 您可以手动解锁场景，但通常不建议这样做。

锁定方案的原因有很多：

* Workfront Fusion不支持并行处理计划场景。 这些方案在方案执行开始时会被锁定，在完成时会被解锁。 如果执行中断，场景可能无法解锁。 当用户手动强制停止场景或出现系统问题时，可能会发生这种情况。

* Workfront Fusion工程团队可能会锁定场景，因为它会导致性能或其他问题。

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

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++


## 解锁锁定的方案

锁定的方案将从锁定的时间起2 - 4小时解锁。 您可以在计划自动解锁方案之前手动解锁该方案。

>[!WARNING]
>
>手动解锁场景可能会导致场景执行出错。 我们建议仅在场景由于设计场景时运行和停止执行而被锁定时，手动解锁场景。 在其他情况下，我们建议您等待场景自动解锁。


要手动解锁锁定的方案，请执行以下操作：

1. 转至锁定方案的“方案详细信息”页面。
1. 单击屏幕右上角的&#x200B;**[!UICONTROL Options]**。
1. 选择 **[!UICONTROL Unlock execution]**。
1. 单击 **[!UICONTROL Unlock]**。
   ![解锁方案](assets/unlock-scenario.png)
