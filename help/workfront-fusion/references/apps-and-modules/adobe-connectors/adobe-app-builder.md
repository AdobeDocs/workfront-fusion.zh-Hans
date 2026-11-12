---
title: Adobe App Builder模块
description: Adobe App Builder连接器允许您在场景中使用自定义函数。
author: Becky
feature: Workfront Fusion
exl-id: 92661a0c-436b-4fbd-808a-a4fbe3cd2339
source-git-commit: 02c396f33b6398635462bac8741f446eb82bf5a9
workflow-type: tm+mt
source-wordcount: '754'
ht-degree: 16%
---
# Adobe App Builder模块

您可以在Fusion的“函数”区域中创建自定义函数。 然后，以Adobe App Builder模块的形式将这些函数添加到场景中。

由于自定义函数可通过Adobe App Builder使用，因此您的组织必须具有Adobe App Builder许可证才能使用它们。

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

## 创建与Adobe App Builder的连接

该连接使用App Builder项目工作区的Adobe I/O Runtime凭据。 在创建连接之前，请从Adobe Developer Console获取这些凭据。

### 获取运行时凭据

1. 使用拥有您的Adobe Developer Console许可证的组织登录到[App Builder](https://developer.adobe.com/console)。
1. 打开包含您的函数的App Builder项目，然后选择要连接的工作区（例如，**生产**）。
1. 单击右上角的&#x200B;**全部下载**&#x200B;以下载工作区配置JSON文件。
1. 打开文件并找到`runtime`部分。 主库文件包含：

   * `namespace`：要在&#x200B;**命名空间**&#x200B;字段中输入的值
   * `auth`：格式为`username:password`的值。 冒号之前的部分是&#x200B;**用户名**，冒号之后的部分是&#x200B;**密码**。

   >[!NOTE]
   >
   >您还可以通过在Adobe I/O CLI中运行`aio runtime namespace get`或`aio app use`来查找命名空间和身份验证值。

### 创建连接

1. 在模块中，单击&#x200B;**连接**&#x200B;字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL 连接名称]</td> 
      <td>输入此连接的名称。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 环境]</td> 
      <td>选择您要连接到生产环境还是非生产环境。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 类型]</td> 
      <td>选择<b>服务帐户</b>。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 用户名]</td> 
      <td>输入您工作区的<code>auth</code>值（冒号之前的部分）中的用户名。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 密码]</td> 
      <td>从工作区的<code>auth</code>值（冒号后的部分）输入密码。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 命名空间]</td> 
      <td>从工作区配置文件的<code>runtime</code>部分输入<code>namespace</code>值。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**继续**&#x200B;以保存连接。

## Adobe App Builder模块

### 运行自定义代码块

此模块允许您运行代码块。 您可以在设置模块时配置代码块，当模块在场景执行期间运行时，该代码块将运行。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>选择包含要运行的自定义函数的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 代码块]</td> 
   <td>输入您希望模块运行的代码块。<p>若要格式化代码以便于阅读，请单击<b>格式化代码</b>图标。</td> 
  </tr> 
   </tbody> 
</table>

### 从包运行自定义函数

此模块从包中运行函数。

有关包的信息，请参阅[使用自定义函数包](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md)。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>选择包含要运行的自定义函数的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 包]</td> 
   <td>选择包含要在场景中运行的函数的包。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 变量] </td> 
   <td>选择要在场景中运行的函数。</p></td> 
  </tr> 
   </tbody> 
</table>

### 使用包中的变量

此模块会将包中配置的变量引入场景。

有关包的信息，请参阅[使用自定义函数包](/help/workfront-fusion/create-scenarios/map-data/use-custom-function-packages.md)。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>选择包含要运行的自定义函数的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 包]</td> 
   <td>选择包含要纳入场景的变量的资源包。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 变量] </td> 
   <td>选择要纳入场景的变量。</p></td> 
  </tr> 
   </tbody> 
</table>

### 运行自定义函数或代码块

通过此模块，您可以使用存储在函数区域中的之前配置的自定义JavaScript函数。

有关配置自定义函数的说明，请参阅[使用自定义函数映射数据](/help/workfront-fusion/create-scenarios/map-data/map-using-custom-functions.md)。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>选择包含要运行的自定义函数的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 操作]</td> 
   <td>选择要运行的自定义函数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 参数] </td> 
   <td>输入函数参数的值。 可用参数基于创建函数时配置的参数。<p>如果某个参数具有默认值，则您将不会在字段中看到该默认值，但可以通过在字段中输入或映射值来覆盖该默认值。</p></td> 
  </tr> 
   </tbody> 
</table>


