---
title: 聚合器模块
description: 聚合器模块是一种旨在将多捆数据合并到单个捆绑包中的模块。
author: Becky
feature: Workfront Fusion
exl-id: 93cde0d0-4013-463a-b19c-d58180632739
source-git-commit: 99621f57da1eb294834a0eacfe527dcf017408e9
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# [!UICONTROL 汇总]模块

聚合器模块是将多捆数据合并到单个捆绑包中的模块。

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
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

+++## [!UICONTROL 汇总]模块概述

执行[!UICONTROL 汇总]模块时，它将执行以下操作：

* 从单个源模块的操作中累积所有包。
* 输出一个包，其数组包含每个累积包的一个项目。 数组项的内容取决于特定的[!UICONTROL 聚合器]模块及其设置。

下图显示了[!UICONTROL 聚合器]模块的典型设置：

![数组汇总](assets/array-aggregator.png)

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td> <p>[!UICONTROL Source Module]</p> </td> 
   <td> <p>捆绑聚合开始的模块。 源模块通常是输出一系列捆绑包的迭代器或搜索模块。</p><p>设置聚合器源模块（并关闭聚合器设置）时，源模块和聚合器模块之间的路由将封装在灰色区域中，以便您可以清楚地看到聚合的开始和结束。 
   </p> <p>有关迭代器的详细信息，请参阅<a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">[!UICONTROL Iterator]模块</a>。</p> 
   <p>有关搜索模块的详细信息，请参阅模块概述中的<a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#search-modules" class="MCXref xref">搜索模块</a>。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 目标结构类型]</p><p>（仅适用于[!UICONTROL 数组汇总]模块。）</p> </td> 
   <td> <p> 聚合数据的目标结构。 默认选项[!UICONTROL 自定义]允许您选择应聚合到[!UICONTROL 数组聚合器]的输出捆绑包的<code>Array </code>项中的项：</p> <p> <img src="assets/output-bundle-array-item.png"> </p> <p>在[!UICONTROL Array aggregator]模块之后连接多个模块，并返回到聚合模块的设置后，[!UICONTROL Target]结构类型下拉菜单将包含以下所有模块及其字段的“集合数组”类型。 <p>在此示例中，[!DNL Slack] &gt;[!UICONTROL 创建消息]模块的[!UICONTROL 附件]字段显示在数组汇总&gt;目标结构类型字段中。 </p> <p> <img src="assets/array-aggregator-slack.png"> </p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 聚合字段]</td> 
   <td>要包含在聚合器模块输出中的字段。</td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL 分组依据]</p> </td> 
   <td> <p>使用“分组依据”字段，您可以定义包含一个或多个映射项的表达式。 然后，聚合的数据将按表达式的值分成组。 每个组输出为一个单独的捆绑包，包含一个键和一个数据数组。 通过对结果进行分组，您可以在后续模块中将键用作过滤器。</p>
   <p>每个捆绑包包含两个项目：</p> 
    <ul> 
     <li><code>Key</code>：您作为分组依据的值。</li> 
     <li><code>Array</code>：公式计算为<code>Key</code>值的捆绑中的聚合数据。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td> <p>在空聚合后停止处理</p> </td> 
   <td> <p>默认情况下，即使没有捆绑包到达[!UICONTROL 聚合]模块，[!UICONTROL 聚合]模块也会输出聚合结果（例如，因为已从包含聚合器的路径中筛选出了所有捆绑包）。 如果启用了选项[!UICONTROL Stop processing after an empty aggregation]，则在没有输入捆绑包时，[!UICONTROL Aggregator]模块不会生成任何输出捆绑包。 相反，流量会停止。</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!UICONTROL 聚合器]模块不输出源模块和[!UICONTROL 聚合器]模块之间模块生成的捆绑包。 流中位于[!UICONTROL 聚合]之后的模块无法访问这些包。 如果需要源模块和[!UICONTROL 聚合器]模块之间的模块输出的捆绑包中的任何数据，请确保在[!UICONTROL 聚合器]模块的设置中包含给定项（例如，在[!UICONTROL 数组聚合器]模块设置的[!UICONTROL 聚合字段]字段中）。


## 聚合器如何工作的示例场景

此示例方案显示如何压缩所有电子邮件附件并将ZIP文件上传到[!DNL Dropbox]。

![Dropbox存档示例](assets/dropbox-archive.png)

以下方案显示如何：

* 第一个模块监视邮箱是否有传入电子邮件。 [!UICONTROL 电子邮件] >[!UICONTROL 查看电子邮件]触发器输出包含项目`Attachments[]`的捆绑包，该项目是一个包含所有电子邮件附件的数组。

* 第二个模型迭代电子邮件的附件：[!UICONTROL 电子邮件] >[!UICONTROL 迭代附件]迭代器逐个从`Attachments[]`数组获取项目，然后作为单独的捆绑包进一步发送它们。

* 第三个模块是聚合器。 它会聚合[!UICONTROL 电子邮件] >[!UICONTROL 迭代附件]模块输出的包。 [!UICONTROL 存档] >[!UICONTROL 创建存档聚合器]累计它接收的所有包，并输出包含ZIP文件的单个包。

* 最后一个模块会将生成的ZIP文件上载到[!DNL Dropbox]。  [!DNL Dropbox] > [!UICONTROL 上载文件]从[!UICONTROL 存档] > [!UICONTROL 获取ZIP文件创建存档]模块并将其上载到[!DNL Dropbox]。



以下是[!UICONTROL 存档] > [!UICONTROL 创建存档]聚合器的示例设置：

![创建存档](assets/archive-create-an-archive.png)
