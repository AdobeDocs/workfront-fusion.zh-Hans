---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: 管理锁定的场景
description: 在Adobe Workfront Fusion中管理锁定方案
author: Becky
feature: Workfront Fusion
exl-id: b5e92bdc-cc1d-4b22-8c5f-42cc279d5590
TQID: https://experienceleague.adobe.com/1eVGWr4SwutYzNmCKB62CCWbQ6ExdXtpjC5BORh-kxo
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 327
ht-degree: 29%

---

# 管理锁定的场景

在某些情况下，场景可能会暂时锁定Workfront Fusion。 锁定方案将在2-4小时内自动解锁。 您可以手动解锁场景，但通常不建议这样做。

锁定方案的原因有很多：

* Workfront Fusion不支持并行处理计划场景。 这些方案在方案执行开始时会被锁定，在完成时会被解锁。 如果执行中断，场景可能无法解锁。 当用户手动强制停止场景或出现系统问题时，可能会发生这种情况。

* Workfront Fusion工程团队可能会锁定场景，因为它会导致性能或其他问题。

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

## 解锁锁定的方案

锁定的方案将从锁定的时间起2 - 4小时解锁。 您可以在计划自动解锁方案之前手动解锁该方案。

>[!WARNING]
>
>手动解锁场景可能会导致场景执行出错。 我们建议仅在场景由于设计场景时运行和停止执行而被锁定时，手动解锁场景。 在其他情况下，我们建议您等待场景自动解锁。


要手动解锁锁定的方案，请执行以下操作：

1. 转至锁定方案的“方案详细信息”页面。
1. 单击屏幕右上角的&#x200B;**[!UICONTROL 选项]**。
1. 选择&#x200B;**[!UICONTROL 解锁执行]**。
1. 单击&#x200B;**[!UICONTROL 解锁]**。
   ![解锁方案](assets/unlock-scenario.png)
