---
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe存储模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，要在Adobe Admin Console中创建和管理项目。
author: Becky
feature: Workfront Fusion
exl-id: 78ee905f-4713-44a4-bffb-c64cdb3665c2
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1386'
ht-degree: 2%

---

# Adobe存储模块

在[!DNL Adobe Workfront Fusion]方案中，您可以在Adobe Admin Console中创建和管理项目。

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

## 创建与Adobe Storage的连接

创建与Adobe Storage的连接需要在Adobe Developer Console以及Fusion中进行一些配置。

### 在Adobe Developer Console中配置项目

您必须在Adobe Developer Console中将API添加到您的项目。

1. 在Adobe Developer Console中打开您的项目。
1. 单击&#x200B;**添加到项目**，然后选择&#x200B;**API**。
1. 从可用API列表中，选择&#x200B;**Adobe Cloud Platform和Collaboration API**。
1. 在选择身份验证类型屏幕上，选择&#x200B;**OAuth服务器到服务器**，然后单击&#x200B;**下一步**。
1. 为凭据添加名称。
1. 单击&#x200B;**下一步**，然后单击&#x200B;**保存配置的API**。
1. 记下提供的凭据，在Workfront Fusion中配置连接时将使用这些凭据。
1. 继续[在Adobe Admin Console中将技术帐户设为管理员](#make-your-technical-account-an-admin-in-the-adobe-admin-console)。

### 在Adobe Admin Console中将您的技术帐户设为管理员

从Adobe Admin Console页面中，选择顶部导航栏中的产品选项卡，然后选择Workfront Fusion

1. 查找并复制组织中技术帐户用户的电子邮件地址。
1. 如果显示了列表，请选择顶部的链接。
1. 这是用户工作的生产实例。
1. 在显示的列表中，选择产品配置文件选项卡，单击Workfront产品配置文件链接的名称。

   此列表包含已分配给您的Workfront生产实例的所有用户。

1. 选择用户列表上方的&#x200B;**管理员**&#x200B;选项卡。
1. 选择&#x200B;**添加管理员**。
1. 在添加产品配置文件管理员框中，输入技术帐户的电子邮件地址，然后选择&#x200B;**保存**。

   技术帐户将被设为管理员。

1. 继续[在Workfront Fusion中创建连接](#create-the-connection-in-workfront-fusion)。

### 在Workfront Fusion中创建连接

要为您的[!DNL Adobe Storage]模块创建连接：

1. 在任意模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL 连接类型]</td>
        <td>选择 <code>Server to server</code>。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
        </tr>
        <td role="rowheader">[!UICONTROL 客户端ID]</td>
        <td>输入您的[!UICONTROL Adobe] [!UICONTROL 客户端ID]。 这可以在[!DNL Adobe Developer Console]中项目的[!UICONTROL 凭据详细信息]部分找到。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。 这可以在[!DNL Adobe Developer Console]中项目的[!UICONTROL 凭据详细信息]部分找到。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL IMS组织ID]</td>
        <td>输入或映射您的Adobe IMS组织ID。 这是一个格式为<code> 123abc@AdobeOrg</code>的字符串，其中@之前的部分是一个十六进制数字。 您可以在Adobe Admin Console或用户管理集成的Adobe.IO控制台中，将此值作为组织的URL路径的一部分找到。</td>
        </tr>
      </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## Adobe存储模块及其字段

在配置Adobe用户管理模块时，Workfront Fusion会显示以下列出的字段。 除此之外，可能还会显示其他Adobe用户管理字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [ESM存储](#esm-stores)
* [邀请](#invitations)
* [其他](#other)

### ESM存储

* [创建ESM存储](#create-an-esm-store)
* [删除ESM存储](#delete-an-esm-store)
* [丢弃ESM存储](#discard-an-esm-store)
* [恢复ESM存储](#restore-an-esm-store)

#### 创建ESM存储

此操作模块可设置一个新的企业存储管理(ESM)存储区，以组织和管理业务关键型资产。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Storage的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >创建与Adobe Storage的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">项目名称</td> 
   <td>输入或映射新项目的名称。</td> 
  </tr> 
 </tbody> 
</table>

#### 删除ESM存储

此操作模块将永久删除现有ESM存储及其所有相关数据。 无法撤消此操作。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Storage的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >创建与Adobe Storage的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">商店ID</td> 
   <td>输入或映射要删除的存储的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 丢弃ESM存储

此操作模块标记EMS存储区以供删除，从而允许在永久删除之前设置宽限期。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Storage的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >创建与Adobe Storage的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">商店ID</td> 
   <td>输入或映射要放弃的存储的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 恢复ESM存储

此操作模块恢复以前删除的ESM存储区并恢复对其数据和配置的访问。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Storage的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >创建与Adobe Storage的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">商店ID</td> 
   <td>输入或映射要还原的存储的ID。</td> 
  </tr> 
 </tbody> 
</table>

### 邀请

#### 邀请用户

此操作模块发送邀请函，授予新用户访问特定ESM存储区的权限，从而启用协作和文件管理。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Storage的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >创建与Adobe Storage的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">电子邮件地址</td> 
   <td>输入或映射要邀请其加入商店的用户的电子邮件地址。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">资产ID</td> 
   <td>输入或映射要邀请用户访问的资源的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">角色</td> 
   <td>选择您希望新受邀用户具有的资产角色。<ul><li>所有者</li><li>编辑者</li><li>查看者</li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">可以评论</td> 
   <td>启用此选项可允许用户对资源进行评论。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">可以共享</td> 
   <td>启用此选项可允许用户与其他用户共享资产。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">需要接受</td> 
   <td>启用此选项以确保用户必须先接受邀请，然后才能协作处理资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">使用装载</td> 
   <td>如果必须为被邀请者创建资源的装入点，则启用此选项。 必须启用“需要接受”选项才能启用此选项。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">通知类型</td> 
   <td>输入或映射要用于通知用户有关邀请的Adobe通知类型。 如果将其留空，则通知类型将基于资产的mimetype。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">模板名称</td> 
   <td>输入或映射要用于邀请电子邮件的模板的Adobe邮政局ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">区域设置</td> 
   <td>以语言代码和国家/地区代码的形式输入用户的区域设置。 <p>示例： <code>en-us</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">外部的</td> 
   <td>如果要使用Adobe邀请服务之外的系统发送通知，请将此选项设置为true。 仅当不需要接受时才支持外部通知。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">资源类型</td> 
   <td>输入或映射资源类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">消息</td> 
   <td>输入或映射要包含在邀请电子邮件中的消息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">目标URL</td> 
   <td>输入或映射被邀请者可用于查看资源的URL。</td> 
  </tr> 
 </tbody> 
</table>

### 其他

#### 进行自定义API调用

此操作模块会向Adobe Storage API发出自定义HTTP请求。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
   <td>有关创建与Adobe Storage的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-storage" class="MCXref xref" >创建与Adobe Storage的连接</a>。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>URL</p>
      </td>
      <td>
        <p>输入相对路径 <code>https://ccprojects.adobe.io/api/v3/.</code></p>
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
