# Function Menu

Use this file when the user asks what this skill can do, how to call it, or which mode fits a task.

## Everyday Mentor Modes

- `MA` or `mentor-anything`: general expert cognitive neuroscience mentoring. The mode is inferred from the question.
- `MA-concept`: explain concepts, components, methods, theories, and common misunderstandings.
- `MA-result`: interpret figures, statistics, ERP/topomap/microstate results, and unexpected findings.
- `MA-literature`: evaluate evidence for a claim and synthesize supporting, conflicting, and boundary-condition literature.
- `MA-search`: aggressive but legitimate literature/PDF retrieval. Searches local files and external sources, finds official/open/institutional/preprint PDFs where available, downloads and validates PDFs, and updates the project literature index.
- `MA-method`: evaluate design, preprocessing, statistics, analysis choices, and reproducibility.
- `MA-writing`: build manuscript logic, draft or revise sections, and align claims with evidence.
- `MA-devil`: simulate reviewer criticism and identify the strongest threats to a claim.

## Output Depth

- `quick`: short answer with core judgment, main reason, main risk, and next step.
- `standard`: default research mentoring depth with evidence boundary and recommended action.
- `full`: expanded workflow for manuscript audit, paper spine, claim-evidence register, reviewer risk, journal targeting, or submission package.

Examples:

```text
MA quick: 这个 topomap 为什么不像成人 NoGo N2/P3?
MA-result standard: 解释这张 microstate 图，指出审稿风险。
MA-search: 帮我找儿童 Go/NoGo posterior P3 的文献 PDF，尽可能下载，放到 03_literature。
MA-search full: 检索 ERP microstate TANOVA/TCT 方法文献，列出下载成功、无法下载、需要机构登录的文献。
MA-devil: 作为审稿人攻击我对 posterior topography 的解释。
MA-writing full: 基于这些结果搭建 Discussion 的 paper spine。
```

## Paper-Oriented Modes

- `paper spine`: build central problem, gap, claim, evidence, boundary, contribution, and reviewer risk.
- `claim-evidence register`: map manuscript claims to user data and citation support.
- `figure-to-argument`: evaluate whether each figure supports a clear manuscript claim.
- `reviewer risk`: identify likely reviewer objections and how to defend or weaken claims.
- `submission readiness`: check title, abstract, figures, methods transparency, limitations, data/code availability, and target journal fit.

## Project-Specific Strengths

For the user's current project, the skill is optimized for:

- Go/No-Go and inhibitory-control interpretation;
- child developmental ERP;
- ERP components and topographies;
- ERP microstate analysis, TCT, TANOVA, clustering, backfitting, GEV, coverage, duration, onset, and transition;
- attention, reading, and mathematics risk;
- categorical groups vs continuous risk scores;
- high-quality manuscript construction and submission strategy.
