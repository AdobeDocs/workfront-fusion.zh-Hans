---
title: 解决由 Break 指令处理的错误
description: 有时，如果故障原因可能很快得到解决，则重新执行失败模块会很有用。
author: Becky
feature: Workfront Fusion
exl-id: d568942c-2cd5-430c-bdbf-e1496da25b50
TQID: https://experienceleague.adobe.com/2Gw-2VZoILhCB-96exxTRry7S5mgOetJ-lkl-APgypI
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 516
ht-degree: 20%

---

# 解决由 Break 指令处理的错误

当错误由Break指令处理时，会在Incomplete executions文件夹中创建记录。 此记录存储场景执行的状态以及来自先前模块的数据。 记录引用了引发错误的模块，并包含有关模块接收到的输入数据的信息。 对于每个导致错误的数据包，将创建一个单独的记录。

有关详细信息，请参阅[查看并解决未完成的执行](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md)。

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

## 解决由Break指令导致的错误

您可以通过更新场景（如果需要）并运行一次来手动解决该错误。

您还可以将方案配置为通过重新执行方案来自动处理不完整的执行。 要配置模块以处理未完成的执行，请执行以下操作：

1. 单击左侧面板中的&#x200B;**[!UICONTROL 方案]**&#x200B;选项卡。
1. 选择要添加解决方法的方案。
1. 单击方案上的任意位置以进入方案编辑器。
1. 单击&#x200B;**流量控制**&#x200B;图标![流量控制](assets/flow-control-icon.png)并选择&#x200B;**中断**。
1. 在Break模块内，启用&#x200B;[!UICONTROL **自动完成执行**]&#x200B;选项。
1. 在&#x200B;**尝试次数**&#x200B;字段中，输入或映射您希望模块重试执行的最大尝试次数

   此数字必须介于1和100之间。
1. 在&#x200B;**尝试间隔**&#x200B;字段中，输入或映射每次重试间隔的分钟数。

启用此选项后，当发生错误时，将检索不完整的执行（在[!UICONTROL 尝试间隔]字段中指定的时间之后）并使用原始输入数据执行。 这将重复执行，直到模块执行完成且无错误或达到指定的尝试次数为止。

>[!NOTE]
>
>如果初始重试尝试失败，重试间隔将每隔一次尝试以指数方式增加。


启用自动完成执行选项后，场景运行将标记为“成功”，因为中断错误处理程序的自动重试正在自动处理该问题。 在这种情况下，用户不会收到有关失败运行的电子邮件。

关闭自动完成执行选项后，该运行将标记为“警告”。

在“不完整的执行”下存储的执行存在一些异常，对于某些错误类型，无法自动重试场景执行。

## 资源

有关详细信息，请参阅配置场景设置一文中的[允许存储不完整的执行](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions)。
