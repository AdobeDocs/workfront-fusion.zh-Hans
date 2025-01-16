---
title: Adobe Experience Manager Forms模块
description: 使用 [!DNL Adobe Workfront Fusion], you can start a scenario based on events in your [!DNL Adobe Experience Manager Forms] 帐户的 [!DNL Adobe Experience Manager Forms] 连接器，创建、上传和更新资产，以及复制或移动文件夹和资产。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 2%

---

# [!DNL Adobe Experience Manager Forms]模块

使用[!DNL Adobe Workfront Fusion]的[!DNL Adobe Experience Manager Forms]连接器，您可以通过创建webhook来基于[!DNL Adobe Experience Manager Forms]帐户中的事件启动方案。

您可以在[!DNL Adobe Experience Manager Forms]内配置表单，以将表单提交内容发送到此webhook。

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

* 您必须拥有[!DNL Adobe Experience Manager Forms]帐户才能使用此模块。

## Adobe Experience Manager Assets API信息

Adobe Experience Manager Assets连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.2.27</td> 
  </tr>
 </tbody> 
 </table>

## 创建与Adobe Experience Manager Forms的连接

要为您的[!DNL Adobe Experience Manager Forms]模块创建连接：

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
        <td>
          <p>选择此连接是连接到生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>选择此帐户是服务帐户还是个人帐户。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance URL without a trailing slash]</td>
        <td>
          <p>输入用于访问帐户的URL，不带最后一个斜杠。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL IMS endpoint]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>输入您的[!DNL Adobe]客户端ID。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>输入您的[!DNL Adobe]客户端密钥。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Org ID]</td>
        <td>输入您的[!DNL Adobe]组织ID。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>输入您的[!DNL Adobe]技术帐户ID。 可在[!DNL Adobe Developer Console]的[!UICONTROL Credentials details]部分中找到此项。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>输入任何适当的元范围       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>输入在[!DNL Adobe Developer Console]中创建凭据时生成的私钥。 </p>
          <p>要提取您的私钥或证书，请执行以下操作：</p>
          <ol>
            <li value="1">
              <p>单击 <b>[!UICONTROL Extract]</b>。</p>
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
              <p>单击<b>[!UICONTROL Save]</b>提取文件并返回连接设置。</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL Continue]**&#x200B;保存连接并返回模块。

## Adobe Experience Manager Forms模块及其字段

目前，Adobe Experience Manager Forms连接器只有一个模块。

### 关注表单事件

这个即时触发器(webhook)允许您在Adobe Experience Manager表单上发生提交操作时启动场景。

>[!IMPORTANT]
>
>此外，还需要在Adobe Experience Manager中配置此模块。 设置此webhook后，必须打开Adobe Experience Manager并配置表单以将提交内容发送到webhook。
>
><!--For instructions on the required form configuration, see insert url here-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p>输入webhook的名称</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Experience Manager]帐户连接到[!DNL Workfront Fusion]的说明，请参阅<a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref">创建与[!DNL Adobe Experience Manager Forms]</a>的连接</p> </td> 
  </tr>

模块将创建一个webhook并提供webhook地址，您可以在[!DNL Adobe Experience Manager Forms]中输入该地址到表单提交对话框中。
