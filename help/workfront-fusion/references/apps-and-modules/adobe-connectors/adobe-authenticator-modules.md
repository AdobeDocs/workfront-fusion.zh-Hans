---
title: Adobe Authenticator模块
description: 借助Adobe Authenticator模块，您可以使用单个连接通过API连接到任何Adobe产品。
author: Becky
feature: Workfront Fusion
exl-id: af4da661-eeee-4033-a2bb-a2196e446a3d
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '1207'
ht-degree: 1%

---

# Adobe Authenticator模块

Adobe Authenticator模块允许您通过单个连接连接到任何Adobe API。 这允许您更轻松地连接到尚未拥有专用Fusion连接器的Adobe产品。

与HTTP模块相比，其优点是您可以创建连接，就像在专用应用程序中一样。

要查看可用Adobe API的列表，请参阅[Adobe API](https://developer.adobe.com/apis)。 您可能只能使用分配给您的API。

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何Adobe Workfront Workflow包和任何Adobe Workfront自动化和集成包</p><p>Workfront Ultimate</p><p>Workfront Prime和Select包，以及额外购买的Workfront Fusion。</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>标准</p><p>工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证</td> 
   <td>
   <p>基于操作：不需要Workfront Fusion许可证</p>
   <p>基于连接器（旧版）：用于工作自动化和集成的Workfront Fusion </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>如果贵组织具有不包含Workfront Automation and Integration的Select或Prime Workfront包，则贵组织必须购买Adobe Workfront Fusion。</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档[中的](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)访问要求。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

* 您必须具有您希望模块连接到的Adobe产品的访问权限。
* 您必须具有Adobe Developer Console的访问权限。
* 您在Adobe Developer Console上必须有一个项目，该项目包含您希望模块连接到的API。 您可以：

   * 使用API创建新项目。

     或
   * 将API添加到现有项目。

  有关在Adobe Developer Console上创建API或将API添加到项目的信息，请参阅Adobe文档中的[创建项目](https://developer.adobe.com/dep/guides/dev-console/create-project/)。

## Adobe Authenticator API信息

Adobe Authenticator连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.1.4</td> 
  </tr>
 </tbody> 
 </table>

## 创建连接

Adobe Authenticator连接可连接到Adobe Developer Console上的单个项目。 要对多个Adobe API使用相同的连接，请将API添加到同一项目，然后创建与该项目的连接。

您可以为不同的项目创建单独的连接，但无法使用连接访问不在该连接中指定的项目上的API。

>[!IMPORTANT]
>
>使用Adobe Authenticator连接器，您可以选择建立OAuth服务器到服务器连接或服务帐户(JWT)连接。 Adobe已弃用JWT凭据，这些凭据将在2025年1月1日之后停止工作。 **因此，我们强烈建议您创建OAuth连接。**
>
>有关这些类型连接的详细信息，请参阅Adobe文档中的[服务器到服务器身份验证](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/)

要创建连接，请执行以下操作：

1. 在任意Adobe Authenticator模块中，单击连接字段旁边的&#x200B;**添加**。
1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL 连接类型]</td>
        <td>
          <p>选择是要创建OAuth服务器到服务器连接，还是要创建服务帐户(JWT)连接。 我们强烈建议创建OAuth连接。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 连接名称]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端ID]</td>
        <td>输入您的[!DNL Adobe]客户端ID。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的[!DNL Adobe]客户端密钥。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 范围]</td>
        <td>如果您选择了OAuth连接，请输入此连接所需的范围。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 技术帐户ID]</td>
        <td>如果您选择了JWT连接，请输入您的[!DNL Adobe]技术帐户ID。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 组织ID]</td>
        <td>如果您选择了JWT连接，请输入您的[!DNL Adobe]组织ID。 这可以在[!DNL Adobe Developer Console]的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>如果已选择JWT连接，请输入此连接所需的元范围。 </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 私钥]</td>
        <td>
          <p>如果您选择了JWT连接，请输入在[!DNL Adobe Developer Console]中创建凭据时生成的私钥。 </p>
          <p>要提取您的私钥或证书，请执行以下操作：</p>
          <ol>
            <li value="1">
              <p>单击<b>[!UICONTROL 提取]</b>。</p>
            </li>
            <li value="2">
              <p>选择要提取的文件类型。</p>
            </li>
            <li value="3">
              <p>选择包含私钥或证书的文件。</p>
            </li>
            <li value="4">
              <p>输入文件的密码。</p>
            </li>
            <li value="5">
              <p>单击<b>[!UICONTROL 保存]</b>以提取文件并返回到连接设置。</p>
            </li>
          </ol>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 基本URL]</td>
        <td>必须添加希望此验证器允许的基本URL。 在场景的后面部分使用进行自定义API调用模块时，您将添加选定URL的相对路径。 通过在此处输入URL，您可以控制发出自定义API调用模块可以连接到的内容，从而提高安全性。<p>对于要添加到验证器的每个基本URL，单击<b>添加项</b>并输入基本URL。</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 身份验证URL]</td>
        <td>将此项留空以使用<code>https://ims-na1.adobelogin.com</code>的标准Adobe IMS身份验证URL。 如果不使用Adobe IMS进行身份验证，请输入用于身份验证的URL。</td>
      </tr>
    </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## 模块

* [进行自定义API调用](#make-a-custom-api-call)
* [进行自定义API调用（旧版）](#make-a-custom-api-call-legacy)

### 进行自定义API调用

通过此操作模块，可调用任何Adobe API。 它支持大型文件，而不是纯文本正文。

此模块已于2024年11月14日发布。 在此日期之前配置的任何Adobe Authenticator >进行自定义API调用都不会处理大型文件，现在被视为进行自定义API调用（旧版）模块。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>有关创建与Adobe Authenticator模块的连接的说明，请参阅本文中的<a href="#create-a-connection" class="MCXref xref" >创建连接</a>。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 基本URL]</p>
      </td>
      <td>
        <p>输入要连接的API点的基本URL。</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>输入相对于基本URL的路径。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 方法]</p>
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion会自动添加授权标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 查询字符串]  </td>
      <td>
        <p>输入请求查询字符串。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 主体类型]</td>
   <td> 选择此API请求的主体类型：
   <ul>
   <li>原始</li>
   <li>application/x-www-form-urlencoded</li>
   <li>多部分/表单数据</li>
   </ul>
      </td>
      </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 输出类型]  </td>
      <td>
        <p>选择您希望模块输出的数据类型。 如果不选择类型，模块将自动选择类型。</p>
      </td>
    </tr>
  </tbody>
</table>

### 进行自定义API调用（旧版）

通过此操作模块，可调用任何Adobe API。

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>有关创建与Adobe Authenticator模块的连接的说明，请参阅本文中的<a href="#create-a-connection" class="MCXref xref" >创建连接</a>。</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 基本URL]</p>
      </td>
      <td>
        <p>输入要连接的API点的基本URL。</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>输入相对于基本URL的路径。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL 方法]</p>
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override="">HTTP请求方法</a>。</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>以标准JSON对象的形式添加请求的标头。</p>
        <p>例如， <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion会自动添加授权标头。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL 查询字符串]  </td>
      <td>
        <p>输入请求查询字符串。</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
