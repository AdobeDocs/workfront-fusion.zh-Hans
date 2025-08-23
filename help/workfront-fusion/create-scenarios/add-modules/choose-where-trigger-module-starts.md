---
title: 选择触发器模块的启动位置
description: 某些触发器模块允许您选择希望开始捆绑包检索的第一个捆绑包。
author: Becky
feature: Workfront Fusion
exl-id: 83628fa5-82e2-4f67-bfed-70a4c3c19f7f
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---

# 选择触发器模块的启动位置

某些触发器模块允许您选择希望开始捆绑包检索的第一个捆绑包。

您还可以指定是在特定日期之后检索所有捆绑包，还是仅检索捆绑包。

有关触发器模块的更多信息，请参阅文章模块概述中的[触发器模块](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules)部分。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前： [!UICONTROL Work]或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新：</p> <ul><li>[!UICONTROL Select]或[!UICONTROL Prime] Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li><li>[!UICONTROL Ultimate] Workfront计划：包括Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 选择触发器模块的启动位置

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要选择触发器开始位置的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 配置并保存触发器模块。

   或

   右键单击触发器模块的图标，然后选择&#x200B;**选择开始位置**。

   ![选择开始位置](assets/choose-where-to-start.png)

1. 在出现的&#x200B;**[!UICONTROL 选择开始位置]**&#x200B;框中选择一个选项。

   显示的选项取决于给定服务的可能性。 它们可能包括：

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody>
    <tr>
    <td>[!UICONTROL 从现在开始]（默认）</td>
    <td>在选择此选项后检索添加或更新的所有包（取决于设置）</td>
    </tr>
     <tr>
    <td>[!UICONTROL 自特定日期起]</td>
    <td>检索在指定日期和时间之后添加或更新的所有包（取决于设置）</td>
      </tr>
      <tr>
    <td>[!UICONTROL All]</td>
    <td>检索所有可用的包</td>
     </tr>
      <tr>
    <td>[!UICONTROL 手动选择]</td>
    <td>允许您选择从中开始检索包的第一个包</td>
     </tr>
     </tbody>
   </table>
