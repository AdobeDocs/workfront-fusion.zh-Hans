---
content-type: overview
title: 方案执行流程
description: 本文介绍了场景的执行方式以及数据流通过场景的方式。 它还介绍了可在何处找到有关已处理数据的信息以及如何读取该信息。
author: Becky
feature: Workfront Fusion
exl-id: bd4f05e2-df3c-4848-9a70-3df18ca4461b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# 方案执行流程

本文介绍了场景如何执行以及数据流经场景以及如何查看每个模块处理的数据。

要查看数据如何流经活动方案，请参阅[查看正在运行方案中的数据流](/help/workfront-fusion/manage-scenarios/view-scenario-data-flow.md)。

## 方案执行流程

正确设置并激活场景后，该场景将根据其定义的计划执行。

在场景开始时，第一个模块会响应已设置为监视的事件。 在返回数据时，该数据将打包为多个包。 场景为每个事件返回一个捆绑包。 例如，如果某个模块设置为观察问题，它将为其找到的每个问题返回一个数据捆绑。

如果触发模块返回任何数据包，则这些包将传递到下一个模块，并且场景会继续，将包传递通过每个后续模块，一次传递一个。

如果捆绑包在所有模块中正确处理，则在“方案详细信息”页面中将该方案标记为成功。

### 示例：[!UICONTROL 用于工作自动化的Workfront Fusion]

>[!BEGINSHADEBOX]

**示例：**&#x200B;在这种情况下，在Workfront中监视传入请求，然后将它们转换为Workfront项目，数据将按如下方式流动：

场景的第一步由第一个模块执行，即监视请求。 找到的每个请求都视为一个捆绑包。 如果模块运行时未找到任何捆绑包，则场景将在第一个模块后结束。

如果第一个模块返回一个捆绑包，则该捆绑包将传递场景的其余部分。 在此示例中，捆绑包将转到第二个模块，后者将请求转换为项目。

![Workfront场景的执行流程](assets/example-execution-flow-wf-only.png)

>[!ENDSHADEBOX]

### 示例： [!UICONTROL 用于工作自动化和集成的Workfront Fusion]

>[!BEGINSHADEBOX]

**示例：**&#x200B;在这种从Adobe Workfront下载文档并将文档发送到[!DNL Dropbox]中的文件夹的情况中，数据将按如下方式流动：

场景的第一步由第一个模块执行，即在Workfront中查看文档。 找到的每个文档都被视为一个捆绑包。 如果模块运行时未找到任何捆绑包，则场景将在第一个模块后结束。

如果返回一个束，则该束将通过场景的其余部分。 在此示例中，方案的其余部分包含secondmodule，它将包上载到[!DNL Dropbox]文件夹。

![集成方案的执行流程](assets/example-execution-flow-wf-dropbox.png)

如果第一个模块返回多个包，则在上传第二个包之前，会将第一个包上传到[!DNL Dropbox]。 然后，第二个包上传，第三个包上传，依此类推。

>[!ENDSHADEBOX]

## 有关已处理包的信息

对于每个模块，捆绑包在进入下一个模块或到达其最终目标之前将经过4步的过程。

* 初始化
* 操作
* 提交/回滚
* 最终完成

>[!NOTE]
>
>大场景也会经历这一过程。 有关方案级别上此过程的信息，请参阅[方案执行、周期和阶段](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md)。

场景运行完成后，每个模块会显示一个图标，其中显示了执行的操作数。 您可以单击此图标以显示有关进程中每个步骤的已处理捆绑的详细信息。 您可以查看使用了哪些模块设置以及每个模块返回的包。

![已处理的包](assets/Info-processed-bundles.png)

在此示例中，模块接收了如下输入信息：

* 它发现的问题的ID
* 问题将转换为的对象（项目）
* 用于创建项目的模板的ID
* 找到对象的记录类型（OPTASK，这是一个问题）

处理后，模块返回以下输出信息：

* 新创建的项目的ID。

如果模块发现多个问题，则会分别捕获每个捆绑包的信息。 将有一个操作2区域，其输入和输出部分描述第二个束，依此类推。

## 执行场景时出错

在场景运行期间可能会出错。 例如，如果您删除了模块将用来创建新项目的模板，则场景将终止，并显示一条错误消息。 有关如何处理错误的详细信息，请参阅[错误类型](/help/workfront-fusion/references/errors/error-processing.md)。

## 资源

* 有关设置方案的详细信息，请参阅[方案编辑器](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md)。
* 有关方案详细信息页面的详细信息，请参阅[方案详细信息](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-details.md)。
* 有关激活方案的详细信息，请参阅[激活或停用方案](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md)。
* 有关计划方案的详细信息，请参阅[计划方案](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md)。
* 有关模块的详细信息，请参阅[模块概述](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md)。
