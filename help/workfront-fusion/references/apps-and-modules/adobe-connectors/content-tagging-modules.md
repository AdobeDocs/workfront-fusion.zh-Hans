---
title: Adobe Content Tagger模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Adobe Content Tagger的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: 737e9b07237960d5833cd21e110ef573ddd0a72c
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 20%

---

# Adobe Content Tagger模块

在Adobe Workfront Fusion场景中，您可以自动使用Adobe Content Tagger的工作流，并将其连接到多个第三方应用程序和服务。

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

## 创建与Adobe Content Tagger的连接

要为Adobe Content Tagger模块创建连接，请执行以下操作：

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


## Adobe Content Tagger模块及其字段

在配置Adobe Content Tagger模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Adobe Content Tagger字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 操作

* [标记颜色](#tag-colors)
* [标记关键词](#tag-keywords)
* [标记图像中的文本](#tag-text-in-an-image)

#### 标记颜色

此模块返回图像由不同像素颜色覆盖的百分比，按40种颜色类别进行排序。


<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Content Tagger的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >创建与Adobe Content Tagger的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像文件名</td> 
   <td>输入或映射要为其标记颜色的图像的文件名。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像数据</td> 
   <td>输入或映射要为其标记颜色的图像的文件数据。</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">图像格式</td> 
    <td>选择要为其标记颜色的图像类型。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">颜色数量</td> 
    <td>输入或映射要返回的颜色数量。 要返回所有结果，请输入0。</p></td> 
  </tr> 
 <tr> 
   <td role="rowheader">最小覆盖范围</td> 
   <td>输入或映射要为其标记颜色的最小覆盖范围。 将仅返回至少覆盖此图像量的颜色。 值1表示图像的100%，值。5表示图像的50%。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">在提取之前调整图像大小。</td> 
   <td>选择“是”将图像大小调整为320x320，然后再提取颜色。 选择“否”从全尺寸图像中提取颜色。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">启用前景/背景蒙版</td> 
   <td>如果要单独报告整个图像、前景和背景的颜色，请选择“是”。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">检索色调</td> 
   <td>如果要在颜色之外检索有关暖色、中性色和冷色的数据，请选择“是”。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">返回颜色的最大数量</td> 
   <td>输入或映射模块在一个执行周期内返回的最大颜色数。</td> 
  </tr> 
 </tbody> 
</table>



#### 标记关键词

此模块可提取最能描述文档主题的关键字或关键短语。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Content Tagger的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >创建与Adobe Content Tagger的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">文档文件名</td> 
   <td>输入或映射要从中提取关键字的文档的文件名。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像数据</td> 
   <td>输入或映射要从中提取关键字的文档的文件数据。</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">图像格式</td> 
    <td>选择要从中提取关键字的文档格式。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">应用程序Id</td> 
   <td>输入或映射文档的应用程序ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">关键短语数量</td> 
   <td>输入或映射您希望模块返回的关键短语数量。 要返回所有结果，请输入0。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">最小相关性</td> 
   <td>输入或映射不会返回结果的得分阈值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">最小关键短语长度（单词数）</td> 
   <td>输入或映射关键短语中所需的最小字数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">最大关键词长度（字）</td> 
   <td>输入或映射关键短语中所需的最大字数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">语义单元深度</td> 
   <td>选择您希望层次响应完成的深度。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">实体类型</td> 
   <td>对于要限制键短语的每个实体类型，单击<b>添加项</b>并输入实体类型的信息。</td> 
  </tr> 
 </tbody> 
</table>

#### 标记图像中的文本

此模块指示文本是否在图像中存在，如果存在，则返回文本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Content Tagger的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-content-tagger" class="MCXref xref" >创建与Adobe Content Tagger的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像文件名</td> 
   <td>输入或映射要从中提取文本的文档的文件名。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像数据</td> 
   <td>输入或映射要从中提取文本的文档的文件数据。</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">图像格式</td> 
    <td>选择要从中提取文本的文档格式。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">使用字典过滤</td> 
   <td>选择是否只返回英语词典中的单词。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">最小概率</td> 
   <td>输入或映射最小概率，模块将仅返回至少具有此概率识别的单词。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">最小相关性</td> 
   <td>输入返回文本应覆盖的图像的最小百分比。 相关性计算为提取文本边界框的区域与完整图像相比的分数。 0.01将翻译为至少占图像1%的文本。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">返回结果的最大数目</td> 
   <td>输入或映射模块在一个执行周期内返回的最大结果数。</td> 
  </tr> 
 </tbody> 
</table>
