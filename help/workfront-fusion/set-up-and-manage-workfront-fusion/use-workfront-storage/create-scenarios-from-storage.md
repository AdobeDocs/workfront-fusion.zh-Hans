---
title: 从存储创建方案
description: 存储与Fusion的方案生成器集成，因此您可以直接从“存储”页面创建预配置的方案以下载或上传文件。
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: aef1685cb25c0cdcb0dcdf9b0c73fb482d392e5f
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 0%

---

# 从存储创建方案

有关存储的概述，请参阅[存储概述](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/storage-overview.md)。

存储与Fusion的场景生成器集成。 在“存储”页面中，用户可以创建将下载所选文件的方案。

## 下载方案

1. 在Workfront Fusion中，单击左侧导航栏中的&#x200B;**存储**。
1. 导航到包含要在场景中下载的文件的存储库。
1. 选择一个文件，然后单击操作栏中的&#x200B;**“在场景中下载”**。

然后Fusion创建一个名为&#x200B;**“下载{fileName}”**&#x200B;的新方案。 此方案将在单独的浏览器选项卡中打开。

此方案预配置了：

* 活动连接。
* 预先选定的存储库、文件夹和文件。
* 用于生成预签名的下载URL的模块。
* 用于从该URL获取文件的HTTP模块。
* 默认计划间隔为15分钟。

## 在场景中上传文件

1. 在Workfront Fusion中，单击左侧导航栏中的&#x200B;**存储**。
1. 导航到包含要在场景中下载的文件的存储库和文件夹。
1. 在文件夹内浏览时，单击&#x200B;**“上传文件”**&#x200B;下拉列表。
1. 选择&#x200B;**“上载方案中的文件”**。

然后Fusion创建一个名为&#x200B;**“上载到{folderName}”**&#x200B;的新方案。 此方案将在新的浏览器选项卡中打开。 您必须添加模块以提供要上传的文件，例如“Workfront”>“下载文档”模块。

此方案预配置了：

* 活动连接。
* 已预选存储库和文件夹。
* 用于生成带有占位符文件名的预签名上传URL的模块。
* 默认计划间隔为15分钟。

