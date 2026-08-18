---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: 设置UI扩展工具和帐户
description: 设置UI扩展工具和帐户
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 500
ht-degree: 0%

---


# 设置UI扩展工具和帐户

在为Workfront Fusion创建UI扩展之前，必须设置工具和帐户。 只需执行一次。

>[!NOTE]
>
>本文假定您对软件开发工具有一定的了解。

<!--Access requirements-->

## 先决条件

要设置UI可扩展性工具和帐户，您需要以下各项：

* **有权访问Adobe组织的Adobe ID**。 这是用于登录到Fusion的帐户。
* **开发人员对App Builder的访问权限。** 您的组织管理员可能需要向您授予&#x200B;**开发人员**&#x200B;角色，并将您添加到包含App Builder的&#x200B;**产品配置文件**。 如果以后命令失败，显示为“您不是开发人员”或无法看到您的组织，请让您的Adobe组织管理员添加您。
* **系统管理员** <!--Adobe? Fusion?-->（可能是您团队中的其他人）完成最终发布步骤。 创建和部署只需要开发人员角色，但&#x200B;**提交扩展以供审批/发布需要系统管理员角色**。

  有关Adobe访问级别的详细信息，请参阅
  在Adobe文档中[如何获取访问权限](https://developer.adobe.com/uix/docs/guides/get-access/)。

* **可以安装软件**&#x200B;并运行终端命令（macOS、Windows或Linux）的计算机。

## 安装节点.js

Adobe工具在&#x200B;**Node.js**&#x200B;上运行。 您必须安装&#x200B;**LTS**&#x200B;版本（18或20）。

1. 转到<https://nodejs.org>并下载&#x200B;**LTS**&#x200B;安装程序。
1. 运行安装程序并接受默认值。
1. 打开终端并运行以下命令，确认此功能正常工作：

   ```sh
   node --version
   npm --version
   ```

   您应该会看到版本号（例如`v20.17.0`和`10.x`）。

1. （视情况而定）如果未找到`node`，请关闭并重新打开终端，或重新启动计算机。

1. 继续[安装Adobe I/O CLI (`aio`)](#install-the-adobe-io-cli-aio)。

>[!TIP]
>
>* 如果使用多个节点版本，则版本管理器（如`nvm`）很方便，但它是可选的。
>* Adobe CLI需要Node 18或更高版本。 非常新的非LTS版本偶尔会导致问题，因此我们建议使用LTS。

## 安装Adobe I/O CLI (`aio`)

用于创建、生成和发布扩展的命令行工具名为`aio`。

要全局安装，请执行以下操作：

1. 在命令行中使用以下`npm`命令。

   ```sh
   npm install -g @adobe/aio-cli
   ```

1. 使用以下命令确认安装了该软件：

   ```sh
   aio --version
   ```

   您应会看到`@adobe/aio-cli/11.x.x`之类的内容。

1. 继续[登录到Adobe](#sign-in-to-adobe)。

>[!NOTE]
>
> 如果您在macOS/Linux上看到权限错误，请&#x200B;**不**&#x200B;使用`sudo`。 请改为修复npm的全局文件夹权限，或使用安装在主目录中的Node版本管理器。

## 登录到Adobe

1. 使用以下命令将CLI连接到您的Adobe帐户：

   ```sh
   aio login
   ```

1. 在打开的浏览器窗口中，使用您的Adobe ID登录并审批访问权限。

1. 登录成功后，关闭浏览器选项卡并返回终端。

1. （可选）要稍后注销（例如切换帐户），请使用命令： `aio logout`。
1. 继续[确认您的活动组织](#confirm-your-active-organization)。

## 确认您的活动组织

检查CLI指向哪个组织：

```sh
aio console org list      # see organizations you can use
aio console where         # see your currently selected org/project/workspace
```

如果您属于多个组织，请选择正确的组织：

```sh
aio console org select
```

您现在可以创建项目。
