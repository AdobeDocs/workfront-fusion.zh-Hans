---
title: Adobe Target模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动执行使用 [!DNL Adobe Target], as well as connect it to multiple third-party applications and services. [!DNL Adobe Target] 模块的工作流，这些模块允许您创建、读取、更新或删除记录，列出给定类型的所有记录，根据您指定的条件搜索记录，或对 [!DNL Adobe Target] API执行自定义API调用。
author: Becky
feature: Workfront Fusion
exl-id: f3c1ed7b-b69b-478a-8240-1a2ab89e11e5
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1923'
ht-degree: 0%

---

# [!DNL Adobe Target]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Adobe Target]的工作流，并将其连接到多个第三方应用程序和服务。 [!DNL Adobe Target]模块允许您创建、读取、更新或删除记录，列出给定类型的所有记录，根据您指定的条件搜索记录，或对[!DNL Adobe Target] API执行自定义API调用。


如果需要有关创建方案的说明，请参阅[创建方案：项目索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
      <td>
        <p>[!UICONTROL Pro] 或更高</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
      <td>
        <p>[!UICONTROL Plan]， [!UICONTROL Work]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td>
      <td>
   <p>当前许可证要求：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成] </p>
   </td>
    </tr>
    <tr>
      <td role="rowheader">产品</td>
      <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Adobe Workfront]计划，则您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[!UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td>
    </tr>
    </tr>
  </tbody>
</table>


要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## 先决条件

在使用[!DNL Adobe Target]连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的[!DNL Adobe Target]帐户。

## Adobe Target API信息

Adobe Target连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.7.33</td> 
  </tr>
 </tbody> 
 </table>

## 创建与[!DNL Adobe Target]的连接

>[!IMPORTANT]
>
>2024年6月3日之后创建的连接需要Adobe Target服务器到服务器连接。
>
>* 现有的服务帐户连接将继续工作到2025年1月。 您必须在2024年1月之前将服务帐户连接替换为Adobe Target服务器到服务器连接。
>* 您必须是组织的开发人员才能创建Adobe Target服务器到服务器连接。 开发人员角色在Adobe Admin Console中设置。

要为您的[!DNL Adobe Target]模块创建连接：

1. 单击“连接”框旁边的&#x200B;**[!UICONTROL Add]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>选择是要创建服务帐户连接，还是要创建Adobe Target服务器到服务器连接。<p><b>重要信息</b>： 2024年6月3日之后创建的连接需要Adobe Target服务器到服务器连接。 现有的服务帐户连接将继续工作到2025年1月。 您必须在2024年1月之前将服务帐户连接替换为Adobe Target服务器到服务器连接。
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>选择您要连接到生产环境还是非生产环境。
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>选择您是要连接到服务帐户还是个人帐户。
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>输入您的[!DNL Adobe]客户端ID。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>输入您的[!DNL Adobe]客户端密钥。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>输入您的[!DNL Adobe]技术帐户ID。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>输入您的[!DNL Adobe]组织ID。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Tenant]</td>
        <td>
          <p> 要找到您的租户，请登录到[!DNL Adobe Experience Cloud]，打开[!DNL Target]，然后单击[!DNL Target]信息卡。 使用URL子域中所述的租户ID值。</p>
          <p>例如，如果您在登录到[!DNL Adobe Target]时的URL是<code>&lt;https://mycompany.experiencecloud.adobe.com/...></code>，则您的租户ID是“mycompany”。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>输入<code>ent_marketing_sdk</code>       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>输入在[!DNL Adobe Developer Console]中创建凭据时生成的私钥。 </p>
          <p>要提取您的私钥或证书，请执行以下操作：</p>
          <ol>
            <li value="1">
              <p>单击 <b>[!UICONTROL Extract]</b>。</p>
            </li>
            <li value="2">
              <p>选择要提取的文件类型。</p>
            </li>
            <li value="3">
              <p>选择包含私钥或证书的文件。</p>
            </li>
            <li value="4">
              <p>输入文件的密码。</p>
            </li>
            <li value="5">
              <p>单击<b>[!UICONTROL Save]</b>提取文件并返回连接设置。</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;保存连接并返回模块。

## [!DNL Adobe Target]模块及其字段

配置[!DNL Adobe Target]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Adobe Target]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)

* [搜索](#searches)


### 操作

* [[!UICONTROL Create a record]](#create-a-record)

* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)

* [[!UICONTROL Delete a record]](#delete-a-record)

* [[!UICONTROL Read a record]](#read-a-record)

* [[!UICONTROL Update a record]](#update-a-record)


#### [!UICONTROL Create a record]

此操作模块可创建AB或XT活动、选件或受众。

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>有关创建与[!DNL Adobe Target]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-target" class="MCXref xref" >创建与[!DNL Adobe Target]</a>的连接。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>
      <p>选择要创建的记录类型。</p>
      <ul>
        <li>
        <b>属性</b><p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Properties/operation/createProperty">创建属性</a>。</p>
        </li>
        <li>
        <b>优惠推荐</b><p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Offers/operation/createOffer">创建新的推荐选件</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL Offer JSON]</b>
          <p>继续<a href="#offer-fields" class="MCXref xref" >优惠字段</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL Offer Content]</b>
          <p>继续<a href="#offer-fields" class="MCXref xref" >优惠字段</a>。</p>
        </li>
        <li>
        <b>环境</b><p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Environments/operation/createEnvironment">创建环境</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL Audience]</b>
          <p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Audiences/operation/createAudience_1_1">创建受众</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL AB Activity]</b>
          <p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">创建AB活动</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL XT Activity]</b>
          <p>继续<a href="#xt-activity-fields" class="MCXref xref" >XT活动字段</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL AP Activity]</b>
          <p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_2">创建AP活动</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL Response Token]</b>
          <p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Response-tokens/operation/createResponseToken">创建响应令牌</a>。</p>
        </li>
      </ul>
    </td>
  </tr>
</tbody>
</table>

<!--

##### AB Activity fields

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this activity. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>For each option that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the option across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the option. The name must be no more than 250 characters.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>Select or map the Offer associated with the option.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Mboxes]</td>
      <td>
        <p>For each Mbox that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Selectors]</td>
      <td>
        <p>For each selector that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and fill in the following fields:</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>For each audience that you want to add to the Mbox, click <b>[!UICONTROL Add item]</b> and select the Audience ID.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Selector]</b>
            </p>
            <p>Enter or map a string to be used to track the location across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map a name for the Location. The name must be no more than 250 characters.</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>A list of locations on the page where the content offer is served. A location contains the following:
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>Enter or map the ID of the experience</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Enter or map the name of the experience
</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>For each audience that you want to see the experience, click <b>[!UICONTROL Add item]</b> and enter the Audience ID.
</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>Enter or map the percentage of visitors that is allocated to the experience</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td><p>For details on metrics, see <a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">Create AB activity</a> in the Adobe Target API documentation.</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>Enter or map an ID to identify this activity. You can choose this ID. This ID must not be the same as another activity, and can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>Enter or map the date and time to start the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>Enter or map the date and time to end the activity in the format <code>YYYY-MM-DD hh:mm:ss.z</code>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>Enter or map the state of the activity.</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>Enter a number that defines the priority of the activity. Higher numbers have higher priority. This value must be between 0 and 999. The default value is 5.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>Enable this option to auto-allocate traffic. Auto-allocating sends more traffic to the more successful experience.</p>
        <p>Select or map the evaluation criteria by which to judge which experience is more successful.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>Enter or map the workspace that the activity is associated with</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>For each property that you want to add to the activity, click <b>[!UICONTROL Add item]</b> and select or map the property's ID.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>For each reporting audience that you want to add to the activity, click [!UICONTROL Add item] and enter the following information:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the Reporting Audience across API requests.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>Enter or map the Segment to be used in reporting</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>Enter or map a string to be used to track the metric across API requests.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

-->

##### XT活动字段

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>输入或映射此活动的名称。 名称不能超过250个字符。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>对于要添加到活动的每个选项，单击<b>[!UICONTROL Add item]</b>并填写以下字段：</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Option local ID]</b>
            </p>
            <p>输入或映射用于跨API请求跟踪选项的字符串。</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>输入或映射选项的名称。 名称不能超过250个字符。</p>
          </li>
          <li>
            <p><b>[!UICONTROL Offer ID]</b>
            </p>
          </li>
          <li>
            <p>选择或映射与选项关联的选件。</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Locations]</td>
      <td>
        <p>对于要添加到活动的每个Mbox，单击<b>[!UICONTROL Add item]</b>并填写以下字段：</p>
        <ul>
          <li>
            <p>[!UICONTROL Audience IDs]</p>
            <p>对于要添加到Mbox的每个受众，单击<b>[!UICONTROL Add item]</b>并选择受众ID。</p>
          </li>
          <li>
            <p><b>[!UICONTROL Location local ID]</b>
            </p>
            <p>输入或映射用于跨API请求跟踪位置的字符串。</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>输入或映射“位置”的名称。 名称不能超过250个字符。</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Experiences]</td>
      <td>
        <p>页面上提供内容选件的位置的列表。 位置包含以下内容：
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Experience local ID]</b>
            </p>
            <p>输入或映射体验的ID</p>
          </li>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>输入或映射体验的名称

</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>对于要查看体验的每个受众，单击<b>[!UICONTROL Add item]</b>并输入受众ID。

</p>
          </li>
          <li>
            <p><b>[!UICONTROL Visitor Percentage]</b>
            </p>
            <p>输入或映射分配给体验的访客百分比</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Metrics]</td>
      <td> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Third Party ID]</td>
      <td>输入或映射ID以标识此活动。 您可以选择此ID。 此ID不得与其他活动相同，并且不得超过250个字符。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts at]</td>
      <td>以<code>YYYY-MM-DD hh:mm:ss.z</code>格式输入或映射启动活动的日期和时间。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends at]</td>
      <td>以<code>YYYY-MM-DD hh:mm:ss.z</code>格式输入或映射结束活动的日期和时间。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL State]</td>
      <td>
        <p>输入或映射活动的状态。</p>
        <ul>
          <li>
            <p>[!UICONTROL Approved]</p>
          </li>
          <li>
            <p>[!UICONTROL Deactivated]</p>
          </li>
          <li>
            <p>[!UICONTROL Paused]</p>
          </li>
          <li>
            <p>[!UICONTROL Saved] </p>
          </li>
          <li>
            <p>[!UICONTROL Deleted]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Priority]</td>
      <td>输入一个用于定义活动优先级的数字。 数字越大，优先级越高。 此值必须介于0和999之间。 默认值为5。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Auto-allocate traffic]</td>
      <td>
        <p>启用此选项以自动分配流量。 自动分配会向更成功的体验发送更多流量。</p>
        <p>选择或映射用于判断哪些体验更成功的评估标准。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>输入或映射与活动关联的工作区</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Property IDs] </td>
      <td>对于要添加到活动的每个属性，单击<b>[!UICONTROL Add item]</b>并选择或映射属性的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Reporting audiences]</td>
      <td>
        <p>对于要添加到活动的每个报表受众，单击[!UICONTROL Add item]并输入以下信息：</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Reporting Audience local ID]</b>
            </p>
            <p>输入或映射用于跨API请求跟踪报表受众的字符串。</p>
          </li>
          <li>
            <p><b>[!UICONTROL Audience ID]</b>
            </p>
            <p>输入或映射要在报表中使用的区段</p>
          </li>
          <li>
            <p><b>[!UICONTROL Metric local ID]</b>
            </p>
            <p>输入或映射用于跨API请求跟踪量度的字符串。</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### 优惠字段

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>输入或映射此活动的名称。 名称不能超过250个字符。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Content]</td>
      <td>
        <p>输入或映射将向用户显示的选件内容。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>输入或映射与选件关联的工作区的ID。 如果留空，选件将与帐户的默认工作区关联。 此功能仅适用于[!DNL Target] Premium帐户。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>输入或映射修改此选件的日期和时间。</p>
      </td>
    </tr>
  </tbody>
</table>

<!--

##### Audience fields

>[!NOTE]
>
>Audiences created through Workfront Fusion can only be edit in Fusion or through the API. They cannot be edited from within Target.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Enter or map a name for this audience. The name can be no more than 250 characters.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Description]</td>
      <td>
        <p>Enter or map a description of this audience.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Origin]</td>
      <td>
        <p>Select whether this audience's origin is from Target or from the cloud.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Target Rule]</td>
      <td>
        <p>Enable the toggle to make rules AND, that is, all rules must be applied.</p>
        <p>For each rule that you want to apply to the audience, click <b>[!UICONTROL Add item]</b> and enter the JSON of the rule you want to apply. </p>
        <div class="example"><span class="autonumber"><span><b>Example: </b></span></span>
          <p>Example 1:</p>
          <p ><code>&lbrace;</code></p>
                    <p ><code>                "page": "url",</code>
                    </p>
                    <p><code>                "equals":&lbrack;</code>
                    </p>
                    <p ><code>                    "http://www.myhomepage.com/"</code>
                    </p>
                    <p><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;,</code>
                    </p>
                    <p>Example 2</p>
                    <p ><code>            &lbrace;</code>
                    </p>
                    <p><code>                "geo": "region",</code>
                    </p>
                    <p><code>                "matches": &lbrack;</code>
                    </p>
                    <p ><code>                    "california"</code>
                    </p>
                    <p ><code>                &rbrack;</code>
                    </p>
                    <p ><code>            &rbrace;</code>
                    </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Workspace]</td>
      <td>
        <p>Enter or map the ID of the workspace associated with the audience. If left blank, the offer is associated with the default workspace of the account. This functionality applies only to [!DNL Target Premium] accounts.</p>
      </td>
    </tr>
  </tbody>
</table>

-->

#### [!UICONTROL Make a custom API call]

此模块对[!DNL Adobe Target] API进行自定义API调用。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Target]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-target" class="MCXref xref" >创建与[!DNL Adobe Target]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL [!DNL Target] 基本URL</td>
      <td>输入或映射您的[!DNL Target]基本URL。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>输入相对于{baseURL}的路径/</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 自动添加授权标头和x-api-key标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>输入请求查询字符串。</p>
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

#### [!UICONTROL Delete a record]

此操作模块可删除单个AB活动、XT活动、选件或受众。

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>有关创建与[!DNL Adobe Target]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-target" class="MCXref xref" >创建与[!DNL Adobe Target]</a>的连接。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>选择要删除的记录类型。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>输入或映射要删除的记录的ID。</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Read a record]

此操作模块检索单个活动、选件、受众、属性或报表的数据。

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>有关创建与[!DNL Adobe Target]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-target" class="MCXref xref" >创建与[!DNL Adobe Target]</a>的连接。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>选择要读取的记录类型。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record ID]</td>
    <td>输入或映射要读取的记录的ID。</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL Update a record]

此操作模块更新Target中的记录。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Target]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-target" class="MCXref xref" >创建与[!DNL Adobe Target]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>
        <p>选择要更新的记录类型。</p>
       </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Field names]</td>
      <td>选择要更新的字段。 这些字段显示在下方。
          <p>有关字段的详细信息，请参阅<a href="https://developer.adobe.com/target/administer/admin-api/">Adobe Target API文档</a>。</p>
      </td>
    </tr>
  </tbody>
</table>

### 搜索

* [[!UICONTROL Get records]](#get-records)

* [[!UICONTROL Search]](#search)


#### [!UICONTROL Get records]

此搜索模块检索选定类型的记录列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Target]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-target" class="MCXref xref" >创建与[!DNL Adobe Target]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Record type]</td>
      <td>选择要更新的记录类型。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Sort by]</td>
      <td>对于要作为排序依据的每个字段，单击<b>[!UICONTROL Add item]</b>并选择该字段以及返回的结果应为升序还是降序。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Starts At]</td>
      <td>
        <p>输入要检索记录的最早日期。 </p>
        <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Ends At]</td>
      <td>
        <p>输入要检索记录的最晚日期。 </p>
        <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">在[!DNL Adobe Workfront Fusion]</a>中键入强制。</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Search]

此搜索模块会根据您指定的标准搜索活动、选件或受众。

<table style="table-layout:auto"> 
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
    <td>有关创建与[!DNL Adobe Target]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-target" class="MCXref xref" >创建与[!DNL Adobe Target]</a>的连接。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Record type]</td>
    <td>选择要更新的记录类型。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Sort by]</td>
    <td>对于要作为排序依据的每个字段，单击<b>[!UICONTROL Add item]</b>并选择该字段以及返回的结果应为升序还是降序。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Search criteria]</td>
    <td>对于要设置的每个规则，选择字段、运算符和值。 单击<b>[!UICONTROL Add AND rule]</b>以创建其他规则。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Offset]</td>
    <td>
      <p>输入您希望模块返回的第一个响应的编号。 第一个返回的响应的偏移量为<code>0</code>。 将此字段与[!UICONTROL Maximum number of returned results]字段结合使用可将响应分页。</p>
      <p>例如，要查看响应的第三个页面，当每个页面有十个响应时，请将[!UICONTROL Offset]设置为20，将[!UICONTROL Maximum number of returned]结果设置为10。</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]</td>
    <td>
      <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。 将此字段与[!UICONTROL Offset]字段结合使用可将响应分页。</p>
      <p>例如，要查看响应的第三个页面，当每个页面有十个响应时，请将[!UICONTROL Offset]设置为20，将[!UICONTROL Maximum number of returned]结果设置为10。</p>
    </td>
  </tr>
</tbody>
</table>
