---
title: 用于创建方案的工作流
description: 按照此常规工作流创建方案
author: Becky
feature: Workfront Fusion
exl-id: 49f8edd7-e29a-4ead-9134-a9f0d1cc244d
source-git-commit: 0029e6a79c6fb7479ddd0948c773349efa075403
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# 用于创建方案的工作流

根据贵组织的需求构建方案，并使用应用程序和模块满足您的用例要求。 但是，无论使用案例如何，创建场景时都会遵循相同的基本工作流。 本文介绍了创建场景的基本过程。


* [创建方案并为其命名](#create-and-name-the-scenario)
* [添加并配置第一个模块](#configure-the-first-module)
* [创建连接](#create-connections)
* [添加和配置其他模块](#add-and-configure-additional-modules)
* [在模块之间映射数据](#map-data-between-modules)
* [配置路由](#configure-routing)
* [配置错误处理](#configure-error-handling)
* [配置方案设置](#onfigure-scenario-settings)
* [测试和修订](#test-and-revise)
* [激活方案](#activate-the-scenario)

键盘快捷键



## 创建方案并为其命名

1. 登录您的[!DNL Workfront Fusion]帐户。
1. 单击左侧面板中的&#x200B;**[!UICONTROL Scenarios]** ![方案图标](assets/scenarios-icon.png)。

   >[!NOTE]
   >
   >如果未看到左侧导航面板或其图标，请单击菜单![菜单](assets/main-menu-icon-left-nav.png)图标。

1. （可选）在&#x200B;[!UICONTROL **文件夹**]&#x200B;面板中，单击&#x200B;**[!UICONTROL Add folder]**&#x200B;图标![添加文件夹图标](assets/add-folder-icon.png)，然后为第一个文件夹键入诸如“实践方案”之类的名称。

1. （可选）打开文件夹，然后单击页面右上角的&#x200B;**[!UICONTROL Create a new scenario]**。

1. 选择左上角的&#x200B;**[!UICONTROL New scenario]**&#x200B;占位符名称，然后键入诸如“Practice scenario 1”之类的名称。

   ![命名方案](assets/name-the-scenario.png)

1. 继续[连接下面的第一个模块](#2-connect-the-first-module)。

## 添加并配置第一个模块

方案的第一个模块是触发器模块，当满足某些条件时，该模块将启动方案。

有关将第一个模块添加到方案的说明，请参阅将模块添加到方案一文中的[将第一个模块添加到方案](/help/workfront-fusion/create-scenarios/add-modules/add-a-module-basic.md#add-the-first-module-to-a-scenario)。

有关配置模块的说明，请参阅[配置模块](/help/workfront-fusion/create-scenarios/add-modules/configure-a-modules-settings.md)

## 创建连接

配置模块时，必须输入或创建连接。 模块将使用此连接及其包含的权限来访问应用程序中的日期。

有关如何创建连接的基本说明，请参阅[创建连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)。

有关涉及Google、Microsoft或没有专用连接器的应用程序的特定用例，请参阅[连接到应用程序：文章索引](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-apps-toc.md)下的其他文章。

## 添加和配置其他模块

继续添加和配置其他模块。

有关添加模块方法的说明，请参阅[添加模块：文章索引](/help/workfront-fusion/create-scenarios/add-modules/add-modules-toc.md)下列出的文章。

## 在模块之间映射数据

您可以将先前模块的输出用作后续模块的输入。 例如，您可以在一个模块中创建Workfront项目，并在后续模块中将文档上传到该模块。

有关说明，请参阅[映射数据：文章索引](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md)下的文章。

## 配置路由

工艺路线允许方案根据数据值执行不同的操作。

有关说明，请参阅[添加路由器模块并配置路由](/help/workfront-fusion/create-scenarios/add-modules/router-module.md)。

## 配置错误处理

错误处理允许场景从错误中恢复。 您可以选择希望场景在不同错误情况下做出何种反应。

有关说明，请参阅[添加错误处理](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md)。

## 配置方案设置

您可以为整个方案配置设置，例如计划方案、进行注释或确定数据存储方式。

有关说明，请参阅[配置方案设置：文章索引](/help/workfront-fusion/create-scenarios/config-scenarios-settings/config-scenario-settings-toc.md)下的文章。

## 测试和修订

通过测试方案，可确定方案是否按预期工作。 然后，您可以根据结果修订场景，然后重新测试。

1. 单击方案编辑器左下角的&#x200B;**[!UICONTROL Run once]**。
1. 场景运行完毕后，单击每个模块上方的执行检查器气泡可查看信息输入和该模块的输出。

   * 有关读取方案执行信息的一般信息，请参阅[方案执行流程](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)。
   * 有关已处理捆绑包的信息，请参阅[方案执行、周期和 [!DNL Adobe Workfront Fusion]](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md)中的阶段。

1. 在[!DNL Workfront Fusion]中，单击左下角附近的&#x200B;**[!UICONTROL Save]** ![保存图标](assets/save-icon.png)以保存方案进度。

   >[!IMPORTANT]
   >
   >在磨练和测试场景时经常保存。

## 激活方案

此示例方案没有触发器模块。 如果您将这种情况用于实际数据，则它将以触发模块开头，您的最后一个操作是激活它。 在激活方案后，默认情况下，它每15分钟运行一次。 您可以通过定义运行的时间和频率来更改此设置。

有关激活方案的详细信息，请参阅[激活或停用方案](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md)。

有关计划的信息，请参阅[计划方案](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。

## Workfront Fusion场景键盘快捷键

创建或编辑方案时，可以使用以下键盘快捷键：

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <thead> 
  <tr> 
   <th> <p>操作</p> </th> 
   <th>[!DNL Windows]</th> 
   <th> <p>[!DNL MacOS]</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save] </td> 
   <td>Ctrl+Shift+S</td> 
   <td><span style="font-weight: normal;">Cmd+Shift+S</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Run Once]</td> 
   <td>Ctrl+Shift+Enter</td> 
   <td><span style="font-weight: normal;">Cmd+Shift+Enter</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Open the DevTool]</td> 
   <td>F12</td> 
   <td><span style="font-weight: normal;">Ctrl+Fn+F12</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy]</td> 
   <td>Ctrl+C</td> 
   <td><span style="font-weight: normal;">Cmd+C</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Paste]</td> 
   <td>Ctrl+V</td> 
   <td><span style="font-weight: normal;">Cmd+V</span> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select multiple modules]</td> 
   <td>Shift +拖动</td> 
   <td><span style="font-weight: normal;">Shift+拖动</span> </td> 
  </tr> 
 </tbody> 
</table>



