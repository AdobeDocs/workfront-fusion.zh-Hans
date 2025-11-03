---
title: JSONata模块
description: Adobe Workfront Fusion JSONata连接器提供了一个用于处理JSON格式数据的模块，以便Adobe Workfront Fusion可以进一步处理数据内容。
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# [!UICONTROL JSONata]模块

Adobe Workfront Fusion [!UICONTROL JSONata]连接器允许您查询JSON对象。 此模块不需要连接。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何Adobe Workfront Workflow包和任何Adobe Workfront自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime和Select包，以及额外购买的Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>标准</p><p>工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果贵组织具有不包含Workfront Automation and Integration的Select或Prime Workfront包，则贵组织必须购买Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

+++



## JSONata模块及其字段

### 评估

此操作模块可查询JSON对象并返回数组。

<table style="table-layout:auto"> 
 <col data-mc-conditions=""> 
 <col data-mc-conditions=""> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL表达式]</td> 
   <td>输入要用于计算JSON对象的表达式。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL数据] </td> 
   <td> 输入要计算的JSON对象。  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Stringify输出] </td> 
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
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择用于连接到要用于此模块的大型语言模型(LLM)的连接。</p> <p>目前，仅支持Anthropic API密钥。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入架构]</td> 
   <td> <p>输入或映射要用于此表达式的输入架构。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出架构]</td> 
   <td> <p>输入或映射要用于此表达式的输出架构。</p> </td> 
  </tr> 
 </tbody> 
</table>
