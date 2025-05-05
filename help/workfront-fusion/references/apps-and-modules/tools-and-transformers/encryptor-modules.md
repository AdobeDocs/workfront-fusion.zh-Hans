---
title: 加密程序
description: Adobe Workfront Fusion Encryptor模块允许您加密任何文本数据。 它们当前支持通过AES256和PGP (OpenPGP)进行消息加密。
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 0%

---

# 加密程序

[!DNL Adobe Workfront Fusion] [!UICONTROL 加密程序]模块允许您加密任何文本数据。 它们当前支持通过AES256和PGP ([!UICONTROL OpenPGP])进行消息加密。

这些模块需要熟悉加密过程。

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
   <p>无Workfront Fusion许可证要求</p>
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

## 使用PGP进行消息加密和解密

当通过PGP进行加密和解密时，必须使用密钥链并创建私钥或公钥（或两者）。

有关公钥和私钥的更多信息，请参阅[Adobe Workfront Fusion术语表](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md)。

有关密钥的详细信息，请参阅[密钥](/help/workfront-fusion/references/modules/keys.md)。

## [!UICONTROL 加密程序]模块及其字段

配置[!UICONTROL 加密程序]模块时，将显示以下字段。 模块中的粗体标题表示必填字段。

### AES解密（高级）

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>选择您希望模块使用的键。 要创建密钥，请单击<b>添加</b>并输入密钥的名称、密钥和编码类型。</td>
    </tr>
    <tr>
        <td>位</td>
        <td>选择您希望模块使用128位还是256位加密。</td>
    </tr>
    <tr>
        <td>输入编码</td>
        <td>选择要使用的输入编码类型：
        <ul>
        <li>二进制</li>
        <li>以64为底</li>
        <li>十六进制</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>数据</td>
        <td>输入或映射要解密的数据。</td>
    </tr>
    <tr>
        <td>输出编码</td>
        <td>选择要使用的输出编码类型：
        <ul>
        <li>ASCII</li>
        <li>二进制</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>密码算法</td>
        <td>选择要使用的密码算法：
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>初始化矢量编码</td>
        <td>选择要使用的初始化矢量编码：
        <ul>
        <li>UTF-8</li>
        <li>二进制</li>
        <li>以64为底</li>
        <li>十六进制</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>身份验证标记编码</td>
        <td>选择要使用的身份验证标记编码：
        <ul>
        <li>UTF-8</li>
        <li>二进制</li>
        <li>以64为底</li>
        <li>十六进制</li>
        </ul>
        </td>
    </tr>
</table>

### AES解密（简单）

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>选择您希望模块使用的键。 要创建密钥，请单击<b>添加</b>并输入密钥的名称、密钥和编码类型。</td>
    </tr>
   <tr>
        <td>输入编码</td>
        <td>选择要使用的输入编码类型：
        <ul>
        <li>二进制</li>
        <li>以64为底</li>
        <li>十六进制</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>数据</td>
        <td>输入或映射要解密的数据。</td>
    </tr>
    <tr>
        <td>输出编码</td>
        <td>选择要使用的输出编码类型：
        <ul>
        <li>ASCII</li>
        <li>二进制</li>
        <li>UTF-8</li>
        </ul>
        </td>
     </tr>
    <tr>
        <td>密钥</td>
        <td>输入或映射要使用的密钥。</td>
    </tr>
</table>

### AES加密（高级）

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>选择您希望模块使用的键。 要创建密钥，请单击<b>添加</b>并输入密钥的名称、密钥和编码类型。</td>
    </tr>
    <tr>
        <td>位</td>
        <td>选择您希望模块使用128位还是256位加密。</td>
    </tr>
    <tr>
        <td>输入编码</td>
        <td>选择要使用的输入编码类型：
        <ul>
        <li>二进制</li>
        <li>ASCII</li>
        <li>十六进制</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>数据</td>
        <td>输入或映射要加密的数据。</td>
    </tr>
    <tr>
        <td>输出编码</td>
        <td>选择要使用的输出编码类型：
        <ul>
        <li>ASCII</li>
        <li>二进制</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>密码算法</td>
        <td>选择要使用的密码算法：
        <ul>
        <li>CBC</li>
        <li>GCM</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>初始化矢量编码</td>
        <td>选择要使用的身份验证标记编码：
        <ul>
        <li>UTF-8</li>
        <li>二进制</li>
        <li>以64为底</li>
        <li>十六进制</li>
        </ul>
        </td>
    </tr>
</table>

### AES加密（简单）

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Key]</td>
        <td>选择您希望模块使用的键。 要创建密钥，请单击<b>添加</b>并输入密钥的名称、密钥和编码类型。</td>
    </tr>
   <tr>
        <td>输入编码</td>
        <td>选择要使用的输入编码类型：
        <ul>
        <li>二进制</li>
        <li>ASCII</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>数据</td>
        <td>输入或映射要加密的数据。</td>
    </tr>
    <tr>
        <td>输出编码</td>
        <td>选择要使用的输出编码类型：
        <ul>
        <li>以64为底</li>
        <li>二进制</li>
        <li>十六进制</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>密钥</td>
        <td>输入或映射要使用的密钥。</td>
    </tr>
</table>


### 创建数字签名

此模块允许您使用公钥和私钥解密消息。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 私钥]</td>
        <td>选择要用于此签名的私钥。 要添加私钥，请单击<b>添加</b>并输入密钥的名称、密钥文本和密码。</td>
    </tr>
    <tr>
        <td>算法 </td>
        <td>选择您要使用RSA-SHA1还是RSA-SHA256。 </td>
    </tr>
   <tr>
        <td>输入编码</td>
        <td>选择要使用的输入编码类型：
        <ul>
        <li>ASCII</li>
        <li>二进制</li>
        <li>UTF-8</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>输出编码</td>
        <td>选择要使用的输出编码类型：
        <ul>
        <li>以64为底</li>
        <li>十六进制</li>
        </ul>
        </td>
    </tr>
    <tr>
        <td>数据</td>
        <td>输入或映射要从中创建签名的数据。</td>
    </tr>
</table>

### 解密PGP消息

此模块允许您使用公钥和私钥解密消息。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 私钥]</td>
        <td>选择要用于此邮件的收件人私钥。 要添加私钥，请单击<b>添加</b>并输入密钥的名称、密钥文本和密码。</td>
    </tr>
    <tr>
        <td>[!UICONTROL 公钥]</td>
        <td>输入发件人的公钥。 这可以对发件人的身份进行身份验证。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>映射要解密的消息。</td>
    </tr>
</table>

### 加密PGP消息

此模块允许您使用公钥和私钥加密消息。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL 私钥]</td>
        <td>输入发件人的私钥。 这可以对发件人的身份进行身份验证。</td>
    </tr>
    <tr>
        <td>[!UICONTROL 公钥]</td>
        <td>输入收件人的公钥。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>输入要加密的消息。</td>
    </tr>
    </table>
