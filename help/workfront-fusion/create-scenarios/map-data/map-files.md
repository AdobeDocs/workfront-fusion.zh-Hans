---
title: 在模块之间映射文件
description: 某些模块具有处理文件的功能。 这些模块可以返回要发送以供进一步处理的输出文件，也可以要求将文件传递给它们以供处理。 这些模块需要相互映射，才能共同处理文件。
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# 在模块之间映射文件

有些模块可以处理文件。 这些模块可以返回要发送以供进一步处理的输出文件，也可以要求将文件传递给它们以供处理。 可以映射文件，以便一个模块输出的文件可以由另一个模块处理。

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

## 将文件从源模块映射到目标模块

模块处理文件需要两点信息：

* 文件名
* 文件内容（数据）

如果之前有任何模块输出文件，则可以选择源模块，该模块输出的文件名称和数据将映射到目标模块。

您还可以手动输入此名称和数据，或从以前的模块中映射这些名称和数据。 例如，当重命名文件时，这可能很方便。

>[!NOTE]
>
>如果您需要处理来自URL的文件，我们建议使用`HTTP > Get a File`模块从URL下载文件，然后将文件从`HTTP > Get a File`模块映射到场景中所需模块的字段。
>
>![映射文件](assets/map-source-file.png)

要映射文件，请执行以下操作：

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要映射文件的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 在要映射到的目标模块中，找到&#x200B;**Source文件**&#x200B;区域。
1. 要映射上一个模块输出的文件，请选择输出文件的模块。

   ![Workfront下载文档](assets/wf-download-document.png)

1. 要手动映射名称和数据，请选择映射，然后输入或映射文件的名称和数据。

   ![使用映射选项](assets/use-the-map-option.png)

1. 继续配置模块，或单击&#x200B;**确定**。
