# Analysis Decision Log

Use this template whenever the user chooses among analysis paths. The goal is to create manuscript-ready reasoning and prevent ad hoc decisions.

## Decision Template

```text
Decision:
Scientific question:
Chosen approach:
Alternative approaches:
Why this approach fits the question:
What this approach cannot answer:
Statistical unit:
Model or test:
Multiple-comparison plan:
Robustness check:
Reviewer concern:
Manuscript justification:
```

## Common Decisions In This Project

### Group vs Continuous Scores

Preferred default:

- primary: continuous attention, reading, and math scores;
- secondary: categorical groups for visualization and robustness.

Justification:

- learning and attention risk often vary dimensionally;
- continuous models preserve information and reduce cutoff arbitrariness;
- groups remain useful for communicating profiles and comparing with prior risk-group literature.

Watch:

- collinearity among scores;
- unequal group sizes;
- comorbidity or overlapping risk;
- whether a score is reversed or standardized.

### Grand Average vs Individual Evoked Clustering

Grand average segmentation:

- good for comparability with classic ERP microstate papers;
- easier to present;
- may hide individual variability.

Individual evoked pooling:

- better aligned with dimensional score analysis;
- preserves subject-level variability;
- requires stronger checks for map stability, subject contribution, and trial-count imbalance.

Recommended compromise:

- use a common map solution derived from pooled individual evokeds for primary dimensional analysis;
- compare with group/condition grand-average solution as robustness or descriptive validation.

### Choosing K

Do not choose K only because the maps are interpretable.

Consider:

- cross-validation or fit criterion;
- GEV elbow;
- map stability across bootstraps or splits;
- theoretical interpretability;
- whether K splits a known broad component into meaningful sub-states or overfits noise.

### Time Windows

Avoid selecting windows only after seeing significant group effects.

Prefer:

- literature-based windows;
- GFP peaks;
- task/component-informed windows;
- microstate onset/offset from global segmentation;
- sensitivity analyses with neighboring windows.

### Statistics For Microstate Metrics

For subject-level metrics, prefer models that preserve the unit of analysis:

```text
metric ~ condition * score_attention + condition * score_reading + condition * score_math + covariates + random effects
```

or, if using profile groups:

```text
metric ~ condition * group + covariates + random effects
```

Covariates may include age, sex, handedness, trial count, task accuracy, and site/session variables if relevant.
