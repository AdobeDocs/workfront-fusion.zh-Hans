---
title: SOAP 模块
description: 您可以使用SOAP模块连接到Adobe Workfront Fusion中的SOAP API。
author: Becky
feature: Workfront Fusion
exl-id: dbcc04f8-8306-4a81-aed8-1ce0798e145f
TQID: https://experienceleague.adobe.com/MIMXln44-LWfrQf0w-lZXfZJ3020Flty2CgwSC3JI9c
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
feature_v2:
  - id: b58ad82f-df6b-4b01-81a3-3a02ab9567a0
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 647
ht-degree: 27%

---

# [!UICONTROL SOAP]模块

您可以使用[!UICONTROL SOAP]模块连接到[!UICONTROL Adobe Workfront Fusion]中的[!UICONTROL SOAP] API。

## SOAP模块及其字段

SOAP连接器仅包含一个模块：执行SOAP操作

### 执行SOAP操作

此操作模块执行指定的SOAP操作。



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
   <td role="rowheader">Adobe Workfront Fusion 许可证</td> 
   <td>
   <p>基于操作：不需要 Workfront Fusion 许可证</p>
   <p>基于连接器（旧版）：Workfront Fusion for Work Automation and Integration </p>
   </td> 
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

有关 Adobe Workfront Fusion 许可证的详细信息，请参阅 [Adobe Workfront Fusion 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## SOAP模块及其字段

配置SOAP模块时，Workfront Fusion会显示以下列出的字段。  模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 执行SOAP操作

此操作模块根据您指定的WSDL执行SOAP操作。

<table style="table-layout:auto">
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL WSDL]</td> 
   <td> 选择您希望模块使用的WSDL。 要创建WSDL，请单击字段旁边的<b>添加</b>并填写这些字段。 </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL HTTP标头]</td> 
   <td> 对于每个要添加的HTTP标头，单击<b>添加项</b>并输入标头的名称和值。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL SOAP headers]</td> 
   <td> 对于每个要添加的SOAP标头，单击<b>添加项</b>并输入标头的名称、值、命名空间和XMLNS。</td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td>[!UICONTROL Force SOAP headers]</td> 
   <td> 启用此选项以配置SOAP 1.2的标头。 </td> 
  </tr> 
  </tbody> 
</table>

## [!UICONTROL SOAP]模块的限制

>[!NOTE]
>
>在WDSL加载期间禁用重定向。 这是一项安全功能，但可能意味着运行模块时会阻止未验证的重定向。

[!UICONTROL SOAP]模块当前为测试版，不支持：

* 重新定义元素
* 分数数字限制
* 总数字限制
* 空格限制
* 输入和输出消息中有多个部分。 仅支持单部分消息
* 在SOAP编码架构和元素的帮助下定义的自定义XML架构元素。

>[!BEGINSHADEBOX]

**示例：**

[!UICONTROL Workfront Fusion]无法正确识别以下内容：

```
<complexType name="ArrayOfFloat">
   <complexContent>
      <restriction base="soapenc:Array">
         <attribute ref="soapenc:arrayType"
            wsdl:arrayType="xsd:integer[]"/>
      </restriction>
   </complexContent>
</complexType>
```

此示例包括[!UICONTROL Workfront Fusion]中尚不支持的`soapenc:Array`、`soapenc:arrayType`和`wsdl:arrayType`引用。

>[!ENDSHADEBOX]

## 解决方法

如果[!UICONTROL SOAP]模块拒绝处理WSDL文件或在该模块的配置中引发各种错误，您可以尝试改用通用&#x200B;**[!UICONTROL HTTP] > [!UICONTROL 发出请求]**&#x200B;模块：

1. 在Workfront Fusion中，创建新方案。
1. 在方案中插入&#x200B;**[!UICONTROL HTTP] > [!UICONTROL 发出请求]**&#x200B;模块。
1. 打开模块的配置，并填写以下字段：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL 方法]</td> 
      <td> <p>[!UICONTROL POST]</p> </td> 
     </tr> 
     <tr data-mc-conditions=""> 
      <td role="rowheader">[!UICONTROL 主体类型]</td> 
      <td> <p>[!UICONTROL Raw]</p> </td>
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 内容类型]</td> 
      <td> <p>[!UICONTROL XML (application/xml)]</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL 解析响应]</td> 
      <td>[!UICONTROL 已启用]</td> 
     </tr> 
    </tbody> 
   </table>

   <!--![Workaround](/help/workfront-fusion/references/apps-and-modules/assets/workaround-350x443.png)-->

1. 打开新的Web浏览器窗口或选项卡。
1. 将WSDL URL粘贴到Web浏览器的地址栏并提取XML文件。

   WSDL URL通常以`?wsdl`结尾，但不一定以`http://voip.ms/api/v1/server.wsdl`结尾。

1. 如果WSDL文件未直接显示在Web浏览器中，请在文本编辑器中打开下载的文件。
1. 搜索`<service>`或`<wsdl:service>`标记：

   <!--![Service](/help/workfront-fusion/references/apps-and-modules/assets/service-350x65.png)-->

1. 找到后，从`location`属性复制URL。
1. 在Workfront Fusion中，将URL粘贴到HTTP模块的&#x200B;**请求内容**&#x200B;字段中。
1. 通过将问号替换为实际值来为所选参数提供值。

   >[!NOTE]
   >
   > 要从WSDL文件中获取特定值，请使用在线WSDL查看器。

   <!--![Request](/help/workfront-fusion/references/apps-and-modules/assets/request-xml-350x172.png)-->

1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;关闭模块的配置。
1. 执行方案或模块。
