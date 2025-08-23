---
title: Adobe Experience Manager Forms模块
description: 使用Adobe Workfront Fusion的 [!DNL Adobe Experience Manager Forms] 连接器，您可以基于 [!DNL Adobe Experience Manager Forms] 帐户中的事件启动方案，创建、上传和更新资源，以及复制或移动文件夹和资源。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 1%

---

# [!DNL Adobe Experience Manager Forms]模块

使用Adobe Workfront Fusion的[!DNL Adobe Experience Manager Forms]连接器，您可以通过创建webhook来基于[!DNL Adobe Experience Manager Forms]帐户中的事件启动方案。

您可以在[!DNL Adobe Experience Manager Forms]内配置表单，以将表单提交内容发送到此webhook。

## 访问要求

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront计划*</td>
  <td> <p>[！UICONTROL Pro]或更高版本</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证*</td>
   <td> <p>[！UICONTROL计划]，[！UICONTROL工作]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>当前许可证要求：无Workfront Fusion许可证要求。</p>
   <p>或</p>
   <p>旧版许可证要求：[！UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>当前产品要求：如果您有[！UICONTROL Select]或[！UICONTROL Prime] Adobe Workfront计划，则贵组织必须购买Adobe Workfront Fusion和Adobe Workfront，才能使用本文中所述的功能。 Workfront Fusion包含在[！UICONTROL Ultimate] Workfront计划中。</p>
   <p>或</p>
   <p>旧版产品要求：您的组织必须购买Adobe Workfront Fusion和Adobe Workfront，才能使用本文中所述的功能。</p>
   </td> 
  </tr> 
 </tbody> 
</table>

要了解您拥有的计划、许可证类型或访问权限，请联系您的Workfront管理员。

有关Adobe Workfront Fusion许可证的信息，请参阅[Adobe Workfront Fusion许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

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

1. 在任意模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[！UICONTROL连接名称]</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL环境]</td>
        <td>
          <p>选择此连接是连接到生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL类型]</td>
        <td>
          <p>选择此帐户是服务帐户还是个人帐户。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL实例URL，不带尾随斜杠]</td>
        <td>
          <p>输入用于访问帐户的URL，不带最后一个斜杠。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL IMS端点]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL客户端ID]</td>
        <td>输入您的[!DNL Adobe]客户端ID。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL客户端密钥]</td>
        <td>输入您的[!DNL Adobe]客户端密钥。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL组织ID]</td>
        <td>输入您的[!DNL Adobe]组织ID。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL技术帐户ID]</td>
        <td>输入您的[!DNL Adobe]技术帐户ID。 这可以在[!DNL Adobe Developer Console]的[！UICONTROL凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL元范围]</td>
        <td>输入任何适当的元范围       </td>
      </tr>
      <tr>
        <td role="rowheader">[！UICONTROL私钥]</td>
        <td>
          <p>输入在[!DNL Adobe Developer Console]中创建凭据时生成的私钥。 </p>
          <p>要提取您的私钥或证书，请执行以下操作：</p>
          <ol>
            <li value="1">
              <p>单击<b>[！UICONTROL提取]</b>。</p>
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
              <p>单击<b>[！UICONTROL保存]</b>以提取文件并返回到连接设置。</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. 单击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

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
   <td role="rowheader">[！UICONTROL Webhook名称]</td> 
   <td> <p>输入webhook的名称</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Connection]</td> 
   <td> <p>有关将[!DNL Adobe Experience Manager]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref">创建与[!DNL Adobe Experience Manager Forms]</a>的连接</p> </td> 
  </tr>

模块将创建一个webhook并提供webhook地址，您可以在[!DNL Adobe Experience Manager Forms]中输入该地址到表单提交对话框中。
