---
title: Google Docs模块
description: 通过Adobe Workfront Fusion [!DNL Google Docs] 模块，您可以在 [!DNL Google Docs] 和 [!DNL Google Docs] （对于 [!DNL Google Workspace] 用户）中监视、创建、编辑和检索文档。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: cd44250d-c2cd-46b2-8773-15b30472a8d8
source-git-commit: 2af808aaf8136253c623ee65641d0e57d4f6cf10
workflow-type: tm+mt
source-wordcount: '4045'
ht-degree: 0%

---

# [!DNL Google Docs]模块

通过[!DNL Adobe Workfront Fusion] [!DNL Google Docs]模块，您可以在[!DNL Google Docs]和[!DNL Google Docs]（针对[!DNL Google Workspace]用户）中监视、创建、编辑和检索文档。

要将[!DNL Google Docs]与[!DNL Adobe Workfront Fusion]一起使用，需要具有[!DNL Google]帐户。 如果您还没有[!DNL Google]帐户，则可以在[!DNL Google]帐户帮助页面中创建一个帐户。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

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
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[&#128279;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

要使用[!DNL Google Docs]模块，您必须拥有Google帐户。

## Google Docs API信息

Google Docs连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://docs.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.4.13</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Docs]模块及其字段

在配置[!DNL Google Docs]模块时，[!UICONTROL Workfront Fusion]显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Google Docs]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 文档

* [[!UICONTROL 创建文档]](#create-a-document)
* [[!UICONTROL 从模板创建文档]](#create-a-document-from-a-template)
* [[!UICONTROL 删除文档]](#delete-a-document)
* [[!UICONTROL 下载文档]](#download-a-document)
* [[!UICONTROL 获取文档的内容]](#get-content-of-a-document)
* [[!UICONTROL 向文档插入段落]](#insert-a-paragraph-to-a-document)
* [[!UICONTROL 将图像插入文档]](#insert-an-image-to-a-document)
* [[!UICONTROL 列出文档]](#list-documents)
* [[!UICONTROL 替换文档中的文本]](#replace-text-in-a-document)
* [[!UICONTROL 用新图像替换图像]](#replace-an-image-with-a-new-image)
* [[!UICONTROL 观看文档]](#watch-documents)

#### [!UICONTROL 创建文档]

此操作模块允许您在选定文件夹中创建新文档。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 名称] </td> 
   <td> <p>输入文档的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 内容]</td> 
   <td> <p>输入文档的内容。 您可以包含HTML来设置文档的格式。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要创建文档的驱动器类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>在“新建文档”的“位置”字段中，选择要创建文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>在“新建文档”的“位置”字段中，选择要创建文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要创建文档的共享驱动器。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 插入标头]</td> 
   <td> <p> 启用此选项可将页眉插入到文档，然后输入或映射页眉的文本。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 插入页脚] </td> 
   <td> <p>启用此选项可将页脚插入文档，然后输入或映射页眉的文本。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 从模板创建文档]

此操作模块会创建现有模板文档的副本并替换任何标记。 此模块还允许用户按URL将图像替换为新图像。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 从模板创建文档]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>选择此选项以映射文档模板。</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>选择此选项可从下拉菜单中选择文档模板。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择模板所在的驱动器类型。 如果您在上一个字段中选择了[!UICONTROL By Dropdown] ，则此选项可用。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p>  </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择模板所在的共享驱动器。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文档ID]</td> 
   <td> <p>如果您已选择按映射，请映射模板的ID，或者选择模板和模板的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Values]</p> </td> 
   <td> <p>对于要为其输入值的每个标记，单击<b>添加项</b>，输入该标记，然后输入将在新文档中输入的值而不是该标记。</p> 
    <ul> 
     <li><strong>[!UICONTROL 标记]</strong> <br>输入文档模板中包含的标记。 不要使用<code>&#123;&#123;&#125;&#125;</code>。 示例：使用<code>name</code>而不是<code>&#123;&#123;name&#125;&#125;</code>。</li> 
     <li><strong>[!UICONTROL 替换的值]</strong><br>输入标记的值。</li> 
    </ul> <p>例如，源文档中的<code> &#123;&#123;name&#125;&#125;</code>变量将显示为此处的name字段，可以插入该值，如<code>John</code>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 图像替换]</p> </td> 
   <td> <p>&gt;对于要输入值的每个标记，单击<b>添加项</b>，然后输入要替换当前图像的[!UICONTROL 图像对象ID]和[!UICONTROL 图像URL]链接。</p> <p>注意：您可以使用[!UICONTROL 获取文档]模块检索图像ID，其中ID包含在数组[!UICONTROL 内联对象数组]中。</p> <p>我们建议您向[!DNL Google]文档中的图像添加替换文字。 </p> <p>向[!DNL Google Docs]图像添加替换文本：</p> 
    <ol> 
     <li value="1">右键单击图像。</li> 
     <li value="2">选择[!UICONTROL 替换文本]选项。</li> 
     <li value="3">在[!UICONTROL 标题]字段中输入[!UICONTROL 替换文本]，然后单击[!UICONTROL 确定]。</li> 
    </ol> <p>将ALT文本添加到图像后，ALT文本显示在括号中的字段名称中。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标题] </td> 
   <td> <p>输入新文档的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择模板所在的驱动器类型。 如果您在上一个字段中选择了[!UICONTROL By Dropdown] ，则此选项可用。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择要创建文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择要创建文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要创建文档的共享驱动器。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除文档]

此操作模块删除文档。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要删除的文档所在的驱动器类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择要删除的文档所在的文件夹，然后选择该文档。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择要删除的文档所在的文件夹，然后选择该文档。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要删除的文档所在的共享驱动器，然后选择该文档。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 共享驱动器]</td> 
   <td> <p>选择包含要下载的文档的驱动器，然后选择文档。 如果您在[!UICONTROL 选择驱动器]字段中选择了[!DNL My Drive]，则此选项可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文档ID]</td> 
   <td> <p> 选择或映射要删除的文档。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 下载文档]

此操作模块转换并下载所选文档。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要下载的文档所在的驱动器类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>在“文档ID”字段中，选择要下载的文档所在的文件夹，然后选择该文档。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>在“文档ID”字段中，选择要下载的文档所在的文件夹，然后选择该文档。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要下载的文档所在的共享驱动器，然后选择该文档。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 类型] </p> </td> 
   <td> <p>选择下载文档的目标文件格式。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取文档的内容]

此操作模块检索指定文档。

您可能需要扩展您的权限。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Get Content of a Document]</td> 
   <td> <p>选择是要映射文档的文档ID，还是手动从下拉菜单中选择文档。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择包含要检索的文档的驱动器类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择包含要检索的文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择包含要检索的文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择包含要检索的文档的共享驱动器。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文档ID]</td> 
   <td> <p>输入或选择要检索的文档。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 筛选器]</p> </td> 
   <td> <p>选择您希望模块输出中返回的对象。</p> 
    <ul> 
     <li>[!UICONTROL Image]（默认）</li> 
     <li>[!UICONTROL Drawing]</li> 
     <li>[!UICONTROL 图表]</li> 
    </ul> <p>注意：  <p>要进一步映射这些对象，请在此模块的输出中使用[!UICONTROL Inline Objects Array]值（而不是[!UICONTROL inlineObjects]）。</p> <p>[!UICONTROL Inline Objects Array]对象按照它们在文档中的显示顺序排序。 这将使任何进一步的处理更容易。</p> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 向文档插入段落]

此操作模块可在现有文档中添加或插入新段落。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 选择文档]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>选择此选项以映射文档。</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>选择此选项可从下拉菜单中选择文档。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要添加段落的文档所在的驱动器类型。 如果您在上一个字段中选择了[!UICONTROL By Dropdown] ，则此选项可用。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择要添加段落的文档所在的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择要添加段落的文档所在的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要向其添加段落的文档所在的共享驱动器，然后选择该文档。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文档ID]</td> 
   <td> <p>映射或选择要插入文本的文档。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 插入段落]</p> </td> 
   <td> <p>选择希望新文本插入文档的方式。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL ，按位置规范]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL ，按索引]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL 索引]</strong> </p> <p>输入要插入文本的索引编号。 您可以使用[!UICONTROL Get a Document]模块检索索引号。</p> </li> 
         <li> <p><strong>[!UICONTROL 插入文本]</strong> </p> <p>输入要插入到文档的文本。</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL ，按区段ID]</strong> </p> <p>选择要插入文本内容的页眉和页脚，并输入要插入到相应字段中的文本。</p> <p>如果页眉或页脚已包含文本，则新文本将添加到现有文本之前。</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL ，附加到文档正文中]</strong> </p> <p>在文档正文内容的末尾附加输入的文本。</p> <p>新段落的样式将从当前插入索引处的段落中复制，包括列表和项目符号。</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL ，附加到区段（页眉和页脚）的末尾]</strong> </p> <p>选择要插入文本内容的页眉和页脚，并输入要插入到相应字段中的文本。</p> <p>如果页眉或页脚已包含文本，则新文本将添加到现有文本之后。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 附加文本]</td> 
   <td>输入或映射要附加到文档的文本</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 将图像插入文档]

此操作模块会将图像从URL插入到文档。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 选择文档]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>选择此选项以映射文档模板。</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>选择此选项可从下拉菜单中选择文档。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要添加图像的文档所在的驱动器类型。 如果您在上一个字段中选择了[!UICONTROL By Dropdown] ，则此选项可用。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择要添加图像的文档所在的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择要添加图像的文档所在的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要添加图像的文档所在的共享驱动器，然后选择文档。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文档ID]</td> 
   <td> <p>映射或选择要插入图像的文档。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 插入图像]</p> </td> 
   <td> <p>选择您希望新图像插入到文档中的方式。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL ，按位置规范]</strong> </p> 
      <ul> 
       <li> <p><strong>[!UICONTROL ，按索引]</strong> </p> 
        <ul> 
         <li> <p><strong>[!UICONTROL 索引]</strong> </p> <p>输入要插入图像的索引编号。 您可以使用[!UICONTROL Get a Document]模块检索[!UICONTROL 索引号]。</p>  </li> 
         <li> <p><strong>[!UICONTROL 图像URL]</strong> </p> <p>输入要插入文档的图像的URL。</p> <p>最大图像大小为50 MB。 不得超过2500万像素。 仅支持PNG、JPEG或GIF格式。</p> </li> 
        </ul> </li> 
       <li> <p><strong>[!UICONTROL ，按区段ID]</strong> </p> <p>选择要将图像插入到的页眉和页脚，并在相应的字段中输入图像URL。</p> <p>最大图像大小为50 MB。 图像不能超过2500万像素。 仅支持PNG、JPEG或GIF格式。</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL ，附加到文档正文中]</strong> </p> <p>在文档正文内容的末尾附加特定图像。</p> </li> 
    </ul> 
    <ul> 
     <li> <p><strong>[!UICONTROL ，附加到区段（页眉和页脚）的末尾]</strong> </p> <p>选择要插入图像的页眉和页脚，并输入要插入到相应字段的图像URL。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 高度模（以点为单位）/宽度模（以点为单位）]</p> </td> 
   <td> <p>定义插入图像的高度或宽度。 将保持宽高比。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出文档]

此操作模块从选定的文件夹中检索文档列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要从中列出文档的驱动器类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择要从中列出文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择要从中列出文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要从中列出文档的共享驱动器。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>设置在一个执行周期中返回的最大文档数[!DNL Workfront Fusion]。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 替换文档中的文本]

此操作模块替换文档中的文本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 选择文档]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>选择此选项以映射文档模板。</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>选择此选项可从下拉菜单中选择文档。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要向其添加文本的文档所在的驱动器类型。 如果您在上一个字段中选择了[!UICONTROL By Dropdown] ，则此选项可用。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择要向其添加文本的文档所在的文件夹，然后选择该文档。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择要向其添加文本的文档所在的文件夹，然后选择该文档。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要向其添加文本的文档所在的共享驱动器，然后选择该文档。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文档ID]</td> 
   <td> <p>映射或选择要替换文本的文档。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 替换文本]</p> </td> 
   <td> <p>对于要替换的每段文本，单击<b>添加项</b>并输入以下内容：</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 要替换的旧文本]</strong> </p> <p>输入要替换的文本。</p> </li> 
     <li> <p><strong>[!UICONTROL 要插入的新文本]</strong> </p> <p>输入新文本。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
 </table>

#### [!UICONTROL 用新图像替换图像]

此操作模块替换现有图像。 将保持原始图像的纵横比。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 选择文档]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>选择此选项以映射文档模板。</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>选择此选项可从下拉菜单中选择文档。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要替换图像的文档所在的驱动器类型。 如果您在上一个字段中选择了[!UICONTROL By Dropdown] ，则此选项可用。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择要替换图像的文档所在的文件夹，然后选择该文档。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择要替换图像的文档所在的文件夹，然后选择该文档。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要替换图像的文档所在的共享驱动器，然后选择该文档。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文档ID]</td> 
   <td> <p>映射或选择要替换图像的文档。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL 图像替换]</p> </td> 
   <td> 对于每个要替换的图像，单击<b>添加项</b>并输入现有图像ID，然后输入或映射将替换现有图像的新图像的URL。 <p>图像按其在文档中的显示顺序列出。 例如，<code>Body: Image No. 1</code>是文档中的第一个图像。</p> </td> 
  </tr> 
 </tbody> 
</table>
</table>

#### [!UICONTROL 观看文档]

在所选文件夹中创建或修改新文档时，此触发器模块返回文档详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Watch文档]</td> 
   <td> <p style="color: #000000;">选择您是要观看已创建的([!UICONTROL By Created Date])文档还是已修改的([!UICONTROL By Modified Date])文档。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要监视的驱动器类型。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择要监视创建或修改文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择要监视创建或修改文档的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要监视的共享驱动器。</p> <p>注意：如果您在此字段中选择了[!DNL Google Shared Drive]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制] </td> 
   <td> <p>设置Workfront Fusion在一个执行周期中返回的最大文档数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

* [[!UICONTROL 使文档中的所有链接都可点击]](#make-all-links-in-a-document-clickable)
* [[!UICONTROL 进行API调用]](#make-an-api-call)

#### [!UICONTROL 使文档中的所有链接都可点击]

此操作模块查找文档中的所有链接并使它们可点击。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Make All Links in a Document]</p> </td> 
   <td> 
    <ul> 
     <li><strong>[!UICONTROL By Mapping]</strong> <br>选择此选项以映射文档模板。</li> 
     <li><strong>[!UICONTROL By Dropdown]</strong> <br>选择此选项可从下拉菜单中选择文档。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 选择驱动器]</td> 
   <td> <p>选择要使链接可点击的文档所在的驱动器类型。 如果您在上一个字段中选择了[!UICONTROL By Dropdown] ，则此选项可用。</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL 我的驱动器]</strong> </p> <p>选择要使链接可点击的文档所在的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL 已与我共享]</strong> </p> <p>选择要使链接可点击的文档所在的文件夹。</p> </li> 
     <li> <p><strong>[!UICONTROL [!DNL Google]共享驱动器]</strong> （仅适用于[!DNL Google Workspace]用户）</p> <p>选择是否希望[!UICONTROL 使用域管理员访问权限]。 选择[!UICONTROL 是]会以域管理员身份发出请求，并且会返回请求者是管理员的所有共享驱动器。</p> <p>选择要使链接可点击的文档所在的共享驱动器，然后选择该文档。</p> <p>注意：如果您在此字段中选择了[!DNL Google Docs]选项，并且您不是[!DNL Google Workspace]用户，则会返回错误<code>[400] Invalid Value</code>。</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 共享驱动器]</td> 
   <td> <p>选择包含要更新链接的文档的驱动器，然后选择文档。 如果您在[!UICONTROL 选择驱动器字段]中选择了[!DNL My Drive]，则此选项可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 文档ID]</td> 
   <td> <p> 选择或映射要更新链接的文档。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 进行API调用]

此操作模块允许您执行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref">创建连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td> <p>输入相对于<code>https://docs.googleapis.com/</code>的路径。 示例： <code>/v1/documents/{presentationID}</code>。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 例如，<code>{"Content-type":"application/json"}</code>。 [!DNL Workfront Fusion]为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p> 输入请求查询字符串。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**&#x200B;以下API调用检索Google Docs中指定文档的详细信息：

**URL：**

/v1/documents/1ujkf-GDgB0TQSYPrxbCSK4Uso54tHVMqHZEVZZxB6aY

**方法：**

[!UICONTROL GET]

![API调用示例](/help/workfront-fusion/references/apps-and-modules/assets/api-call-example.png)

在[!UICONTROL 包] > [!UICONTROL 正文]下的模块输出中可找到检索文档的详细信息。

![API调用输出](/help/workfront-fusion/references/apps-and-modules/assets/api-output.png)

>[!ENDSHADEBOX]
