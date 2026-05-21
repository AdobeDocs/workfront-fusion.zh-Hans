---
title: Qualtrics 模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Qualtrics的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 80b441b7-c808-4c4f-b9ff-d614650dbb73
TQID: https://experienceleague.adobe.com/gbH5KTIEYyIAVMSjhmnAyuApEPu7i3eicmMvmJC-gi4
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 352
ht-degree: 59%

---

# Qualtrics 模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL Qualtrics] 的工作流，并将其连接到多个第三方应用程序和服务。

有关创建场景的说明，请参阅[创建场景：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)中的相关文章。

有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的相关文章。

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
   <td role="rowheader">Adobe Workfront Fusion 许可证</td> 
   <td>
   <p>基于操作：不需要 Workfront Fusion 许可证</p>
   <p>基于连接器（旧版）：Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

有关 Adobe Workfront Fusion 许可证的详细信息，请参阅 [Adobe Workfront Fusion 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

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
   <td><pre><code>https://&#123;&#123;connection.dataCenterCode&#125;&#125;.qualtrics.com/API/v3</code></pre></td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 版本</td> 
   <td> v3 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.1.1</td> 
  </tr>
 </tbody> 
 </table>

## 正在将[!DNL Qualtrics]连接到Workfront Fusion

您可以在[!UICONTROL Qualtrics]模块内直接创建与[!DNL Qualtrics]帐户的连接。

1. 在任何[!UICONTROL Qualtrics]模块中，单击[!UICONTROL 连接]字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 输入以下信息：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 连接名称]</p> </td> 
      <td> <p>输入新连接的名称。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 数据中心ID] </td> 
      <td>使用格式<code>&lt;Data Center ID>.qualtrics.com</code>。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td>要查找API密钥，请参阅[!DNL Qualtrics]文档。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Qualtrics] 模块及其字段

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
