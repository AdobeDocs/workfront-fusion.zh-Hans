---
title: Adobe Target模块
description: 在Adobe Workfront Fusion方案中，您可以自动执行使用 [!DNL Adobe Target], as well as connect it to multiple third-party applications and services. [!DNL Adobe Target] 模块的工作流，这些工作流允许您创建、读取、更新或删除记录，列出给定类型的所有记录，根据您指定的条件搜索记录，或对 [!DNL Adobe Target] API执行自定义API调用。
author: Becky
feature: Workfront Fusion
exl-id: f3c1ed7b-b69b-478a-8240-1a2ab89e11e5
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 1%

---

# [!DNL Adobe Target]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Adobe Target]的工作流，并将其连接到多个第三方应用程序和服务。 [!DNL Adobe Target]模块允许您创建、读取、更新或删除记录，列出给定类型的所有记录，根据您指定的条件搜索记录，或对[!DNL Adobe Target] API执行自定义API调用。


如果需要有关创建方案的说明，请参阅[创建方案：项目索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何Adobe Workfront Workflow包和任何Adobe Workfront自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime和Select包，以及额外购买的Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>标准</p><p>工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证</td> 
   <td>
   <p>基于操作：不需要Workfront Fusion许可证</p>
   <p>基于连接器（旧版）：用于工作自动化和集成的Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果贵组织具有不包含Workfront Automation and Integration的Select或Prime Workfront包，则贵组织必须购买Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

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

1. 在任意模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 连接类型]</td>
        <td>选择是要创建服务帐户连接，还是要创建Adobe Target服务器到服务器连接。<p><b>重要信息</b>： 2024年6月3日之后创建的连接需要Adobe Target服务器到服务器连接。 现有的服务帐户连接将继续工作到2025年1月。 您必须在2024年1月之前将服务帐户连接替换为Adobe Target服务器到服务器连接。
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>选择您要连接到生产环境还是非生产环境。
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>选择您是要连接到服务帐户还是个人帐户。
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端ID]</td>
        <td>输入您的[!DNL Adobe]客户端ID。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的[!DNL Adobe]客户端密钥。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 技术帐户ID]</td>
        <td>输入您的[!DNL Adobe]技术帐户ID。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 组织ID]</td>
        <td>输入您的[!DNL Adobe]组织ID。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
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
        <td role="rowheader">[!UICONTROL 私钥]</td>
        <td>
          <p>输入在[!DNL Adobe Developer Console]中创建凭据时生成的私钥。 </p>
          <p>要提取您的私钥或证书，请执行以下操作：</p>
          <ol>
            <li value="1">
              <p>单击<b>[!UICONTROL 提取]</b>。</p>
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
              <p>单击<b>[!UICONTROL 保存]</b>以提取文件并返回到连接设置。</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## [!DNL Adobe Target]模块及其字段

在配置[!DNL Adobe Target]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Adobe Target]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#actions)

* [搜索](#searches)


### 操作

* [[!UICONTROL 创建记录]](#create-a-record)

* [[!UICONTROL 进行自定义API调用]](#make-a-custom-api-call)

* [[!UICONTROL 删除记录]](#delete-a-record)

* [[!UICONTROL 读取记录]](#read-a-record)

* [[!UICONTROL 更新记录]](#update-a-record)


#### [!UICONTROL 创建记录]

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
    <td role="rowheader">[!UICONTROL 记录类型]</td>
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
          <b>[!UICONTROL 选件JSON]</b>
          <p>继续<a href="#offer-fields" class="MCXref xref" >优惠字段</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL 选件内容]</b>
          <p>继续<a href="#offer-fields" class="MCXref xref" >优惠字段</a>。</p>
        </li>
        <li>
        <b>环境</b><p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Environments/operation/createEnvironment">创建环境</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL 受众]</b>
          <p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Audiences/operation/createAudience_1_1">创建受众</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL AB活动]</b>
          <p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_4_1">创建AB活动</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL XT活动]</b>
          <p>继续<a href="#xt-activity-fields" class="MCXref xref" >XT活动字段</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL AP活动]</b>
          <p>有关字段的详细信息，请参阅Adobe Target API文档中的<a href="https://developer.adobe.com/target/administer/admin-api/#tag/Activities/operation/createActivity_2">创建AP活动</a>。</p>
        </li>
        <li>
          <b>[!UICONTROL 响应令牌]</b>
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
      <td role="rowheader">[!UICONTROL 名称]</td>
      <td>输入或映射此活动的名称。 名称不能超过250个字符。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Options]</td>
      <td>
        <p>对于要添加到活动的每个选项，单击<b>[!UICONTROL 添加项]</b>并填写以下字段：</p>
        <ul>
          <li>
            <p><b>[!UICONTROL 选项本地ID]</b>
            </p>
            <p>输入或映射用于跨API请求跟踪选项的字符串。</p>
          </li>
          <li>
            <p><b>[!UICONTROL 名称]</b>
            </p>
            <p>输入或映射选项的名称。 名称不能超过250个字符。</p>
          </li>
          <li>
            <p><b>[!UICONTROL 选件ID]</b>
            </p>
          </li>
          <li>
            <p>选择或映射与选项关联的选件。</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 位置]</td>
      <td>
        <p>对于要添加到活动的每个Mbox，单击<b>[!UICONTROL 添加项]</b>并填写以下字段：</p>
        <ul>
          <li>
            <p>[!UICONTROL 受众ID]</p>
            <p>对于要添加到Mbox的每个受众，单击<b>[!UICONTROL 添加项]</b>并选择受众ID。</p>
          </li>
          <li>
            <p><b>[!UICONTROL 位置本地ID]</b>
            </p>
            <p>输入或映射用于跨API请求跟踪位置的字符串。</p>
          </li>
          <li>
            <p><b>[!UICONTROL 名称]</b>
            </p>
            <p>输入或映射“位置”的名称。 名称不能超过250个字符。</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 体验]</td>
      <td>
        <p>页面上提供内容选件的位置的列表。 位置包含以下内容：
</p>
        <ul>
          <li>
            <p><b>[!UICONTROL 体验本地ID]</b>
            </p>
            <p>输入或映射体验的ID</p>
          </li>
          <li>
            <p><b>[!UICONTROL 名称]</b>
            </p>
            <p>输入或映射体验的名称

</p>
          </li>
          <li>
            <p><b>[!DNL Audience IDs]</b>
            </p>
            <p>对于要查看体验的每个受众，单击<b>[!UICONTROL 添加项]</b>并输入受众ID。

</p>
          </li>
          <li>
            <p><b>[!UICONTROL 访客百分比]</b>
            </p>
            <p>输入或映射分配给体验的访客百分比</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 量度]</td>
      <td> </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 第三方ID]</td>
      <td>输入或映射ID以标识此活动。 您可以选择此ID。 此ID不得与其他活动相同，并且不得超过250个字符。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 开始于]</td>
      <td>以<code>YYYY-MM-DD hh:mm:ss.z</code>格式输入或映射启动活动的日期和时间。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 结束于]</td>
      <td>以<code>YYYY-MM-DD hh:mm:ss.z</code>格式输入或映射结束活动的日期和时间。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 状态]</td>
      <td>
        <p>输入或映射活动的状态。</p>
        <ul>
          <li>
            <p>[!UICONTROL 已批准]</p>
          </li>
          <li>
            <p>[!UICONTROL 已停用]</p>
          </li>
          <li>
            <p>[!UICONTROL 已暂停]</p>
          </li>
          <li>
            <p>[!UICONTROL 已保存] </p>
          </li>
          <li>
            <p>[!UICONTROL 已删除]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 优先级]</td>
      <td>输入一个用于定义活动优先级的数字。 数字越大，优先级越高。 此值必须介于0和999之间。 默认值为 5。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 自动分配流量]</td>
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
      <td role="rowheader">[!UICONTROL 属性ID] </td>
      <td>对于要添加到活动的每个属性，单击<b>[!UICONTROL 添加项]</b>并选择或映射属性的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 报表受众]</td>
      <td>
        <p>对于要添加到活动的每个报表受众，单击[!UICONTROL 添加项目]并输入以下信息：</p>
        <ul>
          <li>
            <p><b>[!UICONTROL 报告受众本地ID]</b>
            </p>
            <p>输入或映射用于跨API请求跟踪报表受众的字符串。</p>
          </li>
          <li>
            <p><b>[!UICONTROL 受众ID]</b>
            </p>
            <p>输入或映射要在报表中使用的区段</p>
          </li>
          <li>
            <p><b>[!UICONTROL 度量本地ID]</b>
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
      <td role="rowheader">[!UICONTROL 名称]</td>
      <td>输入或映射此活动的名称。 名称不能超过250个字符。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 内容]</td>
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

#### [!UICONTROL 进行自定义API调用]

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
      <td role="rowheader">[!UICONTROL [!DNL Target]基本URL]</td>
      <td>输入或映射您的[!DNL Target]基本URL。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 路径]</p>
      </td>
      <td>
        <p>输入相对于{baseURL}的路径/</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 方法]</p>
      </td>
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion会自动添加授权标头和x-api-key标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 查询字符串]  </td>
      <td>
        <p>输入请求查询字符串。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL 删除记录]

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
    <td role="rowheader">[!UICONTROL 记录类型]</td>
    <td>选择要删除的记录类型。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 记录ID]</td>
    <td>输入或映射要删除的记录的ID。</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL 读取记录]

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
    <td role="rowheader">[!UICONTROL 记录类型]</td>
    <td>选择要读取的记录类型。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 记录ID]</td>
    <td>输入或映射要读取的记录的ID。</td>
  </tr>
</tbody>
</table>

#### [!UICONTROL 更新记录]

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
      <td role="rowheader">[!UICONTROL 记录类型]</td>
      <td>
        <p>选择要更新的记录类型。</p>
       </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 字段名称]</td>
      <td>选择要更新的字段。 这些字段显示在下方。
          <p>有关字段的详细信息，请参阅<a href="https://developer.adobe.com/target/administer/admin-api/">Adobe Target API文档</a>。</p>
      </td>
    </tr>
  </tbody>
</table>

### 搜索

* [[!UICONTROL 获取记录]](#get-records)

* [[!UICONTROL 搜索]](#search)


#### [!UICONTROL 获取记录]

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
      <td role="rowheader">[!UICONTROL 记录类型]</td>
      <td>选择要更新的记录类型。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 排序方式]</td>
      <td>对于要作为排序依据的每个字段，单击<b>[!UICONTROL 添加项]</b>并选择该字段以及返回的结果应为升序还是降序。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 开始于]</td>
      <td>
        <p>输入要检索记录的最早日期。 </p>
        <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 结束于]</td>
      <td>
        <p>输入要检索记录的最晚日期。 </p>
        <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 搜索]

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
    <td role="rowheader">[!UICONTROL 记录类型]</td>
    <td>选择要更新的记录类型。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 排序方式]</td>
    <td>对于要作为排序依据的每个字段，单击<b>[!UICONTROL 添加项]</b>并选择该字段以及返回的结果应为升序还是降序。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 搜索条件]</td>
    <td>对于要设置的每个规则，选择字段、运算符和值。 单击<b>[!UICONTROL Add AND rule]</b>以创建其他规则。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 偏移]</td>
    <td>
      <p>输入您希望模块返回的第一个响应的编号。 第一个返回的响应的偏移量为<code>0</code>。 将此字段与[!UICONTROL Maximum number of returned results]字段结合使用可将响应分页。</p>
      <p>例如，要查看响应的第三页，当每个页面有十个响应时，请将[!UICONTROL Offset]设置为20，将[!UICONTROL Maximum number of returned]结果设置为10。</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL 限制]</td>
    <td>
      <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。 将此字段与[!UICONTROL Offset]字段结合使用可将响应分页。</p>
      <p>例如，要查看响应的第三页，当每个页面有十个响应时，请将[!UICONTROL Offset]设置为20，将[!UICONTROL Maximum number of returned]结果设置为10。</p>
    </td>
  </tr>
</tbody>
</table>
