---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe用户管理模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行管理Adobe帐户中的用户的工作流。
author: Becky
feature: Workfront Fusion
exl-id: e8fe8ec4-4b00-4c9a-81a5-acb2039b153b
source-git-commit: 640fec2de63ad59ba89fae5373f85b8147d8dac0
workflow-type: tm+mt
source-wordcount: '2323'
ht-degree: 2%

---

# Adobe用户管理模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动执行管理Adobe帐户中的用户的工作流。

如果需要有关创建方案的说明，请参阅[创建方案：项目索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
  <td> <p>[!UICONTROL Pro] 或更高</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
   <td> <p>[!UICONTROL Plan]， [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前许可证要求：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成]，[!UICONTROL [!DNL Workfront Fusion]用于工作自动化]</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Adobe Workfront]计划，则贵组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[!UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 创建与Adobe用户管理的连接

要为您的[!DNL Adobe User Management]模块创建连接：

1. 单击“连接”框旁边的&#x200B;**[!UICONTROL Add]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>选择您要连接到生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>选择您是要连接到服务帐户还是个人帐户。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>输入您的[!UICONTROL Adobe] [!UICONTROL Client ID]。 这可以在[!UICONTROL Credentials]详细信息部分找到， [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>输入您的[!DNL Adobe] [!UICONTROL Client Secret]。 这可以在[!UICONTROL Credentials]详细信息部分找到， [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS Organization ID]</td>
        <td>输入您的[!DNL Adobe] IMS凭据。 组织的唯一标识符。 这是一个格式为A495E53@AdobeOrg的字符串，其中@的前缀为十六进制数字。 您可以在Admin Console或User Management集成的adobe.io控制台中，将此值作为组织的URL路径的一部分找到。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Additional scopes]</td>
        <td>对于要添加的每个其他范围，单击<b>添加项</b>并输入该范围。</td>
        </tr>
      </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;保存连接并返回模块。



## Adobe用户管理模块及其字段

在配置Adobe用户管理模块时，Workfront Fusion会显示以下列出的字段。 除此之外，还可能会显示其他Adobe用户管理字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)


* [搜索](#searches)
* [用户操作](#user-actions)
* [用户组操作](#user-group-actions)
* [其他](#other)

### 搜索

* [获取用户组和产品配置文件](#get-user-groups-and-product-profiles)
* [获取用户信息](#get-user-information)
* [在用户组或产品配置文件中获取用户](#get-users-in-a-user-group-or-product-profile)
* [获取组织中的用户](#get-users-in-an-organization)

#### 获取用户组和产品配置文件

此搜索模块可检索您组织中所有用户组和产品配置文件的列表，以及有关这些组和配置文件的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">返回结果的最大数目</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

#### 获取用户信息

此搜索模块可检索组织中单个用户的详细信息，根据其电子邮件地址进行标识。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">电子邮件地址</td> 
   <td>输入或映射要为其返回详细信息的用户的电子邮件地址。 对于AdobeID、Enterprise和电子邮件联合用户，这应该是完整的电子邮件地址，包括域。 在所有情况下，参数均不区分大小写。</td> 
  </tr> 
 </tbody> 
</table>

#### 在用户组或产品配置文件中获取用户

此搜索模块可检索指定用户组或产品配置文件中所有用户的列表，以及有关这些用户的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">组名称</td> 
   <td>用户组、产品配置文件名称或管理组。 对于管理员组，该名称可以是固定组<code>_org_admin</code>、<code>_deployment_admin</code>或<code>_support_admin</code>之一；也可以是特定于组的管理员组。 这些在组名上用前缀标识，如<code>_admin_groupName</code>、<code>_product_admin_productName</code>或<code>_developer_groupName</code>。 如果该组存在，但管理员组不存在，则会返回空列表。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">仅直接</td> 
   <td>指定返回的用户结构中的组字段是否仅包含该用户为其直接成员的那些产品配置文件。 如果为false，则返回包含该用户的所有组（用户组、产品配置文件和管理员组），而不管特定产品配置文件的权利是直接（通过用户分配）还是间接（通过包含被分配给产品配置文件的用户的用户组）获得。 如果为true，则返回包含该用户的所有用户组和管理员组，但只返回已为该用户明确分配权利的产品配置文件。 用户既可以是产品配置文件的直接成员，也可以是间接成员。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">排除组</td> 
   <td>指定响应是否排除为每个单独用户返回的组数组。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">状态</td> 
   <td>此选项仅适用于产品配置文件。 选择活动可列出已为产品配置并具有有效许可证的用户。 选择不活动可列出已添加到产品配置文件但没有有效许可证的用户。 如果留空，则模块将返回所有成员用户，无论其权利状态如何。
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">返回结果的最大数目</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

#### 获取组织中的用户

此搜索模块返回与连接相关联的组织的所有用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">返回结果的最大数目</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

### 用户操作

* [将用户添加为组成员](#add-a-user-as-a-member-of-a-group)
* [创建用户](#create-a-user)
* [从组中删除用户](#remove-a-user-from-groups)
* [更新用户](#update-a-user)

#### 将用户添加为组成员

此操作模块添加一个用户作为指定组或组的成员。 此模块最多可以将用户添加到四个组。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">用户</td> 
   <td>输入或映射要添加到组的用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">域</td> 
   <td>对于不是电子邮件地址的Federated ID，请输入用户所属的域。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">组</td> 
   <td>对于要将用户添加到的每个组，单击<b>添加项</b>并输入或映射该组。 您最多可以输入四个组，并且必须至少输入一个。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">使用Adobe ID</td> 
   <td>选择true可确保用户ID被解释为引用现有的Adobe ID，即使存在具有相同名称的Enterprise或Federated ID也是如此。</td> 
  </tr> 
 </tbody> 
</table>

#### 创建用户

此操作模块将在组织中创建新用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID类型</td> 
   <td>选择您要创建具有Adobe ID、Enterprise ID还是Federated ID的用户。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">登录</td> 
   <td>如果要创建具有Federated ID的用户，请选择登录类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">电子邮件</td> 
   <td>输入或映射新用户的电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">域</td> 
   <td>如果要创建Federated ID具有基于域的登录名的用户，请输入或映射域。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">用户</td> 
   <td>如果要创建具有基于域的登录的Federated ID的用户，请输入或映射该新用户将代表的用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">名字</td> 
   <td>输入或映射用户的名字。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">姓氏</td> 
   <td>输入或映射用户的姓氏。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">国家/地区</td> 
   <td>输入或映射双字符ISO国家/地区代码。 创建用户后无法更改此设置。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">选项</td> 
   <td>选择当组织中已存在该用户时要执行的操作。 如果未选择任何选项，并且用户已存在，则模块将返回错误。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">使用Adobe ID</td> 
   <td>为true时，即使用户的ID被解释为引用现有的Adobe ID，即使存在具有相同名称的Enterprise或Federated ID也是如此。</td> 
  </tr> 
 </tbody> 
</table>

#### 从组中删除用户

此操作模块从指定的组中删除用户的成员资格。 一次最多可以从四个组中删除一个用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">用户</td> 
   <td>输入或映射要从组中移除的用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">域</td> 
   <td>对于不是电子邮件地址的Federated ID，请输入用户所属的域。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">组</td> 
   <td>对于要从中删除用户的每个组，单击<b>添加项</b>并输入或映射该组。 您最多可以输入四个组，并且必须至少输入一个。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">使用Adobe ID</td> 
   <td>选择true可确保用户ID被解释为引用现有的Adobe ID，即使存在具有相同名称的Enterprise或Federated ID也是如此。</td> 
  </tr> 
 </tbody> 
</table>



#### 更新用户

此操作模块更新现有用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">用户</td> 
   <td>输入或映射要更新的用户的ID。 这是用户的电子邮件地址，例如 <code>user@example.com</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">域</td> 
   <td>如果您要更新的Federated ID不是电子邮件地址的用户，请输入或映射该用户所属的域，以便识别该用户。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">电子邮件</td> 
   <td>输入或映射用户的新电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">名字</td> 
   <td>输入或映射用户的名字。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">姓氏</td> 
   <td>输入或映射用户的姓氏。</td> 
  </tr> 
 </tbody> 
</table>

### 用户组操作

* [为用户组添加成员资格](#add-memberships-for-a-user-group)
* [创建用户组](#create-a-user-group)
* [删除用户组](#delete-a-user-group)
* [删除用户组的成员资格](#remove-memberships-for-a-user-group)
* [更新用户组](#update-a-user-group)

#### 为用户组添加成员资格

此操作模块可将用户和产品配置文件添加到用户组。 添加到用户组的用户将获得用户组中所有产品配置文件的权限。 添加产品配置文件会将该配置文件的权利授予用户组中的用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">组名称</td> 
   <td>输入或映射要从其中删除用户或配置文件的组的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">用户</td> 
   <td>对于每个要添加的用户，单击<b>添加用户</b>并输入该用户的电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">轮廓</td> 
   <td>对于要添加到群组的每个配置文件，单击<b>添加用户</b>并输入配置文件名称</td> 
  </tr> 
 </tbody> 
</table>

#### 创建用户组

此操作模块将创建新用户组。 如果已存在具有给定名称的组，则模块可以更新现有组。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">组名称</td> 
   <td>输入或映射新用户组的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">描述</td> 
   <td>输入或映射新用户组的描述。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">选项</td> 
   <td>如果组织中已存在用户组，请选择要执行的操作。 如果未选择任何选项，并且用户组已存在，则模块将返回错误。</td> 
  </tr> 
 </tbody> 
</table>

#### 删除用户组

此操作模块删除现有用户组。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">组名称</td> 
   <td>输入或映射要删除的组的名称。</td> 
  </tr> 
 </tbody> 
</table>

#### 删除用户组的成员资格

此操作模块会从用户组中删除用户或配置文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">组名称</td> 
   <td>输入或映射要从其中删除用户或配置文件的组的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">用户</td> 
   <td>对于每个要删除的用户，单击<b>添加用户</b>并输入该用户的电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">轮廓</td> 
   <td>对于要从组中删除的每个配置文件，单击<b>添加用户</b>并输入配置文件名称</td> 
  </tr> 
  <tr> 
   <td role="rowheader">使用Adobe ID</td> 
   <td>为true时，即使用户的ID被解释为引用现有的Adobe ID，即使存在具有相同名称的Enterprise或Federated ID也是如此。</td> 
  </tr> 
 </tbody> 
</table>

#### 更新用户组

此操作模块更新现有的用户组。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">原始组名称</td> 
   <td>输入或映射要更新的组的当前名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">新组名称</td> 
   <td>输入或映射您希望组具有的新名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">原始组名称</td> 
   <td>输入或映射更新的组说明。</td> 
  </tr> 
 </tbody>

### 其他

此操作模块对Adobe用户管理API进行自定义调用。

#### 进行自定义API调用

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe用户管理的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-user-management" class="MCXref xref" >创建与Adobe用户管理的连接</a>。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>输入相对路径 <code>https://usermanagement.adobe.io/v2/usermanagement/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>方法</p>
      </td>
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">标头</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 自动添加授权标头和x-api-key标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">查询字符串  </td>
      <td>
        <p>输入请求查询字符串。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">正文</td>
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
