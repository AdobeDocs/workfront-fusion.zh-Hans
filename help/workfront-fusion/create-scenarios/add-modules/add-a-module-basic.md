---
title: 将模块添加到方案
description: 本文介绍了将模块添加到场景的基本过程。
author: Becky
feature: Workfront Fusion
exl-id: f3757468-3e11-4862-a83e-ed447805545b
source-git-commit: 62b09469c1d85fd2bd1f154cde339cc4a10fc34a
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# 将模块添加到方案

场景由一系列模块组成，这些模块指示应如何在应用程序内转换数据或在应用程序和Web服务之间传输数据。 您可以通过添加和配置模块来构建模块。

本文介绍了将模块添加到场景的基本过程。 有关添加方案的详细说明，请参阅[添加模块：文章索引](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md)下的其他文章。

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
   <p>新：</p> <ul><li>[！UICONTROL Select]或[！UICONTROL Prime] [!DNL Workfront]计划：您的组织必须购买[!DNL Adobe Workfront Fusion]。</li><li>已包含[！UICONTROL Ultimate] [!DNL Workfront]计划： [!DNL Workfront Fusion]。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买[!DNL Adobe Workfront Fusion]。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 将第一个模块添加到方案

方案的第一个模块通常是触发器模块。

有关触发器模块的详细信息，请参阅文章模块概述中的[触发器模块](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules)。

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 通过单击屏幕右上角的&#x200B;**创建新方案**&#x200B;开始创建方案。

   场景编辑器将打开，其中包含占位符（问号）模块和可用连接器的列表。

   ![占位符模块](assets/placeholder-module.png)

1. 选择将启动此方案的连接器或webhook。 您可以在列表的搜索栏中键入连接器的名称，以筛选列表。
1. 配置模块。

   有关配置特定模块的说明，请参阅[Fusion应用程序及其模块引用中列出的选定应用程序的文章：文章索引](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)。

>[!NOTE]
>
>如果您已从场景中删除第一个模块并想要替换它，请单击占位符（问号）模块以打开连接器列表。

## 向方案添加其他模块

1. 如果您不在要添加模块的方案的方案编辑器中，请单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 单击方案上的任意位置以进入方案编辑器。
1. 若要将某个模块添加到另一个模块，请将鼠标悬停在该模块的右侧句柄上，以便在该句柄之后添加模块，然后在该模块出现时单击&#x200B;**添加另一个模块**。

   此时将打开连接器列表，其中显示了场景中已使用的任何连接器。

1. （可选）要选择其他连接器，请单击&#x200B;**在列表中添加其他模块**，然后选择连接器。 您可以在列表的搜索栏中键入连接器的名称，以筛选列表。
1. 配置模块。

   有关配置特定模块的说明，请参阅[Fusion应用程序及其模块引用中列出的选定应用程序的文章：文章索引](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)。

## 在场景中的现有模块之间插入模块

1. 如果您不在要添加模块的方案的方案编辑器中，请单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击要插入模块的模块之间的点状路径。
1. 在出现的菜单中，选择&#x200B;**添加模块**。

此时将打开连接器列表，其中显示了场景中已使用的任何连接器。

1. （可选）要选择其他连接器，请单击&#x200B;**在列表中添加其他模块**，然后选择连接器。 您可以在列表的搜索栏中键入连接器的名称，以筛选列表。
1. 配置模块。

   有关配置特定模块的说明，请参阅[Fusion应用程序及其模块引用中列出的选定应用程序的文章：文章索引](/help/workfront-fusion/references/apps-and-modules/apps-and-modules-toc.md)。

>[!NOTE]
>
>要创建指向特定模块的链接，请在查看以下页面时将`?moduleId=<module-id>`添加到URL：
>
>* 方案编辑页面（URL以`/edit`结尾）
>* 特定场景执行（URL以`/logs/<log-id>`结尾）
>
>查看场景时，`<module-id>`引用模块标签旁边的数字。
>
>这在调试方案或复制模块配置时可能很有用。
