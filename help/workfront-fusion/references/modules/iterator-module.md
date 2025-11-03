---
title: 迭代器模块
description: 迭代器模块是一种特殊类型的模块，可将数组转换为一系列捆绑包。 每个数组项将作为单独的捆绑包输出。
author: Becky
feature: Workfront Fusion
exl-id: 43d39955-3dd7-453d-8eb0-3253a768e114
source-git-commit: 99621f57da1eb294834a0eacfe527dcf017408e9
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# [!UICONTROL 迭代器]模块

[!UICONTROL 迭代器]是一种将数组转换为一系列捆绑包的模块。 每个数组项将作为单独的捆绑包输出。

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

+++## [!UICONTROL 迭代器]模块配置

常规迭代器模块有一个字段[!UICONTROL 数组]字段。 此字段包含要转换或拆分为单独捆绑的数组。

![设置迭代器](assets/set-up-iterator.jpg)

其它连接器可以包括该迭代器特定的迭代器模块。 它们包含一个Source模块字段，允许您选择输出要迭代的数组的模块。

![专用迭代器](assets/specialized-iterators.jpg)

有关详细信息，请参阅[配置模块](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)。

>[!BEGINSHADEBOX]

**示例：**

* 以下方案显示如何检索带有附件的电子邮件，并将附件另存为选定[!DNL Dropbox]文件夹中的单个文件。

  电子邮件可以包含一系列附件。 第一个模块之后的[!UICONTROL 迭代器]模块允许方案分别处理每个附件。 [!UICONTROL 迭代器]模块将附件数组拆分为单个包。 然后，每个带有一个附件的包都会在选定的[!DNL Dropbox]文件夹中一次保存一个。 迭代器模块中的[!UICONTROL 数组]字段应包含`Attachments`数组。

  ![附件数组](assets/attachments-array.jpg)

>[!ENDSHADEBOX]


## 故障排除

### 问题：映射面板在[!UICONTROL 迭代器]模块下未显示可映射项

当[!UICONTROL 迭代器]模块没有有关数组项的结构信息时，[!UICONTROL 迭代器]模块后面的模块中的映射面板在[!UICONTROL 迭代器]模块下只显示两个项： `Total number of bundles`和`Bundle order position`。

![映射面板不显示](assets/mapping-panel-doesnt-display.png)

这是因为每个模块负责提供有关其输出的项的信息，以便这些项目可以在后续模块的映射面板中正确显示。 但是，在某些情况下，多个模块可能无法提供此信息。 例如，[!UICONTROL JSON] > [!UICONTROL 解析JSON]或[!UICONTROL Webhook] > [!UICONTROL 自定义Webhook]模块缺少数据结构将无法提供相关信息。

#### 解决方案

解决方案是手动执行场景。 这将强制模块创建输出。 然后，Fusion可以将此输出的格式应用于场景中的后续模块。

例如，某个方案包含不带数据结构的[!UICONTROL JSON] > [!UICONTROL 解析JSON]模块。

![解析JSON](assets/json-parse-json.png)

连接到此JSON模块的[!UICONTROL 迭代器]模块无法将模块的输出映射到[!UICONTROL 迭代器]模块的设置面板中的Array字段。

![连接迭代器模块](assets/connect-iterator-module.png)

要解决此问题：

在方案编辑器中手动启动方案。

>[!NOTE]
>
>要阻止运行整个方案，您可以：
>
>* 在[!UICONTROL JSON] > [!UICONTROL 解析JSON]模块后取消模块链接，以防止流进一步继续。
>  >   或
>* 右键单击[!UICONTROL JSON] > [!UICONTROL 分析JSON]模块，然后从上下文菜单中选择&#x200B;**[!UICONTROL 仅运行此模块]**&#x200B;以仅执行[!UICONTROL JSON] > [!UICONTROL 分析JSON]模块。

执行[!UICONTROL JSON] > [!UICONTROL 解析JSON]后，它可以向所有后续模块（包括迭代器模块）提供有关其输出的信息。 然后，迭代器设置中的映射面板会显示以下项目：

![映射面板显示项目](assets/mapping-panel-displays-items.png)

此外，在[!UICONTROL 迭代器]模块之后连接的模块中的映射面板将显示数组中包含的项：

![包含在数组中的项](assets/items-contained-in-array.png)
