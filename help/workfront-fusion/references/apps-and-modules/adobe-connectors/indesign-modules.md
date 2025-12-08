---
filename: adobe-indesign-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe InDesign模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Adobe InDesign的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
source-git-commit: 30ddefa8519e6f2052308482137d0fa018676902
workflow-type: tm+mt
source-wordcount: '1693'
ht-degree: 20%

---


# Adobe InDesign模块

在Adobe Workfront Fusion场景中，您可以自动使用Adobe InDesign的工作流，并将其连接到多个第三方应用程序和服务。

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

您必须先拥有有效的Adobe InDesign帐户，然后才能使用Adobe InDesign连接器。

## 创建与Adobe InDesign的连接

要为您的Adobe InDesign模块创建连接，请执行以下操作：

1. 在任意Adobe InDesign模块中，单击“连接”框旁边的&#x200B;**添加**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col>
      </col>
      <col>
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
        <td>
          <p>选择要连接生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">类型</td>
        <td>
          <p>选择连接服务帐户还是个人帐户。</p>
        </td>
      </tr>
        <tr>
          <td role="rowheader">客户端 ID</td>
          <td>输入您的Adobe客户端ID。 可在Adobe Developer Console的“凭据详细信息”部分找到此项</td>
        </tr>
        <tr>
          <td role="rowheader">客户端密钥</td>
          <td>输入您的Adobe客户端密钥。 可在Adobe Developer Console的“凭据详细信息”部分找到此项</td>
        </tr>
        <tr>
          <td role="rowheader">IMS 组织 ID</td>
          <td>输入您的Adobe组织ID。 可在Adobe Developer Console的“凭据详细信息”部分找到此项</td>
        </tr>
      </tbody>
    </table>
1. 点击&#x200B;**继续**&#x200B;保存连接并返回模块。

## InDesign模块及其字段

配置Adobe InDesign模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Adobe InDesign字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 操作

* [创建节目](#create-rendition)
* [删除自定义脚本](#delete-a-custom-script)
* [合并数据](#merge-data)
* [重新映射链接](#remap-links)
* [提交自定义脚本执行请求](#submit-a-custom-script-execution-request)

#### 创建节目

此操作模块创建并返回特定InDesign文档的JPEG、PNG或PDF演绎版。 有关`StatusCompletedRespons/output/data`的结构，请参阅`RenditionOutputData`。 有关`FailedEvent`中可能出现的错误代码列表，请参阅`RenditionFailedData`。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>类型</p>
      </td>
      <td>选择要创建的格式副本的文件类型。 
      <ul><li>JPEG</li><li>PNG</li><li>PDF</li></ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>资源</p>
      </td>
      <td>对于要添加到演绎版的每个资源：<ol><li>单击<b>添加项</b>。</li><li>选择或映射资源的源。</li><li>输入目标。 目标是相对于下载资源的临时基目录（工作目录）的路径。 这可以在参数中标识资源。 它不能使用“……”上传 或“/”。 应存在有效的文件名。</td>
    </tr>
    <tr>
      <td role="rowheader">目标文档</td>
      <td>输入或映射将处理和渲染的文档。 目前，一次仅支持一个文档。</td>
    </tr>
    <tr>
      <td role="rowheader">其他字段</td>
   <td>有关其他字段，请参阅模块中包含的信息。</td>     </tr>
  </tbody>
</table>

#### 删除自定义脚本

此操作模块删除单个注册的自定义脚本。 将永久删除脚本的所有版本。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>脚本名称</p>
      </td>
      <td>输入或映射要删除的脚本的名称。</td>
    </tr>
  </tbody>
</table>

#### 合并数据

此模块通过将CSV数据与InDesign模板合并来创建InDesign文档或PDF。 输出格式包括JPEG、PNG、PDF和InDesign文档。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>资源</p>
      </td>
      <td>对于要添加到数据合并的每个资产：<ol><li>单击<b>添加项</b>。</li><li>选择或映射资源的源。</li><li>输入目标。 目标是相对于下载资源的临时基目录（工作目录）的路径。 这可以在参数中标识资源。 它不能使用“……”上传 或“/”。 应存在有效的文件名。</td>
    </tr>
    <tr>
      <td role="rowheader">目标文档</td>
      <td>输入或映射要用作合并模板的文档。</td>
    </tr>
    <tr>
      <td role="rowheader">数据源</td>
      <td>输入或映射要使用的源文件。</td>
    </tr>
    <tr>
      <td role="rowheader">其他字段</td>
   <td>有关其他字段，请参阅模块中包含的信息。</td>     </tr>
  </tbody>
</table>

#### 重新映射链接

此模块将InDesign文档中的基于文件的链接替换为Adobe Experience Manager (AEM) URL。 这对于使用Adobe Asset Link的Adobe Experience Manager可能很有用。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
      </tr>
    <tr>
      <td role="rowheader">AEM令牌</td>
      <td>输入或映射为AEM技术帐户生成的持有者令牌，不带持有者关键字。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>资源</p>
      </td>
      <td>对于要添加到模块的每个资源：<ol><li>单击<b>添加项</b>。</li><li>选择或映射资源的源。</li><li>输入目标。 目标是相对于下载资源的临时基目录（工作目录）的路径。 这可以在参数中标识资源。 它不能使用“……”上传 或“/”。 应存在有效的文件名。</td>
    </tr>
    <tr>
      <td role="rowheader">目标文档</td>
      <td>输入或映射要在其中重新映射链接的文档。</td>
    </tr>
    <tr>
      <td role="rowheader">数据源</td>
      <td>输入或映射要用于提取和匹配标记的源文件。</td>
    </tr>
    <tr>
      <td role="rowheader">其他字段</td>
   <td>有关其他字段，请参阅模块中包含的信息。</td>     </tr>
  </tbody>
</table>

#### 提交自定义脚本执行请求

此操作模块提交自定义脚本的执行请求。 您可以定义自定义脚本在执行期间使用的输入资源和参数。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>脚本Id</p>
      </td>
      <td>输入或映射自定义脚本的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>资源</p>
      </td>
      <td>对于要为其提交执行请求的每个资产， <ol><li>单击<b>添加项</b>。</li><li>选择或映射资源的源。</li><li>输入目标。 目标是相对于下载资源的临时基目录（工作目录）的路径。 这可以在参数中标识资源。 它不能使用“……”上传 或“/”。 应存在有效的文件名。</td>
    </tr>
    <tr>
      <td role="rowheader">其他字段</td>
   <td>有关其他字段，请参阅模块中包含的信息。</td>     </tr>
  </tbody>
</table>

### 搜索

* [获取自定义脚本详细信息](#get-custom-script-details)
* [获取数据合并标记](#get-data-merge-tags)
* [获取文档信息](#get-document-information)
* [列出自定义脚本](#list-custom-scripts)

#### 获取自定义脚本详细信息

此搜索模块可检索单个已注册自定义脚本的详细信息，包括版本、下载链接、注册日期和脚本名称。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>脚本名称</p>
      </td>
      <td>输入或映射要检索其详细信息的脚本的名称。</td>
    </tr>
  </tbody>
</table>

#### 获取数据合并标记

此模块从文档检索数据合并标记。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>资源</p>
      </td>
      <td>对于要添加到模块的每个资源：<ol><li>单击<b>添加项</b>。</li><li>选择或映射资源的源。</li><li>输入目标。 目标是相对于下载资源的临时基目录（工作目录）的路径。 这可以在参数中标识资源。 它不能使用“……”上传 或“/”。 应存在有效的文件名。</td>
    </tr>
    <tr>
      <td role="rowheader">目标文档</td>
      <td>输入或映射要从中检索标记的文档。</td>
    </tr>
    <tr>
      <td role="rowheader">数据源</td>
      <td>输入或映射要用于提取和匹配标记的源文件。</td>
    </tr>
    <tr>
      <td role="rowheader">其他字段</td>
   <td>有关其他字段，请参阅模块中包含的信息。</td>     </tr>
  </tbody>
</table>

#### 获取文档信息

此模块可检索有关INDD/IDML文档的全面信息，并根据请求中指定的启用信息类型返回数据。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>资源</p>
      </td>
      <td>对于要添加到模块的每个资源：<ol><li>单击<b>添加项</b>。</li><li>选择或映射资源的源。</li><li>输入目标。 目标是相对于下载资源的临时基目录（工作目录）的路径。 这可以在参数中标识资源。 它不能使用“……”上传 或“/”。 应存在有效的文件名。</td>
    </tr>
    <tr>
      <td role="rowheader">目标文档</td>
      <td>输入或映射要从中检索信息的文档。</td>
    </tr>
     <tr>
      <td role="rowheader">其他字段</td>
   <td>有关其他字段，请参阅模块中包含的信息。</td>     </tr>
  </tbody>
</table>

#### 列出自定义脚本

此模块可检索所有已注册自定义脚本的最新版本的详细信息，包括版本、下载链接、注册日期和脚本名称。 结果根据列表长度进行分页。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
      </tr>
    <tr>
      <td role="rowheader">页码</td>
      <td>输入或映射要从中开始的页码。</td>
    </tr>
  <tr> 
   <td>返回结果的最大数目</td> 
   <td>设置Workfront Fusion在一个执行周期中返回的最大团队或组数。</td> 
  </tr> 
  </tbody>
</table>


### 其他 

#### 发起自定义 API 调用

此模块对Adobe InDesign API进行自定义API调用

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">连接</td>
      <td>有关创建与Adobe InDesign的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-indesign" class="MCXref_0">创建与Adobe InDesign的连接</a>。</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>路径</p>
      </td>
      <td>
        <p>输入相对于 <code>https://indesign.adobe.io/v3</code> 的路径。</p><p> 示例： <code>/create-rendition</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>方法</p>
      </td>
      <td>
        <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅[HTTP请求方法](/help/workfront-fusion/references/modules/http-request-methods.md)。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">标头</td>
      <td>
        <p>以标准 JSON 对象的形式添加请求标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion 会自动添加授权标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">查询字符串  </td>
      <td>
        <p>输入请求查询字符串。</p>
      </td>
    </tr>
  <tr> 
   <td role="rowheader">[!UICONTROL 正文]</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  </tbody>
</table>
