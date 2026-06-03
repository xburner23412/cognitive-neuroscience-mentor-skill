# Mentor-Anything Modes

Use this reference when the user says MA, mentor-anything, or asks for expert guidance without a narrower workflow.

MA modes define what to check. They do not require printing every checked item. Use `output_depth_control.md` to decide whether to give quick, standard, or full output.

## Mode Selection

- `MA-concept`: explain a concept, component, method term, cognitive process, brain region, model, or theory.
- `MA-result`: interpret a figure, topography, ERP component, microstate result, behavioral result, or statistical output.
- `MA-literature`: find, compare, or judge evidence for a claim.
- `MA-method`: evaluate task design, preprocessing, analysis choices, statistics, reproducibility, or code consequences.
- `MA-writing`: build manuscript logic, revise paragraphs, draft discussion, prepare reviewer response, or frame claims.
- `MA-devil`: challenge an interpretation as a critical reviewer would.

If the user only says "MA", infer the mode from the question. State the chosen mode briefly only when it helps.

## MA-Concept

Internal checks:

```text
Core concept
Why it matters
Common misunderstanding
Relation to the user's project
Literature type to check
```

Use stable domain knowledge unless the concept is controversial, new, or manuscript-facing.

## MA-Result

Internal checks:

```text
Core judgment
What the result literally shows
Possible cognitive/neural interpretation
Literature support and support strength
Alternative explanations
Reviewer risk
Next analysis
Cautious manuscript wording
```

Never jump directly from a scalp map or microstate class to a brain source or single cognitive process.

## MA-Literature

Internal checks:

```text
Claim to verify
Search/evidence scope
Evidence matrix
Consensus
Conflicts or boundary conditions
Sources usable in the manuscript
Sources usable only as background
```

Search for direct, partial, background, and contradictory evidence. Do not search only for supportive citations.

## MA-Method

Internal checks:

```text
Method choice
Question it answers
Question it cannot answer
Effect on statistical unit and inference level
Main risks
Recommended plan
Manuscript justification
```

When possible, convert methodological advice into a model formula, analysis checklist, or reproducible step.

## MA-Writing

Internal checks:

```text
Task of this paragraph/section
Central claim
Evidence order
Citation type needed
Where to weaken wording
Revised draft
```

Improve argument structure before language polish.

## MA-Devil

Internal checks:

```text
Strongest objection
Likely reviewer concerns
Which concerns seriously threaten the conclusion
Analysis needed to strengthen the claim
Cautious wording for defense
```

Use this when a result is unexpected, overinterpreted, weakly supported, or likely to be challenged.
