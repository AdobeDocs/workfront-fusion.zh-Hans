---
title: 项目数据类型
description: 您的Adobe Workfront Fusion方案可以在捆绑包中包含下面列出的项目类型。
author: Becky
feature: Workfront Fusion
exl-id: 3ad65959-5c19-4727-bc9d-4ff1d238ad8b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 1%

---

# 项目数据类型

可在捆绑包中包含下面列出的项目类型。

有关Workfront Fusion允许相互转换的项目类型的信息，请参阅[类型强制](/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md)。

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>文本</p> </td> 
   <td> <p>最常见的项目类型。 对于某些文本项，Adobe Workfront Fusion检查是否满足允许的最大或最小长度，或者该项是否执行格式验证（电子邮件、URL或文件名）。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>数值</p> </td> 
   <td> <p>对于某些数字项，Workfront Fusion可能会验证指定范围（允许的最小值或最大值）的输入。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>布尔值（是/否）</p> </td> 
   <td> <p>此类型用于仅具有两个可能值的项目：true或false。 </p> <p>设置模块时，布尔类型可以两种不同的形式出现：</p> 
    <ul> 
     <li> <p>如果字段是必填字段，且必须填写，则会显示必填复选框。</p> <p> <img src="assets/boolean-checkbox-350x158.jpg" style="width: 350;height: 158;"> </p> </li> 
     <li> <p>可留空的可选字段将显示为选择框，允许从三个值中进行选择：<code>Yes</code>、<code>No</code>和<code>Not defined</code>（默认值）。</p> <p> <img src="assets/boolean-convert-file-350x129.jpg" style="width: 350;height: 129;"> </p> </li> 
    </ul> <p>如果需要将值映射到其他模块中的项，可以单击<strong>[!UICONTROL 映射]</strong>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>日期</p> </td> 
   <td> <p>日期以ISO 8601日期格式输入，例如<code>2015-09-18T11:58Z</code>。 您可以在配置文件设置中更改时区。 </p> <p>如果单击需要日期的字段，则模块设置中会显示一个弹出日历。 某些项目不需要时间。</p> <p>日期项目的值使用在您的配置文件中选择的本地和Web时区进行格式化。 将鼠标悬停在日期项上可以显示日期项值的ISO 8601版本。</p> <p>注意：如果ISO值未显示，则该项目可能是文本，而不是日期。</p> <p>时间以<code>hours:minutes:seconds</code>格式输入，例如<code>14:03:52</code>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>缓冲区（二进制数据）</p> </td> 
   <td> <p>文件内容通常作为缓冲类型内容（图像内容、视频文件等）发送。 在某些情况下，文本数据包含在此类型中（例如，文本文件）。 Workfront Fusion能够自动将二进制代码中的文本数据转换为文本，并将文本转换为二进制代码中的文本数据。 有关详细信息，请参阅<a href="/help/workfront-fusion/create-scenarios/map-data/map-files.md" class="MCXref xref">映射文件</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>收藏集</p> </td> 
   <td> <p>收藏集是由多个子项目组成的项目。 电子邮件中的“发件人”项目是集合的一个示例：它包含发件人姓名（文本类型）和发件人电子邮件地址（文本类型）。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>选择（菜单）</p> </td> 
   <td> <p>配置模块设置时，您可以从多个相同类型的项目中进行选择。 例如，[!DNL Dropbox]模块的设置中的文件夹选择菜单。 </p> <p>设置模块时，“选择”菜单可以两种形式出现：</p> <p> <p>如果可以进行多项选择，则会显示多个包含复选框的项目。</p> <p> <img src="assets/image-kb-type-list-multi-350x232.jpg" style="width: 350;height: 232;"> </p> </p> <p>如果只有一个选项，则会显示下拉菜单。</p> <p> <img src="assets/select-menu-dropdown-350x130.jpg" style="width: 350;height: 130;"> </p> <p>如果需要映射另一个模块中的项，请使用<strong>映射</strong>按钮。 此按钮将打开文本字段而不是选择菜单。 有关映射的详细信息，请参阅<a href="/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md" class="MCXref xref">映射概述</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>数组</p> </td> 
   <td> <p>您可以使用数组类型处理相同类型的多个值，包括集合。 [!UICONTROL Email]模块就是一个例子：它们返回一系列附件，每个附件都包含名称、内容、大小等。 有关详细信息，请参阅<a href="/help/workfront-fusion/create-scenarios/map-data/map-an-array.md" class="MCXref xref">映射数组或数组元素</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>验证</p> </td> 
   <td> <p>Workfront Fusion可能会对每种类型的项目执行验证。 如果项目未通过验证，则模块将因数据错误而停止处理。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/errors/error-processing.md" class="MCXref xref">错误类型</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>
