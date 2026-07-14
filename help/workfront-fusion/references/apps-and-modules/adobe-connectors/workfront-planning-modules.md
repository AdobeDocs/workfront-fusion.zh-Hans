---
title: Adobe Workfront 规划模块
description: 通过 [!DNL Adobe Workfront Planning] 模块，您可以根据 [!DNL Adobe] Adobe Workfront Planning帐户中的事件启动Workfront Fusion方案，创建、读取或更新协议和其他记录，使用您设置的条件搜索记录以及上载文档。
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
TQID: https://experienceleague.adobe.com/QHOFWDOT-18-c0b3wLXsRV5cjGVxlcyLhvZdkev3GFg
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: f0e185778e01b71a91837531a082e88485e97ca2
workflow-type: tm+mt
source-wordcount: 6075
ht-degree: 34%

---


# Adobe Workfront 规划模块

通过[!DNL Adobe Workfront Planning]模块，您可以在Workfront Planning中发生事件时触发方案。 您还可以创建、读取、更新和删除记录，或者对您的[!DNL Adobe Workfront Planning]帐户执行自定义API调用。

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

## 先决条件

要访问Workfront Planning，您必须具备以下条件：

* 新的Workfront包和许可证。 Workfront Planning不适用于旧版Workfront包或许可证。
* Workfront计划包。
* 您组织的Workfront实例必须载入到Adobe Unified Experience。

## Adobe Workfront规划API信息

Adobe Workfront Planning连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td><pre><code>https://&#123;&#123;connection.host&#125;&#125;/maestro/api/&#123;&#123;common.maestroApiVersion&#125;&#125;/</code></pre></td> 
  </tr>
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## 将Workfront Planning连接到Workfront Fusion

Workfront Planning连接器使用OAuth 2.0连接到Workfront Planning。

可直接从Workfront Planning Fusion模块内部创建与Workfront Planning帐户的连接。

* [使用客户端ID和客户端密钥连接到Workfront Planning](#connect-to-workfront-planning-using-client-id-and-client-secret)
* [使用服务器到服务器连接连接到Workfront Planning](#connect-to-workfront--planning-using-a-server-to-server-connection)

### 使用客户端ID和客户端密钥连接到Workfront Planning

1. 在任意Adobe Workfront规划模块中，单击“连接”字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接类型]</td>
        <td>
          <p>选择<b>Adobe Workfront身份验证</b>连接。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端 ID]</td>
        <td>请输入您的 Workfront 客户端 ID。 您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。 打开您要连接的特定应用程序即可查看客户端 ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的 Workfront 客户端密钥。 您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。 如果您的 Workfront OAuth2 应用程序没有客户端密钥，您可以重新生成一个。 有关操作说明，请参阅 Workfront 文档。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 身份验证 URL]</td>
        <td>此项可保持默认值，或输入您 Workfront 实例的 URL，并在后面添加 <code>/integrations/oauth2</code>。 <p>示例： <code>https://mydomain.my.workfront.com/integrations/oauth2</code></p></td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 主机前缀]</td>
        <td>在大多数情况下，此值应为 <code>origin</code>。
      </tr>
    </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

   如果您未登录Workfront Planning，则会引导您进入登录屏幕。 登录后，您即可允许该连接。

>[!NOTE]
>
>* 通过 OAuth 2.0 连接到 Workfront API 不再依赖 API 密钥。
>* 要连接到 Workfront 沙盒环境，您必须在该环境中创建 OAuth2 应用程序，然后使用该应用程序生成的客户端 ID 和客户端密钥建立连接。

### 使用服务器到服务器连接连接到Workfront Planning

1. 在任意Adobe Workfront规划模块中，单击“连接”字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接类型]</td>
        <td>
          <p>选择 <b>Adobe Workfront 服务器到服务器连接</b>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 实例名称]</td>
        <td>
          <p>输入您的实例名称，即您的域。</p><p>示例：如果您的 URL 为 <code>https://example.my.workfront.com</code>，请输入 <code>example</code>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 实例通道]</td>
        <td>
          <p>输入此连接要访问的环境类型。</p><p>示例：如果您的 URL 为 <code>https://example.my.workfront.com</code>，请输入 <code>my</code>。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端 ID]</td>
        <td>请输入您的 Workfront 客户端 ID。 您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。 打开您要连接的特定应用程序即可查看客户端 ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的 Workfront 客户端密钥。 您可以在 Workfront 的“设置”区域中 OAuth2 应用程序部分找到此信息。 如果您的 Workfront OAuth2 应用程序没有客户端密钥，您可以重新生成一个。 有关操作说明，请参阅 Workfront 文档。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 范围]</td>
        <td>输入此连接所需的相关范围。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 主机前缀]</td>
        <td>在大多数情况下，此值应为 <code>origin</code>。
      </tr>
    </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

   如果您未登录Workfront Planning，则会引导您进入登录屏幕。 登录后，您即可允许该连接。

>[!NOTE]
>
>* 通过 OAuth 2.0 连接到 Workfront API 不再依赖 API 密钥。
>* 要连接到 Workfront 沙盒环境，您必须在该环境中创建 OAuth2 应用程序，然后使用该应用程序生成的客户端 ID 和客户端密钥建立连接。

## [!DNL Adobe Workfront Planning]版本2模块及其字段

>[!IMPORTANT]
>
>此部分中的模块属于Workfront规划V2连接器。有关Workfront规划V1连接器中的模块，请参阅[[!DNL Adobe Workfront Planning] 版本1模块及其字段](#adobe-workfront-planning-version-1-modules-and-their-fields)。

配置Workfront Planning模块时，Workfront Fusion会显示以下列出的字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 Workfront 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

* [工作区](#workspaces-v2)
* [记录类型](#record-types-v2)
* [记录](#records-v2)
* [字段](#fields-v2)
* [视图](#views-v2)
* [权限](#permissions-v2)
* [其他](#other-v2)

### 工作区(V2)

* [创建工作区](#create-a-workspace-v2)
* [删除工作区](#delete-a-workspace-v2)
* [获取所有工作区](#get-all-workspaces-v2)
* [获取工作区](#get-a-workspace-v2)
* [更新工作区](#update-a-workspace-v2)

#### 创建工作区(V2)

此操作模块在Planning中创建新工作区。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace名称]</p>
      </td>
      <td>输入或映射新工作区的名称。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>描述</p>
      </td>
      <td>输入或映射新工作区/td&gt;的说明 
    </tr>
    <tr>
      <td role="rowheader">
        <p>颜色</p>
      </td>
      <td>选择要用于表示新记录类型的颜色</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>图标</p>
      </td>
      <td>映射要用于此记录类型的图标。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>所有者</p>
      </td>
      <td>输入或映射要拥有工作区的用户的Adobe IMS用户ID。</td> 
    </tr>
  </tbody>
</table>

#### 删除工作区(V2)

此操作模块将删除由ID指定的单个工作区。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 工作区 ID]</p>
      </td>
      <td>输入或映射要删除的工作区的ID。</td> 
    </tr>
  </tbody>
</table>

#### 获取所有工作区(V2)

此模块检索所有工作区的列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 返回工作区的最大数量]</p>
      </td>
      <td>输入或映射模块在一个执行周期内返回的最大工作区数。</td> 
    </tr>
  </tbody>
</table>

#### 获取工作区(V2)

此模块通过工作区的ID来检索工作区。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 工作区 ID]</p>
      </td>
      <td>输入或映射要检索的工作区的ID。</td> 
    </tr>
  </tbody>
</table>

#### 更新工作区(V2)

此操作模块可更新Planning中的新工作区。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择要更新的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace名称]</p>
      </td>
      <td>输入或映射新工作区的名称。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>描述</p>
      </td>
      <td>输入或映射新工作区/td&gt;的说明 
    </tr>
    <tr>
      <td role="rowheader">
        <p>颜色</p>
      </td>
      <td>选择要用于表示新记录类型的颜色</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>图标</p>
      </td>
      <td>映射要用于此记录类型的图标。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>所有者</p>
      </td>
      <td>输入或映射要拥有工作区的用户的Adobe IMS用户ID。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>记录类型节</p>
      </td>
      <td>对于要添加到此工作区的每个记录类型节，单击<b>添加项</b>，然后输入节的名称、记录类型ID以及是否要覆盖现有的记录类型ID。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>记录类型节&gt;覆盖</p>
      </td>
      <td>选择是否使用模块中的部分替换现有部分。 如果没有，则会将模块中的部分添加到现有部分列表中。</td> 
    </tr>
  </tbody>
</table>


### 记录类型(V2)

* [创建记录类型](#create-a-record-type-v2)
* [删除记录类型](#delete-a-record-type-v2)
* [获取全局记录类型](#get-global-record-types-v2)
* [获取记录类型](#get-a-record-type-v2)
* [获取记录类型](#get-record-types-v2)
* [更新记录类型](#update-a-record-type-v2)

#### 创建记录类型(V2)

此操作模块在所选工作区中创建新记录类型。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择要创建记录类型的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>显示名称</p>
      </td>
      <td>输入或映射新记录类型的名称。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>描述</p>
      </td>
      <td>输入或映射新记录类型的说明。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>图标</p>
      </td>
      <td>映射要用于此记录类型的图标。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>颜色</p>
      </td>
      <td>选择要用于表示新记录类型的颜色</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>Source记录类型</p>
      </td>
      <td>如果要使用其他记录类型作为起点，请选择该记录类型。</td> 
    </tr>
  </tbody>
</table>

#### 删除记录类型(V2)

此操作模块删除由ID指定的单个记录类型。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录类型ID]</p>
      </td>
      <td>输入或映射要删除的记录类型的ID。</td> 
    </tr>
  </tbody>
</table>

#### 获取全局记录类型(V2)

本模块检索Adobe Workfront Planning帐户中记录类型的列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择工作区。 模块将返回可添加到此工作区的全局记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回的最大记录类型数]</p>
      </td>
      <td>输入或映射模块在一个执行周期内返回的最大记录类型数。</td> 
    </tr>
  </tbody>
</table>

#### 获取记录类型(V2)

此模块按其ID检索记录类型。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录类型ID]</p>
      </td>
      <td>输入或映射要检索的记录类型的ID。</td> 
    </tr>
  </tbody>
</table>

#### 获取记录类型(V2)

此模块检索给定工作区中可用的记录类型列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择要检索其记录类型的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回的最大记录类型数]</p>
      </td>
      <td>输入或映射模块在一个执行周期内返回的最大记录类型数。</td> 
    </tr>
  </tbody>
</table>

#### 更新记录类型(V2)

此模块更新记录类型。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择要更新记录类型的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择要更新记录类型的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>显示名称</p>
      </td>
      <td>输入或映射记录类型的名称。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>描述</p>
      </td>
      <td>输入或映射记录类型的说明。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>主字段ID</p>
      </td>
      <td>输入或映射用作记录类型标题的字段的ID。</td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>图标</p>
      </td>
      <td>映射要用于此记录类型的图标。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>颜色</p>
      </td>
      <td>选择要用于表示新记录类型的颜色</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>可与Workspace ID链接</p>
      </td>
      <td>对于您希望此记录类型能够链接到的每个工作区，单击<b>添加项</b>并输入工作区的ID。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>可与Workspace ID链接&gt;覆盖</p>
      </td>
      <td>选择是否使用模块中的工作区替换现有工作区。 如果为“否”，则模块中的工作区将添加到现有工作区列表中。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>已授权创建动态记录类型</p>
      </td>
      <td>对于有权从此记录类型创建动态记录类型的每个主题，单击<b>添加项</b>并输入主题的类型和ID。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>已授权创建动态记录类型&gt;覆盖</p>
      </td>
      <td>选择是否将现有主题替换为模块中的主题。 如果不包含，则会将模块中的主题添加到现有主题列表。</td> 
    </tr>
  </tbody>
</table>



### 记录(V2)

* [创建记录](#create-a-record-v2)
* [删除记录](#delete-a-record-v2)
* [获取记录](#get-a-record-v2)
* [按记录类型获取记录](#get-records-by-record-type-v2)
* [移动记录](#move-records-v2)
* [搜索记录](#search-records-v2)
* [更新记录](#update-a-record-v2)

#### 创建记录(V2)

此操作在Workfront Planning中创建单个记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择要创建记录的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择要创建的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>其他字段</p>
      </td>
      <td>输入希望新记录具有的值。 这些字段基于您选择的记录类型，并且对于您的Workfront Planning组织是唯一的。</td> 
    </tr>
  </tbody>
</table>

#### 删除记录(V2)

此操作模块删除由ID指定的单个记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录ID]</p>
      </td>
      <td>输入或映射要删除的记录的ID。</td> 
    </tr>
  </tbody>
</table>

#### 获取记录(V2)

此操作模块可检索由其ID指定的记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 工作区 ID]</p>
      </td>
      <td>输入或映射要检索的记录的ID。</td> 
    </tr>
  </tbody>
</table>

#### 按记录类型获取记录(V2)

此模块检索给定记录类型的所有记录的列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择包含要检索的记录的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择要返回的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回的最大记录数]</p>
      </td>
      <td>输入或映射模块在一个执行周期内返回的最大记录数。</td> 
    </tr>
  </tbody>
</table>

#### 移动记录(V2)

此模块通过指定记录类型的放置位置，对记录中的一个或多个记录重新排序。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择包含要移动记录的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择要移动的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择包含要移动记录的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择包含要移动记录的工作区。</td> 
    </tr>
  </tbody>
</table>

#### 搜索记录(V2)

根据您指定的条件返回记录

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择包含要检索的记录的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择包含要检索的记录的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL其他字段]</p>
      </td>
      <td>对于要作为筛选依据的每个字段，输入该字段的运算符和值。 这些字段基于您选择的记录类型，并且对于您的Workfront Planning组织是唯一的。</td> 
    </tr>
  </tbody>
</table>

#### 更新记录(V2)

此模块更新指定的记录。



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择包含要更新的记录的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录类型ID]</p>
      </td>
      <td>选择要更新的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录ID]</p>
      </td>
      <td>输入或映射要更新的记录ID。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL其他字段]</p>
      </td>
      <td>输入其他字段的值。 可用字段取决于所选记录。</td> 
    </tr>
  </tbody>
</table>


### 字段(V2)

* [创建字段](#create-a-field-v2)
* [删除字段](#delete-a-field-v2)
* [获取字段](#get-a-field-v2)
* [按记录类型获取字段](#get-fields-by-record-type-v2)
* [更新一个字段](#update-a-field-v2)

#### 创建字段(V2)

此操作模块在指定的记录类型上创建新字段。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择要创建字段的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择要为其创建字段的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>显示名称</p>
      </td>
      <td>输入或映射新字段的名称。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>描述</p>
      </td>
      <td>输入或映射新字段的说明。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>字段类型</p>
      </td>
      <td>为字段选择数据类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>其他字段</p>
      </td>
      <td>特定于该所选字段类型的其他字段可能可用。 填写这些字段的值。</td> 
    </tr>
  </tbody>
</table>

#### 删除字段(V2)

此操作模块将删除由ID指定的单个字段。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL字段ID]</p>
      </td>
      <td>输入或映射要删除字段的 ID。</td> 
    </tr>
  </tbody>
</table>

#### 获取字段(V2)

此模块通过字段的ID来检索字段。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL字段ID]</p>
      </td>
      <td>输入或映射要检索的字段的ID。</td> 
    </tr>
  </tbody>
</table>

#### 按记录类型获取字段(V2)

此模块检索特定记录类型的字段列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择包含要返回的字段的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择要为其返回字段的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回的最大字段数]</p>
      </td>
      <td>输入或映射模块在一个执行周期内返回的最大字段数。</td> 
    </tr>
  </tbody>
</table>

#### 更新字段(V2)

此模块通过字段的ID来部分更新字段。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源类型]</p>
      </td>
      <td>选择包含要更新的字段的资源类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL字段ID]</p>
      </td>
      <td>选择要更新的字段。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL显示名称]</p>
      </td>
      <td>输入或映射字段的名称。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 描述]</p>
      </td>
      <td>输入或映射字段的说明。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL其他参数]</p>
      </td>
      <td>输入其他字段参数的值。 可用参数取决于所选字段。</td> 
    </tr>
  </tbody>
</table>


### 视图(V2)

* [创建视图](#create-a-view-v2)
* [删除视图](#delete-a-view-v2)
* [获取视图](#get-a-view-v2)
* [按记录类型获取视图](#get-views-by-record-type-v2)
* [更新视图](#update-a-view-v2)

#### 创建视图(V2)

此操作模块为所选记录类型创建新视图。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择要创建视图的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择要为其创建视图的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>视图名称</p>
      </td>
      <td>输入或映射新视图的名称。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>查看类型</p>
      </td>
      <td>选择新视图是表格、时间线还是日历视图。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>开始日期字段</p>
      </td>
      <td>如果视图是时间轴或日历视图，请选择视图将用于在时间轴上放置记录的字段。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>结束日期字段。</p>
      </td>
      <td>如果视图是时间线或日历视图，请选择视图将用于确定时间线结束日期的字段。</td> 
    </tr>
  </tbody>
</table>

#### 删除视图(V2)

此操作模块将删除由ID指定的单个视图。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL视图ID]</p>
      </td>
      <td>输入或映射要删除的视图的ID。</td> 
    </tr>
  </tbody>
</table>

#### 获取视图(V2)

此模块按其ID检索视图。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL视图ID]</p>
      </td>
      <td>输入或映射要检索的视图的ID。</td> 
    </tr>
  </tbody>
</table>

#### 按记录类型获取视图(V2)

此模块检索特定记录类型的视图列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择包含要检索的视图的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择包含要检索的视图的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回视图的最大数目]</p>
      </td>
      <td>输入或映射模块在一个执行周期内返回的最大视图数。</td> 
    </tr>
  </tbody>
</table>

#### 更新视图(V2)

此操作模块更新指定的视图。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>选择要更新视图的工作区。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择要为其更新视图的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>查看 ID</p>
      </td>
      <td>选择要更新的视图。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>视图名称</p>
      </td>
      <td>输入或映射新视图的名称。</td> 
    </tr>
  </tbody>
</table>

### 权限(V2)

* [取消访问请求](#dismiss-access-requests-v2)
* [获取资源的所有成员及其角色](#get-all-members-and-their-roles-for-a-resource-v2)
* [获取当前用户对资源的有效权限](#get-the-current-users-effective-permissions-on-a-resource-v2)
* [列出资源的挂起访问请求](#list-pending-access-requests-for-a-resource-v2)
* [请求对资源的访问权限](#request-access-to-a-resource-v2)

#### 取消访问请求(V2)

此操作模块可取消由ID指定的一个或多个访问请求。



<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源类型]</p>
      </td>
      <td>输入或映射要删除的Workspace的ID。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源ID]</p>
      </td>
      <td>输入或映射要取消访问请求的资源的ID。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL请求ID]</p>
      </td>
      <td>对于要取消的每个访问请求，单击<b>添加项</b>并输入请求ID。</td> 
    </tr>
  </tbody>
</table>

#### 获取资源的所有成员及其角色(V2)

此模块列出了资源上具有显式共享关系的所有用户、组和团队。 此模块连接中使用的凭据必须具有资源的管理权限。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源类型]</p>
      </td>
      <td>选择要为其检索信息的资源类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源ID]</p>
      </td>
      <td>输入或映射要检索其信息的资源的ID。</td> 
    </tr>
  </tbody>
</table>

#### 获取当前用户在资源上的有效权限(V2)

此模块返回当前用户对给定资源的查看、编辑、删除和添加权限。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源类型]</p>
      </td>
      <td>选择要为其检索权限的资源类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源ID]</p>
      </td>
      <td>输入或映射要为其检索权限的资源ID。</td> 
    </tr>
  </tbody>
</table>

#### 列出资源的挂起访问请求(V2)

此模块返回给定资源的所有待处理访问请求。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源类型]</p>
      </td>
      <td>选择要为其检索信息的资源类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源ID]</p>
      </td>
      <td>输入或映射要检索其信息的资源的ID。</td> 
    </tr>
  </tbody>
</table>

#### 请求访问资源(V2)

此模块为给定资源上的当前用户创建或更新访问请求。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源类型]</p>
      </td>
      <td>选择要为其创建或更新访问请求的资源类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL资源ID]</p>
      </td>
      <td>输入或映射要为其创建或更新访问请求的资源的ID。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Message]</p>
      </td>
      <td>输入或映射要包含在访问请求中的消息文本。</td> 
    </tr>
  </tbody>
</table>



### 其他(V2)

* [从Workfront ID获取身份验证ID](#get-auth-id-from-workfront-id-v2)
* [发起自定义 API 调用](#make-a-custom-api-call-v2)
* [监控事件](#watch-events-v2)

#### 从Workfront ID (V2)获取身份验证ID

此模块采用Workfront用户ID并返回Planning使用的匹配授权ID。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workfront用户ID]</p>
      </td>
      <td>输入或映射要检索其授权ID的用户的Workfront ID。</td> 
    </tr>
  </tbody>
</table>

#### 进行自定义API调用(V2)&lt;表

此模块对Workfront规划API进行自定义调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将 Workfront 应用程序连接到 Workfront Fusion 的说明，请参阅本文中的<a href="#connect-workfront-to-workfront-fusion" class="MCXref xref">将 Workfront 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>输入相对于 <code> https://&lt;WORKFRONT_DOMAIN>/maestro/api/.</code> 的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL API 版本]</td> 
   <td>选择您希望模块使用的 Workfront API 版本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。 如需了解详情，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">Adobe Workfront Fusion 中的 HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。 这将决定请求的内容类型。</p> <p>例如，<code> {"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> <p>提示：建议通过 JSON 正文传递信息，而不是作为查询参数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 正文]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 观看活动(V2)

在Workfront Planning中创建、更新或删除记录、记录类型或工作区时，此触发器模块将启动一个方案。

>[!IMPORTANT]
>
>您可以稍后编辑此模块，这将编辑webhook。
>
>更新webhook时，请考虑以下事项：
>
>* Workfront事件订阅会将编辑后的webhook视为新订阅。 对于以前的webhook配置，不会保留事件订阅历史记录，因为它被视为单独的事件订阅。
>* 从旧事件订阅切换到新事件订阅可能不会完全同步。 因此，可能会收到两次事件（如果新订阅在旧订阅停止之前开始运行）或错过事件（如果旧订阅在新订阅开始运行之前停止）。
>
>有关编辑Webhook的详细信息，请参阅[编辑Webhook](/help/workfront-fusion/manage-scenarios/edit-webhooks.md)。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>选择要使用的webhook，或单击“添加”以创建一个新挂接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 对象类型]</td>
      <td>选择您要监视记录、记录类型还是工作区。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL要监视的对象]</td>
      <td>选择是要监视新记录、更新的记录、新记录和更新的记录还是删除的记录。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL配置类型]</td>
      <td>选择是需要简单配置还是高级配置。 <p>有关高级配置的详细信息，请参阅本文中的“监视事件”模块中的<a href="#example-of-advanced-logic-in-the-watch-events-module" class="MCXref xref" >高级逻辑示例</a>。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 状态]</td>
      <td>选择您希望关注旧状态还是新状态。<ul><li><p><b>[!UICONTROL 新状态]</b></p><p>当记录状态更改<b>为</b>指定值时触发场景。</p></li><li><p><b>[!UICONTROL 旧状态]</b></p><p>当记录状态<b>从</b>指定值发生变化时触发场景。</p></li></ul></td> 
    <tr>
      <td role="rowheader">[！UICONTROL Workspace]</td>
      <td>如果观看记录，请选择您想要观看记录的Workspace。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 记录类型]</td>
      <td>如果观看记录，请选择您要观看的记录类型。</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL 事件筛选条件]</p> </td> 
      <td> <p>您可以设置筛选条件，仅观看符合您所选条件的记录。</p> <p>对于每个筛选条件，请输入要评估的字段、运算符以及筛选条件应允许的值。 您可以通过添加 AND 规则来使用多个筛选条件。</p> <p>注意：您无法编辑现有Workfront Webhook中的筛选器。 如需为 Workfront 事件订阅设置不同的筛选条件，请删除当前 Webhook 并创建一个新的。</p> <p>有关事件过滤器的详细信息，请参阅Workfront模块文章中的Workfront &gt; [！UICONTROL观看活动]模块中的<a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">事件订阅过滤器</a>。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL要监视的对象]</td>
      <td>选择是否要监视新的。 更新、新增和更新或删除的记录。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL排除此连接所做的更新]</p>
      </td>
      <td>启用此选项可防止在此模块使用的连接进行更改时触发场景。 如果场景执行触发操作，这将阻止触发场景的另一个实例。</td> 
    </tr>
  </tbody>
</table>

有关在此模块上使用高级逻辑的示例，请参阅监视事件模块中的[高级逻辑示例](#example-of-advanced-logic-in-the-watch-events-module)。






## [!DNL Adobe Workfront Planning]版本1模块及其字段

>[!IMPORTANT]
>
>此部分中的模块属于Workfront规划V1连接器。有关Workfront规划V2连接器中的模块，请参阅[[!DNL Adobe Workfront Planning] 版本2模块及其字段](#adobe-workfront-planning-version-2-modules-and-their-fields)。

配置Workfront Planning模块时，Workfront Fusion会显示以下列出的字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 Workfront 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。


![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)
* [未分类](#uncategorized)

### 触发器

#### 监控事件

在Workfront Planning中创建、更新或删除记录、记录类型或工作区时，此触发器模块将启动一个方案。

>[!IMPORTANT]
>
>您可以稍后编辑此模块，这将编辑webhook。
>
>更新webhook时，请考虑以下事项：
>
>* Workfront事件订阅会将编辑后的webhook视为新订阅。 对于以前的webhook配置，不会保留事件订阅历史记录，因为它被视为单独的事件订阅。
>* 从旧事件订阅切换到新事件订阅可能不会完全同步。 因此，可能会收到两次事件（如果新订阅在旧订阅停止之前开始运行）或错过事件（如果旧订阅在新订阅开始运行之前停止）。
>
>有关编辑Webhook的详细信息，请参阅[编辑Webhook](/help/workfront-fusion/manage-scenarios/edit-webhooks.md)。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Webhook]</td>
      <td>选择要使用的webhook，或单击“添加”以创建一个新挂接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 对象类型]</td>
      <td>选择您要监视记录、记录类型还是工作区。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 状态]</td>
      <td>选择您希望关注旧状态还是新状态。<ul><li><p><b>[!UICONTROL 新状态]</b></p><p>当记录状态更改<b>为</b>指定值时触发场景。</p></li><li><p><b>[!UICONTROL 旧状态]</b></p><p>当记录状态<b>从</b>指定值发生变化时触发场景。</p></li></ul></td> 
    <tr>
      <td role="rowheader">[！UICONTROL Workspace]</td>
      <td>如果观看记录，请选择您想要观看记录的Workspace。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 记录类型]</td>
      <td>如果观看记录，请选择您要观看的记录类型。</td>
    </tr>
    </tr>
    <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL 事件筛选条件]</p> </td> 
      <td> <p>您可以设置筛选条件，仅观看符合您所选条件的记录。</p> <p>对于每个筛选条件，请输入要评估的字段、运算符以及筛选条件应允许的值。 您可以通过添加 AND 规则来使用多个筛选条件。</p> <p>注意：您无法编辑现有Workfront Webhook中的筛选器。 如需为 Workfront 事件订阅设置不同的筛选条件，请删除当前 Webhook 并创建一个新的。</p> <p>有关事件过滤器的详细信息，请参阅Workfront模块文章中的Workfront &gt; [！UICONTROL观看活动]模块中的<a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">事件订阅过滤器</a>。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL要监视的对象]</td>
      <td>选择是否要监视新的。 更新、新增和更新或删除的记录。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL排除此连接所做的更新]</p>
      </td>
      <td>启用此选项可防止在此模块使用的连接进行更改时触发场景。 如果场景执行触发操作，这将阻止触发场景的另一个实例。</td> 
    </tr>
  </tbody>
</table>

有关在此模块上使用高级逻辑的示例，请参阅监视事件模块中的[高级逻辑示例](#example-of-advanced-logic-in-the-watch-events-module)。

### 操作

* [删除记录类型](#delete-a-record-type)
* [进行自定义AI调用](#make-a-custom-api-call)

#### 删除记录类型

此操作模块通过ID删除Workfront Planning中的单个记录类型。

>[!WARNING]
>
>删除Workfront Planning中的记录类型也会删除记录类型表中的所有记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录类型ID]</p>
      </td>
      <td>输入或映射要删除的记录类型的ID。</td> 
    </tr>
  </tbody>
</table>

#### 发起自定义 API 调用

此模块对[!DNL Adobe Workfront Planning] API进行自定义API调用。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>输入相对路径 <code>https://(YOUR_WORKFRONT_DOMAIN)/maestro/api/</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 方法]</p>
      </td>
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。 有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 标头]</td>
      <td>
        <p>以标准 JSON 对象的形式添加请求标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion 会自动添加授权标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 查询字符串]  </td>
      <td>
        <p>对于要添加到查询字符串的每个键/值对，单击<b>添加项</b>并输入键和值。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 正文]</td>
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>


### 搜索

#### 搜索记录

此操作模块根据您指定的条件检索记录列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Workspace]</p>
      </td>
      <td>输入或映射包含要搜索的记录的Workspace。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型]</p>
      </td>
      <td>选择要搜索的记录类型。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录字段]</p>
      </td>
      <td>对于要在搜索中使用的每个字段，请找到该字段，选择运算符，然后输入或映射要搜索的值。 根据所选的记录类型，字段可用。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Condition for filters]</p>
      </td>
      <td>选择过滤器的条件：<ul><li><b>和</b><p>模块返回符合所选字段值的<b>所有</b>的记录。</p></li><li><b>或者</b><p>该模块返回符合所选字段值的<b>any</b>的记录。</p></li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 限制]</p>
      </td>
   <td> <p>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</p> </td> 
    </tr>
  </tbody>
</table>


### 未分类


#### 创建记录

此操作在Workfront Planning中创建单个记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录类型ID]</p>
      </td>
      <td>输入或映射要创建的记录类型。 可用的记录类型基于您的Workfront Planning帐户。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>其他字段</p>
      </td>
      <td>输入希望新记录具有的值。 这些字段基于您选择的记录类型。</td> 
    </tr>
    <tr>
  </tbody>
</table>

### 删除记录

此操作模块删除Workfront Planning中的指定记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录ID]</p>
      </td>
      <td>输入或映射要删除的记录的ID。</td> 
    </tr>
  </tbody>
</table>

### 获取记录

此操作模块从其ID指定的[!DNL Adobe Workfront Planning]中检索单个记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL记录ID]</td>
      <td>输入或映射要检索的记录的ID。</td>
    </tr>
  </tbody>
</table>

### 按记录类型获取记录

此操作模块检索指定类型的所有记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Workspace]</td>
      <td>选择或映射包含要检索的记录的工作区。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 记录类型]</td>
      <td>选择要检索的记录类型。</td>
    </tr>
    <!--
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td>
    </tr>
    -->
  </tbody>
</table>

### 获取记录类型

此操作模块检索[!DNL Adobe Workfront Planning]帐户中的记录类型列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Workspace]</td>
      <td>选择或映射包含要检索的记录类型的工作区。</td>
    </tr>
  </tbody>
</table>

### 更新记录

此操作更新Workfront Planning中的单个记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Workfront Planning] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与 [!DNL Adobe Workfront Planning]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL记录ID]</p>
      </td>
      <td>输入或映射要更新的记录类型。 可用的记录类型基于您的Workfront Planning帐户。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>其他字段</p>
      </td>
      <td>输入希望记录具有的新值。 这些字段基于您选择的记录类型。</td> 
    </tr>
    <tr>
  </tbody>
</table>


## 将JSONata用于可读的`record-types`划分

以下JSONata表达式创建了Planning查询的可读输出，该输出为您提供了记录类型划分。 这使记录类型名称、字段名称和字段选项名称（如果适用）可由名称读取，并保持结构的其余部分不变。

```
(
    $s0 := ({"data":$ ~> | fields | {"options":(options){name:$}} |});
    $s1 := ({"data":$s0.data ~> | **.fields | {"options_name":(options.*){displayName:$}} | });
    $s2 := $s1 ~> | data | {"fields":(fields){displayName:$}} |; 
    $s2.data{displayName:$}
)
```

有关使用JSONata模块的信息，请参阅[JSONata模块](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/jsonata-module.md)。

## 监视事件模块中的高级逻辑示例

这是使用Workfront规划>关注事件模块时，高级逻辑采用哪种格式的示例。

```
[
  {
    "fieldName": "recordTypeId",
    "fieldValue": "Rt68c886502d4b5554ee80896b",
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "planning"
    },
    "comparison": "eq",
    "state": "newState"
  },
  {
    "fieldName": "data",
    "fieldValue": {
      "F68c886502d4b5554ee808975": "active"
    },
    "comparison": "eq",
    "state": "newState"
  }
]
```

在Watch Event模块中使用高级逻辑时，请考虑以下事项：

* 第一个`"fieldvalue":`条目是从URL中提取的计划记录类型ID。 在此示例中，Planning记录类型ID为`Rt68c886502d4b5554ee80896b`。
* Planning数据在名为`data `的数组中返回，该数组在此示例中显示为`"fieldName": "data"`。
* 规划fieldNames作为以`F`开头的ID返回。
* 由于此示例是针对`OR`筛选器连接器进行评估，因此该示例包含相同字段(`F68c886502d4b5554eec808975`)的两个条目。  模块正在筛选的两个下拉选项是`"planning"`和`"active"`。

