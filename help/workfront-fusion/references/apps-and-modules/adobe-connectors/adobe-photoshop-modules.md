---
title: Adobe Photoshop模块
description: 借助Adobe Photoshop模块，您可以根据Adobe Photoshop帐户中的事件启动Adobe Workfront Fusion方案，创建、读取或更新协议和其他记录，使用您设置的标准搜索记录以及上传文档。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0e41d1af-af69-4f9b-a5b3-479562254084
source-git-commit: db1d6f5bf29063b069681395c6ff6d3554c67dc3
workflow-type: tm+mt
source-wordcount: '4359'
ht-degree: 0%

---

# [!DNL Adobe Photoshop]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Adobe Photoshop]的工作流，并将其连接到多个第三方应用程序和服务。


如果需要有关创建方案的说明，请参阅[创建方案：项目索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

+++**展开以查看本文中各项功能的访问要求。**

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
      <td>
        <p>[！UICONTROL Pro]或更高版本</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
      <td>
        <p>[！UICONTROL计划]，[！UICONTROL工作]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td>
      <td >
        <p>[！UICONTROL Workfront Fusion for Work Automation and Integration]</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">产品</td>
      <td>您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</td>
    </tr>
    </tr>
  </tbody>
</table>


&#42;要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

&#42;&#42;有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[!DNL [Adobe Workfront Fusion] licenses](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

在使用[!DNL Adobe Photoshop]连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的[!DNL Adobe Photoshop]帐户。
* 您必须拥有Firefly服务许可证。
* 您必须具有客户端ID和客户端密钥。 您可以从Adobe Developer Console获取这些资源。

## Adobe Photoshop API信息

Adobe Photoshop连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td>https://image.adobe.io/pie/psdService</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.12.31</td> 
  </tr>
 </tbody> 
 </table>

## 创建与[!DNL Adobe Photoshop]的连接

要为您的[!DNL Adobe Photoshop]模块创建连接：

1. 在任意模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[！UICONTROL连接名称]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL客户端ID]</td>
        <td>输入您的[！UICONTROL Adobe] [！UICONTROL客户端ID]。 可在[！UICONTROL Credentials]的 [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL客户端密钥]</td>
        <td>输入您的[!DNL Adobe] [！UICONTROL客户端密钥]。 可在[！UICONTROL Credentials]的 [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL技术帐户ID]</td>
        <td>输入您的[!DNL Adobe] [！UICONTROL技术帐户ID]。 可在[！UICONTROL Credentials]的 [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL组织ID]</td>
        <td>输入您的[!DNL Adobe] [！UICONTROL组织ID]。 可在[！UICONTROL Credentials]的 [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL私钥]</td>
        <td>
          <p>输入在[!DNL Adobe Developer Console]中创建凭据时生成的私钥。 </p>
          <p>要提取您的私钥或证书，请执行以下操作：</p>
          <ol>
            <li value="1">
              <p>单击<b>[！UICONTROL提取]</b>。</p>
            </li>
            <li value="2">
              <p>选择要提取的文件类型。</p>
            </li>
            <li value="3">
              <p>选择包含私钥或证书的文件。</p>
            </li>
            <li value="4">
              <p>输入文件的密码。</p>
            </li>
            <li value="5">
              <p>单击<b>保存</b>以提取文件并返回连接设置。</p>
            </li>
          </ol>
        </td>
        </tr>
      </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## [!DNL Adobe Photoshop]模块及其字段

配置[!DNL Adobe Photoshop]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Adobe Photoshop]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [应用PSD编辑](#apply-psd-edits)
* [自动颜色校正图像](#auto-color-correct-an-image)
* [转换图像格式](#convert-image-format)
* [创建蒙版](#create-a-mask)
* [创建新的PSD](#create-a-new-psd)
* [编辑文本图层](#edit-text-layers)
* [执行深度模糊](#execute-depth-blur)
* [执行Photoshop操作](#execute-photoshop-actions)
* [执行Photoshop操作(JSON)](#execute-photoshop-actions-json)
* [执行产品裁切](#execute-product-crop)
* [获取图层信息](#get-layer-info)
* [进行自定义API调用](#make-a-custom-api-call)
* [删除背景](#remove-background)
* [替换智能对象](#replace-a-smart-object)
* [调整图像大小](#resize-an-image)
* [为图像添加水印](#watermark-an-image)

### 应用PSD编辑

此操作模块可应用各种文档和图层级编辑。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输入）存储]</td>
      <td>
        <p>选择存储要编辑文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输入）文件位置]</p>
      </td>
   <td> 输入或映射要编辑的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL （选项&gt;文档&gt;图像大小）高度]</p>
      </td>
      <td> 输入或映射图像的高度（像素）。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL （选项&gt;文档&gt;图像大小）宽度]</p>
      </td>
      <td> 输入或映射图像的宽度（像素）。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL （选项&gt;文档&gt;画布大小）顶部]</p>
      </td>
   <td> 输入或映射文档左上角的y坐标（像素）。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL (Options &gt; Document &gt; Canvas size) Bottom]</p>
      </td>
   <td> 输入或映射文档右下角的y坐标（像素）。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL （选项&gt;文档&gt;画布大小）左侧]</p>
      </td>
   <td> 输入或映射文档左上角的x坐标（像素）。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL （选项&gt;文档&gt;画布大小） Right]</p>
      </td>
   <td> 输入或映射文档右下角的x坐标（像素）。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL (Options &gt; Document) Trim]</p>
      </td>
   <td> 选择“透明像素”以根据图像中的透明像素进行修剪。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（选项）默认字体]</p>
      </td>
   <td> 输入要用作文档全局默认字体的完整postscript名称。 此字体将用于缺少字体且没有专门为该图层提供其他字体的任何文本图层。 如果缺少此字体，则在“管理缺少的字体”中指定的选项将生效。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL (Options) Fonts]</p>
      </td>
   <td> 对于文档所需的每种字体，单击“添加项目”并输入该字体的存储位置和文件位置。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL (Options) Manage missing fonts]</p>
      </td>
   <td> 选择文档中存在一个或多个缺少的字体时要执行的操作。 <ul><li><code>fail</code>：作业将不会成功，并且状态将设置为“失败”，在状态的详细信息部分中提供了错误的详细信息。</li><li><code>useDefault</code>：作业将成功，但默认情况下，所有缺失的字体将替换为ArialMT。</li></ul></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（选项）图层]</p>
      </td>
   <td> 对于每个要添加图层，单击“添加项目”并填充图层详细信息。 <p>有关图层选项的详细信息，请参阅Adobe Photoshop文档中的<a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_applyPsdEdits/">应用PSD编辑</a>。  </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出]</td>
      <td>
        <p>对于每个要创建的转换文件，单击“添加项目”，然后输入此表中所列的存储、位置和类型。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）存储]</td>
      <td>
        <p>选择要存储新文件的文件服务。</p><p>选择Fusion内部存储可使文件可用于后续模块，但不会使文件在方案外部可用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）文件位置]</p>
      </td>
   <td> 输入或映射将存储新文件的URL或路径。 仅当尚未为输出存储选择Fusion内部存储时才需要此操作。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）类型]</p>
      </td>
   <td>选择要将文件转换到的文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。 这仅适用于Adobe存储中的文件。</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回结果的最大数目]</p>
      </td>
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
    </tr>
    </tbody>
</table>



### 自动颜色校正图像

此操作模块自动颜色更正指定的图像。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输入）存储]</td>
      <td>
        <p>选择存储要校正颜色的文件所在的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输入）文件位置]</p>
      </td>
   <td> 输入或映射要用颜色校正的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）存储]</td>
      <td>
        <p>选择要存储新文件的文件服务。</p><p>选择Fusion内部存储可使文件可用于后续模块，但不会使文件在方案外部可用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）文件位置]</p>
      </td>
   <td> 输入或映射将存储新文件的URL或路径。 仅当尚未为输出存储选择Fusion内部存储时才需要此操作。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）类型]</p>
      </td>
   <td>选择要将文件转换到的文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。 这仅适用于Adobe存储中的文件。</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回结果的最大数目]</p>
      </td>
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
    </tr>
    </tbody>
</table>


### 转换图像格式

此操作模块将文件转换为JPEG、PNG、PSD或TIFF。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输入）存储]</td>
      <td>
        <p>选择要从中删除背景的文件存储到的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输入）文件位置]</p>
      </td>
   <td> 输入或映射要删除背景的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出]</td>
      <td>
        <p>对于每个要创建的转换文件，单击“添加项目”，然后输入此表中所列的存储、位置和类型。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）存储]</td>
      <td>
        <p>选择要存储新文件的文件服务。</p><p>选择Fusion内部存储可使文件可用于后续模块，但不会使文件在方案外部可用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）文件位置]</p>
      </td>
   <td> 输入或映射将存储新文件的URL或路径。 仅当尚未为输出存储选择Fusion内部存储时才需要此操作。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）类型]</p>
      </td>
   <td>选择要将文件转换到的文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。 这仅适用于Adobe存储中的文件。</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回结果的最大数目]</p>
      </td>
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
    </tr>
    </tbody>
</table>



### 创建蒙版

此操作模块返回一个PNG文件，该文件的主体围绕主题应用。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输入）存储]</td>
      <td>
        <p>选择要从中创建掩码的文件存储到的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输入）文件位置]</p>
      </td>
   <td> 输入或映射要从中创建蒙版的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）存储]</td>
      <td>
        <p>选择要存储掩码文件的文件服务。</p><p>选择Fusion内部存储可使文件可用于后续模块，但不会使文件在方案外部可用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）文件位置]</p>
      </td>
   <td> 输入或映射将存储掩码文件的URL或路径。 仅当尚未为输出存储选择Fusion内部存储时才需要此操作。</td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。 这仅适用于Adobe存储中的文件。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL颜色空间]</p>
      </td>
   <td>选择输出图像是使用RGB还是RGBA颜色。 </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[！UICONTROL蒙版格式]</p>
      </td>
   <td>选择蒙版是柔软（羽化）还是二进制。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL优化]</p>
      </td>
   <td>选择“性能”可优化速度，选择“批处理”可允许等待时间。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL后处理过程]</p>
      </td>
   <td></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL版本]</p>
      </td>
   <td>默认值为4.0</td> 
    </tr> 
        <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回结果的最大数目]</p>
      </td>
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
    </tr>
    </tbody>
</table>

### 创建新的PSD

此操作模块使用可选层创建新的PSD，并生成演绎版或另存为PSD。

有关与此模块相关的字段，请参阅Adobe Photoshop文档中的[创建新的PSD](https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/documentCreate)。

### 编辑文本图层

此操作模块可编辑Photoshop文件中的文本图层。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输入文件存储]</td>
      <td>
        <p>选择存储要编辑文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输入文件URL]</p>
      </td>
   <td> 输入或映射要编辑的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Manage missing fonts]</td>
      <td>
        <p>选择文档中存在一个或多个缺少的字体时要执行的操作。 如果未提供该字体，模块将使用默认字体。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL默认字体]  </td>
      <td>
        <p>输入要用作文档全局默认字体的完整postscript名称。 此字体将用于缺少字体且没有专门为该图层提供其他字体的任何文本图层。 如果缺少此字体，则在“管理缺少的字体”中指定的选项将生效。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL层]</td>
   <td> <p>有关图层选项的详细信息，请参阅Adobe Photoshop文档中的<a href="https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/text">编辑文本图层</a>。</p>  </td>     </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出文件存储]</td>
      <td>
        <p>选择要存储编辑文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件URL]</p>
      </td>
   <td> 输入或映射将存储编辑文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件类型]</p>
      </td>
   <td> 为编辑的文件选择文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL压缩]</p>
      </td>
   <td> 选择输出文件的压缩级别。 </td> 
    </tr>
  </tbody>
</table>



### 执行Photoshop操作(JSON)

此操作模块使用JSON命令执行Photoshop操作。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输入）存储]</td>
      <td>
        <p>选择存储要编辑文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输入）文件位置]</p>
      </td>
   <td> 输入或映射要编辑的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL操作JSON]</td>
      <td>
        <p>输入要执行的操作的JSON命令。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL字体/图案/画笔/其他图像]</td>
      <td>
        <p>对于要在此操作中使用的每种字体、图案、画笔或其他图像，单击“添加项目”并输入项目的存储和文件位置。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL字体/模式/画笔文件URL]</p>
      </td>
   <td> 输入或映射要使用的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出文件存储]</td>
      <td>
        <p>选择要存储编辑文件的文件服务。</p><p>选择Fusion内部存储可使文件可用于后续模块，但不会使文件在方案外部可用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件URL]</p>
      </td>
   <td> 输入或映射将存储编辑文件的URL或路径。  仅当尚未为输出存储选择Fusion内部存储时才需要此操作。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件类型]</p>
      </td>
   <td> 为编辑的文件选择文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL压缩]</p>
      </td>
   <td> 选择输出文件的压缩级别。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出]</td>
      <td>
        <p>对于每个要创建的转换文件，单击“添加项目”，然后输入此表中所列的存储、位置和类型。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）存储]</td>
      <td>
        <p>选择要存储新文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）文件位置]</p>
      </td>
   <td> 输入或映射将存储新文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）类型]</p>
      </td>
   <td>选择要将文件转换到的文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。 这仅适用于Adobe存储中的文件。</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回结果的最大数目]</p>
      </td>
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
    </tr>
      </tbody>
</table>

### 执行深度模糊

此操作模块对所选文件执行“深度模糊”。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输入文件存储]</td>
      <td>
        <p>选择存储要编辑文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输入文件URL]</p>
      </td>
   <td> 输入或映射要编辑的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出文件存储]</td>
      <td>
        <p>选择要存储编辑文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件URL]</p>
      </td>
   <td> 输入或映射将存储编辑文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件类型]</p>
      </td>
   <td> 为编辑的文件选择文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL其他字段]</td>
      <td>
        <p>有关其他深度模糊选项的详细信息，请参阅Adobe Photoshop API文档中的<a href="https://developer.adobe.com/photoshop/photoshop-api-docs/api/#tag/Photoshop/operation/depthBlur">执行深度模糊</a>。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL压缩]</p>
      </td>
   <td> 选择输出文件的压缩级别。 </td> 
    </tr>
  </tbody>
</table>

### 执行Photoshop操作

此操作模块对所选图像执行Photoshop操作。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输入文件存储]</td>
      <td>
        <p>选择存储要编辑文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输入文件URL]</p>
      </td>
   <td> 输入或映射要编辑的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Actions文件存储]</td>
      <td>
        <p>选择存储操作文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL操作文件URL]</p>
      </td>
   <td> 输入或映射操作文件的URL或路径。 </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[！UICONTROL操作名称]</p>
      </td>
   <td> 如果只想执行特定操作，则可以从ActionSet中指定要播放的操作。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL字体/图案/画笔存储]</td>
      <td>
        <p>选择存储要使用的文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL字体/模式/画笔文件URL]</p>
      </td>
   <td> 输入或映射要使用的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出文件存储]</td>
      <td>
        <p>选择要存储编辑文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件URL]</p>
      </td>
   <td> 输入或映射将存储编辑文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件类型]</p>
      </td>
   <td> 为编辑的文件选择文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL压缩]</p>
      </td>
   <td> 选择输出文件的压缩级别。 </td> 
    </tr>
  </tbody>
</table>

### 执行产品裁切

此操作模块对所选图像执行产品裁切。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输入文件存储]</td>
      <td>
        <p>选择存储要裁切文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输入文件URL]</p>
      </td>
   <td> 输入或映射要裁切的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL单元]</p>
      </td>
   <td> 选择您要以像素还是以百分比描述高度和宽度调整。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL宽度]</p>
      </td>
   <td> 输入或映射要添加宽度边距的量。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL Height]</p>
      </td>
   <td> 输入或映射要添加的高度边距量。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出文件存储]</td>
      <td>
        <p>选择要存储编辑文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件URL]</p>
      </td>
   <td> 输入或映射将存储编辑文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输出文件类型]</p>
      </td>
   <td> 为编辑的文件选择文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL压缩]</p>
      </td>
   <td> 选择输出文件的压缩级别。 </td> 
    </tr>
  </tbody>
</table>

### 获取图层信息

此操作模块从指定的PSD文件中检索层信息。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输入文件存储]</td>
      <td>
        <p>选择要从中检索层信息的文件的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL输入文件URL]</p>
      </td>
   <td> 输入或映射要从中检索图层信息的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL缩略图]</p>
      </td>
   <td> </td> 
    </tr>
  </tbody>
</table>

### 进行自定义API调用

此操作模块对Photoshop API进行自定义调用。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL URL]</td>
      <td>
        <p>输入相对于<code>https://image.adobe.io/pie/psdService</code>的路径。 示例： <code>/photoshopActions</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL方法]</p>
      </td>
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 自动添加授权标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL查询字符串]  </td>
      <td>
        <p>输入请求查询字符串。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Body]</td>
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### 删除背景

此操作模块标识图像的主要主题并删除背景。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输入）存储]</td>
      <td>
        <p>选择要从中删除背景的文件存储到的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输入）文件位置]</p>
      </td>
   <td> 输入或映射要删除背景的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）存储]</td>
      <td>
        <p>选择要存储新文件的文件服务。</p><p>选择Fusion内部存储可使文件可用于后续模块，但不会使文件在方案外部可用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）文件位置]</p>
      </td>
   <td> 输入或映射将存储新文件的URL或路径。  仅当尚未为输出存储选择Fusion内部存储时才需要此操作。</td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。 这仅适用于Adobe存储中的文件。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL颜色空间]</p>
      </td>
   <td>选择输出图像是使用RGB还是RGBA颜色。 </td> 
    </tr>
     <tr>
      <td role="rowheader">
        <p>[！UICONTROL蒙版格式]</p>
      </td>
   <td>选择图像的边缘是柔和（羽化）还是二进制。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL优化]</p>
      </td>
   <td>选择“性能”可优化速度，选择“批处理”可允许等待时间。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL后处理过程]</p>
      </td>
   <td></td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL版本]</p>
      </td>
   <td>默认值为4.0</td> 
    </tr> 
        <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回结果的最大数目]</p>
      </td>
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
    </tr>
    </tbody>
</table>



### 替换智能对象

此操作模块将替换PSD层中的智能对象，并生成新演绎版。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输入）存储]</td>
      <td>
        <p>选择存储智能对象的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输入）文件位置]</p>
      </td>
   <td> 输入或映射智能对象的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL层]</p>
      </td>
   <td>对于要添加到智能对象的每个图层，单击添加项目并输入对象的名称或ID、存储智能对象的文件服务以及图层的URL或路径。<p>有关此区域高级设置的说明，请参阅Photoshop API文档中的<a href="https://developer.adobe.com/firefly-services/docs/photoshop/api/photoshop_replaceSmartObject/">替换智能对象</a> </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出]</td>
      <td>
        <p>对于您希望模块生成的每个新演绎版，单击添加项目并填写以下字段。 最多可以有25个输出文件。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）存储]</td>
      <td>
        <p>选择要存储新文件的文件服务。</p><p>选择Fusion内部存储可使文件可用于后续模块，但不会使文件在方案外部可用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）文件位置]</p>
      </td>
   <td> 输入或映射将存储新文件的URL或路径。  仅当尚未为输出存储选择Fusion内部存储时才需要此操作。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）宽度]</p>
      </td>
   <td> 输出文件的宽度（像素）。 模块将保留原始纵横比。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。 这仅适用于Adobe存储中的文件。</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回结果的最大数目]</p>
      </td>
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
    </tr>
    </tbody>
</table>



### 调整图像大小

此操作使用相同的纵横比调整图像大小。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL存储]</td>
      <td>
        <p>选择存储要调整大小的文件所在的文件服务。</p><p>选择Fusion内部存储可使文件可用于后续模块，但不会使文件在方案外部可用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL文件位置]</p>
      </td>
   <td> 输入或映射要调整大小的文件的URL或路径。  仅当尚未为输出存储选择Fusion内部存储时才需要此操作。</td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL输出]</td>
      <td>
        <p>对于每个要创建的转换文件，单击“添加项目”并输入存储、位置和其他选项，如本表中所列。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL类型]</p>
      </td>
   <td>选择要将文件转换到的文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL宽度]</p>
      </td>
   <td>输入一个数字，以像素为单位表示调整后图像的宽度。 纵横比将被保留。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL最大宽度]</p>
      </td>
   <td>当宽度为0时，可提供的最大和来获取大小。 最大宽度优先，因为它小于文档宽度。</td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。 这仅适用于Adobe存储中的文件。</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[！UICONTROL Trim to canvas]</p>
      </td>
   <td>选择“是”将格式副本修剪为“画布”大小，或选择“否”将格式副本设置为“图层大小”。</td> 
    </tr>
    </tbody>
</table>

### 为图像添加水印

此操作模块向选定图像添加水印。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Photoshop]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-photoshop" class="MCXref xref" >创建与[!DNL Adobe Photoshop]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL （基本/输入）存储]</td>
      <td>
        <p>选择要向其中添加水印的文件存储到的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（基本/输入）文件位置]</p>
      </td>
   <td> 输入或映射要添加水印的文件的URL或路径。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（水印/输入）存储]</td>
      <td>
        <p>选择存储要添加的水印的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（水印/输入）存储]</td>
      <td>
        <p>选择存储要添加的水印的文件服务。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（水印/边界）高度]</p>
      </td>
   <td>输入或映射所需的水印高度（以像素为单位）。</td> 
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（水印/边界）宽度]</p>
      </td>
   <td> 输入或映射所需的水印宽度（像素）。 </td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（水印/边界）左侧]</p>
      </td>
   <td> 输入或映射以像素为单位的距离应该包含水印的图像。</td> 
    </tr>  
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（水印/边界）顶部]</p>
      </td>
   <td> 输入或映射以像素为单位的水印应该位于的图像顶部的距离。</td> 
    </tr>  
    <tr>
      <td role="rowheader">[！UICONTROL（输出）存储]</td>
      <td>
        <p>选择要存储带水印文件的文件服务。</p><p>选择Fusion内部存储可使文件可用于后续模块，但不会使文件在方案外部可用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）文件位置]</p>
      </td>
   <td> 输入或映射将存储带水印文件的URL或路径。 仅当尚未为输出存储选择Fusion内部存储时才需要此操作。</td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）类型]</p>
      </td>
   <td>选择要将文件转换到的文件类型。 </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[！UICONTROL（输出）宽度]</p>
      </td>
   <td> 输出文件的宽度（像素）。 模块将保留原始纵横比。 </td> 
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL（输出）覆盖]</td>
      <td>
        <p>选择新编辑的文件是否会覆盖任何已存在的输出文件。 这仅适用于Adobe存储中的文件。</p>
      </td>
    </tr>
        <tr>
      <td role="rowheader">
        <p>[！UICONTROL返回结果的最大数目]</p>
      </td>
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
    </tr>
    </tbody>
</table>
