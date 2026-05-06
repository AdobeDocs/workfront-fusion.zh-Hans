---
title: Adobe Firefly 模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Adobe Firefly Lightroom的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 965cb643039be36eb3608cd801439a6a055974e4
workflow-type: tm+mt
source-wordcount: '1430'
ht-degree: 16%

---

# Adobe Firefly Lightroom模块

<!--add to tocs-->

在Adobe Workfront Fusion场景中，您可以自动使用Adobe Firefly Lightroom的工作流，并将其连接到多个第三方应用程序和服务。

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

在使用Adobe Firefly Lightroom连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的Adobe Firefly Lightroom帐户。

## 创建与Adobe Firefly Lightroom的连接

要为您的Adobe Firefly Lightroom模块创建连接，请执行以下操作：

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


## Adobe Firefly Lightroom模块及其字段

配置Adobe Firefly Lightroom模块时，Workfront Fusion会显示以下列出的字段。 除了这些以外，还可能会显示其他Adobe Firefly Lightroom字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [将XMP添加到图像](#add-xmp-to-image)
* [应用Lightroom编辑](#apply-lightroom-edits)
* [应用Lightroom预设](#apply-lightroom-presets)
* [自动拉直](#auto-straighten)
* [自动色调](#auto-tone)


### 将XMP添加到图像

本模块会将基于XMP的Lightroom预设应用到图像。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly Lightroom的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >创建与Adobe Firefly Lightroom的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像URL</td> 
   <td>输入或映射一个预签名URL，该URL表示要应用XMP的图像。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">存储类型</td> 
   <td>选择存储映像的存储类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">XMP内容</td> 
   <td>输入或映射要添加到图像的XMP内容的文本。 这应该是一个XML字符串。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">方向</td> 
    <td>输入或映射要应用于图像的EXIF方向。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出存储</td> 
    <td>选择要存储输出文件的位置。 <p>Fusion内部存储不会将图像存储在场景之外，但允许场景中的其他模块访问图像。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出类型</td> 
   <td>选择输出文件的文件类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">覆盖</td> 
   <td>如果要允许模块覆盖已存在的输出，请选择“是”。 这仅适用于Adobe云存储。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">质量</td> 
   <td>输入或映射输出图像的质量。 1是最低质量，12是最高质量。 这仅适用于JPEG文件。</td> 
  </tr> 
 </tbody> 
</table>

### 应用Lightroom编辑

此模块会将一个或多个Lightroom编辑应用于图像。 编辑包括曝光、对比度、锐度和饱和度。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly Lightroom的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >创建与Adobe Firefly Lightroom的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像URL</td> 
   <td>输入或映射一个预签名URL，该URL表示要应用XMP的图像。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">存储类型</td> 
   <td>选择存储映像的存储类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">编辑选项</td> 
   <td>设置要应用于图像的任何编辑选项。<p>有关选项的详细信息，请参阅Adobe Firefly Lightroom API文档中的<a href="https://developer.adobe.com/firefly-services/docs/lightroom/api/#operation/applyEdits">应用Lightroom编辑</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出存储</td> 
    <td>选择要存储输出文件的位置。 <p>Fusion内部存储不会将图像存储在场景之外，但允许场景中的其他模块访问图像。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出类型</td> 
   <td>选择输出文件的文件类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">覆盖</td> 
   <td>如果要允许模块覆盖已存在的输出，请选择“是”。 这仅适用于Adobe云存储。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">质量</td> 
   <td>输入或映射输出图像的质量。 1是最低质量，12是最高质量。 这仅适用于JPEG文件。</td> 
  </tr> 
 </tbody> 
</table>

### 应用Lightroom预设

此模块通过使用给定的预设XMP Lightroom文件，将一个或多个XMP预设应用于给定的图像。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly Lightroom的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >创建与Adobe Firefly Lightroom的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像URL</td> 
   <td>输入或映射一个预签名URL，该URL表示要应用XMP的图像。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">存储类型</td> 
   <td>选择存储映像的存储类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">预设</td> 
   <td>对于每个要应用的预设，单击<b>添加项</b>，输入预设的预定义URL，然后选择其存储类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出存储</td> 
    <td>选择要存储输出文件的位置。 <p>Fusion内部存储不会将图像存储在场景之外，但允许场景中的其他模块访问图像。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出类型</td> 
   <td>选择输出文件的文件类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">覆盖</td> 
   <td>如果要允许模块覆盖已存在的输出，请选择“是”。 这仅适用于Adobe云存储。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">质量</td> 
   <td>输入或映射输出图像的质量。 1是最低质量，12是最高质量。 这仅适用于JPEG文件。</td> 
  </tr> 
 </tbody> 
</table>

### 自动拉直

此模块通过应用自动直立变换来自动校正图像。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly Lightroom的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >创建与Adobe Firefly Lightroom的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像URL</td> 
   <td>输入或映射一个预签名URL，该URL表示要应用XMP的图像。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">存储类型</td> 
   <td>选择存储映像的存储类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">直立模式</td> 
   <td>选择要使用的直立模式类型。 如果不设置值，则会自动提供相应的模式。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">限制裁切</td> 
   <td>选择是否应裁剪已拉直的图像以删除所有空白边缘。</td> 
  </tr> 
 <tr> 
   <td role="rowheader">输出存储</td> 
    <td>选择要存储输出文件的位置。 <p>Fusion内部存储不会将图像存储在场景之外，但允许场景中的其他模块访问图像。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出类型</td> 
   <td>选择输出文件的文件类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">覆盖</td> 
   <td>如果要允许模块覆盖已存在的输出，请选择“是”。 这仅适用于Adobe云存储。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">质量</td> 
   <td>输入或映射输出图像的质量。 1是最低质量，12是最高质量。 这仅适用于JPEG文件。</td> 
  </tr> 
 </tbody> 
</table>


### 自动色调

此模块可自动校正图像的曝光、对比度、锐度和饱和度。



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly Lightroom的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly-lightroom" class="MCXref xref" >创建与Adobe Firefly Lightroom的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">图像URL</td> 
   <td>输入或映射一个预签名URL，该URL表示要应用XMP的图像。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">存储类型</td> 
   <td>选择存储映像的存储类型。</td> 
  </tr> 
  </tr> 
 <tr> 
   <td role="rowheader">输出存储</td> 
    <td>选择要存储输出文件的位置。 <p>Fusion内部存储不会将图像存储在场景之外，但允许场景中的其他模块访问图像。</p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">输出类型</td> 
   <td>选择输出文件的文件类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">覆盖</td> 
   <td>如果要允许模块覆盖已存在的输出，请选择“是”。 这仅适用于Adobe云存储。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">质量</td> 
   <td>输入或映射输出图像的质量。 1是最低质量，12是最高质量。 这仅适用于JPEG文件。</td> 
  </tr> 
 </tbody> 
</table>


