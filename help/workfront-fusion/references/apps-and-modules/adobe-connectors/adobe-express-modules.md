---
title: Adobe Express模块
description: 在Adobe Workfront Fusion场景中，您可以自动执行使用Adobe Express的工作流。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: eab04db9a38020ed973f98d7f8f290ccd183251c
workflow-type: tm+mt
source-wordcount: '1372'
ht-degree: 17%

---

# Adobe Express模块

在Adobe Workfront Fusion场景中，您可以自动使用Adobe Express的工作流，并将其连接到多个第三方应用程序和服务。

如果需要有关创建方案的说明，请参阅[创建方案：项目索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的相关文章。

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

## 先决条件

在使用Adobe Express连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的Adobe Express帐户。

## 创建与Adobe Express的连接

要为您的Adobe Express模块创建连接，请执行以下操作：

1. 在任意模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">连接名称</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">环境</td>
        <td>选择您要连接到生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">类型</td>
        <td>选择连接服务帐户还是个人帐户。</td>
        </tr>
        <tr>
        <td role="rowheader">客户端 ID</td>
        <td>输入您的Adobe客户端ID。 可在Adobe Developer Console的“凭据详细信息”部分找到此项。</td>
        </tr>
        <tr>
        <td role="rowheader">客户端密钥</td>
        <td>输入您的Adobe客户端密钥。 可在Adobe Developer Console的“凭据详细信息”部分找到此项。</td>
        </tr>
      </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。


## Adobe Express模块及其字段

配置Adobe Express模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Adobe Express字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 操作

#### 导出节目

本模块会将文档导出为JPG或PNG格式。 它可以为页面呈现版本提供预签名的URL，该URL的有效期限为四小时。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Express的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-express" class="MCXref xref" >创建与Adobe Express的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">文档</td> 
   <td>选择要导出演绎版的文档。</td> 
  </tr>
  <tr> 
   <td role="rowheader">页码</td> 
   <td>输入或映射要包含在演绎版中的页码。 一个以逗号分隔的页码字符串，将为其发出演绎版请求。 例如，“1,2，3”。 还可以指定页面范围。 例如，“1-3”包括页面1、2和3。 另一个示例为“1,3-5”，包括第1、3、4和5页。 “1 — ”可用于指定所有页面，而“5 — ”表示页面5到最后一页。 如果未提供，则默认情况下会考虑第一页。 页码从1开始。</td> 
  </tr>
  <tr> 
   <td role="rowheader">节目类型</td> 
   <td>选择要导出的演绎版类型：图像、视频或PDF</td> 
  </tr>
  <tr> 
   <td role="rowheader">格式化</td> 
   <td>选择演绎版的文件格式。</td> 
  </tr>
  <tr> 
   <td role="rowheader">PDF类型</td> 
   <td>如果要导出PDF，请选择是导出标准版还是打印PDF。</td> 
  </tr>
  <tr> 
   <td role="rowheader">大小</td> 
   <td>如果要导出图像或视频，请输入或映射最长边的大小（以像素为单位）。 保持纵横比。 对于图像，支持的最小大小为1像素，支持的最大大小为8192像素。 如果未提供，则考虑默认页面大小。</td> 
  </tr>
  <tr> 
   <td role="rowheader">下载单个PDF文件</td> 
   <td>如果要导出PDF，请选择是否将页面作为单独的PDF文件下载。 为true时，每个页面将下载为自己的PDF文件。 为false时，所有页面合并为一个PDF文件。</td> 
  </tr>
  <tr> 
   <td role="rowheader">配置</td> 
   <td>如果要导出PDF，请选择是希望该PDF采用标准配置还是打印配置。</td> 
  </tr>
  <tr> 
   <td role="rowheader">辅助功能标记</td> 
   <td>如果要导出标准PDF，请选择是否在PDF中包含辅助功能标记。</td> 
  </tr>
  <tr> 
   <td role="rowheader">出血</td> 
   <td>如果要导出打印PDF，请选择是否在导出中包括出血设置</td> 
  </tr>
  <tr> 
   <td role="rowheader">出血设置&gt;数量</td> 
   <td>输入出血利润的金额。</td> 
  </tr>
  <tr> 
   <td role="rowheader">“出血设置”&gt;“单位”</td> 
   <td>选择数量是指英寸还是毫米。</td> 
  </tr>
  <tr> 
   <td role="rowheader">裁剪</td> 
   <td>如果要导出打印PDF，请选择是否在导出中包含裁切设置</td> 
  </tr>
  <tr> 
   <td role="rowheader">“裁剪设置”&gt;“数量”</td> 
   <td>输入裁切边距的数量。</td> 
  </tr>
  <tr> 
   <td role="rowheader">“裁切设置”&gt;“单位”</td> 
   <td>选择数量是指英寸还是毫米。</td> 
  </tr>
 </tbody> 
</table>

#### 生成变体

此模块基于提供的输入参数创建文档变体。 处理之后，它临时存储生成的文档，并将它提供给指定文件夹内的用户。 该文档在30天内保持可访问状态，之后系统将自动将其删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Express的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-express" class="MCXref xref" >创建与Adobe Express的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">文档</td> 
   <td>选择要为其生成变体的文档。</td> 
  </tr>
  <tr> 
   <td role="rowheader">页码</td> 
   <td>输入或映射要包含在演绎版中的页码。 一个以逗号分隔的页码字符串，将为其发出变体请求。 例如，“1,2，3”。 还可以指定页面范围。 例如，“1-3”包括页面1、2和3。 另一个示例为“1,3-5”，包括第1、3、4和5页。 “1 — ”可用于指定所有页面，而“5 — ”表示页面5到最后一页。 如果未提供，则默认情况下会考虑第一页。 页码从1开始。</td> 
  </tr>
  <tr> 
   <td role="rowheader">首选文档名称。</td> 
   <td>输入或映射新文档的名称。 如果不提供名称或该名称已在使用中，系统将生成唯一名称。</td> 
  </tr>
  <tr> 
   <td role="rowheader">项目 ID</td> 
   <td>输入将存储变体的项目的ID。</td> 
  </tr>
  <tr> 
   <td role="rowheader">其他字段</td> 
   <td>输入其他字段的值。 可用字段基于所选文档。</td> 
  </tr>
 </tbody> 
</table>


### 搜索

#### 检索带标记的文档

此模块检索已标记文档的列表以及相关元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Express的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-express" class="MCXref xref" >创建与Adobe Express的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">开始索引</td> 
   <td>输入或映射分页开始索引。 当您检索到另一个结果列表并想要继续该列表时，使用此选项。 默认索引为0。</td> 
  </tr>
  <tr> 
   <td role="rowheader">返回结果的最大数目</td> 
   <td>输入或映射每个执行周期希望模块返回的最大结果数。</td> 
  </tr>
  <tr> 
   <td role="rowheader">排序方式</td> 
   <td>选择要按其排序结果的属性。</td> 
  </tr>
  <tr> 
   <td role="rowheader">方向</td> 
   <td>选择要按升序或降序对结果进行排序。</td> 
  </tr>
 </tbody> 
</table>

#### 检索文档详细信息

此模块检索指定文档中页面和标记元素的详细信息。 它会返回文档页面的分页列表以及有关每个页面的元数据。 如果文档带有标记元素，则API包含其各自的详细信息，如大小和位置。 如果文档没有标记的元素，则返回空数组。 响应包括分页信息，以帮助用户导航文档的页面。 一个循环最多可返回10页。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Express的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-express" class="MCXref xref" >创建与Adobe Express的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">文档</td> 
   <td>选择要返回其页面和详细信息的文档。</td> 
  </tr>
  <tr> 
   <td role="rowheader">起始页</td> 
   <td>输入或映射将从中检索详细信息的第一页的页码。</td>

#### 检索作业状态

此模块通过作业ID检索作业的状态。 根据作业类型，响应可能包括特定于作业的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Express的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-express" class="MCXref xref" >创建与Adobe Express的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">作业 ID</td> 
   <td>输入或映射要检索其详细信息的作业的ID。</td> 
  </tr>

