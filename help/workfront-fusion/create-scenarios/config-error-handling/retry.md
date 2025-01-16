---
title: 配置重试错误处理解决方法
description: 有时，如果故障原因可能很快得到解决，则重新执行失败模块会很有用。
author: Becky
feature: Workfront Fusion
exl-id: 08e19a1a-7ca9-4c79-a165-f200048a5cda
source-git-commit: 0668441df8405610488e3e33658635e4cc7db270
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# 配置`retry`错误处理解决方法

有时，如果故障原因可能很快得到解决，则重新执行失败模块会很有用。

Adobe Workfront Fusion当前不提供`retry`错误处理指令，但有两种变通方法可用于模拟`retry`功能。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront计划：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront计划：包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## [!UICONTROL Retry]错误处理指令的解决方法

Workfront Fusion当前不提供`retry`错误处理指令。 使用以下变通方法之一来模拟重试功能。

有关说明，请参阅错误处理](/help/workfront-fusion/references/errors/directives-for-error-handling.md)的[指令。

* [使用Break指令](#use-the-break-directive)
* [使用中继器模块](#use-the-repeater-module)

### 使用Break指令

Break指令执行时，场景执行的状态存储在未完成执行的队列中。 如果发生这种情况，您可以手动解决未完成的执行。

有关说明，请参阅[解决Break指令处理的错误](/help/workfront-fusion/create-scenarios/config-error-handling/resolve-error-from-break-directive.md)

有关解决未完成执行的说明，请参阅[查看并解决未完成的执行](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)。

#### 缺点

* 最小重试间隔为一分钟。
* 如果模块正在处理多个捆绑包并且捆绑包处理失败，则将部分执行（仅导致错误的捆绑包）移动到不完整执行文件夹并根据[!UICONTROL Break]指令设置计划重试。 但是，当前执行继续，模块将继续处理后续捆绑包。

  要在成功解析存储在“未完成执行”文件夹中的执行之前阻止再次执行方案，请在[!UICONTROL Scenario settings]中启用“[!UICONTROL Sequential processing]”选项。

有关未完成执行的详细信息，请参阅[查看并解决未完成的执行](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)。

### 使用中继器模块

中继器模块的解决方法更复杂，但更可自定义。

#### 配置错误处理程序路由

1. 单击左侧面板中的&#x200B;**[!UICONTROL Scenarios]**&#x200B;选项卡。
1. 选择要添加解决方法的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击&#x200B;**流量控制**&#x200B;图标![流量控制](assets/flow-control-icon.png)并选择&#x200B;**中继器**。
1. 在中继器模块中，将&#x200B;**[!UICONTROL Repeats]**&#x200B;字段设置为您希望方案重试的最大次数。
1. 在&#x200B;**[!UICONTROL Repeater]**&#x200B;模块后附加可能失败的模块。
1. 将错误处理程序路由附加到可能失败的模块。

   有关说明，请参阅[添加错误处理](/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md)。
1. 将&#x200B;**[!UICONTROL Tools]>[!UICONTROL Sleep]**&#x200B;模块添加到错误处理程序路由，并将其&#x200B;**[!UICONTROL Delay]**&#x200B;字段设置为重试尝试之间的秒数。

1. 在&#x200B;**[!UICONTROL Tools]>[!UICONTROL Sleep]**&#x200B;模块后添加&#x200B;**[!UICONTROL Ignore]**&#x200B;指令。
1. 继续[配置默认路由](#configure-the-default-route)。

#### 配置默认路由

1. 将&#x200B;**[!UICONTROL Tools]>[!UICONTROL Set variable]**&#x200B;模块添加到可能失败的模块之后的单独（非错误处理程序）路由中，并将其配置为将该模块的结果存储在名为的变量中，例如`Result`。

1. 在&#x200B;**[!UICONTROL Tools]>[!UICONTROL Set variable]**&#x200B;之后添加&#x200B;**[!UICONTROL Array aggregator]**&#x200B;模块，并在其Source模块字段中选择&#x200B;**[!DNL Repeater]**&#x200B;模块。

1. 将&#x200B;**[!UICONTROL Tools]>[!UICONTROL Get variable]**&#x200B;模块添加到&#x200B;**[!UICONTROL Array aggregator]**&#x200B;模块之后，并将`Result`变量的值映射到该模块。

1. 在&#x200B;**[!UICONTROL Repeater]**&#x200B;模块和可能失败的模块之间插入&#x200B;**[!UICONTROL Tools]>[!UICONTROL Get variable]**&#x200B;模块，并将`Result`变量的值映射到它。

1. 在此&#x200B;**[!UICONTROL Tools]>[!UICONTROL Get variable]**&#x200B;模块与可能失败的模块之间插入一个过滤器，以仅在`Result`变量不存在时继续。

>[!BEGINSHADEBOX]

**示例：**

在此示例方案中，[!UICONTROL HTTP] > [!UICONTROL Make a request]模块表示可能失败的模块：

![](assets/http-make-request.png)

>[!ENDSHADEBOX]

如果可能失败的模块的结果过于复杂，无法存储在一个简单的变量中，则可以使用数据存储来存储和检索结果。 数据存储将只包含一个记录。 例如，记录的键可以是`Result`。

有关数据存储区的详细信息，请参阅[数据存储](/help/workfront-fusion/create-scenarios/map-data/data-stores.md)。

#### 缺点

* 此解决方法比较复杂。
* 此解决方法需要使用更多操作。

## 资源

* 有关中继器模块和中断指令的详细信息，请参阅[流控制](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/flow-control.md)。
* 有关获取变量模块的详细信息，请参阅[工具](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/tools-modules.md)。
