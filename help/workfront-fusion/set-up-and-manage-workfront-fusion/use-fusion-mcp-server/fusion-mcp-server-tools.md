---
title: Adobe Workfront Fusion MCP服务器工具
description: Adobe Workfront Fusion MCP服务器向AI代理平台和同事公开的工具的参考列表。
source-git-commit: 5f3bd6b7b8837632af245ea2c172205625e4ecba
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 7%
---

# Adobe Workfront Fusion MCP服务器工具


本文列出了Adobe Workfront Fusion MCP服务器向连接的AI代理公开的工具。 当您要求代理查找、检查、创建、运行、更新或删除Fusion项目时，代理会代表您调用这些工具。

每个受支持的界面中都提供了相同的工具：Claude、ChatGPT、Copilot或您自己的代理中的自定义MCP连接；以及Fusion右边栏中的独立和Co-worker。 有关设置，请参阅[配置Adobe Workfront Fusion MCP服务器](configure-fusion-mcp-server.md)。

代理使用您的Adobe ID、Fusion组织角色和团队角色在Fusion中执行操作。 只有在Fusion中具有相应的权限时，工具才有效。 Adobe对代理对您的Fusion数据所做的更改不承担任何责任。

## 读取和写入操作

每项工具均分类为：

* **读取**：检索信息而不更改任何内容，例如列出方案或获取执行。
* **写入**：创建、更改、运行或删除Fusion数据，例如克隆场景或清除webhook队列。

## 组织工具

活动组织适用于当前会话中的所有其他工具。

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 列出组织 | `fusion_orgs_list` | 读取 | 列出您可以访问的Fusion组织，包括ID、区域（区域）和标签。 |
| 设置活动组织 | `fusion_orgs_set` | 会话 | 切换当前会话的活动组织。 不更改任何Fusion数据。 |

## 场景工具

### 场景

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 列出方案 | `fusion_scenarios_list` | 读取 | 列出组织中的方案。 |
| 获取方案 | `fusion_scenarios_get` | 读取 | 返回方案，包括其完整的Blueprint。 |
| 获取方案依赖关系 | `fusion_scenarios_getDependencies` | 读取 | 返回连接、键、数据存储、数据结构和Webhook方案的蓝图引用。 |
| 查找相关方案 | `fusion_scenarios_dependents` | 读取 | 查找引用给定webhook、数据存储、数据结构、连接、键或方案的方案。 在更改或删除资源之前进行影响分析很有用。 |
| 验证Blueprint | `fusion_scenarios_validate_blueprint` | 读取 | 从结构上验证团队的Blueprint（模块引用、连接、必填字段），而不保存任何内容。 |
| 创建方案 | `fusion_scenarios_create` | 写入 | 从Blueprint在团队中创建方案，其中包含可选名称、描述、文件夹、计划和顺序处理。 |
| 克隆方案 | `fusion_scenarios_clone` | 写入 | 将方案克隆到同一组或不同组。 跨团队进行克隆时，可以将每个连接、webhook、数据存储、数据结构和键映射到目标资源。 （可选）从上次处理的记录继续。 |
| 更新方案 | `fusion_scenarios_update` | 写入 | 更改名称、描述、文件夹、计划或活动状态（激活/停用）。 还可以恢复已删除的方案。 |
| 运行场景一次 | `fusion_scenarios_execute` | 写入 | 运行场景一次，并等待（最长超时）结果并返回状态和任何错误消息。 即时（webhook触发）方案不支持。 |
| 删除方案 | `fusion_scenarios_delete` | 写入 | 删除方案。 删除的方案可以使用&#x200B;**更新方案**&#x200B;恢复。 |

示例提示：

* _营销团队中的哪些活动方案在6个月内未编辑？_
* _“→Workfront同步”方案使用哪些连接？_
* _将“潜在客户引入”克隆到Sales团队并在Sales Salesforce连接中进行交换。_
* _在我导入此Blueprint之前对其进行验证。_
* _运行一次“夜间报告”，并告诉我是否成功。_

### 方案版本

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 列出方案版本 | `fusion_scenario_versions_list` | 读取 | 列出方案的已保存版本。 按`version`、`createdAt`、`comment`筛选。 |
| 获取方案版本 | `fusion_scenario_versions_get` | 读取 | 返回特定版本的Blueprint和元数据。 |

示例提示：

* _此方案的版本12和版本14之间发生了什么变化？_

### 文件夹

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 列出文件夹 | `fusion_folders_list` | 读取 | 列出方案文件夹，其中包含方案计数。 |
| 创建文件夹 | `fusion_folders_create` | 写入 | 在团队中创建文件夹。 |
| 重命名文件夹 | `fusion_folders_update` | 写入 | 重命名文件夹。 |
| 删除文件夹 | `fusion_folders_delete` | 写入 | 删除文件夹。 |

## 执行工具

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 列出执行 | `fusion_executions_list` | 读取 | 列出场景或不完整执行的执行。 按`status`筛选（例如`status==3`错误，`status==2`警告），`timestamp`，`duration`，`bundles`，`operations`，`transfer`。 （可选）包括检查运行。 |
| 获取执行 | `fusion_executions_get` | 读取 | 返回单个执行以及有关其方案或不完整执行的元数据。 |

示例提示：

* _向我显示昨天失败的“发票同步”运行并总结错误。_
* _此方案的哪个执行使用了本周最多的操作？_

## 操作（使用）工具

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 获取操作 | `fusion_operations_get` | 读取 | 返回最多1年的日期范围的操作时间序列（按天或月）。 按团队、方案或包过滤；按模块、包、方案或团队分组。 |
| 获取操作摘要 | `fusion_operations_summary_by_org` | 读取 | 返回日期范围内每个方案和团队的总操作数以及总操作数。 |

示例提示：

* _上个月按操作排列的前10个方案。_
* _Salesforce应用程序在第3季度使用了多少操作？_

## 连接和关键工具

这些工具仅返回元数据。 它们不会返回凭据、令牌或机密值。

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 搜索连接 | `fusion_connections_search` | 读取 | 列出连接。 按`name`、`accountName`、`accountType`、`expire`、`teamId`、`scopesCount`、`editable`、`environmentType`、`authenticationType`筛选。 |
| 获取连接 | `fusion_connections_get` | 读取 | 返回单个连接的详细信息。 |
| 搜索键 | `fusion_keys_search` | 读取 | 列出键。 按`name`、`typeName`、`teamId`筛选。 |
| 获取密钥 | `fusion_keys_get` | 读取 | 返回单个键的详细信息。 |

示例提示：

* _哪些连接将在接下来的30天后过期，以及哪些场景使用它们？_

## Webhook工具

### Webhook

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 列出Webhook | `fusion_hooks_list` | 读取 | 列出Webhook（挂钩）。 按`name`、`teamId`、`type`、`enabled`、`gone`、`typeName`、`scenarioId`、`priority`、`detached`等筛选。 |
| 获取webhook | `fusion_hooks_get` | 读取 | 返回webhook的配置、所有者绑定和外部引用。 |
| 查找依赖的Webhook | `fusion_hooks_dependents` | 读取 | 查找引用给定连接的Webhook。 |

### Webhook队列

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | -------- | --- |
| 获取队列统计信息 | `fusion_queue_stats` | 读取 | 返回已排队事件的数量、队列限制以及webhook是否已启用。 |
| 列出队列 | `fusion_queue_list` | 读取 | 列出等待处理的webhook事件。 |
| 获取队列项目 | `fusion_queue_get` | 读取 | 返回单个排队的事件，包括其已解码的有效负载。 |
| 删除队列项目 | `fusion_queue_delete` | 写入 | 删除特定排队的事件（最多50个）或清除队列，可以选择排除某些事件。 无法删除当前处理的事件。 |

示例提示：

* _是否正在备份“表单提交” webhook？_
* _显示排队时间最长的事件的有效负载。_

## 数据存储和数据结构工具

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 列出数据存储 | `fusion_datastores_list` | 读取 | 列出具有记录计数、大小和最大大小的数据存储。 |
| 获取数据存储 | `fusion_datastores_get` | 读取 | 返回数据存储的元数据和用法、链接的数据结构和严格验证设置。 |
| 列出数据存储记录 | `fusion_data_list` | 读取 | 使用偏移分页从数据存储中读取记录（键+ JSON数据）。 |
| 查找相关数据存储 | `fusion_datastores_dependents` | 读取 | 查找使用给定数据结构的数据存储。 |
| 搜索数据结构 | `fusion_data_structures_search` | 读取 | 列出数据结构。 按`name`、`strict`、`teamId`筛选。 |
| 获取数据结构 | `fusion_data_structures_get` | 读取 | 返回数据结构，包括其完整字段规范。 |

示例提示：

* _哪些数据存储已占用80%以上？_
* _显示“客户地图”数据存储中的前20条记录。_

## 活动日志工具

| 工具 | 名称 | 操作 | 描述 |
| --- | --- | --- | --- |
| 列出活动日志 | `fusion_activity_logs_list` | 读取 | 列出组织的审核事件（谁执行了什么操作、对哪个实体执行了什么操作、何时执行）。 按`entity` （例如`scenario`、`connection`、`webhook`、`data store`、`user`）、`action` （例如`created`、`deleted`、`updated`、`transferred ownership`）、用户、团队和时间戳进行筛选。 |
| 导出活动日志 | `fusion_activity_logs_export` | 读取 | 使用相同的过滤器将活动日志导出为CSV或XLSX。 |

示例提示：

* _过去7天内谁删除了方案？_
* _将本季度的所有连接更改导出到Excel。_

## 同事

本文中的所有工具均以协作方式提供，包括独立工具和Fusion右边栏工具，具体取决于相同的读/写设置和您的权限。

## 如何更新工具

当Adobe发布新版本的Fusion MCP服务器时，连接的代理会自动选取更新的工具集。 您无需重新连接。


