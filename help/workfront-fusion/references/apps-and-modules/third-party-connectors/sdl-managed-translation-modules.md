---
title: SDL托管翻译模块
description: 在Adobe Workfront Fusion方案中，您可以将SDL Managed Translation帐户连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 1%

---

# [!DNL SDL Managed Translation]模块

在Adobe Workfront Fusion方案中，您可以将[!DNL SDL Managed Translation]帐户连接到多个第三方应用程序和服务。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront计划*</td>
  <td> <p>[!UICONTROL Pro]或更高版本</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证*</td>
   <td> <p>[!UICONTROL 计划]，[!UICONTROL 工作]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前许可证要求：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] Adobe Workfront计划，则贵组织必须购买Adobe Workfront Fusion和Adobe Workfront，才能使用本文中所述的功能。 Workfront Fusion包含在[!UICONTROL Ultimate] Workfront计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买Adobe Workfront Fusion和Adobe Workfront，才能使用本文中所述的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有的计划、许可证类型或访问权限，请联系您的Workfront管理员。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## SDL Managed Translation API信息

SDL Managed Translation连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td>https://languagecloud.sdl.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.4.26</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL SDL Managed Translation]模块

>[!NOTE]
>
>调用[!DNL SDL Managed Translation]的操作超时为&#x200B;**120秒**。

### 文件

#### [!UICONTROL 下载已翻译文件]

此模块检索单个已翻译文件的内容，这些文件包含在指定的项目中。 如果请求的文件尚未处于Downland状态，则文件的内容可能尚未完全翻译。 如果文件处于下载状态，并且您已成功检索到它，请确保使用`Cancel or Complete File`方法将文件标记为完成。

#### [!UICONTROL 上载文件]

此模块允许上传要翻译或包含在翻译项目中作为参考材料的文件。 上载必须使用多部分/表单数据提交，并且可以包含多个文件。 您指定用于评估已上传文件的`ProjectOptionId`。 这会确定您上传的每个文件是翻译的可能候选项，还是必须作为参考材料处理。 对于存档（`zip `、`rar`、`7z`、`tar`个文件），应用程序将检查存档的内容，并指示存档是否可以整个翻译，或者存档是否包含可翻译和不可翻译的混合文件。

>[!NOTE]
>
>不建议一次上传多个文件，因为这样会增加任何失败的影响。

#### [!UICONTROL 添加参考文件]

此模块添加一个参考文件。

### 项目

#### [!UICONTROL 创建项目]

此模块创建指定的项目。

#### 取消或完成项目

此模块可取消或完成指定的项目。 如果项目正在等待下载，则项目会完成工作流中的任何最终步骤，并最终移动至完成。 如果项目正在等待审批或供应商选择已取消。 如果项目处于任何其他状态，请求将失败。

#### [!UICONTROL 下载项目Zip]

此模块获取指定项目的已翻译文件的`zip`文件。

#### [!UICONTROL 读取项目]

此模块获取指定的项目。

#### [!UICONTROL 获取状态为]的项目

此模块获取所有处于指定状态的可用项目。 此方法允许通过指定`$top`、`$skip`和`$orderby`查询参数来分页结果。

#### [!UICONTROL 获取项目列表]

获取所有项目的简单列表，提供有关每个项目的一般信息。 通过指定`$top`、`$skip`和`$orderby`查询参数，此方法允许将结果设置为页面。

#### [!UICONTROL 搜索项目创建选项]

此模块获取项目创建选项。

### 其他

#### [!UICONTROL 进行API调用]

此模块执行任意授权的API调用。
