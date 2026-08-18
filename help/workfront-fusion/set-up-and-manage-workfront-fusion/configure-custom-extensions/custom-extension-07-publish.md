---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 发布自定义扩展
description: 发布自定义扩展
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: 925a8ee910434c474d527c2914897d7c42e4a3d1
workflow-type: tm+mt
source-wordcount: 1236
ht-degree: 1%

---

# 发布自定义扩展

>[!NOTE]
>
>本文假定您对软件开发工具有一定的了解。

您的扩展只有在&#x200B;**生成**、**部署到Adobe**&#x200B;并为您的组织&#x200B;**批准**&#x200B;之后才能在Fusion中运行。 此页面上的过程说明了如何发布扩展以及如何验证结果。

此信息根据Adobe的官方文档进行改编，具体适用于Workfront Fusion。 有关Adobe的一般信息，请参阅Adobe文档中的[UI扩展开发流程](https://developer.adobe.com/uix/docs/guides/development-flow/)和[UI扩展管理](https://developer.adobe.com/uix/docs/guides/publication/)。

## 工作区

每个App Builder项目都有一个&#x200B;**阶段**&#x200B;和一个&#x200B;**生产**&#x200B;工作区。 将它们视为环境：

* **阶段**&#x200B;用于开发和测试。 在迭代过程中，请在此处部署。 无需审批，并且结果仅通过下面描述的暂存测试开关（或本地预览）可见。
* **生产**&#x200B;将发布给每个人。 部署到生产环境后，您提交&#x200B;**审批请求**，在获得批准后，该扩展将在Adobe应用程序注册表中注册并向整个组织显示。

>[!NOTE]
>
> **角色：**&#x200B;创建和部署需要&#x200B;**开发人员**&#x200B;角色；提交审批请求以进行发布需要&#x200B;**系统管理员**角色。
>有关更多信息，请参阅：
>
> * [设置UI扩展工具和帐户](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-02-set-up-tools-account.md)
> * 在Adobe文档中[如何获取访问权限](https://developer.adobe.com/uix/docs/guides/get-access/)。

默认情况下，Fusion仅显示&#x200B;**已发布的**&#x200B;扩展。 这些是您已部署到&#x200B;**生产**&#x200B;工作区并提交&#x200B;**审批**&#x200B;的扩展。 这是安全的默认设置，因此进行中的部署绝不会意外出现在整个组织中。

对&#x200B;**Stage**&#x200B;工作区的部署未发布，因此它本身不会出现在Fusion中。 在发布扩展之前，您可以通过两种方式尝试该扩展：

* **使用`aio app run`在本地预览它**（请参阅Adobe文档中的[UI扩展的本地预览](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/)）。 没有部署任何内容，只有您看到它。
* 在Fusion配置文件中打开每个用户的测试开关，从Fusion **中的Stage加载它**。 本文中的[在Fusion](#test-a-stage-build-in-fusion)中测试暂存内部版本中对此进行了说明。

## 在Fusion中测试暂存内部版本

使用此流在发布Fusion之前查看Stage部署。

### 第1步：选择舞台工作区

```sh
aio console where                  # shows current org / project / workspace
aio console workspace select       # choose Stage
```

### 步骤2：构建

```sh
aio app build
```

这将编译您的前端并运行元数据挂接（生成`app-metadata.json`）。 修复所有报告的错误，然后再继续。

### 步骤3：部署

```sh
aio app deploy
```

`deploy`执行两项操作：

* **在Adobe的内容交付网络上以`https://<project>-stage.adobeio-static.net`之类的URL承载您的UI**。 CLI完成时打印此&#x200B;**扩展终结点URL**。 这是加载到其iframe中的URL Fusion。
* **在阶段工作区中为扩展点(`fusion/nav-organization/1`)注册扩展端点**。

>[!TIP]
>
> **如果部署失败，并且“扩展点&#39;fusion/nav-organization/1&#39;不存在”（错误1060）：**尚未为您的组织启用Fusion扩展点。 这是载入步骤，不是代码中的错误。
>有关详细信息，请参阅疑难解答文章中的[扩展点不存在](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md#error-1060-extension-point-does-not-exist)。

### 步骤4：在Fusion配置文件中打开暂存测试

仅当您选择启用时，Fusion才加载暂存扩展，每个用户：

1. 使用您部署到&#x200B;**同一组织**&#x200B;中的帐户登录到Fusion。
1. 打开上角的用户头像菜单，然后转到&#x200B;**产品设置** > **Fusion配置文件** > **首选项**。
1. 打开&#x200B;**暂存扩展**&#x200B;开关。

   Fusion会提示您重新加载。
1. 确认重新加载。

重新加载后，Fusion会从暂存工作区而不是发布的集加载扩展，并在导航中标记每个&#x200B;**（暂存）**，以便您区分它们。

此开关是存储在浏览器中的个人测试设置，不是组织设置。 将其关闭（并重新加载），以返回到发布的扩展。 由于它存储在本地，因此它不会跟随您转到其他浏览器或计算机。

### 步骤5：在Fusion中验证

1. 打开与扩展点匹配的部分：
   * `fusion/nav-organization/1`→左侧导航的&#x200B;**组织**&#x200B;区域。
   * `fusion/nav-team/1`→**团队**&#x200B;区域（首先选择一个团队）。

   将显示一个具有您在`getWidget()`中设置的标题的按钮，该按钮标记为&#x200B;**（阶段）**。
1. 单击显示的按钮。

您的UI加载并接收[Fusion上下文](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-06-context-reference.md)。

如果按钮未出现或面板显示错误，请参阅[疑难解答](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-08-troubleshooting.md)。

## 发布于生产环境

当扩展在Stage上工作，并且您已经为所有用户做好了准备时：

### 步骤1：切换到生产工作区

```sh
aio console workspace select       # choose Production
```

当CLI提示有关`.env`文件时，请选择&#x200B;**合并**，以便保留环境变量。

### 步骤2：生成并部署到生产环境

```sh
aio app build
aio app deploy
```

### 第3步：提交审批请求

发布是从生产工作区&#x200B;**提交的**&#x200B;审批请求：

1. 打开[Adobe Developer Console](https://developer.adobe.com/console)，选择您的&#x200B;**组织**，打开您的&#x200B;**项目**，然后切换到&#x200B;**生产**&#x200B;工作区。
1. 提交应用程序以进行&#x200B;**审批/发布**（这需要&#x200B;**系统管理员**&#x200B;角色）。
1. 批准后，您的扩展将添加到&#x200B;**Adobe应用程序注册表**，并可在贵组织的[Adobe Experience Cloud](https://experience.adobe.com)（包括Fusion）中使用。

有关详细说明，请参阅Adobe Developer文档中的[UI扩展管理](https://developer.adobe.com/uix/docs/guides/publication/)。

## 状态和更新

一些行为值得一知，因此除了“出了问题”以外，你还可以分辨出“仍在努力”：

* **部署到生产环境与可见环境不同。** 将`aio app deploy`上传到生产环境，但不会显示扩展。 它仅在审批请求提交并审批之后显示。 如果您已部署到生产环境，但仍未在Fusion中看到它，则通常原因是尚未批准它。
* **仅代码更新不需要新审批。** 如果您的扩展已发布，并且您仅更改其代码（UI或运行时操作），请使用以下内容重新部署到同一URL：

  ```sh
  aio app deploy --force-deploy
  ```

  用户下次打开扩展时会获得新版本。 没有可供安装的内容。 您只需在更改&#x200B;**注册**&#x200B;本身（例如添加新的扩展点或更改`getWidget()`的广告）时提交新的审批请求。
* **已撤销或已撤销的扩展已消失。** 如果扩展被您撤销或撤消，它将停止在Fusion中显示，并且不显示错误消息。 如果每个用户都丢失了以前正常使用的扩展，请在搜索代码问题之前检查该扩展是否已撤销。

## 删除（撤销）扩展

删除已发布的扩展操作由&#x200B;**在Adobe Exchange中撤消**&#x200B;完成：

1. 登录到&#x200B;**Adobe Exchange**。
1. 转到&#x200B;**管理** > **App Builder应用程序**。
1. 选择位于要删除的扩展旁边的&#x200B;**撤销**，然后进行确认。

撤销后，扩展在Extension Manager中显示&#x200B;*已撤销*&#x200B;状态，并且不再出现在Fusion中。 要完全删除它，请在Developer Console中删除该项目。 在撤销项目扩展之前，无法删除项目。

对于仅暂存测试部署，您可以通过以下方式删除部署：

```sh
aio app undeploy
```

## 其他资源

Adobe文档中提供了以下资源：

* [UI扩展开发流程](https://developer.adobe.com/uix/docs/guides/development-flow/)
* [UI扩展管理（发布/批准/撤销）](https://developer.adobe.com/uix/docs/guides/publication/)
* [在Developer Console中创建项目](https://developer.adobe.com/uix/docs/guides/creating-project-in-dev-console/)
* [如何获取访问权限（角色）](https://developer.adobe.com/uix/docs/guides/get-access/)
* [UI扩展的本地预览](https://developer.adobe.com/uix/docs/guides/preview-extension-locally/)
