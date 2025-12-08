---
title: Adobe Workfront 规划模块
description: 通过 [!DNL Adobe Workfront Planning] 模块，您可以根据 [!DNL Adobe] Adobe Workfront Planning帐户中的事件启动Workfront Fusion方案，创建、读取或更新协议和其他记录，使用您设置的条件搜索记录以及上载文档。
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: 30ddefa8519e6f2052308482137d0fa018676902
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 44%

---

# [!DNL Adobe Workfront Planning] 模块

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

s##先决条件

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
   <td>https://{{connection.host}}/maestro/api/{{common.maestroApiVersion}}/</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## 创建与 [!DNL Adobe Workfront Planning] 的连接 {#create-a-connection-to-adobe-workfront-planning}

您可以在Workfront Fusion模块内直接创建与[!DNL Workfront Planning]帐户的连接。

1. 在任意 [!DNL Adobe Workfront Planning] 模块中，点击“连接”框旁的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL 连接名称]</td>
          <td>
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 环境]</td>
          <td>选择您要连接到生产环境还是非生产环境。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 类型]</td>
          <td>选择您是要连接到服务帐户还是个人帐户。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端 ID]<p>（可选）</p></td>
          <td>输入您的 [!DNL Adobe] [!UICONTROL 客户端 ID]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端密钥]<p>（可选）</p></td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 身份验证 URL]</td>
          <td>输入您的Workfront实例将用于对此连接进行身份验证的URL。 <p>默认值为 <code>https://oauth.my.workfront.com/integrations/oauth2</code>。</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 主机前缀]</td>
          <td>输入您的主机前缀。<p>默认值为 <code>origin-</code>。</p>
        </tr>
      </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## [!DNL Adobe Workfront Planning] 模块及其字段

在您配置 Workfront 模块时，Workfront Fusion 会显示以下字段。除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 Workfront 字段。模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。


![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)
* [未分类](#uncategorized)

### 触发器

#### 观看活动

在Workfront Planning中创建、更新或删除记录、记录类型或工作区时，此触发器模块将启动一个方案。

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
      <td> <p>您可以设置筛选条件，仅观看符合您所选条件的记录。</p> <p>对于每个筛选条件，请输入要评估的字段、运算符以及筛选条件应允许的值。您可以通过添加 AND 规则来使用多个筛选条件。</p> <p>注意：您无法编辑现有Workfront Webhook中的筛选器。 如需为 Workfront 事件订阅设置不同的筛选条件，请删除当前 Webhook 并创建一个新的。</p> <p>有关事件过滤器的详细信息，请参阅Workfront模块文章中的Workfront &gt; [！UICONTROL观看活动]模块中的<a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">事件订阅过滤器</a>。</p> </td> 
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
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
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
     <!--<tr>
      <td role="rowheader">
        <p>[!UICONTROL Maximum number of returned records]</p>
      </td>
      <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> -->
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

