---
title: 查看和管理方案版本
description: 您可以查看、恢复、重命名或下载方案的早期版本的Blueprint。
author: Becky
feature: Workfront Fusion
exl-id: e7fd0351-b840-422c-b861-82ae110c703b
TQID: https://experienceleague.adobe.com/xVihxZH-fwPCIkryQAQEOWgeShtPTMXth4jEl5OLdbo
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: eb4c1ed6991606928beccbb57a8a86182e58a9e7
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 14%

---

# 查看和管理方案版本

Adobe Workfront Fusion会在每次场景更改时保存场景的一个版本。

您可以查看、恢复、重命名或下载方案的早期版本的Blueprint。

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
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 查看和管理方案的版本历史记录

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]** ![方案图标](assets/scenarios-icon.png)，然后单击方案以将其打开。
1. 单击屏幕底部的[!UICONTROL 更多]图标![更多图标](assets/more-icon.png)，然后单击&#x200B;**[!UICONTROL 以前的版本]**。

   此时将显示早期版本的列表。
1. （可选）若要重命名版本，请单击该版本行上的更多菜单![更多菜单](assets/more-icon-vertical.png)，选择&#x200B;**编辑**，然后在字段中输入名称。 单击&#x200B;**保存**&#x200B;以保存新名称。

   我们建议提供一个名称，用于描述对此版本所做的更改。
1. （可选）要下载以前版本的Blueprint，请单击该版本行上的更多菜单![更多菜单](assets/more-icon-vertical.png)，然后选择&#x200B;**下载**。
1. （可选）要比较两个版本之间的更改，请单击该版本的&#x200B;**查看更改**。

   有关比较版本的详细信息和说明，请参阅本文中的[比较方案版本](#compare-scenario-versions)。
1. （可选）要还原该版本，请单击该版本行上的&#x200B;**还原**


   >[!NOTE]
   >
   >方案的还原版本不会自动保存。 如果要保存方案的恢复版本，则必须手动保存。



## 比较方案版本

&#x200B;AEM
视图更改功能并排显示两个方案版本之间的差异，这样您可以在决定恢复旧版本之前查看确切的更改内容。

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]** ![方案图标](assets/scenarios-icon.png)，然后单击方案以将其打开。
1. 单击屏幕底部的[!UICONTROL 更多]图标![更多图标](assets/more-icon.png)，然后单击&#x200B;**[!UICONTROL 以前的版本]**。

   此时将显示早期版本的列表。
&#x200B;AEM
1. 单击要查看的方案版本的&#x200B;**查看更改**。
1. 将打开&#x200B;**查看更改**&#x200B;视图，并将该版本与当前方案进行比较。

   此时将打开查看更改面板，并排显示两个方案版本。

   * 在左侧，您会看到当前版本。
   * 在右侧，您可以看到您点击的版本。 这是您可以恢复的版本。

   若要了解更改，请参阅本文中的[检查更改](#examine-changes)。

1. 要为任一方选择其他版本，请单击面板顶部附近的&#x200B;**比较自**&#x200B;或&#x200B;**比较至**&#x200B;下拉列表，然后选择其他方案版本。
1. 要交换边，请在方案之间单击&#x200B;**⇄**&#x200B;按钮。
1. 要还原到右侧的方案，请单击&#x200B;**还原到所选版本**

   已还原的版本将另存为新版本，因此将来可以还原。

   若要还原到当前位于左侧的方案，请交换侧面，使其位于右侧，然后单击&#x200B;**还原到所选版本**。


### 检查更改

&#x200B;AEM
每个更改都显示在它所属的一侧，并以恢复操作所显示的内容着色
执行：

* 红色（左）：此更改不在右侧的版本中，如果版本已恢复，将删除该更改。
* 绿色（右）：此更改位于右侧的版本中，如果版本已恢复，则会添加此更改。

如果某些内容发生了更改，该值会在左侧以红色显示，在右侧以绿色显示，而不是删除或添加。
&#x200B;AEM
更改将分组为多个部分：
&#x200B;AEM

* **方案**：名称、说明和类型。
* **方案设置**：计划和处理选项。
* **模块**：已添加、已移除、已移动或重新配置模块。
* **流**：已添加、已删除或重新排序的区段。
* **路由器路由**：路由及其内容。
* **错误处理程序**：错误处理分支。
* **孤立组**：画布上已断开连接的模块。
&#x200B;AEM
如果两个版本相同，视图将显示消息/ **未找到差异**。
&#x200B;AEM


