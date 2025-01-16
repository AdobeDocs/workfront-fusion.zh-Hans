---
title: 映射概述
description: 映射是将模块的输出（按项目结构）分配给其他模块的输入字段的过程。
author: Becky
feature: Workfront Fusion
exl-id: 9208ce20-0757-427a-9669-ce4274d05522
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---

# 映射概述

映射是将模块的输出分配给其他模块的输入字段的过程。

模块的操作将生成零、一个或多个捆绑作为其输出。 捆绑包由一个或多个项目组成。

您可以将这些项目映射到以后模块中的字段。

单击可在其中插入从场景的前一个模块输出的值的字段时，将显示映射面板。 在这里，您可以选择要映射的项目。 映射可以包括以下一项或多项：

* 单个项目
* 多个项目
* 静态文本
* 函数

>[!BEGINSHADEBOX]

**示例**：

单个项目

![](assets/map-single.png)

包含文本的多个项目

![](assets/map-multiple-with-text.png)

包含多个项目和文本的函数

![](assets/map-formula-with-text.png)


>[!ENDSHADEBOX]


有关映射的说明，请参阅[映射数据：项目索引](/help/workfront-fusion/create-scenarios/map-data/map-data-toc.md)下的项目。

>[!NOTE]
>
>封装在[!UICONTROL Iterator]和[!UICONTROL Aggregator]之间的模块的输出无法在[!UICONTROL Aggregator]模块之外访问。

## 映射面板

在可以映射数据的字段中单击后，将打开映射面板。

第一个选项卡![](assets/toolbar-icon-functions-you-map-from-other-modules.png)显示可从其他模块映射的项目。

其他选项卡包括可用于创建公式的函数、运算符和关键字。 根据它们处理的数据类型，这些报告会被分类为不同的选项卡。

![](assets/mapping-panel-blank.png)


有关函数选项卡的详细信息，请参阅[函数概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/function-overview.md)。

有关使用函数映射项的更多信息，请参阅[使用函数映射项](/help/workfront-fusion/create-scenarios/map-data/map-using-functions.md)。

## 集合

项可以包含多种类型的多个值。 这些是收藏集类型的项目。

集合类型捆绑包在模块输出中捆绑包标签旁显示`(Collection)`。

![](assets/collection.png)

在大多数情况下，您可以映射收藏集的元素，而不是映射代表整个收藏集的项。

要在映射面板中定位收藏集的元素，请单击收藏集旁边的箭头。

![](assets/collection-dropdown.png)

有关集合的详细信息，请参阅[项目数据类型](/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md)。

有关映射集合的说明，请参阅“将信息从一个模块映射到另一个模块”文章中的[映射项](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md#map-an-item)。

## 数组

项可以包含相同类型的多个值。 这些是数组类型的项。

数组类型捆绑包在模块输出中捆绑包标签旁显示`(Array)`。

在映射面板中，数组以方括弧显示。 您可以通过项目标签末尾的方括号来标识数组类型项目。 要在映射面板中定位特定的数组元素，请单击数组旁边的箭头。

![](assets/array.png)

有关映射数组和数组元素的信息和说明，请参阅[映射数组和数组元素](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md)。
