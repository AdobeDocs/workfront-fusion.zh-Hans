---
title: Adobe Experience Manager Assets模块
description: 借助适用于Adobe Workfront Fusion的Adobe Experience Manager Assets连接器，您可以创建、上传和更新资源，以及复制或移动文件夹和资源。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: d62a8bd4675c034581f6cf5f3a1e61c177de5ebc
workflow-type: tm+mt
source-wordcount: '3727'
ht-degree: 2%

---

# Adobe Experience Manager Assets模块

借助适用于Adobe Workfront Fusion的Adobe Experience Manager Assets连接器，您可以创建、上传和更新资源，以及复制或移动文件夹和资源。

有关Adobe Experience Manager Assets连接器的视频介绍，请参阅：

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

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
   <p>旧版：用于自动化和集成的Workfront Fusion </p>
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

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

* 您必须拥有Adobe Experience Manager Assets帐户才能使用这些模块。
* 您必须在Adobe Developer控制台中设置服务器到服务器流程。

  有关在Adobe Developer控制台中设置服务器到服务器流的说明，请参阅[为服务器端API生成访问令牌](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=zh-Hans#the-server-to-server-flow)。
* 您的Adobe Experience Manager技术帐户必须具有写入权限。

  有关向Adobe Experience Manager技术帐户添加写入权限的说明，请参阅Adobe Experience Manager文档中的[服务凭据](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials)。

## Adobe Experience Manager Assets API信息

Adobe Experience Manager Assets连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## 将Adobe Experience Manager Assets连接到Workfront Fusion {#connect-adobe-experience-manager-assets-to-workfront-fusion}

要为您的Adobe Experience Manager Assets模块创建连接，请执行以下操作：

1. 单击“连接”框旁边的“添加”。

2. 选择正在创建的连接类型：

   * **AEM Assets as a Cloud Service**

     此配置需要来自Adobe Admin Console的信息。

   * **AEM Assets Basic (Adobe Managed Services)**

     此配置需要用户名和密码。

3. 填写要创建的连接类型的字段。

   对于AEM Assets as a Cloud Service，请参阅[配置AEM Assets as a Cloud Service的连接](#configure-the-connection-for-aem-assets-as-a-cloud-service)。

   对于AEM Assets Basic (Adobe Managed Services)，请参阅[配置AEM Assets Basic的连接](#configure-the-connection-for-aemassets-basic-adobe-managed-services)。

4. 单击&#x200B;**继续**&#x200B;保存连接并返回模块。


### 为AEM Assets as a Cloud Service配置连接

>[!NOTE]
>
>* 这些字段的信息是在Adobe Developer Console中设置服务器到服务器流时生成的。 您可以在作为该设置的一部分生成的服务凭据JSON文件中找到这些值。
>
>   有关在Adobe Developer Console上设置服务器到服务器流的说明，请参阅[为服务器端API生成访问令牌](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html?lang=zh-Hans#the-server-to-server-flow)。
>
>* 您的Adobe Experience Manager技术帐户必须具有写入权限。
>
>   有关向Adobe Experience Manager技术帐户添加写入权限的说明，请参阅Adobe Experience Manager文档中的[服务凭据](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials)。


<table style="table-layout:auto"> 
          <col/>
          <col/>
          <tbody>
              <tr>
                  <td role="rowheader">连接名称</td>
                  <td>
                      <p>输入此连接的名称。</p>
                  </td>
              </tr>
              <tr>
                  <td role="rowheader">实例URL，不带尾随斜杠</td>
                  <td>输入Adobe Experience Manager实例的URL。 不要在URL末尾包含斜杠<code>/</code>。</td>
              </tr>
              <tr>
                  <td role="rowheader">帐户详细信息填写选项</td>
                  <td>选择是要提供描述帐户详细信息的JSON，还是要手动输入详细信息。</td>
              </tr>
              <tr>
                  <td role="rowheader">JSON格式的技术帐户详细信息</td>
                  <td>如果提供JSON，请输入或粘贴描述您帐户详细信息的JSON。</td>
              </tr>
              <tr>
                  <td role="rowheader">客户端 ID</td>
                  <td>如果手动输入详细信息，请输入在服务器到服务器设置中生成的客户端ID。</td>
              </tr>
              <tr>
                  <td role="rowheader">客户端密码</td>
                  <td>如果手动输入详细信息，请输入在服务器到服务器设置中生成的客户端密钥。</td>
              </tr>
              <tr>
                  <td role="rowheader">技术帐户ID</td>
                  <td>如果手动输入详细信息，请输入技术帐户的ID。 这是客户端凭据JSON文件中的“id”字段。</td>
              </tr>
              <tr>
                  <td role="rowheader">组织ID</td>
                  <td class="">如果人工输入详细信息，请输入组织的ID。 这是客户端凭据JSON文件中的“org”字段。</td>
              </tr>
              <tr>
                  <td role="rowheader">元范围</td>
                  <td>输入在服务器到服务器设置中生成的元范围。</td>
              </tr>
              <tr>
                  <td role="rowheader">私钥</td>
                  <td>输入在服务器到服务器设置中生成的私钥。 要提取私钥，请单击“提取”，然后输入要提取的文件和文件的密码。</td>
              </tr>
              <tr>
                  <td role="rowheader">身份验证 URL</td>
                  <td>输入此帐户的身份验证URL。</td>
              </tr>
          </tbody>
      </table>


### 为AEM Assets Basic (Adobe Managed Services)配置连接

<table style="table-layout:auto"> 
        <col/>
        <col />
        <tbody>
            <tr>
                <td role="rowheader">连接名称</td>
                <td>
                    <p>输入此连接的名称。</p>
                </td>
            </tr>
            <tr>
                <td role="rowheader">实例URL，不带尾随斜杠</td>
                <td>输入Adobe Experience Manager实例的URL。 不要在URL末尾包含斜杠<code>/</code>。</td>
            </tr>
            <tr>
                <td role="rowheader">用户名</td>
                <td>输入此连接使用的AEM Assets帐户的用户名。</td>
            </tr>
            <tr>
                <td role="rowheader">密码</td>
                <td>输入此连接使用的AEM Assets帐户的密码。</td>
            </tr>
        </tbody>
    </table>


## Adobe Experience Manager Assets模块及其字段

配置Adobe Experience Manager Assets模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Adobe Experience Manager Assets字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [文件操作](#files-operations)
* [其他](#other)
* [Assets（创作API）](#assets-author-api)
* [事件（创作API）](#events-author-api)
* [元数据（创作API）](#metadata-author-api)
* [导入（创作API）](#import-author-api)
* [关系（创作API）](#relations-author-api)
* [文件夹（文件夹API）](#folders-folders-api)

### 文件操作

* [完成上传](#complete-upload)
* [获取预签名的存储](#get-presigned-storage)
* [启动上载](#initiate-upload)
* [上传资源](#upload-an-asset)

#### 完成上传

上传文件的所有部分后，此操作模块会完成启动的上传。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件名</td> 
   <td> <p>输入或映射上载文件的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">上载令牌</td> 
   <td>输入或映射由启动提供的二进制文件的上载令牌。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">MIME类型</td> 
   <td>输入或映射已完成文件的MIME类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">完整URI</td> 
   <td>输入或映射文件的完整URI。</td> 
  </tr> 
 </tbody> 
</table>


#### 获取预签名的存储

此操作模块会创建一个预签名的临时URL，以便从AEM安全地上传或下载文件，而无需直接凭据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">查找类型</td> 
   <td> <p>选择是要按资产路径还是按其ID查找资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资产</td> 
   <td>选择资源的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UDID</td> 
   <td>输入或映射资源的UDID。</td> 
  </tr> 
 </tbody> 
</table>

#### 启动上载

此操作模块将启动上载。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">目标</td> 
   <td> <p>选择要上载文件的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件名</td> 
   <td> <p>输入或映射已上传文件的名称</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">最大文件大小</td> 
   <td>输入或映射已上载文件的大小（以字节为单位）。</td> 
  </tr> 
 </tbody> 
</table>


#### 上传资源

此操作模块会将资源上传到您的Adobe Experience Manager Assets帐户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">目标</td> 
   <td> <p>选择要上传资源的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Source文件</td> 
   <td>输入或映射源文件的名称和数据。</td> 
  </tr> 
 </tbody> 
</table>

### 其他


* [复制文件夹或资源](#copy-a-folder-or-asset)
* [创建记录](#create-a-record)
* [删除文件夹、资源或演绎版](#delete-a-folder-asset-or-rendition)
* [获取文件夹列表](#get-a-folder-listing)
* [进行自定义API调用](#make-a-custom-api-call)
* [移动文件夹或资源](#move-a-folder-or-asset)
* [更新记录](#update-a-record)



#### 复制文件夹或资源

此操作模块会将文件夹或资产复制到Adobe Experience Manager Assets帐户中的其他位置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择您要复制文件夹还是资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹/资产</td> 
   <td>选择或映射要复制的文件夹或资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">目标路径</td> 
   <td>选择路径，或将路径映射到新文件夹或资源的位置。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">复制的文件夹/资产的名称</td> 
   <td>输入新文件夹或资源的名称。 Adobe Experience Manager Assets中显示的文件夹名称与原始名称相同。 此处输入的名称将显示在新文件夹或资产的URL中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">复制子项</td> 
   <td>如果复制文件夹，请启用此选项以复制文件夹中的任何子文件夹或资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">覆盖</td> 
   <td>启用此选项以覆盖目标位置中与要复制的文件夹或资源同名的任意文件夹或资源。</td> 
  </tr> 
 </tbody> 
</table>



#### 创建记录

此操作模块可创建文件夹或资产评论。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">对象类型</td> 
   <td> <p>选择想要创建文件夹还是要在资源上创建评论。</p> 
    <ul> 
     <li> <p>文件夹</p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p>名称</p> <p>输入文件夹的名称。 此名称将显示在文件路径中，因此不得包含空格或其他字符。 </p> </li> 
       <li> <p>标题</p> <p>输入文件夹的标题，该标题可以显示而不是名称。</p> </li> 
      </ul> </li> 
     <li> <p>资产注释</p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p>资源选择</p> <p>选择或映射您要为其添加评论的资产ID。</p> </li> 
       <li> <p>评论</p> <p>输入注释的文本。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 删除文件夹、资源或演绎版

此操作模块可删除文件夹、资源或演绎版。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择您要删除文件夹、资源还是演绎版。</p> 
    <ul> 
     <li> <p>文件夹</p> <p>通过选择路径中的文件夹来选择要删除的文件夹。</p> </li> 
     <li> <p>资产</p> <p>选择资源的方法是选择其路径中的文件夹，然后选择要删除的资源。</p> </li> 
     <li> <p>节目</p> <p>通过选择格式副本路径中的文件夹来选择格式副本。</p> <p>输入或映射演绎版的名称。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取文件夹列表

此操作模块检索现有文件夹及其子实体（文件夹或资产）的表示形式。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹</td> 
   <td>选择或映射要检索的文件夹。 要将子文件夹添加到路径中，请单击加号图标并选择子文件夹。</td> 
  </tr> 
 </tbody> 
</table>

#### 进行自定义API调用

此操作模块对Adobe Experience Manager Assets API进行自定义API调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL</p> </td> 
   <td> <p>输入相对于Adobe Experience Manager基本URL的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>方法</p> </td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">标头</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion会自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">查询字符串</td> 
   <td> <p>输入请求查询字符串。 对于每个键/值对，单击<b>添加项</b>并输入键和值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">正文</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注意：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 移动文件夹或资源

此操作模块会将给定路径下的资产或文件夹移动到新位置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择您要移动文件夹还是资产。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹/资产</td> 
   <td>选择或映射要移动的文件夹或资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">目标路径</td> 
   <td>选择路径，或将路径映射到要将文件夹或资源移动到的位置。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">已移动文件夹/资产的名称</td> 
   <td>为移动的文件夹或资源输入新名称。 Adobe Experience Manager Assets中显示的文件夹名称与原始名称相同。 此处输入的名称将显示在移动的文件夹或资产的URL中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">覆盖</td> 
   <td>启用此选项以覆盖目标位置中与要移动的文件夹或资源同名的任意文件夹或资源。</td> 
  </tr> 
 </tbody> 
</table>

#### 更新记录

此操作模块更新现有记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择您要删除资源元数据还是资源演绎版。</p> 
    <ul> 
     <li> <p>资源元数据</p> 
      <ul> 
       <li> <p>选择要为其更新元数据的资源。</p> </li> 
       <li> <p>输入资源的新标题。</p> </li> 
      </ul> </li> 
     <li> <p>资源演绎版</p> 
      <ul> 
       <li> <p>选择要为其更新演绎版的资源。</p> </li> 
       <li> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Assets（创作API）

* [删除资源](#delete-asset)
* [获取作业状态](#get-job-status)

#### 删除资源

此操作模块通过单个资产的ID来删除该资产。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资产ID</td> 
   <td> <p>输入或映射要删除的资产ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">强制</td> 
   <td>启用此选项可强制删除资产，即使该资产被引用也是如此。</td> 
  </tr> 
 </tbody> 
</table>

#### 获取作业状态

此操作模块获取异步作业的当前状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">作业ID</td> 
   <td> <p>输入或映射要获取其状态的作业的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 事件（创作API）

#### 观看活动

此触发器模块在AEM Assets中发生事件时启动场景。

该模块包含一个字段： Webhook。 选择要用于这些事件的现有webhook，或创建一个新事件。

要创建新的webhook，请执行以下操作：

1. 单击Webhook字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">Webhook名称</td>
        <td>输入此webhook的名称。</td>
       </tr>
       <tr>
         <td role="rowheader">连接</td>
        <td>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</td>
       </tr>
     </tbody>
   </table>

1. 单击保存以保存webhook并返回到模块。


### 元数据（创作API）

* [获取资源元数据](#get-asset-metadata)
* [更新资源元数据](#update-asset-metadata)

#### 获取资源元数据

此操作模块可检索有关指定资源的元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资产ID</td> 
   <td> <p>输入或映射要为其获取元数据的资源的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 更新资源元数据

此操作模块更新指定资源的元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资产ID</td> 
   <td> <p>输入或映射要为其更新元数据的资源的ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">更新</td> 
   <td> <p>对于每个要更新的元数据项，单击<b>添加项</b>并选择操作。 “添加项”框中的其他字段取决于所选操作。</p> </td> 
  </tr> 
 </tbody> 
</table>


### 导入（创作API）

* [获取导入作业结果](#get-import-job-results)
* [获取导入作业状态](#get-import-job-status)
* [从URL上传资产](#upload-an-asset-from-a-url)

#### 获取导入作业结果

此操作模块检索指定导入作业的结果。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">导入作业ID</td> 
   <td> <p>输入或映射要为其检索结果的作业的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取导入作业状态

此操作模块可检索指定导入作业的状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">导入作业ID</td> 
   <td> <p>输入或映射要检索其状态的作业的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 从URL上传资产

此操作模块通过从指定的URL导入文件来上传新资源。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">标题</td> 
   <td> <p>输入或映射资源的标题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">描述</td> 
   <td> <p>输入或映射资源的描述。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">主题</td> 
   <td> <p>输入或映射资源的主题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">创建者</td> 
   <td> <p>输入或映射资源的创建者。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">过期日期</td> 
   <td> <p>输入或映射资源的体验日期。</p><p>有关支持的日期和时间格式的列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">自定义元数据</td> 
   <td> <p>对于要添加到资源的每个自定义元数据项，单击<b>添加项</b>并输入元数据的名称和值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹路径或标识</td> 
   <td> <p>选择是否要通过目标文件夹的路径或ID来指定目标文件夹，然后选择路径或输入ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">要导入的文件</td> 
   <td> <p>对于每个要导入的文件，单击<b>添加项目&lt;/&gt;并填写文件的详细信息。<code>Title</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"></td> 
   <td> <p></p> </td> 
  </tr> 
 </tbody> 
</table>

### 关系（创作API）

* [创建资产关系](#create-asset-relations)
* [删除资源关系](#create-asset-relations)
* [获取资源关系类型](#get-asset-relation-types)
* [获取资产关系](#get-asset-relations)

#### 创建资产关系

此操作模块为选定资产创建新资产关系。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资产ID</td> 
   <td> <p>输入或映射要将其他资源与之关联的ID资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">相关资产</td> 
   <td> <p>对于要与所选资源关联的每个资源，单击<b>添加项</b>，然后输入或映射资源的ID和关系类型。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 删除资源关系

此操作模块删除资产的资产关系。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资产ID</td> 
   <td> <p>输入或映射要从其中删除关系的ID资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">相关资产</td> 
   <td> <p>输入或映射要删除的关系类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">提供要删除的相关资产的特定ID</td> 
   <td> <p>如果要删除一个特定关系，请选中此框。 如果未选中此框，则所选类型的所有关系都将被删除。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">相关资产ID</td> 
   <td> <p>如果要删除特定关系，请输入或映射要删除的关系的ID。</p> </td> 
  </tr> 
 </tbody> 
</table>


#### 获取资源关系类型

此模块列出指定资源存在的资源关系类型。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资产ID</td> 
   <td> <p>输入或映射要为其列出关系类型的ID资源。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取资产关系

此模块列出指定资产的资产关系。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资产ID</td> 
   <td> <p>输入或映射要为其列出关系的ID资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">关系类型</td> 
   <td> <p>输入或映射要为其列出关系的关系类型列表（以逗号分隔）。</p> </td> 
  </tr> 
 </tbody> 
</table>



### 文件夹（文件夹API）

* [创建文件夹](#create-folders)
* [按ID删除文件夹](#delete-a-folder-by-id)
* [按路径删除文件夹](#delete-folders-by-path)
* [获取文件夹作业结果](#get-folders-job-results)
* [获取文件夹作业状态](#get-folders-job-status)
* [列出文件夹](#list-folders)

#### 创建文件夹

此操作模块在Adobe Experience Manager Assets中创建新文件夹。



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">要创建的文件夹</td> 
   <td> <p>对于要创建的每个文件夹，单击<b>添加项</b>并输入以下信息：</p>
   <ul>
   <li><b>新建文件夹位置</b><p>选择要创建新文件夹的位置路径。</p></li>
       <li> <b>名称</b> <p>输入文件夹的名称。 此名称将显示在文件路径中，因此不得包含空格或其他字符。 </p> </li> 
       <li> <b>标题</b> <p>输入文件夹的标题，该标题可以显示而不是名称。</p> </li> 
   </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 按ID删除文件夹

此操作模块会删除具有指定ID的Adobe Experience Manager Assets文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹 ID</td> 
   <td> 输入或映射要删除的文件夹的ID。</td>
  </tr> 
 <tr> 
   <td role="rowheader">删除子文件夹</td> 
   <td> 启用此选项可删除文件夹及其所有子文件夹。</td>
  </tr> 
 <tr> 
   <td role="rowheader">强制</td> 
   <td> 启用此选项可强制删除文件夹，即使引用了该文件夹也是如此。</td>
  </tr> 
 </tbody> 
</table>

#### 按路径删除文件夹

此操作模块会删除位于指定路径的Adobe Experience Manager Assets文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹路径</td> 
   <td>对于每个要删除的文件夹，单击<b>添加项</b>并选择该文件夹的路径。</td>
  </tr> 
 <tr> 
   <td role="rowheader">删除子文件夹</td> 
   <td> 启用此选项可删除文件夹及其所有子文件夹。</td>
  </tr> 
 <tr> 
   <td role="rowheader">强制</td> 
   <td> 启用此选项可强制删除资产，即使该资产被引用也是如此。</td>
  </tr> 
 </tbody> 
</table>

#### 获取文件夹作业结果

此模块检索Adobe Experience Manager Assets文件夹API创建的异步作业的结果。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">作业ID</td> 
   <td> 输入或映射要为其检索结果的作业的ID。</td>
  </tr> 
 </tbody> 
</table>

#### 获取文件夹作业状态

此模块可检索由Adobe Experience Manager Assets文件夹API创建的异步作业的状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">作业ID</td> 
   <td> 输入或映射要检索其状态的作业的ID。</td>
  </tr> 
 </tbody> 
</table>


#### 列出文件夹

此模块列出指定文件夹的子文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>有关将Adobe Experience Manager Assets帐户连接到Workfront Fusion的说明，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将Adobe Experience Manager Assets连接到Workfront Fusion</a>。</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">文件夹路径或标识</td> 
   <td> <p>选择是否要通过目标文件夹的路径或ID来指定目标文件夹，然后选择路径或输入ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--
i! I added a lot of modules to the AEM Assets connector and we need new documentation for them. The connector is available in the QA environment. Heres the added modules and a brief description of them, more info about them can be found in the Assets Author Api docs and the Folders Api docs. Im not fully confident that i kept all the best practices for naming things :sweat_smile:, i hope you can take a look at that as well. Let me know if theres anything i can tell about the modules and thanks again in advance!
Author API
Assets
Delete Asset
Deletes an asset when provided an Asset ID, There is a force parameter that when toggled will delete the folder regardless if it's referenced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get assets job status
Given an assets job ID will return the state that the job is currently in (PROCESSING, COMPLETED, etc.)
Events
AEM Assets events
The costumer can create a web hook in this module and register it in the Adobe admin console
Metadata
Get asset metadata
Given asset ID returns assets metadata.
Update asset metadata
Given asset ID, there are 6 patch operations that can be done with the metadata. The operations are visible in the module as well as the documentation.
Import
Get import job results
Given Job ID returns it's result.
Get import job status
Given Job ID returns its status.
Upload an asset from url
Takes global metadata which applies to all the assets and local ones which apply individually.In both it is also possible to specify custom metadata.
Also takes the folder path or folder ID to place the assets there and url-s of the assets.
Relations
Create asset relation
Given asset ID and a list of related asset ID as well as the relation types creates those relationships.
Delete asset relations
Given asset ID and relation type deletes all relations of that type. Can also specify a related asset to target only that.
 there is a checkbox that is checked by default and when unchecked reveals a field where the user can specify the related user ID.
Get asset relation types
Given asset ID returns all the relation types that the asset has.
Get asset relations
Given asset ID returns all relations. Can also specify a specific type of relation.
Folders API
Create folders
Given a list of folders with their path, name, title, creates them.
Delete a folder by ID
Given Folder ID deletes the folder. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Delete folders by path
Given a list of paths, deletes everything in them. There is also a way to specify if it should delete folders recursively and if it should be forced.
Return either nothing if the deletion takes less than a few seconds or a job ID which can be used in another module to track the job of deleting the folder.
Get folders job results
Given job ID returns its result.
Get folders job status
Given job ID returns its status.
List Folders
List folders under the given folder. In the module you can choose the root folder either by ID or by Path.
-->

