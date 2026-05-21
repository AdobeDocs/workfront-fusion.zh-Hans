---
title: MariaDB 模块
description: 在 Adobe Workfront Fusion 场景中，您可以自动化使用  [!DNL MariaDB] 的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
draft: Probably
feature: Workfront Fusion
exl-id: 41179cfe-c0f9-4d18-ab7e-374670ac688b
TQID: https://experienceleague.adobe.com/Dq7tbOvvEndH-6k3yX8AvH29kZxp748JeT1HW-zcDDQ
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 657
ht-degree: 60%

---

# [!DNL MariaDB] 模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL MariaDB] 的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用 [!DNL MariaDB] 模块，您必须拥有一个 [!DNL MariaDB] 帐户。

## 将 [!DNL MariaDB] 连接到 Workfront Fusion

您可以在[!DNL MariaDB]模块内直接创建与[!DNL MariaDB]帐户的连接。

1. 在任意[!DNL MariaDB]模块中，单击[!UICONTROL 连接]字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 配置以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL 连接名称]</p> </td> 
      <td> <p>输入新连接的名称。</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>选择此连接是用于生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>选择连接服务帐户还是个人帐户。</td>
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
      <td role="rowheader">[!UICONTROL 密码]</td> 
      <td>输入密码。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL MariaDB] 模块及其字段

在您配置 [!DNL MariaDB] 模块时，Workfront Fusion 会显示以下字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL MariaDB] 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 执行查询（高级）

此操作模块根据您提供的查询从数据库中检索信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关将 [!DNL MariaDB] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">将 [!DNL MariaDB] 连接到 Workfront Fusion</a>。</td> 
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
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关将 [!DNL MariaDB] 帐户连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-mariadb-to-workfront-fusion" class="MCXref xref">将 [!DNL MariaDB] 连接到 Workfront Fusion</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL表]</td> 
   <td> <p>选择包含要读取的记录的表。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 筛选条件]</td> 
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
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
  </tr> 
 </tbody> 
</table>
