---
title: Adobe Experience Manager Assets 模块
description: 借助 Adobe Workfront Fusion 的 Adobe Experience Manager Assets 连接器，您可以创建、上传和更新资源，并复制或移动文件夹和资源。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 361e6c9c-1497-4f47-85bb-503619744968
source-git-commit: d4bdc4005a3b7b22d64adc8ca1d20bcf534ddfd1
workflow-type: ht
source-wordcount: '3734'
ht-degree: 100%

---

# Adobe Experience Manager Assets 模块

借助 Adobe Workfront Fusion 的 Adobe Experience Manager Assets 连接器，您可以创建、上传和更新资源，并复制或移动文件夹和资源。

有关 Adobe Experience Manager Assets 连接器的视频介绍，请参阅：

* [Adobe Experience Manager Assets](https://video.tv.adobe.com/v/3427034/){target=_blank}

## 访问权限要求

+++ 展开可查看本文所述功能的访问权限要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront 包</td> 
   <td> <p>任意 Adobe Workfront Workflow 包以及任意 Adobe Workfront 自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime 和 Select 包，且需额外购买 Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront 许可证</td> 
   <td> <p>标准</p><p>工作版或更高版本</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion 许可证</td> 
   <td>
   <p>基于操作：不需要 Workfront Fusion 许可证</p>
   <p>基于连接器（旧版）：Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果您的组织使用的 Workfront Select 或 Prime 包不包含 Workfront 自动化和集成，则必须单独购买 Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细说明，请参阅[文档中的访问权限要求](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)。

有关 Adobe Workfront Fusion 许可证的详细信息，请参阅 [Adobe Workfront Fusion 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

* 要使用这些模块，您必须拥有 Adobe Experience Manager Assets 帐户。
* 您必须在 Adobe Developer Console 中设置服务器到服务器流程。

  有关在 Adobe Developer Console 中设置服务器到服务器流程的说明，请参阅[为服务器端 API 生成访问令牌](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow)。
* 您的 Adobe Experience Manager 技术帐户必须具备写入权限。

  有关为 Adobe Experience Manager 技术帐户添加写入权限的说明，请参阅 Adobe Experience Manager 文档中的[服务凭据](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials)。

## Adobe Experience Manager Assets API 信息

Adobe Experience Manager Assets 连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.8.61</td> 
  </tr>
 </tbody> 
 </table>

## 将 Adobe Experience Manager Assets 连接到 Workfront Fusion {#connect-adobe-experience-manager-assets-to-workfront-fusion}

要为 Adobe Experience Manager Assets 模块创建连接：

1. 点击“连接”框旁的“添加”。

2. 选择您要创建的连接类型：

   * **AEM Assets as a Cloud Service**

     此配置需要来自 Adobe Admin Console 的信息。

   * **AEM Assets Basic (Adobe Managed Services)**

     此配置需要用户名和密码。

3. 根据所创建的连接类型填写相应字段。

   如需配置 AEM Assets as a Cloud Service，请参阅[配置 AEM Assets as a Cloud Service 的连接](#configure-the-connection-for-aem-assets-as-a-cloud-service)。

   对于 AEM Assets Basic (Adobe Managed Services)，请参阅[配置 AEM Assets Basic 的连接](#configure-the-connection-for-aemassets-basic-adobe-managed-services)。

4. 点击&#x200B;**继续**&#x200B;保存连接并返回模块。


### 配置 AEM Assets as a Cloud Service 的连接

>[!NOTE]
>
>* 这些字段所需的信息是在 Adobe Developer Console 设置服务器到服务器流程时生成的。您可以在该设置流程生成的服务凭据 JSON 文件中找到这些值。
>
>   有关在 Adobe Developer Console 上设置服务器到服务器流程的说明，请参阅[为服务器端 API 生成访问令牌](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/implementing/developing/generating-access-tokens-for-server-side-apis.html#the-server-to-server-flow)。
>
>* 您的 Adobe Experience Manager 技术帐户必须具备写入权限。
>
>   有关为 Adobe Experience Manager 技术帐户添加写入权限的说明，请参阅 Adobe Experience Manager 文档中的[服务凭据](https://experienceleague.adobe.com/zh-hans/docs/experience-manager-learn/getting-started-with-aem-headless/authentication/service-credentials)。


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
                  <td role="rowheader">实例 URL（末尾不带斜杠）</td>
                  <td>输入您的 Adobe Experience Manager 实例的 URL。请勿在 URL 末尾添加斜杠 <code>/</code>。</td>
              </tr>
              <tr>
                  <td role="rowheader">帐户详细信息填写选项</td>
                  <td>选择是要提供描述帐户详细信息的 JSON，还是要手动输入详细信息。</td>
              </tr>
              <tr>
                  <td role="rowheader">JSON 格式的技术帐户详细信息</td>
                  <td>如果提供 JSON，请输入或粘贴用于描述帐户详细信息的 JSON 内容。</td>
              </tr>
              <tr>
                  <td role="rowheader">客户端 ID</td>
                  <td>如果手动输入，请填写在服务器到服务器设置中生成的客户端 ID。</td>
              </tr>
              <tr>
                  <td role="rowheader">客户端密钥</td>
                  <td>如果手动输入，请填写在服务器到服务器设置中生成的客户端密钥。</td>
              </tr>
              <tr>
                  <td role="rowheader">技术帐户 ID</td>
                  <td>如果手动输入，请填写技术帐户的 ID。该值对应于客户端凭据 JSON 文件中的“id”字段。</td>
              </tr>
              <tr>
                  <td role="rowheader">组织 ID</td>
                  <td class="">如果手动输入，请填写您的组织 ID。该值对应于客户端凭据 JSON 文件中的“org”字段。</td>
              </tr>
              <tr>
                  <td role="rowheader">Meta 范围</td>
                  <td>填写在服务器到服务器设置中生成的 Meta 范围。</td>
              </tr>
              <tr>
                  <td role="rowheader">私钥</td>
                  <td>填写在服务器到服务器设置中生成的私钥。如需提取私钥，请点击“提取”，然后输入要提取的文件及其密码。</td>
              </tr>
              <tr>
                  <td role="rowheader">身份验证 URL</td>
                  <td>输入此帐户的身份验证 URL。</td>
              </tr>
          </tbody>
      </table>


### 配置 AEM Assets Basic (Adobe Managed Services) 的连接

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
                <td role="rowheader">实例 URL（末尾不带斜杠）</td>
                <td>输入您的 Adobe Experience Manager 实例的 URL。请勿在 URL 末尾添加斜杠 <code>/</code>。</td>
            </tr>
            <tr>
                <td role="rowheader">用户名</td>
                <td>输入此连接所使用的 AEM Assets 帐户用户名。</td>
            </tr>
            <tr>
                <td role="rowheader">密码</td>
                <td>输入此连接所使用的 AEM Assets 帐户密码。</td>
            </tr>
        </tbody>
    </table>


## Adobe Experience Manager Assets 模块及其字段

在配置 Adobe Experience Manager Assets 模块时，Workfront Fusion 会显示以下字段。除这些字段外，根据您在应用程序或服务中的访问权限，系统可能还会显示其他 Adobe Experience Manager Assets 字段。模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [文件操作](#files-operations)
* [其他](#other)
* [资源（创作 API）](#assets-author-api)
* [事件（创作 API）](#events-author-api)
* [元数据（创作 API）](#metadata-author-api)
* [导入（创作 API）](#import-author-api)
* [关联（创作 API）](#relations-author-api)
* [文件夹（文件夹 API）](#folders-folders-api)

### 文件操作

* [完成上传](#complete-upload)
* [获取预签名存储](#get-presigned-storage)
* [启动上传](#initiate-upload)
* [上传资源](#upload-an-asset)

#### 完成上传

此操作模块用于在文件的所有部分上传完成后，结束已启动的上传流程。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件名</td> 
   <td> <p>输入或映射上传文件的名称。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">上传令牌</td> 
   <td>输入或映射启动上传时提供的二进制文件上传令牌。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">MIME 类型</td> 
   <td>输入或映射已完成文件的 MIME 类型。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">完成 URI</td> 
   <td>输入或映射该文件的完整 URI。</td> 
  </tr> 
 </tbody> 
</table>


#### 获取预签名存储

此操作模块会创建一个临时预签名 URL，用于在无需直接凭据的情况下，从 AEM 安全上传或下载文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">查找类型</td> 
   <td> <p>选择是否按资源路径或 ID 进行查找。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资源</td> 
   <td>选择资源的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">UDID</td> 
   <td>输入或映射该资源的 UDID。</td> 
  </tr> 
 </tbody> 
</table>

#### 启动上传

此操作模块会启动上传流程。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">目标</td> 
   <td> <p>选择要上传文件的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件名</td> 
   <td> <p>输入或映射上传文件的名称</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">最大文件大小</td> 
   <td>输入或映射上传文件的字节大小。</td> 
  </tr> 
 </tbody> 
</table>


#### 上传资源

此操作模块会将资源上传到您的 Adobe Experience Manager Assets 帐户。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">目标</td> 
   <td> <p>选择要上传资源的文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">源文件</td> 
   <td>输入或映射源文件的名称和数据。</td> 
  </tr> 
 </tbody> 
</table>

### 其他


* [复制文件夹或资源](#copy-a-folder-or-asset)
* [创建记录](#create-a-record)
* [删除文件夹、资源或演绎版](#delete-a-folder-asset-or-rendition)
* [获取文件夹列表](#get-a-folder-listing)
* [发起自定义 API 调用](#make-a-custom-api-call)
* [移动文件夹或资源](#move-a-folder-or-asset)
* [更新记录](#update-a-record)



#### 复制文件夹或资源

此操作模块会将文件夹或资源复制到您的 Adobe Experience Manager Assets 帐户中的其他位置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择要复制文件夹还是资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹 / 资源</td> 
   <td>选择或映射要复制的文件夹或资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">目标路径</td> 
   <td>选择或映射新文件夹或资源的位置路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">已复制文件夹／资源的名称</td> 
   <td>为新文件夹或资源输入名称。在 Adobe Experience Manager Assets 中显示的文件夹名称与原始名称相同。此处输入的名称将出现在新文件夹或资源的 URL 中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">复制子项</td> 
   <td>如果复制文件夹，启用此选项可同时复制文件夹中的任何子文件夹或资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">覆盖</td> 
   <td>启用此选项可覆盖目标位置中与复制文件夹或资源同名的文件夹或资源。</td> 
  </tr> 
 </tbody> 
</table>



#### 创建记录

此操作模块用于创建文件夹或资源注释。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">对象类型</td> 
   <td> <p>选择要创建文件夹还是在资源上添加注释。</p> 
    <ul> 
     <li> <p>文件夹</p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p>名称</p> <p>输入文件夹名称。该名称将显示在文件路径中，因此不能包含空格或其他字符。 </p> </li> 
       <li> <p>标题</p> <p>输入文件夹的标题，该标题可替代名称进行显示。</p> </li> 
      </ul> </li> 
     <li> <p>资源注释</p> <p>填写以下字段：</p> 
      <ul> 
       <li> <p>资源选择</p> <p>选择或映射要添加注释的资源 ID。</p> </li> 
       <li> <p>注释</p> <p>输入注释文本。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 删除文件夹、资源或演绎版

此操作模块用于删除文件夹、资源或演绎版。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择要删除文件夹、资源或演绎版。</p> 
    <ul> 
     <li> <p>文件夹</p> <p>通过选择路径中的文件夹来选择要删除的文件夹。</p> </li> 
     <li> <p>资源</p> <p>通过选择路径中的文件夹，然后选择要删除的资源。</p> </li> 
     <li> <p>演绎版</p> <p>通过选择路径中的文件夹来选择演绎版。</p> <p>输入或映射演绎版的名称。</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取文件夹列表

此操作模块会检索现有文件夹及其子实体（文件夹或资源）的结构信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹</td> 
   <td>选择或映射要检索的文件夹。要将子文件夹添加到路径中，请点击加号图标并选择该子文件夹。</td> 
  </tr> 
 </tbody> 
</table>

#### 发起自定义 API 调用

此操作模块会向 Adobe Experience Manager Assets API 发起自定义 API 调用。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>URL</p> </td> 
   <td> <p>输入相对于 Adobe Experience Manager 基础 URL 的路径。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>方法</p> </td> 
   <td> <p>选择用于配置此 API 调用的 HTTP 请求方法。有关更多信息，请参阅 <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP 请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">标头</td> 
   <td> <p>以标准 JSON 对象的形式添加请求标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p> Workfront Fusion 会自动添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">查询字符串</td> 
   <td> <p>输入请求的查询字符串。对于每个键/值对，点击<b>添加项目</b>并输入键和值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">正文</td> 
   <td> <p>以标准 JSON 对象的形式添加 API 调用的正文内容。</p> <p>注意：  <p>在 JSON 中使用 <code>if</code> 等条件语句时，需将引号置于条件语句外部。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### 移动文件夹或资源

此操作模块会将指定路径下的资源或文件夹移动到新的位置。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择要移动文件夹还是资源。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹 / 资源</td> 
   <td>选择或映射要移动的文件夹或资源。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">目标路径</td> 
   <td>选择或映射要将文件夹或资源移动到的位置路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">移动后文件夹/资源的名称</td> 
   <td>为移动后的文件夹或资源输入一个新名称。在 Adobe Experience Manager Assets 中显示的文件夹名称与原始名称相同。此处输入的名称将出现在移动后文件夹或资源的 URL 中。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">覆盖</td> 
   <td>启用此选项可覆盖目标位置中与正在移动的文件夹或资源同名的任何文件夹或资源。</td> 
  </tr> 
 </tbody> 
</table>

#### 更新记录

此操作模块会更新现有记录。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">记录类型</td> 
   <td> <p>选择要删除资源元数据还是资源演绎版。</p> 
    <ul> 
     <li> <p>资源元数据</p> 
      <ul> 
       <li> <p>选择要更新其元数据的资源。</p> </li> 
       <li> <p>输入资源的新标题。</p> </li> 
      </ul> </li> 
     <li> <p>资源演绎版</p> 
      <ul> 
       <li> <p>选择要更新其演绎版的资源。</p> </li> 
       <li> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### 资源（创作 API）

* [删除资源](#delete-asset)
* [获取作业状态](#get-job-status)

#### 删除资源

此操作模块会根据资源 ID 删除单个资源。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资源 ID</td> 
   <td> <p>输入或映射要删除的资源 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">强制删除</td> 
   <td>启用此选项可强制删除资源，即使该资源正在被引用。</td> 
  </tr> 
 </tbody> 
</table>

#### 获取作业状态

此操作模块会获取异步作业的当前状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">作业 ID</td> 
   <td> <p>输入或映射要获取其状态的作业 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 事件（创作 API）

#### 监控事件

当 AEM Assets 中发生事件时，此触发器模块会启动一个场景。

该模块包含一个字段：Webhook。选择一个现有的 Webhook 用于这些事件，或创建一个新的 Webhook。

要创建新的 Webhook：

1. 单击 Webhook 字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">Webhook 名称</td>
        <td>为此 Webhook 输入一个名称。</td>
       </tr>
       <tr>
         <td role="rowheader">连接</td>
        <td>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</td>
       </tr>
     </tbody>
   </table>

1. 点击“保存”以保存 Webhook 并返回模块。


### 元数据（创作 API）

* [获取资源元数据](#get-asset-metadata)
* [更新资源元数据](#update-asset-metadata)

#### 获取资源元数据

此操作模块会检索指定资源的元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资源 ID</td> 
   <td> <p>输入或映射要获取其元数据的资源 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 更新资源元数据

此操作模块会更新指定资源的元数据。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资源 ID</td> 
   <td> <p>输入或映射要更新其元数据的资源 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">更新</td> 
   <td> <p>对于每个要更新的元数据项，点击<b>添加项目</b>并选择操作。“添加项目”框中的其他字段取决于所选操作。</p> </td> 
  </tr> 
 </tbody> 
</table>


### 导入（创作 API）

* [获取导入作业结果](#get-import-job-results)
* [获取导入作业状态](#get-import-job-status)
* [从 URL 上传资源](#upload-an-asset-from-a-url)

#### 获取导入作业结果

此操作模块会检索指定导入作业的结果。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">导入作业 ID</td> 
   <td> <p>输入或映射要检索结果的作业 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取导入作业状态

此操作模块会检索指定导入作业的状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">导入作业 ID</td> 
   <td> <p>输入或映射要检索其状态的作业 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 从 URL 上传资源

此操作模块通过从指定 URL 导入文件来上传新资源。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
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
   <td> <p>输入或映射资源主题。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">创建者</td> 
   <td> <p>输入或映射资源的创建者。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">过期日期</td> 
   <td> <p>输入或映射资源的到期日期。</p><p>有关支持的日期和时间格式列表，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制转换</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">自定义元数据</td> 
   <td> <p>对于每个要添加到资源的自定义元数据项，点击<b>添加项目</b>并输入元数据名称和值。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹路径或 ID</td> 
   <td> <p>选择是按路径还是按 ID 指定目标文件夹，然后选择路径或输入 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">要导入的文件</td> 
   <td> <p>对于每个需要导入的文件，点击<b>添加项目&lt;/&gt;并填写该文件的详细信息。<code>Title</code> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"></td> 
   <td> <p></p> </td> 
  </tr> 
 </tbody> 
</table>

### 关联（创作 API）

* [创建资源关系](#create-asset-relations)
* [删除资源关系](#create-asset-relations)
* [获取资源关系类型](#get-asset-relation-types)
* [获取资源关系](#get-asset-relations)

#### 创建资源关系

此操作模块会为选定的资源创建新的资源关系。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资源 ID</td> 
   <td> <p>输入或映射要与其他资源建立关系的资源 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">关联资源</td> 
   <td> <p>对于每个要与选定资源建立关联的资源，点击<b>添加项目</b>，并输入或映射该资源的 ID 和关系类型。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 删除资源关系

此操作模块用于删除某个资源的关系。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资源 ID</td> 
   <td> <p>输入或映射要从中删除关系的资源 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">关联资源</td> 
   <td> <p>输入或映射要删除的关系类型。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">提供要删除的关联资源的具体 ID</td> 
   <td> <p>如果只需删除单个特定的关系，请选中此复选框。如果未选中此复选框，则会删除所选类型的所有关系。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">关联资源 ID</td> 
   <td> <p>如果要删除特定关系，请输入或映射要删除的关系的 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>


#### 获取资源关系类型

此模块会列出指定资源的关系类型。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资源 ID</td> 
   <td> <p>请输入或映射要列出关联类型的资源 ID。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### 获取资源关系

此模块会列出指定资源的资源关系。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">资源 ID</td> 
   <td> <p>请输入或映射要列出关系的资源 ID。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">关系类型</td> 
   <td> <p>输入或映射以逗号分隔的关系列表类型，用于列出相应的关系。</p> </td> 
  </tr> 
 </tbody> 
</table>



### 文件夹（文件夹 API）

* [创建文件夹](#create-folders)
* [按 ID 删除文件夹](#delete-a-folder-by-id)
* [按路径删除文件夹](#delete-folders-by-path)
* [获取文件夹作业结果](#get-folders-job-results)
* [获取文件夹作业状态](#get-folders-job-status)
* [列出文件夹](#list-folders)

#### 创建文件夹

此操作模块会在 Adobe Experience Manager Assets 中创建一个新文件夹。



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">要创建的文件夹</td> 
   <td> <p>对于每个要创建的文件夹，点击<b>添加项目</b>并输入以下信息：</p>
   <ul>
   <li><b>新文件夹位置</b><p>选择要创建新文件夹的位置路径。</p></li>
       <li> <b>名称</b> <p>输入文件夹名称。该名称将显示在文件路径中，因此不能包含空格或其他字符。 </p> </li> 
       <li> <b>标题</b> <p>输入文件夹的标题，该标题可替代名称进行显示。</p> </li> 
   </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### 按 ID 删除文件夹

此操作模块会删除具有指定 ID 的 Adobe Experience Manager Assets 文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹 ID</td> 
   <td> 输入或映射要删除的文件夹 ID。</td>
  </tr> 
 <tr> 
   <td role="rowheader">删除子文件夹</td> 
   <td> 启用此选项可删除该文件夹及其所有子文件夹。</td>
  </tr> 
 <tr> 
   <td role="rowheader">强制删除</td> 
   <td> 启用此选项可强制删除文件夹，即使该资源正在被引用。</td>
  </tr> 
 </tbody> 
</table>

#### 按路径删除文件夹

此操作模块会删除指定路径下的 Adobe Experience Manager Assets 文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">文件夹路径</td> 
   <td>对于每个要删除的文件夹，点击<b>添加项目</b>并选择该文件夹的路径。</td>
  </tr> 
 <tr> 
   <td role="rowheader">删除子文件夹</td> 
   <td> 启用此选项可删除该文件夹及其所有子文件夹。</td>
  </tr> 
 <tr> 
   <td role="rowheader">强制删除</td> 
   <td> 启用此选项可强制删除资源，即使该资源正在被引用。</td>
  </tr> 
 </tbody> 
</table>

#### 获取文件夹作业结果

此模块会检索由 Adobe Experience Manager Assets 文件夹 API 创建的异步作业结果。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">作业 ID</td> 
   <td> 输入或映射要检索结果的作业 ID。</td>
  </tr> 
 </tbody> 
</table>

#### 获取文件夹作业状态

此模块会检索由 Adobe Experience Manager Assets 文件夹 API 创建的异步作业状态。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">作业 ID</td> 
   <td> 请输入或映射要检索其状态的作业 ID。</td>
  </tr> 
 </tbody> 
</table>


#### 列出文件夹

此模块会列出指定文件夹的子文件夹。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td> <p>要了解如何将 Adobe Experience Manager Assets 帐户连接到 Workfront Fusion，请参阅本文中的<a href="#connect-adobe-experience-manager-assets-to-workfront-fusion" class="MCXref xref">将 Adobe Experience Manager Assets 连接到 Workfront Fusion</a>。</p> </td> 
   </tr> 
   <tr> 
   <td role="rowheader">文件夹路径或 ID</td> 
   <td> <p>选择是按路径还是按 ID 指定目标文件夹，然后选择路径或输入 ID。</p> </td> 
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

