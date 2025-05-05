---
title: Workfront Fusion发行活动：&amp；nbsp；2021年8月30日当周
description: Workfront Fusion发行活动：&amp；nbsp；2021年8月30日当周
author: Luke
draft: Probably
feature: Product Announcements, Workfront Fusion
recommendations: noDisplay, noCatalog
hidefromtoc: true
exl-id: cac11147-5b3d-477b-869b-e255528c4bec
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Workfront Fusion发行活动： 2021年8月30日开始的周

本页介绍了2021年8月30日这一周在Adobe Workfront Fusion中所做的所有增强。

有关所有最近更改的列表，请参阅[Adobe Workfront Fusion发行活动](/help/workfront-fusion/fusion-product-releases/fusion-release-activity.md)。

有关Workfront Fusion中最近的错误修复列表，请参阅[Workfront维护更新](https://experienceleague.adobe.com/docs/workfront-known-issues/releases/current-updates.html?lang=zh-Hans)页面，并检查任何标记为Workfront Fusion维护更新的更新。

## 过滤触发Workfront >关注事件模块的事件

1. 为触发Workfront >关注事件模块的事件设置自定义过滤器

   为了减少不必要的场景运行次数，我们已更新Workfront >关注记录模块以启用事件过滤。 现在，您可以在创建webhook时设置过滤器。 这允许场景仅在事件满足特定条件时触发。

   事件过滤器当前提供以下操作：

   * 等于：仅当事件与过滤器的条件匹配时触发方案。 例如，您可以设置一个过滤器，仅在特定项目中发生事件时触发场景。
   * 不等于：仅当事件与过滤器的条件不匹配时触发方案。 例如，您可以创建一个过滤器，仅在发生事件的问题状态不是“已关闭”时，触发方案。

   以前，Watch记录模块会检索所有记录。 用户只能通过在场景的后面设置过滤器来进行过滤。

   要利用事件过滤功能，请在Watch事件模块中创建新的webhook。 当前无法编辑现有Webhook以包含此功能。 我们强烈建议您使用事件过滤器为现有方案创建新的Webhook。

1. 过滤掉当前连接触发的事件。

   为了更便于为Workfront >观看活动模块设置Webhook，我们添加了最常用的活动过滤器。 现在，webhook有一个选项，可以使用为Watch事件模块指定的连接过滤掉模块所做的任何更改。 换言之，启用此过滤器后，Workfront用户所做的任何与该连接关联的更改都将无法触发该方案。

   以前，此过滤器不可用。 因此，在Workfront模块中所做的更改更容易触发包含这些模块的方案，这可能会导致方案无限期地触发自身。
