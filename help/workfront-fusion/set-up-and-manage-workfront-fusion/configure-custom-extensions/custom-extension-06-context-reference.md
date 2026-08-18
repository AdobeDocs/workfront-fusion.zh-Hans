---
product-previous: workfront-fusion
product-area: workfront-integrations
keywords: Fusion
navigation-topic: workfront-fusion-navigation-topic
title: Fusion上下文引用
description: Fusion上下文引用
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: bbc94bb0-7432-44c5-8000-9aea25916b28
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2: id: f48b5020-b9cd-4d99-bc6e-42c35e90c1f8
source-git-commit: a9dd86f7dc4070ad98c7c4a526a6a38939097940
workflow-type: tm+mt
source-wordcount: 757
ht-degree: 8%

---

# Fusion上下文引用

>[!NOTE]
>
>本文假定您对软件开发工具有一定的了解。

当您的UI调用`attach(...)`时，Fusion共享一个描述当前会话的&#x200B;**上下文**&#x200B;对象。 此页面列出了每个字段、其含义以及Fusion和Adobe IMS标识符的关系。

## 如何阅读上下文

* **初始值：** `connection.sharedContext.get("<key>")`
* **更新：**&#x200B;收听`contextchange`事件。 最新对象到达`event.detail.context`。

有关完整的代码模式，请参阅[构建自定义扩展UI](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-05-build-ui-procedure.md)。

```js
const organization = connection.sharedContext.get("organization");
const fusionOrgId  = organization?.id;        // Fusion's organization id
const imsOrgId     = connection.sharedContext.get("imsOrgId"); // Adobe IMS org id
```

## 顶级键

| 键 | 类型 | 描述 |
| ----- | ------ | ------------- |
| `imsToken` | 字符串 | 登录用户的Adobe **IMS访问令牌**。 将此令牌用作`Bearer`令牌，以代表用户调用Adobe或Fusion API。 **由于这是敏感信息，因此从不记录或显示它。** |
| `imsOrgId` | 字符串 | Adobe **IMS组织ID**，格式为`XXXXXXXXXXXX@AdobeOrg`。 |
| `imsUserId` | 字符串 | 登录用户的Adobe **IMS用户ID**。 |
| `organization` | 对象 | **完全活动的Fusion组织** 有关详细信息，请参阅本文中的[`organization`字段](#organization-fields)。 |
| `team` | 对象\|未定义 | **完全活动的Fusion团队**，当一个团队处于活动状态时（始终与`fusion/nav-team/1`相关）。 有关详细信息，请参阅本文中的[`team`字段](#team-fields)。 |
| `user` | 对象 | **完全登录的Fusion用户**。 有关详细信息，请参阅本文中的[`user`字段](#user-fields)。 |

### Fusion ID和IMS ID

每个实体都有一个&#x200B;**Fusion ID**（由Fusion自己的API使用），如果存在，则有一个&#x200B;**Adobe IMS ID**（由Adobe平台API使用）：

| 实体 | 融合ID | Adobe IMS ID |
| -------- | ----------- | -------------- |
| 组织 | `organization.id` | `imsOrgId` （也公开为`organization.externalOrgId`） |
| 团队 | `team.id` | *（团队仅限Fusion；无IMS ID）* |
| 用户 | `user.id` | `imsUserId` |

## `organization`字段

这些字段可在活动组织记录中找到。 大多数扩展仅需要`id`、`name`和标识符。

| 字段 | 类型 | 描述 |
| ------- | ------ | ------------- |
| `id` | 字符串 | 融合组织ID。 |
| `name` | 字符串 | 组织显示名称 |
| `externalOrgId` | 字符串 | Adobe IMS组织ID （与`imsOrgId`的值相同）。 |
| `externalId` | 字符串 | Fusion集成使用的外部标识符 |
| `countryId` | 字符串 | 国家/地区设置ID。 |
| `timezoneId` | 字符串 | 时区设置标识 |
| `serviceName` | 字符串 | 服务/计划标识符 |
| `teamIds` | 字符串[] | 此组织中团队的ID |
| `license` | 对象 | 计划限制和权利，如操作、数据传输、用户名额和功能标记 |
| `scenariosCount` | 数字 | 组织中的方案总数 |
| `activeScenarios` | 数字 | 当前活动方案 |
| `activeApps` | 数字 | 活动应用程序或连接的数量 |
| `operations`, `operationsExt` | 数字 | 操作使用情况计数器 |
| `transfer`, `transferExt` | 数字 | 数据传输使用计数器 |
| `isPaused` | 布尔 | 是否暂停组织 |
| `isDeleted` | 布尔 | 组织是否标记为已删除 |
| `imsEnabled` | 布尔 | 组织是否已链接到Adobe IMS |
| `usersCount` | 数字 | 组织中的用户数 |
| `nextReset` | 字符串（日期） | 下次重置使用计数器时。 查看[日期](#dates) |

## `team`字段

当团队处于活动状态时，将显示这些字段。 如果团队为`undefined`，则必须提供后备（例如，在未选择团队的组织级别屏幕上）。

| 字段 | 类型 | 描述 |
| ------- | ------ | ------------- |
| `id` | 字符串 | Fusion团队ID。 |
| `name` | 字符串 | 团队显示名称。 |
| `organizationId` | 字符串 | 此团队所属组织的融合ID。 |
| `country` | 字符串 | 团队国家设置。 |
| `timezone` | 字符串 | 团队时区。 |
| `license` | 对象 | 团队级别的限制和权利。 |
| `activeScenarios` | 数字 | 团队中的活动场景。 |
| `activeApps` | 数字 | 团队中的活动应用程序或连接。 |
| `scenarioDrafts` | 布尔 | 方案草稿是否已启用。 |
| `isDeleted` | 布尔 | 团队是否标记为已删除。 |
| `created` | 字符串（日期） | 创建团队的时间。 查看[日期](#dates)。 |

## `user`字段

这些字段适用于已登录的Fusion用户。

| 字段 | 类型 | 描述 |
| ------- | ------ | ------------- |
| `id` | 字符串 | 融合用户ID。 |
| `name` | 字符串 | 全名。 |
| `email` | 字符串 | 电子邮件地址。 |
| `avatar` | 字符串 | 头像图像URL。 |
| `locale` | 字符串 | 用户区域设置，如`en`。 |
| `language` | 字符串 | 首选语言（设置时）。 |
| `timezone` | 字符串 | 时区名称。 |
| `timezoneId` | 字符串 | 时区设置ID |
| `countryId` | 字符串 | 国家/地区设置ID。 |
| `localeId` | 字符串 | 区域设置标识。 |
| `features` | 对象 | 每个用户的功能标志（例如`allow_apps`，`public_templates`）。 |
| `usersAdminsRoleId` | 字符串 | 用户的管理员角色ID（如果适用）。 |

>[!NOTE]
>
> `user`对象可能包含其他内部字段。 您应仅依赖此处记录的字段。 其他字段可以不经通知而更改，并且某些与身份验证相关的字段不得记录或显示。

## 日期

上下文在到达扩展之前已序列化，因此&#x200B;**日期字段以字符串** （ISO 8601，如`"2026-06-24T00:00:00.000Z"`）形式到达，而不是JavaScript `Date`对象。 如果需要，您可以转换这些字段：

```js
const resetDate = new Date(context.organization.nextReset);
```

## 上下文更新

Fusion在以下情况下重新发送整个上下文（通过`contextchange`）：

* 用户&#x200B;**切换组织**，
* 用户&#x200B;**切换组**，或
* **登录用户的**&#x200B;信息已更改。

始终重新读取`contextchange`处理程序中使用的所有键，而不是假定只更改了一个值。

## 安全最佳实践

* **从不记录、显示或保留`imsToken`。** 把它当做密码。
* 仅将该令牌作为`Bearer`令牌通过HTTPS发送到受信任的Adobe/Fusion端点。
* 请勿存储超出功能所需上下文的个人数据。

## 使用令牌调用API

要将`imsToken` （加`organization.id` / `team.id`）转换为真正的Workfront或
对于融合数据，您无法直接从浏览器调用这些API，因为CORS会阻止调用
它。 改为通过小型App Builder运行时操作路由调用。 请参阅
[正在调用Workfront和Fusion API](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-10-calling-apis.md)。


要继续创建自定义扩展的过程，请参阅[发布您的扩展](/help/workfront-fusion/set-up-and-manage-workfront-fusion/configure-custom-extensions/custom-extension-07-publish.md)。
