---
title: 模块概述
description: Adobe Workfront Fusion 区分五种模块类型：操作模块、搜索模块、触发器模块、聚合器模块和迭代器模块。聚合器和迭代器模块适用于高级场景。
author: Becky
feature: Workfront Fusion
exl-id: 4c8fe028-8425-426d-a006-f0c66871b3cd
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: ht
source-wordcount: '917'
ht-degree: 100%

---

# 模块概述

Adobe Workfront Fusion 区分以下五种模块类型：

* 操作模块
* 搜索模块
* 触发器模块
* 聚合器
* 迭代器

聚合器和迭代器模块适用于高级场景。

## 操作模块

操作模块是最常见的模块类型。典型的操作模块会执行某项操作并返回一个单一捆绑包，随后交由下一个模块继续处理。

与触发器模块不同，操作模块可放置在场景的开头、中间或结尾。

场景中可包含无限数量的操作模块，但若模块数量过多（150+），可能会影响性能。

>[!BEGINSHADEBOX]

**示例：**

* **Workfront > [!UICONTROL 上传文件]**&#x200B;会将文件上传至 Workfront，并返回其标识符。
* **[!UICONTROL 图像] > [!UICONTROL 调整大小]**&#x200B;接收一张图像，将其调整为指定尺寸，并将调整后的图像传递给下一个操作。

>[!ENDSHADEBOX]

“操作”类型有四个子类型：

* 创建
* 读取
* 更新
* 删除

“更新”子类型包含以下三种操作：

* **擦除字段内容**。当字段内容解析为 `erase` 关键词时（不要与 `empty` 混淆），将执行此操作。

  ![擦除关键词](assets/erase-content-of-field.png)

* **保持字段内容不变**。 当字段留空，或字段内容解析为空（在 JSON 中表示为 null）时，将执行此操作。

  ![空捆绑包](assets/leave-content-field-unchanged.png)

* **替换字段内容**。除上述两种情况外，所有其他情况均会执行此操作。

>[!NOTE]
>
>* 如果在映射面板中未看到 `erase` 关键词，则说明该模块不是更新模块，或尚未更新至该应用的最新规范。
>* `Empty` 不会更改字段内容。如果需要清除字段内容，可以使用以下公式：
>
>   ![如果为空](assets/formula-ifempty-name-erase.png)
>
>* 目前不支持在字段内容解析为空时保持字段内容不变。

## 搜索模块

搜索模块会返回零个、一个或多个捆绑包，并将这些捆绑包传递给下一个模块继续处理。

搜索模块可放置在场景的开头、中间或结尾。

场景中可包含无限数量的搜索模块，但若模块数量过多（150+），可能会影响性能。

>[!BEGINSHADEBOX]

**示例：**

**Workfront > [!UICONTROL 读取相关记录]**&#x200B;会读取在特定父对象中与指定的搜索查询匹配的记录。

>[!ENDSHADEBOX]

## 触发器模块

触发器模块会在某个服务发生变更（例如创建或更新记录）时生成捆绑包。

触发器模块会返回零个、一个或多个捆绑包，并将这些捆绑包传递给下一个模块继续处理。

由于触发器模块会启动场景执行，因此它们只能放置在场景的开头。

每个场景只能包含一个触发器模块。

Workfront Fusion 提供两种触发器模块：轮询触发器和即时触发器。

### 轮询触发器

轮询触发器会定期轮询指定服务，即使自上次场景运行后没有任何变更。我们建议为包含轮询触发器的场景设置定期运行计划。如果存在与触发器配置匹配的变更，触发器将返回包含该变更信息的捆绑包。如果没有与该配置相匹配的变更，则该触发器不会输出任何捆绑包。

有关如何计划场景运行的说明，请参阅[计划场景](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。

轮询触发器会在您保存触发器或更改触发器设置后自动显示一个面板，您可以在其中选择要首先输出的条目。此选择仅影响模块的首次执行。模块首次运行后，后续执行只会监测最近一次执行之后发生的更改。

如需了解更多信息，请参阅[选择触发器模块的起始位置](/help/workfront-fusion/create-scenarios/add-modules/choose-where-trigger-module-starts.md)。

>[!BEGINSHADEBOX]

**示例：**

* **Workfront > [!UICONTROL 监控记录]**&#x200B;会返回自上次运行该场景后新增的记录。

* **[!DNL Google Sheets]> [!UICONTROL 监控行]**&#x200B;会返回自上次运行该场景后新增的行。

>[!ENDSHADEBOX]

### 即时触发器

即时触发器可在服务发生更改后立即通知 Workfront Fusion。我们建议将包含即时触发器的场景设置为立即运行。

有关操作步骤，请参阅[计划场景](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。

关于即时触发器如何处理传入数据的详细信息，请参阅[即时触发器 (Webhook)](/help/workfront-fusion/references/modules/webhooks-reference.md)。

>[!BEGINSHADEBOX]

**示例：**

* **Workfront > [!UICONTROL 监控事件]**&#x200B;会在 Workfront 中发生特定事件（例如创建任务）时返回相关信息。
* **[!DNL Google Sheets]> [!UICONTROL 监控更改]**&#x200B;会在单元格更新时返回相关信息。

>[!ENDSHADEBOX]

## 聚合器

聚合器模块会将多个捆绑包汇总为单个捆绑包。

聚合器仅返回一个捆绑包，该捆绑包随后会传递给下一个模块继续处理。

聚合器只能放置在场景的中间位置。

场景中可包含无限数量的聚合器，但若模块数量过多（150+），可能会影响性能。

>[!BEGINSHADEBOX]

**示例：**

* **[!UICONTROL 存档] > [!UICONTROL 创建存档]**&#x200B;会将多个文件压缩成 zip 存档。
* **[!UICONTROL CSV] > [!UICONTROL 聚合到 CSV]** 会将 CSV 文件中的多个字符串合并为一行。
* **[!UICONTROL 工具] > [!UICONTROL 文本聚合器]**&#x200B;会将多个字符串合并为一个字符串。

>[!ENDSHADEBOX]

如需了解更多信息，请参阅[聚合器模块](/help/workfront-fusion/references/modules/aggregator-module.md)。

## 迭代器

迭代器是一种将数组拆分为多个独立捆绑包的模块。

迭代器会返回一个或多个捆绑包，然后传递给下一个模块进行处理。

迭代器只能放置在场景的中间位置。

场景中可包含无限数量的迭代器，但若模块数量过多（150+），可能会影响性能。

>[!BEGINSHADEBOX]

**示例：**

**[!UICONTROL 电子邮件] > [!UICONTROL 检索附件]**&#x200B;会将附件数组拆分为多个独立捆绑包。

>[!ENDSHADEBOX]

如需了解更多信息，请参阅[迭代器模块](/help/workfront-fusion/references/modules/iterator-module.md)和[映射数组](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md)。
