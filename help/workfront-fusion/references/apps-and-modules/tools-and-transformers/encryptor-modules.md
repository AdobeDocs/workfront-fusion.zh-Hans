---
title: 加密程序
description: Adobe Workfront Fusion Encryptor模块允许您加密任何文本数据。 它们当前支持通过AES256和PGP (OpenPGP)进行消息加密。
author: Becky
feature: Workfront Fusion
exl-id: 4b119efe-6762-445e-bbc7-c59437fd5060
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---

# 加密程序

[!DNL Adobe Workfront Fusion] [!UICONTROL Encryptor]模块允许您加密任何文本数据。 它们当前支持通过AES256和PGP ([!UICONTROL OpenPGP])进行消息加密。

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
   <p>旧版许可证要求：[!UICONTROL [!DNL Workfront Fusion]用于工作自动化和集成]，[!UICONTROL [!DNL Workfront Fusion]用于工作自动化]</p>
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

## 使用PGP进行消息加密和解密

当通过PGP进行加密和解密时，必须使用密钥链并创建私钥或公钥（或两者）。

有关公钥和私钥的更多信息，请参阅[Adobe Workfront Fusion术语表](/help/workfront-fusion/get-started-with-fusion/understand-fusion/fusion-glossary.md)。<!--For more information on keychains, see [Keys in [!DNL Adobe Workfront Fusion]]().-->

## [!UICONTROL Encryptor]模块及其字段

配置[!UICONTROL Encryptor]模块时，将显示以下字段。 模块中的粗体标题表示必填字段。

### 加密PGP消息

此模块允许您使用公钥和私钥加密消息。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>输入发件人的私钥。 这可以对发件人的身份进行身份验证。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>输入收件人的公钥。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>输入要加密的消息。</td>
    </tr>

### 解密PGP消息

此模块允许您使用公钥和私钥解密消息。

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Private key]</td>
        <td>输入收件人的私钥。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Public key]</td>
        <td>输入收件人的公钥。 这可以对发件人的身份进行身份验证。</td>
    </tr>
    <tr>
        <td>[!UICONTROL Message]</td>
        <td>映射要解密的消息。</td>
    </tr>
</table>
