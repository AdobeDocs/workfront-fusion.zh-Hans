---
title: 在模块之间映射文件
description: 某些模块具有处理文件的功能。 这些模块可以返回要发送以供进一步处理的输出文件，也可以要求将文件传递给它们以供处理。 这些模块需要相互映射，才能共同处理文件。
author: Becky
feature: Workfront Fusion
exl-id: 25c632f4-169e-4d3c-989a-f57b398bd3f0
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 1%

---

# 在模块之间映射文件

有些模块可以处理文件。 这些模块可以返回要发送以供进一步处理的输出文件，也可以要求将文件传递给它们以供处理。 可以映射文件，以便一个模块输出的文件可以由另一个模块处理。

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

1. 单击左侧面板中的&#x200B;**[!UICONTROL Scenarios]**&#x200B;选项卡。
1. 选择要映射文件的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 在要映射到的目标模块中，找到&#x200B;**Source文件**&#x200B;区域。
1. 要映射上一个模块输出的文件，请选择输出文件的模块。

   ![Workfront下载文档](assets/wf-download-document.png)

1. 要手动映射名称和数据，请选择映射，然后输入或映射文件的名称和数据。

   ![使用映射选项](assets/use-the-map-option.png)

1. 继续配置模块，或单击&#x200B;**确定**。
