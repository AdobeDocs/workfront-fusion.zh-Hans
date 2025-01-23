---
title: Jira软件模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用 [!DNL Jira] 软件的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 92cac080-d8f6-4770-a6a6-8934538c978b
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1880'
ht-degree: 1%

---

# [!DNL Jira Software]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Jira Software]的工作流，并将其连接到多个第三方应用程序和服务。

这些说明适用于Jira Cloud和Jira服务器模块。

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
   <p>当前：无Workfront Fusion许可证要求。</p>
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

要使用[!DNL Jira]模块，您必须具有[!DNL Jira]帐户。

## Jira API信息

Jira连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"></td> 
   <td> Jira Cloud</td> 
   <td> Jira服务器</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersion</td> 
   <td> 2</td> 
   <td> 2</td> 
  </tr> 
  <tr> 
   <td role="rowheader">apiVersionAgile</td> 
   <td> 1.0 </td> 
   <td> 1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>1.7.29</td> 
   <td>1.0.19</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Jira Software]连接到[!DNL Workfront Fusion]

您的连接方法基于您使用的是[!DNL Jira Cloud]还是[!DNL Jira Server]。

* [连接 [!DNL Jira Cloud] 到Workfront Fusion](#connect-jira-cloud-to-workfront-fusion)
* [连接 [!DNL Jira Server] 到 [!DNL Workfront Fusion]](#connect-jira-server-to-workfront-fusion)

### 将[!DNL Jira Cloud]连接到[!DNL Workfront Fusion]

将[!DNL Jira Cloud]连接到[!DNL Workfront Fusion]

要将[!DNL Jira Software]连接到[!DNL Workfront Fusion]，您必须创建一个API令牌，并将其与您的服务URL和用户名一起插入到[!DNL Workfront Fusion]中的[!UICONTROL Create a connection]字段。

#### 在[!DNL Jira]中创建API令牌

1. 在Jira中创建API令牌。

   有关说明，我们建议您在Jira文档中搜索“创建API令牌”。
1. 创建令牌后，将令牌复制到安全位置。

   >[!IMPORTANT]
   >
   >关闭此对话框后，无法再次查看令牌。
1. 将生成的令牌存储在安全位置。
1. 继续[在 [!DNL Workfront Fusion]](#configure-the-jira-api-token-in-workfront-fusion)中配置 [!DNL Jira] API令牌。

#### 在[!DNL Workfront Fusion]中配置[!DNL Jira] API令牌

1. 在[!DNL Workfront Fusion]中的任意[!DNL Jira Cloud]模块中，单击[!UICONTROL connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 指定以下信息：

   * **环境**
   * **类型**
   * **[!UICONTROL Service URL]：**&#x200B;这是用于访问Jira帐户的基本URL。 示例： `yourorganization.atlassian.net`
   * **[!UICONTROL Username]**
   * **[!UICONTROL API token]：**&#x200B;这是您在[在此文章的 [!DNL Jira]](#create-an-api-token-in-jira)部分中创建API令牌时创建的API令牌。

1. 单击[!UICONTROL Continue]以创建连接并返回模块。

### 将[!DNL Jira Server]连接到[!DNL Workfront Fusion]

要授权[!DNL Workfront Fusion]与[!DNL Jira Server]之间的连接，您需要消费者密钥、私钥和服务URL。 您可能需要联系[!DNL Jira]管理员以获取此信息。

* [为 [!DNL Jira] 连接生成公钥和私钥](#generate-public-and-private-keys-for-your-jira-connection)
* [将客户端应用程序配置为 [!DNL Jira]中的消费者](#configure-the-client-app-as-a-consumer-in-jira)
* [创建与 [!DNL Workfront Fusion]中的 [!DNL Jira] 服务器或Jira数据中心的连接](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)

#### 为您的[!DNL Jira]连接生成公钥和私钥

要获取[!DNL Workfront Fusion Jira]连接的私钥，您需要生成公钥和私钥。

1. 在终端中，运行以下`openssl`命令。

   * `openssl genrsa -out jira_privatekey.pem 1024`

     此命令生成1024位私钥。

   * `openssl req -newkey rsa:1024 -x509 -key jira_privatekey.pem -out jira_publickey.cer -days 365`

     此命令创建X509证书。

   * `openssl pkcs8 -topk8 -nocrypt -in jira_privatekey.pem -out jira_privatekey.pcks8`

     此命令将私钥（PKCS8格式）提取到`jira_privatekey.pcks8`文件。

   * `openssl x509 -pubkey -noout -in jira_publickey.cer  > jira_publickey.pem`

     此命令将公钥从证书提取到`jira_publickey.pem`文件。

     >[!NOTE]
     >
     >如果您使用的是Windows，您可能需要手动将公钥保存到`jira_publickey.pem`文件：
     >
     >1. 在终端中，运行以下命令：
     >   
     >   `openssl x509 -pubkey -noout -in jira_publickey.cer`
     >   
     >1. 复制终端输出，包括`-------BEGIN PUBLIC KEY--------`和`-------END PUBLIC KEY--------`。
     >   
     >1. 将终端输出粘贴到名为`jira_publickey.pem`的文件中。


1. 继续[将客户端应用程序配置为 [!DNL Jira]](#configure-the-client-app-as-a-consumer-in-jira)中的消费者

#### 在[!DNL Jira]中将客户端应用配置为消费者

1. 登录到您的[!DNL Jira]实例。
1. 在左侧导航面板中，单击&#x200B;**[!UICONTROL [!DNL Jira] Settings]** ![](/help/workfront-fusion/references/apps-and-modules/assets/jira-settings-icon.png) > **[!UICONTROL Applications]**> **[!UICONTROL Application links]**。
1. 在&#x200B;**[!UICONTROL Enter the URL of the application you want to link]**&#x200B;字段中，输入

   ```
   https://app.workfrontfusion.com/oauth/cb/workfront-jiraserver-oauth1
   ```

1. 单击 **[!UICONTROL Create new link]**。忽略“No received from the URL you entered（从输入的URL未收到任何响应）”错误消息。
1. 在&#x200B;**[!UICONTROL Link applications]**&#x200B;窗口中，在&#x200B;**[!UICONTROL Consumer key]**&#x200B;和&#x200B;**[!UICONTROL Shared secret]**&#x200B;字段中输入值。

   您可以选择这些字段的值。

1. 将&#x200B;**[!UICONTROL Consumer key]**&#x200B;和&#x200B;**[!UICONTROL Shared secret]**&#x200B;字段的值复制到安全位置。

   在配置过程的后续步骤中，您将需要这些值。

1. 按如下方式填写URL字段：

   | 字段 | 描述 |
   |---|---|
   | [!UICONTROL Request Token URL] | `<Jira base url>/plugins/servlet/oauth/request-token` |
   | [!UICONTROL Authorization URL] | `<Jira base url>/plugins/servlet/oauth/authorize` |
   | [!UICONTROL Access Token URL] | `<Jira base url>/plugins/servlet/oauth/access-token` |

1. 选中&#x200B;**[!UICONTROL Create incoming link]**&#x200B;复选框。
1. 单击 **[!UICONTROL Continue]**。
1. 在&#x200B;**[!UICONTROL Link applications]**&#x200B;窗口中，填写以下字段：

   <table style="table-layout:auto"> 
    <col data-mc-conditions=""> 
    <col data-mc-conditions=""> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Consumer Key]</p> </td> 
      <td> 将您复制的使用者密钥粘贴到安全位置。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Consumer name]</td> 
      <td>输入您选择的名称。 此名称供您参考。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Public key]</td> 
      <td>从<code>[!DNL jira_publickey.pem]</code>文件中粘贴公钥。</td> 
     </tr> 
    </tbody> 
   </table>

1. 单击 **[!UICONTROL Continue]**。
1. 继续[在 [!DNL Workfront Fusion]](#create-a-connection-to-jira-server-or-jira-data-center-in-workfront-fusion)中创建与 [!DNL Jira Server] 或 [!DNL Jira Data Center] 的连接

#### 在[!DNL Workfront Fusion]中创建与[!DNL Jira Server]或[!DNL Jira Data Center]的连接

>[!NOTE]
>
>使用[!DNL Jira Server]应用连接到[!DNL Jira Server]或[!DNL Jira Data Center]。

1. 在[!DNL Workfront Fusion]中的任意[!DNL Jira Server]模块中，单击[!UICONTROL connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 在[!UICONTROL Create a connection]面板中，填写以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Connection name]</p> </td> 
      <td> <p>输入连接的名称</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Environment]</p> </td> 
      <td> <p>选择您使用的是生产环境还是非生产环境。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[!UICONTROL Type]</p> </td> 
      <td> <p>选择您使用的是服务帐户还是个人帐户。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Consumer Key]</td> 
      <td>将您复制的使用者密钥粘贴到<a href="#configure-the-client-app-as-a-consumer-in-jira" class="MCXref xref">中的安全位置在[!DNL Jira]</a>中将客户端应用程序配置为使用者</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Private Key]</td> 
      <td>粘贴您在<a href="#generate-public-and-private-keys-for-your-jira-connection" class="MCXref xref">中为[!DNL Jira]连接</a>生成公钥和私钥的<code>[!DNL jira_privatekey.pcks8]</code>文件中的私钥。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Service URL]</td> 
      <td>输入您的[!DNL Jira]实例URL。 示例： <code>yourorganization.atlassian.net</code></td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。

## [!DNL Jira Software]模块及其字段

配置[!DNL Jira Software]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Jira Software]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!UICONTROL Watch for records]

此触发器模块在添加、更新或删除记录时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>选择要用于监视记录的webhook。 </p> <p>要添加新的webhook，请执行以下操作：</p> 
    <ol> 
     <li value="1">单击 <strong>[!UICONTROL Add]</strong></li> 
     <li value="2">输入webhook的名称。</li> 
     <li value="3"> <p>选择要用于webhook的连接。 </p> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </li> 
     <li value="4"> <p>选择要软件监视的记录类型：</p> 
      <ul> 
       <li>[!UICONTROL Comment] </li> 
       <li>[!UICONTROL Issue]</li> 
       <li>[!UICONTROL Project] </li> 
       <li>[!UICONTROL Sprint]</li> 
      </ul> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Add issue to sprint]](#add-issue-to-sprint)
* [[!UICONTROL Create a Record]](#create-a-record)
* [[!UICONTROL Custom API Call]](#custom-api-call)
* [[!UICONTROL Delete a record]](#delete-a-record)
* [[!UICONTROL Download an attachment]](#download-an-attachment)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Update a record]](#update-a-record)

#### [!UICONTROL Add issue to sprint]

此操作模块向冲刺添加一个或多个问题。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sprint ID]</td> 
   <td>输入或映射要添加问题的冲刺(sprint)的Sprint ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Issue ID or Keys]</td> 
   <td>对于要查看体验的每个问题或密钥，单击<b>[!UICONTROL Add item]</b>并输入问题ID或密钥。 在一个模块中最多可输入50个。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Record]

此操作模块在Jira中创建新记录。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择您希望模块创建的记录类型，然后填写特定于此记录类型的其他字段显示在模块中。</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

此操作模块允许您对[!DNL Jira Software] API进行经过身份验证的自定义调用。 使用此模块创建其他[!DNL Jira Software]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对路径<code>&lt;Instance URL>/rest/api/2/ </code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   td&gt; <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png">  </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a record]

此操作模块删除指定的记录。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要模块删除的记录类型。 </p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID or Key]</td> 
   <td>输入或映射要删除的记录的ID或键。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

此操作模块下载特定附件。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射要下载的附件的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

此操作模块从[!DNL Jira Software]中的单个记录读取数据。

您指定记录的ID。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要模块读取的[!DNL Jira]记录的类型。</p> 
    <ul> 
     <li>[!UICONTROL Attachment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL User]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>选择要接收的输出。 输出选项基于“[!UICONTROL Record Type]”字段中选择的记录类型可用。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td> <p>输入或映射您希望模块读取的记录的唯一[!DNL Jira Software] ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

此操作模块更新现有记录，如问题或项目。

您指定记录的ID。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择您希望模块更新的记录类型。 选择记录类型后，该记录类型特有的其他字段将显示在模块中。</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint] </li> 
     <li>[!UICONTROL Transition issue]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID or Key]</td> 
   <td>输入或映射要更新的记录的ID或键，然后填写特定于该记录类型的其他字段显示在模块中。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [[!UICONTROL List records]](#list-records)
* [[!UICONTROL Search for records]](#search-for-records)

#### [!UICONTROL List records]

此搜索模块可检索与您的搜索查询匹配的特定类型的所有项目

您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择您希望模块列出的记录类型。 选择记录类型后，该记录类型特有的其他字段将显示在模块中。</p> 
    <ul> 
     <li>[!UICONTROL Comment]</li> 
     <li>[!UICONTROL Issue]</li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Sprint issue]</li> 
     <li>[!UICONTROL Worklog]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Max Results]</p> </td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中检索的最大记录数。</p> </td> 
  </tr> <!--
   <tr> 
    <td role="rowheader">Offset</td> 
    <td> Enter or map the ID of the first item you want to retrieve details for. This is a way to paginate the records. If you enter the 5000th item as the offset, the module would return items 5000-9999.</td> 
   </tr>
  --> 
 </tbody> 
</table>

#### [!UICONTROL Search for records]

此搜索模块在[!DNL Jira Software]中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Jira Software]帐户连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#connect-jira-software-to-workfront-fusion" class="MCXref xref" data-mc-variable-override="">将[!DNL Jira Software]连接到[!DNL Workfront Fusion]</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>选择要模块搜索的记录类型。 选择记录类型后，该记录类型特有的其他字段将显示在模块中。</p> 
    <ul> 
     <li>[!UICONTROL Issues]</li> 
     <li> <p>[!UICONTROL Issues by JQL (Jira Query Lanuguage)] </p> <p>有关JQL的详细信息，请参阅Atlassian帮助网站上的<a href="https://www.atlassian.com/blog/jira-software/jql-the-most-flexible-way-to-search-jira-14#:~:text=JQLstandsforJiraQuery,projectmanagers%2Candbusinessusers.">JQL</a>。 </p> </li> 
     <li>[!UICONTROL Project]</li> 
     <li>[!UICONTROL Project by issue]</li> 
     <li>[!UICONTROL User]</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
