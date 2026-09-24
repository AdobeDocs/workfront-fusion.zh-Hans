---
applyTo: "help/workfront-fusion/**"
source-git-commit: e3e28f86494207dd5e674a2882887d00da6a0c61
workflow-type: tm+mt
source-wordcount: '2352'
ht-degree: 1%
---

# Fusion场景编辑器UI重新设计 — 项目注释

> 此文件是保存的克劳德代码内存文件(`fusion-scenario-editor-redesign.md`)的同步副本，因此GitHub Copilot具有相同的上下文。 Claude的副本是事实的来源 — 无论何时更新，此文件都应更新以匹配相同的编辑/提交。 如果两者存在分歧，请信任克劳德内存文件，然后重新同步该文件。
>
> 这是限定范围的Copilot指令文件(`.github/instructions/*.instructions.md`)，不是存储库范围的`.github/copilot-instructions.md`，因此它仅在Copilot处理`help/workfront-fusion/`下的文件时应用，而不是在存储库中的每个请求时应用。

Becky正在许多文章中记录Fusion的场景编辑器UI重新设计（新体验与经典体验）。 这是&#x200B;**动态索引** — 每当拍摄新屏幕快照或确认新UI详细信息时更新它（而不只是附加），因此任何查看此工作的人（或任何助手）都可以回答“我们是否已经拥有X的屏幕快照/事实？” 而不重新衍生它。

分支`becky-updates-to-Fusion-scenario-editor`上发生工作。 主跟踪电子表格：`C:\Users\rebeccas\Desktop\Fusion scenario editor UI redesign - affected articles.xlsx`（工作表“受影响的文章”=每个文章的状态/优先级；工作表“功能比较”=经典vs — 新功能差异）。

标记这些文档中任何未确认内联内容的惯例：`<!-- BECKY CHECK ME: ... -->`位于正位置，从不作为可见标注。

## 屏幕快照清单（新体验）

通过绝对路径跨文章重用，而不是复制文件 — 例如`/help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/run-once-new.png`。

**`help/workfront-fusion/get-started-with-fusion/navigate-fusion/assets/`** （从`scenario-editor.md`重写 — 共享的UI Chrome图标，可随时随地重复使用）：
`run-once-new.png` （运行一次，仅图标）、`save-icon-new.png`、`notes-icon-new.png`、`scheduling-new.png` （底部栏计划切换+频率标签，例如“数据到达后立即”）、`auto-align-icon-new.png`、`scenario-editor-new.png` （完整画布）、`top-bar-new.png`、`controls-new.png`、`tools-new.png`、`favorites-new.png`、`ask-ai-new.png`、`canvas-navigation-new.png`、`search-modules-icon-new.png`、`find-and-replace-icon-new.png`、`snippets-icon-new.png`、`explain-flow-icon-new.png`、`export-blueprint-icon-new.png`、`export-as-headless-template-icon-new.png`、`import-blueprint-icon-new.png`、`previous-version-icon-new.png`、`devtool-icon-new.png`、`scenario-settings-icon-new.png`、`additional-controls-new.png`。

**`help/workfront-fusion/build-practice-scenarios/assets/`** （来自基本方案教程）：
`new-placeholder-module.png` （空画布占位符卡）、`new-connector-picker.png` （应用程序/服务选取器面板 — 左边的类别列表：收藏夹、所有应用程序、Adobe Workfront、Adobe Firefly Services、Adobe Creative &amp; Content、Adobe Cloud Services、创作AI、内置；搜索权限）、`new-renamed-module.png`、`new-map-toggle.png`、`new-map-id.png`、`new-execution-bubble.png`、`clock-icon-on-watch-record.png` （卡片上的模块级计划/时钟徽章）、`new-map-in-filter.png` （使用映射的项目ID条件设置筛选器窗口）、`new-mapped-update-record.png` （将ID映射到“更新记录”模块）、`new-text-binary-function.png` （“T”映射面板）， `new-module-output-icon.png` （星型映射面板选项卡）、`new-mapped-name-block.png` （`upper(...)`内的映射名称块）。

**`help/workfront-fusion/create-scenarios/add-modules/assets/`**:
`add-a-module-between-modules.png` （右键单击两个模块→菜单之间的路径：设置过滤器/取消链接/添加路由器/添加模块/添加注释 — 在路径上捕获的尚未包含过滤器/路由器，因此可能不是特定于路由或承载过滤器的路径上设置的完整选项）、`new-filter-setup-xml-example.png` （设置过滤器窗口，与`add-a-filter-to-a-scenario.md`中使用的File-Name-ends-with-.xml示例匹配）、`fallback-route-new.png` （设置过滤器窗口，选中并高亮显示备用路由复选框，用于router-module.md）、`new-filter-specific-user.png` （在标记为“特定用户”的路由路径上设置过滤器窗口， fallback复选框未选中，映射ID条件，橙色高亮显示框 — 用于router-module.md的“将过滤器添加到新体验中的路由”分步中）、`new-filter-specific-user-unmarked.png` （相同“特定用户”过滤器，无高亮显示框 — 用作router-module.md中if/else示例的`if`一半）、`new-not-specific-user-unmarked.png` （设置过滤器窗口，标记为“非特定用户”，已选中回退复选框，无条件，无高亮显示框 — 用作router-module.md中if/else示例的`else`一半）。

**尚未获得**：当前没有尚未完成的router-module.md。

**`help/workfront-fusion/create-scenarios/config-error-handling/assets/`**:
`new-add-error-handler-in-menu.png` （右键单击模块→设置上下文菜单：仅运行此模块/添加错误处理程序/重命名/克隆/复制模块/添加注释/复制映射/复制模块名称/应用程序元数据/删除模块 — 突出显示的“添加错误处理程序” — 用于error-handling.md）、`new-error-handling-directives.png` （从错误处理程序中打开应用程序/服务选取器，并选择专用的“错误处理”类别，在左侧面板中显示5个指令 — Break、Commit、Ignore、Resume、Rollback — 以及正常应用程序类别；用于error-handling.md — 重新用于模块和路由器添加的错误处理程序流），`new-error-handler-examples-with-numbers.png`错误处理程序层次结构演练的示例场景，根据`scenario-editor.md`的画布视图切换在&#x200B;**紧凑视图**&#x200B;中捕获 — 在error-handling.md中使用；将图像描述为紧凑视图以提高可读性)。

**`help/workfront-fusion/get-started-with-fusion/understand-fusion/assets/`**:
`new-scenario-example-unmarked.png` (提供源屏幕快照Becky，未标记 — 8模块Excel/Workfront用户同步方案：关注添加的用户→路由器→在Workfront中查找用户→路由器→ 3个分支[设置现有用户ID /在Workfront中创建新用户→设置新用户ID /获取用户ID变量→将用户ID上载到电子表格] — 方案与classic的`fusion-integration-example.png`和`fusion-glossary.md`的“方案”条目(`entire-scenario-blank.png`)相同；将此方案作为本示例中任何进一步标记的源)，`new-entire-scenario-scenario.png`，`new-scenario-trigger.png`，`new-scenario-module.png` `new-scenario-route.png` （全部通过红色高亮框从以上未标记的源派生 — 请参见每篇文章的注释以了解确切的框位置）、`new-scenario-connectors.png` （Becky提供的，新Experience连接器选取器中应用程序列表周围的红色框）、`new-scenario-segment.png` （Becky提供的，2个模块的Workfront Watch Events →转换对象区段，盒装，后跟未盒装的Microsoft 365电子邮件模块）、`new-fusion-automation-example.png` (Becky提供的，未标记，4个模块的Workfront仅示例 — 观看记录→获取项目信息→获取“分配给”→创建更新 — 场景与经典的`fusion-template-example.png`相同； `license-automation-vs-integration.md`的“Workfront Fusion for Work Automation示例”部分（如果Becky也希望包含该部分），`new-module.png` （来自`new-scenario-example-unmarked.png`的“在Workfront中查找用户”模块的单卡裁切，通过PowerShell/System.Drawing裁切 — 通常用于`fusion-glossary.md`的“模块”条目，无红色框）。

**`help/workfront-fusion/create-scenarios/config-scenarios-settings/assets/`**:
`new-scenario-settings-ex-1.png` (两模块示例场景 — 标记为关注传入请求的关注记录……” →标记为“将请求转化为项目”的杂项操作 — 用于configure-scenario-settings.md的Max-number-of-cycles示例)，`new-max-number-cycles.png` （在画布上打开的“方案设置”面板，通过“控件”区域中的齿轮图标打开，“最大周期数”字段突出显示值`1` — 用于configure-scenario-settings.md）。

## 确认了新体验UI事实（无需屏幕快照即可重复使用这些事实）

- 将鼠标悬停在模块的右边缘上，→出现&#x200B;**添加其他模块**&#x200B;按钮，单击该按钮→会打开应用程序/服务选取器（→添加第一个模块时相同的选取器）。
- 右键单击模块→设置上下文菜单（顺序）：仅运行此模块/**添加错误处理程序** /重命名/克隆/复制模块/添加注释/复制映射/复制模块名称/应用程序元数据/ **删除模块**。 两者均确认与Classic相同。
- 用左键单击两个模块之间的路径，→会直接打开&#x200B;**设置过滤器**&#x200B;窗口。 右键单击同一路径会打开其他（更完整）上下文菜单，而不是打开“设置过滤器”作为选项的菜单。
- 右键单击路径→ **添加路由器**&#x200B;和&#x200B;**添加模块**&#x200B;都是选项（请参阅`add-a-module-between-modules.png`）。
- **复制筛选器** / **粘贴筛选器**（通过右键单击已具有筛选器的路径）并以相同的方式工作 — 通过视觉方式重新设置样式以匹配新的卡片画布，但选项/标签相同。
- 单击路由器模块本身（不将鼠标悬停在其边缘）仍会添加一条新路由 — 确认保持不变。
- **订购路由**（右键单击“订购路由”→的路由器模块→拖放） — 已确认仍然有效，与Classic相同。
- **禁用路由**（右击路由的路径→“禁用路由”）和禁用路由可视化（灰色路径+标签上的禁用路由图标） — 已确认经典未更改。
- 路由器模块（“流量控制”>“路由器”）位于新选取器的&#x200B;**内置**&#x200B;类别下（也出现在“所有应用程序”下，但“内置”是要在说明中引用的类别）。
- 备用路由：与经典（在路由器模块本身上使用不同的箭头标记）不同，新体验通过在路由标签上以绿色文本显示&#x200B;**“备用”**&#x200B;来标记备用路由 — 此事实无需使用箭头标记屏幕截图。
- 错误处理程序路由：与经典（透明与实心圆）不同，新体验使用虚线和红色&#x200B;**“错误处理程序”**&#x200B;标签标记错误处理程序路由 — 此事实无需屏幕快照。
- 模块名称更正（实际的Workfront名称，不是来自旧草稿的拼写错误）： **“监视记录”**（单数，而不是“监视记录”），**“更新记录”**（不是“更新记录”）。
- 仍未确认并阻止`debug-a-scenario.md` +一些其他文章：**DevTool**&#x200B;是否从新Experience中删除（传闻中听到，尚无其他详细信息 — 请参阅“功能”比较表、“DevTool”行）。

## 为此重新设计而制定的内部惯例（适用于所有剩余条款）

- 完全并行复制：一个针对“……在新版（推荐）”的H2/H3树，另一个针对“……在经典版”的树，在任意位置使用`(Classic)`后缀以避免锚点冲突。 在现在具有2个以上子项的任何标题下添加mini-TOC。
- 在文章介绍&#x200B;**（不是自己的H2）的**&#x200B;末尾，将“新说明与经典说明”折叠为单个`>[!NOTE]`，重复使用此确切的措辞，并在链接后附加“在文章场景编辑器中”：
  > Workfront Fusion正在将场景编辑器转换为新Experience。 在此过渡期间，经典体验和新体验均可用，您可以随时在它们之间切换。 我们建议使用新Experience。 有关详细信息，请参阅文章场景编辑器中的[新体验和经典体验](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md#new-and-classic-experiences)。
- 新体验标题带有`(Recommended)`（例如`## Add a filter in the new experience (Recommended)`）。
- 真正与UI无关的内容（例如`add-a-module-basic.md`中的`?moduleId=` URL参数注释）不需要复制 — 使用判断，但如果不确定（移动注释时她之前推回，而不询问），请首先与Becky检查。
- 如果Becky确认体验之间的整个过程相同（不仅仅是不限用户界面注释），则根本不要将它拆分为新的/经典的H2/H3 — 使用新的体验措辞折叠为单个过程（例如`view-scenario-data-flow.md`的“在正在运行的情况下查看数据流”）。 缺省的假设仍然是，过程不同且需要拆分 — 仅在明确确认后折叠。
- 对于新视觉效果和传统视觉效果真正不同的单个说明性屏幕截图（不是完整的逐步过程），请勿选取一种或标记等待 — 首先显示两者：紧靠每个图像上方的纯文本标签行（“新体验”/“传统体验”），然后是新体验。 首先在周围的文章中提及新体验行为（例如“……在新体验中用X标记，或在经典体验中用Y标记”），而不仅仅是在图像标签中。 查看`view-scenario-data-flow.md`的运行/输出指示器。
- 将任何未确认的内容直接标记为`<!-- BECKY CHECK ME: ... -->` — 从不显示标注。
- 解析文章中的每个标记后，在跟踪电子表格的“受影响的文章”表（列G）中标记该行`Yes`。 如果仅解析了部分标志，则使用`In progress`。

## 每篇文章的状态（截至2026-09-22年）

完全完成（0标志，电子表格列G标记为`Yes`）： `scenario-editor.md`、`create-basic-scenario.md`、`add-trigger-to-basic-scenario.md`、`add-filter-basic-scenario.md`、`add-a-webhook-to-basic-scenario.md`、`use-function-to-build-practice-scenario.md`、`add-a-module-basic.md`、`add-a-filter-to-a-scenario.md`、`router-module.md`（行10）、`error-handling.md`（行15，已重建为新的/经典并行H3/H4树，用于“将错误处理程序添加到模块”和“……添加到路由器”）、`configure-scenario-settings.md`（行20 — 在跟踪电子表格中标记`Yes`，尚未更新）。 “打开场景设置”重新构建为新的/经典H2/H3拆分 — 新体验使用现有的`scenario-settings-icon-new.png`（控件区域，可能位于三个点图标的后面）而不是经典“齿轮”图标。 “最大循环数”示例shadebox现在使用新体验屏幕截图`new-scenario-settings-ex-1.png`（2模块示例场景，观看记录→杂项操作/转换对象）和`new-max-number-cycles.png`（通过控件中的齿轮图标打开场景设置面板，突出显示了“最大循环数”字段）。 第三个屏幕截图(`scenario-detail-350x207.png`)已完全放下 — 替换为文本：“您可以在Scenario Details （方案详细信息）页面的History （历史记录）区域看到已运行的周期。”

`scenario-overview.md` （行34 — 在跟踪电子表格中标记`Yes`，尚未在其中更新）：完全完成，0个标志。 纯概念性文章（没有分步的“点击X”说明），因此不需要新的/经典H2/H3拆分 — 只是添加了标准转换NOTE。 所有8个原始标记均已解析：
- 在Becky未标记的源`new-scenario-example-unmarked.png`上通过PowerShell/System.Drawing绘制的红色高亮框显示4（整个方案、触发器、模块、路由）（通过裁切+缩放源而不是像素扫描找到坐标 — PowerShell 5.1中的泛洪/像素循环方法始终在数组与标量异常上失败，并且速度仍然太慢）： `new-entire-scenario-scenario.png`、`new-scenario-trigger.png`、`new-scenario-module.png`、`new-scenario-route.png`。
- 2（连接器，场景区段）通过Becky提供的屏幕截图已标记： `new-scenario-connectors.png`，`new-scenario-segment.png`。
- 通过确认`fusion-integration-example.png` （经典）解析的1 （集成示例）与`new-scenario-example-unmarked.png`是完全相同的方案 — 直接重用，没有新标记。
- 1 （模板示例）已使用Becky未标记的`new-fusion-automation-example.png`进行解析，匹配经典的`fusion-template-example.png` — 如果Becky也希望在`license-automation-vs-integration.md`的“用于工作自动化的Workfront Fusion示例”部分中重用。

`view-scenario-data-flow.md` （行23 — 在跟踪电子表格中标记`Yes`，尚未在其中更新）：完全完成，0个标志。 添加了标准转换NOTE。 已确认两个体验中的“在正在运行的场景中查看数据流”相同（Becky的调用 — 此处不需要新的/经典拆分，不同于大多数其他过程） — 使用新体验措辞（包括“单击场景上的任意位置以进入场景编辑器”步骤）折叠回单个过程，保留现有的经典屏幕快照`assets/currently-running.png`，因为执行历史记录面板已确认不更改。 两个说明性运行/输出指示器的确在视觉上因体验而异，因此 — 与通常的单屏幕快照交换模式不同 — 旧屏幕快照和新屏幕快照并排显示，每个屏幕快照上方均有一个纯文本标签（新体验/经典体验，新优先）：运行指示器是`assets/new-spinning-icon.png`（模块图标上的旋转环）与经典`assets/ring-around-module.png`（模块周围的增长环）；输出指示器是`assets/new-output-indicator.png`与经典`assets/data-flow-output.png`（相同的绿色循环计数 — 气泡概念，已重新样式）。 这种“显示两者，标记的，新的第一个，标签在图像上方”的模式是一个住宅惯例 — 见上文。 描述性段落文本本身也首先提及新体验行为，然后是经典行为（例如，“……在新体验中用模块的图标上的旋转圆环标记，或者在经典体验中用模块周围的生长圆环标记。”）  — 新优先排序适用于散文，而不仅仅是图像/标签排序。

`fusion-glossary.md` （行43 — 在跟踪电子表格中标记`Yes`，尚未在其中更新）：完全完成，0个标志。 纯词汇表，没有程序。 在表之前添加了标准转换NOTE。 无需用户提供新的屏幕截图，即可解析两个嵌入图像（原始HTML `<img>`标记，而不是Markdown）：“Scenario”条目的`entire-scenario-blank.png`与`new-scenario-example-unmarked.png`完全相同的场景（直接重用），并且“Module”条目的`module.png`已替换为`new-module.png`，即来自同一来源的单卡裁切。

已阻止（与`debug-a-scenario.md`的处理方式相同 — 已标记，未在标记之外编辑，列G留空）： `advanced-error-handling.md`（行16）。 在简介中添加了标准过渡NOTE，但其两个示例（“示例：使用过滤器进行错误处理”和“嵌套示例”）是一个连续的示例Dropbox场景，没有分步的“单击X”内容以拆分为新的/经典 — 屏幕截图被有意保留为经典，按照Becky的指示，不要逐段触摸。 已内联标记（紧靠“###示例：使用过滤器处理错误”之前和紧靠嵌套`>[!BEGINSHADEBOX]`之前）表明文章需要在新版Experience **中构建一个**&#x200B;全新示例场景（Becky建议使用Workfront模块而不是Dropbox），而不仅仅是替换现有场景的屏幕截图。 电子表格列D和F用相同的范围注释更新；列G留空。

未开始：跟踪电子表格中的其他所有内容（`debug-a-scenario.md`在DevTool确认时受阻；其余内容保持不变）。
