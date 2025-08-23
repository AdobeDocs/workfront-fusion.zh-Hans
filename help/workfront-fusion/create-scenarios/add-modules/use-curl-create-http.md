---
title: 使用cURL添加HTTP模块
description: 您可以将cURL请求粘贴到场景中，然后Fusion会创建根据cURL请求配置的HTTP模块。
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 2%

---

# 使用cURL添加HTTP模块

您可以将cURL请求粘贴到场景中，然后Fusion会创建根据cURL请求配置的HTTP模块。

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
   <td> <p>新增：标准</p><p>或</p><p>当前： [！UICONTROL Work]或更高版本</p> </td> 
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
   <p>新：</p> <ul><li>[！UICONTROL Select]或[！UICONTROL Prime] Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li><li>[！UICONTROL Ultimate] Workfront计划：包括Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 从cURL请求创建HTTP模块


要使用cURL创建HTTP模块，请执行以下操作：

1. 在Fusion之外创建cURL请求的文本，例如在文本编辑器中。
1. 将cURL请求复制到剪贴板。
1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要创建模块的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 右键单击方案编辑器中的任何空白区域，然后选择&#x200B;**粘贴**。

   或

   按Ctrl + V (Windows)或Cmd + V (Mac)。


   将创建HTML模块。
1. 拖动模块以将其连接到场景。

## 故障排除

如果cURL未粘贴到场景中，请检查浏览器设置以确保启用从剪贴板粘贴。
