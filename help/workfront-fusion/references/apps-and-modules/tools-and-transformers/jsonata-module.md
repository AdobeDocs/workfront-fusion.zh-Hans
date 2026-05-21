---
title: JSONata 模块
description: Adobe Workfront Fusion JSONata连接器提供了一个用于处理JSON格式数据的模块，以便Adobe Workfront Fusion可以进一步处理数据内容。
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
TQID: https://experienceleague.adobe.com/luvZBccaWY5-8muR71o8C82qVROYJvcuAqt3Ol2LZac
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 28%

---

# [!UICONTROL JSONata]模块

Adobe Workfront Fusion [!UICONTROL JSONata]连接器允许您查询JSON对象。 此模块不需要连接。

## 访问权限要求

+++ 展开可查看本文所述功能的访问权限要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 包</td> 
   <td> <p>任意 Adobe Workfront Workflow 包以及任意 Adobe Workfront 自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime 和 Select 包，且需额外购买 Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 许可证</td> 
   <td> <p>标准</p><p>工作版或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

+++



## JSONata模块及其字段

### 评估

此操作模块可查询JSON对象并返回数组。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 表达式]</td> 
   <td>输入要用于计算JSON对象的表达式。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 数据] </td> 
   <td> 输入要计算的JSON对象。  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Stringify输出] </td> 
   <td> 启用此选项可将输出转换为字符串。  </td> 
  </tr> 
  </tbody>
  </table>

>[!BEGINSHADEBOX]

**示例**：

目标是从以下JSON对象返回名称数组：

```JSON
{
  "people": [
    { "name": "Alice", "age": 30 },
    { "name": "Bob", "age": 25 },
    { "name": "Charlie", "age": 35 }
  ]
}
```

1. 在表达式字段中，输入`people.name`。
1. 在数据字段中，输入JSON对象。

模块返回从JSON对象拉取的名称数组。

>[!ENDSHADEBOX]



### JSONata MCP

该操作模块通过分析指定的输入和输出架构生成JSONata表达式。 提供架构，模型上下文协议(MCP)使用这些架构生成将输入转换为输出的表达式。




<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择用于连接到要用于此模块的大型语言模型(LLM)的连接。</p> <p>目前，仅支持Anthropic API密钥。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输入架构]</td> 
   <td> <p>输入或映射要用于此表达式的输入架构。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出架构]</td> 
   <td> <p>输入或映射要用于此表达式的输出架构。</p> </td> 
  </tr> 
 </tbody> 
</table>
