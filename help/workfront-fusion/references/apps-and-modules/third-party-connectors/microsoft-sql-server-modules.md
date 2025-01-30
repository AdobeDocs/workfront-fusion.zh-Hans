---
title: Microsoft SQL Server模块
description: 您可以使用 [!DNL Adobe Workfront Fusion] 连接到Microsoft SQL Server。
author: Becky
feature: Workfront Fusion
exl-id: 8f3293f7-8b45-4e42-8ad8-f9d4969b63fd
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# [!DNL Microsoft SQL Server]模块

您可以使用[!DNL Adobe Workfront Fusion]连接到[!UICONTROL Microsoft SQL Server]。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
  <td> <p>[!UICONTROL Pro] 或更高</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
   <td> <p>[!UICONTROL Plan]， [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前许可证要求：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Adobe Workfront]计划，则您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[!UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。



## 正在将[!DNL Microsoft SQL Server]服务连接到[!DNL Workfront Fusion]

有关将[!DNL Microsoft SQL Server]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

>[!NOTE]
>
>某些Microsoft应用程序使用相同的连接，该连接与单个用户权限相关联。 因此，在创建连接时，权限同意屏幕除了显示当前应用程序所需的任何新权限外，还会显示以前授予此用户连接的任何权限。
>
>例如，如果用户拥有通过Excel Connector授予的“读取表”权限，然后在Outlook Connector中创建连接以读取电子邮件，则权限同意屏幕将显示已授予的“读取表”权限和新要求的“写入电子邮件”权限。

## 使用[!DNL Microsoft SQL Server]模块

您可以通过存储过程直接在数据库服务器上执行自定义逻辑。 [!DNL Adobe Workfront Fusion]动态加载输入/输出参数和记录集的接口，以便可以单独映射每个参数或值。 在开始配置方案之前，请确保用于连接到数据库的帐户具有对`INFORMATION_SCHEMA.ROUTINES`和`INFORMATION_SCHEMA.PARAMETERS`视图的读取权限。

当[!DNL Fusion]建立与[!DNL SQL server]目标的连接时，[!DNL Fusion]用户将识别主机（承载服务器的域名或IP地址）和端口。 [!DNL Fusion]可以连接到任何可用的主机和端口。

有关[!DNL Workfront Fusion]使用的特定IP地址的信息，请参阅[用于访问的IP地址 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)

要了解有关创建存储过程的更多信息，请参阅[!DNL Microsoft SQL Server]文档。

>[!NOTE]
>
>[!DNL Workfront Fusion]不支持多个记录集。 仅处理第一个实例。

## 疑难解答错误[!UICONTROL ER_LOCK_WAIT_TIMEOUT: Lock wait timeout exceeded; try restarting transaction]

使用多个模块修改相同的数据时，会发生此错误。 它由SQL事务引起。

执行任何SQL模块时，都会启动一个事务。 事务在方案完全执行后完成。

如果另一个模块尝试访问相同的数据，则必须等到上一个事务完成。 由于第一个事务将在方案完成后完成，因此第二个事务永远不能开始。

### 解决方案：

打开自动提交。 自动提交在模块执行完成后立即完成（提交）每个事务。

1. 单击屏幕底部的[!UICONTROL Scenario settings]图标![方案设置图标](/help/workfront-fusion/references/apps-and-modules/assets/scenario-settings-icon.png)。
1. 单击&#x200B;**[!UICONTROL Auto commit]**&#x200B;复选框。
1. 单击&#x200B;**[!UICONTROL OK]**&#x200B;保存方案设置。
