---
title: Adobe Workfront规划模块
description: 使用 [!DNL Adobe Workfront Planning] 模块，您可以基于 [!DNL Adobe] Workfront Planning帐户中的事件启动 [!DNL Adobe Workfront Fusion] 方案，创建、读取或更新协议和其他记录，使用您设置的条件搜索记录以及上载文档。
author: Becky
feature: Workfront Fusion
exl-id: d1bc9e39-da49-4090-a106-14b52855bc8f
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1532'
ht-degree: 0%

---

# [!DNL Adobe Workfront Planning]模块

通过[!DNL Adobe Workfront Planning]模块，您可以在Workfront Planning中发生事件时触发方案。 您还可以创建、读取、更新和删除记录，或者对您的[!DNL Adobe Workfront Planning]帐户执行自定义API调用。

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
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

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
   <td role="rowheader">基本URL</td> 
   <td>https://{{connection.host}}/maestro/api/{{common.maestroApiVersion}}/</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.13.7</td> 
  </tr>
 </tbody> 
 </table>

## 创建与[!DNL Adobe Workfront Planning]的连接 {#create-a-connection-to-adobe-workfront-planning}

您可以在[!DNL Workfront Fusion]模块内直接创建与[!DNL Workfront Planning]帐户的连接。

1. 在任意[!DNL Adobe Workfront Planning]模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

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
          <td role="rowheader">[!UICONTROL 客户端ID]<p>（可选）</p></td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端ID]。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端密钥]<p>（可选）</p></td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 身份验证URL]</td>
          <td>输入您的Workfront实例将用于对此连接进行身份验证的URL。 <p>默认值为<code>https://oauth.my.workfront.com/integrations/oauth2</code>。</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 主机前缀]</td>
          <td>输入您的主机前缀。<p>默认值为<code>origin-</code>。</p>
        </tr>
      </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## [!DNL Adobe Workfront Planning]模块及其字段

配置Workfront模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Workfront字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。


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
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 对象类型]</td>
      <td>选择您要监视记录、记录类型还是工作区。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 状态]</td>
      <td>选择您要观察旧状态还是新状态。<ul><li><p><b>[!UICONTROL 新状态]</b></p><p>当记录将<b>更改为</b>给定值时触发方案。</p></li><li><p><b>[!UICONTROL 旧状态]</b></p><p>当记录从</b>更改<b>给定值时触发方案。</p></li></ul></td> 
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>如果观看记录，请选择您想要观看记录的Workspace。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 记录类型]</td>
      <td>如果观看记录，请选择您要观看的记录类型。</td>
    </tr>
    </tr>
     <tr data-mc-conditions=""> 
      <td> <p>[!UICONTROL 事件过滤器]</p> </td> 
      <td> <p>您可以设置过滤器，以仅监视符合您选择标准的记录。</p> <p>对于每个筛选器，输入希望筛选器计算的字段、运算符以及希望筛选器允许的值。 通过添加AND规则，您可以使用多个过滤器。</p> <p>注意：您无法编辑现有[!DNL Workfront] Webhook中的筛选器。 要为[!DNL Workfront]事件订阅设置不同的筛选器，请删除当前webhook并创建一个新筛选器。</p> <p>有关事件过滤器的详细信息，请参阅Workfront模块文章中的[!DNL Workfront] &gt; [!UICONTROL 监视事件]模块中的<a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#event-subscription-filters-in-the-workfront--watch-events-modules" class="MCXref xref">事件订阅过滤器</a>。</p> </td> 
     </tr> 
    <tr>
      <td role="rowheader">[!UICONTROL 要监视的对象]</td>
      <td>选择是否要监视新的。 更新、新增和更新或删除的记录。</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 排除此连接所做的更新]</p>
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
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型ID]</p>
      </td>
      <td>输入或映射要删除的记录类型的ID。</td> 
      </tr>
  </tbody>
</table>

#### 进行自定义API调用

此模块对[!DNL Adobe Workfront Planning] API进行自定义API调用。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
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
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 自动添加授权标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 查询字符串]  </td>
      <td>
        <p>对于要添加到查询字符串的每个键/值对，单击<b>添加项</b>并输入键和值。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
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
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Workspace]</p>
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
        <p>[!UICONTROL 记录字段]</p>
      </td>
      <td>对于要在搜索中使用的每个字段，请找到该字段，选择运算符，然后输入或映射要搜索的值。 根据所选的记录类型，字段可用。</td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL Condition for filters]</p>
      </td>
      <td>选择过滤器的条件：<ul><li><b>和</b><p>模块返回符合所选字段值的<b>所有</b>的记录。</p></li><li><b>或</b><p>该模块返回符合所选字段值的<b>any</b>的记录。</p></li></ul></td> 
      </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 限制]</p>
      </td>
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
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
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录类型ID]</p>
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
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录ID]</p>
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
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 记录ID]</td>
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
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
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
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
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
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Workfront Planning]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-workfront-planning" class="MCXref xref" >创建与[!DNL Adobe Workfront Planning]</a>的连接。</td>
    </tr>
     <tr>
      <td role="rowheader">
        <p>[!UICONTROL 记录ID]</p>
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
