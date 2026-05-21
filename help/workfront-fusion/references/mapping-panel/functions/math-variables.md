---
title: 数学变量
description: 以下数学变量在 [!DNL Adobe Workfront Fusion mapping] 面板中可用。
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
TQID: https://experienceleague.adobe.com/7vPwofVyFGdTGAXXuqbP5mmpPgSEK0JqimFqWu-UlJU
product_v2: id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 52
ht-degree: 11%

---

# 数学变量

## pi

表示数学符号$\pi$。

## [!UICONTROL random]

返回范围[`0`，`1`]中的浮点伪随机数（包括`0`但不包括`1`）。

使用以下公式生成范围[`min`，`max`]中的整数伪随机数（包括`min`和`max`）：

![Random](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
