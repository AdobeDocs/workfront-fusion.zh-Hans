---
title: 使用自定义函数映射数据
description: 在映射项目时，您可以使用函数创建简单或复杂的公式。
author: Becky
feature: Workfront Fusion
exl-id: dc4e697a-a65c-48bc-99de-8e26fbeb7ba7
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
    internal-label: Workfront
feature_v2:
  - id: c3a155b4-a54b-4a82-a3d2-c8f0f971673e
    internal-label: Workfront Fusion
source-git-commit: c716296d771974ffdb59e916f9865c9efb2ad5a9
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 11%
---
# 使用自定义函数映射数据

您可以在Fusion的“函数”区域中创建自定义函数。 然后，以Adobe App Builder模块的形式将这些函数添加到场景中。

由于自定义函数可通过Adobe App Builder使用，因此您的组织必须具有Adobe App Builder许可证才能使用它们。

与大多数场景元素一样，自定义函数由团队拥有。

函数是简单的JavaScript函数。 要在函数逻辑中包含变量或依赖项，请使用包。

有关包的信息，请参阅[使用自定义函数包](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md)。

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

您可以在函数区域中创建可在多个方案中使用的自定义函数，也可以在单个方案中配置自定义函数。

* [创建要在多个方案中使用的自定义函数](#create-a-custom-function-to-use-in-multiple-scenarios)
* [在场景中创建自定义函数](#create-a-custom-function-within-a-scenario)

### 创建要在多个方案中使用的自定义函数

可以在Workfront Fusion的函数区域中配置可以在多个场景中使用的自定义函数。 配置函数后，您可以使用Adobe App Builder连接器将其添加到方案。

* [初始化运行时环境](#initialize-your-runtime-environment)
* [连接现有App Builder项目](#connect-an-existing-app-builder-project)
* [在函数区域创建自定义函数](#create-a-custom-function-in-the-functions-area)

#### 初始化运行时环境

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

#### 连接现有App Builder项目

当Fusion创建App Builder项目时，它将为您处理运行时设置。 如果您的团队已有一个在使用Fusion之前创建的App Builder项目，则必须通过创建使用该项目的运行时命名空间和凭据的App Builder连接来手动连接该项目。 您无需重新创建项目。

>[!NOTE]
>
>您在Fusion中输入的凭据是运行时凭据。 它们不是您的Adobe登录详细信息。 确保下载的配置文件安全，并且不共享其`auth`值。

1. 在Fusion中，选择需要连接的团队。
1. 单击左侧面板中的&#x200B;**连接**&#x200B;选项卡，然后单击&#x200B;**创建连接**。
1. 将Select **Adobe App Builder**&#x200B;作为连接类型，并输入标识现有项目的名称。
1. 在[Adobe Developer Console](https://developer.adobe.com/console)中，打开现有项目，然后选择要连接的工作区。
1. 在项目概述中，单击&#x200B;**全部下载**&#x200B;以下载工作区配置JSON文件，然后在文本编辑器中打开该文件。
1. 在文件的`runtime`部分中，找到`namespace`值。 在Fusion中，在&#x200B;**命名空间**&#x200B;字段中输入它。
1. 在`runtime`部分中，找到`auth`值。 其格式为`username:password`。

   * 在Fusion中，在&#x200B;**用户名**&#x200B;字段中输入冒号之前的部分。
   * 在Fusion中，在&#x200B;**密码**&#x200B;字段中输入冒号后的部分。

1. 单击&#x200B;**继续**&#x200B;以保存连接。
1. 返回Fusion中的&#x200B;**函数**&#x200B;选项卡，并根据需要刷新页面。

有关连接字段的详细信息，请参阅[Adobe App Builder模块](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md#create-a-connection-to-adobe-app-builder)。

#### 在函数区域创建自定义函数

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

### 在场景中创建自定义函数

要在方案中创建自定义函数，请在Adobe App Builder连接器中使用&#x200B;**运行自定义代码块**&#x200B;模块。

有关说明，请参阅[Adobe App Builder模块](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md)。

## 向方案添加自定义函数

要向场景添加自定义函数，请使用Adobe App Builder连接器。

有关说明，请参阅[Adobe App Builder模块](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-app-builder.md)。

