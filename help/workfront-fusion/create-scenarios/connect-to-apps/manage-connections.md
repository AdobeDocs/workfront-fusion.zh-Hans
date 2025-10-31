---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: connections-annd-webhooks
title: 管理连接
description: 对于大多数应用程序，必须创建一个连接，Adobe Workfront Fusion才能通过该连接根据特定场景的设置与给定的第三方服务进行通信。
author: Becky
feature: Workfront Fusion
exl-id: 26d7caad-8e12-4f04-ac7c-f71686c90ee6
source-git-commit: 93d06cb917680f9cabc1bad6be0f9cd843449d07
workflow-type: tm+mt
source-wordcount: '583'
ht-degree: 1%

---

# 管理连接

连接表示Fusion用于访问应用程序的授权和权限。 您可以为每个应用程序创建一个或多个连接，并可以在多个模块或方案中使用相同的连接。

您可以在“连接”区域管理这些连接。

有关连接的详细信息，请参阅[连接概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md)。

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
   <p>基于连接器（旧版）：要连接到Workfront产品系列之外的应用程序，您必须具有Workfront Fusion for Work Automation and Integration </p>
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

## 查看和管理连接

您可以从“连接”区域管理所有连接。

>[!NOTE]
>
>连接由团队拥有。 如果找不到要查找的连接，请检查您查看的是正确的团队。
>
>要选择新团队，请单击左侧导航中的团队名称并选择新团队。

1. 要打开“连接”区域，请在左侧导航中单击&#x200B;**连接** ![连接图标](assets/connections-icon.png)。
1. 找到要管理的连接，然后在该连接的行中执行以下一个或多个步骤。
1. （可选）通过单击&#x200B;**环境**&#x200B;和&#x200B;**类型**&#x200B;下拉列表并选择一个选项来分配环境和连接类型。
1. （可选）要查看为Workfront Fusion提供的连接权限，请单击“查看”图标![查看该连接的连接权限](assets/view-connection-permissions.png)。
1. （可选）要重命名连接，请突出显示连接名称并键入新名称。
1. （可选）要重新授权连接，请选中连接旁边的复选框，然后单击屏幕底部附近的&#x200B;**重新授权**。
1. （可选）要删除连接，请选中该连接旁边的复选框，单击屏幕底部附近的&#x200B;**删除**，然后单击&#x200B;**确定吗？**。
1. （可选）要验证是否成功建立了与服务的连接，请选中连接旁边的复选框，然后单击屏幕底部附近的&#x200B;**验证**。
1. （可选）要查看使用此连接的活动方案，请选中连接旁边的复选框，然后单击&#x200B;**获取活动方案**。 然后，您可以单击活动方案列表中的方案以转到该方案。

## 续订连接

Workfront Fusion通常可以在无限制的时间内获得对给定服务的访问权限。 某些应用程序要求在一定时间段后续订访问权限。 在这些情况下，Workfront Fusion会在访问权限到期前不久通过电子邮件通知您。

要续订连接，请执行以下操作：

1. 要打开“连接”区域，请在左侧导航中单击&#x200B;**连接** ![连接图标](assets/connections-icon.png)。
1. 找到要续订的连接。
1. 在该连接的行中，选中该连接旁边的复选框，然后单击屏幕底部附近的&#x200B;**重新授权**。

## 资源

* 有关连接元数据（如环境和类型）的详细信息，请参阅[连接元数据](/help/workfront-fusion/references/connections/connection-metadata.md)。
