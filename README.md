# Cognitive Neuroscience Mentor Skill

A Codex skill for cognitive neuroscience research mentoring.

It supports:

- `mentor-anything` expert Q&A for cognitive neuroscience questions;
- evidence-supported mentoring with explicit citation direction and support levels;
- cognitive neuroscience research planning;
- literature search and evidence synthesis;
- EEG/ERP, MEG, fMRI, fNIRS, eye-tracking, behavioral, and computational-method reasoning;
- result interpretation;
- statistics and analysis review;
- scientific writing, manuscript revision, reviewer responses, grants, and applications.

The skill uses Simplified Chinese by default, while preserving technical terms in English when useful.

## Work Modes

- `mentor-anything`: default expert mentor mode for any professional cognitive neuroscience question.
- `quick`: concept explanation, first-pass result interpretation, or narrow writing/statistics questions.
- `standard`: most research mentoring tasks, with claim/evidence/boundary, literature support, alternatives, and next steps.
- `full`: manuscript restructuring, reviewer responses, grant/application work, systematic synthesis, or major analysis review.

## Install

Copy the `cognitive-neuroscience-mentor/` folder into your Codex skills directory:

```powershell
Copy-Item -Recurse -Force .\cognitive-neuroscience-mentor "$env:USERPROFILE\.codex\skills\"
```

After installation, start a new Codex session and invoke it naturally, for example:

```text
Use cognitive-neuroscience-mentor to help interpret this ERP result.
```

or:

```text
使用 cognitive-neuroscience-mentor 帮我设计一个认知神经科学研究问题。
```

## Contents

- `cognitive-neuroscience-mentor/SKILL.md`: trigger description and core workflow.
- `cognitive-neuroscience-mentor/references/mentor_anything_protocol.md`: default expert Q&A mentor subfunction.
- `cognitive-neuroscience-mentor/references/cognitive_neuroscience_domain_map.md`: broad cognitive neuroscience domain map.
- `cognitive-neuroscience-mentor/references/project_setup_guide.md`: how to adapt the mentor to a new project folder.
- `cognitive-neuroscience-mentor/references/research_workflow.md`: research question, literature, evidence, and synthesis workflow.
- `cognitive-neuroscience-mentor/references/scientific_writing_workflow.md`: academic research, Nature-style, and PaperSpine-inspired writing workflow.
- `cognitive-neuroscience-mentor/references/erp_microstate_guide.md`: EEG/ERP and ERP microstate guidance.
- `cognitive-neuroscience-mentor/references/statistics_and_analysis_guide.md`: statistical and analysis review guidance.
- `cognitive-neuroscience-mentor/references/manuscript_and_review_guide.md`: manuscript and reviewer-response guidance.
- `cognitive-neuroscience-mentor/references/ethics_and_interpretation_boundaries.md`: child, clinical, risk-label, privacy, and interpretation boundaries.
- `cognitive-neuroscience-mentor/references/example_prompts.md`: example prompts for onboarding and real use.

## Example Prompts

```text
Use cognitive-neuroscience-mentor in standard mode. Interpret this ERP topomap result and suggest what literature I should check.
```

```text
Use mentor-anything with literature support. Explain why my child Go/No-Go ERP topomap differs from the adult NoGo-N2/P3 pattern.
```

```text
请作为认知神经科学导师帮我评估这个 fMRI ROI 结果，重点检查统计解释、替代解释和论文写法。
```

```text
Use full mode to rebuild my Discussion. First create a controlling motivation, claim register, and section blueprint.
```

## Privacy

This repository should contain only the reusable skill files. Do not add private project data, PDFs, manuscripts, participant data, analysis outputs, or local machine paths.

## License

MIT License. See `LICENSE`.
