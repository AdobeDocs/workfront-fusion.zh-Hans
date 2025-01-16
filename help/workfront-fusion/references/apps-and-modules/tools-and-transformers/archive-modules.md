---
title: 存档模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以将存档文件（如压缩文件）连接到多个第三方应用程序和服务。 例如，您可以配置一个方案，该方案
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# [!UICONTROL Archive]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以在方案中使用存档，如压缩文件，从而允许您在自动化或集成中使用它。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。 有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## [!UICONTROL Archive]模块及其字段

配置[!UICONTROL Archive]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!UICONTROL Archive]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Extract an archive]](#extract-an-archive)
* [[!UICONTROL Create an archive]](#create-an-archive)
* [[!UICONTROL Inflate]](#inflate)
* [[!UICONTROL Deflate]](#deflate)

## [!UICONTROL Extract an archive]

此操作模块会从存档中提取您标识的文件。

模块会返回文件的ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p> 选择要提取的文件。 此文件可以从以前的模块（如[!DNL Workfront] &gt;[!UICONTROL Download a document]模块）进行映射。</p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**示例：**&#x200B;从定义的[!DNL Dropbox]文件夹中获取ZIP文件（例如，存档），使用[!UICONTROL Archive]模块提取该文件，并将提取的文件作为带有[!UICONTROL Email]或[!DNL Gmail]模块的附件发送到所需的电子邮件地址。
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

## [!UICONTROL Create an archive]

此聚合器模块将所需文件添加到[!UICONTROL ZIP]或[!UICONTROL TAR]存档。

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
   <td>[!UICONTROL Type] </td> 
   <td> <p>选择您要将文件添加到[!UICONTROL ZIP]存档还是[!UICONTROL TAR]存档。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>输入要添加到存档中的注释。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Group by]</td> 
   <td> <p>定义要按其分组聚合输出的表达式。 此表达式可以包含一个或多个映射项。 随后，将使用此表达式的值将聚合的数据分成不同的组。 每个组输出为一个单独的捆绑，其中包含一个键（经过计算的表达式）和一个值（聚合文本）。 在后续模块中，您可以将该键用作过滤器。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>选择此选项可在没有结果时停止方案。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Archive name]</td> 
   <td> <p> 输入已创建存档的名称。 请勿添加扩展。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**示例：**&#x200B;使用[!DNL Gmail] >[!UICONTROL Watch emails]模块观看传入电子邮件。 如果收到电子邮件，则其附件将迭代为单独的包，然后存档到[!DNL ZIP]文件并保存到定义的Dropbox文件夹。
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

## [!UICONTROL Inflate]

此转换器模块使用膨胀算法解压缩二进制数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>使用膨胀函数输入或映射要解压缩的数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

## [!UICONTROL Deflate]

此转换器模块使用压缩算法压缩二进制数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>使用deflate函数输入或映射要压缩的数据。</p> </td> 
  </tr> 
 </tbody> 
</table>
