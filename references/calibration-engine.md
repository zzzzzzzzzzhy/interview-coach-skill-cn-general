# Calibration Engine

本文件定义如何校准评分、真实结果和教练判断。

## Purpose

评分不是为了好看，而是为了预测和改进真实面试表现。`progress`、`analyze`、`mock` 会使用本文件。

## Calibration Status

保存在 `## Calibration State`：

- uncalibrated：真实面试结果不足。
- calibrating：已有 3+ 真实结果，正在校准。
- calibrated：评分与结果大体一致。
- miscalibrated：评分与结果长期不一致，需要调整。

## Outcome-Score Check

当有 3+ real interview outcomes：

1. 对每场真实面试取最近一次相关 practice/mock/analyze 分数。
2. 对比结果：advanced / rejected / offer。
3. 看哪些维度和推进更相关。
4. 看外部反馈是否支持评分。
5. 找未测因素：状态、语速、热情、反问、岗位匹配、竞争强度。

不要把小样本相关性说成因果。

## Scoring Drift

如果外部反馈连续 2 次以上和教练评分冲突，记录到：

`## Calibration State` -> `### Scoring Drift Log`

示例：

| Date | Dimension | Direction | Evidence | Adjustment |
|---|---|---|---|---|

## Cross-Dimension Root Causes

同一根因影响多个维度时，记录到：

`### Cross-Dimension Root Causes (active)`

常见例子：

- 过度使用“我们”影响 Substance 和 Credibility。
- 回避冲突影响 Substance 和 Differentiation。
- 紧张影响 Structure 和 Relevance。

处理原则：一个根因用一个统一训练方案，不要拆成多个无关 drill。

## Success Pattern Analysis

有 advanced / offer 时，也要学习成功模式：

- 哪些故事有效。
- 哪些维度高时更容易推进。
- 哪类公司/岗位更匹配。
- 哪个表达策略应该保留。

## Role Drill Score Mapping

`practice role` 的专业分数需要映射回核心维度：

- 专业准确性 -> Substance / Technical Accuracy。
- 思考过程 -> Structure。
- 岗位贴合 -> Relevance。
- 个人贡献 -> Credibility。
- 独特判断 -> Differentiation。

## Rules

- 3 个真实结果前，只能做早期判断。
- 外部反馈高信号，但也要看具体程度。
- 校准结论要写入 `Calibration State`。
- 如果当前策略 3 次不动，建议 pivot。
