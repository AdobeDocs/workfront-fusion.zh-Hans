---
title: Split.io模块
description: 在Adobe Workfront Fusion方案中，您可以自动使用 [!DNL Split.io]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 7d738a96-5424-4c30-831f-82e1d4c6f9d2
source-git-commit: 28de0fbe4fd6dfbcdc8ea4032e1aa95ae3e7c556
workflow-type: tm+mt
source-wordcount: '1919'
ht-degree: 0%

---

# [!DNL Split.io]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Split.io]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求</p>
   <p>或</p>
   <p>旧版：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

要使用[!DNL Split.io]模块，您必须具有[!DNL Split.io]帐户。

## Split.io API信息

Split.io连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td> https://api.split.io/internal/api</td>
   </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.34.1</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Split.io]连接到Workfront Fusion  {#connect-split-io-to-workfront-fusion}

您可以在[!DNL Split.io]模块内直接创建与[!DNL Split.io]帐户的连接。

1. 在任意[!DNL Split.io]模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
1. 填写以下字段。

   <table style="table-layout:auto"> 
     <col> 
     <col> 
     <tbody> 
      <tr> 
       <td role="rowheader">[!UICONTROL 连接名称]</td> 
       <td> <p>输入连接的名称。</p> </td> 
      </tr> 
      <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>
          <p>选择是连接到生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>
          <p>选择您是要连接到服务帐户还是个人帐户。</p>
        </td>
      </tr>
      <tr> 
       <td role="rowheader">[!UICONTROL API密钥]</td> 
       <td>输入您的[!DNL Split.io] API密钥。<p>有关[!DNL Split.io] API密钥的更多信息，请参阅<a href="https://help.split.io/hc/en-us/articles/360019916211-API-keys">文档中的</a>API密钥[!DNL Split.io]。</p></td> 
      </tr> 
     </tbody> 
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Split.io]模块及其字段

在配置[!DNL split.io]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL split.io]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)
* [搜索](#searches)

### 操作

* [[!UICONTROL 关联标记]](#associate-tags)
* [[!UICONTROL 创建拆分]](#create-split)
* [[!UICONTROL 在环境中创建拆分定义]](#create-split-definition-in-environment)
* [[!UICONTROL 自定义API调用]](#custom-api-call)
* [[!UICONTROL 删除拆分]](#delete-split)
* [[!UICONTROL 获取拆分]](#get-split)
* [[!UICONTROL 获取环境中的拆分定义]](#get-split-definition-in-environment)
* [[!UICONTROL 环境中的部分更新拆分定义]](#partial-update-split-definition-in-environment)
* [[!UICONTROL 从环境中移除拆分定义]](#remove-split-definition-from-environment)

#### [!UICONTROL 关联标记]

此操作模块将标记添加到指定的对象。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要添加标记的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 对象名称]</td> 
   <td>输入或映射要添加标记的对象的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 对象类型]</td> 
   <td> <p>输入或映射要添加标记的对象的类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标记]</td> 
   <td> <p>对于要添加的每个标记，单击<b>[!UICONTROL 添加项]</b>并输入或映射该标记。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建拆分]

在给定流量类型的情况下，此操作模块会在您的组织中创建新拆分。

>[!NOTE]
>
>该API不会在任何环境中配置拆分。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要在其中创建拆分的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 流量类型ID或名称]</td> 
   <td>选择或映射要创建拆分的流量类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拆分名称]</td> 
   <td> <p>输入或映射要创建的拆分的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拆分说明]</td> 
   <td>为要创建的拆分输入或映射[!UICONTROL split]说明。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 在环境中创建拆分定义]

此操作模块为特定环境配置拆分定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要在其中创建拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 环境名称或ID]</td> 
   <td>选择或映射要创建拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拆分名称]</td> 
   <td> <p>输入或映射要为其创建定义的分割的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>输入或映射要添加到拆分定义的任何注释。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 规则]</td> 
   <td> <p>对于要添加到定义的每个定位规则，单击<b>[!UICONTROL 添加项]</b>，然后输入或映射该规则。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 默认规则]</td> 
   <td> <p>输入或映射希望拆分用于不符合其他规则规范的流量的规则。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 默认待遇]</td> 
   <td> <p>输入或映射在拆分被终止或客户不包含在流量分配中的情况下希望拆分使用的处理方式。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 处理]</td> 
   <td> <p>对于要添加到定义的每个处理，单击<b>[!UICONTROL 添加项]</b>，然后输入或映射处理和大小。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 自定义API调用]

此操作模块允许您对[!DNL split.io] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL split.io]模块无法实现的数据流自动化。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code>https://api.split.io/internal/api/v2/</code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射每个方案执行周期中您希望模块使用的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除拆分]

此操作模块会从您的组织中删除拆分。 这会自动从所有环境中取消配置剥离定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要删除拆分的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拆分名称]</td> 
   <td> <p>输入或映射要删除的分割的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取拆分]

此操作模块将检索拆分。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要检索的分割的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拆分名称]</td> 
   <td> <p>输入或映射要检索的分割的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取环境中的拆分定义]

此操作模块从指定的环境中检索特定的拆分定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要检索的拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 环境名称或ID]</td> 
   <td>选择或映射包含要检索的拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拆分名称]</td> 
   <td> <p>输入或映射要检索其拆分定义的分割的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 环境中的部分更新拆分定义]

此操作模块更新特定环境的拆分定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要更新拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 环境名称或ID]</td> 
   <td>选择或映射要更新拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拆分名称]</td> 
   <td> <p>输入或映射要更新其定义的分割的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 更新内容]</td> 
   <td> <p>对于要更新的拆分的每个属性，单击<b>[!UICONTROL 添加项]</b>并输入或映射所需的更改。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>输入或映射要添加到拆分定义的任何注释。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 从环境中移除拆分定义]

此操作模块为特定环境取消配置拆分定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要删除拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 环境名称或ID]</td> 
   <td>选择或映射要删除拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拆分名称]</td> 
   <td> <p>输入或映射要删除其定义的分割的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comments]</td> 
   <td>输入或映射要添加到拆分定义的任何注释。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 关联标记]

此操作模块将标记添加到指定的对象。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射要添加标记的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 对象名称]</td> 
   <td>输入或映射要添加标记的对象的名称，</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 对象类型]</td> 
   <td> <p>输入或映射要添加标记的对象的类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标记]</td> 
   <td> <p>对于要添加的每个标记，单击<b>[!UICONTROL 添加项]</b>并输入或映射该标记。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL 获取环境]](#get-environments)
* [[!UICONTROL 获取流量类型]](#get-traffic-types)
* [[!UICONTROL 获取工作区]](#get-workspaces)
* [[!UICONTROL 列出环境中的拆分定义]](#list-split-definitions-in-an-environment)
* [[!UICONTROL 列表拆分]](#list-splits)

#### [!UICONTROL 获取环境]

此搜索模块可检索环境列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要列出的环境的工作区。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取流量类型]

此搜索模块可检索流量类型的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要列出的流量类型的工作区。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取工作区]

此搜索模块检索组织的工作区。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射每个方案执行周期中您希望模块检索的最大工作区数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出环境中的拆分定义]

此搜索模块检索给定环境中的拆分定义列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要列出的拆分定义的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 环境名称或ID]</td> 
   <td>选择或映射包含要列出的拆分定义的环境。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射每个方案执行周期中您希望模块检索的最大拆分定义数。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列表拆分]

此搜索模块检索拆分列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Split.io]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-split-io-to-workfront-fusion" class="MCXref xref">将[!DNL Split.io]连接到[!UICONTROL Workfront Fusion] </a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要列出的拆分的工作区。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射您希望模块在每个方案执行周期中检索的最大拆分数。</td> 
  </tr> 
 </tbody> 
</table>
