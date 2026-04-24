---
product-previous: workfront-fusion
content-type: release-notes
product-area: workfront-integrations
navigation-topic: fusion-release-activity
title: Workfront Fusion 发行活动：2021 年 5 月 3 日当周
description: 本页介绍了2021年5月3日这一周在Adobe Workfront Fusion中所做的所有增强。
author: Luke
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 8858fc79-5eda-4938-9bb5-c05be38f02bc
source-git-commit: bc4c5c047f4847b929c4b047be1897d8872709e9
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 20%

---

# Workfront Fusion 发行活动：2021 年 5 月 3 日当周

本页介绍了2021年5月3日这一周在Adobe Workfront Fusion中所做的所有增强。

如需查看所有近期更改的完整列表，请参阅 [Adobe Workfront Fusion 发行活动](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md)。

如需查看 Workfront Fusion 的近期错误修复，请访问 [Workfront 维护更新](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html)页面，并查找标记为“Workfront Fusion 维护更新”的更新内容。

## Salesforce连接器现在可以使用SOQL进行搜索

Salesforce >搜索记录模块现在可以选择使用SOQL（Salesforce对象查询语言）进行搜索。 您还可以使用以前可用的选项（SOSL和简单搜索）进行搜索。

## Azure DevOps连接器中的新连接类型所需的作用域更少

为了增强安全性，我们已在Workfront Fusion Azure DevOps连接器中添加了新的连接器类型。 现在，在Azure DevOps模块中创建连接时，您可以从两种类型的连接中进行选择：

* Azure DevOps

  此新连接类型将作用域限制为Workfront Fusion特别需要的范围。

* Azure DevOps（请求所有作用域）

  这是旧版连接类型，它请求在与Azure DevOps的连接中所有可用的作用域。

我们建议您在使用Azure DevOps的所有新场景中使用Azure DevOps连接类型。 我们还建议您更改现有方案中的任何Azure DevOps模块以使用新的连接类型。 不久的将来，弃用旧版Azure DevOps（请求所有范围）连接类型。
