---
title: Adobe I/O Events模块
description: 通过Adobe I/O Events模块，您可以基于Adobe应用程序中的事件启动Adobe Workfront Fusion场景。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: b2229f3e-a2a7-4b07-8ead-a37d193c2ec7
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '957'
ht-degree: 1%

---

# Adobe I/O Events模块

通过Adobe I/O Events模块，您可以基于没有专用Adobe Workfront Fusion连接器的Adobe帐户和服务中的事件启动Workfront Fusion方案。

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

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

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
   <td role="rowheader">基本URL</td> 
   <td>https://api.adobe.io/events</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.6.7</td> 
  </tr>
 </tbody> 
 </table>

## 创建与Adobe I/O Events的连接

要为您的Adobe I/O Events模块创建连接，请执行以下操作：

1. 单击“连接”框旁边的“添加”。

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
        <td role="rowheader">客户端密码</td>
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

1. 单击&#x200B;**继续**&#x200B;保存连接并返回模块。

## Adobe I/O Events模块及其字段

配置[!DNL Adobe I/O Events]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Adobe I/O Events]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### 创建事件注册

此操作模块使用webhook创建事件说明。 您可以在此处配置webhook。 如果您使用的是现有webhook，则此模块中的字段为只读。

要创建webhook，请执行以下操作：

1. 单击Webhook字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[！UICONTROL Webhook名称]</td>
        <td>输入此webhook的名称。</td>
       </tr>
       <tr>
         <td role="rowheader">[！UICONTROL Connection]</td>
        <td>有关创建与[!DNL Adobe I/O Events]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >创建与[!DNL Adobe I/O Events]</a>的连接。</td>
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

1. 单击保存以保存webhook并返回到模块。

### 操作

#### 从日志中获取所有事件

此搜索模块从日志中检索注册的所有事件。

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[！UICONTROL Connection]</td>
        <td>有关创建与[!DNL Adobe I/O Events]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >创建与[!DNL Adobe I/O Events]</a>的连接。</td>
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
           [！UICONTROL返回的最大记录数]
         </td>
         <td>
              输入或映射您希望模块在每个方案执行周期内返回的最大记录数。 
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL返回在]之后发生的事件
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [！UICONTROL Seek]
         </td>
         <td>
         </td>
       </tr>
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

#### 进行自定义API调用

此操作模块对[!DNL Adobe I/O Events] API进行自定义API调用

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[！UICONTROL Connection]</td>
        <td>有关创建与[!DNL Adobe I/O Events]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >创建与[!DNL Adobe I/O Events]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL路径]</p>
      </td>
      <td>
        <p>输入相对路径 <code>https://api.adobe.io/events</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL方法]</p>
      </td>
      <td>
  <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p>  
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion会自动添加授权标头和x-api-key标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL查询字符串]  </td>
      <td>
        <p>输入请求查询字符串。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Body]</td>
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### 搜索

#### 获取提供程序和事件ID

此搜索模块获取指定提供程序和事件的Adobe I/O Events ID。

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[！UICONTROL Connection]</td>
        <td>有关创建与[!DNL Adobe I/O Events]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" >创建与[!DNL Adobe I/O Events]</a>的连接。</td>
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

<!--

Watch Events

This trigger module starts a scenario when an event occurs in the chosen Adobe product or service.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">Webhook</td> 
   <td><p>Select the webhook that you want to use for this trigger, or add a new webhook. </p><p>To add a new webhook, <ol><li>Click <b>Add</b> next to the webhook field.</li><li>Enter the following: <ul><li>A name for the webhook</li><li>The connection that you want to use for this webhook</li><li>The source of the events you want to watch</li></ul></li><li>Click <b>Save</b> to save the webhook and return to the module. </td> 
   </tr> 
   </tbody> 
</table>

-->
