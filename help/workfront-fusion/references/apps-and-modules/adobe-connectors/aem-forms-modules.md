---
title: Adobe Experience Manager Forms 模块
description: 使用Adobe Workfront Fusion的 [!DNL Adobe Experience Manager Forms] 连接器，您可以基于 [!DNL Adobe Experience Manager Forms] 帐户中的事件启动方案，创建、上传和更新资源，以及复制或移动文件夹和资源。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
TQID: https://experienceleague.adobe.com/LTNDa0pulA4RE5tG59Fui-5bPlKxqHoQHEsKOp485No
product_v2:
  - id: c4a86a5d-6562-4fc6-aa00-bfa25833aed9
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 219b9dbf3a7e4be1676b21bc3d3752d70d743b13
workflow-type: tm+mt
source-wordcount: 600
ht-degree: 50%

---

# [!DNL Adobe Experience Manager Forms] 模块

使用Adobe Workfront Fusion的[!DNL Adobe Experience Manager Forms]连接器，您可以通过创建webhook来基于[!DNL Adobe Experience Manager Forms]帐户中的事件启动方案。

您可以在[!DNL Adobe Experience Manager Forms]内配置表单，以将表单提交内容发送到此webhook。

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

* 您必须拥有[!DNL Adobe Experience Manager Forms]帐户才能使用此模块。

## Adobe Experience Manager Assets API 信息

Adobe Experience Manager Assets 连接器使用以下内容：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API 标记</td> 
   <td>v1.2.27</td> 
  </tr>
 </tbody> 
 </table>

## 创建与Adobe Experience Manager Forms的连接

要为您的 [!DNL Adobe Experience Manager Forms] 模块创建连接：

1. 在任意模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

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
        <td>
          <p>选择此连接是连接到生产环境还是非生产环境。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 类型]</td>
        <td>
          <p>选择此帐户是服务帐户还是个人帐户。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 实例URL，不带尾随斜杠]</td>
        <td>
          <p>输入用于访问帐户的URL，不带最后一个斜杠。</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL IMS端点]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端 ID]</td>
        <td>输入您的[!DNL Adobe]客户端ID。 该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 客户端密钥]</td>
        <td>输入您的[!DNL Adobe]客户端密钥。 该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 组织ID]</td>
        <td>输入您的[!DNL Adobe]组织ID。 该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 技术帐户ID]</td>
        <td>输入您的[!DNL Adobe]技术帐户ID。 该值可在 [!DNL Adobe Developer Console] 的[!UICONTROL 凭据详细信息]部分找到。
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>输入任何适当的元范围       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL 私钥]</td>
        <td>
          <p>输入在[!DNL Adobe Developer Console]中创建凭据时生成的私钥。 </p>
          <p>要提取您的私钥或证书：</p>
          <ol>
            <li value="1">
              <p>点击<b>[!UICONTROL 提取]</b>。</p>
            </li>
            <li value="2">
              <p>选择您要提取的文件类型。</p>
            </li>
            <li value="3">
              <p>选择包含私钥或证书的文件。</p>
            </li>
            <li value="4">
              <p>输入该文件的密码。</p>
            </li>
            <li value="5">
              <p>点击<b>[!UICONTROL 保存]</b>以提取文件，并返回连接设置界面。</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。

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
   <td role="rowheader">[!UICONTROL Webhook 名称]</td> 
   <td> <p>输入 Webhook 的名称</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 连接]</td> 
   <td> <p>有关将[!DNL Adobe Experience Manager]帐户连接到Workfront Fusion的说明，请参阅<a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref">创建与[!DNL Adobe Experience Manager Forms]</a>的连接</p> </td> 
  </tr>

模块将创建一个webhook并提供webhook地址，您可以在[!DNL Adobe Experience Manager Forms]中输入该地址到表单提交对话框中。
