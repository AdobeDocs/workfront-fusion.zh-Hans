---
title: GitLab模块
description: 除了Adobe Workfront许可证之外，Adobe Workfront Fusion还需要Adobe Workfront Fusion许可证。
author: Becky
feature: Workfront Fusion
exl-id: fabbadce-5669-4363-834e-6d7428520f62
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '4122'
ht-degree: 1%

---

# [!UICONTROL GitLab]模块

除了Adobe Workfront许可证之外，Adobe Workfront Fusion还需要Adobe Workfront Fusion许可证。

在Adobe Workfront Fusion方案中，您可以自动使用[!UICONTROL GitLab]的工作流，并将其连接到多个第三方应用程序和服务。

>[!NOTE]
>
>本文期望读者对API文档以及一般的[!DNL GitLab]功能有一定的了解。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront计划*</td>
  <td> <p>[！UICONTROL Pro]或更高版本</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证*</td>
   <td> <p>[！UICONTROL计划]，[！UICONTROL工作]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前许可证要求：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[！UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[！UICONTROL Select]或[！UICONTROL Prime] Adobe Workfront计划，则贵组织必须购买Adobe Workfront Fusion和Adobe Workfront，才能使用本文中所述的功能。 Workfront Fusion包含在[！UICONTROL Ultimate] Workfront计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买Adobe Workfront Fusion和Adobe Workfront，才能使用本文中所述的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有的计划、许可证类型或访问权限，请联系您的Workfront管理员。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## 将[!DNL GitLab]连接到Workfront Fusion {#connect-gitlab-to-workfront-fusion}

1. 在任意Workfront Fusion [!DNL Gitlab]模块中，单击连接字段旁边的&#x200B;**[!UICONTROL 添加]**。
1. 配置以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[！UICONTROL连接名称]</td> 
      <td> <p>输入连接的名称。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL [!DNL GitLab] URL]</td> 
      <td>输入[!DNL GitLab]实例的URL。</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL访问令牌]</td> 
      <td><p>输入您的[！UICONTROL专用令牌]或[！UICONTROL个人访问令牌]。</p><p>有关在[!DNL GitLab]中查找或创建个人访问令牌的信息，请参阅<a href="https://docs.gitlab.com/ee/user/profile/personal_access_tokens.html">文档中的</a>个人访问令牌[!DNL GitLab]中的“创建个人访问令牌”。</p></td> 
     </tr> 
    </tbody> 
   </table>


1. 单击&#x200B;**[!UICONTROL 继续]**。
1. 单击&#x200B;**[!UICONTROL 授权]**&#x200B;以创建连接并返回模块。

## [!DNL GitLab]模块及其字段

在配置[!DNL GitLab]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL GitLab]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 触发器

+++**[!UICONTROL 监视生成状态]**

此即时触发器模块会在内部版本状态更改时启动方案。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望webhook监视生成状态更改的项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 观看提交/MR/问题/代码片段评论]**

此即时触发器模块在对提交、合并请求、问题或代码片段进行注释时启动场景。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望webhook监视其注释的项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 观看提交（推送）]**

此即时触发模块会在将提交推送到存储库时启动方案。 此模块不会在推送标记时启动方案。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望webhook监视提交的项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 观看问题评论]**

此即时触发器模块在对问题作出评论时启动场景。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望webhook关注的问题评论</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 关注问题]**

此[!UICONTROL 即时触发器]模块在创建问题或更新、关闭或重新打开现有问题时启动方案。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望webhook关注的问题项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 观看合并请求]**

出现以下情况之一时，此即时触发模块将启动一个场景：

* 已创建新的合并请求
* 现有合并请求已更新、合并或关闭
* 在源分支中添加了提交


<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望webhook监视合并请求的项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 监视合并请求注释]**

此即时触发器模块在对合并请求作出评论时启动方案。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>希望webhook监视合并请求注释的项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 监视管道状态]**

此即时触发器模块在管道状态更改时启动场景。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望webhook监视管道状态更改的项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 观看项目]**

此计划触发器模块在添加新项目时启动一个方案，经过身份验证的用户是该新项目的成员。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关将[!DNL GitLab]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">将[!DNL GitLab]连接到Workfront Fusion</a>。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">最大结果</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中监视的最大记录数。</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 监视存储库分支]**

此计划触发器模块会在向存储库添加新分支时启动方案。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关将[!DNL GitLab]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">将[!DNL GitLab]连接到Workfront Fusion</a>。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">最大结果</td> 
   <td> <p>输入或映射您希望模块在每个方案执行周期中监视的最大记录数。</p> </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 监视存储库标记]**

此即时触发器模块会在存储库中创建或删除标记时启动方案。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望webhook监视标记的项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 观看代码片段的评论]**

此即时触发器模块在对代码片段进行新注释时启动方案。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望webhook监视其注释的项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 观看待办事项]**

此计划触发器模块在添加新待办事项后启动方案。 未应用筛选器时，触发器将在添加新的待处理任务时运行。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos)获取待办事项列表[!DNL GitLab]。

+++

+++**[!UICONTROL 观看Wiki页面]**

此即时触发器模块会在创建或编辑Wiki页面时启动方案。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Webhook]</td> 
   <td><p>选择要用于此触发器的webhook，或添加新的webhook。 </p><p>要添加新的webhook， <ol><li>单击[！UICONTROL webhook]字段旁边的<b>[！UICONTROL Add]</b>。</li><li>输入以下内容： <ul><li>webhook的名称</li><li>要用于此webhook的连接</li><li>您希望Webhook关注Wiki页面的项目</li></ul></li><li>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。 </td> 
   </tr> 
   </tbody> 
</table>

+++

### 操作

+++**[!UICONTROL 接受合并请求]**

此操作模块将提交的更改与给定的合并请求合并。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html#accept-mr)接受合并请求[!DNL GitLab]。

+++

+++**[!UICONTROL 取消生成]**

此操作模块会取消项目的单次生成。

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关将[!DNL GitLab]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-gitlab-to-workfront-fusion-connect-gitlab-to-workfront-fusion" class="MCXref xref">将[!DNL GitLab]连接到Workfront Fusion</a>。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[！UICONTROL项目ID]</td> 
   <td> <p>选择或映射包含要取消的生成的项目。</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[！UICONTROL内部版本ID]</td> 
   <td>选择或映射要取消的生成。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[！UICONTROL合并提交消息]</td> 
   <td> 输入或映射合并的提交消息。
    </td> 
   </tr> 
   <tr> 
   <td role="rowheader">[！UICONTROL应删除源分支]</td> 
   <td>选择合并完成时是否要删除源分支。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">构建成功时进行[！UICONTROL合并]</td> 
   <td>选择是否在构建完成后立即合并合并合并请求。</td> 
   </tr> 
   <tr> 
   <td role="rowheader">[！UICONTROL SHA]</td> 
   <td>如果存在，则此SHA必须与源分支的HEAD匹配。 如果不匹配，合并将失败。</td> 
   </tr> 
   </tbody> 
</table>

+++

+++**[!UICONTROL 取消管道的生成]**

此操作模块会取消单个管道的构建。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/pipelines.html#cancel-a-pipelines-jobs)取消管道作业[!DNL GitLab]。

+++

+++管道成功时&#x200B;**[!UICONTROL 取消合并]**

如果合并请求设置为在管道成功时合并，则此操作模块将取消该操作。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html)管道成功时取消合并[!DNL GitLab]。

+++

+++**[!UICONTROL 樱桃选择承诺]**

此操作模块樱桃选择提交到给定分支。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/commits.html#cherry-pick-a-commit)Cherry选择提交[!DNL GitLab]。

+++

+++**[!UICONTROL 创建新标签]**

此操作模块为给定存储库创建新标签。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/labels.html#create-a-new-label)创建新标签[!DNL GitLab]。

+++

+++**[!UICONTROL 创建新管道]**

此操作模块为给定项目创建新管道。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/pipelines.html#create-a-new-pipeline)新建管道[!DNL GitLab]。

+++

+++**[!UICONTROL 创建新版本]**

此操作模块将发行说明添加到现有的Git标记。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/releases/#create-a-release)创建版本[!DNL GitLab]。

+++

+++**[!UICONTROL 新建标记]**

此操作模块在存储库中创建一个指向所提供的参考的新标记。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/tags.html#create-a-new-tag)创建新标记[!DNL GitLab]。

+++

+++**[!UICONTROL 创建任务]**

此操作模块为选定问题的当前用户创建一个任务。 当前用户是由用于此模块的连接上的凭据标识的用户。

有关字段的信息，请参阅文档中的[创建待办事项](https://docs.gitlab.com/ee/api/issues.html#create-a-todo)。[!DNL GitLab]

+++

+++**[!UICONTROL 对合并请求创建任务]**

此操作模块为所选合并请求上的当前用户创建一个任务。 当前用户是由用于此模块的连接上的凭据标识的用户。

有关字段的信息，请参阅文档中的[创建待办事项](https://docs.gitlab.com/ee/api/merge_requests.html#create-a-todo)。[!DNL GitLab]

+++

+++**[!UICONTROL 创建合并请求]**

此操作模块在项目上创建新的合并请求。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html#create-mr)创建合并请求[!DNL GitLab]。

+++

+++**[!UICONTROL 在存储库中创建新文件]**

此操作模块在选定存储库中创建新文件。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/repository_files.html#create-new-file-in-repository)在存储库中创建新文件[!DNL GitLab]。

+++

+++**[!UICONTROL 新建问题说明]**

此操作模块为单个项目问题创建问题说明。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#create-new-issue-note)新建问题说明[!DNL GitLab]。

+++

+++**[!UICONTROL 创建新的合并请求注释]**

此操作模块为单个合并请求创建注释。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#create-new-merge-request-note)新建合并请求注释[!DNL GitLab]。

+++

+++**[!UICONTROL 创建新里程碑]**

此操作模块为项目创建新的里程碑。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/milestones.html#create-new-milestone)新建里程碑[!DNL GitLab]。

+++

+++**[!UICONTROL 创建新代码片段备注]**

此操作模块为单个代码片段创建新注释。 代码片段注释是用户可以在代码片段中发布的评论。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#create-new-snippet-note)新建代码片段注释[!DNL GitLab]。

+++

+++**[!UICONTROL 创建存储库分支]**

此操作模块会创建一个存储库分支。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/branches.html#create-repository-branch)创建存储库分支[!DNL GitLab]。

+++

+++**[!UICONTROL 创建生成变量]**

此操作模块创建一个新的生成变量。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/project_level_variables.html#create-variable)创建变量[!DNL GitLab]。

+++

+++**[!UICONTROL 删除合并请求]**

此操作模块仅适用于管理员和项目所有者。 它会删除有问题的合并请求

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html#delete-a-merge-request)删除合并请求[!DNL GitLab]。

+++

+++**[!UICONTROL 删除存储库中的现有文件]**

此操作模块从存储库中删除现有文件。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/repository_files.html#delete-existing-file-in-repository)删除存储库[!DNL GitLab]中的现有文件。

+++

+++**[!UICONTROL 删除存储库分支]**

此操作模块会从存储库中删除分支。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/branches.html#delete-repository-branch)删除存储库分支[!DNL GitLab]。

+++

+++**[!UICONTROL 编辑问题]**

此操作模块可更新现有项目问题。 此调用还用于将问题标记为已关闭。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/issues.html#edit-issue)编辑问题[!DNL GitLab]。

+++

+++**[!UICONTROL 编辑里程碑]**
此操作模块可更新现有项目里程碑。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/milestones.html#edit-milestone)编辑里程碑[!DNL GitLab]

+++

+++**[!UICONTROL 擦除生成]**

此操作模块会清除项目的生成（删除作业工件和作业日志）。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/jobs.html#erase-a-job)擦除作业[!DNL GitLab]。

+++

+++**[!UICONTROL 获取待办事项列表]**

此搜索模块检索待办事项列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/todos.html#get-a-list-of-todos)获取待办事项列表[!DNL GitLab]。

+++

+++**[!UICONTROL 获取单个内部版本]**

此操作模块可检索项目的单个作业。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/jobs.html#get-a-single-job)获取单个作业[!DNL GitLab]。

+++

+++**[!UICONTROL 获取单个存储库标记]**

此操作模块可检索由其名称确定的特定存储库标记。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/tags.html#get-a-single-repository-tag)获取单个存储库标记[!DNL GitLab]。

+++

+++**[!UICONTROL 获取特定部署]**

此操作模块可检索特定部署。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/deployments.html#get-a-specific-deployment)获取特定部署[!DNL GitLab]。

+++

+++**[!UICONTROL 获取分配给单个里程碑的所有问题]**

此搜索模块可检索分配给单个项目里程碑的所有问题。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/milestones.html#get-all-issues-assigned-to-a-single-milestone)获取分配给单个里程碑的所有问题[!DNL GitLab]。

+++

+++**[!UICONTROL 从存储库获取文件]**

此操作模块可检索存储库中文件的相关信息，如名称、大小或内容。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/repository_files.html#get-file-from-repository)从存储库获取文件[!DNL GitLab]。

+++

+++**[!UICONTROL 获取项目用户]**

此搜索模块可检索项目的用户。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/projects.html#get-project-users)获取项目用户[!DNL GitLab]。

+++

+++**[!UICONTROL 获取单个问题]**

此操作模块可检索问题详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>要创建新连接，请参阅本文中的<a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[！UICONTROL将[!DNL GitLab]连接到Workfront Fusion]</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL项目]</td> 
   <td> <p>选择包含您要检索其详细信息的问题的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL问题ID]</td> 
   <td> <p>输入或映射您要检索其详细信息的问题的名称。</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL 获取单个问题说明]**

此操作模块可检索特定项目问题的单个注释。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#get-single-issue-note)获取单个问题说明[!DNL GitLab]。

+++

+++**[!UICONTROL 获取单一合并请求]**

此操作模块可检索有关单个合并请求的信息。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr)获取单一合并请求[!DNL GitLab]。

+++

+++**[!UICONTROL 获取单一合并请求更改]**

此搜索模块可检索有关合并请求的信息，包括其文件和更改。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-changes)获取单一合并请求更改[!DNL GitLab]。

+++

+++**[!UICONTROL 获取单一合并请求提交]**

此操作模块检索合并请求提交的列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html#get-single-mr-commits)获取单一合并请求提交[!DNL GitLab]。

+++

+++**[!UICONTROL 获取单合并请求注释]**

此操作模块为给定的合并请求返回单个注释。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#get-single-merge-request-note)获取单一合并请求注释[!DNL GitLab]。

+++

+++**[!UICONTROL 获取里程碑]**

此操作模块可检索里程碑详细信息。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/milestones.html#get-single-milestone)获取单个里程碑[!DNL GitLab]。

+++

+++**[!UICONTROL 获取单个项目]**

此操作模块可检索项目详细信息。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/projects.html#get-single-project)获取单个项目[!DNL GitLab]。

+++

+++**[!UICONTROL 获取单个存储库分支]**

此操作模块可检索存储库分支详细信息。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/branches.html#get-single-repository-branch)获取单个存储库分支[!DNL GitLab]。

+++

+++**[!UICONTROL 获取代码片段注释]**

此模块检索给定代码片段的单个注释。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#get-single-snippet-note)获取单个代码片段注释[!DNL GitLab]。

+++

+++**[!UICONTROL 获取提交的注释]**

此搜索模块检索项目中提交的注释。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/commits.html#get-the-comments-of-a-commit)获取承诺[!DNL GitLab]的注释。

+++

+++**[!UICONTROL 获取提交的差异]**

此操作模块获取项目中的提交差异。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/commits.html#get-the-diff-of-a-commit)获取提交[!DNL GitLab]的差异。

+++

+++**[!UICONTROL 保留项目]**

防止在设置了到期时删除工件。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/job_artifacts.html#keep-artifacts)保留工件[!DNL GitLab]。

+++

+++**[!UICONTROL 列出所有合并请求注释]**

此搜索模块检索单个合并请求的所有注释列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#list-all-merge-request-notes)列出所有合并请求注释[!DNL GitLab]。

+++

+++**[!UICONTROL 列出所有代码片段备注]**

此模块获取单个代码片段的所有注释列表。 代码片段注释是用户可以在代码片段中发布的评论。

有关字段的信息，请参阅[🔗文档中的](https://docs.gitlab.com/ee/api/notes.html#list-all-snippet-notes)[!DNL GitLab]。

+++

+++**[!UICONTROL 列出提交生成]**

此搜索模块会返回项目中特定提交的内部版本列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>要创建新连接，请参阅本文中的<a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[！UICONTROL将[!DNL GitLab]连接到Workfront Fusion]</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL项目ID]</td> 
   <td> <p>选择包含要为其列出内部版本的提交的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL作用域]</td> 
   <td> 要将搜索限制为以特定状态构建，请选择状态。 将此字段留空将返回提交的所有生成。  </td> 
  </tr> 
 </tbody> 
</table>

+++

+++**[!UICONTROL 列出问题]**

此搜索模块按指定的过滤器设置返回所有问题。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/issues.html#list-issues)列出问题[!DNL GitLab]。

+++

+++**[!UICONTROL 列出合并时关闭的问题]**

此搜索模块可检索通过合并提供的合并请求而关闭的所有问题。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html#list-issues-that-will-close-on-merge)列出合并时关闭的问题[!DNL GitLab]。

+++

+++**[!UICONTROL 列出标签]**

此搜索模块检索项目中的所有标签。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/labels.html#list-labels)列表标签[!DNL GitLab]。

+++

+++**[!UICONTROL 列出合并请求]**

此搜索模块按筛选器设置检索所有合并请求。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html#list-merge-requests)列出合并请求[!DNL GitLab]。

+++

+++**[!UICONTROL 列出拥有的项目]**

此搜索模块可检索其已验证用户设置为所有者的项目。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/projects.html#list-all-projects)列出用户项目[!DNL GitLab]。

+++

+++**[!UICONTROL 列出项目内部版本]**

此搜索模块可检索项目中的内部版本列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/jobs.html#list-project-jobs)列出项目作业[!DNL GitLab]。

+++

+++**[!UICONTROL 列出项目部署]**

此搜索模块可检索项目中的部署列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/deployments.html#list-project-deployments)列出项目部署[!DNL GitLab]。

+++

+++**[!UICONTROL 列出项目问题说明]**

此搜索模块可检索单个问题的所有注释列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#list-project-issue-notes)列出项目问题说明[!DNL GitLab]。

+++

+++**[!UICONTROL 列出项目问题]**

此搜索模块返回指定项目中的所有问题。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/issues.html#list-project-issues)列出项目问题[!DNL GitLab]。

+++

+++**[!UICONTROL 列出项目里程碑]**

此搜索模块检索项目中的所有里程碑。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/milestones.html#list-project-milestones)列出项目里程碑[!DNL GitLab]。

+++

+++**[!UICONTROL 列出项目管道]**

此搜索模块检索项目的所有管道。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/pipelines.html#list-project-pipelines)列出项目管道[!DNL GitLab]。

+++

+++**[!UICONTROL 列出项目存储库标记]**

此搜索模块从项目中检索存储库标记的列表，这些标记按名称的逆字母顺序排序。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/tags.html#list-project-repository-tags)列出项目存储库标记[!DNL GitLab]。

+++

+++**[!UICONTROL 列出项目变量]**

此搜索模块可检索项目变量的列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/project_level_variables.html#list-project-variables)列出项目变量[!DNL GitLab]。

+++

+++**[!UICONTROL 列出项目]**

此搜索模块可检索经过身份验证的用户所属的所有项目。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/projects.html#list-all-projects)列出所有项目[!DNL GitLab]。

+++

+++**[!UICONTROL 列出存储库分支]**

此模块按搜索词搜索存储库分支。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/branches.html#list-repository-branches)列出存储库分支[!DNL GitLab]。

+++

+++**[!UICONTROL 列出存储库提交]**

此搜索模块可检索项目中的存储库提交列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/commits.html#list-repository-commits)列出存储库提交[!DNL GitLab]。

+++

+++**[!UICONTROL 列出存储库参与者]**

此搜索模块可检索存储库参与者列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/repositories.html#contributors)参与者[!DNL GitLab]。

+++

+++**[!UICONTROL 列出存储库树]**

此搜索模块可检索项目中的存储库文件和目录的列表。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/repositories.html#list-repository-tree)列出存储库树[!DNL GitLab]。

+++

+++**[!UICONTROL 将待办事项标记为完成]**

此操作模块将当前用户ID给定的单个待办事项标记为完成。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/todos.html#mark-a-todo-as-done)将待办事项标记为完成[!DNL GitLab]。

+++

+++**[!UICONTROL 修改现有问题说明]**

修改问题的现有注释。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#modify-existing-issue-note)修改现有问题说明[!DNL GitLab]。

+++

+++**[!UICONTROL 修改现有的合并请求注释]**

修改合并请求的现有注释。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#modify-existing-merge-request-note)修改现有的合并请求注释[!DNL GitLab]。

+++

+++**[!UICONTROL 修改现有代码片段注释]**

此操作模块修改代码片段的现有注释。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/notes.html#modify-existing-snippet-note)修改现有代码片段注释[!DNL GitLab]。

+++

+++**[!UICONTROL 新问题]**

此操作模块将创建新的项目问题。

有关字段的信息，请参阅[文档中的](https://www.integromat.com/en/help/app/gitlab)新问题[!DNL GitLab]。

+++

+++**[!UICONTROL 播放内部版本]**

此操作模块会触发启动作业的手动操作。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/jobs.html#play-a-job)播放作业[!DNL GitLab]

+++

+++**[!UICONTROL 发布评论以提交]**

此操作模块向提交添加注释。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/commits.html#post-comment-to-commit)发布要提交的注释[!DNL GitLab]。

+++

+++**[!UICONTROL 删除变量]**

此操作模块可删除项目的变量。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/project_level_variables.html#remove-variable)删除变量[!DNL GitLab]。

+++

+++**[!UICONTROL 重试生成]**

此操作模块在提交中重试单个生成。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>要创建新连接，请参阅本文中的<a href="#connect-gitlab-to-workfront-fusion" class="MCXref xref">[！UICONTROL将[!DNL GitLab]连接到Workfront Fusion]</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL项目ID]</td> 
   <td> <p>选择包含要重试的生成的项目。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL内部版本ID]</td> 
   <td> 选择要重试的生成。 </td> 
  </tr> 
 </tbody> 
</table>

+++

+++重试管道中失败的作业&#x200B;****

此操作模块重试管道中失败的生成。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/pipelines.html#retry-jobs-in-a-pipeline)重试管道[!DNL GitLab]中的作业。

+++

+++**[!UICONTROL 获取变量]**

此模块可检索项目特定变量的详细信息。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/project_level_variables.html#show-variable-details)显示变量详细信息[!DNL GitLab]。

+++

+++**[!UICONTROL 更新版本]**

此操作模块更新版本。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/releases/#update-a-release)更新版本[!DNL GitLab]。

+++

+++**[!UICONTROL 更新合并请求]**

此操作模块更新现有的合并请求。 您可以更改目标分支、标题，甚至关闭MR。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/merge_requests.html#update-mr)更新合并请求[!DNL GitLab]

+++

+++**[!UICONTROL 更新变量]**

此操作模块可更新项目的变量。

有关字段的信息，请参阅[文档中的](https://docs.gitlab.com/ee/api/project_level_variables.html#update-variable)更新变量[!DNL GitLab]

+++
