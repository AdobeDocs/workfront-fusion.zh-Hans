---
title: 模块概述
description: Adobe Workfront Fusion区分了五种类型的模块：操作模块、搜索模块、触发器模块、聚合器和迭代器。 聚合器和迭代器适用于高级方案。
author: Becky
feature: Workfront Fusion
exl-id: 4c8fe028-8425-426d-a006-f0c66871b3cd
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 0%

---

# 模块概述

Adobe Workfront Fusion将模块分为五种类型：

* 操作模块
* 搜索模块
* 触发器模块
* 汇总
* 迭代器

聚合器和迭代器适用于高级方案。

## 操作模块

操作模块是最常见的模块类型。 典型操作模块会执行操作并返回单个捆绑，然后将其传递到下一个模块进行处理。

与触发器模块不同，操作模块可以放置在方案的开头、中间或结尾。

场景可以包含无限数量的操作模块，尽管大量模块（150个以上）可能会影响性能。

>[!BEGINSHADEBOX]

**示例：**

* **[!DNL Workfront]>[!UICONTROL Upload a file]**&#x200B;向[!DNL Workfront]发送文件并返回其标识符。
* **[!UICONTROL Image]>[!UICONTROL Resize]**&#x200B;接收图像，将其大小调整为指定尺寸，然后将调整大小的图像传递到下一个操作。

>[!ENDSHADEBOX]

“操作”类型有四个子类型：

* 创建
* 读取
* 更新
* 删除

Update子类型包含以下三个操作：

* **擦除字段**&#x200B;的内容。 当字段的内容被计算为`erase`关键字（不要与`empty`混淆）时，将发生此操作。

  ![擦除关键字](assets/erase-content-of-field.png)

* **字段的内容保持不变**。 当字段留空或字段内容计算为空（在JSON中通过null表示）时，会发生此操作。

  ![空包](assets/leave-content-field-unchanged.png)

* **替换字段**&#x200B;的内容。 除上述两种情况外，此操作还会发生在所有其他情况下。

>[!NOTE]
>
>* 如果您在映射面板中未看到`erase`关键字，则该模块不是更新模块，或者未更新为应用程序的最新规范。
>* `Empty`不更改字段内容。 如果必须拭除该字段，可以使用以下公式：
>
>   ![如果为空](assets/formula-ifempty-name-erase.png)
>
>* 当前不支持在内容评估为空时保持字段不变。

## 搜索模块

搜索模块返回零、一个或多个包，然后传递给下一个模块进行处理。

您可以将搜索模块放置在方案的开头、中间或结尾。

场景可以包含无限数量的搜索模块，尽管大量模块（150个以上）可能会影响性能。

>[!BEGINSHADEBOX]

**示例：**

**[!DNL Workfront]>[!UICONTROL Read Related Records]**&#x200B;读取在特定父对象中与指定的搜索查询匹配的记录。

>[!ENDSHADEBOX]

## 触发器模块

当给定服务发生更改（例如创建或更新记录）时，触发器将生成捆绑包。

触发器返回零、一个或多个包，然后传递给下一个模块进行处理。

由于触发器会导致方案开始执行，因此它们只能置于方案的开头。

每个方案只能包含一个触发器。

[!DNL Workfront Fusion]使用两种类型的触发器：轮询触发器和即时触发器。

### 轮询触发器

轮询触发器会定期轮询给定服务，即使自上次方案运行以来没有发生任何更改。 我们建议您安排包含轮询触发器的方案定期运行。 如果存在与触发器配置匹配的更改，触发器将返回包含有关更改信息的包。 如果没有与配置匹配的更改，则触发器不会输出任何包。

有关计划方案的说明，请参阅[计划方案](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。

轮询触发器允许您选择它们应通过面板输出的第一个捆绑包，该面板会在您保存触发器或更改触发器设置后自动显示。 此选择仅影响模块的第一次执行。 模块执行一次后，后续执行仅会监视最近执行后发生的更改。

有关详细信息，请参阅[选择触发器模块的启动位置](/help/workfront-fusion/create-scenarios/add-modules/choose-where-trigger-module-starts.md)。

>[!BEGINSHADEBOX]

**示例：**

* **[!DNL Workfront]>[!UICONTROL Watch records]**&#x200B;返回上次运行方案后新添加的记录。

* **[!DNL Google Sheets]>[!UICONTROL Watch Rows]**&#x200B;返回上次运行方案后添加的新行。

>[!ENDSHADEBOX]

### 即时触发器

即时触发器使服务能够在更改发生后立即通知[!DNL Workfront Fusion]。 我们建议您安排一个包含即时触发器的方案立即运行。

有关说明，请参阅[计划方案](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。

有关即时触发器如何处理传入数据的详细信息，请参阅[即时触发器(webhook)](/help/workfront-fusion/references/modules/webhooks-reference.md)。

>[!BEGINSHADEBOX]

**示例：**

* 在Workfront中发生特定类型的事件（如创建任务）时，**[!DNL Workfront]>[!UICONTROL Watch Events]**&#x200B;会返回信息。
* 更新单元格时，**[!DNL Google Sheets]>[!UICONTROL Watch Changes]**&#x200B;会返回信息。

>[!ENDSHADEBOX]

## 汇总

聚合器模块将多个捆绑累积到单个捆绑中。

聚合器仅返回一个捆绑包，该捆绑包随后将传递到下一个模块以供进一步处理。

只能将聚合放置在场景的中间位置。

场景可以包含无限数量的聚合器，尽管大量模块（150个以上）可能会影响性能。

>[!BEGINSHADEBOX]

**示例：**

* **[!UICONTROL Archive]>[!UICONTROL Create an archive]**&#x200B;将多个文件压缩为zip存档。
* **[!UICONTROL CSV]>[!UICONTROL Aggregate to CSV]**&#x200B;将CSV文件中的多个字符串合并到一行中。
* **[!UICONTROL Tools]>[!UICONTROL Text aggregator]**&#x200B;将多个字符串组合为一个字符串。

>[!ENDSHADEBOX]

有关详细信息，请参阅[聚合器模块](/help/workfront-fusion/references/modules/aggregator-module.md)。

## 迭代器

迭代器是一种将数组拆分为单独捆绑包的模块。

迭代器返回一个或多个包，然后传递给下一个模块进行处理。

只能将迭代器放置在场景的中间位置。

方案可以包含无限数量的迭代器，但大量模块（150个以上）可能会影响性能。

>[!BEGINSHADEBOX]

**示例：**

**[!UICONTROL Email]>[!UICONTROL Retrieve attachments]**&#x200B;将附件数组分解为单独的包。

>[!ENDSHADEBOX]

有关详细信息，请参阅[迭代器模块](/help/workfront-fusion/references/modules/iterator-module.md)和[映射数组](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md)。
