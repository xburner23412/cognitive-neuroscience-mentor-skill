# Result Interpretation Templates

Use these templates when interpreting empirical results. Fill missing fields with explicit assumptions rather than silently guessing.

## Required Extraction

Before interpretation, identify:

- task and paradigm;
- condition or contrast;
- group or continuous predictor;
- dependent variable;
- time window;
- electrode, topography, region, or microstate class;
- statistical model and unit of analysis;
- effect direction and uncertainty;
- behavioral link, if available.

If any item is missing, continue with best assumptions and state what information would change the answer.

## ERP Component / Topography

Use:

```text
事实: condition/contrast shows [direction] at [time] over [scalp distribution].
解释: this may reflect [process], but only if timing/task/electrode pattern fit.
限制: scalp topography is not source localization; component labels are descriptive unless validated.
替代解释: visual processing, attention allocation, motor preparation, trial count, baseline, reference, filtering, age-related latency/topography.
下一步: component ROI, global field power, TANOVA, behavior correlation, trial-count check, reference/baseline sensitivity.
论文表述: "The pattern is consistent with..., although..."
```

## ERP Microstate

Use:

```text
事实: map [label] dominates [time] with changes in duration/coverage/GEV/onset/transition.
解释: a microstate is a stable scalp configuration, not a cognitive module.
限制: labels depend on clustering solution, preprocessing, reference, and fitting criteria.
替代解释: map splitting/merging, condition imbalance, individual variability, latency jitter, visual component persistence.
下一步: justify K, report GEV, backfit to individuals, TANOVA/TCT if appropriate, test metrics with subject-level models.
论文表述: "The temporal predominance of this topography suggests altered recruitment or timing of the network configuration associated with..."
```

## Behavioral Result

Use:

```text
事实: accuracy/RT/commission/omission/d-prime/RT variability differs by [condition/group/predictor].
解释: map to inhibitory control only if NoGo demand and error pattern support it.
限制: RT and accuracy confounds can reflect attention, motivation, speed-accuracy tradeoff, or task comprehension.
下一步: d-prime, commission vs omission, RT variability, post-error slowing, condition-specific trial counts.
```

## Statistical Output

Use:

```text
事实: model term [term] has [estimate, CI, p/effect size].
解释: the effect means [unit-level statement].
限制: association is not causation; check repeated measures, imbalance, multiple comparisons, and random effects.
下一步: effect plot, model diagnostics, sensitivity model, correction strategy, robustness table.
```

## Child Go/No-Go ERP Cautions

- Adult-like frontocentral NoGo-N2/P3 should not be assumed in first-grade children.
- Posterior-dominant patterns may reflect developmental strategy, visual-attentional processing, delayed maturation, or task-specific demands.
- Inhibitory-control wording needs behavioral support, especially commission errors or NoGo-specific performance.
- A NoGo-Go contrast isolates inhibition only partially; it also includes attention, salience, frequency, response conflict, and stimulus evaluation.
