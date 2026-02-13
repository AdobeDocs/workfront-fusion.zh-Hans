---
title: 使用自定义函数映射数据
description: 在映射项目时，您可以使用函数创建简单或复杂的公式。
author: Becky
feature: Workfront Fusion
source-git-commit: 109ea8a6b3c37918110dc930a19ac85ef3e6d764
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 20%

---

# 使用自定义函数映射数据

您可以在Fusion的“函数”区域中创建自定义函数。 然后，以Adobe App Builder模块的形式将这些函数添加到场景中。

由于自定义函数可通过Adobe App Builder使用，因此您的组织必须具有Adobe App Builder许可证才能使用它们。

与大多数场景元素一样，自定义函数由团队拥有。

Workfront Fusion还包括内置函数，允许您创建简单或复杂的公式。 这些函数涵盖了各种用例，包括用于数组、字符串、数字和来自之前模块的数据的函数。

有关内置函数的信息和说明，请参阅[使用内置函数映射项](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md)。

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
   <p><ul><li>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li><li>您必须拥有Adobe App Builder许可证才能使用自定义函数。</ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 配置自定义函数

自定义函数是在Workfront Fusion的函数区域中配置的。 配置函数后，您可以使用Adobe App Builder连接器将其添加到方案。

### 初始化运行时环境

在创建自定义函数之前，必须初始化运行时环境。 仅当您的团队没有任何自定义功能时，才需要执行此操作。

>[!IMPORTANT]
>
>只有有权访问Adobe App Builder的用户（IMS组织内的开发人员或系统管理员）才能执行初始化。
>
>初始化完成后，执行初始化的团队中的所有用户都可以创建和使用函数。

1. 单击左侧面板中的&#x200B;**函数** ![函数图标](assets/functions-icon.png)选项卡。

   如果尚未配置运行时，则会看到消息“未配置运行时环境”。
1. 单击&#x200B;**初始化运行时**。

   一段时间后，将出现一个“函数”列表，其中包含两个示例函数。

### 创建自定义函数

配置运行时环境后，即可开始创建自定义函数。

>[!IMPORTANT]
>
>* 您的自定义函数&#x200B;**必须**&#x200B;是JavaScript函数。
>* 您的自定义函数&#x200B;**必须**&#x200B;返回一个对象。
>* 创建自定义函数后，您无法：
>
>   * 更改其名称
>   * 查看默认参数值

1. 单击左侧面板中的&#x200B;**函数** ![函数图标](assets/functions-icon.png)选项卡。
1. 单击&#x200B;**添加函数**。
1. 输入自定义函数的名称。

   您以后将无法更改此名称。
1. 输入函数的代码。
1. 对于每个要添加的默认参数值，单击&#x200B;**添加参数**&#x200B;并输入参数名称和默认值。

   将函数添加到方案时，可以覆盖默认参数。
1. 单击&#x200B;**保存**

## 向方案添加自定义函数

要向场景添加自定义函数，请使用Adobe App Builder连接器。

有关说明，请参阅[Adobe App Builder模块](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md)。

