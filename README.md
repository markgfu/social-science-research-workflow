# 社会科学研究工作流 · 三技能合集

一次安装三个互相配合的 Codex skill，覆盖研究阶段诊断、经济学文献综述，以及论文成稿与修改。三个 skill 的完整参考资料均包含在本仓库中。

## 三个 skill 如何分工

| Skill | 职责 | 入口 |
| --- | --- | --- |
| `social-science-research-workflow` | 诊断研究阶段、确定下一步、统一证据门槛与作者规范 | [SKILL.md](skills/social-science-research-workflow/SKILL.md) |
| `economics-literature-review` | 文献发现、筛选、全文提取、模型谱系、假设与机制比较、综述及证据审计 | [SKILL.md](skills/economics-literature-review/SKILL.md) |
| `research-paper-writing` | 章节结构、段落衔接、主张与证据对齐、成稿修改及审稿检查 | [SKILL.md](skills/research-paper-writing/SKILL.md) |

典型推进关系：

```text
工作流诊断当前研究阶段
    → 经济学文献检索、精读与综合
    → 人工审核核心证据
    → 论文成稿与修改
```

写作技能与经济学文献技能共同读取工作流中的作者判断规范。三个目录需保持并列、保留原名；专项技能交接后，工作流的证据门槛和作者规范继续适用。

写作技能的章节参考和示例主要来自 ML/CV/NLP 写作场景。用于社会科学或经济学时，应按研究问题、假设、数据、识别、机制和制度背景调整，不直接套用技术论文结构。

## 一次安装完整合集

### 推荐：将下面的请求复制给 Codex

```text
请使用 $skill-installer，从 GitHub 仓库
markgfu/social-science-research-workflow
一次安装以下三个路径中的全部技能：

skills/social-science-research-workflow
skills/economics-literature-review
skills/research-paper-writing

保持三个技能的目录名，并安装到同一个 skills 目录，
以保留它们之间的相对引用。
```

安装完成后，在下一轮对话使用 `$social-science-research-workflow` 开始任务，也可以单独调用另外两个技能。

### 命令行：一次调用安装三个 skill

以下命令使用 Codex 自带的 `skill-installer` 和 Python，无需分别运行三次。

Windows PowerShell：

```powershell
$codexDir = if ($env:CODEX_HOME) { $env:CODEX_HOME } else { Join-Path $HOME '.codex' }
python (Join-Path $codexDir 'skills/.system/skill-installer/scripts/install-skill-from-github.py') --repo markgfu/social-science-research-workflow --path skills/social-science-research-workflow skills/economics-literature-review skills/research-paper-writing
```

macOS / Linux：

```bash
python3 "${CODEX_HOME:-$HOME/.codex}/skills/.system/skill-installer/scripts/install-skill-from-github.py" --repo markgfu/social-science-research-workflow --path skills/social-science-research-workflow skills/economics-literature-review skills/research-paper-writing
```

### 手动安装

下载仓库 ZIP 并解压，将仓库 `skills/` 下的三个完整文件夹复制到同一个 Codex 技能目录：

- Windows：`%USERPROFILE%\.codex\skills\`
- macOS / Linux：`~/.codex/skills/`
- 设置了 `CODEX_HOME` 时：该目录下的 `skills/`

最终目录结构应当是：

```text
skills/
├── social-science-research-workflow/
│   ├── SKILL.md
│   ├── agents/
│   └── references/
├── economics-literature-review/
│   ├── SKILL.md
│   ├── agents/
│   └── references/
└── research-paper-writing/
    ├── SKILL.md
    ├── agents/
    └── references/
```

不要把整个仓库嵌套进一个同名 skill 文件夹，也不要只复制三个 `SKILL.md`。

### 已安装旧版或同名 skill

本仓库已由“根目录是单个 skill”改为 `skills/` 下的三技能合集。原工作流的技能名称和调用方式保持不变，安装源路径改为 `skills/social-science-research-workflow`。

安装器遇到已经存在的同名目录会停止。更新前，先将已有目录备份到技能目录之外，保留自己的修改，再安装这三个路径；或手动比较并合并文件。只补装缺失技能时，可以仅向安装器传入缺失的路径。

## 工作流模式

| 模式 | 适用任务 |
| --- | --- |
| `literature` | 检索范围、筛选、枢纽文献、引文追踪和候选缺口 |
| `reading` | 速读初筛、全文精读、证据笔记和范文分析 |
| `writing` | 研究问题、文献动机、背景、数据、设计与结果讨论 |
| `validation` | 识别威胁、稳健性、异质性、机制与主张边界 |
| `presentation` | 图表说明、研究汇报和研究求助材料 |
| `training` | 明确要求时制定训练计划并复盘 |
| `full` | 从想法到论文的阶段推进及回退检查 |

## 使用示例

### 从研究想法开始

```text
使用 $social-science-research-workflow，进入 full 模式。
我的研究方向是地方环境治理中的政策执行差异。
根据我提供的材料判断当前阶段，推进最能降低不确定性的下一步，
需要时使用已安装的经济学文献技能或写作技能。
```

### 专门做经济学文献综述

```text
使用 $economics-literature-review，梳理我提供的理论论文。
比较各篇的前身模型、基准假设、假设变化、机制与结论，
为主要判断保留原文锚点，未经人工审核的笔记标记为 waiting-review。
```

### 修改已有论文

```text
使用 $research-paper-writing，修改我提供的结果讨论。
遵守共享的作者判断规范，保留引用和术语，
依据已有结果解释研究含义，删除没有证据支持的判断。
```

## 证据与写作规则

- **A 级证据**：核验相关全文或一手材料，并提供页码、章节、表图等定位。
- **B 级证据**：核验正式摘要，只支持初筛和暂定描述。
- **C 级证据**：元数据、检索结果或二手提及，只用于发现来源。
- 区分来源主张、模型解释、跨文献综合和研究者推断。
- AI 新建来源笔记先标记为 `waiting-review`。核心跨文献综合与正式成稿要求相关笔记经人工审核，达到 `accepted + A`。
- 未核验的主张保留 `needs-verification`，未完成检索的候选缺口保留 `needs-search`。
- 写作先明确问题、判断与依据；不虚构数据、引用、结果或研究缺口。写作性修改前，按任务检索并核对真实原文参照。

完整要求见 [工作流入口](skills/social-science-research-workflow/SKILL.md)、[作者判断与证据规范](skills/social-science-research-workflow/references/author-judgment-writing.md) 和 [经济学证据政策](skills/economics-literature-review/references/evidence-policy.md)。

## 工具与格式支持

本合集包含完整的三个研究与写作 skill，不会自动安装软件、开通数据库权限或连接账户。联网检索、全文访问、Zotero/Obsidian 集成，以及 PDF、Word、表格和演示文稿的格式处理，需要运行环境中提供相应工具、权限或格式技能。已有材料的研究诊断与文字处理可按可用工具推进，缺失证据仍须明确标记。

## 来源

研究流程主要依据陈硕《非此即彼：社会科学研究指南》的经审核章级笔记整理；作者判断与写作规范来自维护者直接制定的要求。来源位置、规范与工程化约束的区别见 [来源映射](skills/social-science-research-workflow/references/source-map.md)。

仓库不包含原书 PDF 或原始研究项目材料。写作技能包含参考笔记与论文写作示例；其中引用的书籍、论文和第三方材料，其权利归各自权利人所有。
