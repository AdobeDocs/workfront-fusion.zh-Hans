---
title: 为没有连接器的Web服务配置webhook
description: 如果Web服务当前在Workfront Fusion中没有专用连接器，但它支持发送Webhook，则可以使用自定义Webhook模块作为即时触发器将该服务添加到场景中。
author: Becky
feature: Workfront Fusion
exl-id: 51ef13fb-2978-4927-8d5f-7d83995f11e0
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---

# 为没有连接器的Web服务配置webhook

如果Web服务当前在Workfront Fusion中没有专用连接器，但它支持发送Webhook，则可以使用自定义Webhook模块作为即时触发器将该服务添加到场景中。 此过程称为接收webhook，它需要在您连接到的应用程序侧进行一些配置。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包 
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
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront计划：包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 接收webhook

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要添加webhook的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 添加&#x200B;**Webhook >自定义webhook**&#x200B;模块以开始您的方案。
1. 单击Webhook字段旁边的&#x200B;**添加**。
1. 在显示的框中输入&#x200B;**Webhook名称**
1. （可选）配置webhook。

   有关说明，请参阅[Webhooks](/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md)。

1. 单击&#x200B;**保存**。

1. 单击&#x200B;**将地址复制到剪贴板**，然后单击&#x200B;**确定**。

1. 登录到Web服务，并在该处执行以下操作：

   1. 在Web服务的“设置”区域中，创建一个webhook。

      具体说明取决于应用程序。 我们建议在应用程序的文档中搜索“创建webhook”。
   1. 在步骤3中将复制的地址粘贴到剪贴板。
   1. 选择将触发webhook的事件。

1. 运行方案。

   当发生一个或多个事件时，将触发自定义webhook模块，并且场景将运行。
