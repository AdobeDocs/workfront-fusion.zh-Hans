---
title: 添加错误处理
description: 当在执行场景期间发生错误时，通常是因为服务因故障而不可用、服务以意外数据响应或输入数据验证失败。
author: Becky
feature: Workfront Fusion
exl-id: 82ddaf73-ecf9-4fd6-8f8e-909351023c77
source-git-commit: d7072a2dca50bf47f20d1f25dba4d3fb819d3ddc
workflow-type: tm+mt
source-wordcount: '1152'
ht-degree: 9%

---

# 添加错误处理

在执行场景期间可能会出错。

例如，错误可能是由于：

* 由于故障，服务不可用
* 服务使用意外数据做出响应
* 验证输入数据失败
* 其他原因

如果模块在场景执行期间遇到错误，并且没有附加到模块或其路由的错误处理路由，则执行默认错误处理逻辑。

通过将错误处理程序添加到模块或路由，可以将默认错误处理逻辑替换为您自己的错误处理逻辑。 Adobe Workfront Fusion提供了五个不同的指令，这些指令可以在错误处理程序路由的末尾插入。

有关默认错误处理的详细信息，请参阅[错误类型](/help/workfront-fusion/references/errors/error-processing.md)。

有关错误处理指令的详细信息，请参阅[错误处理指令](/help/workfront-fusion/references/errors/directives-for-error-handling.md)。

>[!NOTE]
>
>Workfront Fusion支持路由级别的错误处理，允许您为每个路由定义一次错误处理逻辑，而不是将错误处理程序附加到每个单独的模块。
>由于路由级别的错误处理是一种更可扩展、更一致和更简洁的错误管理方法，尤其是在高级、多分支自动化中，因此我们建议使用路由级别的错误处理作为最佳实践。

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

## 错误处理程序位置和层次结构

您可以将错误处理程序添加到单个模块或路由器。

附加到模块的错误处理程序仅在处理特定模块时遇到错误时触发。

连接到路由器的错误处理程序会触发该路由器路由上的任何模块遇到的错误。 这包括在任何在其自己的路由器上没有错误处理程序的子路由上遇到的错误。

错误由以下层次结构处理：

1. 模块
2. 路由器
3. 父路由器
4. 默认错误处理

>[!BEGINSHADEBOX]

### 示例

请考虑以下示例场景：

![显示路由和错误处理程序的示例方案](assets/error-handling-route-example-with-numbers.png)

1. 此模块具有错误处理程序。 此模块上的任何错误都由Commit指令处理。
1. 此模块没有错误处理程序。 如果此模块遇到错误，该错误将由创建模块路由的路由器上的处理程序处理。 此模块上的任何错误都由Rollback指令处理。
1. 此模块没有错误处理程序，创建模块路由的路由器也没有错误处理程序，但下一台路由器上有错误处理程序。 此模块上的任何错误都由Break指令处理。

>[!NOTE]
>
>* 如果模块、其路由器或任何父路由器上没有错误处理程序，该模块上的任何错误都将通过默认错误处理来处理。
>* 要创建全局错误处理程序，请在方案开头附近创建一个路由器，并将错误处理附加到该路由器。


>[!ENDSHADEBOX]

## 添加错误处理程序

您可以将错误处理程序添加到模块或路由器。

* [向模块添加错误处理程序](#add-an-error-handler-to-a-module)
* [向路由器添加错误处理程序](#add-an-error-handler-to-a-router)

### 向模块添加错误处理程序

向模块添加错误处理程序：

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要添加错误处理路由的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 右键单击要添加错误处理程序路由的模块，然后选择&#x200B;**[!UICONTROL 添加错误处理程序]**：

   ![错误处理程序路由](assets/error-handler-route.png)

   错误处理程序路由已添加到模块。 如果该模块是路由中的最后一个模块，则错误处理程序将直接跟踪该模块。 如果模块之后有更多的模块，则会添加单独的错误处理程序路由。

   错误处理模块显示指令列表，以及在您的方案中使用的应用程序。

   ![错误路由](assets/error-route.png)

1. 选择指令之一。

   或

   将一个或多个模块添加到错误处理程序路由。

   如果向路由添加更多模块，则缺省情况下将应用“忽略”指令。 如果出现错误，则会处理该路由上的后续模块。

   有关指令的详细信息，请参阅本文中的[处理指令](#error-handling-directives)时出错。

1. （可选）将过滤器添加到错误处理路由。 有关说明，请参阅[将筛选和嵌套添加到错误处理路由](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md)。

>[!NOTE]
>
>请注意，错误处理程序路由由透明圆组成，而常规路由由实心圆组成。

### 向路由器添加错误处理程序

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要添加错误处理路由的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 右键单击要添加错误处理程序路由的路由器，然后选择&#x200B;**[!UICONTROL 添加错误处理程序]**：

   ![错误处理程序路由](assets/error-handler-on-router.png)

   已向路由器添加错误处理程序路由。

   错误处理模块显示指令列表，以及在您的方案中使用的应用程序。

   ![错误路由](assets/error-handler-route-from-router.png)

1. 选择指令之一。

   或

   将一个或多个模块添加到错误处理程序路由。

   如果向路由添加更多模块，则缺省情况下将应用“忽略”指令。 如果出现错误，则会处理该路由上的后续模块。

   有关指令的详细信息，请参阅本文中的[处理指令](#error-handling-directives)时出错。

1. （可选）将过滤器添加到错误处理路由。 有关说明，请参阅[将筛选和嵌套添加到错误处理路由](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md)。

## 处理指令时出错

这些指令简要说明如下。 有关详细信息，请参阅错误处理[的](/help/workfront-fusion/references/errors/directives-for-error-handling.md)指令。

有五个指令，可根据错误后场景执行是否继续将其分组为以下类别。

以下指令可确保场景执行继续：

* **[!UICONTROL 恢复]**：允许您为出现错误的模块指定替代输出。 方案执行状态标记为成功。
* **[!UICONTROL 忽略]**：忽略该错误。 方案执行状态标记为成功。
* **[!UICONTROL 中断]**：将输入存储到未完成执行的队列。 方案执行状态标记为警告。

  有关详细信息，请参阅[查看并解决未完成的执行](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)。

如果发生错误时应停止场景执行，请使用以下指令之一：

* **[!UICONTROL 回滚]**：立即停止方案执行并将其状态标记为错误。
* **[!UICONTROL 提交]**：立即停止方案执行并将其状态标记为成功。

## 资源

有关错误处理的详细信息，请参阅：

* [Adobe Workfront Fusion中错误处理的指令](/help/workfront-fusion/references/errors/directives-for-error-handling.md)
* [为错误处理路由添加筛选和嵌套](/help/workfront-fusion/create-scenarios/config-error-handling/advanced-error-handling.md)
