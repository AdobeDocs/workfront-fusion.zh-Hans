---
title: Adobe Firefly音频和视频模块
description: 在Adobe Workfront Fusion场景中，您可以自动使用Adobe Firefly Audio and Video的工作流，并将其连接到多个第三方应用程序和服务。
author: Becky
feature: Workfront Fusion, Digital Content and Documents
source-git-commit: f54338aa35b8453ac991c9e16974f2b61fd30168
workflow-type: tm+mt
source-wordcount: '1618'
ht-degree: 14%

---

# Adobe Firefly音频和视频模块

在Adobe Workfront Fusion场景中，您可以自动使用Adobe Firefly Audio and Video的工作流，并将其连接到多个第三方应用程序和服务。

如果需要有关创建方案的说明，请参阅[创建方案：项目索引](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md)下的文章。

有关模块的详细信息，请参阅[模块：文章索引](/help/workfront-fusion/references/modules/modules-toc.md)下的相关文章。

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

在使用Adobe Firefly Audio and Video连接器之前，必须确保满足以下先决条件：

* 您必须拥有有效的Adobe Firefly Audio and Video帐户。

## 创建与Adobe Firefly Audio and Video的连接

要为您的Adobe Firefly音频和视频模块创建连接，请执行以下操作：

1. 在任意模块中，单击“连接”框旁边的&#x200B;**[!UICONTROL 添加]**。

1. 填写以下字段：

   <table style="table-layout:auto"> 
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
      </col>
      <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
      </col>
      <tbody>
        <tr>
        <td role="rowheader">连接名称</td>
        <td>
          <p>输入此连接的名称。</p>
        </td>
        </tr>
        <tr>
        <td role="rowheader">环境</td>
        <td>选择您要连接到生产环境还是非生产环境。</td>
        </tr>
        <tr>
        <td role="rowheader">类型</td>
        <td>选择连接服务帐户还是个人帐户。</td>
        </tr>
        <tr>
        <td role="rowheader">客户端 ID</td>
        <td>输入您的Adobe客户端ID。 可在Adobe Developer Console的“凭据详细信息”部分找到此项。</td>
        </tr>
        <tr>
        <td role="rowheader">客户端密钥</td>
        <td>输入您的Adobe客户端密钥。 可在Adobe Developer Console的“凭据详细信息”部分找到此项。</td>
        </tr>
      </tbody>
    </table>

1. 点击&#x200B;**[!UICONTROL 继续]**&#x200B;保存连接并返回模块。


## Adobe Firefly音频和视频模块及其字段

配置Adobe Firefly Audio and Video模块时，Workfront Fusion会显示以下列出的字段。 除此以外，还可能会显示其他Adobe Firefly音频和视频字段，具体取决于应用程序或服务中的访问级别等因素。 模块中的加粗标题表示必填字段。

如果您看到字段或功能上方的映射按钮，可使用它为该字段设置变量和函数。 有关详细信息，请参阅[将信息从一个模块映射到另一个模块](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md)。

![映射切换](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### 操作

* [描述模板](#describe-template)
* [音频或视频配音](#dub-audio-or-video)
* [从文本或音频生成头像视频](#generate-avatar-video-from-text-or-audio)
* [从文本生成语音](#generate-speech-from-text)
* [重新设置视频帧](#reframe-video)
* [渲染模板](#render-template)
* [转录媒体](#transcribe-media)

#### 描述模板

此操作模块分析MOGRT（视频模板）文件并返回可编辑控件、字体、图像、音频、视频和其他受支持值的清单。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与Adobe Firefly的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>输入或映射指向输入模板文件的预签名URL。</td> 
  </tr>
 </tbody> 
</table>

#### 音频或视频配音

此操作模块生成配音音频或视频。 还可以在生成的视频中包含唇同步。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与Adobe Firefly的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">Dub type</td> 
   <td>选择您要生成音频还是视频配对。</td> 
  </tr>
  <tr> 
   <td role="rowheader">预签名URL</td> 
   <td>输入或映射模块将用于输入的预签名URL。<p>Firefly Audio and Video接受以下媒体存储域</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">媒体类型</td> 
   <td>选择输入文件的媒体类型</td> 
  </tr>
  <tr> 
   <td role="rowheader">唇同步</td> 
   <td>选择是否为视频输出生成高品质合成唇同步。</td> 
  </tr>
  <tr> 
   <td role="rowheader">目标区域设置代码</td> 
   <td>对于要添加的每个区域设置代码，单击<b>添加项</b>并选择区域设置代码。</td> 
  </tr>
  <tr> 
   <td role="rowheader">成绩单</td> 
   <td>对于每个要添加的成绩单，单击<b>添加项</b>，然后输入或映射该成绩单的预签名URL。</td> 
  </tr>
 </tbody> 
</table>

#### 从文本或音频生成头像视频

该操作模块根据您提供的转录或音频文件生成头像视频。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与Adobe Firefly的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">URL</td> 
   <td>输入或映射模块将用于输入的预签名URL。   </td> 
  </tr>
  <tr> 
  <tr> 
   <td role="rowheader">区域设置代码</td> 
   <td>选择表示要在结果中使用的语言的区域设置代码。</td> 
  </tr>
   <td role="rowheader">媒体类型(Source)</td> 
   <td>选择输入文件的媒体类型</td> 
  </tr>
  <tr> 
   <td role="rowheader">头像</td> 
   <td>选择要用于所生成视频的头像。</td> 
  </tr>
  <tr> 
   <td role="rowheader">媒体类型</td> 
   <td>为生成的视频选择输出媒体类型。</td> 
  </tr>
  <tr> 
   <td role="rowheader">宽度</td> 
   <td>输入或映射所生成视频的宽度。</td> 
  </tr>
  <tr> 
   <td role="rowheader">高度</td> 
   <td>输入或映射所生成视频的高度。</td> 
  </tr>
  <tr> 
   <td role="rowheader">背景</td> 
   <td>选择要用于所生成视频的背景类型：
   <ul>
   <li><b>视频</b>：输入或映射背景视频的URL。</li> 
   <li><b>图像</b>：输入或映射背景图像的URL。</li>
   <li><b>颜色</b>：输入或映射要用于视频背景的颜色的十六进制值。</li> 
   </ul>
   </td>
  </tr>
 </tbody> 
</table>

#### 从文本生成语音

该操作模块从成绩单生成语音。 您可以提供纯文本成绩单或预签名URL。 响应中包含用于跟踪作业的作业ID和状态URL。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与Adobe Firefly的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">脚本</td> 
   <td>选择要提供的脚本类型。
   <ul>
   <li><b>文本</b>：输入源文本或将源文本映射到文本字段。</li>
   <li><b>文本文件</b>：在URL字段中输入或映射文本文件的URL。</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">区域设置代码</td> 
   <td>选择表示要在结果中使用的语言的区域设置代码。</td> 
  </tr>
  <tr> 
   <td role="rowheader">媒体类型</td> 
   <td>这应为<code>text/plain</code>。</td> 
  </tr>
  <tr> 
   <td role="rowheader">语音</td> 
   <td>选择要使用的声音。 可用的声音来自Adobe Firefly声音目录。</td> 
  </tr>
  <tr> 
   <td role="rowheader">输出</td> 
   <td>这应为<code>audio/wav</code>。</td> 
  </tr>
 </tbody> 
</table>

#### 重新设置视频帧

此模块会重新构建您提供的媒体。 媒体通过预签名的URL提供。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与Adobe Firefly的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">预签名URL</td> 
   <td>输入或映射模块将用于输入的预签名URL。<p>Firefly Audio and Video接受以下媒体存储域</p>
   <ul>
   <li>adobe.io</li>
   <li>frame.io</li>
   <li>amazonaws.com</li>
   <li>windows.net</li>
   <li>dropboxusercontent.com</li>
   <li>drive.google.com</li>
   <li>cloudfront.net</li>
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">场景编辑检测</td> 
   <td>选择是否在重新构建框架之前应用场景编辑检测。 </td> 
  </tr>
  <tr> 
   <td role="rowheader">焦点</td> 
   <td>对于要添加的每个焦点，单击<b>添加项</b>并输入焦点的关键字标识符。</td> 
  </tr>
  <tr> 
   <td role="rowheader">叠加</td> 
   <td>对于要添加的每个叠加，单击<b>添加项</b>并输入叠加信息。
   <ul>
   <li><b>Source</b>：输入或映射指向源媒体的URL。</li> 
   <li><b>开始时间</b>：输入或映射开始时间。</li>
   <li><b>持续时间</b>：输入或映射叠加的持续时间。</li> 
   <li><b>宽度</b>：输入或映射缩放叠加图的宽度。</li> 
   <li><b>高度</b>：输入或映射缩放叠加的高度。</li> 
   <li><b>锚点</b>：为叠加选择锚点。</li> 
   <li><b>偏移量X</b>：输入或映射叠加图的水平偏移量。</li> 
   <li><b>偏移量Y</b>：输入或映射叠加图的垂直偏移量。</li> 
   <li><b>重复</b>：输入<code>loop</code>以导致GIF循环。</li> 
   </ul>
   </td> 
  </tr>
  <tr> 
   <td role="rowheader">媒体格式</td> 
   <td>选择重新设置帧的视频格式。</td> 
  </tr>
  <tr> 
   <td role="rowheader">Sidecar格式</td> 
   <td>选择其他元数据的格式。</td> 
  </tr>
  <tr> 
   <td role="rowheader">节目</td> 
   <td>若要添加其他节目，请单击“添加项目”<b></b>并输入节目信息。<!--add additional info--></td> 
  </tr>
 </tbody> 
</table>

#### 渲染模板

此模块通过应用覆盖和导出预设来呈现一个或多个视频变体。



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与Adobe Firefly的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">输入模板文件URL</td> 
   <td>输入或映射表示要呈现的模板的预签名URL。</td> 
  </tr>
  <tr> 
   <td role="rowheader">字体</td> 
   <td>对于要添加的每个字体，单击<b>添加项</b>并输入该字体的postscript名称和字体文件URL。</td> 
  </tr>
  <tr> 
   <td role="rowheader">当缺少字体时</td> 
   <td>选择是要使渲染失败，还是在缺少字体时使用默认字体。</td> 
  </tr>
  <tr> 
   <td role="rowheader">媒体资产</td> 
   <td>对于要添加的每个媒体资产，单击<b>添加项目</b>，然后输入或映射表示该资产的预签名URL。</td> 
  </tr>
  <tr> 
   <td role="rowheader">导出预设</td> 
   <td>对于要添加的每个导出预设，单击<b>添加项</b>并选择视频预设，然后输入或映射表示预设的预签名URL。</td> 
  </tr>
  <tr> 
   <td role="rowheader">变体</td> 
   <td>对于要添加的每个变体，单击<b>添加项</b>并输入变体的详细信息。 您必须为至少一个变体输入详细信息。<!--add data here--></td> 
  </tr>
  <tr> 
   <td role="rowheader">输出定义</td> 
   <td>通过单击<b>添加项</b>并选择要使用的添加的变体和预设，然后添加文件名来定义输出。 变量和预设的索引为0（变量列表中的第一项为0，下一项为1，依此类推）。</td> 
  </tr>
 </tbody> 
</table>

#### 转录媒体

此模块可转录音频或视频。



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">连接</td> 
   <td>有关创建与Adobe Firefly的连接的说明，请参阅本文中的<a href="#create-a-connection-to-adobe-firefly" class="MCXref xref" >创建与Adobe Firefly的连接</a>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">转录类型</td> 
   <td>选择您要转录音频还是视频。   </td> 
  </tr>
  <tr> 
   <td role="rowheader">预签名URL</td> 
   <td>输入或映射模块将用于输入的预签名URL。   </td> 
  </tr>
  <tr> 
  </tr>
   <td role="rowheader">媒体类型 </td> 
   <td>选择输入文件的媒体类型</td> 
  </tr>
  <tr> 
   <td role="rowheader">目标区域设置代码</td> 
   <td>对于要添加的每个区域设置代码，单击<b>添加项</b>并选择表示要在结果中使用的语言的区域设置代码。</td> 
  <tr> 
   <td role="rowheader">题注格式</td> 
   <td>输入<code>SRT</code>以包含字幕，如果不想要字幕，则保留为空。</td> 
  </tr>
 </tbody> 
</table>



