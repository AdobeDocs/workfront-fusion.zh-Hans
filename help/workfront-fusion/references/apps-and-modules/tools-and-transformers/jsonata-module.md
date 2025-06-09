---
title: JSONata模块
description: Adobe Workfront Fusion JSONata连接器提供了一个用于处理JSON格式数据的模块，以便Adobe Workfront Fusion可以进一步处理数据内容。
author: Becky
feature: Workfront Fusion
exl-id: 8c117ecb-3c05-47d4-a629-18dbc546e2a2
source-git-commit: da3bf98f8254228598372fed8c06d6318718721f
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---

# [!UICONTROL JSONata]模块

[!DNL Adobe Workfront Fusion] [!UICONTROL JSONata]连接器允许您查询JSON对象。 此模块不需要连接。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证</td> 
   <td> <p>新文档： [!UICONTROL Standard]</p><p>或</p><p>当前： [!UICONTROL Work]或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版：任意 </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Workfront]计划：您的组织必须购买[!DNL Adobe Workfront Fusion]。</li><li>已包含[!UICONTROL Ultimate] [!DNL Workfront]计划： [!DNL Workfront Fusion]。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买[!DNL Adobe Workfront Fusion]。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

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
   <td role="rowheader">[!UICONTROL Connection]</td> 
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
