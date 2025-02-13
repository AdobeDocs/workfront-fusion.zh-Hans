---
content-type: reference
title: 错误类型
description: 有时，在执行场景期间可能会出错。 如果由于无法连接到服务而导致服务不可用，或者如果验证失败，则通常会发生这种情况。 本文讨论您可能会遇到的常见错误。
author: Becky
feature: Workfront Fusion
exl-id: abf5f844-d13b-416e-a8b8-2d4ee1786262
source-git-commit: d618d5c4b2306a3b940af7e402f93ced988095a3
workflow-type: tm+mt
source-wordcount: '1145'
ht-degree: 1%

---

# 错误类型

有时，在执行场景期间可能会出错。 如果由于无法连接到服务而导致服务不可用，或者如果验证失败，则通常会发生这种情况。

[!DNL Adobe Workfront Fusion]可区分几种基本错误类型。 错误的类型决定了Fusion场景的后续操作。

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
   <td> 新增：标准<p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] 许可证</td> 
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


要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关Adobe Workfront Fusion许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 连接错误

`ConnectionError`

连接错误是最常见的错误之一。 它们通常是由于多种原因（如过载、维护或中断）导致第三方服务不可用。 此错误的默认处理方式取决于遇到错误的模块。

* 如果第一个模块发生错误，则场景的执行将终止，并显示警告消息。 然后，[!DNL Workfront Fusion]反复尝试以递增的时间间隔重新运行该方案。 如果所有尝试都失败，[!DNL Workfront Fusion]将停用该方案。
* 如果连接错误发生在第一个模块以外的其他模块上，则后续步骤取决于场景高级设置中的“允许存储不完整的执行”选项：

   * 如果启用此选项，则方案的执行将移至[!UICONTROL Incomplete executions]文件夹，其中[!DNL Workfront Fusion]反复尝试以递增的时间间隔重新运行方案。 如果所有尝试都失败，执行将保留在“未完成执行”文件夹中，等待用户手动解析。

     有关未完成执行的详细信息，请参阅[查看并解决未完成的执行](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)。
   * 如果禁用了此选项，则场景的执行将结束并返回错误，然后进入回滚阶段。 然后，[!DNL Workfront Fusion]反复尝试以递增的时间间隔重新运行该方案。 如果所有尝试都失败，[!DNL Workfront Fusion]将停用该方案。

  有关“允许存储未完成的执行”设置的详细信息，请参阅配置场景设置一文中的[允许存储未完成的执行](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions)。

### 增加时间间隔

当出现错误时，增加两次尝试之间时间间隔的算法称为指数回退。 增加的时间间隔设置如下：

1. 10分钟
1. 1 小时
1. 3 小时
1. 12 小时
1. 24 小时

不断增加的时间间隔有助于防止频繁执行的场景在反复失败的尝试中使用操作。

>[!BEGINSHADEBOX]

**示例：**

方案包含[!DNL Google Sheets]触发器[!UICONTROL Watch Rows]。 由于在[!DNL Workfront Fusion]启动方案时进行了维护，[!DNL Google Sheets]在30分钟内不可用，因此无法检索新行。 场景将停止并在10分钟后重试。 由于[!DNL Google Sheets]仍然不可用，[!DNL Workfront Fusion]仍无法获取有关新行的信息。 方案的下次运行安排在1小时内。 [!DNL Google Sheets]此时再次可用，并且方案成功运行。

>[!ENDSHADEBOX]

## 数据错误

`DataError`

如果项目未正确映射，并且未通过在[!DNL Workfront Fusion]端或第三方服务端执行的验证，则会生成数据错误。

如果发生此错误，则将场景（直到模块失败）移至未完成执行文件夹，您可以在其中解决问题。 但是，场景不会停止，而是会按照其计划继续运行。 要在出现数据错误时停止方案的执行，请启用方案设置面板中的顺序处理选项。

如果尚未在方案设置中启用[!UICONTROL Allow storing incomplete executions]选项，则方案的执行会因错误而终止，并且会执行回滚。

## 重复数据错误

`DuplicateDataError`

如果[!DNL Workfront Fusion]尝试将同一捆绑包两次插入到不允许重复数据的服务中，则会生成重复数据错误。 如果发生此错误，[!DNL Workfront Fusion]将以与处理数据错误相同的方式进行。

有关详细信息，请参阅本文中的[数据错误](#data-error)。


## 访问令牌无效错误

`InvalidAccessTokenError`

当[!DNL Workfront Fusion]无法访问您在第三方服务中注册的帐户时，会发生访问令牌无效错误。 这通常发生在您在管理给定服务时撤消[!DNL Workfront Fusion]的访问权限时，但使用该服务的方案继续按计划运行。

如果发生此错误，则场景执行将立即停止。 从发生错误的模块开始的场景的其余部分移至未完成执行文件夹。

## 速率限制错误

`RateLimitError`

如果超过给定服务设置的限制，则会生成速率限制错误。 如果发生此错误，[!DNL Workfront Fusion]将以与处理连接错误相同的方式进行。

有关详细信息，请参阅本文中的[连接错误](#connection-error)。

## 不完整数据错误

`IncompleteDataError`

只有触发器出现不完整数据错误。 如果触发器无法从给定服务下载所需数据，则会生成此错误。

如果方案以`IncompleteDataError`终止，则其进一步的行为将取决于其[!UICONTROL Max number of consecutive errors]的设置。

有关详细信息，请参阅配置方案设置一文中的[连续错误数](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors)。

>[!BEGINSHADEBOX]

**示例：**

方案将[!DNL Workfront]触发器[!UICONTROL Watch Record]设置为监视文档。 场景在上传大文档（如长视频）时执行。 由于[!UICONTROL Workfront Fusion]尝试在视频仍上传到Workfront时下载视频，因此场景因`IncompleteDataError`而终止。

>[!ENDSHADEBOX]

## 运行时错误

`RuntimeError`

在场景执行期间出现且不属于这些错误类型之一的任何错误均报告为`RunTimeError`。

如果方案以`RuntimeError`终止，则其进一步的行为取决于[!UICONTROL Max number of consecutive errors]设置。

有关详细信息，请参阅配置方案设置一文中的[连续错误数](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors)。


>[!NOTE]
>
>如果方案以即时触发器启动并遇到此错误，则忽略[!UICONTROL Max number of consecutive errors]的设置，并立即停用方案。
>有关详细信息，请参阅“模块概述”一文中的[即时触发器](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers)。

## 不一致性错误

`InconsistencyError`

如果在提交或回滚阶段出现上述任何错误，则场景将终止，并出现不一致错误。

如果某个场景中出现此错误，则该场景的执行将立即停止。

## 警告

在执行场景时，您可能会收到一则警告消息，向您通知问题。 警告不会阻止方案成功完成。

例如，当超出允许的最大文件大小且禁用[!UICONTROL Enable data loss]选项时，可能会显示警告。

## 资源

有关映射的详细信息，请参阅[映射概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md)。

有关未完成执行的信息，请参阅[查看并解决未完成的执行](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)。

有关方案设置面板的信息，请参阅[配置方案设置](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md)。

有关计划的信息，请参阅[计划方案](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。

有关方案阶段的信息，请参阅[方案执行、周期和阶段](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md)。

有关启用数据丢失选项的信息，请参阅配置方案设置一文中的[启用数据丢失](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss)。
