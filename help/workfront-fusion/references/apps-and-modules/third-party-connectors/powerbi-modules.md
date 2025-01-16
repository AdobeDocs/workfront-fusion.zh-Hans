---
title: Power BI模块
description: 除了Adobe Workfront许可证之外，Adobe Workfront Fusion还需要Adobe Workfront Fusion许可证。
author: Becky
feature: Workfront Fusion
exl-id: 73eb70e1-3f3d-419d-9cde-3ec3cda224f8
source-git-commit: 9e560995ff9f58a76bbecc521f7d2eef9d47fa48
workflow-type: tm+mt
source-wordcount: '2089'
ht-degree: 0%

---

# [!DNL Power BI]模块

[!DNL Power BI]是一个应用程序，它允许您可视化数据并向利益相关者展示数据。 它可以获取来自各种来源的数据。

>[!NOTE]
>
>[!DNL Workfront Fusion]不是数据源。 虽然[!DNL Workfront Fusion]可以创建和使用数据源，但它不会存储您的数据。


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

## MicrosoftPower BIAPI信息

MicrosoftPower BI连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td> https://api.powerbi.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.0.2</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Power BI]模块及其字段

配置[!DNL Power BI]时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，还可能会显示其他字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[在Adobe Workfront Fusion中将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [仪表板](#dashboards)
* [报告](#reports)
* [数据集](#dataset)
* [应用程序](#apps)
* [其他](#other)

### 仪表板

* [创建功能板](#create-a-dashboard)
* [获取功能板](#get-a-dashboard)
* [获取功能板拼贴](#get-a-dashboard-tile)
* [列出功能板磁贴](#list-dashboard-tiles)
* [列出仪表板](#list-dashboards)

#### [!UICONTROL Create a Dashboard]

此操作模块将创建一个新仪表板。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>输入或映射功能板的名称。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射将拥有新功能板的组的ID。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dashboard]

此操作模块检索指定功能板的元数据。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
      <td>
        <p>选择或映射选项以选择要为其检索元数据的仪表板。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dashboard ID]</td>
      <td>
        <p>输入或映射要为其检索元数据的仪表板的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射拥有您要为其检索元数据的功能板的组的ID。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dashboard Tile]

此操作模块可检索指定功能板拼贴的元数据。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
      <td>
        <p>选择或映射选项以选择要检索的仪表板详细信息。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dashboard ID]</td>
      <td>
        <p>输入或映射要检索其详细信息的仪表板的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tile ID]</td>
      <td>输入或映射要检索其详细信息的[!DNL Power BI]拼贴的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射拥有您要检索的拼贴的组的ID。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Dashboard Tiles]

此搜索模块可检索功能板磁贴的列表。

<table>
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
    <td>
      <p>选择或映射选项以选择要列出其图块的仪表板。</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Dashboard ID]</td>
    <td>
      <p>输入或映射包含要列出的图块的仪表板的ID。</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Group ID]  </td>
    <td>选择或映射拥有包含要列出的图块的仪表板的组的ID。</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]  </td>
    <td>
      <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p>
    </td>
  </tr>
</tbody>
</table>

#### [!UICONTROL List Dashboards]

此搜索模块可检索功能板列表。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>
        <p>选择或映射拥有要列出的功能板的组的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p>
      </td>
    </tr>
  </tbody>
</table>

### 报告

* [复制报告](#copy-a-report)
* [删除报告](#delete-a-report)
* [获取报表](#get-a-report)
* [列表报告](#list-reports)

#### [!UICONTROL Copy a Report]

此操作模块复制现有报表。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>选择或映射选项以选择要复制的报表。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>输入或映射要复制的报表的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射拥有要复制的报表的组的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL New Copied Report Name]</td>
      <td>输入或映射新报表的名称。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a Report]

此操作模块删除报表。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>选择或映射选项以选择要删除的报表。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>输入或映射要删除的报表的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射拥有要删除的报表的组的ID。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Report]

此操作模块检索指定报表的元数据。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>选择或映射选项以选择要为其检索元数据的报表。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>输入或映射要为其检索元数据的报表的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射拥有您要为其检索元数据的报表的组的ID。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Reports]

此搜索模块可检索报告列表。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>
        <p>选择或映射拥有要列出的报告的组的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p>
      </td>
    </tr>
  </tbody>
</table>


### 数据集

* [在数据集表中添加/删除行](#add-or-delete-rows-in-a-dataset-table)
* [创建数据集](#create-a-dataset)
* [删除数据集](#delete-a-dataset)
* [获取数据集](#get-a-dataset)
* [列出数据集](#list-datasets)
* [刷新数据集](#refresh-a-dataset)

#### [!UICONTROL Add or Delete Rows in a Dataset Table]

此操作模块添加或删除指定推送数据集表的行。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a table]</td>
      <td>选择或映射选项以选择包含要调整的表的数据集。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dataset ID]</td>
      <td>输入或映射包含要添加或删除的行的数据集的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Table Name]  </td>
      <td>
        <p>输入或映射包含要添加或删除的行的表的名称。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>输入或映射拥有数据集的组的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Select the Action]</td>
      <td>
        <p>选择或映射要执行的操作。</p>
        <ul>
          <li>
            <p>[!UICONTROL Add rows]</p>
          </li>
          <li>
            <p>[!UICONTROL Delete All Rows]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rows]</td>
      <td>
        <p>添加行字段。</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Key]</b>
            </p>
            <p>输入或映射密钥名称。</p>
          </li>
          <li>
            <p><b>[!UICONTROL Field Type]</b>
            </p>
            <p>选择或映射字段类型：</p>
            <ul>
              <li>
                <p>布尔型</p>
              </li>
              <li>
                <p>日期</p>
              </li>
              <li>
                <p>文本</p>
              </li>
              <li>
                <p>数字</p>
              </li>
            </ul>
          </li>
          <li>
            <p>[!UICONTROL Value]</p>
            <p>输入或映射键值。</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Create a Dataset]

此操作模块将创建新数据集。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>输入或映射数据集的名称。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射将拥有新数据集的组的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default Mode]</td>
      <td>
        <p>选择或映射数据集的默认模式：</p>
        <ul>
          <li>
            <p><b>[!UICONTROL As Azure]</b>：实时连接到的数据集 [!DNL Azure Analysis Service]</p>
          </li>
          <li>
            <p><b>[!UICONTROL As on Prem]</b>：与[!DNL On-premise Analysis]服务有实时连接的数据集</p>
          </li>
          <li>
            <p><b>[!DNL Push]</b>：允许以编程方式访问将数据推入的数据集 [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Push Streaming]</b>：支持数据流式传输并允许以编程方式访问将数据推入的数据集 [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Streaming]</b>：支持数据流的数据集</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tables]</td>
      <td>向数据集添加表。 有关字段，请参阅<a href="#Table" class="MCXref_0">表字段</a></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Data sources]</td>
      <td>添加数据源。 有关字段，请参阅<a href="#Data" class="MCXref_0">数据源字段</a>。</td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Default Retention Policy]  </td>
      <td>
        <p>选择或映射数据集的有意策略：</p>
        <ul>
          <li>
            <p>[!UICONTROL None]</p>
          </li>
          <li>
            <p>[!UICONTROL Basic FIFO]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### 表格字段

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>
        <p>  输入或映射表的名称。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Columns]</td>
      <td>
        <p>添加列：</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>输入（映射）列名。</p>
          </li>
          <li>
            <p><b>[!UICONTROL Data Type]</b>
            </p>
            <p>选择或映射数据类型：</p>
            <ul>
              <li>
                <p>[!UICONTROL String]</p>
              </li>
              <li>
                <p>[!UICONTROL Integer]</p>
              </li>
              <li>
                <p>[!UICONTROL Boolean]</p>
              </li>
              <li>
                <p>[!UICONTROL Date Time]</p>
              </li>
            </ul>
          </li>
          <li>
            <p><b>[!UICONTROL Format String]</b>
            </p>
            <p>输入（映射）格式字符串。</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rows]</td>
      <td>输入或映射行详细信息。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Measures]</td>
      <td>为表添加度量。</td>
    </tr>
  </tbody>
</table>

##### 数据源字段

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Database]  </td>
      <td>
        <p>输入或映射要使用的数据库。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Server]  </td>
      <td>
        <p>输入或映射要使用的服务器的名称。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]  </td>
      <td>
        <p>输入或映射要使用的URL。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data source ID]</td>
      <td>
        <p>  输入或映射数据源的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data source Type]  </td>
      <td>
        <p>选择或映射数据源类型。 示例： SQL。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gateway ID]  </td>
      <td>输入或映射要使用的网关ID。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a Dataset]

此操作模块删除数据集。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>选择或映射选项以选择要删除的数据集。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>输入或映射要删除的数据集的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射拥有要删除的数据集的组的ID。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dataset]

此操作模块检索指定数据集的元数据。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>选择或映射选项以选择要为其检索元数据的报表。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>输入或映射要为其检索元数据的数据集的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射拥有要为其检索元数据的数据集的组的ID。</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Datasets]

此搜索模块可检索数据集列表。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>选择或映射拥有您要为其检索元数据的报表的组的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>
        <p>在每个方案执行周期中，输入或映射您希望模块记录的最大数目，即[action]。</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Refresh a Dataset]

此操作模块刷新指定的数据集。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a dataset]</td>
      <td>选择或映射选项以选择要刷新的数据集。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dataset ID]</td>
      <td>输入或映射要刷新的数据集的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Table Name]  </td>
      <td>
        <p>输入或映射包含要添加或删除的行的表的名称。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>输入或映射拥有数据集的组的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Notify Option]  </td>
      <td>
        <p>选择或映射要通知的选项：</p>
        <ul>
          <li>
            <p>[!UICONTROL Mail on Completion]</p>
          </li>
          <li>
            <p>[!UICONTROL Mail on Failure]</p>
          </li>
          <li>
            <p>[!UICONTROL No Notification]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### 应用程序

* [获取应用程序](#get-an-app)
* [获取应用程序仪表板](#get-an-apps-dashboard)
* [获取应用程序的报表](#get-an-apps-report)
* [列出应用程序的控制面板](#list-apps-dashboards)
* [列出应用程序的报表](#list-apps-reports)
* [列出应用程序](#list-apps)
* [Watch应用程序](#watch-apps)

#### [!UICONTROL Get an App]

此操作模块可检索指定应用程序的元数据。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>选择或映射您要检索的应用程序的ID。</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an App's Dashboard]

此操作模块可检索指定应用程序功能板的元数据。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>选择或映射包含要检索的功能板的应用程序的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>  选择或映射要检索的仪表板ID。</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an App's Report]

此操作模块检索指定应用程序报表的元数据。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>选择或映射包含要检索的报表的应用程序ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>  选择或映射要检索的报表的ID。</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Apps]

此搜索模块可检索已安装的所有应用程序的列表。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List App's Dashboards]

此搜索模块从指定的应用程序中检索功能板列表。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]</td>
      <td>选择或映射您要从中列出功能板的应用程序的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List App's Reports]

此搜索模块从指定的应用程序中检索所有报表的列表。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]</td>
      <td>选择或映射要从中列出报表的应用程序的ID。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch Apps]

此触发器模块会在应用程序更新时启动方案。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p>
      </td>
    </tr>
  </tbody>
</table>

### 其他

#### [!UICONTROL Make an API Call]

此操作模块对[!DNL Power BI] API执行API调用。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>有关将[!DNL Power BI]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override="">创建与Adobe[!DNL Workfront Fusion]的连接 — 基本说明</a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>输入相对于<code>https://api.powerbi.com</code>的路径。 示例： <code>/v1.0/myorg/datasets</code>。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
      <td>
        <p>选择配置API调用所需的[!UICONTROL HTTP]请求方法。 有关详细信息，请参阅[!UICONTROL HTTP]请求方法。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 自动添加授权标头和x-api-key标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>输入请求查询字符串。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
