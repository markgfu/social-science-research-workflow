---
name: social-science-research-workflow
description: Diagnose and execute evidence-grounded social-science research workflows for literature discovery, close reading, research-question development, literature synthesis, academic writing and revision, validation, presentation, and explicit training or full-project requests. Apply the user's author-judgment and evidence writing standard; retain it when routing prose polishing or economics lineage reviews to a dedicated skill.
---

# Social Science Research Workflow

把社会科学研究任务路由到当前最需要的阶段，并交付可核验、可继续推进的成果。输出语言跟随用户。

## 先诊断，再执行

开始时确定四件事：

1. 用户要解决的具体问题和本轮交付物。
2. 当前阶段：文献、阅读、写作、验证、展示、训练或全流程。
3. 已有证据等级、人工审核状态和最主要缺口。
4. 哪个动作能最快降低当前最大不确定性。

显式模式优先；用户未指定时，根据任务自动路由。不要为了展示完整流程而扩展用户范围。

| 模式 | 典型任务 | 需要读取 |
|---|---|---|
| `literature` | 文献生态、检索、筛选、枢纽文献和引文链 | [literature-reading.md](references/literature-reading.md) |
| `reading` | 速读、精读、结构识别、证据笔记、灵感管理 | [literature-reading.md](references/literature-reading.md) |
| `writing` | 研究问题、动机、背景、数据、研究设计、段落衔接 | [writing-validation.md](references/writing-validation.md) |
| `validation` | 内生性、稳健性、机制、异质性、论文拓展 | [writing-validation.md](references/writing-validation.md) |
| `presentation` | 图、表、汇报结构、研究求助 brief | [presentation-training.md](references/presentation-training.md) |
| `training` | 周/月训练、研究习惯、进度复盘 | 仅在用户明确要求训练或复盘时读取 [presentation-training.md](references/presentation-training.md) |
| `full` | 从想法到论文的完整链路 | [full-workflow.md](references/full-workflow.md)，并按当前阶段读取其他 reference |

需要核对本 skill 的来源边界时，读取 [source-map.md](references/source-map.md)。不要默认加载所有 references。

## 文献阅读与写作的作者规范

开展精读、范文分析、文献综合、章节写作或文字修改时，必须先读取 [author-judgment-writing.md](references/author-judgment-writing.md)。纯元数据检索、导出和文件格式操作无需加载。

- 动笔前在内部明确本段的问题、判断和依据；证据缺失时补查、缩小或删除判断。
- 写作性修改前检索 AMJ、《求是》等真实原文，核对同类段落；以1—3个高质量参照研究论证方法，不套句式或固定段式。
- 每段一个主要任务，正面立论，按论证需要取舍事实、机制和边界。用简单句直接表达核心观点，统一术语，解释结果的研究含义。
- 完成后在内部检查判断、依据、语言和作者理解并直接修正；不默认交付内部质检过程。这些要求在交接专用写作 skill 后继续适用。

## 证据门槛

- `A`：已核验全文或一手材料，并有页码、章节、公式、表、图或附录锚点；可支持核心分析。
- `B`：已核验正式摘要；只可支持初筛和暂定描述。
- `C`：元数据、检索结果、引文图谱或二手提及；只用于发现。
- 区分 `SOURCE CLAIM`、`CODEX INTERPRETATION`、`CROSS-PAPER SYNTHESIS` 和 `OUR INFERENCE`。
- 无全文锚点写 `needs-verification`；未完成系统检索的“缺口”写 `needs-search`。
- 不虚构数据、结果、引用、机制、稳健性、研究缺口或识别成立条件。
- 速读和摘要不能冒充精读。打开 PDF 不等于 A 级证据，必须实际核对相关原页。
- 核心跨文献综合和正式成稿只使用 `status: accepted` 且 `source_level: A` 的笔记。AI 完成的新笔记先标记 `waiting-review`。
- 保留排除项、失败检索、旧版本和不确定性；不要自动覆盖人工文字。

## 统一输出契约

先交付本轮成果；以下信息按实际需要简要报告，已在成果中说清的不再重复。不将输出契约变成固定的收尾清单，也不报告内部质检过程：

1. 使用了哪些输入和证据等级；
2. 产物、路径或结构；
3. 未解决的 `needs-verification` / `needs-search`；
4. 当前门槛状态；
5. 最小安全下一步。

阅读类输出必须包含：研究问题、动机、设计、数据、发现、贡献、限制、原文锚点、对当前研究的用途和后续行动。缺项应明确写“未核验”或“不适用”。

写作类输出维持以下闭环，并检查相邻模块是否承接：

```text
研究问题 → 文献动机 → 背景 → 数据 → 研究设计 → 结果主张
```

## 专用能力交接

- 经济学文献谱系、检索审计或正式经济学综述：使用 [economics-literature-review](../economics-literature-review/SKILL.md)，保留本 skill 的阶段诊断与输出契约。
- 证据集合已固定后的论文成稿或纯文字润色：使用 [research-paper-writing](../research-paper-writing/SKILL.md)；交接时保留本 skill 的证据门槛与作者规范，不默认附加提纲、段落角色标签或自检清单。
- PDF、文档、表格或演示文件需要格式级处理时，使用相应格式 skill；内容主张仍受这里的证据规则约束。

## 停止条件

在以下情况停止当前阶段并报告缺口：关键来源只有摘要；论文全文未核验；核心笔记未获人工接受；数据或识别前提不存在；用户选择会实质改变研究对象；继续执行需要超出授权的访问或外部操作。
