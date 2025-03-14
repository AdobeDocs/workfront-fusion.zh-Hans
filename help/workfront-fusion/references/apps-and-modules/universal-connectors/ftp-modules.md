---
title: FTP模块
description: FTP模块允许您监视选定文件夹中的文件更改，将新文件上传到所需文件夹，以及修改或删除文件夹中已存在的现有文件。
author: Becky
feature: Workfront Fusion
exl-id: 1e14f778-ab8c-421f-a4b4-c57be66c7cad
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1381'
ht-degree: 0%

---

# FTP模块

FTP模块允许您监视选定文件夹中的文件更改，将新文件上传到所需文件夹，以及修改或删除文件夹中已存在的现有文件。

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

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 先决条件

要使用FTP模块，您必须拥有具有FTP服务的帐户。

## 在FTP模块中创建连接 {#create-a-connection}

1. 在任意FTP模块中，单击连接框旁边的&#x200B;**添加**。
1. 填写以下字段。

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[！UICONTROL连接名称]</td> 
      <td> <p> 输入FTP连接的名称。</p> </td> 
     </tr> 
     <tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL环境]</p> </td> 
      <td> <p>选择您使用的是生产环境还是非生产环境。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>[！UICONTROL类型]</p> </td> 
      <td> <p>选择您使用的是服务帐户还是个人帐户。</p> </td> 
     </tr> 
     <tr> 
      <td>[！UICONTROL主机] </td> 
      <td> <p>输入FTP服务器主机名。 示例： <code>myftp123.server.com</code></p> </td> 
     </tr> 
     <tr> 
      <td>[！UICONTROL端口] </td> 
      <td> <p>输入FTP服务器端口号。 示例： <code>21</code></p> </td> 
     </tr> 
     <tr> 
      <td>[！UICONTROL用户名] </td> 
      <td> <p>输入您的FTP帐户用户名。</p> </td> 
     </tr> 
     <tr> 
      <td>[！UICONTROL密码] </td> 
      <td> <p>输入您的FTP帐户密码。</p> </td> 
     </tr> 
     <tr> 
      <td> <p>使用安全连接(TLS)</p> </td> 
      <td> <p>选择是否要使用安全连接。</p> <ul><li><p><b>[！UICONTROL否]</b></p> <p>连接不安全。</p></li><li> <p><b>显式加密</b>或<b>隐式加密</b></p> <p>使用SSL保护连接。</p> </td> 
     </tr> 
    <tr> 
   <td> <p>[！UICONTROL拒绝未经授权的证书]</p> </td> 
   <td> <p>启用此选项以验证FTP服务器证书。 如果验证失败，将不会创建连接。 要通过验证，证书必须满足以下条件之一：</p> 
    <ul> 
     <li>由根证书颁发机构签名</a></li> 
     <li>由中间证书颁发机构签名。 在这种情况下，所有中间证书都应安装在FTP服务器上。</li> 
     <li>是[！UICONTROL Self-signed certificate]字段中提供的自签名证书（见下文）</li> </ul>
     <p>如果禁用此选项，则不会验证FTP服务器证书。 我们强烈建议不要禁用此选项，因为它会导致连接不安全，并带来严重的安全风险。</p></td>
    </tr> 
    <tr> 
     <td> <p>[！UICONTROL自签名证书]</p> </td> 
     <td> <p>单击<b>[！UICONTROL Extract]</b>按钮以打开上载对话框。</p> <p>上载证书以将TLS与您的自签名证书一起使用。 [!DNL Workfront Fusion]不保留或存储您提供的任何数据，如文件和密码。 文件和密码仅用于提取证书。</p> </td> 
    </tr> 
   </tbody> 
   </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

## FTP模块及其字段

* [触发器](#triggers)
* [操作](#actions)

### 触发器

#### [!UICONTROL 监视文件]

[!UICONTROL 监视文件]是FTP的唯一触发器模块。 它监视选定文件夹的文件内容。 将新文件添加到指定文件夹中时，将执行触发器。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关建立与FTP帐户的连接的说明，请参阅本文中的FTP模块</a>中的<a href="#create-a-connection" class="MCXref xref">[！UICONTROL创建连接]。</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[！UICONTROL文件夹]</p> </td> 
   <td> <p>选择要监视的文件夹。</p> <p><b>注意：</b>每个方案只允许一个文件夹。 子文件夹将被忽略。</p> <p><b>提示：</b>若要监视多个文件夹，请为每个文件夹创建单独的方案。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL返回的最大文件数] </td> 
   <td> <p>设置您希望模块在一个周期内使用的最大结果数。 如果该值设置得过高，则可能会中断FTP服务器端的连接。 [!DNL Workfront Fusion]对此没有影响。 我们建议您设置较低的值，并为最大循环数定义较高的值，或者更频繁地运行方案。</p> </td> 
  </tr> 
 </tbody> 
</table>

### 操作

* [[!UICONTROL 更改权限]](#change-permissions)
* [[!UICONTROL 创建文件夹]](#create-a-folder)
* [[!UICONTROL 删除文件]](#delete-a-file)
* [[!UICONTROL 删除文件夹]](#delete-a-folder)
* [[!UICONTROL 获取文件]](#get-a-file)
* [[!UICONTROL 文件夹中的文件列表]](#list-of-files-in-a-folder)
* [[!UICONTROL 移动文件或文件夹]](#move-a-file-or-folder)
* [[!UICONTROL 上传]文件](#upload-a-file)

#### [!UICONTROL 更改权限]

此操作模块更改文件或文件夹的权限设置。

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[！UICONTROL Connection]</td>
            <td>有关建立与FTP帐户的连接的说明，请参阅本文中的FTP模块</a>中的<a href="#Create" class="MCXref xref" >[！UICONTROL创建连接]。</td>
         </tr>
         <tr>
            <td>[！UICONTROL更改权限设置]</td>
            <td>
               <p>选择是否要更改文件或文件夹的设置。</p>
            </td>
         </tr>
         <tr>
            <td>[！UICONTROL文件路径]</td>
            <td>输入或映射文件夹或文件的文件路径。</td>
         </tr>
         <tr>
            <td>[！UICONTROL Permissions]</td>
            <td>
               <p>设置所需的文件或文件夹权限。 使用chmod参数。 例如： <code>777 </code>或<code>-rwxrwxrwx</code>。</p>
               <p>权限必须符合模式<code> /(.?([r-][w-][x-]){3})|[0-7]{3,4}/</code>。</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL 创建文件夹]

此操作模块将创建新文件夹。

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[！UICONTROL Connection]</td>
            <td>有关建立与FTP帐户的连接的说明，请参阅本文中的FTP模块</a>中的<a href="#Create" class="MCXref xref" >[！UICONTROL创建连接]。</td>
         </tr>
         <tr>
            <td>[！UICONTROL文件夹路径]</td>
            <td>输入或映射文件路径到新文件夹。</td>
         </tr>
         <tr>
            <td>[！UICONTROL新文件夹名称]</td>
            <td>
               <p>输入或映射新文件夹的名称。</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL 删除文件]

此操作模块从指定的文件夹中删除文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
            <td>有关建立与FTP帐户的连接的说明，请参阅本文中的FTP模块</a>中的<a href="#Create" class="MCXref xref" >[！UICONTROL创建连接]。</td>
  </tr> 
  <tr> 
   <td>[！UICONTROL文件夹] </td> 
   <td> <p>选择要从中删除文件的FTP文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件名]</td> 
   <td> <p> 输入文件名，包括文件扩展名。 示例： <code>[!DNL image].png</code></p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 删除文件夹]

此操作模块将永久删除指定的文件夹。

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[！UICONTROL Connection]</td>
            <td>有关建立与FTP帐户的连接的说明，请参阅本文中的FTP模块</a>中的<a href="#Create" class="MCXref xref" >[！UICONTROL创建连接]。</td>
         </tr>
         <tr>
            <td>[！UICONTROL文件夹]</td>
            <td>
               <p>选择要从中删除文件的FTP文件夹。</p>
            </td>
         </tr>
   </tbody>
</table>

#### [!UICONTROL 获取文件]

此操作模块从FTP服务器检索文件。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关建立与FTP帐户的连接的说明，请参阅本文中的<a href="#creating-the-ftp-connection" class="MCXref xref">创建FTP连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件路径]</td> 
   <td> <p> 输入要获取的文件路径。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 文件夹中的文件列表]

此操作模块可检索文件和/或文件夹信息。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td> <p>有关建立与FTP帐户的连接的说明，请参阅本文中的<a href="#creating-the-ftp-connection" class="MCXref xref">创建FTP连接</a>。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件夹] </td> 
   <td> <p>选择要搜索的FTP文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Show] </td> 
   <td> <p>选择是要检索有关文件或文件夹的信息，还是同时检索两者。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL搜索] </td> 
   <td> <p>输入搜索词。 如果未输入搜索词，则将检索指定文件夹中的所有文件或文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL返回的最大文件数]</td> 
   <td> <p>输入或映射您希望模块在一个周期内使用的最大结果数。</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 移动文件或文件夹]

此操作模块会将文件或文件夹移动到其他位置。

<table>
   <col>
   <col>
   <tbody>
         <tr>
            <td>[！UICONTROL Connection]</td>
            <td>有关建立与FTP帐户的连接的说明，请参阅本文中的FTP模块</a>中的<a href="#Create" class="MCXref xref" >[！UICONTROL创建连接]。</td>
         </tr>
         <tr>
            <td>[！UICONTROL旧文件路径]</td>
            <td>
               <p>输入要从中移动文件的路径。 示例： <code>/folder1/document.txt</code>。</p>
            </td>
         </tr>
         <tr>
            <td>[！UICONTROL新建文件路径]</td>
            <td>
               <p>输入要移动文件的路径。 示例： <code>/folder2/document.txt</code>。</p>
            </td>
         </tr>
   </tbody>
</table>


#### [!UICONTROL 上载文件]

将文件上传到FTP服务器。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[！UICONTROL Connection] </td> 
   <td>有关建立与FTP帐户的连接的说明，请参阅本文中的<a href="#creating-the-ftp-connection" class="MCXref xref">创建FTP连接</a>。</td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL文件夹] </td> 
   <td> <p>选择要将文件上传到的FTP文件夹。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL Source file] </td> 
   <td> <p>从上一个模块中选择源文件，或映射源文件的名称和数据。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL附加到现有文件]</td> 
   <td> <p>如果启用了此选项，并且FTP服务器上已存在文件，则文件的内容将附加到现有文件。 如果未启用此选项，则将覆盖文件的内容。</p> </td> 
  </tr> 
  <tr> 
   <td>[！UICONTROL创建文件夹（如果不存在）] </td> 
   <td> <p>如果启用了此选项，并且FTP服务器上不存在您输入到“文件夹”字段的文件夹，则模块将创建该文件夹</p> </td> 
  </tr> 
 </tbody> 
</table>

## 故障排除 {#troubleshooting}

如果在创建连接期间或模块操作期间FTP应用程序遇到问题，请尝试使用某个常用FTP客户端，并尝试执行相同的操作（例如，创建连接或在文件夹中列出文件）。 与FTP客户端一起使用。 如果您也遇到与FTP客户端相同的问题，原因可能是FTP服务器的配置错误。
