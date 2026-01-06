---
title: Jira 模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Jira软件的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: b74a3618-c4a1-4965-a88d-1643bfab12db
source-git-commit: 017341e045a703f5d6e933a6df860f4fc8c0649d
workflow-type: tm+mt
source-wordcount: '2348'
ht-degree: 20%

---

# Jira 模块

>[!NOTE]
>
>这些说明适用于Jira连接器的新版本，它简单地标记为Jira。 有关旧版Jira Cloud和Jira服务器连接器的说明，请参阅[Jira软件模块](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-software-modules.md)。

在Adobe Workfront Fusion场景中，您可以自动使用Jira的工作流，并将其连接到多个第三方应用程序和服务。

Jira连接器可用于Jira云和Jira数据服务器。

有关创建场景的说明，请参阅[创建场景：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)中的相关文章。

有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)中的相关文章。

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

* 要使用Jira模块，您必须具有Jira帐户。
* 您必须有权访问Jira Developer Console才能在Jira中创建OAuth2应用程序。

## 将Jira连接到Workfront Fusion

创建与Jira的连接过程因您创建的是基本连接还是OAuth2连接而异。

* [创建与Jira的OAuth2连接](#create-an-oauth2-connection-to-jira)
* [创建与Jira的基本连接](#create-a-basic-connection-to-jira)

### 创建与Jira的OAuth2连接

要创建与Jira的OAuth2连接，必须先在Jira中创建应用程序，然后才能在Fusion中配置连接。

* [在Jira中创建OAuth2应用程序](#create-an-oauth2-application-in-jira)
* [在Fusion中配置Outt2连接](#configure-the-oauth2-connection-in-fusion)

#### 在Jira中创建OAuth2应用程序

>[!IMPORTANT]
>
>您必须有权访问Jira Developer Console，才能为Jira连接创建和配置OAuth2应用程序。

1. 转到[Jira Developer Console](https://developer.atlassian.com/console.myapps/)。
1. 在“我的应用程序”区域中，单击&#x200B;**创建**，然后选择&#x200B;**OAuth 2.0集成**。
1. 输入集成的名称，同意开发人员条款，然后单击&#x200B;**创建**。

   此时将创建应用程序，并转到应用程序配置区域。
1. 在左侧导航面板中单击&#x200B;**权限**。
1. 在“权限”区域中，找到&#x200B;**Jira API**&#x200B;行。
1. 单击Jira API行中的&#x200B;**添加**，然后单击同一行中的&#x200B;**继续**。
1. 启用以下范围：

   * 查看Jira问题数据(`read:jira-work`)
   * 查看用户配置文件(`read:jira-user`)
   * 创建和管理问题(`write:jira-work`)

1. 在左侧导航中，单击&#x200B;**授权**。
1. 在OAuth 2.0授权的行中单击&#x200B;**添加**。
1. 在&#x200B;**回调URL**&#x200B;字段中，根据您的Workfront Fusion数据中心，输入以下URL之一：

   | 融合数据中心 | 回调 URL |
   |---|---|
   | US | `https://app.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | 欧盟 | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira2` |
   | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira2` |

1. 在左侧导航中，单击&#x200B;**设置**。
1. （可选）在“描述”字段中输入描述，然后单击该字段下的&#x200B;**保存更改**。
1. 将客户端ID和客户端密钥从设置区域复制到安全位置，或者在Fusion中配置连接时保持此页面打开。
1. 继续[在Fusion](#configure-the-oauth2-connection-in-fusion)中配置OAutt2连接

#### 在Fusion中配置Oauth2连接

1. 在任意Jira模块中，单击“连接”字段旁边的&#x200B;**添加**。
1. 配置以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>连接类型</p> </td> 
      <td> <p>选择<b>OAuth 2</b>。</p> </td> 
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
      <td> <p>输入您在<a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override="">中创建的Jira应用程序的客户端ID在Jira</a>中创建OAuth2应用程序。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">客户端密钥</td> 
      <td> <p>输入您在<a href="#create-an-oauth2-application-in-jira" class="MCXref xref" data-mc-variable-override="">中创建的Jira应用程序的客户端密钥。在Jira</a>中创建OAuth2应用程序。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">其他范围</td> 
      <td>输入要添加到此连接的任何其他范围。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API 版本</td> 
      <td>选择您希望此连接连接到的Jira API版本。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

### 创建与Jira的基本连接

创建与Jira的基本连接有所不同，具体取决于您是创建与Jira云还是Jira数据中心的连接。

* [创建与Jira Cloud的基本连接](#create-a-basic-connection-to-jira-cloud)
* [创建与Jira数据中心的基本连接](#create-a-basic-connection-to-jira-data-center)

#### 创建与Jira Cloud的基本连接

>[!IMPORTANT]
>
> 要创建与Jira云的基本连接，您必须具有Jira API令牌。
>有关获取Jira API令牌的说明，请参阅Atlassian文档中的[管理Atlassian帐户的API令牌](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account)。


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
      <td role="rowheader">电子邮件</td> 
      <td>输入您的电子邮件地址。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">api令牌</td> 
      <td>输入您的API令牌。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API 版本</td> 
      <td>选择您希望此连接连接到的Jira API版本。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

#### 创建与Jira数据中心的基本连接

>[!IMPORTANT]
>
> 要创建与Jira数据中心的基本连接，您必须具有Jira个人访问令牌(PAT)。
>有关获取Jira个人访问令牌的说明，请参阅Atlassian文档中的[管理Atlassian帐户的API令牌](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html)。
>有关创建PAT时的注意事项，请参阅本文中的[配置PAT](#configure-your-pat)。

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
      <td role="rowheader">PAT（个人访问令牌）</td> 
      <td>输入您的Jira个人访问令牌。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">API 版本</td> 
      <td>选择您希望此连接连接到的Jira API版本。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

##### 配置您的PAT

要创建与Jira数据中心的基本连接，您必须具有Jira个人访问令牌(PAT)。

有关获取Jira个人访问令牌的说明，请参阅Atlassian文档中的[管理Atlassian帐户的API令牌](https://confluence.atlassian.com/enterprise/using-personal-access-tokens-1026032365.html)。

配置PAT时，可能需要以下信息

* 重定向URL

  | 融合数据中心 | 重定向 URL |
  |---|---|
  | US | `https://app.workfrontfusion.com/oauth/cb/workfront-jira` |
  | 欧盟 | `https://app-eu.workfrontfusion.com/oauth/cb/workfront-jira` |
  | Azure | `https://app-az.workfrontfusion.com/oauth/cb/workfront-jira` |

* 文件配置

要使用PAT，必须在文件`jira/bin/WEB-INF/classes`的文件`jira-config.properties`中启用以下内容：

* `jira.rest.auth.allow.basic = true`
* `jira.rest.csrf.disabled = true`

如果此文件不存在，则必须创建它。

## Jira模块及其字段

配置Jira模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Jira字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

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
   <td> <p>选择要用于监视记录的webhook，或创建新的webhook。 </p> <p>要创建新的 Webhook：</p> 
    <ol> 
     <li>单击<strong>添加</strong></li> 
     <li>输入webhook的名称。</li> 
     <li> 选择要用于webhook的连接。 <p>有关将Jira帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将Jira连接到Workfront Fusion</a>。</p> </li> 
     <li> <p>选择要软件监视的记录类型：</p> 
      <ul> 
       <li>问题</li> 
       <li>注释 </li> 
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
     <li>注释</li> 
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
   td&gt; <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">标头</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">查询字符串</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">正文</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
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
     <li>注释</li> 
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
     <li>注释</li> 
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
     <li>注释</li> 
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

>[!IMPORTANT]
>
>旧版Jira连接器使用的搜索模块可能会导致以下错误：
>
>`[410] The requested API has been removed. Please migrate to the /rest/api/3/search/jql API. A full migration guideline is available at https://developer.atlassian.com/changelog/#CHANGE-2046`
>
>这是由于Jira方面的弃用。
>
>如果遇到此错误，您可以使用新连接器的搜索模块替换旧版Jira连接器的搜索模块。 请注意，新连接器允许您选择使用的API版本。 创建连接时请务必选择V3。
>
> 新Jira连接器中的![API版本选项](/help/workfront-fusion/references/apps-and-modules/assets/jira-version-option.png)
>
>请注意：
>
>* 只有搜索模块受影响。 目前，Fusion连接器使用的其他Jira API端点不受此弃用的影响。
>
>* 地理转出可能会导致不一致。 Atlassian正在区域范围内推出此更改，这意味着某些Jira云实例可能仍会临时支持旧端点。 这可能会导致环境之间的行为不一致。

#### 搜索记录

此搜索模块在Jira中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景后续的模块中映射这些信息。

在配置此模块时，会显示以下字段。

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
     <li>注释</li> 
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
