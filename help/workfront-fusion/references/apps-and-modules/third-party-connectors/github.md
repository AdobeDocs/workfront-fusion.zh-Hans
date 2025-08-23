---
title: GitHub模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用GitHub的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: d9e6c26c-8770-40bc-a83a-8c05f86e4a3f
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 0%

---

# [!DNL GitHub]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!UICONTROL GitHub]的工作流，并将其连接到多个第三方应用程序和服务。

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

要使用[!DNL GitHub]模块，您必须拥有[!DNL GitHub]帐户。

## 将[!DNL GitHub]连接到Workfront Fusion

有关将[!DNL GitHub]帐户连接到[!UICONTROL Workfront Fusion]的说明，请参阅[创建与[!UICONTROL Adobe Workfront Fusion]的连接 — 基本说明](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md)

## [!DNL GitHub]模块及其字段。

在配置[!DNL GitHub]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL GitHub]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)

### 触发器

* [[!UICONTROL 观看评论]](#watch-comments)
* [[!UICONTROL 监视分支]](#watch-forks)
* [[!UICONTROL 关注问题]](#watch-issues)
* [[!UICONTROL 观看拉取请求]](#watch-pull-requests)
* [[!UICONTROL 监视存储库]](#watch-repositories)

#### [!UICONTROL 观看评论]

此触发器模块会在添加新评论或修改现有评论时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择要监视的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 问题编号]</td> 
   <td>如果要通过仅搜索针对特定问题提出的新注释来限制搜索，请输入问题编号。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大问题数]</td> 
   <td> <p> 设置Workfront Fusion在一个周期内返回的最大评论数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 监视]</td> 
   <td>选择是要只查看新注释，还是要查看注释及所有更改。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 监视分支]

此触发器模块会在创建新分支后启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择要监视分支的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的分叉最大数量]</td> 
    <td>输入或映射您希望模块在每个方案执行周期中返回的最大分支数。</td>
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 关注问题]

此触发器模块会在添加新问题或修改现有问题时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 我要观看]</td> 
   <td>选择是要监视与此帐户关联的所有存储库，还是只监视一个存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>如果您已选择仅在一个存储库中监视问题，请选择要监视的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大问题数]</td> 
   <td> <p> 设置Workfront Fusion在一个周期内返回的最大问题数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 监视]</td> 
   <td>选择您是希望仅关注新问题，还是希望关注新问题和所有更改。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 筛选器]</td> 
   <td> <p>您可以过滤要关注的问题，方法是通过您与它们的关联方式。</p> 
    <ul> 
     <li>[!UICONTROL 所有问题]</li> 
     <li>[!UICONTROL 仅分配给我的问题]</li> 
     <li>[!UICONTROL Only Issues created by me]</li> 
     <li>[!UICONTROL 仅问题提及我]</li> 
     <li>[!UICONTROL 仅我订阅的更新问题]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 状态]</td> 
   <td>选择是只查看未完成的问题，还是只查看已关闭的问题。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标签]</td> 
   <td>对于要添加的每个标记，单击<b>添加项</b>并输入标记。 模块会监视这些标记是否存在问题。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 观看拉取请求]

添加新的拉取请求或修改现有拉取请求时，将触发此模块。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择要监视的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大拉取请求数]</td> 
   <td> <p> 设置Workfront Fusion在一个周期内返回的最大拉取请求数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 状态]</td> 
   <td>选择是要监视[!UICONTROL 仅打开拉取]请求，还是要监视[!UICONTROL 仅关闭拉取]请求，还是要监视所有拉取请求。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 监视]</td> 
   <td>选择您是只关注新的拉取请求，还是只关注新的拉取请求和所有更改。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 监视存储库]

此触发器模块会在创建或修改存储库时启动方案。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回存储库的最大数量]</td> 
   <td> <p> 设置Workfront Fusion在一个周期内返回的最大存储库数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 监视]</td> 
   <td>选择是要监视新存储库和所有更改，还是只监视新存储库。</td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 添加被分派人]](#add-assignees)
* [[!UICONTROL 向问题添加标签]](#add-labels-to-an-issue)
* [[!UICONTROL 创建评论]](#create-a-comment)
* [[!UICONTROL 创建问题]](#create-an-issue)
* [[!UICONTROL 获取问题]](#get-an-issue)
* [[!UICONTROL 列出评论]](#list-comments)
* [[!UICONTROL 从问题中删除标签]](#remove-a-label-from-an-issue)
* [[!UICONTROL 移除被分派人]](#remove-assignees)
* [[!UICONTROL 搜索问题]](#search-for-an-issue)
* [[!UICONTROL 更新问题]](#update-an-issue)

#### [!UICONTROL 添加被分派人]

此模块将受分派人添加到指定问题

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择包含要添加被分配人的问题的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 被分派人]</td> 
   <td>选择要分配给问题的人员。 可用的被分配者包括拥有存储库写入权限的任何人和拥有存储库读取权限的组织成员。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 编号]</td> 
   <td>输入或映射要添加被分配人的问题的问题编号。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 向问题添加标签]

此模块向问题添加标签。 标签在存储库级别定义，并且只能由对存储库具有写入权限的用户创建。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择包含您要向其添加标签的问题存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标签]</td> 
   <td>选择要添加到问题的标签。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 编号]</td> 
   <td>输入或映射要添加标签的问题编号。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建评论]

此模块创建指定问题的评论。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择包含您要为其创建评论的问题的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 编号]</td> 
   <td>输入或映射您要创建评论的问题编号。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>输入或映射注释的内容。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 创建问题]

此模块在选定存储库中创建新问题。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择要在其中创建问题的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 被分派人]</td> 
   <td>选择要分配给问题的人员。 可用的被分配者包括拥有存储库写入权限的任何人，以及拥有存储库读取权限的组织成员。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 里程碑]</td> 
   <td>选择要与新问题关联的里程碑。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标签]</td> 
   <td>选择要应用于新问题的任何标签。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标题]</td> 
   <td>输入或映射新问题的标题。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>输入或映射问题的正文，如描述或其他信息</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 获取问题]

此模块检索有关指定问题的详细信息

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择包含您要检索其详细信息的问题的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 编号]</td> 
   <td>输入或映射要检索其详细信息的问题的问题编号。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 列出评论]

此模块列出了有关指定问题的所有注释。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择包含您要从中列出注释的问题的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 编号]</td> 
   <td>输入或映射要从中列出注释的问题编号。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 始自]</td> 
   <td>模块将返回在此日期之后创建的注释。 有关支持的日期格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大评论数]</td> 
   <td> <p> 设置Workfront Fusion在一个周期内返回的最大评论数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 从问题中删除标签]

此模块从问题中删除单个标签。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择包含要从其中移除标签的问题存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标签]</td> 
   <td>选择要从问题中删除的标签。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 编号]</td> 
   <td>输入或映射要从其中移除标签的问题编号。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 移除被分派人]

此模块从指定问题中删除被分配人。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择包含要从其中移除被分配人的问题的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 被分派人]</td> 
   <td>选择要从问题中删除的人员。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 编号]</td> 
   <td>输入或映射要从其中移除被分配人的问题的问题编号。 </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 搜索问题]

此模块将搜索与您的搜索条件匹配的问题。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回的最大问题数]</td> 
   <td> <p> 设置Workfront Fusion在一个周期内返回的最大问题数。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 排序方式]</td> 
   <td> <p>选择您希望对搜索结果进行排序的方式。</p> 
    <ul> 
     <li> <p>[!UICONTROL 最佳匹配] </p> </li> 
     <li>[!UICONTROL 创建日期]</li> 
     <li>[!UICONTROL 更新日期]</li> 
     <li>[!UICONTROL 评论数]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 排序方向]</td> 
   <td> <p>选择升序或降序。 </p> <p>对于日期，选择<strong>[!UICONTROL descending]</strong>将首先返回最近的日期。 </p> <p>对于[!UICONTROL 评论数]，选择<strong>[!UICONTROL 降序]</strong>将首先返回评论数最多的问题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query]</td> 
   <td>输入或映射您的搜索查询。 有关搜索选项的详细说明，请参阅<a href="https://docs.github.com/en/github/searching-for-information-on-github/searching-issues-and-pull-requests">帮助网站上的</a>搜索问题和拉取请求[!DNL GitHub]。</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新问题]

此模块更新现有的[!DNL GitHub]问题。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL GitHub]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe Workfront Fusion的连接 — 基本说明</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 存储库]</td> 
   <td>选择要更新问题的存储库。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 被分派人]</td> 
   <td>选择要分配给问题的人员。 可用的被分配者包括拥有存储库写入权限的任何人和拥有存储库读取权限的组织成员。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 里程碑]</td> 
   <td>选择要与问题关联的里程碑。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标签]</td> 
   <td>选择要应用于问题的任何标签。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 编号]</td> 
   <td>输入或映射要更新的问题的问题编号。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 状态]</td> 
   <td>选择要将问题更新到的状态。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 标题]</td> 
   <td>输入或映射问题的新标题。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td>输入或映射问题的新正文，如说明或附加信息</td> 
  </tr> 
 </tbody> 
</table>
