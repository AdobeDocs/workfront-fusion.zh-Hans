---
title: Adobe Campaign v7/v8模块
description: 通过 [!DNL Adobe Campaign] 模块，您可以根据 [!DNL Adobe Campaign] 帐户中的事件启动Adobe Workfront Fusion方案，创建、读取或更新协议和其他记录，使用您设置的条件搜索记录以及上载文档。
author: Becky
feature: Workfront Fusion
exl-id: 9fdff26c-c7c0-4eb8-a36f-4aeaf432b333
source-git-commit: aa5b5f1fe805f43b6398e26bf1773d7540ef1634
workflow-type: tm+mt
source-wordcount: '1401'
ht-degree: 35%

---

# [!DNL Adobe Campaign] 模块

通过[!DNL Adobe Campaign]模块，您可以根据[!DNL Adobe Campaign v7/v8]帐户中的事件启动Adobe Workfront Fusion方案，创建、读取或更新记录，使用您设置的条件搜索记录，以及执行自定义API调用。

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
   <td role="rowheader">API 标记</td> 
   <td>v1.7.22</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Adobe Campaign]连接到Adobe Workfront Fusion

>[!IMPORTANT]
>
>我们强烈建议创建服务器到服务器连接。 Adobe Campaign更新了其API，以仅接受服务器到服务器连接。 如果要连接到Campaign版本8或更高版本，则&#x200B;**必须**&#x200B;创建服务器到服务器连接。
>
>有关Campaign新连接要求的详细信息，请参阅Campaign文档中的[将Campaign技术操作员迁移到Adobe Developer Console](https://experienceleague.adobe.com/docs/campaign/technotes-ac/tn-new/ims-migration.html)。

1. 在任意[!DNL Adobe Campaign]模块中，单击&#x200B;**[!UICONTROL 连接]**&#x200B;字段旁边的[!UICONTROL 添加]。
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
            <p>选择是要创建基本连接，还是要创建服务器到服务器连接。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 连接名称]</td>
          <td>
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL基本URL]</td>
          <td>输入用于连接到[!DNL Adobe Campaign]实例的基本URL。</td>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL用户名]</td>
          <td>如果要创建基本连接，请输入您的Adobe Campaign用户名。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 密码]</td>
          <td>如果要创建基本连接，请输入您的Adobe Campaign密码。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端 ID]</td>
          <td>如果要创建服务器到服务器连接，请输入您的[!DNL Adobe] [！UICONTROL客户端ID]。 该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端密钥]</td>
          <td>如果要创建服务器到服务器连接，请输入您的[!DNL Adobe] [！UICONTROL客户端密钥]。 该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。
        </tr>
     </tbody>
    </table>
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;以创建连接并返回模块。

## [!DNL Adobe Campaign] 模块及其字段

在您配置 [!DNL Adobe Campaign] 模块时，Workfront Fusion 会显示以下字段。除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Adobe Campaign] 字段。模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

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

* [[!UICONTROL 创建记录]](#create-a-record)
* [[!UICONTROL 删除记录]](#delete-record)
* [[!UICONTROL 发起自定义 API 调用]](#make-a-custom-api-call)
* [[!UICONTROL 执行操作]](#perform-an-action)
* [[!UICONTROL 读取记录]](#read-a-record)
* [[!UICONTROL 订阅或取消订阅]](#subscribe-or-unsubscribe)
* [[!UICONTROL 更新记录]](#update-record)

#### [!UICONTROL 创建记录]

此操作模块在[!DNL Adobe Campaign]中创建新记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>有关创建与 [!DNL Adobe Campaign] 的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与 [!DNL Adobe Campaign]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资源]</td> 
   <td>选择要创建的[!DNL Adobe Campaign]记录的类型，或选择**自定义资源**并输入资源详细信息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 字段] </td> 
   <td>选择创建记录时要为其设置值的字段，然后填写这些字段的值。 字段因您选择的记录类型而异。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL自定义字段]</td> 
   <td> 对于要添加到新记录的每个自定义字段，单击<b>[！UICONTROL添加项]</b>并输入或映射字段的名称和值。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除记录]

此操作模块从[!DNL Adobe Campaign]中删除单个记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>有关创建与 [!DNL Adobe Campaign] 的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与 [!DNL Adobe Campaign]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资源]</td> 
   <td>选择要删除的资源类型，或选择**自定义资源**并输入资源详细信息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>输入或映射要删除的资源的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 发起自定义 API 调用]

此模块对[!DNL Adobe Campaign] API进行自定义API调用

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
   <td>有关创建与 [!DNL Adobe Campaign] 的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与 [!DNL Adobe Campaign]</a> 的连接。</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 操作]</td>
      <td><p>选择您希望API调用执行的操作。</p>
      <p>[！UICONTROL执行查询]</p>
      <p>[！UICONTROL写入]</p>
      <p>[！UICONTROL Get entity if more recent]</p>
      <p>[！UICONTROL全选]</p>
      <p>[！UICONTROL推送事件]</p>
    </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 标头]</td>
      <td>
        <p>以标准 JSON 对象的形式添加请求标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion会自动添加[！UICONTROL x-security]令牌标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL XML Body]</td>
   <td> <p>以XML形式为API调用添加正文内容，而不添加会话元素。 </td>     </tr>
  </tbody>
</table>


#### [!UICONTROL 执行操作]

此操作模块对[!DNL Adobe Campaign] API中的对象执行选定的操作。

有关特定操作和字段的信息，请参阅[[!DNL Adobe Campaign] - API文档](https://experienceleague.adobe.com/developer/campaign-api/api/p-14.html)。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>有关创建与 [!DNL Adobe Campaign] 的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与 [!DNL Adobe Campaign]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资源]</td> 
   <td>选择要对其执行操作的资源类型，或选择**自定义资源**并输入资源详细信息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 操作]</td> 
   <td><p>选择要对对象执行的操作。</p>
   <ul>
   <li><p><b>[!DNL List]</b></p><p> 有关可用字段，请参阅本文中的<a href="#search" class="MCXref xref" >[！UICONTROL搜索]</a>。 </p></li>
     <li><p><b>[！UICONTROL Get]</b></p><p> 有关可用字段，请参阅本文中的<a href="#search" class="MCXref xref" >[！UICONTROL搜索]</a>。 </p></li> 
   <li><p><b>[！UICONTROL创建]</b></p><p> 有关可用字段，请参阅本文中的<a href="#create-a-record" class="MCXref xref" >[！UICONTROL创建记录]</a>。 </p></li>
   <li><p><b>[！UICONTROL更新]</b></p><p> 有关可用字段，请参阅本文中的<a href="#update-record" class="MCXref xref" >[！UICONTROL更新记录]</a>。 </p></li>
   <li><p><b>[！UICONTROL Delete]</b></p><p> 有关可用字段，请参阅本文中的<a href="#delete-record" class="MCXref xref" >[！UICONTROL删除记录]</a>。 </p></li>
   </ul>
   </td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 读取记录]

此操作模块从[!DNL Adobe Campaign]读取记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>有关创建与 [!DNL Adobe Campaign] 的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与 [!DNL Adobe Campaign]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资源]</td> 
   <td>选择要读取的[!DNL Adobe Campaign]记录的类型，或选择**自定义资源**并输入资源详细信息。</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>在映射中输入要读取的记录的ID。</td> 
  </tr> 
 <tr> 
   <td role="rowheader">要包含在输出中的[！UICONTROL字段] </td> 
   <td>选择要包含在模块输出中的字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL要包含在输出中的自定义字段]</td> 
   <td>对于要包含在输出中的每个自定义字段，请单击<b>[！UICONTROL添加]</b>并输入自定义字段的名称。</td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL 订阅或取消订阅]

此操作模块为用户订阅或取消订阅信息服务的用户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>有关创建与 [!DNL Adobe Campaign] 的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与 [!DNL Adobe Campaign]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL订阅或取消订阅]</td> 
   <td>选择您要订阅还是取消订阅信息服务。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL服务名称]</td> 
   <td>选择要订阅或取消订阅的服务。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL收件人电子邮件地址] </td> 
   <td>输入或映射要订阅或取消订阅信息服务的用户的电子邮件地址。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新记录]

此操作模块更新[!DNL Adobe Campaign]中的单个记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>有关创建与 [!DNL Adobe Campaign] 的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与 [!DNL Adobe Campaign]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资源]</td> 
   <td>选择要更新的[!DNL Adobe Campaign]记录的类型，或选择**自定义资源**并输入资源详细信息。</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL ID] </td> 
   <td>输入要更新的记录的映射ID。</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL 字段] </td> 
   <td>选择要更新其值的字段，然后填写这些字段的值。 字段因您选择的记录类型而异。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL自定义字段]</td> 
   <td> 对于每个要更新的自定义字段，请单击<b>[！UICONTROL添加项]</b>并输入或映射该字段的名称和值。 </td> 
  </tr> 
 </tbody> 
</table>

### 搜索

#### [!UICONTROL 搜索]

此搜索模块会根据指定的条件返回记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td>
   <td>有关创建与 [!DNL Adobe Campaign] 的连接的说明，请参阅本文中的<a href="#connect-adobe-campaign-to-adobe-workfront-fusion" class="MCXref xref" >创建与 [!DNL Adobe Campaign]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL资源]</td> 
   <td>选择要返回的[!DNL Adobe Campaign]记录的类型，或选择**自定义资源**并输入资源详细信息。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 搜索条件]</td> 
   <td>输入您希望搜索使用的字段和值。 字段取决于所选的资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td>输入或映射每次场景执行周期中该模块允许返回的最大记录数量。</td> 
  </tr> 
 </tbody> 
</table>
