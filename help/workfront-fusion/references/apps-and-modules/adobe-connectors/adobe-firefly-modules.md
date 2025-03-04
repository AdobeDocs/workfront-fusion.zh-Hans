---
title: Adobe Firefly模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用 [!DNL Adobe Firefly]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '2432'
ht-degree: 0%

---

# [!DNL Adobe Firefly]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Adobe Firefly]的工作流，并将其连接到多个第三方应用程序和服务。

如果需要有关创建方案的说明，请参阅[创建方案：项目索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

在使用[!DNL Adobe Firefly]连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的[!DNL Adobe Firefly]帐户。

## Adobe Firefly API信息

Adobe Firefly连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## 创建与[!DNL Adobe Firefly]的连接

要为您的[!DNL Adobe Firefly]模块创建连接：

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
        <td role="rowheader">[！UICONTROL环境]</td>
        <td>选择您要连接到生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL类型]</td>
        <td>选择您是要连接到服务帐户还是个人帐户。</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL客户端ID]</td>
        <td>输入您的[！UICONTROL Adobe] [！UICONTROL客户端ID]。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL Credentials]详细信息部分找到。</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL客户端密钥]</td>
        <td>输入您的[!DNL Adobe] [！UICONTROL客户端密钥]。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL Credentials]详细信息部分找到。</td>
        </tr>
      </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## [!DNL Adobe Firefly]模块及其字段

配置[!DNL Adobe Firefly]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Adobe Firefly]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 展开图像

此操作模块可展开图像，可以选择从提供的提示中使用内容。

此模块适用于Firefly API V3异步。 此模块的先前版本已被弃用，不久将会删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与[!DNL Adobe Firefly]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Prompt]</td> 
   <td>输入或映射要用于展开图像的内容的提示。 如果未提供任何提示，则图像将展开，并且内容与原始图像匹配。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量数]</td> 
   <td>输入一个介于1-4之间的数字。 模块将生成此数量的扩展图像变体。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source]</td> 
   <td>选择提供源文件的方式：<ul><li><p><b>文件</b></p><p>从上一个模块中选择一个源文件，或映射源文件的参考图像文件名和参考图像文件。</p></li><li><p><b>预签名URL</b></p><p>输入或映射源图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL扩展图像格式]</td> 
   <td>选择将保存扩展图像的文件格式。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL展开方式]</td> 
   <td>  <p>选择要通过使用图像放置还是使用蒙版来展开图像。</p> 
   <ul>
   <li><b>放置环境</b><p>输入水平和垂直对齐方式，以及置入的图像从边缘的插入。</p></li>
   <li><b>蒙版</b><p>选择掩码的源文件，以及是否应反转掩码。</p></li>
   </ul>
</td> 
</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL大小]</td> 
   <td>选择希望扩展图像达到的高度和宽度。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL种子]</td> 
   <td>对于模块将生成的每个图像，单击<b>添加项</b>并输入或映射整数。 您可以在另一个扩展图像模块中使用此相同的种子，以生成具有不同样式的相似图像。 添加的种子数必须等于变体数字段。</td> 
  </tr> 
 </tbody> 
</table>

### 展开图像（已弃用）

此模块已弃用，不久将会删除。 请改用展开图像模块。

### 填充图像

此操作模块会填充图像的蒙版区域，可以选择使用您提供的提示中的内容。

此模块适用于Firefly API V3异步。 此模块的先前版本已被弃用，不久将会删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与[!DNL Adobe Firefly]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL图像&gt; Source]</td> 
   <td>选择提供图像源文件的方式：<ul><li><p><b>文件</b></p><p>从上一个模块中选择一个源文件，或映射源文件的参考图像文件名和参考图像文件。</p></li><li><p><b>预签名URL</b></p><p>输入或映射源图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL蒙版&gt; Source]</td> 
   <td>选择提供掩码源文件的方式：<ul><li><p><b>文件</b></p><p>从上一个模块中选择一个源文件，或映射源文件的参考图像文件名和参考图像文件。</p></li><li><p><b>预签名URL</b></p><p>输入或映射源图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Prompt]</td> 
   <td>输入或映射要用于填充图像的内容的提示。 如果未提供任何提示，则图像将填充与原始图像匹配的内容。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量数]</td> 
   <td>输入一个介于1-4之间的数字。 模块将生成此数量的已填充图像变体。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL填充图像格式]</td> 
   <td>选择将保存已填充图像的文件格式。</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL种子]</td> 
   <td>对于模块将生成的每个图像，单击<b>添加项</b>并输入或映射整数。 您可以在另一个扩展图像模块中使用此相同的种子，以生成具有不同样式的相似图像。 添加的种子数必须等于变体数字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL大小]</td> 
   <td>选择希望填充图像的大小。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL区域设置]</td> 
   <td>如果提供了区域设置，则模块会生成与指定区域设置更相关的内容。 <p>必须以ISO 639-1语言代码和ISO 3166-1区域提供区域设置。</p><p> 示例： <code>en-US</code></p></td> 
  </tr> 
 </tbody> 
</table>

### 填充图像（已弃用）

此模块已弃用，不久将会删除。 请改用“填充图像”模块。

## 生成图像

该操作模块会根据您提供的提示生成和图像。 您还可以提供一个可选的参考图像，生成的图像将与参考图像的样式匹配。

此模块适用于Firefly API V3异步。 此模块的先前版本已被弃用，不久将会删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与[!DNL Adobe Firefly]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Prompt]</td> 
   <td>为要生成的图像输入或映射提示。 在提示中显示更多详细信息，将允许您更好地控制映像中显示的内容。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量数]</td> 
   <td>输入一个介于1-4之间的数字。 模块将生成此数量的图像变体。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL生成的图像格式]</td> 
   <td>选择将保存扩展图像的文件格式。 如果选择“默认”，则在未提供参考图像的情况下，文件格式将为JPEG。 如果提供了参考图像，则生成的图像的文件格式将与参考图像相同。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Structure &gt; Image reference]</td> 
    <td>选择为新图像结构提供源文件的方式：<ul><li><p><b>文件</b></p><p>从上一个模块中选择一个源文件，或映射源文件的参考图像文件名和参考图像文件。</p></li><li><p><b>预签名URL</b></p><p>输入或映射源图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL结构&gt;强度]</td> 
    <td>输入一个介于0和100之间的数字，以控制Firefly遵循源图像结构的严格程度。 数字越大，表示Firefly越严格地遵循图像。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL样式&gt;图像引用]</td> 
    <td>选择为新图像的样式提供源文件的方式：<ul><li><p><b>文件</b></p><p>从上一个模块中选择一个源文件，或映射源文件的参考图像文件名和参考图像文件。</p></li><li><p><b>预签名URL</b></p><p>输入或映射源图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL结构&gt;强度]</td> 
    <td>输入一个介于0和100之间的数字，以控制Firefly遵循源图像样式的严格程度。 数字越大，表示Firefly越严格地遵循图像。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL样式&gt;预设]</td> 
   <td>如果要使用预设样式，请单击“添加项目”，然后输入或映射要使用的样式。<p>有关预设样式的列表，请参阅Adobe开发人员文档中的<a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >图像模型样式</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL负提示]</td> 
   <td>在生成的内容中输入或映射要避免使用的单词。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL内容类]</td> 
   <td>选择您希望生成的图像更类似于照片，还是更类似于创建的图片。 <ul><li><b>照片</b><p>输入“光圈”、“快门速度”（以秒为单位）和“视场”（以毫米为单位）的值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Seed]</td> 
   <td>对于模块将生成的每个图像，单击<b>添加项</b>并输入或映射整数。 您可以在另一个扩展图像模块中使用此相同的种子，以生成具有不同样式的相似图像。 添加的种子数必须等于变体数字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL大小]</td> 
   <td>选择希望生成的图像的大小。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[！UICONTROL视觉强度]</td> 
   <td>输入或映射一个整数，该整数表示照片现有视觉特征的整体强度。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL区域设置]</td> 
   <td>如果提供了区域设置，则模块会生成与指定区域设置更相关的内容。 <p>必须以ISO 639-1语言代码和ISO 3166-1区域提供区域设置。</p><p> 示例： <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL可拼贴]</td> 
   <td>启用此选项可生成可在每个方向无限重复的图像。</td> 
  </tr> 
 </tbody> 
</table>

### 生成图像（已弃用）

此模块已弃用，不久将会删除。 请改用生成图像模块。

### 生成对象组合

此操作模块可合并Firefly生成的图像以创建图像复合。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与[!DNL Adobe Firefly]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Prompt]</td> 
   <td>为要生成的图像输入或映射提示。 在提示中显示更多详细信息，将允许您更好地控制映像中显示的内容。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量数]</td> 
   <td>输入一个介于1-4之间的数字。 模块将生成此数量的图像变体。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL内容类]</td> 
   <td>选择您希望生成的图像更类似于照片还是图像。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL图像&gt; Source]</td> 
    <td>选择为新图像结构提供源文件的方式：<ul><li><p><b>文件</b></p><p>从上一个模块中选择一个源文件，或映射源文件的参考图像文件名和参考图像文件。</p></li><li><p><b>预签名URL</b></p><p>输入或映射源图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL生成的图像格式]</td> 
   <td>选择将保存扩展图像的文件格式。 如果选择“默认”，则在未提供参考图像的情况下，文件格式将为JPEG。 如果提供了参考图像，则生成的图像的文件格式将与参考图像相同。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL样式&gt;图像引用]</td> 
    <td>选择为新图像的样式提供源文件的方式：<ul><li><p><b>文件</b></p><p>从上一个模块中选择一个源文件，或映射源文件的参考图像文件名和参考图像文件。</p></li><li><p><b>预签名URL</b></p><p>输入或映射源图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL结构&gt;强度]</td> 
    <td>输入一个介于0和100之间的数字，以控制Firefly遵循源图像样式的严格程度。 数字越大，表示Firefly越严格地遵循图像。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL样式&gt;预设]</td> 
   <td>如果要使用预设样式，请单击“添加项目”，然后输入或映射要使用的样式。<p>有关预设样式的列表，请参阅Adobe开发人员文档中的<a href="https://developer.adobe.com/firefly-services/docs/firefly-api/guides/concepts/style-presets//" >图像模型样式</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL大小]</td> 
   <td>选择要生成的复合的大小。 </td> 
  </tr> 
 </tbody> 
</table>

### 生成类似图像

此操作模块生成的图像与指定的源图像类似。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Campaign]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与[!DNL Adobe Firefly]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量数]</td> 
   <td>输入一个介于1-4之间的数字。 模块将生成此数量的图像变体。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL生成的图像格式]</td> 
   <td>选择将保存扩展图像的文件格式。 如果选择“默认”，则在未提供参考图像的情况下，文件格式将为JPEG。 如果提供了参考图像，则生成的图像的文件格式将与参考图像相同。</td> 
  </tr> 
   <tr> 
   <td role="rowheader">[！UICONTROL图像&gt; Source]</td> 
    <td>选择为新图像结构提供源文件的方式：<ul><li><p><b>文件</b></p><p>从上一个模块中选择一个源文件，或映射源文件的参考图像文件名和参考图像文件。</p></li><li><p><b>预签名URL</b></p><p>输入或映射源图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL样式&gt;图像引用]</td> 
    <td>选择为新图像的样式提供源文件的方式：<ul><li><p><b>文件</b></p><p>从上一个模块中选择一个源文件，或映射源文件的参考图像文件名和参考图像文件。</p></li><li><p><b>预签名URL</b></p><p>输入或映射源图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL大小]</td> 
   <td>选择要生成的复合的大小。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL种子]</td> 
   <td>对于模块将生成的每个图像，单击<b>添加项</b>并输入或映射整数。 您可以在另一个扩展图像模块中使用此相同的种子，以生成具有不同样式的相似图像。 添加的种子数必须等于变体数字段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL可拼贴]</td> 
   <td>启用此选项可生成可在每个方向无限重复的图像。</td> 
  </tr> 
 </tbody> 
</table>


### 进行自定义API调用

此操作模块对Firefly API进行自定义调用。

有关特定的可用API，请参阅Adobe Developer文档中的[Adobe Firefly API](https://developer.adobe.com/firefly-services/docs/firefly-api/)。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Firefly]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与[!DNL Adobe Firefly]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL URL]</td>
      <td>
        <p>输入相对于<code>https://firefly-api.adobe.io/</code>的路径。</p>
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
      <td role="rowheader">[！UICONTROL Body]</td>
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

