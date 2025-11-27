---
title: Adobe PDF Services
description: Adobe PDF Services
author: Becky
draft: Probably
feature: Workfront Fusion, Digital Content and Documents
exl-id: e6fbbc20-4315-4668-9e11-af7cfa82ae66
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: ht
source-wordcount: '4151'
ht-degree: 100%

---

# [!DNL Adobe PDF Services]

通过 Adobe Workfront Fusion 的 [!DNL Adobe PDF Services]，您可以从 PDF 文件中提取数据，或根据您提供的数据生成新的 PDF 文件。此外，您可以将多种文件类型转换为 PDF，或将 PDF 转换为其他文件类型。PDF Services 还允许您合并、压缩 PDF 文件、读取 PDF 文件的元数据，以及控制文件的密码保护设置。

有关创建场景的说明，请参阅[创建场景：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)中的相关文章。

有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)中的相关文章。

有关 PDF Services 使用的 API，请参阅 [Adobe 文档生成 API](https://www.adobe.io/apis/documentcloud/dcsdk/doc-generation.html)。

## 使用 [!DNL Adobe PDF Services] 时的安全考虑

[!DNL Adobe PDF Services] 可以读取、转化或修改您的文件，但 [!DNL Adobe] 和 Workfront Fusion 均不会存储您的文件或数据。这意味着：

* 您始终掌控您的文件，包括其安全性。
* 您无需拥有 [!UICONTROL Adobe] 存储或云存储帐户即可使用 PDF Services。

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

要创建 OAuth 服务器到服务器连接，您必须在 Adobe Developers Console 中添加 Adobe PDF Services API。在添加该 API 时，选择 OAuth 服务器到服务器选项。

有关说明，请参阅 Adobe 开发人员文档中的[使用 OAuth 用户身份验证凭据在项目中添加 API](https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication)。

## Adobe PDF Services API 信息

Adobe PDF Services 连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td>https://pdf-services-stage.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v2.1.4</td> 
  </tr>
 </tbody> 
 </table>

## 创建与 [!DNL Adobe PDF Services] 的连接

要为您的 [!DNL Adobe PDF Services] 模块创建连接：

1. 在任意 [!DNL Adobe PDF Services] 模块中，点击“连接”框旁的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
          <td role="rowheader">[!UICONTROL 连接类型]</td>
          <td>
            <p>选择您要创建服务器到服务器连接还是 JWT 连接。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 连接名称]</td>
          <td>
            <p>输入此连接的名称。</p>
          </td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端 ID]</td>
          <td>输入您的 [!DNL Adobe] [!UICONTROL 客户端 ID]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。<p>有关查找凭据的说明，请参阅 Adobe 开发人员文档中的<a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >凭据</a>部分。</p></td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端密钥]</td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。<p>有关查找凭据的说明，请参阅 Adobe 开发人员文档中的<a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >凭据</a>部分。</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 技术帐户 ID]（仅适用于 JWT）</td>
          <td>输入您的 [!DNL Adobe] [!UICONTROL 技术帐户 ID]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。<p>有关查找凭据的说明，请参阅 Adobe 开发人员文档中的<a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >凭据</a>部分。</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 组织 ID]（仅适用于 JWT）</td>
          <td>输入您的 [!DNL Adobe] [!UICONTROL 组织 ID]。该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。<p>有关查找凭据的说明，请参阅 Adobe 开发人员文档中的<a href="https://developer.adobe.com/developer-console/docs/guides/services/services-add-api-oauth-user-authentication#credentials" class="MCXref xref" >凭据</a>部分。</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL Meta 范围]（仅适用于 JWT）</td>
          <td>
            输入此连接所需的 meta 范围。
          </td>
        </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 私钥]</td>
        <td>
          <p>如果您选择了 JWT 连接，请输入在 [!DNL Adobe Developer Console] 中创建凭据时生成的私钥。 </p>
          <p>要提取您的私钥或证书：</p>
          <ol>
            <li value="1">
              <p>点击<b>[!UICONTROL 提取]</b>。</p>
            </li>
            <li value="2">
              <p>选择您要提取的文件类型。</p>
            </li>
            <li value="3">
              <p>选择包含私钥或证书的文件。</p>
            </li>
            <li value="4">
              <p>输入该文件的密码。</p>
            </li>
            <li value="5">
              <p>点击<b>[!UICONTROL 保存]</b>以提取文件，并返回连接设置界面。</p>
            </li>
          </ol>
        </td>
      </tr>
       </tbody>
    </table>
1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。


## [!DNL Adobe PDF Services] 模块及其字段

在您配置 [!DNL PDF Services] 时，Workfront Fusion 会显示以下字段。除这些字段外，根据您的应用程序或服务访问权限级别，可能会显示更多字段。模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL 合并 PDF 文件]](#combine-pdf-files)
* [[!UICONTROL 压缩 PDF 文件]](#compress-pdf-files)
* [[!UICONTROL 将文档转化为 PDF 文件]](#convert-document-to-pdf-file)
* [[!UICONTROL 将 HTML 转化为 PDF 文件]](#convert-html-to-pdf-file)
* [[!UICONTROL 将图像转化为 PDF 文件]](#convert-image-to-pdf-file)
* [[!UICONTROL 将 PDF 转化为文档]](#convert-pdf-to-document)
* [[!UICONTROL 将 PDF 转化为图像]](#convert-pdf-to-image)
* [[!UICONTROL 提取文本/表]](#extract-text--table)
* [[!UICONTROL 生成文档]](#generate-document)
* [[!UICONTROL 对 PDF 文件进行线性化]](#linearize-a-pdf-file)
* [发起自定义 API 调用](#make-a-custom-api-call)
* [[!UICONTROL PDF 文件的 OCR]](#ocr-for-pdf-file)
* [[!UICONTROL 页面操作]](#page-manipulation)
* [[!UICONTROL PDF 辅助功能自动标记]](#pdf-accessibility-auto-tag)
* [[!UICONTROL PDF 文件属性]](#pdf-file-properties)
* [[!UICONTROL 保护 PDF 文件]](#protect-pdf-file)
* [[!UICONTROL 移除对 PDF 文件的保护]](#remove-protection-of-a-pdf-file)
* [拆分 PDF 文件](#split-a-pdf-file)

### [!UICONTROL 合并 PDF 文件]

此操作模块会将多个 PDF 文件合并为一个 PDF 文件。例如，该模块可在项目完成时，将某个 [!UICONTROL Workfront] 项目中的所有文档合并为一个 PDF 文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文档]</td> 
   <td> <p>您可以使用聚合器模块来收集要合并成 PDF 的文档，也可以手动添加文档。 </p> <p>我们建议使用[!UICONTROL 数组聚合器]模块来聚合前一个模块的输出。使用聚合器后，您无需预先知道要合并的文件名称、位置或数量。因此，使用聚合器比手动输入要合并的文档更加灵活且具有更高的可扩展性。</p> <p>要在使用聚合器的情况下使用[!UICONTROL 合并 PDF] 文档模块，您必须在[!UICONTROL 文档]字段上启用映射。 </p> <p>在此示例中，[!UICONTROL 读取相关记录]模块识别与项目关联的文档，[!UICONTROL 下载文档]模块下载每个文档。所有 PDF 文件会聚合成一个数组，并传入[!UICONTROL 合并 PDF]文档模块。</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/combine-example-350x104.png" style="width: 350;height: 104;"> </p> <p>您也可以手动输入文档。</p> <p>对于每个要包含在合并 PDF 中的文档：</p> 
    <ol> 
     <li value="1"> <p>点击[!UICONTROL 添加文档]</p> </li> 
     <li value="2"> <p>在[!UICONTROL 源文件]字段中，选择输出您要包含的文档的模块，或映射源文件的名称和数据。 </p> </li> 
     <li value="3"> <p>（可选）如果您只想包含源文件中的部分页面，则需为每个要添加的页码范围在[!UICONTROL 页面]字段中点击<strong>[!UICONTROL 添加项目]</strong>，然后输入该页码范围的起始页和结束页，并点击<strong>[!UICONTROL 添加]</strong>。您可以从同一个文档中包含多个页码范围。</p> </li> 
     <li value="4"> <p>点击<strong>[!UICONTROL 添加]</strong>。 </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 压缩 PDF 文件]

此操作模块会对 PDF 文件进行压缩。这对于节省带宽或内存非常有用。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须是 PDF 格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 压缩级别]</td> 
   <td>选择您希望使用的压缩级别。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 将文档转化为 PDF 文件]

此工具会将文档转化为 PDF 文件。源文件必须是以下文档格式之一：

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
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须是以下格式之一：</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>XLS</p> </li> 
     <li> <p>PPT</p> </li> 
     <li> <p>TXT</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 语言]</td> 
   <td> <p>选择源文档的默认语言。如果源文件未包含字体，这可使模块选择合适的字体。</p> <p>从以下语言中选择：</p> 
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
     <li> <p>nb-NO：挪威博克马尔语（挪威）</p> </li> 
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

### [!UICONTROL 将 HTML 转化为 PDF 文件]

此工具会将 HTML 文件转换为 PDF 文件。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>重要提示：源文件必须为 HTML 或 ZIP 格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL JSON]</td> 
   <td> <p>如果您的 HTML 引用了 JavaScript 变量，您可以在此处加入这些变量。 </p> <p>对于每个变量，点击<strong>[!UICONTROL 添加项目]</strong>，并输入变量的键和值。</p> <p>注意：   
     <ul> 
      <li> <p>当从 ZIP 文件创建 PDF 时，源素材必须包含如下脚本元素：<code> &lt;script src='./json.js' type='text/javascript'&gt;&lt;/script&gt;</code> </p> </li> 
      <li> <p>当从 URL 创建 PDF 时，该 JSON 对象的内容会在页面渲染之前注入到浏览器 VM 中。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 包括页眉和页脚]</td> 
   <td> <p>启用此选项以为 PDF 文档创建页眉和页脚。</p> 
    <ul> 
     <li> <p>页眉包含日期和文档标题。</p> </li> 
     <li> <p>页脚包含文件名称和页码。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 页面宽度]</td> 
   <td>输入纸张宽度（单位为英寸）。模块会根据此信息对所生成 PDF 文件的页面进行格式设置。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 页面高度]</td> 
   <td>输入纸张高度（单位为英寸）。模块会根据此信息对所生成 PDF 文件的页面进行格式设置。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 将图像转化为 PDF 文件]

此工具会将图像转化为 PDF 文件。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和图像文件。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 将 PDF 转化为文档]

此工具会将 PDF 文件转化为文档。您可以为输出文件选择以下格式之一：

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
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须是 PDF 格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出文件格式]</td> 
   <td> <p>选择您希望文件输出的格式：</p> 
    <ul> 
     <li> <p>DOC</p> </li> 
     <li> <p>DOCX</p> </li> 
     <li> <p>PPTX</p> </li> 
     <li> <p>XLSX</p> </li> 
     <li> <p>RTF</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 语言]</td> 
   <td> <p>选择源文档的默认语言。如果源文件未包含字体，这可使模块选择合适的字体。</p> <p>从以下语言中选择：</p> 
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
     <li> <p>nb-NO：挪威博克马尔语（挪威）</p> </li> 
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

### [!UICONTROL 将 PDF 转化为图像]

此工具会将 PDF 转换为 PNG 或 JPEG 格式的图像，并将其输出为列表，或将其合并为一个 ZIP 文件。

如果输出为 ZIP，PDF 的每一页都会转化为一张图像，且每张图像会以页码结尾。然后这些图像文件会被合并为一个 ZIP 文件。

例如，一个名为 &quot;TestFile&quot; 的 8 页文件将生成 8 张图像，分别命名为 &quot;TestFile_1&quot; 到 &quot;TestFile_8&quot;。该模块的输出是一个包含这 8 张图像的 ZIP 文件。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须是 PDF 格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出文件格式]</td> 
   <td> <p>选择您希望文件输出为的格式：</p> 
    <ul> 
     <li>PNG</li> 
     <li>JPEG</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出类型]</td> 
   <td> <p>选择您希望将文件输出为文件列表，还是 ZIP 文件。</td> 
  </tr> 
  <tr> 
 </tbody> 
</table>

### [!UICONTROL 提取文本/表]

此操作模块允许您从 PDF 文件中提取数据。该模块会输出独立的文本元素，例如段落，或表格单元格中的文本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td>从上一个模块中选择源文件，或映射源文件的名称和数据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 应该提取为 JSON 的元素]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL 文本]</p> </li> 
     <li> <p>[!UICONTROL 表]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 是否提取定界框？]</td> 
   <td>启用此选项可提取文本定界框的数据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 是否包含输出的样式信息？]</td> 
   <td>启用此选项可在输出 JSON 中加入样式信息。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 生成文档]

[!UICONTROL 生成文档]模块提供了一种功能强大的方式，用于创建包含所选数据的 PDF。您可以使用 [!DNL Microsoft Word] 模板进行格式化，也可以以 JSON 格式提供数据。

有关[!UICONTROL [!DNL Adobe PDF Services]生成文档]功能的更多信息，请参阅 [!DNL Adobe Document Services] 文档中的[文档生成概述](https://www.adobe.io/apis/documentcloud/dcsdk/docs.html)。

* [使用[!UICONTROL 生成文档]模块搭配 [!DNL Microsoft Word] 模板](#use-the-generate-document-module-with-a-microsoft-word-template)
* [使用[!UICONTROL 生成文档]模块搭配 JSON](#use-the-generate-document-module-with-json)

#### 使用[!UICONTROL 生成文档]模块搭配 [!DNL Microsoft Word] 模板


>[!NOTE]
>
>有关 Microsoft Word 模板的说明，请参阅 [Microsoft Word 模板模块](/help/workfront-fusion/references/apps-and-modules/third-party-connectors/microsoft-word-templates-modules.md)。
>
>您无需使用 Microsoft Word 模板模块，也可以在 PDF Services 的生成文档模块中使用 Microsoft Word 模板。


若要使用[!UICONTROL 生成文档]模块搭配 [!UICONTROL Microsoft Word] 模板，您必须先创建该模板。如需创建模板的说明，请在 [!DNL Microsoft Office] 文档中搜索“创建模板”。

按以下方式填写[!UICONTROL 生成文档]模块字段：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>此源文件是模块用于生成新 PDF 的 [!DNL Microsoft Word] 模板。</p> <p>我们建议在 Workfront 中创建一个项目，用于存放您在 Workfront Fusion 中使用的 [!DNL Microsoft Word] 模板。这样，您便可以使用 Workfront &gt; [!UICONTROL 下载文档]模块将相应模板导入到您的场景中。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出格式]</td> 
   <td> <p>选择生成文档的格式。</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 用于合并的数据]</td> 
   <td> <p>对于模板中您希望替换文本的每个值标记，请填写以下内容：</p> 
    <ul> 
     <li> <p>[!UICONTROL 键]</p> <p>输入一个键。在模板中，该键即值标记中显示的文本。例如，如果您想向值标记 <code>&#123;&#123;name&#125;&#125;</code> 插入文本，则需在键字段中输入 <code>name </code>。</p> </li> 
     <li> <p>值类型</p> <p>选择值字段中的数据类型是单个值、对象，还是对象数组。</p> </li> 
     <li> <p>[!UICONTROL 值]</p> <p>输入或映射您希望在生成的文档中替换值标记的文本。</p> </li> 
    </ul> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/generate-with-template-350x241.png" style="width: 350;height: 241;"> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 使用[!UICONTROL 生成文档]模块搭配 JSON

要使用[!UICONTROL 生成文档]模块搭配 JSON，请按以下方式填写字段：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 输出格式]</td> 
   <td> <p>选择生成文档的格式。</p> 
    <ul> 
     <li> <p>PDF</p> </li> 
     <li> <p>DOCX</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 用于合并的数据]</td> 
   <td> <p>要在此模块中使用 JSON，您必须在该字段上启用映射。</p> <p>输入或映射用于生成文档的 JSON。 </p> <p>您可以在此字段中直接输入 JSON，或映射来自 JSON 模块的 JSON 输出。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 对 PDF 文件进行线性化]

此工具会将 PDF 文档线性化，以创建适用于 Web 的优化 PDF 文档。线性化 PDF 文档可按页查看，而无需下载整个文档。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

## 发起自定义 API 调用

此操作模块会向 PDF Services API 发起自定义 HTTP 请求。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> 输入相对路径或 URL。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标头]</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion 会自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 字段]</td> 
   <td> <p>对于每个要添加到 API 调用中的字段，点击<b>添加项目</b>，并输入该字段的键和可选值。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


### [!UICONTROL PDF 文件的 OCR]

此工具会对文件执行光学字符识别（OCR），并生成 PDF。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 语言]</td> 
   <td>选择此文档的语言。<p>有关语言选项，请参阅本文中的<a href="#convert-document-to-pdf-file" class="MCXref xref" >将文档转化为 PDF 文件</a>。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL OCR 类型]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL 已修改的原始图像]类型可确保文本可搜索、可选择，但会在清理过程中（例如校正倾斜）对原始图像进行修改，然后再在其上方放置一层不可见文本层。此类型会移除不需要的图像伪影，在某些情况下可生成更易阅读的文档。 </p> </li> 
     <li> <p>[!UICONTROL 未更改的原始图像]类型同样会在原始图像上叠加可搜索的文本层，但在此情况下，原始图像不会被修改。此类型可最大程度保持原始图像的真实外观。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 页面操作]

此模块允许您选择性地旋转或删除 PDF 文档中的页面。例如，您可以将纵向视图更改为横向视图，或从 PDF 文档中删除特定页面。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 操作]</td> 
   <td> <p>选择您希望对文件执行的操作。</p> 
    <ul> 
     <li> <p><b>[!UICONTROL 删除]</b> </p> <p>选择此选项以从文档中删除页面。</p><p>对于每个要删除的页面范围，点击<strong>[!UICONTROL 添加]</strong>，并输入该页面范围的起始页与结束页。 </p> <p>注意：   
     <ul> 
      <li> <p>您可以使用负数从文档末尾开始倒数页面。文档的最后一页为 -1，倒数第二页为 -2，以此类推。</p> </li> 
      <li> <p>若要删除单个页面，请将起始页与结束页设置为相同的页码。</p></ul> </li> 
     <li> <p><b>[!UICONTROL 旋转]</b> </p> <p>选择此选项以旋转页面，然后输入要相对于起始方向顺时针旋转的角度（以度为单位）。</p> <p>要将页面从纵向旋转为横向，或从横向旋转为纵向，请将页面旋转 90 度或 270 度。</p> <p>如果页面倒置，请旋转 180 度。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 页面]</td> 
   <td> <p>对于每个要删除的页面范围，点击<strong>[!UICONTROL 添加]</strong>，并输入该页面范围的起始页与结束页。 </p> <p>注意：   
     <ul> 
      <li> <p>您可以使用负数从文档末尾开始倒数页面。文档的最后一页为 -1，倒数第二页为 -2，以此类推。</p> </li> 
      <li> <p>若要删除单个页面，请将起始页与结束页设置为相同的页码。</p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td> <p>输入或映射模块在每次场景执行周期中可处理的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF 辅助功能自动标记]

此操作模块会创建一个包含辅助功能标签的 PDF，以支持辅助功能用例。此外，它还可生成一个可选的 Microsoft Excel 报告，用于列出问题并提供修复建议。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 调整标题]</td> 
   <td> <p>启用此选项可调整文档中的标题。</p> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 生成报告]</td> 
   <td> <p>启用此选项可生成报告，其中列出 PDF 中的辅助功能问题及其位置，并提供解决这些问题的建议。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL PDF 文件属性]

此工具会提取文档的基本信息，例如：

* 页数
* PDF 版本
* 文件是否已加密
* 文件是否已线性化
* 文件是否包含嵌入式文件

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 保护 PDF 文件]

此工具会使用用户密码或所有者密码来保护 PDF 文档。它还会为 PDF 文档中的某些功能（如打印、编辑、复制）设置限制。您可以选择要加密的内容类型以及加密算法。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须是 PDF 格式。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 密码保护类型]</td> 
   <td> <p>启用此选项以使用密码加密输入的 PDF 文档。如果启用此选项，您必须为以下一项或两项指定并输入值： </p> 
    <ul> 
     <li> <p>[!UICONTROL 用户密码]</p> </li> 
     <li> <p>[!UICONTROL 所有者密码] </p> </li> 
    </ul> <p>每个密码最长可达 128 个字符。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 加密算法]</td> 
   <td> <p>选择加密算法。 </p> 
    <ul> 
     <li> <p>[!UICONTROL AES-128 加密]</p> <p>密码仅支持 LATIN-I 字符。 </p> </li> 
     <li> <p>[!UICONTROL AES-256 加密]</p> <p>密码支持 Unicode 字符集。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 要加密的内容]</td> 
   <td> <p>选择要加密的内容类型。</p> 
    <ul> 
     <li> <p>[!UICONTROL 所有内容]</p> </li> 
     <li> <p>[!UICONTROL 除元数据以外的所有内容]</p> </li> 
     <li> <p>[!UICONTROL 仅嵌入数据] </p> </li> 
    </ul> <p>选择“[!UICONTROL 仅嵌入数据]”将使所有访问权限设置失效。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 权限]</td> 
   <td> <p>选择要包含的权限，以允许打印、编辑或复制内容。</p> <p>仅当在[!UICONTROL 所有者密码]字段中设置了[!UICONTROL 密码保护类型]时，权限设置才会生效。</p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 移除对 PDF 文件的保护]

此工具可移除 PDF 文档的安全设置（密码保护）。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须是 PDF 格式。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 密码]</td> 
   <td>输入当前用于保护该文件的密码。</td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL 拆分 PDF 文件]

此操作模块可将一个 PDF 文档拆分为多个较小的文档。您可以指定按文件数量、每个文件的页数或页码范围进行拆分。

<table style="table-layout:auto"> 
 <col> 
 </col> 
 <col> 
 </col> 
 <tbody> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>选择要用于此模块的连接。</p> 有关创建与 [!DNL Adobe PDF Services] 的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-pdf-services" class="MCXref xref" >创建与 [!DNL Adobe PDF Services]</a> 的连接。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 源文件]</td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> <p>源文件必须是 PDF 格式。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 拆分选项]</td> 
   <td>选择文件的拆分方式。 
   <ul>
   <li><p><b>页面范围</b></p><p>对于每个需要拆分为独立文档的页面范围，点击<b>添加</b>，并输入起始页和结束页。</p></li>
   <li><p><b>页数</b></p><p>输入您希望包含在新文档中的页数。</p></li>
   <li><p><b>文件数量</b></p><p>输入您希望将文档平均拆分成的文件数量。</p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

