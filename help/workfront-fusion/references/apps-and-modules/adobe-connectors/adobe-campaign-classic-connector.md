---
title: Adobe Campaign v7/v8模块
description: 使用 [!DNL Adobe Campaign] 模块，您可以基于 [!DNL Adobe Campaign] 帐户中的事件启动 [!DNL Adobe Workfront Fusion] 方案，创建、读取或更新协议和其他记录，使用您设置的条件搜索记录以及上载文档。
author: Becky
feature: Workfront Fusion
exl-id: 9fdff26c-c7c0-4eb8-a36f-4aeaf432b333
source-git-commit: 9bcda2cc1a5f483a8db49eae8e4f3d10f0d39c67
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# [!DNL Adobe Campaign]模块

通过[!DNL Adobe Campaign]模块，您可以基于[!DNL Adobe Campaign v7/v8]帐户中的事件启动[!DNL Adobe Workfront Fusion]方案，创建、读取或更新记录，使用您设置的条件搜索记录，以及执行自定义API调用。

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

必须将Fusion IP地址添加到[!DNL Adobe Campaign]。

* 列入允许列表 列入允许列表有关将IP地址添加到Campaign的说明，请参阅Adobe Campaign文档中的[将IP地址添加到](https://experienceleague.adobe.com/en/docs/control-panel/using/sftp-management/ip-range-allow-listing#adding-ip-addresses-allow-list)。
* 有关要添加到允许列表列入允许列表的IP地址列表，请参阅组织的中的[为Fusion配置IP地址](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md)。

## Adobe Campaign API信息

Adobe Campaign连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.7.22</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Adobe Campaign]连接到[!DNL Adobe Workfront Fusion]

>[!IMPORTANT]
>
>我们强烈建议创建服务器到服务器连接。 Adobe Campaign更新了其API，以仅接受服务器到服务器连接。 如果要连接到Campaign版本8或更高版本，则&#x200B;**必须**&#x200B;创建服务器到服务器连接。
>
>有关Campaign新连接要求的详细信息，请参阅Campaign文档中的[将Campaign技术操作员迁移到Adobe Developer Console](https://experienceleague.adobe.com/docs/campaign/technotes-ac/tn-new/ims-migration.html)。

1. 在任意[!DNL Adobe Campaign]模块中，单击[!UICONTROL Connection]字段旁边的&#x200B;**[!UICONTROL Add]**。
1. 填写以下字段：
   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL Connection type]</td>
          <td>
            <p>选择是要创建基本连接，还是要创建服务器到服务器连接。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Connection name]</td>
          <td>
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Base URL]</td>
          <td>输入用于连接到[!DNL Adobe Campaign]实例的基本URL。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Username]</td>
          <td>如果要创建基本连接，请输入您的Adobe Campaign用户名。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Password]</td>
          <td>如果要创建基本连接，请输入您的Adobe Campaign密码。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client ID]</td>
          <td>如果您正在创建服务器到服务器连接，请输入您的[!DNL Adobe] [!UICONTROL Client ID]。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Client Secret]</td>
          <td>如果您正在创建服务器到服务器连接，请输入您的[!DNL Adobe] [!UICONTROL Client Secret]。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。
        </tr>
     </tbody>
    </table>
1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;以创建连接并返回模块。

## [!DNL Adobe Campaign]模块及其字段

配置[!DNL Adobe Campaign]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Adobe Campaign]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

<!--* [Triggers](#triggers)-->
* [操作](#actions)
* [搜索](#searches)

<!--### Triggers

#### [!UICONTROL Watch records]

This scheduled trigger module starts a scenario when a record changes.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Campaign], see <a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >Create a connection to [!DNL Adobe Campaign]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Select whether you want to watch for new records, updated records, or both.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>Select the resource that you want to watch for.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output]</td> 
   <td>Select the fields that you want to include in the module's output.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>For each custom field that you want to include in output, click <b>[!UICONTROL Add]</b> and enter the name of the custom field.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td>Enter or map the maximum number of records you want the module to return during each scenario execution cycle.</td> 
  </tr> 
 </tbody> 
</table>-->


### 操作

* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Delete a record]](#delete-record)
* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)
* [[!UICONTROL Perform an action]](#perform-an-action)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Subscribe or unsubscribe]](#subscribe-or-unsubscribe)
* [[!UICONTROL Update a record]](#update-record)

#### [!UICONTROL Create a record]

此操作模块在[!DNL Adobe Campaign]中创建新记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与[!DNL Adobe Campaign]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>选择要创建的[!DNL Adobe Campaign]记录的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>选择创建记录时要为其设置值的字段，然后填写这些字段的值。 字段因您选择的记录类型而异。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> 对于要添加到新记录的每个自定义字段，单击<b>[!UICONTROL Add item]</b>并输入或映射字段的名称和值。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Record]

此操作模块从[!DNL Adobe Campaign]中删除单个记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与[!DNL Adobe Campaign]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>选择要删除的资源类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射要删除的资源的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Make a custom API call]

此模块对[!DNL Adobe Campaign] API进行自定义API调用

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与[!DNL Adobe Campaign]</a>的连接。</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Action]</td>
      <td><p>选择您希望API调用执行的操作。</p>
      <p>[!UICONTROL Execute query]</p>
      <p>[!UICONTROL Write]</p>
      <p>[!UICONTROL Get entity if more recent]</p>
      <p>[!UICONTROL Select all]</p>
      <p>[!UICONTROL Push event]</p>
    </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 自动添加[!UICONTROL x-security]令牌标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL XML Body]</td>
   <td> <p>以XML形式为API调用添加正文内容，而不添加会话元素。 </td>     </tr>
  </tbody>
</table>


#### [!UICONTROL Perform an action]

此操作模块对[!DNL Adobe Campaign] API中的对象执行选定的操作。

有关特定操作和字段的信息，请参阅[[!DNL Adobe Campaign] - API文档](https://experienceleague.adobe.com/developer/campaign-api/api/p-14.html)。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与[!DNL Adobe Campaign]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Action]</td> 
   <td><p>选择要对对象执行的操作。</p>
   <ul>
   <li><p><b>[!DNL List]</b></p><p> 有关可用字段，请参阅本文中的<a href="#search" class="MCXref xref" >[!UICONTROL Search]</a>。 </p></li>
     <li><p><b>[!UICONTROL Get]</b></p><p> 有关可用字段，请参阅本文中的<a href="#search" class="MCXref xref" >[!UICONTROL Search]</a>。 </p></li> 
   <li><p><b>[!UICONTROL Create]</b></p><p> 有关可用字段，请参阅本文中的<a href="#create-a-record" class="MCXref xref" >[!UICONTROL Create a record]</a>。 </p></li>
   <li><p><b>[!UICONTROL Update]</b></p><p> 有关可用字段，请参阅本文中的<a href="#update-record" class="MCXref xref" >[!UICONTROL Update a record]</a>。 </p></li>
   <li><p><b>[!UICONTROL Delete]</b></p><p> 有关可用字段，请参阅本文中的<a href="#delete-record" class="MCXref xref" >[!UICONTROL Delete a record]</a>。 </p></li>
   </ul>
   </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

此操作模块从[!DNL Adobe Campaign]读取记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与[!DNL Adobe Campaign]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>选择要读取的[!DNL Adobe Campaign]记录的类型。</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>在映射中输入要读取的记录的ID。</td> 
  </tr> 
 <tr> 
   <td role="rowheader">[!UICONTROL Fields to include in output] </td> 
   <td>选择要包含在模块输出中的字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields to include in output]</td> 
   <td>对于要包含在输出中的每个自定义字段，请单击<b>[!UICONTROL Add]</b>并输入自定义字段的名称。</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Subscribe or unsubscribe]

此操作模块为用户订阅或取消订阅信息服务的用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与[!DNL Adobe Campaign]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subscribe or unsubscribe]</td> 
   <td>选择您要订阅还是取消订阅信息服务。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service name]</td> 
   <td>选择要订阅或取消订阅的服务。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recipient email address] </td> 
   <td>输入或映射要订阅或取消订阅信息服务的用户的电子邮件地址。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update record]

此操作模块更新[!DNL Adobe Campaign]中的单个记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与[!DNL Adobe Campaign]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>选择要创建的[!DNL Adobe Campaign]记录的类型。</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>输入要更新的记录的映射ID。</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Fields] </td> 
   <td>选择要更新其值的字段，然后填写这些字段的值。 字段因您选择的记录类型而异。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> 对于每个要更新的自定义字段，单击<b>[!UICONTROL Add item]</b>并输入或映射该字段的名称和值。 </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL Search]

此搜索模块会根据指定的条件返回记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td>
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与[!DNL Adobe Campaign]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource]</td> 
   <td>选择要创建的[!DNL Adobe Campaign]记录的类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Search criteria]</td> 
   <td>输入您希望搜索使用的字段和值。 字段取决于所选的资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit] </td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
  </tr> 
 </tbody> 
</table>
