---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: Workfront Fusion发行活动： 2020年11月16日开始的周
description: 本页介绍了2020年11月16日这一周在Adobe Workfront Fusion中所做的所有增强。
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: 69e4a458-fd32-4dcd-be43-19a9467cf678
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Workfront Fusion发行活动： 2020年11月16日开始的周

本页介绍了2020年11月16日这一周在Adobe Workfront Fusion中所做的所有增强。

有关所有最近更改的列表，请参阅[Adobe Workfront Fusion发行活动](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md)。

有关Workfront Fusion中最近的错误修复列表，请参阅[Workfront维护更新](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=zh-Hans)页面，并检查任何标记为Workfront Fusion维护更新的更新。

## Jira云连接器的更新

为了扩展您使用Jira云连接器的方式，我们添加了三个新模块：

* 将问题添加到冲刺
* 列出记录
* 搜索记录

我们还更新了现有模块以支持“Sprint”对象类型。 以前，只能通过自定义API调用模块访问“Sprint”对象。

## 执行ID现在可用于场景中的映射

现在，映射面板中提供了方案的执行ID。 此ID表示场景的特定执行，可用作元数据。 例如，执行ID可以与Fusion创建的记录一起保存，以便您稍后可以确定创建该记录的Fusion执行。 您可以在映射面板中的“常规函数”下找到执行ID。

## Workfront Fusion 2.0方案的键盘快捷键

为了使场景构建更加方便，我们添加了一些键盘快捷键：

* Ctrl/Cmd+Shift+Enter：运行方案一次
* Ctrl/Cmd + Shift + S：保存方案

## Office 365 Excel连接器的更新

为了扩展您使用Office 365 Excel连接器的方式，我们添加了一些新模块。 现在您可以：

* 从对工作簿的更改触发模块
* 搜索或下载工作簿
* 列出工作表、工作表行、表或表行
* 更新表或工作表行
* 删除表或工作表行
* 检索表的元数据
* 进行自定义API调用

应用程序中仍存在以前可用的模块。


## 在您的Workfront应用程序连接中使用OAuth 2.0

我们已更新Workfront连接器以使用OAuth 2.0。此更新意味着更轻松地在Workfront应用程序连接中进行更改。 例如，如果连接发生了更改（如密码），则无需更新场景中的各个连接。 此外，OAuth2还提供其他好处，例如增强安全性和使用单点登录(SSO)的功能。

现有连接此时不需要任何更改。 但是，如果您希望利用OAuth 2.0的好处，可以重新授权现有连接。
