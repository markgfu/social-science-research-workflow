# 社会科学研究工作流

一个面向社会科学研究的 Codex skill。根据当前研究阶段，处理文献发现、论文阅读、研究问题、学术写作、研究设计验证、汇报和研究训练，并保留可核验的证据与后续行动。

技能名称：`social-science-research-workflow`。

## 能做什么

| 模式 | 适用任务 |
| --- | --- |
| `literature` | 制定检索范围、筛选文献、识别枢纽论文、追踪引文和检验候选缺口 |
| `reading` | 速读初筛、全文精读、证据提取、来源笔记和范文分析 |
| `writing` | 收敛研究问题，组织文献动机、背景、数据、研究设计和结果讨论 |
| `validation` | 识别威胁、稳健性、异质性、机制及主张边界 |
| `presentation` | 图表说明、研究汇报和研究求助材料 |
| `training` | 用户明确要求时，制定训练计划并复盘 |
| `full` | 从想法到论文的阶段推进；关键证据或设计变化时回退检查 |

用户可以指定模式，也可以直接描述任务，由 skill 判断当前最需要推进的阶段。输出语言跟随用户。

## 安装

下载本仓库，将包含 `SKILL.md`、`agents/` 和 `references/` 的完整文件夹保存为：

- Windows：`%USERPROFILE%\.codex\skills\social-science-research-workflow`
- macOS / Linux：`~/.codex/skills/social-science-research-workflow`

若使用了自定义 `CODEX_HOME`，将文件夹放入该目录下的 `skills/`。仓库根目录就是 skill 根目录，无需再嵌套一层同名文件夹。

也可以将本仓库链接交给 Codex 的 `skill-installer`，要求安装仓库根目录中的 skill。

## 使用示例

在 Codex 中使用 `$social-science-research-workflow` 调用。例如：

```text
使用 $social-science-research-workflow，进入 literature 模式。
我的研究问题是地方环境治理中的政策执行差异。请先制定检索范围、
纳入排除标准和首轮查询，保留检索记录，并把尚未核验的缺口标出来。
```

```text
使用 $social-science-research-workflow，精读我提供的论文。
区分作者主张和你的解释，为研究设计、主要发现和限制提供原文页码，
未能核验的内容保持待核验状态。
```

```text
使用 $social-science-research-workflow，检查我的结果讨论。
先核对相关原文参照，再依据现有结果解释研究含义，
保留引用和术语，删除没有证据支持的判断。
```

```text
使用 $social-science-research-workflow，进入 full 模式。
根据我现有的研究材料判断当前阶段，推进最能降低不确定性的下一步，
并记录仍需人工审核的证据。
```

## 证据与写作规则

- **A 级证据**：核验相关全文或一手材料，并提供页码、章节、表图等定位。
- **B 级证据**：核验正式摘要，只支持初筛和暂定描述。
- **C 级证据**：元数据、检索结果或二手提及，只用于发现来源。
- 区分来源主张、模型解释、跨文献综合和研究者推断。
- AI 新建的来源笔记先标记为 `waiting-review`。核心跨文献综合与正式成稿要求相关笔记通过人工审核，达到 `accepted + A`。
- 未核验的主张保留 `needs-verification`，未完成检索的候选缺口保留 `needs-search`。
- 写作先明确问题、判断与依据；不虚构数据、引用、结果或研究缺口。写作性修改前，按任务检索并核对 AMJ、《求是》等真实原文参照。

完整规则见 [SKILL.md](SKILL.md) 和 [作者判断与证据规范](references/author-judgment-writing.md)。

## 文件结构

```text
social-science-research-workflow/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── author-judgment-writing.md
    ├── full-workflow.md
    ├── literature-reading.md
    ├── presentation-training.md
    ├── source-map.md
    └── writing-validation.md
```

`SKILL.md` 负责阶段诊断与路由；参考资料按任务加载。

## 配套技能与工具

本仓库包含上述工作流及参考资料。处理专门任务时，工作流会交接给 `economics-literature-review`、`research-paper-writing`，或 PDF、文档、表格、演示文稿等格式技能；这些配套技能需要另行安装。联网检索、全文访问与文件处理也取决于运行环境中可用的工具和访问权限。

## 来源

研究流程主要依据陈硕《非此即彼：社会科学研究指南》的经审核章级笔记整理；作者判断与写作规范来自维护者直接制定的要求。来源位置、规范与工程化约束的区别见 [来源映射](references/source-map.md)。

仓库不包含原书 PDF、OCR 全文或原始研究项目材料。参考资料中列出的书籍和论文，其权利归各自权利人所有。
