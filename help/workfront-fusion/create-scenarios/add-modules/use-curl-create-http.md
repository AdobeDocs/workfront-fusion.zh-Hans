---
title: 使用 cURL 添加 HTTP 模块
description: 您可以将cURL请求粘贴到场景中，然后Fusion会创建根据cURL请求配置的HTTP模块。
author: Becky
feature: Workfront Fusion
exl-id: 6d466809-860d-4f72-9044-ebe2df943674
TQID: https://experienceleague.adobe.com/vPAMsVLVV7C3ykPPXgbMgDTosd0M3hYKYVL-OFszXqw
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 39%

---

# 使用 cURL 添加 HTTP 模块

您可以将cURL请求粘贴到场景中，然后Fusion会创建根据cURL请求配置的HTTP模块。

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
