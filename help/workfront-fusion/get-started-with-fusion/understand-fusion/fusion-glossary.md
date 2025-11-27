---
title: Adobe Workfront Fusion 术语表
description: 以下术语表解释了 Adobe Workfront Fusion 中的一些常用术语。
author: Becky
feature: Workfront Fusion
exl-id: 7f098ec2-8594-4e5d-9ce7-d1738a05f9a6
source-git-commit: 190bfe5992fb21b789a7246c4ae732a5dc7672fa
workflow-type: ht
source-wordcount: '924'
ht-degree: 100%

---

# Adobe Workfront Fusion 术语表

以下术语表解释了 Adobe Workfront Fusion 中的一些常用术语。


<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>操作</p> </td> 
   <td>一种模块，可执行操作，例如从所选应用程序或服务读取数据或向其写入数据。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>聚合器</p> </td> 
   <td> <p>一种模块类型，可将多个捆绑包（多个数据集合）合并为单一捆绑包。 </p><p>如需了解更多信息，请参阅<a href="/help/workfront-fusion/references/modules/aggregator-module.md" class="MCXref xref">聚合器模块</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API</td> 
   <td>应用程序编程接口（API）是一种使应用程序与服务之间能够相互通信的方式。Fusion 通过 API 与您要连接的应用程序进行通信。每个应用程序都有各自独立的 API。 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API 密钥</td> 
   <td>用于身份验证的唯一代码，用于标识调用软件 API 的用户、开发人员或程序。由于 Fusion 模块通过连接 API 运行，因此有时需要 API 密钥。API 密钥由需要它们的应用程序分发。例如，如果您需要将 Fusion 连接到 Adobe Lightroom，则需通过您的 Adobe Lightroom 帐户申请 API 密钥。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">应用程序或服务</td> 
   <td> <p>一种软件应用程序。Fusion 可以连接大多数应用程序，即使该应用程序没有专用连接器。</p> <p>应用程序也可以是操作数据的特殊功能，例如迭代器或聚合器。 </p> <p>服务是数据来源，可能包括 Web API、网页、不同类型的服务器（FTP、SMTP、IMAP）等。 </p>  </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>捆绑包</p> </td> 
   <td> <p>捆绑包是模块返回或接收的基本数据单元。例如，一个返回三条记录的搜索模块会输出三个数据捆绑包，每个捆绑包对应一条记录。捆绑包由多个项目组成。</p> </td> 
  </tr> 
  <tr>
   <td role="rowheader"> <p>连接</p> </td> 
   <td> <p>连接表示用于连接某项服务的一组凭据。您可以在任意模块中配置连接，并在其他模块中复用该连接。每个模块都必须选择一个连接，以便 Fusion 使用这些凭据访问该模块所需的信息。 </p><p>有关更多信息，请参阅<a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md" class="MCXref xref">连接概述</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">连接器</td> 
   <td>连接器是一组为特定应用程序提供的模块集合。Workfront Fusion 为许多常见的工作类应用程序（如 Workfront、Salesforce 和 Jira）提供连接器。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>周期</p> </td> 
   <td> <p>一个周期由场景运行的两个阶段组成：操作阶段和提交阶段。场景可能包含一个或多个周期。有关更多详细信息，请参阅<a href="/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md" class="MCXref xref">场景执行、周期与阶段</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>数据存储</p> </td> 
   <td> <p>数据存储用于保存场景中的数据，或用于在不同场景或场景运行之间传输数据。 </p><p>有关更多信息，请参阅<a href="/help/workfront-fusion/create-scenarios/map-data/data-stores.md" class="MCXref xref">数据存储</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>筛选条件</p> </td> 
   <td> <p> 筛选条件可应用在两个模块之间，便于您仅处理符合特定条件的捆绑包。您可以应用多种不同类型的筛选条件。 </p><p>有关更多信息，请参阅<a href="/help/workfront-fusion/create-scenarios/add-modules/add-a-filter-to-a-scenario.md" class="MCXref xref">向场景添加筛选条件</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>ID </p> </td> 
   <td> <p>用于唯一标识捆绑包的名称。ID 通常用于区分需要在某个服务中更新或删除的捆绑包。ID 可以从上一个模块的输出中映射。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>项目</p> </td> 
   <td> <p>捆绑包的一部分。 捆绑包可以包含多个项目。 项目类型多样，包括文本、数字、布尔值（是/否）、日期、时间、缓冲区（二进制数据）、收藏集、选择菜单、数组和验证字段。</p><p> 有关更多信息，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">项目数据类型</a>。</p> </td> 
  </tr>
  <tr> 
   <td role="rowheader"> <p>迭代器</p> </td> 
   <td> <p>一种模块类型，可将一个数据捆绑包（数据集合）拆分为多个独立的捆绑包。这些捆绑包随后可由后续模块分别进行处理。 </p><p>有关更多信息，请参阅<a href="/help/workfront-fusion/references/modules/iterator-module.md" class="MCXref xref">[!UICONTROL 迭代器]模块</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>模块</p> </td> 
   <td> <p>场景中的单个步骤，在关联的应用程序或服务中执行某项功能，例如创建记录。</p> <p>每个应用程序或服务都具有多个模块，这些模块定义了其响应请求的方式。</p>  <p> <img src="assets/module.png"> </p> <p>有关更多信息，请参阅<a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">模块概述</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>操作</p> </td> 
   <td> <p>模块执行的操作，例如检索记录或上传文件。</p><p>有关更多信息，请参阅<a href="/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md" class="MCXref xref">操作</a>。</p>
  </tr> 
  <tr> 
   <td role="rowheader">公钥/私钥</td> 
   <td>公钥和私钥用于加密和解密数据。公钥可以公开分发，任何拥有公钥的人都可以对数据进行加密，但只有私钥才能解密这些数据。同样，拥有私钥的用户也可以加密数据，而任何拥有公钥的人都可以解密。私钥加密可确保数据由私钥所有者生成，从而验证数据来源的可信性。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>路由器</p> </td> 
   <td>路由器可在场景中复制数据或添加新路由，以便重新路由数据并分别处理不同的数据组。</p><p> 有关更多信息，请参阅<a href="/help/workfront-fusion/create-scenarios/add-modules/router-module.md" class="MCXref xref">[!UICONTROL 路由器]模块</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>场景</p> </td> 
   <td> <p>由用户创建的一系列自动化步骤，每个步骤由一个模块表示并执行。场景的目的在于移动和处理数据。</p> <p> <img src="assets/entire-scenario-blank.png" style="width: 350;height: 178;"> </p> <p> 有关更多信息，请参阅<a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md" class="MCXref xref">场景概述</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>场景区段</p> </td> 
   <td> <p> 场景区段是场景中的一个部分，由一系列连接到同一应用程序的模块组成。场景区段通常表示应用程序中的一段短工作流程。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>触发器</p> </td> 
   <td> <p>触发器是一种模块，用于监控新增或更新的数据，并在符合模块中配置的条件时启动场景。触发器可以配置为按计划（轮询）启动场景，也可以在数据发生变化时立即启动（即时触发器或 Webhook）。</p> <p>有关更多信息，请参阅模块概述文章中的<a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md" class="MCXref xref">触发器</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Webhook</p> </td> 
   <td> <p>一种特殊的触发器，可在新捆绑包可用时立即运行场景。 </p><p>有关更多信息，请参阅<a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref">即时触发器</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>
