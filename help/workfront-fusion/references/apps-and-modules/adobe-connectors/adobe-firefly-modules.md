---
title: Adobe Firefly 模块
description: 在 Adobe Workfront Fusion 场景中，您可以自动化使用  [!DNL Adobe Firefly] 的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3b29ba3d-a769-4e97-b2c2-0b4eeed5b029
source-git-commit: 4e432e277c84f95b3792cb7c295cba41a5563244
workflow-type: tm+mt
source-wordcount: '3886'
ht-degree: 15%

---

# [!DNL Adobe Firefly] 模块

在 Adobe Workfront Fusion 场景中，您可以自动化使用 [!DNL Adobe Firefly] 的工作流，并将其连接到多个第三方应用程序和服务。

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

在使用[!DNL Adobe Firefly]连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的[!DNL Adobe Firefly]帐户。

## Adobe Firefly API信息

Adobe Firefly连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.4.24</td> 
  </tr>
 </tbody> 
 </table>

## 创建与 [!DNL Adobe Firefly] 的连接

要为您的 [!DNL Adobe Firefly] 模块创建连接：

1. 在任意模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>选择您要连接到生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>选择连接服务帐户还是个人帐户。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 客户端 ID]</td>
        <td>输入您的[！UICONTROL Adobe] [！UICONTROL客户端ID]。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL Credentials]详细信息部分找到。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL Credentials]详细信息部分找到。</td>
        </tr>
      </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## [!DNL Adobe Firefly] 模块及其字段

在您配置 [!DNL Adobe Firefly] 模块时，Workfront Fusion 会显示以下字段。 除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多 [!DNL Adobe Firefly] 字段。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 展开图像

此操作模块可展开图像，可以选择从提供的提示中使用内容。

此模块适用于Firefly API V3异步。 此模块的先前版本已被弃用，不久将会删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td> 
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
   <li><b>投放</b><p>输入水平和垂直对齐方式，以及置入的图像从边缘的插入。</p></li>
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
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td> 
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

### 生成自适应复合

该动作模块将主题图像无缝地组合到被遮罩位置的背景图像中。 您可以控制应用阴影的强度、对象光照和颜色与背景的协调方式，以及是否将原始背景细节保留在蒙版区域中。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL背景&gt;图像&gt; Source]</td> 
   <td>选择提供背景图像的方式。 背景图像是将合成对象的目标场景。<ul><li><p><b>上传图像</b></p><p>上传背景图像，或从上一个模块映射图像文件。</p></li><li><p><b>图像URL</b></p><p>输入或映射背景图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL背景&gt;填充区域蒙版&gt; Source]</td> 
   <td>选择如何提供填充区域蒙版。 填充区域蒙版指示将放置对象的背景区域。<ul><li><p><b>上传图像</b></p><p>上载填充区域蒙版图像，或从上一个模块映射图像文件。</p></li><li><p><b>图像URL</b></p><p>输入或映射填充区域蒙版图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL对象&gt;图像&gt; Source]</td> 
   <td>选择如何提供对象图像。 对象图像是复合到背景中的对象的源图像。<ul><li><p><b>上传图像</b></p><p>上传对象图像，或从上一个模块映射图像文件。</p></li><li><p><b>图像URL</b></p><p>输入或映射对象图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL对象&gt;蒙版&gt; Source]</td> 
   <td>选择提供对象蒙版的方式。 对象蒙版是对象的分段蒙版。<ul><li><p><b>上传图像</b></p><p>上载对象蒙版图像，或从上一个模块映射图像文件。</p></li><li><p><b>图像URL</b></p><p>输入或映射对象蒙版图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量数]</td> 
   <td>输入一个介于1和3之间的数字。 模块生成此数量的复合变体。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL种子]*</td> 
   <td>单击<b>添加项</b>以添加种子值，然后输入或映射整数。 每个变体使用一个种子。 如果同时提供了种子值和变体数，则种子值的计数必须与[！UICONTROL Number of Variations]值匹配。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL协调]*</td> 
   <td>输入一个介于0和1之间的数字，以控制调整对象的颜色和光照以匹配背景的程度。 <code>0.0</code>应用最小协调，<code>1.0</code>应用最大协调。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL阴影强度]*</td> 
   <td>输入一个介于0和1之间的数字，以控制合成结果中的阴影强度。 较低的值会减少阴影。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL保留背景]*</td> 
   <td>选择在合成过程中是否将原始背景细节保留在被遮罩的区域中。 <ul><li><b>是</b><p>在合成期间，会保留被遮罩区域中的原始背景细节。</p></li><li><b>否</b><p>在合成期间，被遮罩区域中的原始背景细节不会被保留。</p></li><li><b>未定义</b><p>对此选项使用默认行为。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Output &gt; Media Type]*</td> 
   <td>选择生成的复合将另存为的文件格式。</td> 
  </tr> 
 </tbody> 
</table>

* 这些字段是高级字段，除非选择&#x200B;**[!UICONTROL 显示高级设置]**，否则不会显示这些字段。

### 生成图像

该操作模块会根据您提供的提示生成和图像。 您还可以提供一个可选的参考图像，生成的图像将与参考图像的样式匹配。

此模块适用于Firefly API V3异步。 此模块的先前版本已被弃用，不久将会删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Prompt]</td> 
   <td>为要生成的图像输入或映射提示。 在提示中显示更多详细信息，将允许您更好地控制映像中显示的内容。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL模型版本]</td> 
   <td>选择要用于生成图像的Firefly模型版本。</td> 
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
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td> 
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

### 使用图像5生成图像

此操作模块使用[!DNL Adobe Firefly] Image5模型生成图像。 提供文本提示和（可选）参考图像来指导生成。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Prompt]</td> 
   <td>输入或映射要生成的图像的描述。 提示必须介于1和1500个字符之间。 提示中的更多详细信息允许您更好地控制映像中显示的内容。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL长宽比]</td> 
   <td>选择所生成图像的形状。 如果提供了参考图像，请选择<b>自动</b>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL分辨率]</td> 
   <td>选择所生成图像的分辨率。 生成更高分辨率需要更长的时间。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL参考图像]</td> 
   <td>可选地提供一个参考图像来指导生成。 单击<b>添加项</b>并提供图像。 使用参考图像时，将[！UICONTROL长宽比]设置为<b>自动</b>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL种子]*</td> 
   <td>单击<b>添加项</b>并输入或映射一个整数以重现特定的生成结果。 留空将生成随机结果。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL提示推理]*</td> 
   <td>选择生成过程中使用的提示推理策略。<ul><li><p><b>质量 — 生成图像描述</b></p><p>在模块的输出中生成图像描述。</p></li><li><p><b>速度 — 更快的生成，无说明</b></p><p>更快地生成图像，但图像描述留空。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL区域设置]*</td> 
   <td>输入或映射语言和区域代码以根据特定的国家/地区和语言定制生成的内容。 <p>必须以ISO 639-1语言代码和ISO 3166-1区域提供区域设置。</p><p>示例： <code>en-US</code></p></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量数]*</td> 
   <td>输入每个请求要生成的图像数。 当前仅支持1个。 要生成多个图像，请发送单独的请求。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL模型]*</td> 
   <td>选择要用于生成图像的[!DNL Firefly]模型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射您希望模块在一个执行周期内使用的最大结果数。</td> 
  </tr> 
 </tbody> 
</table>

*这些字段是高级字段，除非选择&#x200B;**[!UICONTROL 显示高级设置]**，否则不会显示这些字段。

### 生成精确复合

此动作模块将主题放置在背景图像的蒙版区域中，并应用生成协调，以便主题与背景自然混合。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL背景&gt;图像&gt; Source]</td> 
   <td>选择提供背景图像的方式。 背景图像是将合成对象的目标场景。<ul><li><p><b>上传图像</b></p><p>上传背景图像，或从上一个模块映射图像文件。</p></li><li><p><b>图像URL</b></p><p>输入或映射背景图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL背景&gt;填充区域蒙版&gt; Source]</td> 
   <td>选择如何提供填充区域蒙版。 填充区域蒙版指示将放置对象的背景区域。<ul><li><p><b>上传图像</b></p><p>上载填充区域蒙版图像，或从上一个模块映射图像文件。</p></li><li><p><b>图像URL</b></p><p>输入或映射填充区域蒙版图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL对象&gt;图像&gt; Source]</td> 
   <td>选择如何提供对象图像。 对象图像是复合到背景中的对象的源图像。<ul><li><p><b>上传图像</b></p><p>上传对象图像，或从上一个模块映射图像文件。</p></li><li><p><b>图像URL</b></p><p>输入或映射对象图像的URL。</p></li></ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量数]</td> 
   <td>输入一个介于1和3之间的数字。 模块生成此数量的复合变体。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL种子]*</td> 
   <td>单击<b>添加项</b>以添加种子值，然后输入或映射整数。 每个变体使用一个种子。 如果同时提供了种子值和变体数，则种子值的计数必须与[！UICONTROL Number of Variations]值匹配。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Blend]*</td> 
   <td>输入介于0和1之间的数字，以控制对象的协调外观与原始外观之间的混合。 <code>0.0</code>应用完全协调，而<code>1.0</code>保留原始对象的外观。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Output &gt; Media Type]*</td> 
   <td>选择生成的复合将另存为的文件格式。</td> 
  </tr> 
 </tbody> 
</table>

* 这些字段是高级字段，除非选择&#x200B;**[!UICONTROL 显示高级设置]**，否则不会显示这些字段。

### 生成类似图像

此操作模块生成的图像与指定的源图像类似。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL变量数]</td> 
   <td>输入一个介于1-4之间的数字。 模块将生成此数量的图像变体。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL模型版本]</td> 
   <td>选择要用于生成图像的Firefly模型版本。</td> 
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


### 生成视频

此操作模块从文本提示生成视频。 您还可以提供一个或多个参考图像来指导视频生成。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Prompt]</td> 
   <td>输入或映射要生成的视频的说明。 提示中的更多详细信息允许您更好地控制视频中显示的内容。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL图像&gt;条件]</td> 
   <td>可选地提供一个或多个参考图像以引导视频生成。 为每个参考图像单击<b>添加项</b>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL大小]</td> 
   <td>单击<b>添加项</b>，然后输入或映射所生成视频的尺寸。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL比特率因子]*</td> 
   <td>输入一个介于0和63之间的数字，以指定所生成视频的比特率因子。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL视频设置&gt;相机动态]*</td> 
   <td>选择要在生成的视频中使用的相机动画。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL视频设置&gt;提示样式]*</td> 
   <td>选择要用于所生成视频的提示样式。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL视频设置&gt;拍摄角度]*</td> 
   <td>选择要在生成的视频中使用的拍摄角度。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL视频设置&gt;拍摄大小]*</td> 
   <td>选择要在生成的视频中使用的拍摄大小。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射您希望模块在一个执行周期内使用的最大结果数。</td> 
  </tr> 
 </tbody> 
</table>

* 这些字段是高级字段，除非选择&#x200B;**[!UICONTROL 显示高级设置]**，否则不会显示这些字段。

### 发起自定义 API 调用

此操作模块对Firefly API进行自定义调用。

有关特定的可用API，请参阅Adobe Developer文档中的[Adobe Firefly API](https://developer.adobe.com/firefly-services/docs/firefly-api/)。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL 连接]</td>
      <td>有关创建与 [!DNL Adobe Firefly] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与 [!DNL Adobe Firefly]</a> 的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>输入相对于 <code>https://firefly-api.adobe.io/</code> 的路径。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 方法]</p>
      </td>
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。 有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 标头]</td>
      <td>
        <p>以标准 JSON 对象的形式添加请求标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion 会自动添加授权标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 正文]</td>
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

