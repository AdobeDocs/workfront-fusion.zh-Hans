---
title: 存档模块
description: 在Adobe Workfront Fusion场景中，您可以将存档（例如压缩文件）连接到多个第三方应用程序和服务。 例如，您可以配置一个方案，该方案
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 0%

---

# [!UICONTROL 存档]模块

在Adobe Workfront Fusion场景中，您可以在场景中使用档案，例如压缩文件，从而允许您在自动化或集成中使用它。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。 有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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

+++



## [!UICONTROL 存档]模块及其字段

在配置[!UICONTROL 存档]模块时，Workfront Fusion显示以下列出的字段。 此外，还可能会显示其他[!UICONTROL 存档]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)
* [汇总](#aggregators)
* [变压器](#transformers)

## 操作

### [!UICONTROL 提取存档]

此操作模块会从存档中提取您标识的文件。

模块会返回文件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>  <p>从上一个模块中选择源文件，或映射源数据。</p></p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**&#x200B;从定义的[!DNL Dropbox]文件夹中获取ZIP文件（例如，存档），使用[!UICONTROL 存档]模块提取该文件，并将提取的文件作为带有[!UICONTROL 电子邮件]或[!DNL Gmail]模块的附件发送到所需的电子邮件地址。

![示例Dropbox](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

>[!ENDSHADEBOX]

## 汇总

### [!UICONTROL 创建存档]

此聚合器模块将所需文件添加到[!UICONTROL ZIP]、GZIP或[!UICONTROL TAR]存档。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module]</td> 
   <td> <p> 选择要从中检索文件的模块。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 类型] </td> 
   <td> <p>选择是将文件添加到[!UICONTROL ZIP]、GZIP还是[!UICONTROL TAR]存档。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>输入要添加到存档中的注释。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 分组依据]</td> 
   <td> <p>定义要按其分组聚合输出的表达式。 此表达式可以包含一个或多个映射项。 随后，将使用此表达式的值将聚合的数据分成不同的组。 每个组输出为一个单独的捆绑，其中包含一个键（经过计算的表达式）和一个值（聚合文本）。 在后续模块中，您可以将该键用作过滤器。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 在出现空聚合后停止处理]</td> 
   <td>选择此选项可在没有结果时停止方案。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 存档名称]</td> 
   <td> <p> 输入已创建存档的名称。 请勿添加扩展。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**&#x200B;使用[!DNL Gmail] >[!UICONTROL 观看电子邮件]模块观看传入电子邮件。 如果收到电子邮件，则其附件将迭代为各个包，然后存档到[!DNL ZIP]文件并保存到定义的Dropbox文件夹。

![示例Gmail](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

>[!ENDSHADEBOX]

## 变压器

* [[!UICONTROL Deflate]](#deflate)
* [[!UICONTROL 膨胀]](#inflate)

### [!UICONTROL Deflate]

此转换器模块使用压缩算法压缩二进制数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 数据] </td> 
   <td> <p>使用deflate函数输入或映射要压缩的数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 膨胀]

此转换器模块使用膨胀算法解压缩二进制数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL 数据] </td> 
   <td> <p>使用膨胀函数输入或映射要解压缩的数据。</p> </td> 
  </tr> 
 </tbody> 
</table>
