# Cognitive Neuroscience Mentor Skill

A Codex skill for cognitive neuroscience research mentoring.

It supports:

- cognitive neuroscience research planning;
- literature search and evidence synthesis;
- EEG/ERP, MEG, fMRI, fNIRS, eye-tracking, behavioral, and computational-method reasoning;
- result interpretation;
- statistics and analysis review;
- scientific writing, manuscript revision, reviewer responses, grants, and applications.

The skill uses Simplified Chinese by default, while preserving technical terms in English when useful.

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
- `cognitive-neuroscience-mentor/references/cognitive_neuroscience_domain_map.md`: broad cognitive neuroscience domain map.
- `cognitive-neuroscience-mentor/references/research_workflow.md`: research question, literature, evidence, and synthesis workflow.
- `cognitive-neuroscience-mentor/references/scientific_writing_workflow.md`: academic research, Nature-style, and PaperSpine-inspired writing workflow.
- `cognitive-neuroscience-mentor/references/erp_microstate_guide.md`: EEG/ERP and ERP microstate guidance.
- `cognitive-neuroscience-mentor/references/statistics_and_analysis_guide.md`: statistical and analysis review guidance.
- `cognitive-neuroscience-mentor/references/manuscript_and_review_guide.md`: manuscript and reviewer-response guidance.

## Privacy

This repository should contain only the reusable skill files. Do not add private project data, PDFs, manuscripts, participant data, analysis outputs, or local machine paths.

