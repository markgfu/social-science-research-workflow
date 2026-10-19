# 项目介绍图制作记录

生成方式：内置 `image_gen` 图像模型。三张图采用统一的中文学术插画风格；研究推进图在初次生成后，使用同一图像模型修正了阶段排列与箭头。下列提示词为实际使用的完整文本。

图片均保存在本仓库的 `docs/images/` 中。图片用于项目介绍；执行规则以技能文件为准。

## 1. project-overview

最终文件：[project-overview.png](images/project-overview.png)

```text
Use case: infographic-diagram.
Create a polished Chinese editorial infographic for a GitHub project, landscape 16:9, high resolution, crisp highly legible Chinese typography. Topic: a bundle of three Codex skills for social-science research. Warm ivory background, dark navy text, teal, muted terracotta and antique gold accents. Restrained academic editorial design with subtle paper textures, fine line icons, generous whitespace, elegant flat illustration, no gradients, no photorealism, no logos or watermarks. The illustration should look like a carefully art-directed academic handbook, not a software dashboard.
Layout: large title and short subtitle at top. Three equally important substantial illustrated panels across the center, gently connected. Left panel: compass and map of research questions. Middle: paper stack, magnifying glass and model lineage tree. Right: manuscript with paragraph marks and a pen. A slim shared-foundation strip runs below all three, showing that all use the same evidence and writing standard.
Render ONLY these Chinese texts, precisely and legibly:
Title: "社会科学研究工作流"
Subtitle: "三个技能协作，从研究问题到论文表达"
Left panel heading: "整体工作流"
Left detail: "阶段诊断 · 任务路由 · 研究推进"
Middle panel heading: "经济学文献综述"
Middle detail: "文献检索 · 模型谱系 · 证据综合"
Right panel heading: "论文写作与修改"
Right detail: "章节结构 · 段落衔接 · 主张核对"
Foundation heading: "共享规范"
Foundation detail: "证据可追溯　人工审核　先有判断，再有文字"
Small bottom label: "一次安装，按任务使用"
No additional words or invented product claims. Ensure all text remains away from edges and at comfortable reading size.
```

## 2. research-journey

最终文件：[research-journey.png](images/research-journey.png)

```text
Use case: infographic-diagram.
Create an original Chinese academic editorial infographic for the same social-science research skill bundle. Landscape 16:9 high resolution. Warm ivory background, dark navy text, teal steps, muted terracotta for the human-review checkpoint, antique gold for the final manuscript. Elegant flat illustrations, subtle paper texture, precise arrows, large readable Chinese text, abundant whitespace. This is an explanatory poster, not an app screenshot. No logos, no watermarks.
Visualize a clear research journey in two rows of three generously spaced illustrated stations, numbered 01 through 06. The path flows left to right across the first row, then down and from left to right across the second row, using a clear routed connector around the outside so there is no ambiguous backward reading. Alternatively a single six-station horizontal route is acceptable if labels stay large. Each station has an expressive but simple illustration.
Title exact: "研究如何一步步推进"
Subtitle exact: "先解决当前最大的不确定性"
Station 01: "研究问题" and "明确对象、关系与边界"
Station 02: "文献发现" and "保留查询与筛选记录"
Station 03: "全文精读" and "核对原文并保存锚点"
Station 04: "人工审核" and "确认核心笔记可被采用"
Station 05: "综合与设计" and "比较机制，核对研究假设"
Station 06: "成稿与展示" and "组织论证，解释发现"
A clear restrained dashed feedback arrow from the final stages toward the earlier stages, labelled exactly: "问题、证据或设计变化时，回退检查"
Small footer exact: "检索记录 → 来源笔记 → 综合表 → 论文稿"
The human review is a real checkpoint before core synthesis, not an optional decoration. Do not depict automated acceptance or automatically proven causality. Render the quoted texts exactly, no other text.
```

### 修正流程箭头的编辑提示词

```text
Edit this Chinese research workflow infographic. Preserve its existing illustration style, colors, typography, all six station texts, all six station illustrations, title, subtitle, feedback label and bottom artifact strip. Correct ONLY the station arrangement and flow connectors so that human review is never bypassed.
Use a snake route with the following exact arrangement:
TOP ROW from left to right: 01 研究问题, 02 文献发现, 03 全文精读.
BOTTOM ROW from left to right: 06 成稿与展示, 05 综合与设计, 04 人工审核.
Thus swap the entire current bottom-left 04 panel with the entire current bottom-right 06 panel. Keep the center 05 panel in place.
Solid teal arrows must show EXACTLY: 01 → 02 → 03 ↓ 04 ← 05 ← 06 is NOT correct; the correct sequence is 01 → 02 → 03, then 03 ↓ 04 on the right, then 04 → 05 toward the left, then 05 → 06 toward the left. In visual screen direction, arrowheads along the bottom row point LEFT, because chronological reading is right-to-left there. Final correct chronological sequence: 01,02,03,04,05,06.
Use only five solid progression connectors: 01→02; 02→03; 03→04 downward at right; 04→05 leftward; 05→06 leftward. Remove all previous progression connectors that contradict this. In particular, NEVER connect 03 to 06.
Dashed terracotta feedback connector may go from 06 back to 01 along the left outside margin, with arrowhead at 01. Keep existing feedback text in the white horizontal gap between rows but ensure this label is visually separate from the solid progression path.
Keep the exact original text in every panel: 04 人工审核 / 确认核心笔记可被采用; 05 综合与设计 / 比较机制，核对研究假设; 06 成稿与展示 / 组织论证，解释发现. Everything else stays the same.
No new labels, no added captions. All text sharp and legible, all arrowheads unambiguous.
```

## 3. evidence-and-judgment

最终文件：[evidence-and-judgment.png](images/evidence-and-judgment.png)

```text
Use case: infographic-diagram.
Create a polished Chinese editorial infographic explaining evidence and author judgment in a social-science research workflow. Landscape 16:9 high resolution; warm ivory paper background, dark navy typography, teal, muted terracotta and antique gold; subtle paper texture; elegant flat academic icons; no logo, watermark, fake charts or software screens. Text must be clean, accurate and highly legible. Use generous margins and calm visual hierarchy.
Title: "每个判断，都能回到证据"
Two balanced panels below title.
Left panel heading: "证据分级"
Three independent horizontal cards, with no arrows implying automatic promotion:
"A" heading "已核验全文" detail "有页码、章节或表图定位"
"B" heading "已核验摘要" detail "用于初筛与暂定描述"
"C" heading "元数据与检索结果" detail "用于发现来源"
Use small book and magnifier icons on A, abstract page on B, search results cards on C. A strongest in teal.
Right panel heading: "人工审核门槛"
Flow of four compact illustrated steps: "AI 提取" → "等待审核" → "人工接受" → "核心综合"
Under the flow, show a prominent precise badge: "核心综合：A级证据 + 人工接受"
Below that badge: "待核验的主张，保留不确定性"
Full-width bottom strip, lightly separated:
heading "作者判断"
text "先明确问题、判断与依据，再组织文字"
small supporting line "不虚构引用、数据、结果或研究缺口"
No additional text. Do not imply that AI makes a human acceptance decision. Make all labels readable at typical GitHub README viewing size.
```
