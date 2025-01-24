---
title: 使用大文件
description: Workfront和HTTP连接器当前支持大文件。
author: Becky
feature: Workfront Fusion
exl-id: 6df81943-e70c-42b3-aa44-d82343598a51
source-git-commit: 0e69dfa23fc12cb20c3fed772d72ef348536ea24
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 1%

---

# 使用大文件

>[!IMPORTANT]
>
>大文件功能仅适用于Workfront Ultimate包上的组织。

Workfront Fusion中现在提供了增强的数据传输功能，支持在场景中处理显着更大的文件。

要处理较大的文件，必须更新方案。

## 支持大文件的连接器

目前，以下连接器支持大型文件。

* Workfront
   * 上传文档
   * 下载文档
* Adobe Experience Manager Assets
   * 上传文档
* Workfront 验证
   * 上传文件
   * 下载校对
* Adobe Authenticator
   * 进行自定义API调用
* SharePoint
   * 创建文件
   * 获取文件
* Salesforce
   * 上传文件
* AWS S3
   * 上传文件
   * 获取文件
* HTTP

其他连接器将在未来版本中受支持。

## 更新方案以处理大文件

Workfront >上传文档模块已修改，可处理较大的文件。 此模块的前一版本现在显示附加到模块名称的`(Legacy)`。 在大多数情况下，旧版模块将继续正常运行。

如果您计划处理较大的文件，我们建议将旧版模块替换为新的上传文档模块。 新的上传文档模块可以防止超时和其他错误。

![上载文档](assets/new-upload-document.png)

## 常见问题解答

### 新的文件大小限制是什么？

用户现在可以处理超过以前的1 GB限制的文件，从而提高效率和生产力。  虽然该平台单个操作（如上传文件）最多可支持15 GB的单个文件，但还有其他因素会影响数据传输。 单个操作的文件大小限制最终取决于Fusion连接到的Web服务。 数据传输是单次执行的总体处理。 这意味着，单次执行中的多个操作会对总数据传输做出贡献。

Fusion会处理文件，直到达到40分钟的执行限制。 在Fusion场景中，大文件可能需要一些时间才能上传、下载或处理。 虽然单个文件大小没有限制，但方案执行时间限制为40分钟。 因此，如果大文件导致执行时间超过40分钟，则场景会失败。 场景执行时间还受场景大小、模块复杂性和网络速度影响。 因此，我们建议您在使用大文件时考虑方案的这些方面。

### Fusion的新文件传输工作方式

Fusion处理文件时，会将较大的文件添加到永久存储（S3存储段或Azure Blob存储）。 当Fusion模块执行文件操作（如上载或下载）时，Fusion使用永久存储中的文件作为源，而不是使用活动内存。

### 我能否处理不完整执行的大型文件？

是，Fusion支持具有较大文件的未完成执行。 请注意，未完成的执行在组织内大小有限，应积极管理。

### 我可以在任何连接器中使用较大的文件吗？

必须更新每个Fusion连接器以支持更大的文件。 支持的连接器包括Workfront、HTTP和AEM Assets。 Fusion连接器仍受Web服务支持的文件大小的限制。 文件大小限制通常包含在用于下载和上传文件的Web服务端点的API文档中。

### 这是否会影响操作？

不会，模块执行的操作数是相同的。

### 何时更新Fusion的UI以显示文件传输数据？

此功能已经完成并部署到生产环境。

### 有哪些方法可以帮助我设计场景来考虑新的文件处理限制？

设计一个在40分钟执行限制内工作的场景可能看起来很复杂。 我们建议在设计场景时牢记以下几点：

* **了解您对执行时间的业务要求**： Fusion对执行时间的平台限制为40分钟，但大多数业务流程自动执行的速度预计会快得多。 例如，用户启动的具有依赖结果的后续的自动化应在40分钟限制内很好地完成。
* **在设计方案时考虑执行时间**：在设计方案时，必须了解各个文件操作（如上载和下载）的模块执行时间。 此知识可帮助您规划涉及多个文件操作的方案。  为了确保设计的准确性，我们建议将模块的执行时间四舍五入以包含缓冲区。
例如，如果Fusion在144秒（2.4分钟）内下载文档，您可以预计单次执行可以多次执行类似操作。 在本例中，执行模块需要144秒，您应该为下载安排3分钟的执行时间。 如果您的要求包括上载和下载，则预计执行时间约为6分钟。 请注意，Fusion执行时间限制为40分钟。

* **合并文件操作**：在Fusion场景中，最常见的文件操作示例是一次下载和一次上传。 大多数仅具有这两个操作的方案将在几分钟内执行。 如有可能，Fusion设计人员应将其方案限制为一次下载和一次上传。

* **使用映射面板计算大小**： Workfront和其他Web服务在下载模块的输出中包含文件的文件大小。 您可以使用此数据过滤掉对于模块上传来说太大或者对于方案执行时间来说太大的一些文件。

* **在处理多个文件时，将文件操作隔离在自己的方案中**： Fusion设计器应考虑将文件操作隔离到单独的方案中。 例如，对于由带有多个附加文件的新Workfront请求触发的Fusion场景，可能需要容纳最多30个文件。 由于上传和下载每个文件最多可能需要3分钟，因此在一次执行中处理所有文件将超过Fusion的40分钟执行限制。 解决方案是创建一个文件操作方案，专门用于处理单个文件的上传和下载。 请求触发的场景将遍历附加文件，并使用HTTP模块为每个文件调用文件操作场景。 此方法可确保在执行时间限制内处理每个文件。

<!--
## Connectors that do not support large files

Some Fusion connectors do not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

The following connectors do **not** support large files. 

* Archive
* Box
* Convert
* CSV
* Datastores
* Flow control
* FTP
* JSON
* JWT
* Markdown
* Math
* Microsoft Word templates
* MIME
* Microsoft SQL
* SFTP
* Adobe Acrobat Sign
* SOAP
* Tools
* XML

If a connector is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.-->






<!--## Connectors that support large files

The following connectors support large files.

Workfront
HTTP
Webhooks
Salesforce
Microsoft Email
Workfront Proof
AEM Assets
Email
Slack
Jira
Microsoft Excel
SharePoint
Frame.io
Adobe PDF Services
Marketo
Azure Devops 
Google Email
Jira Server
Google Sheets
Microsoft OneDrive
ServiceNow 
AWS S3
Bynder
OneDrive Business
Adobe Authenticator
Google Drive
Microsoft Dynamics
Google Docs
NetSuite
Airtable
Azure AD
QuickBase 
Adobe Target
Adobe Campaign Classic
Microsoft Calendar
Workfront Planning
HubSpot CRM  
DropBox
Cloud Convert
Egnyte
Adobe Firefly
OpenAI / Chat GPT
Allocadia
Cvent
GitLab 
Google Team Drive
Google Calendar
Workfront SDL Managed Translation
Widen
Workfront Boards
Google Slides
Qualtrics
Microsoft Power BI
Adobe Photoshop
Anaplan
DocuSign 
MariaDB
Adobe Creative Cloud Libraries
Figma
AEM Forms
Datadog
GitHub 
Google Forms
Adobe I/O Events
Trello
Workday
Adobe Journey Optimizer
Adobe Lightroom


If a file is not on this list, it does not support large files. For these connectors, Fusion's total processing capacity for files is **1 GB**. 

This limit is based on a total memory cost. Every operation contributes to that cost. If a single file of 400 MB is downloaded and uploaded then the total cost to the file capacity would be 800 MB.

-->
