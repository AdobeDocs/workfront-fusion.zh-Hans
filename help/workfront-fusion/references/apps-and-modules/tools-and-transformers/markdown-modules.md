---
title: Markdown模块
description: 在 [!DNL Adobe Workfront Fusion] 场景中，您可以使用Markdown模块将Markdown转换为HTML，并将HTML转换为Markdown。
author: Becky
feature: Workfront Fusion
exl-id: f1134bbf-c244-4f52-8744-f97453b2ce8a
source-git-commit: 1e95c93213c48aea9297a82669fb2012dbb27601
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# [!UICONTROL Markdown]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以使用[!UICONTROL Markdown]模块将Markdown转换为HTML，并将HTML转换为Markdown。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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

## [!UICONTROL Markdown to HTML]

此模块可将Markdown转换为HTML。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Markdown]</td> 
   <td> <p>输入Markdown格式纯文本。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL GitHub Flavored Markdown] </td> 
   <td> <p>启用此选项可将GitHub Flavored Markdown转换为HTML。</p> <p>有关详细信息，请参阅[!DNL GitHub]文档中的Markdown备忘单。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sanitize]</td> 
   <td>选择一个选项以指示您是要从文本中剥离HTML标签还是要转义HTML。</td> 
  </tr> 
 </tbody> 
</table>

## [!UICONTROL HTML to Markdown]

此模块可将HTML代码转换为Markdown。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Markdown]</td> 
   <td> <p>输入要转换为Markdown的HTML代码。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL GitHub Flavored Markdown] </td> 
   <td> <p>启用此选项以将HTML转换为[!DNL GitHub Flavored Markdown]。</p> <p>有关详细信息，请参阅[!DNL GitHub]文档中的Markdown备忘单。</p> </td> 
  </tr> 
 </tbody> 
</table>
