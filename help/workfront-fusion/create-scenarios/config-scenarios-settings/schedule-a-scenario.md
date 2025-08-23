---
content-type: reference
title: 计划方案
description: 默认情况下，场景每15分钟运行一次。 您可以通过定义激活方案运行的时间和频率来更改此设置。 融合场景可以计划为每5分钟运行一次。
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 2%

---

# 计划方案

默认情况下，场景每15分钟运行一次。 您可以通过定义激活方案运行的时间和频率来更改此设置。 融合场景可以计划为每5分钟运行一次。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前： [！UICONTROL Work]或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新：</p> <ul><li>[！UICONTROL Select]或[！UICONTROL Prime] Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li><li>[！UICONTROL Ultimate] Workfront计划：包括Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">访问级别配置*</td> 
   <td> 
     <p>您必须是组织的Workfront Fusion管理员。</p>
     <p>您必须是团队的Workfront Fusion管理员。</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 计划方案

1. 单击左侧面板中的&#x200B;**方案**&#x200B;选项卡。
1. 选择要计划的方案。
1. 在“方案详细信息”页面的右上角，单击&#x200B;**[!UICONTROL 选项]** > **[!UICONTROL 计划]**

   或

   单击方案触发器模块上的&#x200B;**[!UICONTROL 计划]**&#x200B;图标（时钟）。

1. 在下列字段中输入信息：

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[！UICONTROL运行方案]</td> 
      <td> <p>选择要运行方案的频率，然后选择间隔。</p> 
       <ul> 
        <li> <p><strong>[！UICONTROL，按固定间隔]</strong> </p> <p>输入两次执行之间的分钟数。 默认值为15分钟。</p> </li> 
        <li> <p><strong>[！UICONTROL一次]</strong> </p> <p>输入您希望方案运行的日期和时间。 使用格式<code>MM/DD/YYYY h:mm A</code>。 示例：<code>06/25/2019 11:00 PM</code>。</p> </li> 
        <li> <p><strong>[！UICONTROL每天]</strong> </p> <p>输入您希望方案运行的时间。 使用格式<code>h:mm A</code>。 示例：<code>11:00 PM</code>。</p> </li> 
        <li> <p><strong>[！UICONTROL一周天数]</strong> </p> <p>天数：选择您希望方案在一周中运行的天数。 您可以选择一天或多天。</p> <p>时间：输入您希望方案在选定日期运行的时间。 使用格式<code>h:mm A</code>。 示例： <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[！UICONTROL每月日期]</strong> </p> <p>天数：选择要运行方案的月中天数。 您可以选择一天或多天。</p> <p>时间：输入您希望方案在选定日期运行的时间。 使用格式<code>h:mm A</code>。 示例： <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[！UICONTROL指定日期]</strong> </p> <p>月份：选择要运行方案的月份。 您可以选择一个或多个月份。</p> <p>天数：选择要运行方案的月中天数。 您可以选择一天或多天。</p> <p>时间：输入您希望方案在选定日期运行的时间。 使用格式<code>h:mm A</code>。 示例： <code>11:00 PM</code></p> </li> 
       </ul> <p>注：方案必须存在日期才能在该日期运行。 例如，仅安排在每月第31天的方案将不会在2月、4月、6月、9月或11月运行，因为这些月份没有第31天。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL高级计划]</td> 
      <td>您可以定义运行方案的特定时间间隔。 您可以指定一天中的时间间隔、工作日或月。 对于每个间隔，单击<strong>[！UICONTROL添加]</strong>并按照[！UICONTROL运行场景]字段中所述填写字段。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL开始]</td> 
      <td>输入您希望方案运行的日期和时间。 使用格式<code>MM/DD/YYYY h:mm A</code>。 示例：<code>06/25/2019 11:00 PM</code>。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL结尾]</td> 
      <td>输入您希望方案运行之前的日期和时间。 使用格式<code>MM/DD/YYYY h:mm A</code>。 示例：<code>06/25/2019 11:00 PM</code>。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;保存计划设置并返回方案。
