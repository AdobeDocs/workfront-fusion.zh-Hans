---
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: scenarios
title: 使用模板连接Adobe Workfront Fusion和Jira
description: 使用这些模板可自动执行Adobe Workfront Fusion和Jira之间的工作流。
author: Becky
feature: Workfront Fusion
hide: true
hidefromtoc: true
source-git-commit: c3d1abb898eec6fc84dc1de0fb7799d13d9e3571
workflow-type: tm+mt
source-wordcount: '4171'
ht-degree: 3%

---

# 使用模板连接Adobe Workfront Fusion和Jira

Adobe Workfront Fusion提供了可自动执行Fusion和Jira之间常用工作流的模板。

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
   <td role="rowheader">产品</td> 
   <td>
   <p>Workfront：如果贵组织具有不包含Workfront Automation and Integration的Select或Prime Workfront包，则必须购买Adobe Workfront Fusion。</p><p>Jira：您必须拥有Jira Cloud的许可证</p>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">访问级别配置</td> 
   <td> <p>Workfront：创建用户、自定义表单和自定义字段的权限。</p> <p>Jira：创建用户和自定义字段以及修改屏幕和Webhook的权限。</td> 
  </tr> 
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++

## 先决条件

### Workfront

* 您必须在Adobe Developer Console上拥有技术帐户。

  有关信息和说明，请参阅Adobe文档中的[技术帐户设置](https://developer.adobe.com/cloud-storage/guides/getting-started/technical-account-setup)。
* 您必须在Adobe Admin Console产品配置文件区域将系统管理员权限应用到技术帐户。

  有关信息和说明，请参阅[使用Adobe Admin Console在Workfront中创建系统管理员](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console#create-system-administrators-in-workfront-with-the-adobe-admin-console)

### Jira

如果您使用Jira的OAuth2授权（推荐），则必须在[https://developer.atlassian.com/console](https://developer.atlassian.com/console)处设置OAuth2应用程序。 有关信息和说明，请参阅Jira模块文章中的[创建与Jira](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#create-an-oauth2-connection-to-jira)的OAuth2连接。

<!--

When configuring this application, you will need the following scopes:

* `read:jira-work` 
* `read:jira-user`
* `write:jira-work`

-->

## 假设

这些模块采用以下形式：

* Workfront是整个营销活动项目的真实来源
* Jira正被技术团队使用，完成在Workfront启动的项目的一部分。
* 并非所有Jira用户都可以访问Workfront，反之亦然。
* Workfront和Jira托管在云中。

## 数据模型（字段映射）


| Workfront | Jira | 方向 | 注释 |
|---|---|---|---|
| 对象ID | WF ID * | WF → Jira | 在Jira问题创建时 |
| Jira键* | 问题密钥 | Jira → WF | 在Jira问题创建时 |
| Jira URL * | - | Jira → WF | WF中的用户可点击链接到Jira |
| - | WF链接* | WF → Jira | Jira中的用户可点击链接到WF |
| 名称 | 摘要 | WF → Jira |  |
| 描述 | 描述 | WF → Jira |  |
| 状态 | WF状态 | WF → Jira | WF状态 |
| Jira状态* | 状态 | Jira → WF | Jira状态 |
| 规划完成日期 | 到期日期 | WF → Jira | 规划完成日期 |
| 注释 | 评论 | WF ↔ Jira | 双向复制 |
| 文档 | 附件 | WF → Jira | 作为问题创建的附件和创建后新文档的注释。 |

\*这些字段配置为此集成设置的一部分。 有关说明，请参阅[在Workfront、Jira和Workfront Fusion中配置先决条件](/help/workfront-fusion/create-and-manage-templates/use-jira-scenario-templates.md#configure-prerequisites-in-workfront-jira-and-workfront-fusion)。

## 在Workfront、Jira和Workfront Fusion中配置先决条件

要使用Jira集成模板，您必须执行以下配置：

* [配置Jira](#configure-jira)
* [配置Workfront](#configure-workfront)
* [在Workfront Fusion中配置连接](#configure-connections-in-workfront-fusion)

### 配置Jira

要使用这些模块，必须在Jira中创建以下内容：

* 系统集成用户
* 三个特定的自定义字段

#### 在Jira中创建系统集成用户

1. 在Jira中，创建一个名为系统集成用户的特定用户。 此用户应仅由Workfront Fusion使用，而不应代表人类用户。 Workfront Fusion连接将使用此用户的凭据。

#### 在Jira中创建必要的自定义字段

此集成要求它连接到的Jira帐户中包含三个特定字段。 如果没有这些字段，集成将失败

1. 在Jira中，转到&#x200B;**设置**（齿轮图标）并选择&#x200B;**工作项**。
1. 在左侧导航中，选择&#x200B;**自定义字段**。
1. 在屏幕的右上角，单击&#x200B;**创建自定义字段。**
1. 创建以下字段：

   | 字段名称 | 字段类型 |
   |---|---|
   | WF ID | 文本字段（单行） |
   | WF状态 | 文本字段（单行） |
   | WF链接 | URL字段 |

   有关在Jira中创建链接的信息，请参阅有关创建字段的Jira文档。
1. 将新创建的字段添加到与您的Jira项目关联的屏幕。

   有关Jira屏幕的信息，请参阅有关设置工作项屏幕的Jira文档。


### 配置Workfront

要使用这些模块，必须在Workfront中创建以下内容：

* 系统集成用户
* 特定自定义表单

#### 在Workfront中创建系统集成用户

1. 在Workfront中，创建系统集成用户。 此用户仅由Workfront Fusion使用，不代表人类用户。 分配给此用户的任务将触发将Workfront与Jira同步的方案。

   有关说明，请参阅Workfront文档中的[添加用户](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/add-users)。

#### 在Workfront中创建自定义表单

1. 在Workfront中，开始创建自定义表单。

   有关说明，请参阅Workfront文档中的[创建自定义表单](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/design-a-form/design-a-form)。
1. 将表单命名为“**JIRA字段**”。
1. 在自定义表单中包含以下字段：

| 字段名称 | 字段类型 |
|---|---|
| Jira键 | 单行文本字段 |
| Jira URL | 单行文本字段 |
| Jira状态 | 单行文本字段 |

1. 添加您要在Jira和Workfront之间映射的任何其他字段。
1. 保存自定义表单。

>[!NOTE]
>
>我们建议限制其他用户编辑此表单。 为此，您可以确保添加到自定义表单的任何用户仅具有查看权限。
>
>有关说明，请参阅Workfront文档中的[共享自定义表单](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/customize/custom-forms/manage-custom-forms/share-access-to-a-custom-form)。

### 在Workfront Fusion中配置连接

在创建连接之前，您必须在Jira和Workfront中创建系统集成用户。

创建这些连接时，请确保使用已创建的系统集成用户的凭据。

如果需要，您可以在配置模板时创建这些连接。

* 有关创建与Workfront的连接的说明，请参阅Workfront模块一文中的[将Workfront连接到Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/workfront-modules.md#connect-workfront-to-workfront-fusion)。
* 有关创建与Jira连接的说明，请参阅“Jira软件模块”一文中的[将Jira连接到Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion)。


## 场景

Jira的八个现成可用模板可帮助复制通用工作流并加快实施。 模板是完全可自定义的，可满足特定的业务需求，并且可以随着需求的发展而扩展。

您无需实施所有方案。 最低限度的实施将需要情景1，这将从Workfront的一项任务创建一个与JIRA问题的单向集成。  您可以添加其他场景，以在Workfront和JIRA之间增加稳健性和更双向的交互连接。  您还可以创建其他方案以处理项目到大型集成或JIRA问题到Workfront问题或任务等情况。

这些模板或这些模板的扩展的任何使用都被视为自定义配置，我们建议使用Adobe Professional Services或Adobe合作伙伴提供支持和实施。

* **[Workfront到Jira：从Workfront任务或问题分配创建JIRA问题](#scenario-1-workfront-to-jira-create-jira-issue-from-workfront-task-or-issue-assignment)**
* [JIRA到Workfront： JIRA到Workfront：将问题和评论的更新从Jira发送回Workfront](#scenario-2-jira-to-workfront-send-updates-on-issues-and-comments-back-to-workfront-from-jira)
* [Workfront到Jira：将Workfront任务更改为JIRA问题](#scenario-3-workfront-to-jira-changes-to-workfront-task-to-jira-issue)
* [Workfront到Jira：将Workfront问题更改为JIRA问题](#scenario-4-workfront-to-jira-changes-to-workfront-issue-to-jira-issue)
* [Workfront到Jira：在有关Workfront任务或问题的新注释时在JIRA中创建评论](#scenario-5-workfront-to-jira-create-comment-in-jira-when-new-note-on-workfront-task-or-issue)
* [Workfront到Jira：在JIRA中创建Workfront任务或问题已删除注释的评论](#scenario-6-workfront-to-jira-create-comment-in-jira-on-deleted-note-on-workfront-task-or-issue)
* [从Workfront到Jira：新建有关Workfront任务或问题的文档时，在JIRA中创建评论](#scenario-7-workfront-to-jira-create-comment-in-jira-when-new-document-on-workfront-task-or-issue)
* [从Workfront到Jira：在JIRA中创建Workfront任务或问题上已删除文档的评论](#scenario-8-workfront-to-jira-create-comment-in-jira-on-deleted-document-on-workfront-task-or-issue)

### 常规参数

配置这些模板时，请使用以下常规参数：

* **JiraBaseURL**： Jira实例的基本URL。 示例：`https://myjira.atlassian.net/`
* **wfBaseURL**： Workfront实例的基本URL。  通常： `https://<domain>.my.workfront.com`，其中`<domain>`是您的特定Workfront域名。
* **defaultJIRAReporterID**： JIRA中发生问题的用户的ID。 （示例： `557058:5aedf933-2312-40bc-b328-0c21314167f0`）
您可以通过执行以下操作之一来获取此ID：
   * 在JIRA中单击用户的个人资料，然后查看浏览器中的URL。
（示例`https://myjira.atlassian.net/jira/people/<JiraUserID>`）
   * 在您的JIRA实例上运行以下API调用，以获取JIRA中特定帐户的ID：
     `GET /rest/api/3/user/search?query=email@example.com`


### 情景1：Workfront到Jira：从Workfront任务或问题分配创建JIRA问题

当将Workfront任务或问题分配给系统集成用户时，此方案会创建Jira问题。 该方案填写“摘要”、“描述”、“到期日”、“WF状态”和“WF ID”字段。 创建问题后，此方案还会上传与Workfront中的原始任务或问题相关的附件列表和注释历史记录。

如果分配了Workfront任务，则Jira中的问题为任务。 如果分配了Workfront问题，则Jira问题为错误。

+++**展开以查看有关将方案1:Workfront配置为Jira的说明：从Workfront任务或问题分配创建JIRA问题**

#### 配置触发器模块

1. 单击左侧导航面板中的&#x200B;**模板**&#x200B;选项卡![模板图标](assets/templates-icon.png)。
1. 使用屏幕左上角附近的搜索栏搜索模板。 您可以按模板名称或包含的应用程序进行搜索。
1. 单击&#x200B;**Workfront to Jira：从Workfront任务或问题分配**&#x200B;模板创建JIRA问题。

   此时将打开模板视图，显示信息以及数据流动画。
1. 在第一个模块中，开始添加webhook。
1. 选择您在[在Workfront Fusion](#configure-connections-in-workfront-fusion)中配置连接中创建的Workfront连接。
1. 在&#x200B;**记录类型**&#x200B;字段中，选择`Assignment`。
1. 在&#x200B;**状态**&#x200B;字段中，选择`New state`。
1. 使用&#x200B;**And**&#x200B;选项通过以下操作配置筛选器：

   | 字段 | 操作员 | 值 |
   |---|---|---|
   | assignedToID | 等于 | (输入系统集成用户的Workfront ID) |
   | 任务编号 | 已存在 |  |
   | projectID | 等于 | （输入希望webhook监视的一个或多个项目的ID） |

1. 启用&#x200B;**排除此连接所做的更新**&#x200B;选项。
1. 在&#x200B;**记录来源**&#x200B;字段中，选择“仅新建记录”。
1. 单击&#x200B;**保存**&#x200B;以保存webhook，然后单击&#x200B;**确定**&#x200B;以保存触发器模块。
1. 继续[将模板模块连接到Workfront和Jira](#connect-template-modules-to-workfront-and-jira)

#### 将模板模块连接到Workfront和Jira

1. 在&#x200B;**每个** Workfront模块的连接字段中，选择您在[在Workfront Fusion中配置连接](#configure-connections-in-workfront-fusion)中创建的Workfront连接，然后单击&#x200B;**确定**&#x200B;保存与该模块的连接。
1. 在&#x200B;**每个** Jira模块的“连接”字段中，选择您在[在Workfront Fusion中配置连接](#configure-connections-in-workfront-fusion)中创建的Workfront连接，然后单击&#x200B;**确定**&#x200B;保存与该模块的连接。
1. 继续[更新常规参数模块](#update-the-general-parameters-module)。

#### 更新常规参数模块

1. 在模板的第二个模块（“设置环境详细信息”）中，对于以下每个变量，单击&#x200B;**添加项**&#x200B;并输入变量的名称和值

   | 变量名称 | 变量值 |
   |---|---|
   | defaultJiraReporterID | 当Jira中不存在创建者用户时，输入默认用户的ID。 您可以通过单击用户配置文件并检查浏览器的URL来查找此用户ID。 示例：`https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 输入您要连接的Jira帐户的基本URL。 |
   | wfBaseURL | 输入您要连接的Workfront帐户的基本URL。 |

1. 继续[映射Jira中的自定义字段](#map-custom-fields-in-jira)

<!--#### Map custom fields in Jira. 

Awaiting feedback-->

+++

### 情景2：JIRA到Workfront：将问题和评论的更新从Jira发送回Workfront

在Jira中创建问题时，此方案会创建一个Workfront任务或问题。

>[!NOTE]
>
>此方案需要Jira的OAuth2连接。
>若要对Jira使用OAuth2授权，您必须在[https://developer.atlassian.com/console](https://developer.atlassian.com/console)处设置OAuth2应用程序。 有关信息和说明，请参阅Jira文档。

+++**展开以查看有关配置方案2：将JIRA配置到Workfront：将问题和评论的更新从Jira发送回Workfront的说明**

1. 单击左侧导航面板中的&#x200B;**模板**&#x200B;选项卡![模板图标](assets/templates-icon.png)。
1. 使用屏幕左上角附近的搜索栏搜索模板。 您可以按模板名称或包含的应用程序进行搜索。
1. 单击&#x200B;**第2部分：从JIRA到Workfront：将问题和评论的更新从Jira**&#x200B;模板发送回Workfront。

   此时将打开模板视图，显示信息以及数据流动画。
1. 在第一个模块中，开始添加webhook。
1. 选择使用系统集成用户凭据的连接，或使用系统集成凭据创建与Jira的连接。

* 有关创建与Jira连接的说明，请参阅“Jira软件模块”一文中的[将Jira连接到Workfront Fusion](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/jira-modules-new.md#connect-jira-to-workfront-fusion)。

1. 配置webhook过滤器

1. 继续[在Jira中配置webhook](#configure-a-webhook-in-jira)

#### 在Jira中配置webhook

1. 在Jira中，创建一个webhook。

   有关说明，请参阅Jira文档中的[Webhooks](https://developer.atlassian.com/server/jira/platform/webhooks/)。

1. 配置webhook时，请使用以下值：

   * **JQL**：项目=“您的项目名称”（其中，您的项目名称= JIRA项目名称）
   * **问题**：已创建、已更新
   * **评论**：已创建，已删除


1. 继续[将模板模块连接到Workfront和Jira（模块2）](#connect-template-modules-to-workfront-and-jira-module-2)

#### 将模板模块连接到Workfront和Jira（模块2）

1. 在&#x200B;**每个** Workfront模块的连接字段中，选择您在[在Workfront Fusion中配置连接](#configure-connections-in-workfront-fusion)中创建的Workfront连接，然后单击&#x200B;**确定**&#x200B;保存与该模块的连接。
1. 在&#x200B;**每个** Jira模块的“连接”字段中，选择您在[在Workfront Fusion中配置连接](#configure-connections-in-workfront-fusion)中创建的Workfront连接，然后单击&#x200B;**确定**保存与该模块的连接。
   <!--#### Map custom fields-->

+++

### 场景3：将Workfront更改为Jira：将Workfront任务更改为JIRA问题

+++**展开以查看有关配置方案3：WF到Jira更改（任务）的说明**

1. 单击左侧导航面板中的&#x200B;**模板**&#x200B;选项卡![模板图标](assets/templates-icon.png)。
1. 使用屏幕左上角附近的搜索栏搜索模板。 您可以按模板名称或包含的应用程序进行搜索。
1. 单击&#x200B;**Part 3： Workfront to Jira： Changes to Workfront task to JIRA issue**&#x200B;模板。

   此时将打开模板视图，显示信息以及数据流动画。

1. 单击模板以进入编辑器。
1. 选择将拥有此方案的组织和团队。
1. 在第一个模块中，开始添加webhook。
1. 在连接字段中，选择使用系统集成凭据的Workfront连接。
1. 在&#x200B;**记录类型**&#x200B;字段中，选择`Task`。
1. 在&#x200B;**状态**&#x200B;字段中，选择`New state`。
1. 使用&#x200B;**And**&#x200B;选项通过以下操作配置筛选器：

   | 字段 | 操作员 | 值 |
   |---|---|---|
   | assignedToID | 等于 | 输入系统集成用户的Workfront ID |
   | projectID | 等于 | 输入希望webhook监视的一个或多个项目的ID。 |
   | DE： Jira键 | 已存在 |  |

1. 启用&#x200B;**排除此连接所做的更新**&#x200B;选项。
1. 在&#x200B;**记录来源**&#x200B;字段中，选择`Updated record only`。
1. 单击&#x200B;**保存**&#x200B;以保存webhook，然后单击&#x200B;**确定**&#x200B;以保存触发器模块。
1. 在&#x200B;**设置JIRA变量**&#x200B;模块中，设置以下变量，然后单击&#x200B;**确定**&#x200B;保存该模块。

   | 变量名称 | 变量值 |
   |---|---|
   | defaultJiraReporterID | 这是Jira中不存在创建者用户时的默认用户ID。 您可以通过单击用户配置文件并检查浏览器的URL来查找此用户ID。 示例：`https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 要连接的Jira帐户的基本URL。 |
   | wfBaseURL | 要连接的Workfront帐户的基本URL。 |

1. 在&#x200B;**each** Workfront模块的“连接”字段中，选择使用系统集成凭据的Workfront连接，然后单击&#x200B;**确定**&#x200B;以保存该模块。
1. 在&#x200B;**每个** Jira模块的“连接”字段中，选择使用系统集成凭据的Jira连接，然后单击&#x200B;**确定**&#x200B;保存模块。

+++

### 场景4：将Workfront更改为Jira：将Workfront问题更改为JIRA问题

此方案会将Workfront问题中的更新发送到之前连接的JIRA问题。

+++**展开以查看有关配置场景4：将Workfront更改为Jira：将Workfront问题更改为JIRA问题**&#x200B;的说明

1. 单击左侧导航面板中的&#x200B;**模板**&#x200B;选项卡![模板图标](assets/templates-icon.png)。
1. 使用屏幕左上角附近的搜索栏搜索模板。 您可以按模板名称或包含的应用程序进行搜索。
1. 单击&#x200B;**方案4：WF到Jira的更改（问题）**&#x200B;模板。

   此时将打开模板视图，显示信息以及数据流动画。

1. 单击模板以进入编辑器。
1. 选择将拥有此方案的组织和团队。
1. 在第一个模块中，开始添加webhook。
1. 在连接字段中，选择使用系统集成凭据的Workfront连接。
1. 在&#x200B;**记录类型**&#x200B;字段中，选择`Issues`。
1. 在&#x200B;**状态**&#x200B;字段中，选择`New state`。
1. 使用&#x200B;**And**&#x200B;选项通过以下操作配置筛选器：

   | 字段 | 操作员 | 值 |
   |---|---|---|
   | assignedToID | 等于 | 输入系统集成用户的Workfront ID |
   | projectID | 等于 | 输入希望webhook监视的一个或多个项目的ID。 |
   | DE： Jira键 | 已存在 |  |

1. 启用&#x200B;**排除此连接所做的更新**&#x200B;选项。
1. 在&#x200B;**记录来源**&#x200B;字段中，选择`Updated record only`。
1. 单击&#x200B;**保存**&#x200B;以保存webhook，然后单击&#x200B;**确定**&#x200B;以保存触发器模块。
1. 在&#x200B;**设置JIRA变量**&#x200B;模块中，设置以下变量，然后单击&#x200B;**确定**&#x200B;保存该模块。

   | 变量名称 | 变量值 |
   |---|---|
   | defaultJiraReporterID | 这是Jira中不存在创建者用户时的默认用户ID。 您可以通过单击用户配置文件并检查浏览器的URL来查找此用户ID。 示例：`https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 要连接的Jira帐户的基本URL。 |
   | wfBaseURL | 要连接的Workfront帐户的基本URL。 |

1. 在&#x200B;**each** Workfront模块的“连接”字段中，选择使用系统集成凭据的Workfront连接，然后单击&#x200B;**确定**&#x200B;以保存该模块。
1. 在&#x200B;**每个** Jira模块的“连接”字段中，选择使用系统集成凭据的Jira连接，然后单击&#x200B;**确定**&#x200B;保存模块。

+++

### 场景5：从Workfront到Jira：在有关Workfront任务或问题的新注释时在JIRA中创建评论

+++**展开以查看有关配置场景5：将Workfront配置为Jira：在有关Workfront任务或问题的新注释时在JIRA中创建注释**

1. 单击左侧导航面板中的&#x200B;**模板**&#x200B;选项卡![模板图标](assets/templates-icon.png)。
1. 使用屏幕左上角附近的搜索栏搜索模板。 您可以按模板名称或包含的应用程序进行搜索。
1. 单击&#x200B;**方案5：WF到Jira新注释（任务和问题）**&#x200B;模板。

   此时将打开模板视图，显示信息以及数据流动画。
1. 在第一个模块中，开始添加webhook。
1. 在连接字段中，选择使用系统集成凭据的Workfront连接。
1. 在&#x200B;**记录类型**&#x200B;字段中，选择`Note`。
1. 在&#x200B;**状态**&#x200B;字段中，选择`New state`。
1. 使用以下操作配置过滤器：

   | 字段 | 操作员 | 值 |
   |---|---|---|
   | projectID<br>和<br>任务ID | 等于<br><br>存在 | 输入希望webhook监视的一个或多个项目的ID。 |
   | 或者 |  |  |
   | projectID<br>和<br>OpTaskID | 等于<br><br>存在 | 输入希望webhook监视的一个或多个项目的ID。 |

1. 启用&#x200B;**排除此连接所做的更新**&#x200B;选项。
1. 在&#x200B;**记录来源**&#x200B;字段中，选择`New record only`。
1. 单击&#x200B;**保存**&#x200B;以保存webhook，然后单击&#x200B;**确定**&#x200B;以保存触发器模块。
1. 在&#x200B;**设置变量**&#x200B;模块中设置以下变量，然后单击&#x200B;**确定**&#x200B;保存该模块。

   | 变量名称 | 变量值 |
   |---|---|
   | defaultJiraReporterID | 这是Jira中不存在创建者用户时的默认用户ID。 您可以通过单击用户配置文件并检查浏览器的URL来查找此用户ID。 示例：`https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 要连接的Jira帐户的基本URL。 |
   | wfBaseURL | 要连接的Workfront帐户的基本URL。 |

1. 在&#x200B;**each** Workfront模块的“连接”字段中，选择使用系统集成凭据的Workfront连接，然后单击&#x200B;**确定**&#x200B;以保存该模块。
1. 在&#x200B;**每个** Jira模块的“连接”字段中，选择使用系统集成凭据的Jira连接，然后单击&#x200B;**确定**&#x200B;保存模块。

+++

### 情景6：Workfront到Jira：在JIRA中创建Workfront任务或问题已删除注释的评论

+++**展开以查看有关配置方案6：从Workfront到Jira：在JIRA中创建有关Workfront任务或问题的已删除注释的注释**

1. 单击左侧导航面板中的&#x200B;**模板**&#x200B;选项卡![模板图标](assets/templates-icon.png)。
1. 使用屏幕左上角附近的搜索栏搜索模板。 您可以按模板名称或包含的应用程序进行搜索。
1. 单击&#x200B;**方案6：WF-to-Jira删除注释（任务和问题）**&#x200B;模板。

   此时将打开模板视图，显示信息以及数据流动画。
1. 在第一个模块中，开始添加webhook。
1. 在连接字段中，选择使用系统集成凭据的Workfront连接。
1. 在&#x200B;**记录类型**&#x200B;字段中，选择`Note`。
1. 在&#x200B;**状态**&#x200B;字段中，选择`New state`。
1. 使用以下操作配置过滤器：

   | 字段 | 操作员 | 值 |
   |---|---|---|
   | projectID<br>和<br>任务ID | 等于<br><br>存在 | 输入希望webhook监视的一个或多个项目的ID。 |
   | 或者 |  |  |
   | projectID<br>和<br>OpTaskID | 等于<br><br>存在 | 输入希望webhook监视的一个或多个项目的ID。 |

1. 启用&#x200B;**排除此连接所做的更新**&#x200B;选项。
1. 在&#x200B;**记录来源**&#x200B;字段中，选择`Deleted record only`。
1. 单击&#x200B;**保存**&#x200B;以保存webhook，然后单击&#x200B;**确定**&#x200B;以保存触发器模块。
1. 在第二个模块中，设置以下变量，然后单击&#x200B;**确定**&#x200B;保存该模块。

   | 变量名称 | 变量值 |
   |---|---|
   | defaultJiraReporterID | 这是Jira中不存在创建者用户时的默认用户ID。 您可以通过单击用户配置文件并检查浏览器的URL来查找此用户ID。 示例：`https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 要连接的Jira帐户的基本URL。 |
   | wfBaseURL | 要连接的Workfront帐户的基本URL。 |

1. 在&#x200B;**each** Workfront模块的“连接”字段中，选择使用系统集成凭据的Workfront连接，然后单击&#x200B;**确定**&#x200B;以保存该模块。
1. 在&#x200B;**每个** Jira模块的“连接”字段中，选择使用系统集成凭据的Jira连接，然后单击&#x200B;**确定**&#x200B;保存模块。

+++

### 场景7：从Workfront到Jira：新增有关Workfront任务或问题的文档时，在JIRA中创建评论

+++**展开以查看有关配置场景7：将Workfront配置为Jira：当有关Workfront任务或问题的新文档时，在JIRA中创建评论**

1. 单击左侧导航面板中的&#x200B;**模板**&#x200B;选项卡![模板图标](assets/templates-icon.png)。
1. 使用屏幕左上角附近的搜索栏搜索模板。 您可以按模板名称或包含的应用程序进行搜索。
1. 单击&#x200B;**方案7：WF到Jira的新附件（任务和问题）**&#x200B;模板。

   此时将打开模板视图，显示信息以及数据流动画。
1. 在第一个模块中，开始添加webhook。
1. 在连接字段中，选择使用系统集成凭据的Workfront连接。
1. 在&#x200B;**记录类型**&#x200B;字段中，选择`Document`。
1. 在&#x200B;**状态**&#x200B;字段中，选择`New state`。
1. 使用&#x200B;**And**&#x200B;选项通过以下操作配置筛选器：

   | 字段 | 操作员 | 值 |
   |---|---|---|
   | assignedToID | 等于 | 输入系统集成用户的Workfront ID |
   | projectID | 等于 | 输入希望webhook监视的一个或多个项目的ID。 |

1. 在第二个模块中，设置以下变量。

   | 变量名称 | 变量值 |
   |---|---|
   | defaultJiraReporterID | 这是Jira中不存在创建者用户时的默认用户ID。 您可以通过单击用户配置文件并检查浏览器的URL来查找此用户ID。 示例：`https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 要连接的Jira帐户的基本URL。 |
   | wfBaseURL | 要连接的Workfront帐户的基本URL。 |

1. 启用&#x200B;**排除此连接所做的更新**&#x200B;选项。
1. 在&#x200B;**记录来源**&#x200B;字段中，选择`New record only`。
1. 单击&#x200B;**保存**&#x200B;以保存webhook，然后单击&#x200B;**确定**&#x200B;以保存触发器模块。
1. 在&#x200B;**each** Workfront模块的“连接”字段中，选择使用系统集成凭据的Workfront连接，然后单击&#x200B;**确定**&#x200B;以保存该模块。
1. 在&#x200B;**每个** Jira模块的“连接”字段中，选择使用系统集成凭据的Jira连接，然后单击&#x200B;**确定**&#x200B;保存模块。

+++

### 情景8：Workfront到Jira：在JIRA中创建Workfront任务或问题上的已删除文档的评论

+++**展开以查看有关配置场景8：将Workfront配置为Jira：在JIRA中创建Workfront任务或问题上已删除文档的注释**

1. 单击左侧导航面板中的&#x200B;**模板**&#x200B;选项卡![模板图标](assets/templates-icon.png)。
1. 使用屏幕左上角附近的搜索栏搜索模板。 您可以按模板名称或包含的应用程序进行搜索。
1. 单击&#x200B;**方案8：WF到Jira删除附件（任务和问题）**&#x200B;模板。

   此时将打开模板视图，显示信息以及数据流动画。
1. 在第一个模块中，开始添加webhook。
1. 在连接字段中，选择使用系统集成凭据的Workfront连接。
1. 在&#x200B;**记录类型**&#x200B;字段中，选择`Document`。
1. 在&#x200B;**状态**&#x200B;字段中，选择`New state`。
1. 使用以下操作配置过滤器：

   | 字段 | 操作员 | 值 |
   |---|---|---|
   | projectID<br>和<br>任务ID | 等于<br><br>存在 | 输入希望webhook监视的一个或多个项目的ID。 |
   | 或者 |  |  |
   | projectID<br>和<br>OpTaskID | 等于<br><br>存在 | 输入希望webhook监视的一个或多个项目的ID。 |

1. 在&#x200B;**Set variables**&#x200B;模块中设置以下变量。

   | 变量名称 | 变量值 |
   |---|---|
   | defaultJiraReporterID | 这是Jira中不存在创建者用户时的默认用户ID。 您可以通过单击用户配置文件并检查浏览器的URL来查找此用户ID。 示例：`https://myjira.atlassian.net/jira/people/<JiraUserID>` |
   | JiraBaseURL | 要连接的Jira帐户的基本URL。 |
   | wfBaseURL | 要连接的Workfront帐户的基本URL。 |

1. 启用&#x200B;**排除此连接所做的更新**&#x200B;选项。
1. 在&#x200B;**记录来源**&#x200B;字段中，选择`Deleted record only`。
1. 单击&#x200B;**保存**&#x200B;以保存webhook，然后单击&#x200B;**确定**&#x200B;以保存触发器模块。
1. 在&#x200B;**each** Workfront模块的“连接”字段中，选择使用系统集成凭据的Workfront连接，然后单击&#x200B;**确定**&#x200B;以保存该模块。
1. 在&#x200B;**每个** Jira模块的“连接”字段中，选择使用系统集成凭据的Jira连接，然后单击&#x200B;**确定**&#x200B;保存模块。


+++

