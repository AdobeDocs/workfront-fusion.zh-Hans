---
title: Adobe Journey Optimizer模块
description: 在 [!DNL Adobe Workfront Fusion] 方案中，您可以自动使用 [!DNL Adobe Journey Optimizer]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 1d0ccf4d-9f06-4210-86ec-7da7970f6a47
source-git-commit: 3ba5d67806e0d495bd4a91589d06cfb9adb25c0c
workflow-type: tm+mt
source-wordcount: '3276'
ht-degree: 0%

---

# [!DNL Adobe Journey Optimizer]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Adobe Journey Optimizer]的工作流，并将其连接到多个第三方应用程序和服务。 [!DNL Adobe Journey Optimizer]模块允许您创建、读取、更新或删除记录，或执行对[!DNL Adobe Journey Optimizer] API的自定义API调用。


如果需要有关创建方案的说明，请参阅[创建方案：项目索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] 计划*</td>
      <td>
        <p>[!UICONTROL Pro] 或更高</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Adobe Workfront] 许可证*</td>
      <td>
        <p>[!UICONTROL Plan]， [!UICONTROL Work]</p>
      </td>
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

+++

## 先决条件

在使用[!DNL Adobe Journey Optimizer]连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的[!DNL Adobe Journey Optimizer]帐户。

## Adobe Journey Optimizer API信息

Adobe Journey Optimizer连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td>{{connection.url}}</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.7.11</td> 
  </tr>
 </tbody> 
 </table>

## 创建与Adobe Journey Optimizer的连接

您可以在任意Adobe Journey Optimizer模块中创建连接。

1. 单击“连接”框旁边的&#x200B;**[!UICONTROL Add]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>选择您要连接到生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>选择您是要连接到服务帐户还是个人帐户。</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>输入您的[!UICONTROL Adobe] [!UICONTROL Client ID]。 这可以在[!UICONTROL Credentials]详细信息部分找到， [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>输入您的[!DNL Adobe] [!UICONTROL Client Secret]。 这可以在[!UICONTROL Credentials]详细信息部分找到， [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>输入您的[!DNL Adobe] [!UICONTROL Organization ID]。 这可以在[!UICONTROL Credentials]详细信息部分找到， [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Sandbox Name]</td>
        <td>输入此连接将使用的沙盒的名称。</td>
        </tr>
      </tbody>
    </table>



   <!--Markdown 0032 placeholder-->


## [!DNL Adobe Journey Optimizer]模块及其字段

配置[!DNL Adobe Journey Optimizer]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Adobe Journey Optimizer]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [配置管理](#configuration-management)
* [包管理](#package-management)
* [记录管理](#record-management)
* [消息管理](#message-management)
* [状态检查](#status-checks)
* [搜索](#searches)
* [其他](#other)




### 配置管理

* [创建配置](#create-a-configuration)
* [部署配置](#deploy-a-configuration)
* [更新配置](#update-a-configuration)
* [取消部署配置](#undeploy-a-configuration)
* [检查配置是否可以部署](#check-if-configuration-can-be-deployed)
* [删除配置](#delete-a-configuration)
* [获取配置](#get-a-configuration)

#### 创建配置

此操作模块创建上限端点或限制配置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>选择是创建上限配置还是限制配置。<ul><li><p><b>上限</b></p>继续<a href="#capping-fields" class="MCXref xref" >设置字段上限</a>。</li><li><p><b>限制</b></p>继续<a href="#throttling-fields" class="MCXref xref" >限制字段</a>。</li></ul></td> 
  </tr> 
   </tbody> 
</table>

##### 字段上限

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入或映射要配置的端点的URL。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL IMS Org ID]</td> 
   <td>输入或映射组织的Adobe IMS ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methods]</td> 
   <td>选择要在此配置中使用的方法。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Service]</td> 
   <td>选择您是使用此配置的操作还是数据源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum HTTP connections]</td> 
   <td>输入或映射与此端点的最大同时连接数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum calls]</td> 
   <td>输入或映射“时间段”字段中指定的时间段内要执行的最大呼叫数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Time period (milliseconds)]</td> 
   <td>输入或映射与最大调用数字段相关的毫秒数。</td> 
  </tr> 
 </tbody> 
</table>

##### 限制字段

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>输入或映射此配置的名称。</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>输入或映射此配置的描述。</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL URL pattern]</td> 
   <td>输入或映射要限制的终结点的URL。</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Methods]</td> 
   <td>选择要在此配置中使用的方法。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Max throughput]</td> 
   <td>选择您是使用此配置的操作还是数据源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum HTTP connections]</td> 
   <td>输入或映射与此端点的最大同时连接数。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum calls]</td> 
   <td>输入或映射您要为此端点设置的最大吞吐量。 此值必须介于200和5000之间。</td> 
  </tr> 
 </tbody> 
</table>

#### 部署配置

此操作模块部署指定的上限或限制配置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>选择是部署上限配置还是限制配置。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>输入或映射要部署的配置的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 更新配置

此操作模块可更新指定的上限或限制配置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>选择是更新上限配置还是限制配置。<ul><li><p><b>上限</b></p>有关字段，请参阅本文创建配置部分中的<a href="#capping-fields" class="MCXref xref" >字段上限</a>。</li><li><p><b>限制</b></p>有关字段，请参阅本文创建配置部分中的<a href="#throttling-fields" class="MCXref xref" >限制字段</a>。</li></ul></td> 
  </tr> 
  </tbody> 
</table>

#### 取消部署配置

此操作模块可取消部署上限或限制配置。 配置状态已更改回部署（`created`或`updated`）之前的状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>选择是取消部署上限配置还是限制配置。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>输入或映射要取消部署的配置的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 检查配置是否可以部署

此操作模块验证是否可以部署上限或限制配置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>选择您是检查上限配置还是限制配置。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>输入或映射要检查的配置的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 删除配置

此操作模块删除上限端点或限制配置。

如果已部署配置，则必须先取消部署该配置，然后才能将其删除。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>选择是删除上限配置还是限制配置。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>输入或映射要删除的配置的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 获取配置

此操作模块返回由指定ID标识的上限或限制配置。 将返回最新的定义。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>选择是检索上限配置还是限制配置。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Configuration ID]</td> 
   <td>输入或映射要检索的配置的ID。</td> 
  </tr> 
 </tbody> 
</table>




### 包管理

* [创建资源包](#create-a-package)
* [更新包](#update-a-package)
* [删除资源包](#delete-a-package)
* [查找包](#look-up-a-package)
* [导入资源包](#import-a-package)
* [Publish包](#publish-a-package)
* [提交导入](#submit-an-import)



#### 创建资源包

此操作模块创建一个多工件包。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>输入或映射包的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>输入或映射包的描述。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expiration date]</td> 
   <td>输入或映射定义包到期日期的时间戳。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package type]</td> 
   <td>选择要创建的包类型。<ul><li><p><b>完全</b></p>程序包将包含所有工件</p></li><li><p><b>部分</b></p><p>该资源包将仅包含您添加的工件。 </p></li><ul></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>如果要创建部分包，请为每个要添加的项目单击<b>添加项目</b>并指定项目的ID、类型和标题。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Sandbox]</td> 
   <td>输入或映射沙盒的名称和IMS组织ID，该沙盒包含您希望包中包含的项目。</td> 
  </tr> 
 </tbody> 
</table>

#### 更新包

此操作模块从包中添加或删除工件，或者更新包元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select action]</td> 
   <td>选择要执行的操作。<ul><li><p><b>添加工件</b></p><p>对于要添加的每个项目，单击<b>添加项目</b>并指定项目的ID、类型和标题，然后输入或映射包的到期日期。 </p></li><li><p><b>删除构件</b></p><p>对于要删除的每个项目，单击<b>添加项目</b>并指定项目的ID、类型和标题。 </p></li><li><p><b>更新元数据</b></p><p>为名称、描述或源沙盒的名称或IMS组织ID输入新值。</p></li></ul></td> 
  </tr> 
 </tbody> 
</table>

#### 删除资源包

此操作模块删除多工件包。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>输入或映射要删除的程序包的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 查找包

此操作模块可检索指定包的详细信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>输入或映射要为其返回详细信息的程序包的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 导入资源包

此操作模块获取指定目标沙盒中的冲突对象。 冲突对象表示目标沙盒中已存在的类似对象。

在导入包之前，您必须先发布包。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>输入或映射要导入的程序包的ID。</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Target sandbox]</td> 
   <td>输入或映射要从中导入包的沙盒的名称。</td> 
  </tr> 
 </tbody> 
</table>

#### Publish包

在导入包之前，您必须先发布包。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>输入或映射要发布的包的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 提交导入

该操作模块在您检查了冲突并提供替代之后，会提交资源包的导入。 结果作为有效负载提供，有效负载将启动在有效负载中指定的目标沙盒的导入作业。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>输入或映射要发布的包的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>输入或映射导入作业的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>输入或映射导入作业的描述</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Destination sandbox) Name]</td> 
   <td>输入或映射要将导入提交到的沙盒的名称。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Destination sandbox) IMS Org ID]</td> 
   <td>输入或映射要将导入提交到的沙盒的Adobe IMS组织ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source sandbox) ID]</td> 
   <td>输入或映射包含要发布的包的沙盒的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source sandbox) Type]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL (Source sandbox) Link]</td> 
   <td>输入或映射要发布的包的链接。</td> 
  </tr> 
 </tbody> 
</table>


<!--

### Artifact management

* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)

#### Copy artifacts synchronously

This action module copies artifacts from a source sandbox into a destination sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the new file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination sandbox]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to copy, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>

#### Export Artifacts asynchronously

This action module exports artifacts from the specified sandbox.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>Enter or map a name for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Enter or map a description for the export file</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Artifacts]</td> 
   <td>For each artifact you want to export, click <b>Add artifact</b> and continue to <a href="#artifact-fields" class="MCXref xref" >Artifact fields</a>.</td> 
  </tr> 
 </tbody> 
</table>

##### Artifact fields

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Enter or map the ID of the artifact.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Enter or map the artifact type, such as <code>REGISTRY_SCHEMA<code> or <code>JOURNEY</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Version]</td> 
   <td>Enter or map the visibility of the artifact. This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Enter or map the visibility (tenant or global). This applies only to Registry objects.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Found]</td> 
   <td>Select <b>Yes</b> if this item was found using a GET operation.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tasks]</td> 
   <td>For each task you want to add, click <b>Add task</b> and fill in the following:
   <ul>
   <li><p><b>Method</b></p></li>
   <li><p><b>Action</b></p></li>
   <li><p><b>Using</b></p></li>
   <li><p><b>With</b></p></li>
   </ul>
   </td> 
  </tr> 
   <tr> 
   <td role="rowheader">[!UICONTROL Messages]</td> 
   <td>For each task you want to add, click <b>Add message</b> and fill in the following:
   <ul>
   <li><p><b>Status</b></p><p>Enter or map the status that this message represents, such as <code>ERROR</code>.</li>
   <li><p><b>Attempt</b></p><p>Enter or map the attempt number related to this message. This may be useful if different attempts produce different messages.</p></li>
   <li><p><b>Message</b></p><p>Enter or map the text of the message.</li>
   <li><p><b>Object</b></p></li>
   </ul>
   </td> 
  </tr> 
 </tbody> 
</table>



#### Import Artifacts asynchronously

This action module imports a snapshot containing artifacts.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Snapshot ID]</td> 
   <td>Enter or map the ID of the snapshot you want to import.</td> 
  </tr> 
 </tbody> 
</table>

-->

### 记录管理

* [创建记录](#create-a-record)
* [更新记录](#update-a-record)
* [删除记录](#delete-a-record)
* [修补记录](#patch-a-record)
* [获取记录](#get-a-record)

#### 创建记录

此操作模块创建新的内容模板或内容片段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>选择是创建内容模板还是内容片段。<ul><li><p><b>内容模板</b></p>继续<a href="#template-fields" class="MCXref xref" >模板字段</a>。</li><li><p><b>内容片段</b></p>继续<a href="#fragment-fields" class="MCXref xref" >片段字段</a>。</li></ul></td> 
  </tr> 
  </tbody> 
</table>

##### 模板字段

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>输入或映射此内容模板的名称。</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>输入或映射此内容模板的描述。</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>选择要创建的模板类型。</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channels]</td> 
   <td>选择此模板中包含的渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content template origin]</td> 
   <td>选择此模板的源。</td>  
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>要在新模板中包含自定义属性，请选择“添加元数据”，然后输入或映射元数据的键和值。 对每个要包含的自定义字段重复执行上述操作。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email HTML]</td> 
   <td>输入或映射此模板中包含的电子邮件HTML。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor context]</td> 
   <td>要在电子邮件中包含自定义属性，请选择“添加编辑器上下文”，然后输入或映射上下文的键和值。 对每个要包含的自定义字段重复执行上述操作。</td> 
  </tr> 
 </tbody> 
</table>

##### 片段字段

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> <tr> 
   <td role="rowheader">[!UICONTROL Name]</td> 
   <td>输入或映射此内容片段的名称。</td> 
<tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>输入或映射此内容片段的描述。</td> 
  </tr> 
<tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>选择要创建的模板类型。</td> 
  </tr> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Channels]</td> 
   <td>选择此模板中包含的渠道。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content fragment origin]</td> 
   <td>选择此片段的源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Metadata]</td> 
   <td>要在新模板中包含自定义属性，请选择“添加元数据”，然后输入或映射元数据的键和值。 对每个要包含的自定义字段重复执行上述操作。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content]</td> 
   <td>输入或映射片段的内容。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Editor context]</td> 
   <td>要在电子邮件中包含自定义属性，请选择“添加编辑器上下文”，然后输入或映射上下文的键和值。 对每个要包含的自定义字段重复执行上述操作。</td> 
  </tr> 
 </tbody> 
</table>

#### 更新记录

此操作模块更新内容模板或片段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>选择是更新上限配置还是限制配置。<ul><li><p><b>模板</b></p>有关字段，请参阅本文创建记录部分中的<a href="#template-fields" class="MCXref xref" >模板字段</a>。</li><li><p><b>片段</b></p>有关字段，请参阅本文创建记录一节中的<a href="#fragment-fields" class="MCXref xref" >片段字段</a>。</li></ul></td> 
  </tr> 
  </tbody> 
  </table>

#### 删除记录

此操作模块可删除内容模板或内容片段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>选择您要删除内容模板还是内容片段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Template/Fragment ID]</td> 
   <td>输入或映射要删除的模板或片段的ID。</td> 
  </tr> 
 </tbody> 
</table>

#### 修补记录

此操作模块使用带JSON指针格式的PATCH更新记录

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>选择是要修补内容模板还是内容片段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Template/Fragment ID]</td> 
   <td>输入或映射要修补的模板或片段的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Payload data]</td> 
   <td>要将记录添加到此修补程序的负载中，请执行以下操作： <ol><li>单击<b>添加记录</b>。</li><li>选择操作：“添加”、“移除”或“替换”。</li><li>在“路径”字段中，选择要为名称或说明打补丁。</li><li> 在从字段中，输入或映射包含JSON指针值的字符串。</li><li>在“值”字段中，输入要在工序中使用的值。</li></ol></td> 
  </tr> 
 </tbody> 
</table>

#### 获取记录

此操作模块返回由指定ID标识的内容模板或内容片段。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>选择是检索内容模板还是内容片段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Template/Fragment ID]</td> 
   <td>输入或映射要检索的模板或片段的ID。</td> 
  </tr> 
 </tbody> 
</table>


### 消息管理

* [触发单一消息执行](#trigger-a-unitary-message-execution)
* [触发基于受众的消息](#trigger-an-audience-based-message)
* [检查基于受众的消息的状态](#check-the-status-for-audience-based-message)



#### 触发单一消息执行

此操作模块会向您指定的收件人触发一条单一消息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request ID]</td> 
   <td>输入或映射与此消息关联的请求的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>输入或映射与此消息关联的营销活动的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Recipients]</td> 
   <td>对于要接收此邮件的每个收件人，单击<b>添加收件人</b>并输入以下内容：
   <ul>
   <li><p><b>类型</b></p>选择 <code>aep</code>。</li>
   <li><p><b>用户 ID</b></p>输入或映射收件人的Adobe Experience Platform配置文件标识符。</li>
   <li><p><b>命名空间</b></p>输入或映射收件人的Adobe Experience Platform配置文件命名空间。</li>
   <li><p><b>电子邮件地址</b></p></li>
   <li><p><b>手机号码</b></p></li>
   <li><p><b>名字</b></p></li>
   <li><p><b>姓氏</b></p></li>
   <li><p><b>产品</b></p>输入或映射与此消息关联的产品。 这用于消息内容中的动态变量替换。</li>
   </ul></td> 
  </tr> 
 </tbody> 
</table>

#### 触发基于受众的消息

此操作模块根据您指定的请求和活动，触发基于受众的消息的执行。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Request ID]</td> 
   <td>输入或映射与此消息关联的请求的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>输入或映射与此消息关联的营销活动的ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Product]</td> 
   <td>输入或映射与此消息关联的产品。 这用于消息内容中的动态变量替换。</td> 
  </tr> 
 </tbody> 
</table>

#### 检查基于受众的消息的状态

此操作模块检查基于受众的批量消息的状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Message execution ID]</td> 
   <td>输入或映射要检查的消息执行ID。</td> 
  </tr> 
 </tbody> 
</table>

### 状态检查

<!--* [Check service health](#check-service-health)-->
* [检查导入依赖关系](#check-the-import-dependencies)
* [检查导入作业的状态](#check-the-status-of-an-import-job)

<!--

#### Check service health

This action module checks that the service represented by the connection is running.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Adobe Journey Optimizer], see <a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >Create a connection to [!DNL Adobe Journey Optimizer]</a> in this article.</td> 
  </tr> 
 </tbody> 
</table>

-->

#### 检查导入依赖关系

此操作模块检查包对象的依赖关系。 这允许您检查您是否具有导入包对象的权限。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>输入或映射要检查其权限的包ID。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Target sandbox]</td> 
   <td>输入或映射要将包导入到的沙盒的名称。</td> 
  </tr> 
 </tbody> 
</table>

#### 检查导入作业的状态

此操作模块检查导入作业是成功还是失败。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Job ID]</td> 
   <td>输入或映射要为其检索数据的作业的ID。</td> 
  </tr> 
 </tbody> 
</table>

### 搜索

* [列出所有依赖对象](#list-all-dependent-objects)
* [列出配置](#list-configurations)
* [列出导出和导入作业](#list-export-and-import-jobs)
* [列出包](#list-packages)
* [列出记录](#list-records)

#### 列出所有依赖对象

此搜索模块列出指定程序包中对象的所有依赖对象

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package objects]</td> 
   <td>对于包中要返回其依赖对象的每个对象，单击<b>添加对象</b>并输入对象的名称和类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Package ID]</td> 
   <td>输入或映射要为其列出依赖对象的程序包的ID。</td> 
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Target sandbox]</td> 
   <td>输入或映射沙盒的名称，该沙盒包含要为其列出依赖对象的包。</td> 
  </tr> 
 </tbody> 
</table>

#### 列出配置

此操作模块列出了所有上限或限制配置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select configuration type]</td> 
   <td>选择您要列出上限配置还是限制配置。</td> 
  </tr> 
 </tbody> 
</table>

#### 列出导出和导入作业

此搜索模块列出了当前的导出和导入作业。 您可以使用查询参数来筛选列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
      <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
      <td>选择是按创建日期还是按修改日期对结果进行排序。</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Query parameter]</td> 
   <td>对于要作为筛选依据的每个查询参数，单击<b>添加查询参数</b>，然后选择字段和运算符，输入筛选器的字段值。</td> 
  </tr> 
 </tbody> 
</table>



#### 列出包

此搜索模块列出了您组织中的所有资源包。 您可以使用查询参数来筛选列表。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
      <td>输入或映射您希望模块在每个方案执行周期内返回的最大记录数。</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
      <td>选择是按创建日期还是按修改日期对结果进行排序。</td>
  </tr> 
    <tr> 
   <td role="rowheader">[!UICONTROL Query parameter]</td> 
   <td>对于要作为筛选依据的每个查询参数，单击<b>添加查询参数</b>，然后选择字段和运算符，输入筛选器的字段值。</td> 
  </tr> 
 </tbody> 
</table>

#### 列出记录

此搜索模块列出了所有上限或限制配置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select content type]</td> 
   <td>选择是检索内容模板还是内容片段。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td>输入或映射要作为此列表排序依据的参数名称。 添加<code>-</code>或<code>+</code>以按降序或升序排序。 如果未指定符号，则列表将降序排序。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start]</td> 
   <td>此字段用于分页。 根据排序依据字段中指定的属性，输入或映射下一页的条件。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Order by]</td> 
   <td>输入或映射要作为此列表排序依据的参数名称。 添加<code>-</code>或<code>+</code>以按降序或升序排序。 如果未指定符号，则列表将降序排序。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter by property]</td> 
   <td>对于要添加的每个属性筛选器，单击<b>添加项</b>并输入属性的键和值。 列表中包括为该属性指定的值的记录。</td> 
  </tr> 
 </tbody> 
</table>


### 其他


#### 进行自定义API调用

此操作模块对Adobe Journey Optimizer API进行自定义API调用。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td>有关创建与[!DNL Adobe Journey Optimizer]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-journey-optimizer" class="MCXref xref" >创建与[!DNL Adobe Journey Optimizer]</a>的连接。</td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]</td>
      <td>
        <p>输入相对于基本URL的路径。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅[!DNL Adobe Workfront Fusion]</a>中的<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法。</p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>[!DNL Workfront Fusion] 自动添加授权、<code>x-api-key</code>和<code>x-gw-ims-org-id</code>标头。</p>
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







<!--

* [Check if configuration can be deployed](#check-if-configuration-can-be-deployed)
* [Check service health](#check-service-health)
* [Check the import dependencies](#check-the-import-dependencies)
* [Check the status for audience-based message](#status-for-audience-based-message)
* [Copy artifacts synchronously](#copy-artifacts-synchronously)
* [Create a configuration](#create-a-configuration)
* [Create a package](#create-a-package)
* [Create a record](#create-a-record)
* [Delete a configuration](#delete-a-configuration)
* [Delete a package](#delete-a-package)
* [Delete a record](#delete-a-record)
* [Deploy a configuration](#deploy-a-configuration)
* [Export artifacts asynchronously](#export-artifacts-asynchronously)
* [Get a configuration](#get-a-configuration)
* [Get a record](#get-a-record)
* [Import a package](#import-a-package)
* [Import artifacts asynchronously](#import-artifacts-asynchronously)
* [List all dependent objects](#list-all-dependent-objects)
* [List export and import jobs](#list-import-and-export-jobs)
* [Look up a package](#look-up-a-package)
* [Make a custom API call](#make-a-custom-api-call)
* [Patch a record](#patch-a-record)
* [Publish a package](#publish-a-package)
* [Submit an import](#submit-an-import)
* [Trigger a unitary message execution](#trigger-a-unitary-message-execution)
* [Trigger an audience-based message](#trigger-an-audience-based-message)
* [Undeploy a configuration](#undeploy-a-configuration)
* [Update a configuration](#update-a-configuration)
* [Update a package](#update-a-package)
* [Update a record](#update-a-record)
* [List configurations](#list-configurations)
* [List packages](#list-packages)
* [List records](#list-records)

-->
