---
title: 查看和管理时区
description: 了解如何在Adobe Workfront Fusion中查看和管理时区设置。
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9910d9b4-5a7a-4f4a-9e66-8600d3b6c785
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: 39c34b17e766678e187837e07c90b67f365a4f1d
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 17%
---
# 查看和管理时区

Adobe Workfront Fusion包括组织和用户级别的时区控件。

* 组织时区：方案使用组织时区来确定计划事件何时发生。

* 用户时区：用户时区确定显示给用户的时间。

>[!BEGINSHADEBOX]

示例：

组织位于纽约市，组织时间设置为UTC-5（美国/纽约）。 方案A归该组织所有，计划于每天上午9:00运行。 场景在纽约时区的上午9:00运行。

此组织中的用户住在洛杉矶，并将其用户时区设置为UTC-8 （美国/洛杉矶）。 当此用户查看方案A的方案执行历史记录时，他们会看到方案在上午6:00运行。 即使场景按照纽约时间运行，用户仍会看到时间转换为他们自己的时区。

>[!ENDSHADEBOX]



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
  <tr> 
   <td role="rowheader">访问级别</td> 
   <td> 您必须是组织的所有者或管理员才能编辑该组织的时区。 </td>
   </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 查看和管理用户时区

1. 在Fusion中，单击屏幕右上角的Adobe配置文件图标。
1. 在打开的菜单中，选择&#x200B;**Fusion配置文件**。
1. 选择&#x200B;**时区选项**选项卡。 选项卡直接位于您的名称下。
此时会打开“时区选项”列表。
1. 在“时区选项”列表的Web区域中，找到您的姓名。

   您当前的用户时区设置显示在您姓名的右侧。
1. 要编辑时区，请单击时区旁边的编辑![编辑时区](assets/edit-timezone-icon.png)。
1. 在“更改详细信息”窗口的&#x200B;**时区**&#x200B;字段中，选择要为自己设置的时区。
1. 单击&#x200B;**保存**。


## 查看和管理组织的时区

>[!NOTE]
>
>您必须是组织的所有者或管理员才能编辑该组织的时区。

1. 在Fusion中，单击屏幕右上角的Adobe配置文件图标。
1. 在打开的菜单中，选择&#x200B;**Fusion配置文件**。
1. 选择&#x200B;**时区选项**选项卡。 选项卡直接位于您的名称下。
此时会打开“时区选项”列表。
1. 在“时区选项”列表的“方案”区域中，找到要查看或管理其时区的组织。

   组织的当前时区设置显示在组织名称的右侧。
1. 要编辑时区，请单击时区旁边的编辑![编辑时区](assets/edit-timezone-icon.png)。
1. 在“更改详细信息”窗口的&#x200B;**时区**&#x200B;字段中，选择要为组织设置的时区。
1. 单击&#x200B;**保存**。


