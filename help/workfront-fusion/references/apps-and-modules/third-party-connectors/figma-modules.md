---
title: 图形模块
description: 使用Adobe Workfront Fusion Figma模块，您可以检索注释、文件、文件版本或项目的列表。 您还可以向Figma API发布评论或进行调用。
author: Becky
feature: Workfront Fusion
exl-id: 1220460b-1957-4dfc-b7c1-4c97b36ea061
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2594'
ht-degree: 0%

---

# [!DNL Figma]模块

使用Adobe Workfront Fusion [!DNL Figma]模块，您可以检索注释、文件、文件版本或项目的列表。 您还可以向[!DNL Figma] API发布评论或进行调用。

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
   <p>当前：无Workfront Fusion许可证要求</p>
   <p>或</p>
   <p>旧版：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

要使用[!DNL Figma]模块，您必须具有[!DNL Figma]帐户。

## 图API信息

Figma连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td> https://api.figma.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.8.25</td> 
  </tr>
 </tbody> 
 </table>

## 创建与Figma的连接

要为您的Figma模块创建连接：

1. 在任意Figma模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

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
          <p> 对于新连接，选择<code>Figma</code>而不使用旧标记。 </p><p>Figma于2025年1月更改了身份验证要求。 <code>Figma</code>连接类型符合新要求。 未来将删除<code>Figma (Legacy)</code>连接类型。</p>
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
        <td>输入您的[！UICONTROL数字] [！UICONTROL客户端ID]。</td>
        </tr>
        <tr>
        <td role="rowheader">[！UICONTROL客户端密钥]</td>
        <td>输入您的Figma [！UICONTROL客户端密钥]。</td>
        </tr>
        <tr>
        <td role="rowheader">自定义范围</td>
        <td>输入此连接所需的任何自定义范围。</td>
        </tr>
        <tr>
        <td role="rowheader">自定义连接验证URL</td>
        <td>验证连接是否成功创建的默认终结点为： <code>https://api.figma.com/v1/me</code>如果自定义范围不支持此URL，请提供自定义验证URL。</td>
        </tr>
      </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。



## [!DNL Figma]模块及其字段

在配置[!DNL Figma]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Figma]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [评论](#comments)

* [项目和文件](#projects-and-files)

* [组件和样式](#components-and-styles)

* [其他](#other)


### 评论

* [删除评论](#delete-a-comment)

* [列出注释](#list-comments)

* [发表评论](#post-a-comment)


#### [!UICONTROL 删除评论]

此操作模块从文件删除单个注释。

<table style="table-layout:auto"> 
  <col/>
  <col />
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td> <p>有关将[!DNL Figma]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">创建与Figma的连接</a>。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL文件ID]</td>
      <td>输入或映射要添加或删除注释的文件的文件ID。 </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL注释ID]</td>
      <td>输入要删除的注释的文本。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 列出评论]

此搜索模块列出了附加到[!DNL Figma]中单个文件的所有注释。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td> <p>有关将[!DNL Figma]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">创建与Figma的连接</a>。</p>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL文件ID]</td>
      <td>
        <p>输入或映射要为其检索注释的文件的文件ID。 </p>
        <ul>
          <li>
            <p>如果您不知道该ID，请单击<b>[！UICONTROL查找文件]</b>，然后输入或映射与该文件关联的项目的ID，然后选择该文件。</p>
          </li>
          <li>
            <p>如果您不知道项目的ID，请单击<b>[！UICONTROL查找项目]</b>，然后输入或映射拥有该文件所关联项目的团队的ID，然后选择该项目，然后选择该文件。</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL返回的最大评论数]</td>
      <td>输入或映射您希望模块在每个方案执行周期中返回的最大注释数。</td>
    </tr>
  </tbody>
</table>


#### [!UICONTROL 发表评论]

此操作模块向Figma文件发布评论。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td> <p>有关将[!DNL Figma]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">创建与Figma的连接</a>。</p>
    </tr>
    <tr>
      <td  role="rowheader">[！UICONTROL文件ID]</td>
      <td>
        <p>输入或映射要向其发布注释的文件的文件ID。 </p>
        <ul>
          <li>
            <p>如果您不知道文件的ID，请单击<b>[！UICONTROL查找文件]</b>，然后输入或映射与文件关联的项目的ID，然后选择该文件。</p>
          </li>
          <li>
            <p>如果您尝试查找文件的ID但不知道项目的ID，请单击<b>[！UICONTROL查找项目]</b>，然后输入或映射拥有该文件关联的项目的团队的ID。 选择项目，然后选择文件。</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Comment]</td>
      <td>输入注释的文本。</td>
    </tr>
  </tbody>
</table>


### 项目和文件

* [获取文件或图像](#get-a-file-or-image)

* [列出文件版本历史记录](#list-file-version-history)

* [列出项目文件](#list-project-files)

* [列出项目](#list-projects)


#### [!UICONTROL 获取文件或图像]

此操作模块从Figma库中检索单个文件或图像

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td> <p>有关将[!DNL Figma]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">创建与Figma的连接</a>。</p>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL对象类型]</td>
      <td>
        <p>选择要检索的对象类型。</p>
        <ul>
          <li>
            <p><b>[！UICONTROL文件]</b>
            </p>
            <p>模块会返回由[！UICONTROL Key]引用的文档作为JSON对象。 可以从任何Figma文件URL解析文件密钥。</p>
            <p>有关字段，请参阅<a href="#get-a-file-or-image-file" class="MCXref xref" >[！UICONTROL获取文件或图像：文件]</a>。</p>
          </li>
          <li>
            <p><b>[！UICONTROL文件节点]</b>
            </p>
            <p>将ID引用的节点作为JSON对象返回。 从[！UICONTROL Key]引用的[!DNL Figma]文件中检索节点。</p>
            <p>有关字段，请参阅<a href="#get-a-file-or-image-file-nodes" class="MCXref xref" >[！UICONTROL获取文件或图像：文件节点]</a>。</p>
          </li>
          <li>
            <p><b>[！UICONTROL图像]</b>
            </p>
            <p>模块从文件渲染图像。</p>
            <p>有关字段，请参阅<a href="#get-a-file-or-image-image" class="MCXref xref" >[！UICONTROL获取文件或图像：图像]</a>。</p>
          </li>
          <li>
            <p><b>[！UICONTROL图像填充]</b>
            </p>
            <p>模块会返回文档图像填充中存在的所有图像的下载链接。 图像填充是[!DNL Figma]表示任何用户提供的图像的方式。 将图像拖入[!DNL Figma]中时，[!DNL Figma]会创建一个矩形，其中只有一个填充代表图像，用户能够转换矩形（和填充上的属性）。</p>
            <p>有关字段，请参阅<a href="#get-a-file-or-image-image-fills" class="MCXref xref" >[！UICONTROL获取文件或图像：图像填充]</a>。</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>


##### 获取文件或图像：文件

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL文件键]</td>
      <td>选择要从中返回JSON的文件。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL版本ID]</td>
      <td>输入或映射您希望模块返回的文件版本。 对于当前模块，请将此字段留空。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL节点ID]</td>
      <td>
        <p>要仅返回文档的子集，请输入您希望模块返回的节点。 该模块会返回列出的节点、它们的子节点以及根节点与列出的节点之间的任何内容。</p>
        <p>对于每个要返回的节点，单击<b>[！UICONTROL添加]</b>并输入节点的文本。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL深度]</td>
      <td>
        <p>输入或映射一个整数，该整数表示在文档树中要返回结果的深度。 </p>
        <div class="example"><span class="autonumber"><span><b>示例： </b></span></span>
          <ul>
            <li>
              <p>要仅返回页面，请输入<code>1</code>。</p>
            </li>
            <li>
              <p>要返回页面和顶级对象，请输入<code>2</code>。</p>
            </li>
          </ul>
        </div>
        <p>要返回所有节点，请将此字段留空。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Geometry]</td>
      <td>若要返回矢量数据，请输入<code>paths</code>。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL插件数据]</td>
      <td>插件ID和/或字符串“[！UICONTROL shared]”的逗号分隔列表。 由这些插件编写的文档中存在的任何数据都将包含在<code>pluginData</code>和<code>sharedPluginData</code>属性的结果中。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL分支数据]</td>
      <td>启用此选项可返回所请求文件的分支元数据。 如果文件是分支，则主文件的密钥包含在返回的响应中。 如果文件具有分支，则其元数据将包含在返回的响应中。 默认值： <code>false</code>。</td>
    </tr>
  </tbody>
</table>

##### 获取文件或图像：文件节点

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL文件键]</td>
      <td>选择要从中返回JSON的文件。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL节点ID]</td>
      <td>
        <p>输入您希望模块返回并转换的节点</p>
        <p>对于每个要返回的节点，单击<b>[！UICONTROL添加]</b>并输入节点的文本。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL版本ID]</td>
      <td>输入或映射您希望模块返回的文件版本。 对于当前模块，请将此字段留空。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL深度]</td>
      <td>
        <p>输入或映射一个整数，该整数表示在文档树中要返回结果的深度。 </p>
        <div class="example"><span class="autonumber"><span><b>示例： </b></span></span>
          <ul>
            <li>
              <p>要仅返回页面，请输入<code>1</code>。</p>
            </li>
            <li>
              <p>要返回页面和顶级对象，请输入<code>2</code>。</p>
            </li>
          </ul>
        </div>
        <p>要返回所有节点，请将此字段留空。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Geometry]</td>
      <td>若要返回矢量数据，请输入<code>paths</code>。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL插件数据]</td>
      <td>插件ID和/或字符串“shared”的逗号分隔列表。 由这些插件编写的文档中存在的任何数据都将包含在pluginData和sharedPluginData属性的结果中。</td>
    </tr>
  </tbody>
</table>


##### 获取文件或图像：图像

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL文件键]</td>
      <td>选择要从中返回JSON的文件。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL节点ID]</td>
      <td>
        <p>输入您希望模块呈现的节点。</p>
        <p>对于要渲染的每个节点，单击<b>[！UICONTROL添加]</b>并输入节点的文本。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL缩放]</td>
      <td>要缩放图像，请输入或映射缩放因子。 此数字必须介于0.01和4之间。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL格式]</td>
      <td>
        <p>选择图像输出的格式。</p>
        <ul>
          <li>
            <p>JPG</p>
          </li>
          <li>
            <p>PNG</p>
          </li>
          <li>
            <p>SVG</p>
          </li>
          <li>
            <p>PDF</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL SVG — 包含ID]</td>
      <td>启用此选项可包含所有SVG元素的ID属性。 默认值： [！UICONTROL false]。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL SVG — 简化描边]</td>
      <td>启用此选项可简化内/外描边并使用描边属性（如果可能）而不是&lt;mask&gt;。 默认值： [！UICONTROL true]。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL使用绝对边界]</td>
      <td>启用此选项可使用节点的完整尺寸，无论是否裁剪节点或节点周围的空间为空。 使用此项导出文本节点而不进行裁剪。 默认值： [！UICONTROL false]。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL版本]</td>
      <td>输入或映射您希望模块返回的文件版本。 对于当前模块，请将此字段留空。</td>
    </tr>
  </tbody>
</table>

##### 获取文件或图像：图像填充

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL文件键]</td>
      <td>选择要从中返回JSON的文件。</td>
    </tr>
  </tbody>
</table>

### [!UICONTROL 列出文件版本历史记录]

此搜索模块返回[!UICONTROL Figma]中单个文件的版本历史记录。
<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td> <p>有关将[!DNL Figma]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">创建与Figma的连接</a>。</p>
    <tr>
      <td role="rowheader">[！UICONTROL文件ID]</td>
      <td>
        <p>输入或映射要检索其版本历史记录的文件的文件ID。 </p>
        <ul>
          <li>
            <p>如果您不知道文件的ID，请单击<b>[！UICONTROL查找文件]</b>，然后输入或映射与文件关联的项目的ID，然后选择该文件。</p>
          </li>
          <li>
            <p>如果您尝试查找文件的ID但不知道项目的ID，请单击<b>[！UICONTROL查找项目]</b>，然后输入或映射拥有该文件关联的项目的团队的ID。 选择项目，然后选择文件。</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL返回的最大文件数]</td>
      <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 列出项目文件]

此搜索模块返回指定项目中所有文件的列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td> <p>有关将[!DNL Figma]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">创建与Figma的连接</a>。</p>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL文件ID]</td>
      <td>
        <p>输入或映射要为其检索文件的项目的项目ID。 </p>
        <ul>
          <li>
            <p>如果您不知道项目的ID，请单击<b>[！UICONTROL查找项目]</b>，然后输入或映射与项目关联的团队的ID，然后选择该项目。</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL返回的最大文件数]</td>
      <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL 列出项目]

此搜索模块返回指定团队中所有项目的列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td> <p>有关将[!DNL Figma]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">创建与Figma的连接</a>。</p>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL团队ID]</td>
      <td>输入或映射要检索其文件的项目的项目ID。 团队ID可在Figma中的团队页面URL中找到</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL返回的最大项目数]</td>
      <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td>
    </tr>
  </tbody>
</table>


### 组件和样式

#### [!UICONTROL 获取样式或组件]

此操作模块可检索单个样式或组件，或一组样式或组件。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td> <p>有关将[!DNL Figma]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">创建与Figma的连接</a>。</p>
    </tr>
    <tr>
      <td role="rowheader">对象&gt;类型</td>
      <td>选择要检索的对象类型。</td>
    </tr>
    <tr>
      <td role="rowheader">&lt;[！UICONTROL Object&gt;键]</td>
      <td>输入要检索的对象的键（唯一标识符）。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL团队ID]</td>
      <td>如果检索团队组件或团队组件集，请输入或映射与记录关联的团队的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL页面大小]</td>
      <td>如果检索团队组件或团队组件集，请输入或映射每页要返回的数量或结果。 默认值：30。</td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL After]</td>
      <td>
        <p>如果检索团队组件或团队组件集，请输入或映射结果编号，之后将开始检索结果。 可以与[！UICONTROL Page Size]字段结合使用来对结果进行分页。</p>
        <p>此值未与对象ID相对应。</p>
        <p>此字段不能与[！UICONTROL Before]字段结合使用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Before]</td>
      <td>
        <p>如果检索团队组件或团队组件集，请输入或映射要开始检索结果的结果数量。 可以与[！UICONTROL Page Size]字段结合使用来对结果进行分页。</p>
        <p>此值未与对象ID相对应。</p>
        <p>此字段不能与[！UICONTROL After]字段结合使用。</p>
      </td>
    </tr>
  </tbody>
</table>


### 其他

* [进行API调用](#make-an-api-call)

* [观看活动](#watch-events)


#### [!UICONTROL 进行API调用]

通过此操作模块，您无需考虑身份验证，即可对Figma API进行经过身份验证的自定义调用。 这样，您可以创建其他图形模块无法实现的数据流自动化。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Connection]</td>
      <td> <p>有关将[!DNL Figma]帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#create-a-connection-to-figma" class="MCXref xref" data-mc-variable-override="">创建与Figma的连接</a>。</p>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL URL]</td>
      <td>
        <p>输入相对于<code>https://api.figma.com/v1/</code>的路径。</p>
        <p>例如： <code>[!DNL files/7179110/comments]</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL方法]</td>
      <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion会为您添加授权标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL查询字符串]</td>
      <td>
        <p>以标准JSON对象的形式添加API调用的查询。</p>
        <p>例如： <code>{"name":"something-urgent"}</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[！UICONTROL Body]</td>
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

#### [!UICONTROL 观看活动]

当您的[!DNL Figma]团队空间中的特定团队发生以下事件之一时，此触发器模块将启动一个方案：

* 文件更新

* 文件版本更新

* 文件删除

* 库发布

* 文件注释

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[！UICONTROL Webhook]</td>
      <td>
        <p>选择模块监视的webhook。</p>
        <p>要添加新的webhook，请执行以下操作：</p>
        <ol>
          <li>
            <p>单击[！UICONTROL Webhook]字段旁边的<b>[！UICONTROL Add]</b>。</p>
          </li>
          <li>
            <p>输入webhook的名称。</p>
          </li>
          <li>
            <p>选择要用于此webhook的连接。 有关将[!DNL Figma]帐户连接到[！UICONTROL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[！UICONTROL Adobe Workfront Fusion]的连接 — 基本说明。</a></p>
          </li>
          <li>
            <p>选择您希望模块监视的事件类型。</p>
          </li>
          <li>
            <p>输入希望webhook观看其事件的团队的ID。</p>
          </li>
          <li>
            <p>选择是希望激活还是暂停webhook。</p>
          </li>
          <li>
            <p>输入webhook的说明。</p>
          </li>
          <li>
            <p>单击<b>[！UICONTROL保存]</b>以保存webhook并返回模块。</p>
          </li>
        </ol>
      </td>
    </tr>
  </tbody>
</table>
