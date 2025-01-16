---
title: FTP模块
description: FTP模块允许您监视选定文件夹中的文件更改，将新文件上传到所需文件夹，以及修改或删除文件夹中已存在的现有文件。
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%

---

# FTP模块

FTP模块允许您监视选定文件夹中的文件更改，将新文件上传到所需文件夹，以及修改或删除文件夹中已存在的现有文件。

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

若要将[Fusion应用程序]与[!DNL Workfront Fusion]一起使用，您必须具有FTP帐户。

## 在FTP模块中创建连接 {#create-a-connection}

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection name]</td> 
   <td> <p> 输入FTP连接的名称。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Host] </td> 
   <td> <p>输入FTP服务器主机名。 E.g. <code>myftp123.server.com</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Port] </td> 
   <td> <p>输入FTP服务器端口号。 E.g. <code>21</code></p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL User name] </td> 
   <td> <p>输入您的FTP帐户用户名。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Password] </td> 
   <td> <p>输入您的FTP帐户密码。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>使用安全连接(TLS)</p> </td> 
   <td> <p>选择是否要使用安全连接。</p> <p style="font-weight: bold;">[!UICONTROL No]</p> <p>连接不安全。</p> <p style="font-weight: bold;">[!UICONTROL Explicit encryption or Implicit encryption]</p> <p>使用SSL保护连接。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Reject unauthorized certificates]</p> </td> 
   <td> <p>启用此选项以验证FTP服务器证书。 如果验证失败，将不会创建连接。 要通过验证，证书必须满足以下条件之一：</p> 
    <ul> 
     <li>由根<a href="https://en.wikipedia.org/wiki/Certificate_authority">证书颁发机构</a>签名</li> 
     <li>由中间证书颁发机构签名（如<a href="https://knowledge.digicert.com/solution/SO16297.html">证书链的工作方式</a>了解进一步说明）。 在这种情况下，所有中间证书都应安装在FTP服务器上。</li> 
     <li>是[!UICONTROL Self-signed certificate]字段中提供的自签名证书（见下文）</li> </ul>

如果禁用此选项，则不会验证FTP服务器证书。 我们强烈建议不要禁用此选项，因为它会导致连接不安全，并带来严重的安全风险。</td>
</tr> 
  <tr> 
   <td> <p>[!UICONTROL Self-signed certificate]</p> </td> 
   <td> <p>单击<b>[!UICONTROL Extract]</b>按钮以打开上载对话框。</p> <p>上载证书以将TLS与您的自签名证书一起使用。 [!DNL Workfront Fusion]不保留或存储您提供的任何数据，如文件和密码。 文件和密码仅用于提取证书。</p> </td> 
  </tr> 
 </tbody> 
</table>

## FTP模块及其字段

* [触发器](#triggers)
* [操作](#actions)

### 触发器

#### [!UICONTROL Watch files]

[!UICONTROL Watch files]是FTP的唯一触发器模块。 它监视选定文件夹的文件内容。 将新文件插入指定的文件夹时，将执行触发器。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关建立与FTP帐户的连接的说明，请参阅本文中FTP模块</a>的<a href="#create-a-connection" class="MCXref xref">[!UICONTROL Create a connection]。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Folder]</p> </td> 
   <td> <p>选择要监视的文件夹。</p> <p><b>注意：</b>每个方案只允许一个文件夹。 子文件夹将被忽略。</p> <p><b>提示：</b>若要跟踪多个文件夹，请为每个文件夹创建独立的方案。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files] </td> 
   <td> <p>设置[!DNL Workfront Fusion]在一个周期内可处理的最大结果数。 如果该值设置得过高，则可能会中断与给定第三方服务的连接（超时）。 [!DNL Workfront Fusion]对此没有影响。 我们建议您设置较低的值，并为最大循环数定义较高的值，或者更频繁地运行方案。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL Change permissions]](#change-permissions)
* [[!UICONTROL Create a folder]](#create-a-folder)
* [[!UICONTROL Delete a file]](#delete-a-file)
* [[!UICONTROL Delete a folder]](#delete-a-folder)
* [[!UICONTROL Get a file]](#get-a-file)
* [[!UICONTROL List of files in a folder]](#list-of-files-in-a-folder)
* [[!UICONTROL Move a file or folder]](#move-a-file-or-folder)
* [[!UICONTROL Upload]文件](#upload-a-file)

#### [!UICONTROL Change permissions]

此操作模块更改文件或文件夹的权限设置。

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">有关建立与FTP帐户的连接的说明，请参阅本文中FTP模块</a>的<a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection]。</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!UICONTROL Change permission settings of]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">
               <p>选择是否要更改文件或文件夹的设置。</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL File path]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">输入或映射文件夹或文件的文件路径。</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-MediumGray" role="rowheader">[!UICONTROL Permissions]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-MediumGray">
               <p>设置所需的文件或文件夹权限。 使用chmod参数。 例如： <code>777 </code>或<code>-rwxrwxrwx</code>。</p>
               <p>权限必须符合模式<code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code>。</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Create a folder]

此操作模块将创建新文件夹。

<table style="width: 100%;" class="TableStyle-TableStyle-List-options-in-steps" cellspacing="0">
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1" />
   <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2" />
   <tbody>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-LightGray" role="rowheader">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">有关建立与FTP帐户的连接的说明，请参阅本文中FTP模块</a>的<a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection]。</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-MediumGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyE-Column1-MediumGray" role="rowheader">[!UICONTROL Folder path]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-MediumGray">输入或映射文件路径到新文件夹。</td>
         </tr>
         <tr class="TableStyle-TableStyle-List-options-in-steps-Body-LightGray">
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyB-Column1-LightGray" role="rowheader">[!UICONTROL New folder name]</td>
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyA-Column2-LightGray">
               <p>输入或映射新文件夹的名称。</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Delete a file]

从指定的文件夹中删除文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
            <td class="TableStyle-TableStyle-List-options-in-steps-BodyD-Column2-LightGray">有关建立与FTP帐户的连接的说明，请参阅本文中FTP模块</a>的<a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection]。</td>
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>选择要从中删除文件的FTP文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File name]</td> 
   <td> <p> 输入文件名，包括文件扩展名。 示例： <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete a folder]

此操作模块将永久删除指定的文件夹。

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">有关建立与FTP帐户的连接的说明，请参阅本文中FTP模块</a>的<a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection]。</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-MediumGray" style="font-weight: bold;">[!UICONTROL Folder]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-MediumGray">
               <p>选择要从中删除文件的FTP文件夹。</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL Get a file]

从FTP服务器检索可进一步处理的文件，例如上载到[!DNL Dropbox]。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关建立与FTP帐户的连接的说明，请参阅本文中的<a href="#creating-the-ftp-connection" class="MCXref xref">创建FTP连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL File path]</td> 
   <td> <p> 输入要获取的文件路径。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL List of files in a folder]

检索文件和/或文件夹信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>有关建立与FTP帐户的连接的说明，请参阅本文中的<a href="#creating-the-ftp-connection" class="MCXref xref">创建FTP连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>选择要搜索的FTP文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Show] </td> 
   <td> <p>选择是要检索有关文件或文件夹的信息，还是同时检索两者。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search] </td> 
   <td> <p>输入搜索词。 如果未输入搜索词，则会检索指定文件夹中的所有文件和文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of returned files]</td> 
   <td> <p> 设置此模块检索到的最大文件数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move a file or folder]

此操作模块会将文件或文件夹移动到其他位置。

<table style="width: 100%;" class="TableStyle-TableStyle-HeaderRow" cellspacing="15">
   <col style="width: 301px;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <col style="width: 50%;" class="TableStyle-TableStyle-HeaderRow-Column-Column1" />
   <tbody>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-LightGray" style="font-weight: bold;">[!UICONTROL Connection]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-LightGray">有关建立与FTP帐户的连接的说明，请参阅本文中FTP模块</a>的<a href="#Create" class="MCXref xref" >[!UICONTROL Create a connection]。</td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-MediumGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyE-Column1-MediumGray" style="font-weight: bold;">[!UICONTROL Old file path]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyD-Column1-MediumGray">
               <p>输入要从中移动文件的路径。 示例： <code>/folder1/document.txt</code>。</p>
            </td>
         </tr>
         <tr class="TableStyle-TableStyle-HeaderRow-Body-LightGray">
            <td class="TableStyle-TableStyle-HeaderRow-BodyB-Column1-LightGray" style="font-weight: bold;">[!UICONTROL New file path]</td>
            <td class="TableStyle-TableStyle-HeaderRow-BodyA-Column1-LightGray">
               <p>输入要移动文件的路径。 示例： <code>/folder2/document.txt</code>。</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL Upload a file]

将文件上传到FTP服务器。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td>有关建立与FTP帐户的连接的说明，请参阅本文中的<a href="#creating-the-ftp-connection" class="MCXref xref">创建FTP连接</a>。</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>选择要将文件上传到的FTP文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file] </td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Append to an already existing file]</td> 
   <td> <p>如果启用了此选项，并且FTP服务器上已存在文件，则文件的内容将附加到现有文件。 如果未启用此选项，则将覆盖文件的内容。</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Create folders if don't exist] </td> 
   <td> <p>如果启用了此选项，并且FTP服务器上不存在您输入到“文件夹”字段的文件夹，则模块将创建该文件夹</p> </td> 
  </tr> 
 </tbody> 
</table>

## 故障排除 {#troubleshooting}

如果在创建连接期间或模块操作期间FTP应用程序遇到问题，请尝试使用某个常用FTP客户端，并尝试执行相同的操作（例如，创建连接或在文件夹中列出文件）。 与FTP客户端一起使用。 如果您也遇到与FTP客户端相同的问题，原因可能是FTP服务器的配置错误。
