---
title: XML
description: 利用XML应用程序，可通过XML &amp；解析XML模块解析XML格式文本，并将其转换为捆绑包，以便其他模块可以使用该数据。 您还可以通过XML &amp；gt；创建XML模块将捆绑包转换为XML格式文本
author: Becky
feature: Workfront Fusion
exl-id: ab323361-cd04-4dcc-ab02-0fb468334fdb
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '1442'
ht-degree: 2%

---

# XML

通过[!UICONTROL XML]应用，您可以通过[!UICONTROL XML] > [!UICONTROL 解析XML]模块来解析XML格式的文本，并将其转换为捆绑包，以便其他模块可以使用该数据。 您还可以通过[!UICONTROL XML] > [!UICONTROL 创建XML]模块将捆绑包转换为XML格式文本

## 访问要求

+++ 展开以查看本文中各项功能的访问要求。

您必须具有以下权限才能使用本文中的功能：

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront包</td> 
   <td> <p>任何</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront许可证</td> 
   <td> <p>新增：标准</p><p>或</p><p>当前：工作或更高</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion许可证**</td> 
   <td>
   <p>无Workfront Fusion许可证要求</p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">产品</td> 
   <td>
   <p>新增：</p> <ul><li>选择或Prime Workfront包：您的组织必须购买Adobe Workfront Fusion。</li><li>Ultimate Workfront包：其中包含Workfront Fusion。</li></ul>
   <p>或</p>
   <p>当前：您的组织必须购买Adobe Workfront Fusion。</p>
   </td> 
  </tr>
 </tbody> 
</table>

有关此表中信息的更多详细信息，请参阅文档](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md)中的[访问要求。

有关[!DNL Adobe Workfront Fusion]许可证的信息，请参阅[[!DNL Adobe Workfront Fusion] 许可证](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md)。

+++

## 创建XML

[!UICONTROL XML] > [!UICONTROL 创建XML]模块将捆绑包转换为XML格式文本。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Data structure]</p> </td> 
   <td> <p>数据结构描述生成的XML的结构。 如果要创建的XML示例，可以使用该示例生成数据结构：</p> 
    <ol> 
     <li value="1">单击<strong>[！UICONTROL Add]</strong>按钮。</li> 
     <li value="2">单击<strong>[！UICONTROL生成器]</strong>按钮。</li> 
     <li value="3">将XML示例复制并粘贴到示例数据字段中。</li> 
     <li value="4">单击<strong>[！UICONTROL保存]</strong>按钮。</li> 
     <li value="5">验证是否已成功生成数据结构。</li> 
     <li value="6">单击<strong>[！UICONTROL保存]</strong>以保存数据结构。</li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL根元素名称]</td> 
   <td>输入XML根元素的名称。 默认值为<code>root</code>。</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Doctype系统ID]</td> 
   <td>输入要在<code>!DOCTYPE SYSTEM</code>声明中使用的文件名</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL Doctype公共ID]</td> 
   <td>输入要在<code>!DOCTYPE PUBLIC</code>声明中使用的文件名</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL带Xml声明]</td> 
   <td>启用此选项可删除XML声明<code>&lt;?xml ... ?&gt;</code>和<code>&lt;!DOCTYPE ... &gt;</code>，并仅保留XML根元素及其内容。</td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**

典型用例是将数据从[!DNL Google] >电子表格转换为XML。

1. 将[!DNL Google Sheets] > [!UICONTROL 选择方案中的行]模块以获取数据。 设置模块以从[!DNL Google]电子表格中检索行。 将&#x200B;**[!UICONTROL 返回的最大行数]**&#x200B;设置为一个较小的数字，但大于一个以用于测试目的（例如，3）。 执行[!DNL Google Sheets]模块，方法是右键单击该模块并选择“**[!UICONTROL 仅运行此模块]**”。 验证模块的输出。
1. 在[!DNL Google Sheets]模块之后连接[!UICONTROL 数组汇总]模块。 在模块设置的&#x200B;**[!UICONTROL Source节点]**&#x200B;字段中选择[!DNL Google Sheets]模块。 请暂时保留其他字段。
1. 在[!UICONTROL 数组聚合器]模块之后连接[!UICONTROL XML] > [!UICONTROL 创建XML]模块。

   模块的设置需要一个描述XML输出结构的数据结构。 单击&#x200B;**[!UICONTROL 添加]**&#x200B;按钮以打开数据结构设置。 创建此数据结构的最简单方法是从XML示例中自动生成此数据结构。

1. 单击&#x200B;**[!UICONTROL 生成器]**&#x200B;按钮并将XML示例粘贴到[!UICONTROL 示例数据]字段：

   ![示例数据字段](/help/workfront-fusion/references/apps-and-modules/assets/sample-data-field-350x146.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

   Data structure中的Specification字段现在包含生成的结构。
1. 将数据结构的名称更改为更具体的名称，然后单击&#x200B;**[!UICONTROL 保存]**。

   与root数组属性对应的字段在JSON模块的设置中显示为可映射字段。
1. 单击该字段旁边的&#x200B;**[!UICONTROL 映射]**&#x200B;按钮，并将[!UICONTROL 数组汇总]输出中的`Array[]`项映射到它：
1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;以关闭XML模块的设置。
1. 打开[!UICONTROL 数组汇总]模块的设置。 将&#x200B;**[!UICONTROL 目标结构]**&#x200B;从“自定义”更改为与父XML元素对应的XML模块字段。将[!DNL Google Sheets]模块中的项映射到相应的字段。
1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;关闭阵列聚合器模块的设置。
1. 运行方案。

   XML模块输出正确的XML文件。

1. 打开[!DNL Google Sheets]模块的设置，并增加[!UICONTROL 返回的最大行数]数值，使其大于电子表格中的行数，以便处理所有数据。

   生成的XML可以保存到[!DNL Dropbox]、通过电子邮件作为附件发送、通过FTP上传到服务器等等。

>[!ENDSHADEBOX]

### 添加XML属性

如果要向复杂节点（将包含其他节点的节点）添加属性，则必须为自定义数据结构中的复杂注释添加名为`_attributes`的集合。 此集合将映射到节点属性。 如果要向文本节点添加属性（例如： `<node attr="1">abc</node>`），则必须为自定义数据结构中此节点的属性添加集合`_attributes`，并为节点值添加文本属性`_value`。

```
{
   "name": "node",
   "type": "collection",
   "spec": [
      {
         "name": "_attributes",
         "type": "collection"
         "spec": [
            {
               "name": "attr1",
               "type": "text"
            }
         ]
      },
      {
         "name": "_value",
         "type": "text"
      }
   ]
}
```

## [!UICONTROL 分析XML]

[!UICONTROL XML] > [!UICONTROL 解析XML]模块解析XML格式文本并输出包含从XML提取的所有信息的单个包。

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL Data structure]</p> </td> 
   <td> <p>数据结构描述了XML的结构，以使模块的输出在映射面板中可用于以下模块。</p> <p>如果要解析的XML的示例，可以使用该示例生成数据结构：</p> 
    <ol> 
     <li value="1">单击<strong>[！UICONTROL Add]</strong>按钮。</li> 
     <li value="2">单击<strong>[！UICONTROL生成器]</strong>按钮。</li> 
     <li value="3">将XML示例复制并粘贴到<strong>[！UICONTROL示例数据]</strong>字段中。</li> 
     <li value="4">单击<strong>[！UICONTROL保存]</strong>。</li> 
     <li value="5">验证是否已成功生成数据结构。</li> 
     <li value="6"> <p>单击<strong>[！UICONTROL Save]</strong>按钮以保存数据结构。</p> <p>可跳过步骤2-5以提供空的数据结构。 如果数据结构为空，则在至少执行一次模块后，映射面板中才会提供模块的输出。</p> </li> 
    </ol> <p>有关详细信息，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md" class="MCXref xref">数据结构</a>。</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[！UICONTROL保留数字为文本]</td> 
   <td>启用此选项以确保数字保持为文本（字符串）值。 否则，数字将转换为数字值。</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[！UICONTROL XML]</p> </td> 
   <td> <p>输入或映射要解析的XML格式文本。</p> <p>如果使用公式，请确保其结果值类型是（或可以自动强制到）[！UICONTROL Text]数据类型。 </p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/if-you-use-a-formula-350x164.png" style="width: 350;height: 164;"> </p> <p>如果结果值类型为[！UICONTROL Buffer] （二进制数据），则使用<code>toString()</code>函数将其转换为Text数据类型。 有关详细信息，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref">类型强制</a>和<a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">项目数据类型</a>。</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!BEGINSHADEBOX]

**示例：**

要从URL下载XML文件并解析其内容，请执行以下操作：

1. 创建新方案。
1. 添加[!UICONTROL HTTP] > [!UICONTROL 获取文件]模块
1. 打开模块的配置，并按照以下方式对其进行配置：

   **URL**： XML文件的URL （如`https://siftrss.com/f/rqLy05ayMBJ`）

   XML文件的![URL示例](/help/workfront-fusion/references/apps-and-modules/assets/url-of-xml-file-350x184.png)

1. 单击&#x200B;**[!UICONTROL 确定]**&#x200B;保存并关闭模块的配置。
1. 添加[!UICONTROL XML] > [!UICONTROL 分析XML]模块，在[!UICONTROL HTTP] > [!UICONTROL 获取文件]模块后连接该模块，并按如下方式对其进行配置：

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[！UICONTROL Data structure]</td> 
      <td> 
       <ol> 
        <li value="1">单击<strong>[！UICONTROL Add]</strong>按钮。</li> 
        <li value="2">单击<strong>[！UICONTROL生成器]</strong>按钮。</li> 
        <li value="3">在Web浏览器中，打开新的选项卡或窗口。</li> 
        <li value="4">将第三步中使用的URL放入地址栏并获取XML文件。</li> 
        <li value="5">选择所有XML文本并将其复制到剪贴板中。</li> 
        <li value="6">关闭选项卡或窗口并返回方案。</li> 
        <li value="7">将复制的XML文本粘贴到示例数据字段中。</li> 
        <li value="8">单击<strong>[！UICONTROL保存]</strong>。</li> 
        <li value="9">验证是否已成功生成数据结构。</li> 
        <li value="10">单击<strong>[！UICONTROL保存]</strong>以保存数据结构。</li> 
       </ol> <p>可跳过步骤2至9以提供空的数据结构。 如果数据结构为空，则在至少执行一次模块后，映射面板中才会提供模块的输出。</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[！UICONTROL XML]</td> 
      <td> <p>将[！UICONTROL HTTP] &gt; [！UICONTROL Get a file]模块输出中的<code>Data </code>项映射到字段中。 使用<code>toString()</code>函数将其值从[！UICONTROL Buffer] (binary data)类型转换为[！UICONTROL Text]数据类型。</p> <p>您可以将公式的代码复制并粘贴到字段中： <code>&#123;&#123;toString(1.data)&#125;&#125;</code></p> <p>有关Buffer和Text数据类型的详细信息，请参阅<a href="/help/workfront-fusion/references/mapping-panel/data-types/item-data-types.md" class="MCXref xref">项数据类型</a>。</p> <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/paste-formula-code-350x99.png"> </p> </td> 
     </tr> 
    </tbody> 
   </table>

>[!ENDSHADEBOX]

### [!UICONTROL 正在分析XML属性]

默认情况下，[!UICONTROL XML] > [!UICONTROL 分析XML]模块将特殊集合`_attributes`中的特性作为具有这些特性的节点的子项放入。 如果节点是文本节点并且它有属性，则会添加两个特殊属性：属性为`_attributes`，节点的文本内容为`_value`。

>[!BEGINSHADEBOX]

**示例：**&#x200B;此XML：

```
<root attr="1">
<node attr="ABC">Hello, World</node>
</root>
```

将转换为此捆绑包：

![XML已转换为包](/help/workfront-fusion/references/apps-and-modules/assets/xml-converted-to-bundle.png)

>[!ENDSHADEBOX]

## 疑难解答：无法映射来自[!UICONTROL 分析XML]模块的数据

确保正确定义数据结构。 或者，您可以使用空数据结构并至少执行一次该模块以处理XML输入。
