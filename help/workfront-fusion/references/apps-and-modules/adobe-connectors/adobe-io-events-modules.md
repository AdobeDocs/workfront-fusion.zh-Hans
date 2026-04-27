---
title: Adobe I/O Events 模块
description: 通过Adobe I/O Events模块，您可以基于Adobe应用程序中的事件启动Adobe Workfront Fusion场景。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: b2229f3e-a2a7-4b07-8ead-a37d193c2ec7
source-git-commit: bbd1ec27e52127c8814188612a1e8d5cfab0cd25
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 44%

---

# Adobe I/O Events 模块

通过Adobe I/O Events模块，您可以基于没有专用Adobe Workfront Fusion连接器的Adobe帐户和服务中的事件启动Workfront Fusion方案。

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
   <td role="rowheader">Adobe Workfront Fusion 许可证</td> 
   <td>
   <p>基于操作：不需要 Workfront Fusion 许可证</p>
   <p>基于连接器（旧版）：Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

有关 Adobe Workfront Fusion 许可证的详细信息，请参阅 [Adobe Workfront Fusion 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

在使用Adobe I/O Events连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的Adobe帐户。

## Adobe I/O Events API信息

Adobe I/O Events连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td>https://api.adobe.io/events</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.6.7</td> 
  </tr>
 </tbody> 
 </table>

## 创建与Adobe I/O Events的连接

要为您的Adobe I/O Events模块创建连接，请执行以下操作：

1. 点击“连接”框旁的“添加”。

1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">连接名称</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">环境</td>
        <td>
          <p>选择您要连接到生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">类型</td>
        <td>
          <p>选择您要连接到服务帐户还是个人帐户。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">其他范围</td>
        <td>要添加任何其他范围，请单击<b>添加项</b>并输入范围。</td>
      </tr>
      <tr>
        <td role="rowheader">客户端 ID</td>
        <td>输入您的Adobe客户端ID。 可在Adobe Developer Console的“凭据详细信息”部分找到此项</td>
      </tr>
      <tr>
        <td role="rowheader">客户端密钥</td>
        <td>输入您的Adobe客户端密钥。 可在Adobe Developer Console的“凭据详细信息”部分找到此项</td>
      </tr>
      </tr>
        <tr>
        <td role="rowheader">使用者组织ID</td>
        <td>输入您的消费者组织ID。 这可以在项目的凭据URL中找到： <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">凭据ID</td>
        <td>输入凭据ID。 这可以在项目的凭据URL中找到： <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">IMS组织ID</td>
        <td>输入您的Adobe组织ID。 可在Adobe Developer Console的“凭据详细信息”部分找到此项</td>
      </tr>
        <tr>
        <td role="rowheader">项目 ID</td>
        <td>输入您的项目ID。 这可以在项目的凭据URL中找到： <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">WORKSPACE ID</td>
        <td>要查看项目的Workspace ID，请从Adobe Developer Console的项目概述页面下载项目详细信息。 </td>
      </tr>
    </tbody>
    </table>

1. 点击&#x200B;**继续**&#x200B;保存连接并返回模块。

## Adobe I/O Events模块及其字段

在您配置 [!DNL Adobe I/O Events] 模块时，Workfront Fusion 会显示以下字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Adobe I/O Events] 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### 创建事件注册

此操作模块使用webhook创建事件说明。 您可以在此处配置webhook。 如果您使用的是现有webhook，则此模块中的字段为只读。

要创建webhook，请执行以下操作：

1. 单击 Webhook 字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Webhook 名称]</td>
        <td>为此 Webhook 输入一个名称。</td>
       </tr>
       <tr>
         <td role="rowheader">[!UICONTROL 连接]</td>
        <td>有关创建与 [!DNL Adobe I/O Events] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >创建与 [!DNL Adobe I/O Events]</a> 的连接。</td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL Webhook说明]
         </td>
         <td>
           输入此webhook的说明。
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL事件提供程序]
         </td>
         <td>
           选择要从中创建事件的产品或帐户。
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL事件类型]
         </td>
         <td>
           选择您希望webhook观看的事件。 当这些事件发生时，将触发该方案。
         </td>
       </tr>
     </tbody>
   </table>

1. 点击“保存”以保存 Webhook 并返回模块。

### 操作

* [获取提供程序和事件ID](#get-provider-and-event-ids)
* [发起自定义 API 调用](#make-a-custom-api-call)

#### 获取提供程序和事件ID

此搜索模块获取指定提供程序和事件的Adobe I/O Events ID。

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL 连接]</td>
        <td>有关创建与 [!DNL Adobe I/O Events] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >创建与 [!DNL Adobe I/O Events]</a> 的连接。</td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL事件提供程序]
         </td>
         <td>
           选择要为其检索ID的提供程序。
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL事件类型]
         </td>
         <td>
              选择要为其提供ID的事件。 根据事件提供程序，事件将可用。 
         </td>
       </tr>
     </tbody>
   </table>


#### 发起自定义 API 调用

此操作模块对[!DNL Adobe I/O Events] API进行自定义API调用

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL 连接]</td>
        <td>有关创建与 [!DNL Adobe I/O Events] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >创建与 [!DNL Adobe I/O Events]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 路径]</p>
      </td>
      <td>
        <p>输入相对路径 <code>https://api.adobe.io/events</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 方法]</p>
      </td>
      <td>
  <p>选择用于配置此 API 调用的 HTTP 请求方法。 有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p>  
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 标头]</td>
      <td>
        <p>以标准 JSON 对象的形式添加请求标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion会自动添加授权标头和x-api-key标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 查询字符串]  </td>
      <td>
        <p>输入请求的查询字符串。</p>
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

#### 从日志中获取所有事件

此搜索模块从日志中检索注册的所有事件。

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL 连接]</td>
        <td>有关创建与 [!DNL Adobe I/O Events] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >创建与 [!DNL Adobe I/O Events]</a> 的连接。</td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL注册ID]
         </td>
         <td>
           选择要检索事件的注册。
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL返回的最大事件数]
         </td>
         <td>
              输入或映射每次场景执行周期中该模块允许返回的最大记录数量。 
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL返回在]之后发生的事件
         </td>
         <td>输入或映射日期。 模块返回在此日期之后发生的事件。
         </td>
       </tr>
<!--
<tr>
         <td role="rowheader">
           [!UICONTROL Seek]
         </td>
         <td>
         </td>
       </tr>
-->
       <tr>
         <td role="rowheader">
           [！UICONTROL最新]
         </td>
         <td>
         启用此选项可返回最新的事件。
         </td>
       </tr>
     </tbody>
   </table>

监控事件

当所选Adobe产品或服务中发生事件时，此触发器模块将启动一个场景。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">Webhook</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击webhook字段旁边的<b>添加</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>要观看的事件的来源</li></ul></li><li>点击<b>保存</b>以保存 Webhook 并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

-->
