---
title: 数学变量
description: 以下数学变量在 [!DNL Adobe Workfront Fusion mapping] 面板中可用。
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 0%

---

# 数学变量

## pi

表示数学符号$\pi$。

## [!UICONTROL random]

返回范围[`0`，`1`]中的浮点伪随机数（包括`0`但不包括`1`）。

使用以下公式生成范围[`min`，`max`]中的整数伪随机数（包括`min`和`max`）：

![随机](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
