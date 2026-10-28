---
title: 保存和重用包含代码片段的方案部分
description: 代码片段是一组您保存的模块，以便在其他情况下可以重复使用。 您可以组织、共享、导入和导出代码片段。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 5b049973107f23e46d1aadae8e0d157839e8a7f3
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 15%
---

# 保存和重用包含代码片段的方案部分

>[!NOTE]
>
>此功能仅在新的方案编辑器体验中可用。 有关详细信息，请参阅文章场景编辑器中的[新体验和经典体验](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)。

代码片段是一组模块，您可以将其另存为单元。 您可以向其他方案添加代码片段，这样您就不必多次构建方案的相同部分。

使用“代码片段”面板，您可以搜索、标记、预览、固定代码片段并对代码片段进行排序；将它们拖放到场景中；导入和导出代码片段；与团队或组织共享代码片段，或将副本发送给其他用户。

## 访问权限要求

+++ 展开可查看本文所述功能的访问权限要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 包</td> 
   <td> <p>任意 Adobe Workfront Workflow 包以及任意 Adobe Workfront 自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime 和 Select 包，且需额外购买 Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 许可证</td> 
   <td> <p>标准</p><p>工作版或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 创建代码片段

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择包含要保存的模块的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 按住Shift并单击要包含在代码片段中的任何模块。
1. 右键单击其中一个选定的模块，然后选择创建代码片段。
1. 输入代码片段的名称。
1. 单击&#x200B;**保存**

## 向场景添加代码片段

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要添加代码片段的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击控件区域中的&#x200B;**代码片段**&#x200B;图标![代码片段](assets/snippets-icon.png)。

   您可能需要单击“控件”区域中的三个圆点图标来查看“代码片段”图标。

1. （可选）选择要预览的代码片段。
1. 单击代码片段以将其添加到编辑器。
1. 将代码片段连接到场景。
1. 更新代码片段中的任何字段以使用添加了该代码片段的方案。

## 组织代码片段

在“代码片段”面板中，您可以：

* 搜索代码片段。
* 固定您经常使用的代码片段。
* 将代码片段导出为JSON文件。
* 与其他组织、团队或用户共享代码片段。
* 在将代码片段添加到场景之前对其进行预览。
* 对代码片段列表进行排序。
  <!--* Add tags to a snippet, and use tags to find it later.-->

## 共享代码片段

您可以与团队或组织共享代码片段，或直接将副本发送给其他用户。

您可以：

* **与团队或组织共享**：共享该代码片段，以便其他成员可以使用。
* **将副本发送给用户**：将副本发送给一个用户。 用户会收到自己的副本。


1. 单击控件区域中的&#x200B;**代码片段**&#x200B;图标![代码片段](assets/snippets-icon.png)。
1. 将鼠标悬停在要共享的代码片段上，然后单击出现时的共享图标。
1. 选择您是与其他组织、团队还是用户共享该代码片段。
1. 单击&#x200B;**下一步**。
1. 选择要与其共享代码片段的组织或团队，或输入要与其共享代码片段的用户的用户ID。
1. 单击&#x200B;**共享**。

与您共享的代码片段显示在“代码片段”面板的&#x200B;**与我共享**&#x200B;选项卡上。

## 导入和导出代码片段

您可以将代码片段导出到JSON文件，并将其导入到其他方案或环境中。

1. 单击控件区域中的&#x200B;**代码片段**&#x200B;图标![代码片段](assets/snippets-icon.png)。
1. 将鼠标悬停在要共享的代码片段上，然后单击显示的导出图标。
