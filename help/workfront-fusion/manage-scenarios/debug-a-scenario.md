---
title: 调试方案
description: Adobe Workfront Fusion Devtool允许您了解场景并排除其故障。 Devtool可在Chrome开发人员工具中添加一个额外的面板。 使用此调试器面板，您可以检查场景的所有手动运行，查看所有执行的操作，并查看每个执行的API调用的详细信息。 您可以查看导致错误的模块、操作或单个响应，并使用该知识来优化场景。
author: Becky
feature: Workfront Fusion
exl-id: 34215370-27e3-4c28-8bd1-a16268900b86
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# 调试方案

[!DNL Adobe Workfront Fusion] Devtool可帮助您了解和排除方案。 使用Devtool，您可以检查场景的所有手动运行，查看所有执行的操作，并查看每个执行的API调用的详细信息。 您可以查看导致错误的模块、操作或单个响应，并使用该知识来优化场景。

>[!NOTE]
>
>对于机密场景、自动执行和成功操作，调试器面板中的记录将受限或不可用。

有关Fusion Devtool的视频介绍和演练，请参见

* [Fusion开发工具](https://video.tv.adobe.com/v/3427031/){target=_blank}
* [Devtool演练](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/fusion/troubleshooting-and-error-handling/dev-tool-walkthrough.html?lang=zh-Hans)

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证</td> 
   <td> <p>新增： [!UICONTROL Standard]</p><p>或</p><p>当前： [!UICONTROL Work]或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>[!UICONTROL Select] 或[!UICONTROL Prime] [!DNL Workfront]计划：您的组织必须购买[!DNL Adobe Workfront Fusion]。</li><li>[!UICONTROL Ultimate] [!DNL Workfront] 计划： [!DNL Workfront Fusion]已包括在内。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买[!DNL Adobe Workfront Fusion]。</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">访问级别配置*</td> 
   <td> 
     <p>您必须是组织的[!DNL Workfront Fusion]管理员。</p>
     <p>您必须是团队的[!DNL Workfront Fusion]管理员。</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 访问Devtool

如果您在AdobeUnified Shell中使用Fusion，或者已更新到新的Fusion Experience，则可以从场景编辑器访问Devtool。

1. 单击靠近屏幕底部的&#x200B;**帮助程序工具** ![帮助程序工具](assets/debugger-icon.png)图标。

或：

1. 转到要调试的方案的方案编辑器。

   要查找方案编辑器，请参阅[方案编辑器](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md)。

1. 右键单击页面的空白区域（不是模块）。
1. 选择&#x200B;**打开Devtool**。

## 使用[!DNL Workfront Fusion] Devtool

Workfront Fusion Devtool分为3个主要部分。 您可以在Devtool窗口的左侧面板中找到这些内容。

* [实时流](#live-stream)
* [方案调试器](#scenario-debugger)
* [工具](#tools)

### 实时流

在您的场景中单击运行一次后，实时流会显示后台发生的情况。

1. 单击&#x200B;**[!UICONTROL Live Stream]**&#x200B;图标![实时流图标](assets/live-stream-icon.png)以打开实时流部分。
1. 执行以下任一操作：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>操作</th> 
      <th>说明</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td role="rowheader">查看请求信息</td> 
      <td> <p>您可以查看场景中每个模块的以下信息</p> 
       <ul> 
        <li> <p>请求标头（API端点URL、http方法、调用请求的时间和日期、请求标头以及查询字符串）</p> </li> 
        <li> <p>请求正文</p> </li> 
        <li> <p>响应标头</p> </li> 
        <li> <p>响应正文</p> </li> 
       </ul> <p>要查看此信息，请单击[!DNL Workfront Fusion] Devtool右侧面板中相应的选项卡。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>按内容搜索事件</p> </td> 
      <td> <p>在[!DNL Workfront Fusion] Devtool左侧面板的搜索字段中输入搜索词，以仅显示包含搜索词的请求。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>清除请求列表 </p> </td> 
      <td> <p>单击Devtool左面板右上角的垃圾桶图标以清除[!DNL Workfront Fusion] Devtool记录的请求列表。 </p> </td> 
     </tr> 
     <!--<tr> 
      <td role="rowheader"> <p>Enable Console Logging</p> </td> 
      <td> <p>Click the computer icon <img src="assets/console-computer-icon.png"> in the top-right corner of the Devtool's left panel.</p> <p>Logging in the console is enabled when the computer icon is green.</p> </td> 
     </tr>-->
     <tr> 
      <td role="rowheader"> <p>以原始JSON格式或cURL检索请求</p> </td> 
      <td> 
       <ul> 
        <li> <p><strong>原始JSON</strong> </p> <p>单击Devtool右窗格右上角的<strong>[!UICONTROL Copy RAW]</strong>。</p> </li> 
        <li> <p><strong>cURL</strong> </p> <p>单击Devtool右窗格右上角的<strong>[!UICONTROL Copy cURL]</strong>。</p> </li> 
       </ul> </td> 
     </tr> 
    </tbody> 
   </table>

### 场景调试器

场景调试器适用于更复杂的场景。 它显示方案运行的历史记录，使您能够按名称或ID搜索模块。

1. 单击&#x200B;**[!UICONTROL Scenario Debugger]**&#x200B;图标![调试器图标](assets/scenario-debugger-icon.png)以打开方案调试器。
1. （可选）在搜索字段中输入搜索词（名称或模块ID）。
1. 单击模块名称。
1. 单击操作可查看请求详细信息。

### 工具

[!DNL Workfront Fusion] Devtool提供了一些工具，可让您更轻松地设置方案。

1. 单击&#x200B;**[!UICONTROL Tools]**&#x200B;图标![控制台工具图标](assets/console-tools-icon.png)以打开工具。
1. 选择要使用的工具
1. 配置字段，如下所述。
1. 单击 **[!UICONTROL Run]**。

工具及其字段：

* [集中处理模块](#focus-a-module)
* [通过映射查找模块](#find-modules-by-mapping)
* [获取应用程序元数据](#get-app-metadata)
* [复制映射](#copy-mapping)
* [复制筛选器](#copy-filter)
* [复制模块名称](#copy-module-name)
* [交换连接](#swap-connection)
* [交换变量](#swap-variable)
* [基64](#base-64)
* [重新映射Source](#remap-source)

#### [!UICONTROL Focus a Module]

按ID打开指定模块的设置。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Module ID]</td>
        <td>输入模块的ID以打开其设置。</td>
    </tr>
</table>

#### [!UICONTROL Find Modules by Mapping]

允许您搜索指定术语的模块值。 输出包含包含已搜索术语的模块ID。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword]</td> 
   <td> <p> 输入要搜索的搜索词。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Use Only Values]</p> </td> 
   <td> <p>启用此选项可仅搜索模块字段的值。</p> <p>禁用此选项还可搜索模块字段的名称。</p> <p>通过名称和标签参数执行搜索。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get App Metadata]

按应用程序的模块名称或ID检索应用程序的元数据。 例如，在需要了解场景中使用的应用程序版本时，这非常有用。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>选择要检索元数据的模块。</td>
    </tr>
</table>

#### [!UICONTROL Copy Mapping]

将值从源模块复制到目标模块。

>[!CAUTION]
>
>确保设置了正确的源模块和目标模块。 如果选择其他类型的模块，则将删除目标模块中的值。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> 选择模块或输入要从中复制字段值的模块的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>选择模块或输入要插入源模块值的模块的ID。</p> <p>重要信息：将覆盖目标模块中的值。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy Filter]

将过滤器设置从源模块复制到目标模块。

>[!NOTE]
>
>复制操作在位于所选模块左侧的过滤器上执行。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> 选择模块或输入要从中复制筛选器值的模块的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>选择模块或输入要插入源模块中的过滤器值的模块的ID。</p> <p>重要信息：将覆盖目标模块中的值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Preserve Fallback Route setting]</p> </td> 
   <td> <p>源筛选器设置为回退路由。 启用此选项还可以将目标过滤器设置为回退路由。</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Copy Module Name]

将所选模块的名称复制到剪贴板。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Module] </td> 
   <td> <p>选择要复制其名称的模块。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Swap Connection]

在同一应用程序的场景中，复制从源模块到每个模块的连接。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>选择模块或输入要从中复制连接的模块的ID。</td>
    </tr>
</table>

#### [!UICONTROL Swap Variable]

在场景中搜索指定的变量并使用新变量替换它们。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable to Find]</td> 
   <td> <p> 从场景中的变量模块找到要替换的可变丸子，并将其复制到此([!UICONTROL Variable to Find])字段。 在字段中，它带有双大括号。 示例： <code>&#123;&#123;5.value&#125;&#125;</code>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Replace With]</p> </td> 
   <td> <p>从场景中的变量模块找到要用变量替换的变量，并将其复制到此([!UICONTROL Variable to Find])字段。 在字段中，它带有双大括号。 示例： <code>&#123;&#123;5.value&#125;&#125;</code>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Module]</p> </td> 
   <td> <p>选择要替换变量的变量模块。 如果未选择任何模块，则变量将在整个场景中被替换。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Base 64]

允许您将输入的数据编码为Base64或解码Base64。 有些请求被编码为Base64。 当您想要搜索编码请求中的特定数据时，此工具可能很有用。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>选择您要将数据从[!UICONTROL Raw Data]字段编码为Base64还是要将Base64解码为原始数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Raw Data]</p> </td> 
   <td> <p> 根据上面[!UICONTROL Operation]字段中选择的选项，输入要编码为Base64的数据，如果要解码为原始数据，则输入Base64。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remap Source]

允许您将映射源从一个模块更改为另一个模块。

您必须首先将要用作源模块的模块添加到方案中的路由。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module] </td> 
   <td> <p> 选择要替换的模块作为场景中其他模块的映射源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>选择要用作新映射源的模块。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Module to Edit]</p> </td> 
   <td> <p>如果不想更改整个方案中的映射，请选择要更改映射的模块。 </p> </td> 
  </tr> 
 </tbody> 
</table>
