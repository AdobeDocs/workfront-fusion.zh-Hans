---
title: Adobe Lightroom模块
description: 通过Adobe Lightroom模块，您可以根据Adobe Lightroom帐户中的事件启动Adobe Workfront Fusion方案。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 3f29ab35-7a90-4afb-a283-4faaacec5b15
source-git-commit: 4d31a447d0d8d91ef4f86d8fd0bc63663b0f5ad0
workflow-type: tm+mt
source-wordcount: '2770'
ht-degree: 0%

---

# [!DNL Adobe Lightroom]模块

在[!DNL Adobe Workfront Fusion]方案中，您可以自动使用[!DNL Adobe Lightroom]的工作流，并将其连接到多个第三方应用程序和服务。

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

在使用[!DNL Adobe Lightroom]连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的[!DNL Adobe Lightroom]帐户。
* 您必须在Adobe Admin Console中配置OAuth Web应用程序。 有关详细信息，请参阅本文中的[在Adobe Admin Console中配置OAuth应用程序](#configure-an-oauth-application-in-the-adobe-admin-console)。

## Adobe Lightroom API信息

Adobe Lightroom连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本URL</td> 
   <td>https://lr.adobe.io</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.17.128</td> 
  </tr>
 </tbody> 
 </table>



## 创建与Adobe Lightroom的连接

要连接到Adobe Lightroom，您必须首先在Adobe Admin Console中配置OAuth应用程序。 配置此应用程序后，您可以从Workfront Fusion创建连接。

### 在Adobe Admin Console中配置OAuth应用程序

1. 开始在Adobe Admin Console中配置OAuth Web应用程序。

   有关说明，请参阅Adobe开发人员文档中的[User Authentication Implementation Guide](https://developer.adobe.com/developer-console/docs/guides/authentication/UserAuthentication/implementation)。
1. 配置OAuth Web应用程序时，输入以下值：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">[!UICONTROL 范围]</td>
        <td>
          <ul>
            <li>AdobeID</li>
            <li>lr_partner_rendition_api</li>
            <li>openid</li>
            <li>offline_access</li>
            <li>lr_partner_api</li>
          </ul>
        </td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 重定向URI]</td>
        <td><code>https://app.workfrontfusion.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 重定向URI模式]</td>
        <td><code>https://app\.workfrontfusion\.com/oauth/cb/adobe-lightroom5</code></td>
        </tr>
      </tbody>
    </table>

### 从Workfront Fusion创建与Adobe Lightroom的连接

要为您的[!DNL Adobe Lightroom]模块创建连接：

1. 在任意Adobe Lightroom模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

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
        <td role="rowheader">[!UICONTROL 客户端ID]</td>
        <td>输入您的[!UICONTROL Adobe] [!UICONTROL 客户端ID]。 可在[!UICONTROL Credentials]的 [!DNL Adobe Developer Console]</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的[!DNL Adobe] [!UICONTROL 客户端密钥]。 可在[!UICONTROL Credentials]的 [!DNL Adobe Developer Console]</td>
        </tr>
      </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。


## Adobe Lightroom模块及其字段

配置[!DNL Adobe Lightroom]模块时，[!DNL Workfront Fusion]显示下面列出的字段。 除此以外，可能还会显示其他[!DNL Adobe Lightroom]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [其他](#other)
* [资源](#assets)
* [相册](#albums)

### 其他

* [运行状况检查](#health-check)
* [检索用户目录元数据](#retrieve-user-catalog-metadata)

#### 运行状况检查

此操作模块可检索Lightroom服务器版本ID，以验证Lightroom服务当前是否正在运行。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 凭据]</td>
      <td>
        <p>如果要提供特定凭据以确保特定服务器正在运行，请单击<b>添加项</b>并输入凭据。</p><p>自动添加授权标头。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 检索用户目录元数据

此操作模块从Adobe Lightroom中的目录检索元数据。 目录包含资产、专辑或其他资源。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 凭据]</td>
      <td>
        <p>如果要提供特定凭据以确保可以访问正确的用户帐户，请单击“添加项目”并输入凭据。</p><p>自动添加授权标头。</p>
      </td>
    </tr>
  </tbody>
</table>

### 资源

* [创建资源原始文件](#create-an-asset-original-file)
* [创建资产](#create-an-asset)
* [创建资源外部XMP开发设置文件](#create-an-asset-external-xmp-develop-setting-file)
* [为原始文件生成演绎版](#generate-renditions-for-an-original-file)
* [获取目录资源](#get-a-catalog-asset)
* [获取最新的资源外部XMP开发设置](#get-the-latest-asset-external-xmp-develop-setting-file)
* [获取最新的资源演绎版](#get-the-latest-asset-rendition)
* [检索资源](#retrieve-assets)

#### 创建资源原始文件

此操作模块会为资产创建和上传原始文件。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射包含资产的目录的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 资产ID]</td>
      <td>
        <p>输入或映射要为其创建和上传文件的资源的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 内容长度（字节）]</td>
      <td>
        <p>输入或映射内容的长度（字节）。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 字节范围]</td>
      <td>
        <p>输入或映射请求的字节范围，包括第一个和最后一个字节以及RFC 2616中定义的实体长度。 仅当数据过大而无法在一次调用中上传时，才应包含此信息。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 内容类型]</td>
      <td>
        <p>为新文件选择内容类型。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 创建资产

此操作模块使用初始元数据和导入信息创建新资源。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射将在其中创建资产的目录的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 资产ID]</td>
      <td>
        <p>输入或映射新资源的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 资产类型]</td>
      <td>
        <p>选择资源是图像还是视频。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 创建日期时间用户]</td>
      <td>
        <p>输入或映射格式为<code>YYYY-MM-DDT00:00:00-00:00</code>的日期。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 日期时间用户已更新]</td>
      <td>
        <p>输入或映射格式为<code>YYYY-MM-DDT00:00:00-00:00</code>的日期。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 捕获日期]</td>
      <td>
        <p>输入或映射格式为<code>YYYY-MM-DDT00:00:00-00:00</code>的资源捕获日期。 如果捕获日期设置为<code>0000-00-00T00:00:00</code>，服务器将设置此项。 </p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 文件名]</td>
      <td>
        <p>输入或映射要导入到Lightroom中的资源的文件名。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 导入设备的名称]</td>
      <td>
        <p>输入或映射导入资产的设备的名称。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 导入用户的帐户ID]</td>
      <td>
        <p>输入或映射导入资源的用户的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 导入时间戳]</td>
      <td>
        <p>输入或映射格式为<code>YYYY-MM-DDT00:00:00-00:00</code>的日期。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 创建资源外部XMP开发设置文件

此操作模块支持两个工作流：上传资源的外部XMP开发设置文件，或通过从其他资源的外部xmp开发设置文件复制来创建外部XMP开发设置文件。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 内容长度（字节）]</td>
      <td>
        <p>输入或映射内容的长度（字节）。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 上传新的或复制XMP/开发文件]</td>
      <td>
        <p>选择是上传新文件，还是从现有资源复制文件。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射要创建资产的目录的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 资产ID]</td>
      <td>
        <p>输入或映射要上传或复制文件的目标资产ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL XMP/develop文件链接]</td>
      <td>
        <p>输入或映射要上载或复制文件的链接。</p><p>如果复制文件，此文件必须为JSON；如果上传文件，此文件必须为XML。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 为原始文件生成演绎版

此操作模块可异步生成原始文件的演绎版。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 演绎版类型（以分号分隔）]</td>
      <td>
        <p>输入要创建的演绎版的演绎版类型。 如果输入多种类型，请用分号(；)分隔。 <p>可能的类型：</p><ul><li><code>fullsize</code></li><li><code>2560</code></li></ul></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 内容长度（字节）]</td>
      <td>
        <p>输入或映射内容的长度（字节）。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射要生成演绎版的目录的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 资产ID]</td>
      <td>
        <p>输入或映射要为其创建文件演绎版的资源的ID。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 获取目录资源

此操作模块可检索有关目录中单个资产的信息。 目录必须由用户拥有，该用户的凭据在此模块中使用的连接中呈现。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射包含资产的目录的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 资产ID]</td>
      <td>
        <p>输入或映射要为其检索信息的资源的ID。</p>
      </td>
    </tr>
  </tbody>
</table>


#### 获取最新的资源外部XMP开发设置文件

此操作模块可检索最新的资源外部XMP设置文件。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射目录ID，该目录包含与XMP开发设置文件关联的资源。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 资产ID]</td>
      <td>
        <p>输入或映射与XMP开发设置文件关联的资源的ID。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 获取最新的资源演绎版

此操作模块可检索指定类型的最新资产演绎版。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射包含要检索其演绎版的资源的目录的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 资产ID]</td>
      <td>
        <p>输入或映射要为其检索演绎版的资源的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 演绎版类型]</td>
      <td>
        <p>选择要检索的演绎版类型。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 检索资源

此操作模块可检索由用户拥有的资产，该用户的凭据表示在此模块中使用的连接中。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射包含资产的目录的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 开始时间戳]</td>
      <td>
        <p>输入或映射时间戳。 模块返回在此时间戳之后更新的记录。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 返回在给定时间之前捕获的资产]</td>
      <td>
        <p>输入格式为<code>YYYY-MM-DDT00:00:00</code>的日期。 模块会返回在此日期之前捕获的结果。</p><p> 此字段不能与字段<code>Return assets captured after given time</code>一起使用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 返回在给定时间后捕获的资产]</td>
      <td>
        <p>输入格式为<code>YYYY-MM-DDT00:00:00</code>的日期。 模块会返回在此日期之前捕获的结果。</p><p> 此字段不能与字段<code>Return assets captured before given time</code>一起使用。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 返回的最大资产数]</td>
      <td>
        <p>输入您希望模块在每个方案执行周期内返回的最大记录数。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL SHA256原始文件的哈希值]</td>
      <td>
        <p>输入或映射原始文件的哈希值。 将返回具有匹配哈希的Assets。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 隐藏栈栈内的资产？”]</td>
      <td>
        <p>选择“是”可隐藏栈栈内的资产（不返回栈栈内的资产）。 选择否可在结果中包含栈栈内的资源。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Asset子类型值]</td>
      <td>
        <p>输入或映射要返回的子类型值的以分号分隔的列表。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 资产ID]</td>
      <td>
        <p>输入或映射最多100个资源ID，用逗号分隔。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 要排除的资源类型]</td>
      <td>
        <p>选择是要排除完整还是不完整的资源。 要包含所有资源，请将此字段留空。</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 组值]</td>
      <td>
        <p>输入或映射以分号分隔的组值列表。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 名称值]</td>
      <td>
        <p>输入或映射以分号分隔的名称值列表。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 收藏夹状态]</td>
      <td>
        <p>输入或映射要返回结果的收藏夹状态。</p>
      </td>
    </tr>
    </tr>
  </tbody>
</table>

<!--BECKY START HERE-->

### 相册

* [将资源添加到相册](#add-assets-to-an-album)
* [创建相册](#create-an-album)
* [删除相册](#delete-an-album)
* [获取相册](#get-an-album)
* [列出相册的资产](#list-assets-of-an-album)
* [检索相册](#retrieve-albums)
* [更新相册](#update-album)

#### 将资源添加到相册

此操作模块向指定的影集添加一个或多个资产。 在一个执行周期内最多可添加50个资源。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射包含要添加资产的相册的目录ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 专辑ID]</td>
      <td>
        <p>输入或映射要添加资产的相册的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Assets]</td>
      <td>
        <p>对于要添加到相册的每个资源，单击<b>添加项</b>并输入以下字段。</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 资产ID]</td>
      <td>
        <p>输入或映射要添加到相册的资源的ID</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 此资产是否为专辑封面？]</td>
      <td>
        <p>选择是否希望将此资源显示为表示相册的图像。</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 顺序]</td>
      <td>
        <p></p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 元数据]</td>
      <td>
        <p>输入或映射要包含在该资源中的任何元数据。 必须为最大长度为1-24个字符的单个文本字符串。</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 远程ID]</td>
      <td>
        <p>输入资产的标识符。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 创建相册

此操作模块可在Lightroom中创建新相册。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射要创建相册的目录ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 专辑ID]</td>
      <td>
        <p>输入或映射新相册的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtype]</td>
      <td>
        <p>选择相册的子类型。</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL API密钥]</td>
      <td>
        <p>输入正在创建相册的服务的API密钥。</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 创建日期时间用户]</td>
      <td>
        <p>输入或映射格式为<code>YYYY-MM-DDT00:00:00-00:00Z</code>的日期。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 日期时间用户已更新]</td>
      <td>
        <p>输入或映射格式为<code>YYYY-MM-DDT00:00:00-00:00Z</code>的日期。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 相册名称]</td>
      <td>
        <p>输入或映射新相册的名称。</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 封面ID]</td>
      <td>
        <p>输入或映射要用作此相册封面的资产ID。</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 远程ID]</td>
      <td>
        <p>输入资产的标识符。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 创建日期]</td>
      <td>
        <p>输入或映射格式为<code>YYYY-MM-DDT00:00:00-00:00Z</code>的日期。</p>
      </td>
    <tr>
      <td role="rowheader">[!UICONTROL 更新日期]</td>
      <td>
        <p>输入或映射格式为<code>YYYY-MM-DDT00:00:00-00:00Z</code>的日期。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 是否删除了专辑？]</td>
      <td>
        <p>如果删除了外部附属内容，则启用此选项。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL，用于编辑附属内容]</td>
      <td>
        <p>如果存在用户可编辑此相册内容的URL，请在此处输入该URL。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL of location to view affiliated content]</td>
      <td>
        <p>如果存在用户可查看此相册内容的URL，请在此处输入该URL。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 删除相册

此操作模块删除相册。

已删除的相册必须由当前要删除该相册的同一客户端应用程序创建，并且必须是子类型`project`或`project_set`。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射包含要删除的相册的目录ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 专辑ID]</td>
      <td>
        <p>输入或映射要删除的相册的ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 删除子专辑？]</td>
      <td>
        <p>选择是否要删除已删除相册的子相册。</p>
      </td>
    </tr>
  </tbody>
</table>

### 获取相册

此操作模块可检索指定的相册

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射包含要检索的相册的目录ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 专辑ID]</td>
      <td>
        <p>输入或映射要检索的相册ID。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 列出相册的资产

此操作模块可检索指定影集中的资产列表。



#### 检索相册

此操作模块可检索指定目录中的相册列表。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射包含要检索的相册的目录ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Subtypes]</td>
      <td>
        <p>输入或映射要检索的相册ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 当前结果前面的专辑名称]</td>
      <td>
        <p>如果要分页结果，请输入或映射上一页上一张相册的名称。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 返回的最大相册数]</td>
      <td>
        <p>设置[!DNL Workfront Fusion]在一个执行周期内返回的最大资源数。 此字段的默认值为100。如果限制边界处的多个影集具有相同的<code>name_after</code>值，则此模块返回的影集可能超过此限制。</p>
      </td>
    </tr>
  </tbody>
</table>

#### 更新相册

此操作模块更新指定的相册。

更新的相册必须由当前进行更新的同一客户端应用程序创建，并且必须是子类型`project`或`project_set`。

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
      <td>有关创建与[!DNL Adobe Lightroom]的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-lightroom" class="MCXref xref" >创建与[!DNL Adobe Lightroom]</a>的连接。</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 目录ID]</td>
      <td>
        <p>输入或映射包含要更新的相册的目录ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 专辑ID]</td>
      <td>
        <p>输入或映射要更新的相册ID。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">其他字段</td>
      <td>
      <td>有关此模块中其他字段的说明，请参阅本文中的<a href="#create-an-album" class="MCXref xref" >创建相册</a>。</td>
      </td>
    </tr>
  </tbody>
</table>
