---
title: Adobe Substance模块
description: 在 Adobe Workfront Fusion 场景中，您可以自动化使用  [!DNL Adobe Substance] 的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
source-git-commit: 2e44c89d487100b3245b40f6927185a0ff12ef2f
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 32%

---

# [!DNL Adobe Substance]模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL Adobe Substance] 的工作流，并将其连接到多个第三方应用程序和服务。

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

在使用[!DNL Adobe Substance]连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的[!DNL Adobe Substance]帐户。



## [!DNL Adobe Substance] 模块及其字段

在您配置 [!DNL Adobe Substance] 模块时，Workfront Fusion 会显示以下字段。除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Adobe Substance] 字段。模块中字段名称旁边的星号表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [复合](#composites)
* [场景](#scenes)
* [空间](#spaces)

### 复合

#### 生成3D对象组合

此操作模块为包含所选主页资产的3D组合生成内容。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将[!DNL Adobe Substance]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">其他字段</td> 
   <td>根据需要配置其他字段。 有关字段的详细信息，请参阅<a href="https://s3d.adobe.io/docs#/operations/v1/composites/compose">Adobe Substance API文档</a>。</td> 
  </tr> 
<!--  <tr> 
   <td role="rowheader">Camera name</td> 
   <td>Enter or map the name of an existing camera that has been previously defined in the source 3D file.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Content class</td> 
   <td>Select whether you want the composite to have the style of art or of a photo.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Enable ground plane</td> 
   <td>Enable this to enable the auto-generated ground plane under the hero asset. This is useful if the 3D scene contains only a hero asset, without additional elements.</td> 
  </tr> -->
 </tbody> 
</table>

### 场景

* [转换3D文件](#convert-3d-files)
* [创建三维场景](#create-3d-scene)
* [描述3D场景](#describe-3d-scene)
* [渲染3D对象](#render-3d-object)
* [渲染3D对象（基本版本）](#render-3d-object-basic-version)

#### 转换3D文件

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将[!DNL Adobe Substance]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">格式化</td> 
   <td>选择将文件转换为的格式。</td> 
  </tr> 
<tr> 
   <td role="rowheader">模型入口点</td> 
   <td>转换通常需要第一个被视为有效3D模型的文件。 定义此入口点，以便在有多个选项时消除混淆。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">源</td> 
   <td>对于每个要转换的文件，单击<b>添加项</b>并输入文件信息。</td> 
  </tr> 
 </tbody> 
</table>

#### 创建三维场景

此操作模块使用您指定的资源创建场景。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将[!DNL Adobe Substance]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <td role="rowheader">编码</td> 
   <td>选择场景的文件类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件基本名称</td> 
   <td>输入或映射输出文件的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">其他字段</td> 
   <td>根据需要配置其他字段。 有关字段的详细信息，请参阅<a href="https://s3d.adobe.io/docs#/operations/v1/scenes/assemble">Adobe Substance API文档</a>。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">源</td> 
   <td>对于每个要使用的文件，单击<b>添加项</b>并输入文件信息。</td> 
  </tr> 
 </tbody> 
</table>

#### 描述3D场景

此操作模块可检索有关3D场景内容的信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将[!DNL Adobe Substance]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <td role="rowheader">场景文件</td> 
   <td>输入或映射要描述的场景文件的路径。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">源</td> 
   <td>对于每个要描述的文件，单击<b>添加项</b>并输入文件信息。</td> 
  </tr> 
 </tbody> 
</table>

#### 渲染3D对象

此操作模块渲染场景的图像。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将[!DNL Adobe Substance]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
   <td role="rowheader">其他字段</td> 
   <td>根据需要配置其他字段。 有关字段的详细信息，请参阅<a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render">Adobe Substance API文档</a>。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">源</td> 
   <td>对于每个要使用的文件，单击<b>添加项</b>并输入文件信息。</td> 
  </tr> 
 </tbody> 
</table>

#### 渲染3D对象（基本版本）

此操作模块渲染场景的图像，但选项少于渲染3D对象模块。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将[!DNL Adobe Substance]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
   <td role="rowheader">其他字段</td> 
   <td>根据需要配置其他字段。 有关字段的详细信息，请参阅<a href="https://s3d.adobe.io/docs#/operations/v1/scenes/render-basic">Adobe Substance API文档</a>。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">源</td> 
   <td>对于每个要使用的文件，单击<b>添加项</b>并输入文件信息。</td> 
  </tr> 
 </tbody> 
</table>

### 空间

#### 创建空间

该操作模块允许您上传和临时存储文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将[!DNL Adobe Substance]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
   <td role="rowheader">文件名</td> 
   <td>输入或映射正在上载的文件的名称。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">文件数据</td> 
   <td>输入或映射文件的二进制数据。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">名称</td> 
   <td>输入或映射多部分表单值的名称。</td> 
  </tr> 
 </tbody> 
</table>
