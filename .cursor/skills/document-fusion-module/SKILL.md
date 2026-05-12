---
name: document-fusion-module
description: 记录新的Adobe Workfront Fusion连接器模块，方法是：将其添加到help/workfront-fusion/references/apps-and-modules/下的相应连接器文章中。 当用户要求添加、记录或描述新的Fusion模块时，或者当用户提供Fusion模块配置面板的屏幕截图并且希望更新相应的文章时，可使用。
source-git-commit: 976db79104d226a16a35dc04e8c8cb111eb745db
workflow-type: tm+mt
source-wordcount: '1609'
ht-degree: 0%

---


# 记录Fusion连接器模块

使用此技能向Workfront Fusion Connector文章添加一个或多个新模块（例如，`adobe-firefly-modules.md`、`adobe-photoshop-modules.md`、`azure-dev-ops.md`）。

## 所需输入（每个模块）

在填充任何模块的字段之前，用户&#x200B;**必须**&#x200B;提供以下所有内容。 如果有任何文件丢失，请在继续操作之前停止并询问文件。

1. **模块名称** — 与Fusion UI中显示的名称完全相同（例如，`Generate adaptive composite`）。
2. **连接器文章路径** — 代理找到此路径并向用户确认（请参阅阶段1）。
3. **基础API操作的API URL**。 这是必需的，以便可以根据API规范交叉引用每个字段的目的。
4. **标准视图中模块配置面板的屏幕截图** （`Show advanced settings` **未选中**）。
5. **高级视图中模块配置面板的屏幕截图** （`Show advanced settings` **选中**），或显示模块没有高级字段的明确声明。

## 工作流

这是一个多阶段的过程。 步调很重要 — 与&#x200B;*用户合作，而不是在他们之前*。 确认每个阶段边界的进度，并随时接受更正。

### 第1阶段 — 确定工作范围

1. **询问这是一个模块还是多个模块**： *&quot;您是否在向连接器文章中添加单个模块或多个模块？&quot;*

2. **提前收集每个模块名称**，根据答案：
   - **单个模块**：询问其在Fusion UI中显示的确切名称。
   - **多个模块**：一次询问所有名称，或者询问列出这些名称的连接器的屏幕快照（例如，Fusion中的连接器概述屏幕，其中显示每个模块的图块标签）。 无论如何，都以每个要添加的新模块的确认列表来结束此步骤。

3. **根据模块隐含的连接器名称搜索`help/workfront-fusion/references/apps-and-modules/`，以自行找到连接器文章**。 使用`Glob`或`Grep`工具。

4. **使用用户**&#x200B;确认文章路径： *&quot;根据模块名称，这应该在`help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-firefly-modules.md`之内。 对吗？&quot;*

5. **阅读连接器文章**&#x200B;以了解其现有结构和约定。 请注意：
   - 标题样式（句子大小写通常为`### Module name`）
   - 现有模块排序（通常按字母顺序）
   - `Connection`行的措辞
   - 嵌套字段的写入方式（如`Image > Source`）
   - 任何现有的脚注或注释约定

### 阶段2 — 将每个模块的占位符放在前面

即使只有一个新模块，这也可以为用户提供一个清晰的可视化路线图。 如果有多个新模块，请立即放置所有模块。

对于每个新模块，在字母位置插入占位符部分：

```markdown
### Module name

<!-- PLACEHOLDER: Add description of the Module name module here. -->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>For instructions on creating a connection to [!DNL Connector Name], see <a href="#create-a-connection-to-connector-name" class="MCXref xref" >Create a connection to [!DNL Connector Name]</a> in this article.</td> 
  </tr> 
  <!-- PLACEHOLDER: Add field rows for the Module name module here. -->
 </tbody> 
</table>
```

向用户显示已添加的占位符列表（例如，“添加了以下占位符：生成自适应复合、使用图像5生成图像、生成精确复合、生成视频”）。 然后询问以下哪项开始：*“您想从哪项开始？”*

### 阶段3 — 每模块文档循环

对于每个模块，请先完全完成此循环，然后再转到下一个模块：

#### 3a. 获取API URL

向用户询问API URL： *&quot;请共享`<module name>`的基础API操作的API URL。&quot;*

如果您拥有：
- 在URL上尝试`WebFetch`。
- 如果页面为空/JS渲染（与Adobe Developer文档相同），请查找相关的功能指南页面（通常位于`.../guides/how-tos/...` URL）并获取它。
- 如果仍然不走运，则回退到`WebSearch`以获取操作名称。

将您学到的任何内容用作以后字段描述的背景上下文。 不要将其转储到用户上；只需简短确认即可： *&quot;已获取API上下文 — 已准备好标准视图屏幕截图。&quot;*

#### 3b. 获取标准视图屏幕截图

询问： *&quot;请取消选中`Show advanced settings`**并共享模块配置面板的屏幕快照**。 完成标准字段后，我将请求提供高级视图，但不要发送该视图。”*

#### 3c. 记录标准字段

使用标准视图屏幕截图，从上到下捕获每个可见字段。 对于每个字段：

1. 使用字段的精确UI标签作为行标题。 对于分组字段，与` > `联接：

   ```
   [!UICONTROL Background > Image > Source]
   ```

2. 阅读屏幕快照中字段下方的帮助程序文本（灰色/黄色描述）。 将其用作说明的基础。
3. 交叉引用步骤3a中的API上下文以确定字段表示的内容（例如，`background.fillAreaMask`是“将放置对象的背景区域”）。
4. 通过将&#x200B;**什么字段**（来自API）与&#x200B;**如何提供该字段**（来自UI帮助程序文本和字段类型）组合来编写描述。

跳过屏幕快照中不可见的任何字段，即使API支持此字段。 不要发明字段。

设置好标准字段后，向用户简要概述这些字段（例如“添加的标准字段：连接、提示、宽高比……”），然后移至步骤3d。

#### 3d 获取高级视图屏幕截图

询问： *&quot;现在，请与`Show advanced settings`**选中**&#x200B;共享模块配置面板的屏幕快照。 如果模块没有高级字段，请说，我们将跳过这一步。”*

#### 3e. 记录高级字段

使用高级视图屏幕截图：

1. 识别&#x200B;*不是*&#x200B;的字段已存在于标准视图中 — 这些是高级字段。
2. 对于每个高级字段，请执行步骤3c中的相同描述过程。
3. 将`*`附加到`<td role="rowheader">`内的字段名称：

   ```html
   <td role="rowheader">[!UICONTROL Seeds]*</td>
   ```

4. 在结束`</table>`后，在其自己的行中添加此脚注：

   ```markdown
   * These fields are advanced fields, and do not display unless you select **[!UICONTROL Show advanced settings]**.
   ```

如果用户说模块没有高级字段，请完全跳过步骤3d和3e。

#### 3f. 草稿模块描述

现在（不是更早版本），请根据API上下文和字段含义，将部分顶部的描述占位符替换为单句草稿。 始终将其作为草稿提供给用户审阅：

> *“我起草了此描述： &#39;...&#39;。 想要使用它、编辑它或替换它吗？&quot;*

#### 3g。 每模块总结

向用户提供模块已记录字段的最终摘要（标准+高级），并显示任何未完成的问题：

- 屏幕截图中有没有田野被切断？
- 模块描述是否可接受？
- 是否应将任何内容标记为已弃用或值得注意？

等待确认，然后再宣布模块已完成。 然后询问：*“准备好继续下一模块？”* （或“我们已经完成了此连接器文章。”）

### 第4阶段 — 最终验证

在记录完所有模块后，请针对每个模块运行以下核对清单：

- [ ]模块标题为`### ` (H3)且使用句子大小写。
- [ ]模块按与其同级模块相关的字母顺序显示。
- [ ]第一行是`Connection`，使用标准连接链接措辞。
- [ ]每个记录的字段在用户屏幕截图中都可见。
- [ ]高级字段标有`*`，并且表下存在单个脚注。
- [ ]没有单独从API创建的字段。
- [ ] Source下拉列表描述使用精确的UI选项标签（请参阅下面的“Source字段约定”）。
- [ ]模块描述是一个单句摘要，用于描述该模块的功能。

## Source字段惯例

Fusion Connectors中的图像源字段通常显示一个包含两个选项的下拉列表。 **使用用户屏幕快照中显示的确切标签** — 不同代的模块使用不同的措辞：

| 如果下拉菜单显示…… | 使用此格式 |
|---|---|
| **上传图像**&#x200B;和&#x200B;**图像URL**（较新的模块） | `<ul><li><b>Upload Image</b><p>Upload the image, or map the image file from a previous module.</p></li><li><b>Image URL</b><p>Enter or map the URL of the image.</p></li></ul>` |
| **文件**&#x200B;和&#x200B;**预签名URL**（较旧的模块） | `<ul><li><b>File</b><p>Select a source file from a previous module, or map the source file's reference image file name and reference image file.</p></li><li><b>Presigned URL</b><p>Enter or map the URL of the source image.</p></li></ul>` |

如果屏幕快照未显示打开的下拉菜单选项，请要求用户共享它们。

## 字段描述样式

- 匹配同一文章中现有模块条目的声音和结构。
- 简短描述：每个字段通常只用一个或两个句子就够了。
- 为从其他字段引用的任何UI字段名称使用`[!UICONTROL ...]`标记。
- 对文本值(`<code>en-US</code>`， `<code>0.0</code>`)使用`<code>...</code>`。
- 对于数字范围字段，请明确指出允许的范围： *&quot;输入介于0和1之间的数字……&quot;*.
- 对于包含离散选项的下拉列表，请以`<ul>`的形式枚举它们，其中`<b>Option</b>`后跟`<p>`说明。

## 常见字段和推荐的描述

重复使用这些内容以实现模块间的一致性：

**种子**（当字段通过“添加”项允许多个种子值时）：
> 单击&#x200B;**添加项**&#x200B;以添加种子值，然后输入或映射整数。 每个变体使用一个种子。 如果同时提供了种子值和变体数，则种子值的计数必须匹配&#x200B;**变体数**&#x200B;值。

**变体数** （将范围替换为屏幕快照中的实际范围）：
> 请输入介于[分钟]和[最大]之间的数字。 模块生成此数量的[输出类型]变量。

**限制**（标准Fusion执行周期限制；仅在屏幕快照中可见时包含）：
> 输入或映射您希望模块在一个执行周期内使用的最大结果数。

**区域设置**：
> 输入或映射语言和区域代码以根据特定的国家/地区和语言定制生成的内容。 必须以ISO 639-1语言代码和ISO 3166-1区域提供区域设置。 示例：`en-US`

## 随时接受更正

用户可以在工作流中更正先前的工作 — 种子措辞、下拉标签、字段定位、高级/标准拆分等。将任何更正都视为权威性更正并且无需进行反击即可进行更新。 在修正之后，简要总结了更改的内容。

如果用户引入了新的约定中间流程（例如，“让我们使用`*`标记高级字段并添加脚注”），请将其用于会话的其余部分，并将其逆向应用于已记录的任何模块。

## 如果信息有冲突，该怎么办

当API规范和UI存在分歧时（这种情况经常出现）：

1. **信任UI**，因为这是用户在Fusion中实际看到的内容。
2. **请注意您回复用户的差异**，以便他们决定是否进一步调查。
3. **不要在文章正文中创建说明** — 请如实说明UI中的内容。

如果用户的两个屏幕截图相互矛盾（例如，一个屏幕截图显示`Blend`，另一个屏幕截图显示同一模块的`Harmonization`），请停止并询问哪个屏幕截图是正确的，然后再进行编写。 通过交叉引用API规范，识别哪个屏幕快照可能属于不同的模块。
