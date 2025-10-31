---
content-type: reference
title: 设置和管理组织和团队：文章索引
description: 本节包含与在Adobe Workfront Fusion中设置和管理组织和团队相关的文章。
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: f7c1d5b1de74cc0c59e3a00938bed14b489500db
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# 通过[!DNL Adobe Admin Console]删除用户

您只能从Adobe Workfront Fusion中删除一个用户，而保留对任何其他[!DNL Adobe]产品配置文件的访问权限，或者您可以从[!DNL Adobe Admin Console]中完全删除该用户。

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
   <td role="rowheader">产品</td> 
   <td>
   <p>如果贵组织具有不包含Workfront Automation and Integration的Select或Prime Workfront包，则贵组织必须购买Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">访问级别配置</td> 
   <td> 
     <p>您必须是组织的Adobe Admin Console管理员。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

+++

## 仅从Adobe Workfront Fusion中删除用户

您可以从Workfront Fusion中删除用户，同时保持其其他Adobe产品权限不变。

有关说明，请参阅[在Admin Console上管理产品](https://helpx.adobe.com/cn/enterprise/using/manage-products.html)一文中的“从产品中删除用户和用户组”。

## 在[!DNL Adobe Admin Console]的所有产品中停用用户

要删除用户，必须通过[!DNL Adobe Admin Console]取消激活该用户。

当满足以下任一条件时，将从[!DNL Adobe Admin Console]取消激活用户：

* 用户将从产品或产品配置文件中移出，且不会分配到任何其他产品或产品配置文件。
* 将从链接到产品配置文件的组中删除用户，但不包含在与产品配置文件链接的任何其他组中。
* 该用户将从产品配置文件中删除，并且未分配给其他产品配置文件。
* 在包括Workfront Fusion的组织中删除或停用用户。

  有关说明，请参阅[单独管理用户](https://helpx.adobe.com/cn/enterprise/using/manage-users-individually.html)中的“删除用户”部分。

在Workfront Fusion中，停用操作可通过以下方式之一影响用户：

* 如果用户仅在一个组织中，则停用该用户。
* 如果用户位于多个组织中，则会将该用户从在[!DNL Adobe Admin Console]上修改该用户的组织中删除。
* 删除用户时，请考虑以下事项。

### 在Workfront Fusion中删除用户时的注意事项

删除用户时，请考虑以下事项。

* 删除用户后，用户的连接、键和Webhook将被删除。
* 属于用户的任何方案都将转移到组织“所有者”。 必须更新这些方案中的连接，因为属于用户的连接不再有效。
* 如果删除的用户拥有任何应用程序或公共模板，则应用程序或公共模板将转移给组织“所有者”。 如果没有组织“所有者”，则应用程序或公共模板将转移到另一个用户。
