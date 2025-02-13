---
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用Anaplan的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 81c9b141-4e40-430f-99f1-c44b7a833bcd
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '1616'
ht-degree: 0%

---

# [!DNL Anaplan]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Anaplan]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
  <td> <p>[!UICONTROL Pro] 或更高</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
   <td> <p>[!UICONTROL Plan]， [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 许可证**</td> 
   <td>
   <p>当前许可证要求：无[!DNL Workfront Fusion]许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[!UICONTROL Select]或[!UICONTROL Prime] [!DNL Adobe Workfront]计划，则您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]才能使用本文中描述的功能。 [!DNL Workfront Fusion]包含在[!UICONTROL Ultimate] [!DNL Workfront]计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买[!DNL Adobe Workfront Fusion]和[!DNL Adobe Workfront]，才能使用本文中介绍的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有什么计划、许可证类型或访问权限，请与[!DNL Workfront]管理员联系。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

## 先决条件

在使用[!DNL Anaplan]连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的[!UICONTROL Anaplan]帐户。
* 您必须先在[!UICONTROL Anaplan]帐户中配置工作区、模型和其他[!DNL Anaplan]对象，然后[!DNL Workfront Fusion]才能与这些对象交互。

## Anaplan API信息

Anaplan连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td>https://api.anaplan.com/2/0/
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API版本</td> 
   <td> v2 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.11.5/td&gt; 
 </tbody> 
</table>

## 将[!DNL Anaplan]连接到[!DNL Workfront Fusion] {#connect-anaplan-to-workfront-fusion}

要为您的[!DNL Anaplan]模块创建连接：

1. 单击[!UICONTROL Connection]框旁边的&#x200B;**[!UICONTROL Add]**。
1. 选择连接类型。

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL Basic]</td> 
      <td> <p>[!DNL Anaplan] [!UICONTROL Basic]连接只需要电子邮件地址和密码即可创建连接。 </p> <p>输入连接的名称，然后输入您的电子邮件地址和[!DNL Anaplan]帐户的密码。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL CA Certificate]</td> 
      <td> <p>[!DNL Anaplan] [!UICONTROL CA Certificate]连接需要[!UICONTROL Certificate Key]、[!UICONTROL Encoded Data]和[!UICONTROL Encoded Signed Data]。 您可以在[!DNL Anaplan]帐户中生成这些内容。 有关说明，请参阅[!DNL Anaplan]文档。</p> <p>输入连接的名称，然后输入您在[!DNL Anaplan]帐户中生成的[!UICONTROL Certificate Key]、[!UICONTROL Encoded Data]和[!UICONTROL Encoded Signed Data]。</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;保存连接并返回模块。

## [!DNL Anaplan]模块及其字段

配置[!DNL Anaplan]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Anaplan]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [触发器](#triggers)
* [操作](#actions)
* [搜索](#searches)

### 触发器

#### [!DNL Watch records]

此触发器模块在创建或更新所选类型的记录时启动方案。

>[!NOTE]
>
>此模块返回新记录的数据。 它不返回已修改现有记录的数据。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Anaplan]的连接的说明，请参阅本文中的<a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">将[!DNL Anaplan]连接到[!DNL Workfront Fusion]</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">要监视的对象类型</td> 
   <td>选择要监视的项目类型。 此方案从创建或更新此类型的记录时开始。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">&lt;对象&gt; ID</td> 
   <td>在Anaplan中输入与要监视的对象关联的对象ID，例如模型或模块</td> 
  </tr> 
  <tr> 
   <td role="rowheader">限制</td> 
   <td> <p>在每个方案执行周期中，输入或映射您希望模块记录的最大数目，即[action]。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Create a list item]](#create-a-list-item)
* [[!UICONTROL Make a custom API Call]](#make-a-custom-api-call)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Run an action]](#run-an-action)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Upload a file]](#upload-a-file)

#### [!UICONTROL Create a list item]

此操作模块向Anaplan中的列表添加新项。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Connection]</td>
        <td>有关创建与[!DNL Anaplan]的连接的说明，请参阅本文中的<a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">将[!DNL Anaplan]连接到[!DNL Workfront Fusion]</a>。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Workspace ID]</td>
        <td>选择或映射包含要添加项目的列表的Anaplan Workspace的ID。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Model ID]</td>
        <td>选择或映射包含要添加项目的列表的模型的ID。</td>
    </tr>
    <tr>
        <td>[!UICONTROL List ID]</td>
        <td>选择或映射要在其中创建项目的列表的ID。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Name]</td>
        <td>输入新项目的名称。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Code]</td>
        <td>输入新项目的代码。 代码是用户生成的代码，可用于区分具有相同名称的行项目。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Parent]</td>
        <td>输入要在其下创建新项目的父项目的名称。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Properties]</td>
        <td>如果要将项目添加到的列表具有自定义属性，请选择要为其添加值的属性，然后添加值。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Subsets]</td>
        <td>如果要将项添加到的列表具有自定义子集，请选择要将该项添加到的子集，然后选择<b>[!UICONTROL Yes]</b>以将该项添加到该子集。</td>
    </tr>
</table>

#### [!UICONTROL Make a custom API Call]

此模块允许您对[!DNL Anaplan] API执行自定义API调用。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Anaplan]的连接的说明，请参阅本文中的<a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">将[!DNL Anaplan]连接到[!DNL Workfront Fusion]</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>输入相对路径 <code>https://api.anaplan.com/2/0/</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>输入请求查询字符串。</p> </td> 
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

#### [!UICONTROL Delete a record]

此操作模块删除现有记录。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Anaplan]的连接的说明，请参阅本文中的<a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">将[!DNL Anaplan]连接到[!DNL Workfront Fusion]</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Workspace ID]</td> 
   <td>选择或映射包含要删除对象的Anaplan Workspace的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Model ID]</td> 
   <td>输入或映射包含要删除对象的模型的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">删除</td> 
   <td> <p>选择要删除的对象类型。</p> 
    <ul> 
     <li> <p><b>操作</b> </p> <p>选择或映射要删除的操作。</p> </li> 
     <li> <p><b>列表项</b> </p> <p>选择要从中删除项目的列表，然后输入或映射要删除项目的ID或代码</p>  </li> 
     <li> <p><b>[!UICONTROL File]</b> </p> <p>选择或映射要删除的文件。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

此操作模块读取单个记录。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Anaplan]的连接的说明，请参阅本文中的<a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">将[!DNL Anaplan]连接到[!DNL Workfront Fusion]</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>选择要读取的记录类型。</p> 
    <ul> 
     <li> <p><b>模型</b> </p> <p>选择或映射要读取的模型的ID</p> </li> 
     <li> <p><b>模型列表</b> </p> <p>选择或映射包含要读取的列表的Workspace和模型的ID，然后选择列表。 在[!UICONTROL Data type]字段中，选择要读取数据还是元数据。</p> </li> 
     <li> <p><b>模型版本</b> </p> <p>选择或映射要读取的模型的ID。</p> </li> 
     <li> <p><b>用户</b> </p> <p>选择您是要返回有关正在使用的帐户的所有者的数据，还是要返回其他用户的数据。 如果选择另一个用户，请选择该用户的名称。</p> </li> 
     <li> <p><b>Workspace</b> </p> <p>选择或映射您要读取的Workspace的ID。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Run an action]

此操作模块可导入、导出、删除或处理一项操作。

<table style="table-layout:auto"> 
     <col/>
     <col/>
     <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection]</td>
        <td>有关创建与[!DNL Anaplan]的连接的说明，请参阅本文中的<a href="#Connect" class="MCXref xref" >[!UICONTROL Connect Anaplan to Workfront Fusion]</a>。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Workspace ID]</td>
        <td>选择或映射要执行操作的[!DNL Anaplan] Workspace的ID</td>
      </tr>
      <tr >
        <td role="rowheader">[!UICONTROL Model ID]</td>
        <td>选择或映射要执行操作的模型的ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Action type]</td>
        <td>
          <p>选择要执行的操作</p>
            <ul>
              <li>
                <p><b>[!UICONTROL Delete]</b>
                </p>
                <p>输入或映射要删除的操作的ID。</p>
              </li>
              <li>
                <p><b>[!UICONTROL Export]</b>
                </p>
                <p>输入或映射要使用的导出定义的ID。 可导出为以下文件格式：</p>
                  <ul>
                    <li>
                      <p>XLS</p>
                    </li>
                    <li>
                      <p>XLSX</p>
                    </li>
                    <li>
                      <p>CSV</p>
                    </li>
                  </ul>
                </li>
                <li>
                  <p><b>[!UICONTROL Import] </b>
                  </p>
                  <p style="font-weight: normal;">输入或映射要使用的导入定义的ID。</p>
                </li>
                <li>
                 <p><b>[!UICONTROL Process]</b>
                 </p>
                  <p>输入或映射要使用的进程的ID。 </p>
                </li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>


#### [!UICONTROL Update a record]

此操作模块更新[!UICONTROL Anaplan]中的单个记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Anaplan]的连接的说明，请参阅本文中的<a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">将[!DNL Anaplan]连接到[!DNL Workfront Fusion]</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>选择要更新的记录类型。</p> 
    <ul> 
     <li> <p><b>[!UICONTROL List item]</b> </p> <p>有关字段，请参阅本文中的<a href="#create-a-list-item" class="MCXref xref">创建列表项</a>。</p> </li> 
     <li> <p><b>[!UICONTROL Module cell data]</b> </p> <p>更新单元格数据时，使用该数据的所有下游计算也会更新。</p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Model ID]</b> </p> <p>选择或映射包含要更新的单元格的模型。</p> </li> 
       <li> <p><b>[!UICONTROL Module ID]</b> </p> <p>选择或映射包含要更新的单元格的模块</p> </li> 
       <li> <p><b>[!UICONTROL Line item name]</b> </p> <p>选择或映射要更新的单元格的行项</p> </li> 
       <li> <p style="font-weight: bold;">[!UICONTROL Dimension ID]</p> <p>选择或映射行项目上的维度。</p> 
       <p><b>注释：</b> 
       <ul>
       <li> Dimension键（值）必须为<code>dimensionName</code> （下一个）或<code>dimensionId</code> (ID)。</li>
       <li>项目键（值）必须为<code>itemName</code> （文本）、<code>itemCode</code> （文本）或<code>itemId</code> (ID)。</li>
       <li>Dimension和项目键必须属于相同类型（文本或ID）。
       </ul>
        </p> 
        <p>有关维度的信息，请在[!DNL Anaplan Anapedia]中搜索Dimension。</p> </li> 
       <li> <p><b>[!UICONTROL Value]</b> </p> <p>输入或映射单元格的新值。</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Model current fiscal year]</b> </p> <p>输入要更新其会计年度的模型的Workspace ID和模型ID，然后为模型输入或映射新年度。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a file]

此操作模块将文件上传到Anaplan。 该文件必须已上载到Anaplan。 您可以使用此模块将其上传到Anaplan中的其他位置。
<table style="table-layout:auto">
<col>
<col>
<tbody>
<tr>
<td role="rowheader">[!UICONTROL Connection]</td>
<td>有关创建与[!DNL Anaplan]的连接的说明，请参阅本文中的<a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">将[!DNL Anaplan]连接到[!DNL Workfront Fusion]</a>。</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Workspace ID]</td>
<td>选择或映射要上传文件的[!DNL Anaplan] Workspace的ID。</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL Model ID]</td>
<td>选择或映射要上传文件的模型的ID。</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL File ID]</td>
<td>选择或映射要上传的文件的ID。</td>
</tr>
</tbody>
</table>
</div>

### 搜索

#### [!UICONTROL Get record]

此搜索模块返回所选类型的所有可访问记录。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Anaplan]的连接的说明，请参阅本文中的<a href="#connect-anaplan-to-workfront-fusion" class="MCXref xref">将[!DNL Anaplan]连接到[!DNL Workfront Fusion]</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record types]</td> 
   <td> <p>选择要检索的记录类型。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Workspaces]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Models]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Line items]</b> </p> <p>选择或映射包含要检索的[!DNL line]项的模型的ID。</p> </li> 
       <li> <p><b>[!UICONTROL Model lists]</b> </p> <p>选择或映射包含要检索的模型列表的Workspace ID和模型ID。</p> </li> 
       <li> <p><b>[!UICONTROL Model calendar]</b> </p> <p>选择或映射包含要检索的模型日历的Workspace的ID。</p> </li> 
       <li> <p><b>[!UICONTROL Model versions]</b> </p> </li> 
       <li> <p>选择或映射包含要检索的模型版本的模型ID。</p> </li> 
       <li> <p><b>[!UICONTROL Users]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Views]</b> </p> <p>选择是要按模块还是按模型选择视图，然后选择或映射包含要检索的视图的模块或模型的ID。</p> </li> 
      </ul> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Return workspace size]</td> 
   <td>启用此选项可返回工作区的当前大小的估计值。 此估算基于工作区中包含的所有模块的大小。</td> 
  </tr> 
 </tbody> 
</table>
