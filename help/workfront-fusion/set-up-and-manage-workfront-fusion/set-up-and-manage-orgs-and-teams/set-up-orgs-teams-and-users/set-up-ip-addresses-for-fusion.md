---
title: 列入允许列表在组织的中配置用于Fusion的IP地址
description: Fusion使用特定的IP地址和域进行Web通信。 必须将这些组件添加到您组织的允许列表中，然后才能在您的组织中使用Workfront。
author: Becky
feature: Workfront Fusion
exl-id: 406dd45c-0863-4270-a80e-c1c115e0b367
source-git-commit: 59d739093c88238af7a7e97499fd0c7d7cf6053a
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 0%

---

# 列入允许列表在组织的中配置用于Fusion的IP地址

由于Adobe Workfront Fusion与贵组织的网络进行通信，因此必须将贵组织的防火墙配置为允许该通信。 防火墙是一种高效的安全措施，通过将组织的网络与Internet分隔开来发挥作用。 它们可确保只有选定的数据和网络流量才能移入或移出组织的网络。 防火墙根据发送或接收数据的站点允许或阻止数据。 作为Fusion管理员，您必须确保发送到Fusion或从Fusion发送的数据可以通过贵组织的防火墙。

这可以通过允许列表实现，它实际上是“允许”通过防火墙发送或接收数据的站点的“列表”。 可以通过以下两种方式之一标识站点：

* **IP地址**：一系列数字，如52.31.132.175
* **域**： URL的一部分，如`www.thisdomain.com`中的`thisdomain`

Fusion使用特定的IP地址和域进行Web通信。 必须将这些组件添加到您组织的允许列表中，然后才能在您的组织中使用Workfront。

通常，允许列表是由网络管理员配置的。 与贵组织的网络管理员合作，确保您的防火墙允许这些IP地址。 如果您不知道网络管理员是谁，贵组织的IT部门可以引导您向正确的方向前进。

>[!IMPORTANT]
>
>作为Fusion管理员，您必须确保将这些IP地址和域添加到组织的允许列表中。 即使您自己不添加它们，也是如此。 Fusion无法配置组织的允许列表。

您可以将所有Fusion IP地址和域添加到允许列表，也可以查找Fusion群集并仅添加该群集的IP地址和域。

## 添加所有Fusion IP地址和域

将以下IP地址添加到您的允许列表：

* 52.30.133.50
* 54.220.93.204
* 34.254.76.122
* 54.244.142.219
* 52.39.217.230
* 44.241.82.96
* 100.20.126.137
* 34.223.32.4
* 52.39.176.220
* 20.36.133.48/28
* 20.81.156.240/28
* 172.172.84.48/28

此外，如果贵组织使用出站网络过滤，请将以下域添加到您的以使您的允许列表能够访问Workfront Fusion。

* hook.app.workfrontfusion.com
* hook.app-eu.workfrontfusion.com
* hook.app-az.workfrontfusion.com

## 仅为群集添加Fusion IP地址和域

### 识别您的数据中心

IP地址因存储数据的位置而异。

如果通过URL访问Fusion，则可以检查该URL以查找数据中心。

| URL | 数据中心 |
| --- | --- |
| `https://app.workfrontfusion.com` | 美国数据中心 |
| `https://app-eu.workfrontfusion.com` | 欧盟数据中心 |
| `https://app-az.workfrontfusion.com` | Azure群集 |

如果您通过`experience.adobe.com`访问Fusion，则可以检查浏览器中的“网络”选项卡以识别数据中心。

| URL | 数据中心 |
| --- | --- |
| 对`https://fusion.adobe.com`的调用 | 美国数据中心 |
| 对`https://eu.fusion.adobe.com`的调用 | 欧盟数据中心 |
| 对`https://az.fusion.adobe.com`的调用 | Azure群集 |

### 为数据中心添加IP地址和域

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 欧盟数据中心</td> 
   <td> 
    <ul> 
     <li>52.30.133.50</li> 
     <li>54.220.93.204</li> 
     <li>34.254.76.122</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront] 美国数据中心</p> </td> 
   <td> 
    <ul> 
     <li>54.244.142.219</li> 
     <li>52.39.217.230</li> 
     <li>44.241.82.96</li>
     <li>100.20.126.137</li>
     <li>34.223.32.4</li>
     <li>52.39.176.220</li>
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] 在Microsoft Azure群集上</td> 
   <td> 
    <ul> 
     <li>20.36.133.48/28</li> 
     <li>20.81.156.240/28</li> 
     <li>172.172.84.48/28</li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

此外，如果贵组织使用出站网络过滤，请将以下域添加到您的以使您的允许列表能够访问Workfront Fusion。 这些用于Webhook

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] 欧盟数据中心</td> 
   <td> <p> hook.app-eu.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront] 美国数据中心</p> </td> 
   <td> <p>hook.app.workfrontfusion.com </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Adobe Workfront Fusion] 在Microsoft Azure群集上</p> </td> 
   <td> <p>hook.app-az.workfrontfusion.com </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>出站网络过滤不常见。 请咨询网络管理员，了解是否需要更新允许列表以适应环境。
