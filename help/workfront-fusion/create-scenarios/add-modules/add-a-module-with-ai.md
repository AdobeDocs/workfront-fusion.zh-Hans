---
title: 使用AI生成场景区段
description: 您可以使用AI输入文本提示，描述需要场景区段执行的操作。 然后，Fusion将生成一个或多个执行这些操作的模块，您可以在场景中使用这些模块。
author: Becky
feature: Workfront Fusion
exl-id: d231e33a-6033-4e3c-b1d4-7034797c45a5
source-git-commit: 9d29abc82a3bb09affc4d17d7ea214d7bb850294
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 1%

---

# 使用AI生成场景区段

<!--DO NOT DELETE - linked through CSH-->

<!--Check if this is in GA before repo goes live. If not, hide this article.-->

<!--Check if they need to have signed the rider and stuff-->

您可以使用AI输入文本提示，描述需要场景区段执行的操作。 然后，Fusion将生成一个或多个执行这些操作的模块，您可以在场景中使用这些模块。

生成的方案区段包含用于单个连接器的模块。 要为不同的连接器生成模块，请创建单独的提示，然后加入方案中的方案区段。

与从AI生成的任何内容一样，我们建议您仔细检查并测试生成的模块，以确保它们按预期执行。

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
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

您的组织必须满足以下先决条件才能使用此功能：

* 贵组织必须已参与Workfront AI助理Beta计划。
* Adobe必须拥有已签署的AdobeGen AI协议，才能为贵组织文件。

  有关签署协议的更多信息，请参阅Workfront文档中的AI Assistant概述一文中的[签署AdobeGen AI协议](https://experienceleague.adobe.com/zh-hans/docs/workfront/using/basics/ai-assistant/ai-assistant-overview#sign-the-adobe-gen-ai-agreement)。

## 当前支持的AI模块应用程序

Fusion AI当前可以生成连接到以下应用程序的模块：

* Adobe Firefly
* Azure OpenAI
* Microsoft Graph
* Adobe Workfront规划
* Adobe Analytics
* Adobe PDF服务
* AdobeMarketo
* AdobeFrame.io
* Dropbox
* NetSuite
* Google 日历
* 阿特拉西安·吉拉
* GitLab
* Spotify
* 比特桶
* OpenAI
* Slack

## 生成模块

1. 单击左侧面板中的&#x200B;**[!UICONTROL Scenarios]**&#x200B;选项卡。
1. 选择要添加模块的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击屏幕右上角附近的&#x200B;**AI助手**&#x200B;图标![AI助手图标](assets/ai-assistant-icon.png)。
1. 在AI助手面板中输入文本提示。

   有关提示的提示，请参阅本文中的[为方案区段创建提示的提示](#tips-for-creating-prompts-for-scenario-segments)。

   AI Assistant生成模块或模块集。
1. （视情况而定）如有必要，请将应用程序的API令牌添加到模块中。
1. 检查模块，确保已针对相应的应用程序和操作配置它们。
1. （视情况而定）如果生成的场景部分未附加到场景，请将其拖动到适当位置。

我们建议测试这些模块以确保它们按预期执行。

## 有关为场景区段创建提示的提示

文本提示应至少包括以下信息：

* 要连接的应用程序
* 要执行的一个或多个操作

>[!IMPORTANT]
>
>您可以一次生成多个模块，但一次只能为一个应用程序生成模块。

>[!BEGINSHADEBOX]

**示例**：

* `Delete the records 'xyz-123', 'xyz-456', 'xyz-789' from Adobe Workfront Planning`
这包括应用程序`Workfront Planning`和操作`delete records`。 此提示将创建三个模块，每个要删除的记录各一个。
* `Change campaign summary of the record 'xyz-123' from Adobe Workfront Planning`
这包括应用程序`Workfront Planning`和操作`change campaign summary`。
* `Get all field details in the record type with ID 'test-record' from Adobe Workfront Planning`
这包括应用程序`Workfront Planning`和操作`get field details`。

以下示例不正确：

* `Generate an image in Adobe Firefly and upload it to Dropbox`

  此示例不正确，因为它包含多个应用程序

>[!ENDSHADEBOX]

创建文本提示时，请考虑以下事项：

* 使用直接、简单的语言。
* 检查并测试您的场景区段。 如果它未按预期执行，请优化您的提示并重试。
