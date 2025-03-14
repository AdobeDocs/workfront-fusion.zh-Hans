---
title: Google幻灯片模块
description: Adobe Workfront Fusion Google幻灯片模块允许您创建、更新、列出和/或删除演示文稿，并将图像上传到Google Slides帐户中的演示文稿。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 6f5f97b9-b06a-4336-b349-ee9e2606d4bf
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1970'
ht-degree: 0%

---

# [!DNL Google Slides]模块

[!DNL Adobe Workfront Fusion] [!DNL Google Slides]模块允许您创建、更新、列出和/或删除演示文稿，并将图像上载到您[!DNL Google Slides]帐户中的演示文稿。

要将[!DNL Google Slides]与[!DNL Workfront Fusion]一起使用，需要具有[!DNL Google]帐户。 如果您还没有[!DNL Google]帐户，则可以在[!DNL Google]帐户帮助页面中创建一个帐户。

您的[!DNL Google Drive]中还需要[!DNL Google Slides]。

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

要使用[!DNL Google Slides]模块，您必须具有[!DNL Google]帐户。

## Google幻灯片API信息

Google幻灯片连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://slides.googleapis.com/v1</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.5.9</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Google Slides]模块及其字段

在配置[!DNL Google Slides]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Google Slides]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [演示文稿](#presentation)
* [其他](#other)

### 演示文稿

* [[!UICONTROL 添加/删除幻灯片]](#adddelete-a-slide)
* [[!UICONTROL 从模板创建演示文稿]](#create-a-presentation-from-a-template)
* [[!UICONTROL 获取页面/缩略图]](#get-a-pagethumbnail)
* [[!UICONTROL 获取演示文稿]](#get-a-presentation)
* [[!UICONTROL 列出演示文稿]](#list-presentations)
* [[!UICONTROL 刷新图表]](#refresh-a-chart)
* [[!UICONTROL 将图像上载到演示文稿]](#upload-an-image-to-a-presentation)
* [[!UICONTROL 观看演示文稿]](#watch-presentations)

#### [!UICONTROL 添加/删除幻灯片]

此操作模块创建幻灯片或删除指定演示文稿上的现有幻灯片。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择方法]</td> 
   <td> <p>选择您要添加新幻灯片还是删除幻灯片。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Enter a Slide ID]</td> 
   <td> <p>如果要删除幻灯片，请选择是要手动输入幻灯片ID，还是从列表中选择幻灯片。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Presentation ID]</td> 
   <td> <p>选择演示文稿或映射要为其添加或删除幻灯片的演示文稿的演示文稿ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Slide Object ID]</td> 
   <td> <p>如果要删除幻灯片并选择手动输入幻灯片，请输入或映射幻灯片ID。 </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL预定义的布局类型]</td> 
   <td> <p> 选择您希望添加的幻灯片使用的预定义幻灯片布局。 为任何其他字段指定值（如[！UICONTROL Title]）。</p> 
    <ul> 
     <li>[！UICONTROL空白布局，无占位符]</li> 
     <li>[！UICONTROL布局，底部有标题]</li> 
     <li>带有标题和子标题的[！UICONTROL布局]</li> 
     <li>带有标题和正文的[！UICONTROL布局]</li> 
     <li>[！UICONTROL布局，带标题和两列]</li> 
     <li>[！UICONTROL仅带标题的布局]</li> 
     <li>[！UICONTROL带分区标题的布局]</li> 
     <li>[！UICONTROL布局，标题和副标题位于一侧，描述位于另一侧]</li> 
     <li>[！UICONTROL布局，有一个标题和一个正文，排列在一列中]</li> 
     <li>带有主点的[！UICONTROL布局]</li> 
     <li>[!DNL Layout with a big number heading]</li> 
    </ul> <p>如果您选择添加幻灯片，则此字段可用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Content]</td> 
   <td> <p>输入或映射幻灯片的文本内容。 根据您选择的模板，字段可用。</p> <p>如果您选择添加幻灯片，则此字段可用。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 从模板创建演示文稿]

此操作模块通过复制演示文稿，并将中的所有标记（如`{{Name}}`、`{{Email}}`）替换为提供的数据来创建新演示文稿。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL标题] </td> 
   <td> <p>输入新演示文稿的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL复制演示]</td> 
   <td> <p> 如果要复制现有演示文稿，请选择选项：</p> 
    <ul> 
     <li>[！UICONTROL By Mapping]</li> 
     <li>[！UICONTROL By下拉列表]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL现有演示文稿ID的副本]</td> 
   <td> <p> 输入要复制的现有演示文稿的路径或演示文稿ID。 如果您正在创建演示文稿[！UICONTROL By Mapping] ，则会显示此字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择驱动器]</td> 
   <td> <p>选择要列出的演示文稿所在的[!DNL Google Drive]：</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
     <li>[！UICONTROL [!DNL Google]共享驱动器]</li> 
    </ul> <p>如果您正在创建演示文稿[！UICONTROL By Dropdown] ，则会显示此字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL演示文稿ID]</td> 
   <td> <p> 选择演示文稿，或者输入或映射要用作模板的演示文稿ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Values] </td> 
   <td> <p>添加值：</p> 
    <ul> 
     <li><strong>[！UICONTROL标记]</strong>：输入要在演示文稿中替换的标记。 例如， <code>&#123;&#123;Name&#125;&#125;</code></li> 
     <li><strong>[！UICONTROL替换的值]</strong>：输入要替换现有标记的值。 例如，如果演示文稿中的字符串<code>&#123;&#123;Name&#125;&#125;</code>和替换的值是“示例”，则<code>&#123;&#123;Name&#125;&#125;</code>将被替换为<code>Sample</code>。</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL新驱动器位置]</td> 
   <td> <p>选择要存储或添加新演示文稿的[!DNL Google Drive]：</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
     <li>[！UICONTROL [!DNL Google]共享驱动器]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL新文档的位置]</p> </td> 
   <td> <p>选择要存储或添加演示文稿的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL已共享] </td> 
   <td> <p>选择是否要共享演示文稿。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL与他人电子邮件地址共享]</td> 
   <td> <p> 输入要与其共享演示文稿的电子邮件地址。 如果启用“共享”选项而没有在此字段中输入电子邮件，则演示文稿可与任何人共享。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取页面/缩略图]

此操作模块获取指定页面或演示文稿中页面缩略图的最新版本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入演示文稿和页面ID]</td> 
   <td> <p> 选择是手动输入演示文稿和页面ID，还是从列表中选择它们。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL演示文稿ID]</td> 
   <td> <p> 选择要检索的演示文稿ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL页面对象ID]</td> 
   <td> <p> 选择要查看其页面对象详细信息的幻灯片。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL显示页面缩略图]</td> 
   <td> <p> 如果要查看页面缩略图信息，请选中复选框。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取演示文稿]

此操作模块获取指定演示文稿的最新版本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择驱动器]</td> 
   <td> <p>选择要列出的演示文稿所在的[!DNL Google Drive]：</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
     <li>[！UICONTROL [!DNL Google]共享驱动器]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL演示文稿ID]</td> 
   <td> <p> 选择要检索的演示文稿。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出演示文稿]

本模块将检索给定位置的所有演示文稿的列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择驱动器位置]</td> 
   <td> <p>选择要列出的演示文稿所在的[!DNL Google Drive]：</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
     <li>[！UICONTROL [!DNL Google]共享驱动器]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文件夹ID]</td> 
   <td> <p>选择要列出的演示文稿的文件夹位置。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射您希望模块在一个方案执行周期内返回的最大演示文稿数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 刷新图表]

该操作模块刷新存储在ID指定的演示文稿中的图表数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL输入演示ID]</td> 
   <td> <p> 选择是手动输入演示文稿ID，还是从列表中选择它。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择驱动器]</td> 
   <td> <p>如果从列表中选择演示文稿，请选择您要列出的演示文稿所在的[!DNL Google Drive]：</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
     <li>[！UICONTROL [!DNL Google]共享驱动器]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL演示文稿ID]</td> 
   <td> <p>选择演示文稿，或者输入或映射包含要刷新图表的演示文稿ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL图表对象ID]</td> 
   <td> <p> 如果手动输入数据，请输入或映射要刷新图表的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 将图像上载到演示文稿]

上载包含所提供数据的图像。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择演示]</td> 
   <td> <p>选择您要选择图像上传到的演示文稿的方式。</p> 
    <ul> 
     <li>[！UICONTROL By Mapping]</li> 
     <li>[!DNL By Dropdown]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择驱动器]</td> 
   <td> <p>如果从下拉列表中选择，则选择要将图像添加到的演示文稿所在的[!DNL Google Drive]：</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
     <li>[！UICONTROL [!DNL Google]共享驱动器]</li> 
    </ul>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL演示文稿ID]</td> 
   <td> <p> 选择要将图像上传到的演示文稿的演示文稿ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择方法]</td> 
   <td> <p> 选择要如何替换图像。</p>
   <ul>
   <li><p><b>通过替换文本标记上载图像</b></p><p>在“值”字段中，对于要上载的每个图像，单击“添加项”<b></b>，然后输入该图像的标记和新图像的URL。</p></li>
   <li><p><b>通过替换图像上载图像</b></p><p>在“值”字段中，对于要上载的每个图像，单击“添加项”<b></b>，然后输入图像的对象ID、替换方法和新图像的URL。</p></li>
   </ul>
  <p>注意：图像大小必须小于50MB，不能超过2500万像素，并且必须采用PNG、JPEG或GIF格式。</p>   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看演示文稿]

此触发器模块会在创建或更新新演示文稿时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL监视] </td> 
   <td> <p>选择观看演示文稿的选项：</p> 
    <ul> 
     <li> <p>[！UICONTROL创建日期]</p> </li> 
     <li> <p>[！UICONTROL修改日期]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL限制]</td> 
   <td> <p>输入或映射Workfront Fusion在一个场景执行周期内应返回的最大演示文稿数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 其他

* [[!UICONTROL 在演示文稿中插入链接]](#insert-links-in-a-presentation)
* [[!UICONTROL 进行API调用]](#make-an-api-call)

#### [!UICONTROL 在演示文稿中插入链接]

此模块使演示文稿中的所有链接均可点击，或将链接插入到所有匹配的输入文本中。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择演示]</td> 
   <td> <p>选择您要选择图像上传到的演示文稿的方式。</p> 
    <ul> 
     <li>[！UICONTROL By Mapping]</li> 
     <li>[！UICONTROL By下拉列表]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择驱动器]</td> 
   <td> <p>选择要列出的演示文稿所在的[!DNL Google Drive]：</p> 
    <ul> 
     <li>[！UICONTROL我的驱动器]</li> 
     <li>[！UICONTROL与我共享]</li> 
     <li>[！UICONTROL [!DNL Google]共享驱动器]</li> 
    </ul> <p>如果您正在创建演示文稿[！UICONTROL By Dropdown] ，则会显示此字段。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL演示文稿ID]</td> 
   <td> <p>选择要列出的演示文稿的文件夹位置。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL选择]</td> 
   <td> <p>选择是要使演示文稿中的所有链接都可点击，还是要将链接插入到所有匹配的输入文本中。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL文本输入]</td> 
   <td>如果要插入链接，则对于每个要为其添加链接的文本项，单击“添加项”<b></b>并输入文本及其关联的链接。 每次在演示文稿中显示项目时，它都会自动链接到指定的站点。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 进行API调用]

执行任意授权的API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection] </td> 
   <td> <p>有关将[!DNL Google Slides]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与[!DNL Adobe Workfront Fusion]的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL URL]</td> 
   <td> <p>输入相对于<code>https://developers.google.com/slides/</code>的路径。 例如，演示文稿。</p> <p>有关可用端点的列表，请参阅<a href="https://developers.google.com/slides/reference/rest">[!DNL Google Slides] API文档</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Headers]</td> 
   <td> <p>输入所需的请求标头。 您无需添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL查询字符串]</td> 
   <td> <p> 输入请求查询字符串。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**&#x200B;使用API调用，您可以获取您输入的演示文稿ID的演示详细信息。 在[!DNL Google Slides]中打开演示文稿时，可以在URL中找到演示文稿ID。

![API调用示例](/help/workfront-fusion/references/apps-and-modules/assets/api-call-350x13.png)

以下API调用返回演示文稿详细信息：

![演示详细信息](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details.png)

在[!UICONTROL 包] > [!UICONTROL 正文] > [!UICONTROL presentationId]下的模块输出中可以找到搜索匹配项。

在我们的示例中，返回了请求的演示文稿详细信息：

![演示详细信息](/help/workfront-fusion/references/apps-and-modules/assets/presentation-details-2.png)

>[!ENDSHADEBOX]
