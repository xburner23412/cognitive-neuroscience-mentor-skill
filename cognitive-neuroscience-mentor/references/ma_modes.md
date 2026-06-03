# Mentor-Anything Modes

Use this reference when the user says MA, mentor-anything, or asks for expert guidance without a narrower workflow.

## Mode Selection

- `MA-concept`: explain a concept, component, method term, cognitive process, brain region, model, or theory.
- `MA-result`: interpret a figure, topography, ERP component, microstate result, behavioral result, or statistical output.
- `MA-literature`: find, compare, or judge evidence for a claim.
- `MA-method`: evaluate task design, preprocessing, analysis choices, statistics, reproducibility, or code consequences.
- `MA-writing`: build manuscript logic, revise paragraphs, draft discussion, prepare reviewer response, or frame claims.
- `MA-devil`: challenge an interpretation as a critical reviewer would.

If the user only says "MA", infer the mode from the question. State the chosen mode briefly only when it helps.

## MA-Concept

Output:

```text
核心概念
为什么这个概念重要
常见误解
和用户项目的关系
需要查的关键文献类型
```

Use stable domain knowledge unless the concept is controversial, new, or manuscript-facing.

## MA-Result

Output:

```text
核心判断
结果字面上显示什么
可能的认知/神经解释
文献支撑与支持强度
替代解释
审稿风险
下一步分析
可写入论文的谨慎表述
```

Never jump directly from a scalp map or microstate class to a brain source or single cognitive process.

## MA-Literature

Output:

```text
要验证的具体 claim
搜索/证据范围
证据矩阵
共识
冲突或边界条件
哪些文献可用于正文
哪些只能作为背景
```

Search for direct, partial, background, and contradictory evidence. Do not search only for supportive citations.

## MA-Method

Output:

```text
方法选择
它回答什么问题
它不能回答什么问题
对统计单位和推断层级的影响
主要风险
推荐方案
论文中的方法理由
```

When possible, convert methodological advice into a model formula, analysis checklist, or reproducible step.

## MA-Writing

Output:

```text
这段/这一节的任务
中心 claim
证据顺序
需要引用的文献类型
需要降调的地方
修改稿
```

Improve argument structure before language polish.

## MA-Devil

Output:

```text
最强反对意见
可能被审稿人质疑的点
哪些质疑会真正伤害结论
如何用分析补强
如何用谨慎措辞防守
```

Use this when a result is unexpected, overinterpreted, weakly supported, or likely to be challenged.
