---
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用Anaplan的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Workfront Integrations and Apps
exl-id: 81c9b141-4e40-430f-99f1-c44b7a833bcd
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1983'
ht-degree: 1%

---

# [!DNL Anaplan]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Anaplan]的工作流，并将其连接到多个第三方应用程序和服务。

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
   <td>v1.11.5</td> 
 </tbody> 
</table>

## 将[!DNL Anaplan]连接到[!DNL Workfront Fusion] {#connect-anaplan-to-workfront-fusion}

要为您的[!DNL Anaplan]模块创建连接：

1. 单击[!UICONTROL 连接]框旁边的&#x200B;**[!UICONTROL 添加]**。
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
          <p>输入新连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 环境]</td>
        <td>
          <p>选择是连接到生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>
          <p>选择您是要连接到服务帐户还是个人帐户。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 电子邮件]</td>
        <td>
          <p>输入此Anaplan帐户的电子邮件地址</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 密码]</td>
        <td>输入此Anaplan帐户的密码。</td>
      </tr>
     </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

<!--1. Click **[!UICONTROL Add]** next to the [!UICONTROL Connection] box.
1. Select the connection type.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL Basic]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL Basic] connection requires only an email address and password to create the connection. </p> <p>Enter a name for the connection, then enter your email address and the password of your [!DNL Anaplan] account.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!DNL Anaplan] [!UICONTROL CA Certificate]</td> 
      <td> <p>An [!DNL Anaplan] [!UICONTROL CA Certificate] connection requires a [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data]. You can generate these in your [!DNL Anaplan] account. For instructions, see the [!DNL Anaplan] documentation.</p> <p>Enter a name for the connection, then enter the [!UICONTROL Certificate Key], [!UICONTROL Encoded Data], and [!UICONTROL Encoded Signed Data] that you generated in your [!DNL Anaplan] account.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Click **[!UICONTROL Continue]** to save the connection and return to the module.-->

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
   <td> <p>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 创建列表项]](#create-a-list-item)
* [删除记录](#delete-a-record)
* [导出数据](#export-data)
* [导入数据](#import-data)
* [[!UICONTROL 进行自定义API调用]](#make-a-custom-api-call)
* [[!UICONTROL 读取记录]](#read-a-record)
* [[!UICONTROL 运行操作]](#run-an-action)
* [[!UICONTROL 更新记录]](#update-a-record)
* [[!UICONTROL 上载文件]](#upload-a-file)

#### [!UICONTROL 创建列表项]

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
        <td>[!UICONTROL 模型ID]</td>
        <td>选择或映射包含要添加项目的列表的模型的ID。</td>
    </tr>
    <tr>
        <td>[!UICONTROL 列表ID]</td>
        <td>选择或映射要在其中创建项目的列表的ID。</td>
    </tr>
    <tr>
        <td>[!UICONTROL 名称]</td>
        <td>输入新项目的名称。</td>
    </tr>
    <tr>
        <td>[!UICONTROL 代码]</td>
        <td>输入新项目的代码。 代码是用户生成的代码，可用于区分具有相同名称的行项目。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Parent]</td>
        <td>输入要在其下创建新项目的父项目的名称。</td>
    </tr>
    <tr>
        <td>[!UICONTROL 属性]</td>
        <td>如果要将项目添加到的列表具有自定义属性，请选择要为其添加值的属性，然后添加值。</td>
    </tr>
    <tr>
        <td>[!UICONTROL 子集]</td>
        <td>如果要将项目添加到的列表具有自定义子集，请选择要将该项目添加到的子集。</td>
    </tr>
</table>

#### [!UICONTROL 删除记录]

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
   <td role="rowheader">[!UICONTROL 模型ID]</td> 
   <td>输入或映射包含要删除对象的模型的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择要删除的对象类型。</p> 
    <ul> 
     <li> <p><b>操作</b> </p> <p>选择或映射要删除的操作。</p> </li> 
     <li> <p><b>列表项</b> </p> <p>选择要从中删除项目的列表，然后输入或映射要删除项目的ID或代码</p>  </li> 
     <li> <p><b>[!UICONTROL 文件]</b> </p> <p>选择或映射要删除的文件。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>



#### [!UICONTROL 导出数据]

此操作模块使用导出定义从Anaplan中检索数据。

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
   <td>选择或映射包含要导出数据的Anaplan Workspace的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 模型ID]</td> 
   <td>输入或映射包含要导出数据的模型的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">导出定义Id</td> 
   <td> <p>输入或映射要使用的Anaplan导出定义的ID。</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### 导入数据

此操作模块将数据导入Anaplan。

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
   <td>选择或映射要从中导入数据的Anaplan Workspace的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 模型ID]</td> 
   <td>输入或映射要导入数据的模型的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">导出定义Id</td> 
   <td> <p>输入或映射要使用的Anaplan导入定义的ID。</p> 
   </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 进行自定义API调用]

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
   <td role="rowheader"> <p>[!UICONTROL 方法]</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] 自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串] </td> 
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

#### [!UICONTROL 读取记录]

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
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择要读取的记录类型。</p> 
    <ul> 
     <li> <p><b>模型</b> </p> <p>选择或映射要读取的模型的ID</p> </li> 
     <li> <p><b>模型列表</b> </p> <p>选择或映射包含要读取的列表的Workspace和模型的ID，然后选择列表。 在[!UICONTROL 数据类型]字段中，选择要读取数据还是元数据。</p> </li> 
     <li> <p><b>模型版本</b> </p> <p>选择或映射要读取的模型的ID。</p> </li> 
     <li> <p><b>用户</b> </p> <p>选择您是要返回有关正在使用的帐户的所有者的数据，还是要返回其他用户的数据。 如果选择另一个用户，请选择该用户的名称。</p> </li> 
     <li> <p><b>Workspace</b> </p> <p>选择或映射您要读取的Workspace的ID。</p> </li> 
     <li> <p><b>视图</b> </p> <p>选择或映射包含要读取的视图的模型ID。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 运行操作]

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
        <td role="rowheader">[!UICONTROL 模型ID]</td>
        <td>选择或映射要执行操作的模型的ID。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 操作类型]</td>
        <td>
          <p>选择要执行的操作</p>
            <ul>
              <li>
                <p><b>[!UICONTROL 删除]</b>
                </p>
                <p>输入或映射要删除的操作的ID。</p>
              </li>
              <li>
                <p><b>[!UICONTROL 导出]</b>
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
                  <p><b>[!UICONTROL 导入] </b>
                  </p>
                  <p style="font-weight: normal;">输入或映射要使用的导入定义的ID。</p>
                </li>
                <li>
                 <p><b>[!UICONTROL 进程]</b>
                 </p>
                  <p>输入或映射要使用的进程的ID。 </p>
                </li>
              </ul>
            </td>
          </tr>
        </tbody>
      </table>


#### [!UICONTROL 更新记录]

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
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择要更新的记录类型。</p> 
    <ul> 
     <li> <p><b>[!UICONTROL 列表项]</b> </p> <p>有关字段，请参阅本文中的<a href="#create-a-list-item" class="MCXref xref">创建列表项</a>。</p> </li> 
     <li> <p><b>[!UICONTROL 模块单元格数据]</b> </p> <p>更新单元格数据时，使用该数据的所有下游计算也会更新。</p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p><b>[!UICONTROL 模型ID]</b> </p> <p>选择或映射包含要更新的单元格的模型。</p> </li> 
       <li> <p><b>[!UICONTROL 模块ID]</b> </p> <p>选择或映射包含要更新的单元格的模块</p> </li> 
       <li> <p><b>[!UICONTROL 行项名称]</b> </p> <p>选择或映射要更新的单元格的行项</p> </li> 
       <li> <p style="font-weight: bold;">[!UICONTROL Dimension ID]</p> <p>选择或映射行项目上的维度。</p> 
       <p><b>注释：</b> 
       <ul>
       <li> Dimension键（值）必须为<code>dimensionName</code> （下一个）或<code>dimensionId</code> (ID)。</li>
       <li>项目键（值）必须为<code>itemName</code> （文本）、<code>itemCode</code> （文本）或<code>itemId</code> (ID)。</li>
       <li>Dimension和项目键必须属于相同类型（文本或ID）。
       </ul>
        </p> 
        <p>有关维度的信息，请在[!DNL Anaplan Anapedia]中搜索维度。</p> </li> 
       <li> <p><b>[!UICONTROL 值]</b> </p> <p>输入或映射单元格的新值。</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL 模型当前会计年度]</b> </p> <p>输入要更新其会计年度的模型的Workspace ID和模型ID，然后为模型输入或映射新年度。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 上载操作文件]

此操作模块会将Anaplan中的现有文件上传到Anaplan中的其他位置。
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
<td role="rowheader">[!UICONTROL 模型ID]</td>
<td>选择或映射要上传文件的模型的ID。</td>
</tr>
<tr>
<td role="rowheader">[!UICONTROL 文件ID]</td>
<td>选择或映射要上传的文件的ID。</td>
</tr>
</tbody>
</table>
</div>

### 搜索

#### [!UICONTROL 获取记录]

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
   <td role="rowheader">[!UICONTROL 记录类型]</td> 
   <td> <p>选择要检索的记录类型。</p> 
      <ul> 
       <li> <p><b>[!UICONTROL 工作区]</b> </p> </li> 
       <li> <p><b>[!UICONTROL 模型]</b> </p> </li> 
       <li> <p><b>[!UICONTROL 行项目]</b> </p> <p>选择或映射包含要检索的[!DNL line]项的模型的ID。</p> </li> 
       <li> <p><b>[!UICONTROL 模型列表]</b> </p> <p>选择或映射包含要检索的模型列表的Workspace ID和模型ID。</p> </li> 
       <li> <p><b>[!UICONTROL 模型日历]</b> </p> <p>选择或映射包含要检索的模型日历的Workspace的ID。</p> </li> 
       <li> <p><b>[!UICONTROL 模型版本]</b> </p> </li> 
       <li> <p>选择或映射包含要检索的模型版本的模型ID。</p> </li> 
       <li> <p><b>[!UICONTROL 用户]</b> </p> </li> 
       <li> <p><b>[!UICONTROL 视图]</b> </p> <p>选择是要按模块还是按模型选择视图，然后选择或映射包含要检索的视图的模块或模型的ID。</p> </li> 
      </ul> 
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 返回工作区大小]</td> 
   <td>启用此选项可返回工作区的当前大小的估计值。 此估算基于工作区中包含的所有模块的大小。</td> 
  </tr> 
 </tbody> 
</table>
