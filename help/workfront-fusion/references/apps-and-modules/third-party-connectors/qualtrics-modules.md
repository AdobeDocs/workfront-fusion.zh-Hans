---
title: Qualtrics模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Qualtrics的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 80b441b7-c808-4c4f-b9ff-d614650dbb73
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 1%

---

# Qualtrics模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Qualtrics]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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
   <p>基于连接器（旧版）：用于工作自动化和集成的Workfront Fusion </p>
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

## 先决条件

要使用[!DNL Qualtrics]模块，您必须具有[!UICONTROL Qualtrics]帐户。

## Qualtrics API信息

Qualtrics连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td> https://{{connection.dataCenterCode}}.qualtrics.com/API/v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.1.1</td> 
  </tr>
 </tbody> 
 </table>

## 正在将[!DNL Qualtrics]连接到Workfront Fusion

您可以在[!DNL Qualtrics]Qualtrics[!UICONTROL 模块内直接创建与]帐户的连接。

1. 在任何[!UICONTROL Qualtrics]模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
1. 输入以下信息：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL连接名称]</p> </td> 
      <td> <p>输入新连接的名称。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL数据中心ID] </td> 
      <td>使用格式<code>&lt;Data Center ID>.qualtrics.com</code>。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL API Key]</td> 
      <td>要查找API密钥，请参阅[!DNL Qualtrics]文档。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Qualtrics]模块及其字段

以下模块可用于[!DNL Qualtrics]连接器：

* [!UICONTROL 观看新的调查回复]
* [!UICONTROL 创建目录联系人]
* [!UICONTROL 删除目录联系人]
* [!UICONTROL 获取目录联系人]
* [!UICONTROL 更新目录联系人]
* [!UICONTROL 通过短信创建新的调查分发]
* [!UICONTROL 通过电子邮件分发调查]
* [!UICONTROL 进行API调用]
* [!UICONTROL 列出目录联系人]
