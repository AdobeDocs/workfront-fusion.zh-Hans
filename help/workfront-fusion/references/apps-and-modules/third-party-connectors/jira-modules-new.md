---
title: Jira模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Jira软件的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
source-git-commit: d16c1d9f257d44b72cfb93caa2a814fd62b0b733
workflow-type: tm+mt
source-wordcount: '1564'
ht-degree: 5%

---

# Jira模块

>[!NOTE]
>
>这些说明适用于Jira连接器的新版本，它简单地标记为Jira。 有关旧版Jira Cloud和Jira服务器连接器的说明，请参阅[Jira软件模块](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md)。

在Adobe Workfront Fusion场景中，您可以自动使用Jira的工作流，并将其连接到多个第三方应用程序和服务。

Jira连接器可用于Jira云和Jira数据服务器。

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

要使用Jira模块，您必须具有Jira帐户。

## 将Jira连接到Workfront Fusion

您可以直接从Jira模块内创建与Jira帐户的连接。

>[!IMPORTANT]
>
>* 要创建与Jira数据中心的基本连接，您需要一个Jira个人访问令牌。
>* 要创建与Jira云的基本连接，您需要一个Jira API令牌
>* 要创建与Jira云或Jira数据中心的OAuth 2连接，您需要一个Jira客户端ID和客户端密钥。
>
>有关创建其中任何内容的说明，请参阅Jira文档。

1. 在任意Jira模块中，单击“连接”字段旁边的&#x200B;**添加**。
1. 配置以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>连接类型</p> </td> 
      <td> <p>选择是创建基本连接还是OAuth 2连接。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>连接名称</p> </td> 
      <td> <p>输入新连接的名称。</p> </td> 
     </tr> 
     <tr>
      <td role="rowheader">服务URL</td>
      <td>输入您的Jira实例URL。 这是您用于访问Jira的URL。</td>
     </tr>
     <tr>
      <td role="rowheader">Jira帐户类型</td>
       <td>选择您是连接到Jira云还是Jira数据中心。</td>
     </tr>
     <tr> 
      <td role="rowheader">客户端 ID</td> 
      <td> <p>如果要创建OAuth 2连接，请输入您的Jira客户端ID</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">客户端密码</td> 
      <td> <p>如果要创建OAuth 2连接，请输入您的Jira客户端密钥</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">电子邮件</td> 
      <td>如果您正在创建与Jira Cloud的基本连接，请输入您的电子邮件地址。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">api令牌</td> 
      <td>如果您正在创建与Jira Cloud的基本连接，请输入您的API令牌。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">个人访问令牌</td> 
      <td>如果您正在创建与Jira数据中心的基本连接，请输入您的个人访问令牌。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API版本</td> 
      <td>选择您希望此连接连接到的Jira API版本。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。


## Jira模块及其字段

配置Jira模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Jira字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### 留意记录

此触发器模块在添加、更新或删除记录时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Webhook</td> 
   <td> <p>选择要用于监视记录的webhook，或创建新的webhook。 </p> <p>要创建新的webhook，请执行以下操作：</p> 
    <ol> 
     <li>单击<strong>添加</strong></li> 
     <li>输入webhook的名称。</li> 
     <li> 选择要用于webhook的连接。 <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </li> 
     <li> <p>选择要软件监视的记录类型：</p> 
      <ul> 
       <li>问题</li> 
       <li>评论 </li> 
       <li>工作日志 </li> 
       <li>项目 </li> 
       <li>Sprint</li> 
       <li>附件 </li> 
      </ul> </li> 
     <li>选择一个或多个将触发此方案的事件类型。</li> 
     <li>输入此模块的Jira查询语言过滤器。<p>有关JQL的详细信息，请参阅Atlassian帮助网站上的<a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a>。 </p></li>
     <li>单击<b>保存</b>以保存webhook。 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [将问题添加到冲刺](#add-issue-to-sprint)
* [创建记录](#create-a-record)
* [自定义API调用](#custom-api-call)
* [删除记录](#delete-a-record)
* [下载附件](#download-an-attachment)
* [读取记录](#read-a-record)
* [更新记录](#update-a-record)

#### 将问题添加到冲刺

此操作模块向冲刺添加一个或多个问题。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">冲刺ID</td> 
   <td>输入或映射要添加问题的冲刺(sprint)的Sprint ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">问题ID</td> 
   <td>对于要添加到冲刺的每个问题或键，单击<b>添加项</b>并输入问题ID或键。 在一个模块中最多可输入50个。</td> 
  </tr> 
 </tbody> 
</table>

#### 创建记录

此操作模块在Jira中创建新记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择要模块创建的记录类型。</p> 
    <ul> 
     <li>附件</li> 
     <li>评论</li> 
     <li>问题</li> 
     <li>项目</li> 
     <li>Sprint </li> 
     <li>工作日志</li> 
     <li>用户</li> 
     <li>展示板</li> 
     <li>类别</li> 
     <li>筛选条件</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">其他字段</td> 
   <td> 填写其他字段。 字段可用，具体取决于所选的记录类型。 </td> 
  </tr> 
 </tbody> 
</table>

#### 自定义API调用

通过此操作模块，您可以对Jira API进行经过身份验证的自定义调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>输入相对路径<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">方法</td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">标头</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">查询字符串</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">正文</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### 删除记录

此操作模块删除指定的记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择要模块删除的记录类型。 </p> 
    <ul> 
     <li>评论</li> 
     <li>问题</li> 
     <li>项目</li> 
     <li>Sprint </li> 
     <li>工作日志</li> 
     <li>附件</li> 
     <li>展示板</li> 
     <li>类别</li> 
     <li>筛选条件</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">（记录类型）ID</td> 
   <td>输入或映射要删除的记录的ID或键。</td> 
  </tr> 
 </tbody> 
</table>

#### 下载附件

此操作模块下载指定的附件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID</td> 
   <td>输入或映射要下载的附件的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 读取记录

此操作模块从Jira中的指定记录读取数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择您希望模块读取的Jira记录的类型。</p> 
    <ul> 
     <li>附件</li> 
     <li>评论</li> 
     <li>问题</li> 
     <li>项目</li> 
     <li>Sprint </li> 
     <li>工作日志</li> 
     <li>用户</li> 
     <li>展示板</li> 
     <li>类别</li> 
     <li>筛选条件</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出</td> 
   <td>选择要接收的输出。 根据在“记录类型”字段中选择的记录类型，输出选项可用。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">（记录类型）ID</td> 
   <td> <p>输入或映射您希望模块读取的记录的唯一Jira ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 更新记录

此操作模块更新现有记录，如问题或项目。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择您希望模块更新的记录类型。 选择记录类型后，该记录类型特有的其他字段将显示在模块中。</p> 
    <ul> 
     <li>评论</li> 
     <li>问题</li> 
     <li>项目</li> 
     <li>Sprint </li> 
     <li>过渡问题</li> 
     <li>类别 </li> 
     <li>筛选条件 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">ID或密钥</td> 
   <td>输入或映射要更新的记录的ID或键。</td> 
  <tr> 
   <td role="rowheader">其他字段</td> 
   <td> 填写其他字段。 字段可用，具体取决于所选的记录类型。 </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### 搜索记录

此搜索模块在Jira中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择要模块搜索的记录类型。 选择记录类型后，该记录类型特有的其他字段将显示在模块中。</p> 
    <ul> 
     <li>问题</li> 
     <li>项目</li> 
     <li>用户</li> 
     <li>Sprint</li> 
     <li>展示板</li> 
     <li>工作日志</li> 
     <li>评论</li> 
     <li>过渡问题</li> 
     <li>类别</li> 
    </ul> </td> 
  <tr> 
   <td role="rowheader"> <p>最大结果</p> </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中检索的最大记录数。</p> </td> 
  </tr> 
   <tr> 
    <td role="rowheader">偏移</td> 
    <td> 输入或映射要检索其详细信息的第一个项目的ID。 这是对记录进行分页的一种方式。 如果输入第5000个项目作为抵销，则模块将返回项目5000-9999。</td> 
   </tr>
  <tr> 
   <td role="rowheader">其他字段</td> 
   <td> 填写其他字段。 字段可用，具体取决于所选的记录类型。 </td> 
  </tr> 
 </tbody> 
</table>
