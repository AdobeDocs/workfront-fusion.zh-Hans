---
title: 存储概述
description: “存储”是Workfront Fusion中的一个页面，通过该页面，团队可以直接访问其Adobe Enterprise Storage Management (ESM)存储库，从而让用户可以浏览文件夹、上载和下载文件、查看版本历史记录以及创建自动化方案。
author: Becky
feature: Workfront Fusion
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: d5568479d43bd5518adae5b66b132b4075e7f356
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 2%

---

# 存储概述

<!--Add to navigation articles once this goes to production-->

Workfront Fusion中的存储区域让团队可以直接访问其Adobe企业存储管理(ESM)存储库。 用户可以浏览文件夹、上载和下载文件、查看版本历史记录以及创建自动化方案，所有这些操作无需离开Fusion。

存储由团队拥有，并且要求组织登记到Adobe Identity Management System (IMS)，以便访问Adobe Storage。

Fusion Storage中的文件会镜像到Adobe Files (adobe.com/files)中，因此任何可以在Adobe Files中访问的文件都可以在Fusion Storage中访问。

有关使用“存储”的说明，请参阅：

* [初始化存储](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/initialize-storage.md)
* [在Workfront Fusion中查看和管理存储](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-and-manage-storage-in-workfront-fusion.md)
* [将文件上传到存储](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/upload-files-to-storage.md)
* [从存储中下载文件](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/download-files-from-storage.md)
* [从存储中删除文件](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/delete-files-from-storage.md)
* [在存储中查看文件版本历史记录](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/view-storage-file-version-history.md)
* [从存储创建方案](/help/workfront-fusion/set-up-and-manage-workfront-fusion/use-workfront-storage/create-scenarios-from-storage.md)

## 存储先决条件

要使用Workfront Fusion Storage区域，必须满足以下条件：

* 该组织已登记到&#x200B;**Adobe Identity Management System (IMS)**
* 组织有&#x200B;**Adobe存储**&#x200B;可用
* 用户已登录到&#x200B;**正确的Adobe IMS组织**（与选定的Fusion组织匹配的组织）
* 用户的帐户具有Adobe Storage **访问权限**

## 术语表

使用时

| 术语 | 定义 |
| ------ | ----------- |
| **存储库** | Adobe ESM中的顶级存储容器，通常映射到项目或工作区 |
| **Connection** | Fusion和Adobe Storage之间的安全链接，在初始化期间自动创建。 使用具有自动令牌刷新功能的Adobe IMS身份验证 |
| **ESM** | 企业存储管理，Adobe的云文件存储服务 |
| **IMS** | Adobe Identity Management System，Adobe的身份验证和身份平台 |

<!--

## UI Reference — Key Screens

### 1. Initialization Screen

* Cloud icon with **"Adobe Storage"** heading
* Description text explaining the feature
* **"Initialize Storage"** button (primary action)
* Error variants for access restriction, org mismatch, access denied, no storage found

### 2. Repository List

* Table with **Name** and **Region** columns
* **"Open"** action button per row

### 3. File Browser

* Breadcrumb navigation bar
* **"Upload File"** dropdown button (with "Upload File" and "Upload File in Scenario" options)
* File/folder table with **Name**, **Type**, **Size**, **Created** columns
* Floating action bar on file selection with: **Download**, **Download in Scenario**, **Versions**, **Delete**
* Upload/download progress banners (top-right corner)

### 4. Version History Panel

* Right-side slide-out panel
* Version list with date, version badge, and download button per entry
* **"current"** label on the latest version

-->
