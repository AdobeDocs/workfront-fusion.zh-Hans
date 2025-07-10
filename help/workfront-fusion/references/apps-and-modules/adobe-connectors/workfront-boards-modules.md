---
title: Adobe Workfront展示板模块
description: 您可以使用Adobe Workfront展示板连接器自动执行Workfront展示板中的流程，并将其连接到第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: dcc5044d-8fdf-4a74-b664-e965e714ce92
source-git-commit: 899fc717f5107433d6f1aea31c4d079243a85822
workflow-type: tm+mt
source-wordcount: '2868'
ht-degree: 0%

---

# [!DNL Adobe Workfront]讨论区模块

>[!NOTE]
>
>板融合连接器处于Beta状态。 因此，对该连接器的支持有限，并且可能会由于主板未来的发展而发生更改。 此外，GraphQL API可能会有更改，恕不另行通知，这可能会影响您的Fusion连接器过程。

Adobe Workfront展示板是一种灵活的工具，通过提供对包含列和卡片的共享展示板的访问，允许团队协作。

您可以使用Adobe Workfront展示板模块读取或更新记录，对Workfront展示板API进行API调用，或当展示板上发生操作时触发场景。

<!--For general information on Workfront Boards, see [Boards overview](/help/quicksilver/agile/boards-overview.md).-->

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

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

您必须先在Adobe Workfront中配置讨论区，然后才能连接到该讨论区。

## Adobe Workfront展示板API信息

Adobe Workfront主板连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.23.6</td> 
  </tr>
 </tbody> 
 </table>

## 创建与Workfront展示板的连接

>[!NOTE]
>
>您可以使用Workfront连接连接到Workfront展示板，也可以创建单独的Workfront展示板连接。

要创建Workfront展示板连接，请执行以下操作：

1. 在任意[!DNL Adobe Workfront Boards]模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

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
          <td>选择您是要连接到服务帐户还是个人帐户。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端ID]<p>（可选）</p></td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端ID]。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。</td>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 客户端密钥]<p>（可选）</p></td>
          <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 身份验证URL]<p>（可选）</p></td>
          <td>输入您的Workfront实例将用于对此连接进行身份验证的URL。 <p>默认值为<code>https://oauth.my.workfront.com/integrations/oauth2</code>。</p>
        </tr>
        <tr>
          <td role="rowheader">[!UICONTROL 主机前缀]</td>
          <td>输入您的主机前缀。<p>默认值为<code>origin-</code>。</p>
        </tr>
      </tbody>
    </table>
1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## Adobe Workfront展示板模块及其字段

配置Workfront展示板模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除了这些以外，还可能会显示其他Workfront展示板字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [信息卡](#cards)
* [展示板](#boards)
* [列](#columns)
* [标记](#tags)
* [评论](#comments)
* [其他](#other)

### 信息卡

* [添加清单项目](#add-checklist-item)
* [添加子任务](#add-subtask)
* [创建信息卡](#create-a-card)
* [移动信息卡](#move-a-card)
* [读取信息卡](#read-a-card)
* [更新信息卡](#update-a-card)

#### 添加清单项目

此操作模块将一个清单项目添加到指定的信息卡。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 卡ID]</td> 
   <td>输入或映射您要将清单项目添加到的卡的ID。<p>在Workfront中查看信息卡时，您可以在URL中找到该信息卡ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 清单项目]</td> 
   <td>对于要添加的每个清单项目，单击“添加项目”，输入清单项目的名称，然后选择该项目是否已完成。</p></td> 
  </tr> 
 </tbody> 
</table>

#### 添加子任务

此操作模块将一个子任务添加到展示板中的信息卡。 该卡必须是已连接的卡。 该子任务也会添加到卡所代表的Workfront任务中。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 父卡片ID]</td> 
   <td>输入或映射要添加子任务的卡的ID。<p>在Workfront中查看信息卡时，您可以在URL中找到该信息卡ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射包含要向其添加子任务的卡片的展示板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 名称]</td> 
   <td>输入或映射新子任务的名称。</p></td> 
  </tr> 
 </tbody> 
</table>

#### 创建信息卡

此操作模块可在Workfront展示板上创建新信息卡。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射要将信息卡添加到的展示板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 列ID]</td> 
   <td>输入或映射要添加子任务的列的ID。<p>您可以从读取展示板模块返回的信息中找到列ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 名称]</td> 
   <td>输入或映射新卡的名称。</p></td> 
  </tr> 
 </tbody> 
</table>

#### 移动信息卡

该操作模块会将一张信息卡移动到同一展示板上的另一列。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 卡ID]</td> 
   <td>输入或映射要移动的卡的ID。<p>在Workfront中查看信息卡时，您可以在URL中找到该信息卡ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射包含要移动的信息卡的主板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 目标列ID]</td> 
   <td>输入或映射要将卡片移动到的列的ID。<p>您可以从读取展示板模块返回的信息中找到列ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 到索引]</td> 
   <td>输入或映射您希望信息卡在新列中的位置。<p>索引0中列的顶部位置。</p></td> 
  </tr> 
 </tbody> 
</table>

#### 读取信息卡

此操作模块可检索有关特定信息卡的信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 卡ID]</td> 
   <td>输入或映射要读取的信息卡的ID。<p>在Workfront中查看信息卡时，您可以在URL中找到该信息卡ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 卡ID]</td> 
   <td>输入或映射包含要读取的卡的主板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
 </tbody> 
</table>

#### 更新信息卡

此操作模块会更新您指定信息卡的信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 卡ID]</td> 
   <td>输入或映射要更新的信息卡的ID。<p>在Workfront中查看信息卡时，您可以在URL中找到该信息卡ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射包含要更新的卡的主板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 名称]</td> 
   <td>输入或映射卡的新名称。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 描述]</td> 
   <td>输入或映射卡的新描述。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 估计]</td> 
   <td>输入或映射完成此信息卡所需时间的估计值。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 到期日期]</td> 
   <td>输入或映射此卡的到期日期。</p>
   <p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p>
   </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 状态]</td> 
   <td>为信息卡选择新状态。</p></td> 
  </tr> 
 </tbody> 
</table>

### 展示板

* [创建展示板](#create-a-board)
* [阅读讨论区](#read-a-board)

#### 创建展示板

此操作模块可在Workfront中创建展示板。 您可以指定要创建的展示板类型。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板名称]</td> 
   <td>输入或映射新讨论区的名称。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 模板]</td> 
   <td>为要创建的展示板类型选择模板。</td> 
  </tr> 
 </tbody> 
</table>

#### 阅读讨论区

此操作模块返回有关单个展示板的信息，例如展示板的卡片、列、标记和成员。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射要检索其信息的展示板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
 </tbody> 
</table>

### 列

* [创建列](#create-a-column)
* [搜索列](#search-for-a-column)
* [更新列](#update-a-column)

#### 创建列

此操作模块在指定的展示板上创建新列。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射要添加列的展示板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 列ID]</td> 
   <td>输入或映射要更新的列的ID。<p>您可以从读取展示板模块返回的信息中找到列ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 列名称]</td> 
   <td>输入或映射列的新名称。</td> 
  </tr> 
 </tbody> 
</table>

#### 搜索列

此搜索模块返回有关具有指定名称的列的信息。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射包含要检索的列的展示板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 列名称]</td> 
   <td>输入或映射要检索的列的名称。</td> 
  </tr> 
 </tbody> 
</table>

#### 更新列

此操作模块可更新指定列的名称或WIP限制。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射包含要检索的列的展示板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 列名称]</td> 
   <td>输入或映射要检索的列的名称。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL WIP限制]</td> 
   <td>输入或映射列的新WIP限制。</td> 
  </tr> 
 </tbody> 
</table>

### 标记

* [向信息卡添加标记](#add-a-tag-to-a-card)
* [创建标记](#create-a-tag)

#### 向信息卡添加标记

此操作模块会将标记添加到信息卡。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 卡ID]</td> 
   <td>输入或映射要添加标记的卡的ID。<p>在Workfront中查看信息卡时，您可以在URL中找到该信息卡ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射包含要将标记添加到的卡的展示板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 标记ID]</td> 
   <td>输入或映射要添加标记的ID。<p>您可以从读取展示板模块返回的信息中找到标记ID。</p></td> 
  </tr> 
 </tbody> 
</table>

#### 创建标记

此操作模块将创建一个新标记并为其分配一种颜色。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 展示板ID]</td> 
   <td>输入或映射要为其创建标记的展示板的ID。<p>在Workfront中查看展示板时，您可以在URL中找到展示板ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 标记名称]</td> 
   <td>输入或映射新标记的名称。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 标记颜色]</td> 
   <td>选择此标记的颜色。</td> 
  </tr> 
 </tbody> 
</table>

### 评论

* [创建评论](#create-a-comment)
* [阅读信息卡评论](#read-card-comments)

#### 创建评论

此操作模块在指定的信息卡上创建评论。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 卡ID]</td> 
   <td>输入或映射要添加注释的卡的ID。<p>在Workfront中查看信息卡时，您可以在URL中找到该信息卡ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>输入或映射要添加注释的文本。</p></td> 
  </tr> 
 </tbody> 
</table>

#### 阅读信息卡评论

此操作模块从指定的信息卡中检索注释。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 卡ID]</td> 
   <td>输入或映射要为其检索注释的卡片ID。<p>在Workfront中查看信息卡时，您可以在URL中找到该信息卡ID。</p></td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL 限制]</td> 
   <td>输入您希望模块在一个执行周期内返回的最大注释数。</p></td> 
  </tr> 
 </tbody> 
</table>

### 其他

#### 进行自定义API调用

此操作模块对Workfront展示板API进行自定义调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td> <p>输入相对于<code> https://&lt;WORKFRONT_DOMAIN&gt;/boards-service/graphql?</code>的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p><p>对于大多数展示板调用，该方法为POST。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。 这会确定请求的内容类型。</p> <p>例如，<code> { "Content-type":"application/json-stringify()"}</code></p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>对于Workfront展示板，此部分通常留空。</p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以JSON嵌入Graphql的形式添加API调用的正文内容 </p> <p>示例：</p><p>此示例更新列名。 您可以将<code>boardId</code>和<code>columnId</code>作为硬编码的GUID或从以前的模块映射的GUID包含在内。<p><pre>{<br> "query"： "mutation { updateColumn(boardId： \"\"， columnId： \"\"， updateColumnInput： { name： \"\" }) { id name }}"<br>}</pre><p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>


#### 进行自定义GraphQL API调用

此操作模块向Workfront展示板API发出自定义GraphQL请求。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
      <td> <p>您可以使用现有的Workfront连接连接到Workfront展示板，也可以使用特定的Workfront展示板连接。 </p><p>有关将[!DNL Workfront]应用连接到[!DNL Workfront Fusion]的说明，请参阅本文中的<a href="#create-a-connection-to-workfront-boards" class="MCXref xref">创建与Workfront讨论区的连接</a>。</p> </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择此调用的方法。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 操作名称]</td> 
   <td> <p>输入此操作的名称。 这样可以更轻松地跟踪和调试调用。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variables数据源]</td> 
   <td> <p>选择变量是来自表单还是集合。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variables]</td> 
   <td> <p>对于要添加的每个变量，单击<b>添加项</b>并输入变量的键和值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 限制]</td> 
   <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td> 
   </tr> 
 </tbody> 
</table>
