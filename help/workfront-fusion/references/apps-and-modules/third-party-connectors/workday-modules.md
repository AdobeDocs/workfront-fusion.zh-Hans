---
filename: workday-modules
title: Workday模块
description: 在Adobe Workfront Fusion方案中，您可以自动使用 [!DNL Workday]的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion
exl-id: 77237a1b-2acd-4350-9cc0-ec43b8b08137
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 1%

---

# [!DNL Workday]模块

在Adobe Workfront Fusion场景中，您可以自动使用[!DNL Workday]的工作流，并将其连接到多个第三方应用程序和服务。

有关创建方案的说明，请参阅[创建方案：文章索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的文章。

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

要使用[!DNL Workday]模块，您必须：

* 拥有[!DNL Workday]帐户。

* 在[!DNL Workday]中创建OAuth应用程序。 有关说明，请参阅[!DNL Workday]文档。

## Workday API信息

Workday连接器使用以下对象：

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">基本 URL</td> 
   <td>https://{{connection.servicesUrl}}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">API标记</td> 
   <td>v1.6.4</td> 
  </tr>
 </tbody> 
 </table>

## 将[!DNL Workday]连接到Workfront Fusion

1. 在任意Workfront Fusion模块中，单击[!UICONTROL 连接]字段旁边的[!UICONTROL 添加]

2. 填写以下字段：

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL 连接名称]</p>
                </td>
                <td>输入连接的名称。</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Workday host]</td>
                <td>输入不带[!DNL Workday]的<code>https://</code>主机的地址。 例如： <code>mycompany.workday.com</code>。</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL 服务URL]</td>
                <td>输入您的[!DNL Workday] Web服务的地址，但不输入<code>https://</code>。 例如： <code>mycompany-services.workday.com</code>。</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL 租户名称]</td>
                <td>输入此[!DNL Workday]帐户的租户。 您的租户是贵组织的标识符，可在您用于登录Workday的URL中看到。 示例：在地址<code>https://www.myworkday.com/mycompany</code>中，租户是<code>mycompany</code>。</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL 客户端ID]</td>
                <td>输入此连接使用的[!DNL Workday]应用程序的客户端ID。 您在[!DNL Workday]中创建应用程序时获取此内容。</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL 客户端密钥]</td>
                <td>输入此连接使用的[!DNL Workday]应用程序的客户端密钥。 您在[!DNL Workday]中创建应用程序时获取此内容。</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL 会话超时（分钟）]</td>
                <td >输入授权令牌过期的分钟数。</td>
            </tr>
        </tbody>
    </table>


3. 单击[!UICONTROL 继续]保存连接并返回模块

## [!DNL Workday]模块及其字段

在配置[!DNL Workday]模块时，Workfront Fusion将显示以下列出的字段。 除此以外，可能还会显示其他[!DNL Workday]字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的粗体标题表示必填字段。

如果看到字段或函数上方的映射按钮，则可以使用该按钮设置该字段的变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [操作](#action)

* [搜索](#search)


### 操作

* [[!UICONTROL 创建记录]](#create-a-record)

* [[!UICONTROL 删除记录]](#delete-a-record)

* [[!UICONTROL 进行自定义API调用]](#make-a-custom-api-call)

* [[!UICONTROL 更新记录]](#update-a-record)


#### [!UICONTROL 创建记录]

此操作模块在[!DNL Workday]中创建单个记录。

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>有关将[!DNL Workday]帐户连接到Workfront Fusion的说明，请参阅<a href="#Connect" class="MCXref xref" >将[!DNL Workday]连接到Workfront Fusion</a>。</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 记录类型]</td>
            <td>选择要创建的记录类型。</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>输入或映射要创建的记录的ID。</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL 子资源ID]</td>
            <td >输入或映射要创建的子资源的ID。</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL 删除记录]

此操作模块删除[!DNL Workday]中的单个记录。

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>有关将[!DNL Workday]帐户连接到Workfront Fusion的说明，请参阅<a href="#Connect" class="MCXref xref" >将[!DNL Workday]连接到Workfront Fusion</a>。</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 记录类型]</td>
            <td>选择要删除的记录类型。</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL 特定记录类型]</td>
            <td>选择要删除的特定记录类型。 这些基于您选择的记录类型。</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 子资源ID]</td>
            <td>输入或映射要删除的子资源的ID。</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >输入或映射要删除的记录的ID。</td>
        </tr>
    </tbody>
</table>


### [!UICONTROL 进行自定义API调用]

此操作模块允许您对[!DNL Workday] API进行经过身份验证的自定义调用。 这样，您可以创建其他[!DNL Workday]模块无法实现的数据流自动化。

配置此模块时，会显示以下字段。

模块返回a状态代码，以及API调用的标头和正文。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Connection]</p> </td> 
            <td>有关将[!DNL Workday]帐户连接到Workfront Fusion的说明，请参阅<a href="#Connect" class="MCXref xref" >将[!DNL Workday]连接到Workfront Fusion</a>。</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>输入相对于<code style="color: #ff1493;">https://&lt;tenantHostname>/api/&lt;serviceName>/&lt;version>/&lt;tenant></code>的路径。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 方法]</td> 
   <td> <p>选择配置API调用所需的HTTP请求方法。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref">HTTP请求方法</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>以标准JSON对象的形式添加请求的标头。</p> <p>例如， <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion]会为您添加授权标头。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL 查询字符串]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的查询。</p> <p>例如： <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>以标准JSON对象的形式添加API调用的正文内容。</p> <p>注释：  <p>在JSON中使用条件语句（如<code>if</code>）时，请将引号放在条件语句之外。</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL 更新记录]

此操作模块更新[!DNL Workday]中的单个记录。

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>有关将[!DNL Workday]帐户连接到Workfront Fusion的说明，请参阅<a href="#Connect" class="MCXref xref" >[!UICONTROL 将[!DNL Workday]连接到Workfront Fusion]</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 记录类型]</td>
            <td>选择要更新的记录类型。</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>输入或映射要更新的记录ID。</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL 子资源ID]</td>
            <td >输入或映射要更新的子资源的ID。</td>
        </tr>
    </tbody>
</table>

### 搜索

* [[!UICONTROL 读取记录]](#read-a-record)

* [[!UICONTROL 列出记录]](#list-records)


#### [!UICONTROL 读取记录]

此操作模块读取单个记录。

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>有关将[!DNL Workday]帐户连接到Workfront Fusion的说明，请参阅<a href="#Connect" class="MCXref xref" >[!UICONTROL 将[!DNL Workday]连接到Workfront Fusion]</a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL 记录类型]</td>
            <td>选择要删除的记录类型。</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL 特定记录类型]</td>
            <td>选择要读取的特定记录类型。 这些基于您选择的记录类型。</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >输入或映射要删除的记录的ID。</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL 列出记录]

此搜索模块检索指定类型的记录列表。

<table style="table-layout:auto"> 
      <col/>
      <col/>
      <tbody>
          <tr>
              <td role="rowheader">[!UICONTROL Connection]</td>
              <td>有关将[!DNL Workday]帐户连接到Workfront Fusion的说明，请参阅<a href="#Connect" class="MCXref xref" >将[!DNL Workday]连接到Workfront Fusion</a></td>
          </tr>
          <tr>
              <td  role="rowheader">[!UICONTROL 记录类型]</td>
              <td>选择要检索的记录类型。</td>
          </tr>
          <tr>
              <td role="rowheader">[!UICONTROL 限制]</td>
              <td >
                  <p>输入或映射您希望模块在每个方案执行周期中检索的最大记录数。</p>
              </td>
          </tr>
      </tbody>
  </table>
