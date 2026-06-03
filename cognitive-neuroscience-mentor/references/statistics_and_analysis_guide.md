# Statistics And Analysis Guide

Use this file when statistics, reproducibility, model choice, EEG/ERP preprocessing consequences, or microstate metrics affect the inference.

## First Checks

Identify:

- research question;
- unit of analysis;
- sample size and missing data;
- group definition or continuous predictors;
- within-subject factors;
- between-subject factors;
- covariates;
- dependent variable;
- model formula or statistical test;
- correction strategy;
- effect size and confidence interval;
- whether the analysis is confirmatory, planned, exploratory, or robustness-oriented.

## Unit Of Analysis

Do not analyze condition-level or window-level values as if they were independent participants.

Common units:

- trial-level behavior: trials nested in participants;
- subject-level ERP amplitude or microstate metric: one or more values per participant/condition/map;
- electrode/time samples: high-dimensional repeated measures requiring correction or permutation;
- group grand averages: useful for visualization and segmentation, not sufficient for inferential statistics alone.

## Group vs Continuous Predictors

For attention, reading, and mathematics risk, prefer continuous scores when the research question is dimensional and scores are available.

Use groups when:

- the design or hypothesis is explicitly categorical;
- clinical/risk cutoffs are theoretically justified;
- groups help communicate profiles;
- groups are used as descriptive or robustness checks.

Risks of grouping:

- loss of information;
- arbitrary cutoffs;
- unbalanced groups;
- comorbidity hidden inside categories;
- reduced statistical power.

Recommended default for the user's project:

```text
Primary: metric ~ condition * attention_score + condition * reading_score + condition * math_score + covariates + random effects
Secondary: metric ~ condition * risk_group + covariates + random effects
```

Check collinearity among scores and consider separate models if predictors are strongly correlated.

## EEG/ERP-Specific Risks

Check:

- filtering and reference;
- epoch window;
- baseline correction;
- artifact rejection or ICA;
- interpolation and missing channels;
- trial counts per condition and group;
- condition coding;
- response-locked vs stimulus-locked timing;
- group overlap or comorbidity;
- multiple comparisons;
- time-window selection;
- circular analysis;
- map selection and fitting procedure.

## ERP Component Statistics

Prefer:

- literature- or GFP-informed time windows;
- predefined ROIs when component hypotheses are specific;
- mass-univariate or cluster/permutation correction when exploring time/electrode space;
- effect sizes and confidence intervals, not only p-values.

Avoid:

- choosing the strongest-looking time window after seeing group differences;
- interpreting a post hoc window as a classic component without topographic/timing support;
- treating scalp effects as source localization.

## ERP Microstate Statistics

Common dependent variables:

- GEV;
- coverage;
- duration;
- occurrence;
- onset/offset;
- transition probabilities;
- fitting residuals;
- TANOVA/TCT results when using topographic comparisons.

Key checks:

- justify K by fit, stability, cross-validation, and interpretability;
- backfit maps to subject-level evokeds before subject-level inference;
- ensure every participant contributes comparably to pooled clustering;
- check whether maps split or merge across K values;
- control for trial count and signal quality where relevant;
- avoid interpreting map labels as cognitive modules.

Example model:

```text
microstate_metric ~ condition * score_attention + condition * score_reading + condition * score_math + age + sex + trial_count + (1 | subject)
```

If there are multiple maps and metrics, specify the correction family before testing.

## Multiple Comparisons

Define the family:

- electrodes;
- time points;
- time windows;
- components;
- microstate maps;
- microstate metrics;
- risk scores;
- behavioral outcomes.

Use:

- FDR for structured sets of related tests;
- cluster/permutation for dense time-electrode analyses;
- hierarchical or planned contrasts when theory is strong;
- robustness tables for exploratory findings.

Do not hide exploratory multiplicity by reporting only significant tests.

## Model Diagnostics

Check:

- residuals and influential cases;
- heteroscedasticity;
- collinearity;
- random-effect structure;
- convergence warnings;
- outlier sensitivity;
- whether transformations are needed;
- whether nonparametric or permutation methods are more appropriate.

## Interpretation Rules

- Statistical significance is not theoretical significance.
- A non-significant result is not evidence of no effect unless the analysis supports that claim.
- Interactions must be interpreted through simple effects, estimated marginal means, or clear effect plots.
- Correlations with behavior strengthen interpretation but do not prove mechanism.
- Group differences in neural measures can reflect signal quality, task engagement, trial count, or developmental variability.
- For child risk groups, avoid diagnostic language unless diagnosis was measured.

## Recommended Output

For a statistical result, provide:

1. literal statistical meaning;
2. effect direction;
3. practical or theoretical relevance;
4. assumptions and possible violations;
5. alternative explanations;
6. recommended robustness checks;
7. cautious manuscript sentence.
