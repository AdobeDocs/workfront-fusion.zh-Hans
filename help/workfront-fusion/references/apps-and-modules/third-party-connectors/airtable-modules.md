---
title: 可飞行模块
description: 除了Adobe Workfront许可证之外，Adobe Workfront Fusion还需要Adobe Workfront Fusion许可证。
author: Becky
feature: Workfront Fusion
exl-id: 3b445b50-5812-4ded-9788-f467991e0b52
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1890'
ht-degree: 2%

---

# 可飞行模块


使用Adobe Workfront Fusion的[!DNL Airtable]连接器，您可以基于[!DNL Airtable]帐户中的事件启动方案，创建、上载和更新记录、搜索记录以及对Airtable API进行自定义API调用。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront计划*</td>
  <td> <p>[!UICONTROL Pro]或更高版本</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证*</td>
   <td> <p>[!UICONTROL 计划]，[!UICONTROL 工作]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td> <p>[!UICONTROL Workfront Fusion for Work Automation and Integration] </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>您的组织必须购买Adobe Workfront Fusion和Adobe Workfront，才能使用本文中所述的功能。</td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有的计划、许可证类型或访问权限，请联系您的Workfront管理员。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## 先决条件

您必须拥有Airtable帐户才能使用本文中的功能。

<!--
<p>For more information, see the tutorial .</p>
-->

## Airtable API信息

“可通风”连接器使用下列内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td>https://api.airtable.com/v0</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v3.3.28</td> 
  </tr>
 </tbody> 
 </table>

## 将Airtable连接到Workfront Fusion {#connect-airtable-to-workfront-fusion}

<!--

1. Log in to your Airtable account.
1. Open your account overview and generate the API key.
-->
1. 打开Workfront Fusion，然后打开所需模块的&#x200B;**创建连接**&#x200B;对话框。
1. 输入连接的名称。
1. （可选）单击“显示高级设置”，然后输入您的Airtable客户端ID和客户端密钥。
1. 单击&#x200B;**继续**&#x200B;按钮以创建连接并返回模块。

## 可飞行模块及其领域

### 记录

* [创建记录](#create-a-record)
* [删除记录](#delete-a-record)
* [获取记录](#get-a-record)
* [搜索记录](#search-records)
* [更新记录](#update-a-record)
* [更新插入记录](#upsert-a-record)
* [观看记录](#watch-records)
* [Watch响应](#watch-responses)
* [进行API调用](#make-an-api-call)

#### 创建记录 {#create-a-record}

此操作模块创建新记录。

您可以指定要在记录中存储的数据以及存储位置。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>连接 </td> 
   <td> <p>有关将Airtable帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">将Airtable连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>库 </td> 
   <td> <p>选择新记录将属于的基底。</p> </td> 
  </tr> 
  <tr> 
   <td>表 </td> 
   <td> <p>选择新记录所属的表。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>记录</p> </td> 
   <td> <p>输入新记录的值。 可用字段基于您选择的表。</p> <!--<p>For more information on field types, search for "Supported field types" in the Airtable documentation.</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>Multiple lines of text, which may contain "mention tokens", for example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong> : Add the attachment. Airtable will download the file from the provided <code>url</code> and keep its own copy of it. If the File name field is left empty, Airtable generates the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05 (ISO 8601 formatted date)</li> 
     <li>Phone number:</li> 
     <li><strong>Emails</strong>: A valid email address.</li> 
     <li><strong>URL</strong>: A valid URL (for example, airtable.com or https://airtable.com/universe).</li> 
     <li><strong>Number</strong>: Enter a number.</li> 
     <li><strong>Currency</strong>: Currency value.</li> 
     <li><strong>Percent</strong>: A percentage value. Must be higher than or equal to 0.</li> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation. </li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs will be reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>智能链接</td> 
   <td> <p>启用此选项可输入名称，而不是将记录ID输入到链接到另一个表的字段。 如果没有匹配项，则会在链接表中自动创建记录。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 删除记录 {#delete-a-record}

此操作模块删除特定记录。

您可以指定记录的ID和位置。

该模块返回记录ID和任何关联字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>连接 </td> 
   <td> <p>有关将Airtable帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">将Airtable连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>库 </td> 
   <td> <p>选择包含要删除的记录的基础。</p> </td> 
  </tr> 
  <tr> 
   <td>表 </td> 
   <td> <p>选择包含要删除的记录的表。</p> </td> 
  </tr> 
  <tr> 
   <td>记录Id</td> 
   <td> <p>输入或映射您希望模块删除的记录的唯一可通风性ID。 例如，您可以使用搜索记录模块检索ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取记录 {#get-a-record}

此操作模块可检索记录详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>连接 </td> 
   <td> <p>有关将Airtable帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">将Airtable连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>库 </td> 
   <td> <p>选择包含带有要检索的记录的表的基础。</p> </td> 
  </tr> 
  <tr> 
   <td>表</td> 
   <td> <p> 选择包含要检索其详细信息的记录的表。</p> </td> 
  </tr> 
  <tr> 
   <td>记录Id</td> 
   <td> <p> 输入或映射要检索其详细信息的记录ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 搜索记录 {#search-records}

此搜索模块在Airtable中查找与您指定的搜索查询匹配的对象中的记录。

您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>连接 </td> 
   <td> <p>有关将Airtable帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">将Airtable连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>库 </td> 
   <td> <p>选择要搜索记录的基础。</p> </td> 
  </tr> 
  <tr> 
   <td>表 </td> 
   <td> <p>选择要搜索记录的表。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>公式</p> </td> 
   <td> <p>用于筛选记录的公式。 将针对每个记录计算公式，如果结果不是<code>0</code>、<code>false</code>、<code>""</code>、<code>NaN</code>、<code>[]</code>或<code>#Error!</code>，则响应中将包含该记录。</p> <p>如果与<code>view</code>组合，则仅返回该视图中满足公式的记录。</p> <p>例如，要仅包括Name不为空的记录，请传入：<code> NOT({Name} = '')</code></p> <p>要了解更多信息，请在Airtable支持文档中搜索有关公式字段引用的信息。</p> </td> 
  </tr> 
  <tr> 
   <td>排序 </td> 
   <td> <p>选择排序方向和要作为结果排序依据的字段。</p> </td> 
  </tr> 
  <tr> 
   <td>视图 </td> 
   <td> <p>选择要搜索记录的视图。</p> </td> 
  </tr> 
  <tr> 
   <td>限制</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 更新记录 {#update-a-record}

此操作模块更新特定记录。

您可以指定记录的ID以及要包含的新数据。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>连接 </td> 
   <td> <p>有关将Airtable帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">将Airtable连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>库 </td> 
   <td> <p>选择包含要更新的记录的基础。</p> </td> 
  </tr> 
  <tr> 
   <td>表 </td> 
   <td> <p>选择包含要更新的记录的表。</p> </td> 
  </tr> 
  <tr> 
   <td>记录Id </td> 
   <td> <p>输入或映射您希望模块更新的记录的唯一Airtable ID。 例如，您可以使用搜索记录模块检索ID。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>记录</p> </td> 
   <td> <p>输入新记录的值。 可用字段取决于您选择的表。</p> <!--<p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>智能链接</td> 
   <td> <p>输入链接到其他表的字段的名称，而不是记录ID。 如果没有匹配项，则会在链接表中自动创建记录。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 更新插入记录

此操作模块更新或插入特定记录。

您可以指定记录的ID以及要包含的新数据。

该模块会返回与记录关联的任何标准字段，以及连接访问的任何自定义字段和值。 您可以在场景的后续模块中映射此信息。

配置此模块时，会显示以下字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>连接 </td> 
   <td> <p>有关将Airtable帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">将Airtable连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>库 </td> 
   <td> <p>选择包含要更新的记录的基础。</p> </td> 
  </tr> 
  <tr> 
   <td>表 </td> 
   <td> <p>选择包含要更新的记录的表。</p> </td> 
  </tr> 
  <tr> 
   <td>记录Id </td> 
   <td> <p>如果要更新记录，请输入或映射要模块更新的记录的唯一Airtable ID。 例如，您可以使用搜索记录模块检索ID。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>记录</p> </td> 
   <td> <p>输入新记录的值。 可用字段取决于您选择的表。</p> <!-- <p>In order to delete the content of the field, use the erase function. </p>  <p>Field types (via airtable.com/api):</p> 
    <ul> 
     <li> <p><strong>Text</strong>: string</p> <p>A single line of text.</p> </li> 
     <li> <p><strong>Long text</strong>: string</p> <p>The string can contain multiple lines of text with "mention tokens." For example:</p><pre>&lt;airtable:mention id="menE1i9oBaGX3DseR"&gt;@Alex&lt;/airtable:mention&gt;</pre> </li> 
     <li><strong>Attachment</strong>: Add the attachment. Airtable will download the file from the provided url and keep its own copy of it. If the File name field is left empty, Airtable will generate the name automatically.</li> 
     <li><strong>Checkbox</strong>: Select one of the options.</li> 
     <li><strong>Multiple select</strong>: Select multiple options in the checklist.</li> 
     <li><strong>Single select</strong>: Select one option from the drop-down menu.</li> 
     <li><strong>Collaborator</strong>: Enter the email that uniquely identifies a user in Airtable who this base is shared with.</li> 
     <li><strong>Date</strong>: UTC date, for example, 2019-09-05. (ISO 8601 formatted date)</li> 
     <li><strong>Phone number</strong>: A telephone number, for example, (415) 555-9876.</li> 
     <li><strong>Email</strong>valid email address.</li> 
     <li><strong>URL</strong>: lid URL such as airtable.com or https://airtable.coiverse.</li> 
     <li><strong>Number</strongnter a number.</li> 
     <li><strong>Currency</stro Currency value.</li> 
     <li><strong>Percent</stronA percentage value; must be equal to or more than 0i> 
     <li><strong>Duration</strong>: Enter the duration time. If you need help, see the information about the duration field type in the Airtable support documentation.</li> 
     <li><strong>Rating</strong>: Enter the number. For example, "3 stars" is 3. A rating cannot be 0.</li> 
     <li><strong>Link</strong>: Enter the linked records IDs from the table. The order of record IDs is reversed compared to what you see in the app.</li> 
     <li><strong>Rollup</strong>: Computed value: COUNT(values)</li> 
     <li><strong>Lookup</strong>: Array of long text fields</li> 
     <li><strong>Autonumber</strong>: Automatically incremented unique counter for each record.</li> 
     <li> <p><strong>Barcode</strong>: The barcode object may contain the following two properties, both of which are optional.</p> <p>Barcode data (text)</p> <p>Barcode symbology, for example, "upce" or "code39" (type)</p> </li> 
    </ul> --></td> 
  </tr> 
  <tr> 
   <td>智能链接</td> 
   <td> <p>输入链接到其他表的字段的名称，而不是记录ID。 如果没有匹配项，则会在链接表中自动创建记录。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 观看记录 {#watch-records}

在指定表中创建或更新记录时，此触发器模块会启动一个方案。

>[!NOTE]
>
>要使用此模块，必须在表中创建“创建时间”字段或“上次修改时间”字段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>连接 </td> 
   <td> <p>有关将Airtable帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">将Airtable连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>库 </td> 
   <td> <p>选择要监视新记录的基础。</p> </td> 
  </tr> 
  <tr> 
   <td>表 </td> 
   <td> <p>选择要监视新记录的表。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>触发器配置</p> </td> 
   <td> <p>触发器字段</p> <p>用于对记录进行排序的<code>Created Time</code>或<code>Last Modified Time</code>字段。 如果您的架构中没有<code>Created Time</code>或<code>Last Modified Time</code>字段，则需要创建一个。 </p> <p>标签字段</p> <p>用作记录标签的字段，例如，在“选择开始位置”对话框中。</p> </td> 
  </tr> 
  <tr> 
   <td>限制</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中监视的最大记录数。</p> </td> 
  </tr> 
  <tr> 
   <td>视图</td> 
   <td> <p>选择要使用的视图。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>公式</p> </td> 
   <td> <p>用于筛选记录的公式。 将针对每个记录计算公式，如果结果不是<code>0</code>、<code>false</code>、<code>""</code>、<code>NaN</code>、<code>[]</code>或<code>#Error!</code>，则响应中将包含该记录。</p> <p>如果与<code>view</code>组合，则仅返回该视图中满足公式的记录。</p> <p>例如，要仅包括Name不为空的记录，请传入：<code> NOT({Name} = '')</code></p> <p>要了解更多信息，请参阅Airtable支持文档中有关公式字段引用的信息。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### Watch响应

此触发器模块在提交表单时启动方案。

>[!NOTE]
>
>此功能仅适用于付费的Airtable Pro Plan。

webhook URL需要在Workfront Fusion中生成，然后添加到Airtable中的表单配置中。

1. 将Watch New Responses模块添加到您的Workfront Fusion方案。
1. 生成并复制webhook URL。

   <!--For instructions, see [ (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->

1. 登录到您的Airtable帐户。
1. 打开要用于表单的“基础”和表，并创建“表单”视图。
1. 根据需要设置表单，向下滚动表单，然后启用“提交表单后重定向到URL”选项。
1. 将步骤2中生成的Webhook URL输入到显示的对话框中，并在webhook URL之后添加？record_id={record_id}以将记录ID包含在模块输出中，然后单击“保存”。 例如，生成的URL将如下所示：
1. 返回到Workfront Fusion场景并运行观察响应模块，以仅从Airtable加载字段并能够将这些字段映射到其他模块。
1. 在Airtable中提交表单，其中启用了提交表单后重定向到URL选项并添加了Webhook URL（上述步骤6）。

   触发Watch Responses模块并加载所需数据。

1. 在Airtable > Watch Responses模块之后添加Airtable > Get a Record模块，并将record_id映射到记录ID字段。

现在，每次提交表单时，都会触发Workfront Fusion场景中的“监视响应”模块，并且“获取记录”模块会返回提交的表单详细信息。

#### 进行API调用

#### 自定义API调用

此操作模块允许您对[!DNL Airtable] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Airtable]模块无法实现的数据流自动化。

该操作基于您指定的图元类型（Allocadia对象类型）。

配置此模块时，会显示以下字段。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>连接</p> </td> 
   <td> <p>有关将Airtable帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-airtable-to-workfront-fusion" class="MCXref xref">将Airtable连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>输入相对于<code>https://api.airtable.com/</code>的路径。 示例：<code>v0/{base}/{table}</code> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">方法</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">标头</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">查询字符串</td> 
   <td> <p>以键和值的形式添加API调用查询</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">正文</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>
