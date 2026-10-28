---
title: 使用Live Trail查看场景运行
description: 实时跟踪会显示场景在运行时运行，将模块请求组合到一个列表中并运行活动。 您可以打开任何操作的请求和响应详细信息。
author: Becky
feature: Workfront Fusion
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
source-git-commit: 94449f8511d7480f1a4fc0ac6e8db9b067977abd
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 17%
---

# 使用Live Trail查看场景运行

实时轨迹会显示场景在运行时运行。 该功能将模块请求与运行活动合并到一个按时间顺序排列的列表中，这样您就可以在场景编辑器中跟踪一次运行，并在不离开画布的情况下查看错误情况。

>[!NOTE]
>
>此功能仅在新的方案编辑器体验中可用。 有关详细信息，请参阅文章场景编辑器中的[新体验和经典体验](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)。

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

## 打开Live路径

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要查看的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 开始运行该方案，例如，单击&#x200B;**运行一次**。



此时将在画布右侧的面板中打开Live Trail。 如果在运行期间关闭面板，则通过屏幕右侧的小选项卡，可以再次打开该面板，而不会丢失捕获的事件。

## 查看Live Trail中的事件

实时试用版列出了模块请求，并按照其发生的顺序运行活动。 您可以：

* 搜索列表。
* 按状态筛选列表。
* 在继续运行时跟踪最新事件。
* 清除当前跟踪。

## 查看请求和响应详细信息

1. 在Live Trail中，单击要查看其详细信息的请求。

   发出请求的模块将显示在画布上，并且请求和响应详细信息将在面板中打开。

1. 查看详细信息。 详细信息视图包括：

   * 模块操作之间的导航
   * 请求标头和正文
   * 响应标头和正文

1. （可选）通过单击&#x200B;**复制原始**&#x200B;或&#x200B;**复制cURL**，复制详细信息以在其他位置使用：

   * 复制请求和响应的原始报告。
   * 为请求复制cURL命令。

1. 要返回到列表，请单击面板左上角的向后箭头。

## 确保提供请求和响应详细信息

对于每次计划运行或触发运行，请求和响应详细信息都不会保留，因为它们占用大量存储。

* 运行一次会始终保留请求和响应详细信息。
* 对于方案的常规运行，在要检查的运行之前，在方案设置中打开临时调试日志。 有关详细信息，请参阅配置方案设置一文中的[临时调试日志](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#temporary-debug-logs)。

如果从执行历史记录中打开运行，并且请求和响应面板中没有任何数据，则该面板会将您定向到“临时调试日志”设置。
