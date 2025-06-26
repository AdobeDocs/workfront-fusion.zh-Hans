---
title: Adobe PDF服务
description: Adobe PDF服务
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: 896597fa4a0689c19eb56d98f447c6a719d90ca2
workflow-type: tm+mt
source-wordcount: '4128'
ht-degree: 0%

---

# [!DNL Adobe PDF Services]

使用[!DNL Adobe Workfront Fusion] [!DNL Adobe PDF Services]，您可以从PDF文件中提取数据，或从提供的数据生成新的PDF文件。 此外，可以将各种文件类型转换为PDF，或将PDF转换为其他文件类型。 PDF Services还允许您组合、压缩或读取PDF文件的元数据，以及控制对文件的密码保护。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

有关用于PDF服务的API的信息，请参阅[Adobe文档生成API](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html)。

## 使用[!DNL Adobe PDF Services]时的安全注意事项

[!DNL Adobe PDF Services]可以读取、转换或修改您的文件，但[!DNL Adobe]和[!DNL Workfront Fusion]都不能存储您的文件或数据。 这意味着：

* 您可以保持对文件的控制，包括其安全性
* 您无需拥有[!UICONTROL Adobe]存储或云存储帐户即可使用PDF服务。

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
   <p>当前：无Workfront Fusion许可证要求</p>
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

要创建OAuth服务器到服务器连接，必须在Adobe PDF开发人员控制台中添加Adobe服务API。 添加API时，选择OAuth服务器到服务器选项。

有关说明，请参阅Adobe开发人员文档中的[使用OAuth用户身份验证凭据将API添加到项目](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication)。

## Adobe PDF服务API信息

Adobe PDF服务连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td>https://pdf-services-stage.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v2.1.4</td> 
  </tr>
 </tbody> 
 </table>

## 创建与[!DNL Adobe PDF Services]的连接

要为您的[!DNL Adobe PDF Services]模块创建连接：

1. 在任意[!DNL Adobe PDF Services]模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[！UICONTROL连接类型]</td>
          <td>
            <p>选择是要创建服务器到服务器连接还是JWT连接。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL连接名称]</td>
          <td>
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL客户端ID]</td>
          <td>输入您的[!DNL Adobe] [！UICONTROL客户端ID]。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL凭据详细信息]部分找到。<p>有关查找凭据的说明，请参阅Adobe开发人员文档中的<a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >凭据</a>。</p></td>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL客户端密钥]</td>
          <td>输入您的[!DNL Adobe] [！UICONTROL客户端密钥]。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL凭据详细信息]部分找到。<p>有关查找凭据的说明，请参阅Adobe开发人员文档中的<a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >凭据</a>。</p>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL技术帐户ID]（仅限JWT）</td>
          <td>输入您的[!DNL Adobe] [！UICONTROL技术帐户ID]。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL凭据详细信息]部分找到。<p>有关查找凭据的说明，请参阅Adobe开发人员文档中的<a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >凭据</a>。</p>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL组织ID]（仅限JWT）</td>
          <td>输入您的[!DNL Adobe] [！UICONTROL组织ID]。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL凭据详细信息]部分找到。<p>有关查找凭据的说明，请参阅Adobe开发人员文档中的<a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >凭据</a>。</p>
        </tr>
        <tr>
          <td role="rowheader">[！UICONTROL元范围]（仅限JWT）</td>
          <td>
            输入连接所需的任何元范围。
          </td>
        </tr>
      <tr>
        <td role="rowheader">[！UICONTROL私钥]</td>
        <td>
          <p>如果您选择了JWT连接，请输入在[!DNL Adobe Developer Console]中创建凭据时生成的私钥。 </p>
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
              <p>单击<b>[！UICONTROL保存]</b>以提取文件并返回到连接设置。</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。


## [!DNL Adobe PDF Services]模块及其字段

配置[!DNL PDF Services]时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，还可能会显示其他字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL 合并PDF文件]](#combine-pdf-files)
* [[!UICONTROL 压缩PDF文件]](#compress-pdf-files)
* [[!UICONTROL 将文档转换为PDF文件]](#convert-document-to-pdf-file)
* [[!UICONTROL 将HTML转换为PDF文件]](#convert-html-to-pdf-file)
* [[!UICONTROL 将图像转换为PDF文件]](#convert-image-to-pdf-file)
* [[!UICONTROL 将PDF转换为文档]](#convert-pdf-to-document)
* [[!UICONTROL 将PDF转换为图像]](#convert-pdf-to-image)
* [[!UICONTROL 提取文本/表]](#extract-text--table)
* [[!UICONTROL 生成文档]](#generate-document)
* [[!UICONTROL 线性化PDF文件]](#linearize-a-pdf-file)
* [进行自定义API调用](#make-a-custom-api-call)
* PDF文件的[[!UICONTROL OCR]](#ocr-for-pdf-file)
* [[!UICONTROL 页面操作]](#page-manipulation)
* [[!UICONTROL PDF辅助功能自动标记]](#pdf-accessibility-auto-tag)
* [[!UICONTROL PDF文件属性]](#pdf-file-properties)
* [[!UICONTROL 保护PDF文件]](#protect-pdf-file)
* [[!UICONTROL 删除PDF文件的保护]](#remove-protection-of-a-pdf-file)
* [拆分PDF文件](#split-a-pdf-file)

### [!UICONTROL 合并PDF文件]

此操作模块获取多个PDF文件，并将它们合并为一个PDF文件。 例如，此模块可以在项目完成后将[!UICONTROL Workfront]项目中的所有文档合并到单个PDF中。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文档]</td> 
   <td> <p>您可以使用聚合器模块来收集要合并到PDF中的文档，也可以手动添加文档。 </p> <p>我们建议使用[！UICONTROL Array Aggregator]模块来聚合上一个模块的输出。 通过使用聚合器，您无需知道要合并的文件名称、位置或数量。 因此，使用汇总比手动输入要合并的文档要灵活和可伸缩得多。</p> <p>要将[！UICONTROL Combine PDF]文件模块与聚合器结合使用，必须在[！UICONTROL Documents]字段中启用映射。 </p> <p>在此示例中，[！UICONTROL读取相关记录]模块标识与项目关联的文档，而[！UICONTROL下载文档]模块下载每个文档。 所有PDF都聚合到一个数组中，该数组将传递到[！UICONTROL Combine PDF]文件模块中。</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>您也可以手动输入文档。</p> <p>对于要包含在组合PDF中的每个文档：</p> 
    <ol> 
     <li value="1"> <p>单击[！UICONTROL添加文档]</p> </li> 
     <li value="2"> <p>在[！UICONTROL Source file]字段中，选择用于输出要包含的文档的模块，或映射源文件的名称和数据。 </p> </li> 
     <li value="3"> <p>（可选）如果要仅包含源文件中的某些页面，请为要添加的每个页面范围单击[！UICONTROL页面]字段中的<strong>[！UICONTROL添加项]</strong>，然后输入要包含的页面范围的第一个和最后一个页面，并单击<strong>[！UICONTROL添加]</strong>。 您可以从单个文档中包含多个页面范围。</p> </li> 
     <li value="4"> <p>单击<strong>[！UICONTROL添加]</strong>。 </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 压缩PDF文件]

此操作模块接受PDF文件并对其进行压缩。 这对于节省带宽或内存非常有用。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须采用PDF格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL压缩级别]</td> 
   <td>选择要使用的压缩级别。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 将文档转换为PDF文件]

此工具将文档转换为PDF文件。 源文件必须是以下文档格式之一：

* DOC
* XLS
* PPT
* TXT
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须为以下格式之一：</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>XLS</p> </li> 
     <li> <p>PPT</p> </li> 
     <li> <p>TXT</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL语言]</td> 
   <td> <p>选择源文档的默认语言。 这允许模块选择适当的字体（如果源文件中不包括字体）。</p> <p>从以下语言中选择：</p> 
    <ul> 
     <li> <p>en-US（默认）：英语（美利坚合众国）</p> </li> 
     <li> <p>ca-ES：加泰罗尼亚语（西班牙）</p> </li> 
     <li> <p>cs-CZ：捷克语（捷克共和国）</p> </li> 
     <li> <p>da-DK：丹麦语（丹麦）</p> </li> 
     <li> <p>de-DE：德语（德国）</p> </li> 
     <li> <p>en-AE：英语（阿拉伯联合酋长国）</p> </li> 
     <li> <p>en-GB：英语（英国）</p> </li> 
     <li> <p>en-IL：英语（以色列）</p> </li> 
     <li> <p>en-US：英语（美利坚合众国）</p> </li> 
     <li> <p>es-ES：西班牙语（西班牙）</p> </li> 
     <li> <p>es-MX：西班牙语（墨西哥）</p> </li> 
     <li> <p>eu-ES：巴斯克语（西班牙）</p> </li> 
     <li> <p>fi-FI：芬兰语（芬兰）</p> </li> 
     <li> <p>fr-CA：法语（加拿大）</p> </li> 
     <li> <p>fr-FR：法语（法国）</p> </li> 
     <li> <p>fr-MA：法语（摩洛哥）</p> </li> 
     <li> <p>hr-HR：克罗地亚语（克罗地亚）</p> </li> 
     <li> <p>hu-HU：匈牙利语（匈牙利）</p> </li> 
     <li> <p>it-IT：意大利语（意大利）</p> </li> 
     <li> <p>ja-JP：日语（日本）</p> </li> 
     <li> <p>kr-KR：韩语（韩国）</p> </li> 
     <li> <p>nb-NO：挪威语Bokmal（挪威）</p> </li> 
     <li> <p>nl-NL：荷兰语（荷兰）</p> </li> 
     <li> <p>pl-PL：波兰语（波兰）</p> </li> 
     <li> <p>pt-BR：葡萄牙语（巴西）</p> </li> 
     <li> <p>pt-PT：葡萄牙语（葡萄牙）</p> </li> 
     <li> <p>ro-RO：罗马尼亚语（罗马尼亚）</p> </li> 
     <li> <p>ru-RU：俄语（俄罗斯）</p> </li> 
     <li> <p>sk-SK：斯洛伐克语（斯洛伐克）</p> </li> 
     <li> <p>sl-SI：斯洛文尼亚语（斯洛文尼亚）</p> </li> 
     <li> <p>sv-SE：瑞典语（瑞典）</p> </li> 
     <li> <p>tr-TR：土耳其语（土耳其）</p> </li> 
     <li> <p>uk-UA：乌克兰语（乌克兰）</p> </li> 
     <li> <p>zh-CN：中文（中国大陆）</p> </li> 
     <li> <p>zh-TW：中文（台湾）</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 将HTML转换为PDF文件]

此工具将HTML文件转换为PDF文件。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>重要信息： Source文件必须为HTML或ZIP格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL JSON]</td> 
   <td> <p>如果您的HTML引用JavaScript变量，则可以在此处包含这些变量。 </p> <p>对于每个变量，单击<strong>[！UICONTROL添加项]</strong>并包含该变量的键和值。</p> <p>注意：   
     <ul> 
      <li> <p>从ZIP文件创建PDF时，源宣传品必须包括脚本元素，例如： <code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code> </p> </li> 
      <li> <p>从URL创建PDF时，此JSON对象的内容将在呈现页面之前插入到浏览器VM中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Include页眉和页脚]</td> 
   <td> <p>启用此选项以创建PDF文档的页眉和页脚。</p> 
    <ul> 
     <li> <p>标题包括日期和文档标题。</p> </li> 
     <li> <p>页脚包括文件名和页码。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL页面宽度]</td> 
   <td>输入纸张的宽度（以英寸为单位）。 模块将使用此信息来格式化所创建PDF文件中的页面。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL页面高度]</td> 
   <td>输入纸张的高度，以英寸为单位。 模块将使用此信息来格式化所创建PDF文件中的页面。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 将图像转换为PDF文件]

此工具将图像转换为PDF文件。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和图像文件。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 将PDF转换为文档]

此工具将PDF文件转换为文档。 您可以为输出文件选择以下格式之一。

* DOC
* DOCX
* PPTX
* XLSX
* RTF

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须采用PDF格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出文件格式]</td> 
   <td> <p>选择您希望文件输出为的格式：</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL语言]</td> 
   <td> <p>选择源文档的默认语言。 这允许模块选择适当的字体（如果源文件中不包括字体）。</p> <p>从以下语言中选择：</p> 
    <ul> 
     <li> <p>en-US（默认）：英语（美利坚合众国）</p> </li> 
     <li> <p>ca-ES：加泰罗尼亚语（西班牙）</p> </li> 
     <li> <p>cs-CZ：捷克语（捷克共和国）</p> </li> 
     <li> <p>da-DK：丹麦语（丹麦）</p> </li> 
     <li> <p>de-DE：德语（德国）</p> </li> 
     <li> <p>en-AE：英语（阿拉伯联合酋长国）</p> </li> 
     <li> <p>en-GB：英语（英国）</p> </li> 
     <li> <p>en-IL：英语（以色列）</p> </li> 
     <li> <p>en-US：英语（美利坚合众国）</p> </li> 
     <li> <p>es-ES：西班牙语（西班牙）</p> </li> 
     <li> <p>es-MX：西班牙语（墨西哥）</p> </li> 
     <li> <p>eu-ES：巴斯克语（西班牙）</p> </li> 
     <li> <p>fi-FI：芬兰语（芬兰）</p> </li> 
     <li> <p>fr-CA：法语（加拿大）</p> </li> 
     <li> <p>fr-FR：法语（法国）</p> </li> 
     <li> <p>fr-MA：法语（摩洛哥）</p> </li> 
     <li> <p>hr-HR：克罗地亚语（克罗地亚）</p> </li> 
     <li> <p>hu-HU：匈牙利语（匈牙利）</p> </li> 
     <li> <p>it-IT：意大利语（意大利）</p> </li> 
     <li> <p>ja-JP：日语（日本）</p> </li> 
     <li> <p>kr-KR：韩语（韩国）</p> </li> 
     <li> <p>nb-NO：挪威语Bokmal（挪威）</p> </li> 
     <li> <p>nl-NL：荷兰语（荷兰）</p> </li> 
     <li> <p>pl-PL：波兰语（波兰）</p> </li> 
     <li> <p>pt-BR：葡萄牙语（巴西）</p> </li> 
     <li> <p>pt-PT：葡萄牙语（葡萄牙）</p> </li> 
     <li> <p>ro-RO：罗马尼亚语（罗马尼亚）</p> </li> 
     <li> <p>ru-RU：俄语（俄罗斯）</p> </li> 
     <li> <p>sk-SK：斯洛伐克语（斯洛伐克）</p> </li> 
     <li> <p>sl-SI：斯洛文尼亚语（斯洛文尼亚）</p> </li> 
     <li> <p>sv-SE：瑞典语（瑞典）</p> </li> 
     <li> <p>tr-TR：土耳其语（土耳其）</p> </li> 
     <li> <p>uk-UA：乌克兰语（乌克兰）</p> </li> 
     <li> <p>zh-CN：中文（中国大陆）</p> </li> 
     <li> <p>zh-TW：中文（台湾）</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 将PDF转换为图像]

此工具将PDF转换为PNG或JPEG格式的图像，然后输出为列表或合并到ZIP中。

如果输出为ZIP文件，则PDF将转换为每页一个图像，并且每个图像以页码结束。 然后将图像文件合并到ZIP文件中。

例如，一个名为“TestFile”且包含8页的文件将生成8个图像，分别命名为“TestFile_1”和“TestFile_8”。 该模块的输出是一个包含8个图像的ZIP文件。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须采用PDF格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出文件格式]</td> 
   <td> <p>选择您希望文件输出为的格式：</p> 
    <ul> 
     <li>PNG</li> 
     <li>JPEG</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出类型]</td> 
   <td> <p>选择您希望文件输出为文件列表还是ZIP文件。</td> 
  </tr> 
  <tr> 
 </tbody> 
</table>

### [!UICONTROL 提取文本/表]

此操作模块允许您从PDF文件中提取数据。 模块输出单独的文本元素，如段落或表格单个单元格中的文本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td>从上一个模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">应该提取为JSON的[！UICONTROL元素]</td> 
   <td> 
    <ul> 
     <li> <p>[！UICONTROL Text]</p> </li> 
     <li> <p>[！UICONTROL Tables]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL是否提取定界框？]</td> 
   <td>启用此选项可提取有关文本定界框的数据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL是否包含输出的样式信息？]</td> 
   <td>启用此选项以将样式信息添加到输出JSON。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 生成文档]

[!UICONTROL 生成文档]模块是创建包含所选数据的PDF的强大方法。 您可以使用[!DNL Microsoft Word]模板或以JSON格式提供数据来设置其格式。

有关[!UICONTROL [!DNL Adobe PDF Services]生成文档]功能的详细信息，请参阅[!DNL Adobe Document Services]文档中的[文档生成概述](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html)。

* [使用 [!DNL Microsoft Word] 模板生成[!UICONTROL 文档]模块](#use-the-generate-document-module-with-a-microsoft-word-template)
* [使用JSON生成[!UICONTROL 文档]模块](#use-the-generate-document-module-with-json)

#### 使用[!UICONTROL 生成文档]模块和[!DNL Microsoft Word]模板


>[!NOTE]
>
>有关Microsoft Word模板的讨论，请参阅[Microsoft Word模板模块](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md)。
>
>无需使用Microsoft Word模板模块即可将Microsoft Word模板与PDF Services生成文档模块结合使用。


若要将[!UICONTROL 生成文档]模块与[!UICONTROL Microsoft Word]模板一起使用，必须先创建该模板。 有关说明，请在[!DNL Microsoft Office]文档中搜索“创建模板”。

按如下方式填写[!UICONTROL 生成文档]模块字段：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source File]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>此源文件是模块用于生成新PDF的[!DNL Microsoft Word]模板。</p> <p>我们建议在[!DNL Workfront]中为您在[!DNL Workfront Fusion]中使用的[!DNL Microsoft Word]模板创建项目。 然后，您可以使用[!DNL Workfront] &gt; [！UICONTROL下载文档]模块将相应的模板提取到方案中。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出格式]</td> 
   <td> <p>选择所生成文档的格式。</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">用于合并的[！UICONTROL数据]</td> 
   <td> <p>对于模板中要替换为文本的每个值标记，请填写以下内容：</p> 
    <ul> 
     <li> <p>[！UICONTROL Key]</p> <p>输入密钥。 在模板中，键是值标记中显示的文本。 例如，如果要将文本放置在值标记<code>&#123;&#123;name&#125;&#125;</code>中，请在键字段中输入<code>name </code>。</p> </li> 
     <li> <p>值类型</p> <p>选择值字段中的数据是值、对象还是对象数组。</p> </li> 
     <li> <p>[！UICONTROL值]</p> <p>输入或映射要在生成的文档中显示的文本以代替值标记。</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 使用JSON生成[!UICONTROL 文档]模块

要使用JSON的[!UICONTROL 生成文档]模块，请填写以下字段：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source File]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输出格式]</td> 
   <td> <p>选择所生成文档的格式。</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">用于合并的[！UICONTROL数据]</td> 
   <td> <p>要在此模块中使用JSON，必须在此字段上启用映射。</p> <p>输入或映射要从中生成文档的JSON。 </p> <p>您可以直接在此字段中键入JSON，或从JSON模块映射JSON输出。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 线性化PDF文件]

此工具可线性化PDF文档，以创建Web优化的PDF文档。 无需下载整个文档，即可逐页查看线性化PDF文档。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 进行自定义API调用

此操作模块向PDF服务API发出自定义HTTP请求。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL URL]</td> 
   <td> 输入相对路径或URL。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion会自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL字段]</td> 
   <td> <p>对于要添加到API调用的每个字段，单击<b>添加项</b>并输入该字段的键值和可选值。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### PDF文件的[!UICONTROL OCR]

此工具对文件执行光学字符识别(OCR)并生成PDF。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL语言]</td> 
   <td>选择此文档的语言。<p>有关语言选项，请参阅本文中的<a href="#convert-document-to-pdf-file" class="MCXref xref" >将文档转换为PDF文件</a>。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL OCR类型]</td> 
   <td> 
    <ul> 
     <li> <p>[！UICONTROL Modified original image]类型可确保文本可搜索且可供选择，但在清除过程中会修改原始图像（例如，扭曲原始图像），然后再在其上放置不可见的文本图层。 此类型会删除不需要的工件，并且在某些情况下可能会导致文档更易读。 </p> </li> 
     <li> <p>[！UICONTROL Unchanged original image]类型还会将可搜索的文本图层叠加在原始图像上，但在本例中，原始图像保持不变。 此类型生成原始图像的最大保真度。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 页面操作]

通过本模块，您可以选择性地旋转或删除PDF文档中的页面。 例如，您可以将纵向视图更改为横向视图，或从PDF文档中删除某些页面。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL操作]</td> 
   <td> <p>选择要对文件执行的操作。</p> 
    <ul> 
     <li> <p><b>[！UICONTROL删除]</b> </p> <p>选择此选项可从文档中删除页面。</p><p>对于每个要删除的页面范围，单击<strong>[！UICONTROL添加]</strong>，然后输入页面范围的首页和最后一页。 </p> <p>注意：   
     <ul> 
      <li> <p>您可以使用负数从文档结尾往回计数。 文档的最后一页为–1，最后一页的第二页为–2，依此类推。</p> </li> 
      <li> <p>要删除单个页面，请将起始页码和结束页码设置为相同的页码。</p></ul> </li> 
     <li> <p><b>[！UICONTROL旋转]</b> </p> <p>选择此选项可旋转页面，然后输入要相对于文档页面的起始方向旋转文档页面的顺时针角度（以度为单位）。</p> <p>要从纵向旋转到横向，或者反之，请将页面旋转90度或270度。</p> <p>如果某页是颠倒的，请将其旋转180度。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Pages]</td> 
   <td> <p>对于每个要删除的页面范围，单击<strong>[！UICONTROL添加]</strong>，然后输入页面范围的首页和最后一页。 </p> <p>注意：   
     <ul> 
      <li> <p>您可以使用负数从文档结尾往回计数。 文档的最后一页为–1，最后一页的第二页为–2，依此类推。</p> </li> 
      <li> <p>要删除单个页面，请将起始页码和结束页码设置为相同的页码。</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射每个方案执行周期中您希望模块使用的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF辅助功能自动标记]

此操作模块会创建一个PDF，并标记用于辅助功能用例。 它还创建了一个可选的Microsoft Excel报表，其中列出了问题并提供了修复建议。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL班次标题]</td> 
   <td> <p>启用此选项以移动文档上的标题。</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL生成报告]</td> 
   <td> <p>启用此选项可生成一个报告，其中列出PDF中的辅助功能问题及其位置，并提供有关如何修复这些问题的建议。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF文件属性]

此工具提取有关文档的基本信息，例如：

* 页数
* PDF版本
* 文件是否已加密
* 文件是否已线性化
* 文件是否包含嵌入的文件

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 保护PDF文件]

此工具用于保护包含用户或所有者密码的PDF文档。 它还对某些功能设置了限制，例如在PDF文档中打印、编辑和复制。 选择要加密的内容类型和加密算法。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须采用PDF格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL密码保护类型]</td> 
   <td> <p>启用此选项可使用密码加密输入的PDF文档。 如果启用此选项，则必须为以下一项或两项指定并输入值： </p> 
    <ul> 
     <li> <p>[！UICONTROL用户密码]</p> </li> 
     <li> <p>[！UICONTROL所有者密码] </p> </li> 
    </ul> <p>每个密码的长度最多为128个字符。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL加密算法]</td> 
   <td> <p>选择加密算法。 </p> 
    <ul> 
     <li> <p>[！UICONTROL AES-128加密]</p> <p>密码仅支持LATIN-I字符。 </p> </li> 
     <li> <p>[！UICONTROL AES-256加密]</p> <p>密码支持Unicode字符集</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL要加密的内容]</td> 
   <td> <p>选择要加密的内容类型。</p> 
    <ul> 
     <li> <p>[！UICONTROL所有内容]</p> </li> 
     <li> <p>[！UICONTROL除元数据以外的所有内容]</p> </li> 
     <li> <p>[！UICONTROL仅嵌入数据] </p> </li> 
    </ul> <p>选择“[！UICONTROL Only embedded data]”将使任何提供的访问权限无效。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Permissions]</td> 
   <td> <p>选择要包括的任何权限以允许打印、编辑或内容复制。</p> <p>只有在[！UICONTROL Password Protection Type]字段中设置了[！UICONTROL Owner Password]时，才使用权限设置。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 删除PDF文件的保护]

此工具可从PDF文档中删除安全性（密码保护）。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须采用PDF格式。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL密码]</td> 
   <td>输入当前保护文件的密码。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 拆分PDF文件]

此操作模块可将PDF文档拆分为多个较小的文档。 您可以指定是否按文件数、每个文件的页数或页面范围拆分它。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与[!DNL Adobe PDF Services]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与[!DNL Adobe PDF Services]</a>的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Source file]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须采用PDF格式。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL拆分选项]</td> 
   <td>选择要如何拆分文件。 
   <ul>
   <li><p><b>页面范围</b></p><p>对于要拆分为单独文档的每个页面范围，单击<b>添加</b>并输入要开始的页面和要结束的页面。</p></li>
   <li><p><b>页数</b></p><p>输入要包括在新文档中的页数。</p></li>
   <li><p><b>文件计数</b></p><p>输入要分割文档的均匀大小的文件数。</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

