---
title: MariaDB模块
description: 在Adobe Workfront Fusion方案中，您可以自动使用 [!DNL MariaDB]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# [!DNL MariaDB]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL MariaDB]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL MariaDB]模块，您必须具有[!DNL MariaDB]帐户。

## 将[!DNL MariaDB]连接到Workfront Fusion

您可以在[!DNL MariaDB]模块内直接创建与[!DNL MariaDB]帐户的连接。

1. 在任意[!DNL MariaDB]模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
1. 配置以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL连接名称]</p> </td> 
      <td> <p>输入新连接的名称。</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[！UICONTROL环境]</td>
        <td>选择此连接是用于生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL类型]</td>
        <td>选择您是要连接到服务帐户还是个人帐户。</td>
        </tr>
     <tr> 
      <td role="rowheader">[！UICONTROL主机]</td> 
      <td> <p>输入数据库实例的IP地址或主机名。 此主机必须可从网络外部访问。</p> <p>示例： <code>[!DNL mariadb.hwoh2j5h.us-east-1.rds.amazon.com]</code></p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL端口]</td> 
      <td>默认端口为3306。 如果您使用的是非标准端口，请将此号码设置为您的端口。 </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL数据库]</td> 
      <td>输入要与之交互的数据库名称。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL用户]</td> 
      <td>输入您的用户名。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL密码]</td> 
      <td>输入密码。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL MariaDB]模块及其字段

在配置[!DNL MariaDB]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL MariaDB]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 执行查询（高级）

此操作模块根据您提供的查询从数据库中检索信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关将[!DNL MariaDB]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">将[!DNL MariaDB]连接到Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Query]</td> 
   <td> <p>输入您希望模块用于检索数据的SQL查询。</p> <p>重要信息：查询中使用的变量不会经过清理。 确保正确清理变量以防止SQL注入。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 从表中选择行（高级）]

此模块从数据库中读取记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关将[!DNL MariaDB]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">将[!DNL MariaDB]连接到Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL表]</td> 
   <td> <p>选择包含要读取的记录的表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL筛选器]</td> 
   <td> <p>设置要按其选择行的筛选器</p> 
    <ul> 
     <li> <p>选择要作为搜索依据的字段</p> </li> 
     <li> <p>选择要用于搜索的运算符</p> </li> 
     <li> <p>输入或映射要搜索的值。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL排序] </td> 
   <td> <p>对于要作为结果排序依据的每个级别，单击<strong>[！UICONTROL添加项]</strong>，然后选择要作为结果排序依据的字段以及要按升序还是降序排序</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>
