# Transcript Processing

本文件定义 `analyze` 如何处理文字稿。

## Step 1: Clean

清理：

- 时间戳。
- 重复填充词。
- 明显转写噪音。
- 多余系统提示。

保留：

- 问题原意。
- 候选人的回答结构。
- 面试官追问。
- 停顿、打断、转向等有分析价值的信号。

## Step 2: Parse

按格式分流：

- Behavioral：Q#。
- Panel：E#。
- System Design：P#。
- Case Study：CS#。
- Technical+Behavioral Mix：按段落使用对应 ID。

## Step 3: Score

每个单元按核心五维评分：

- Substance
- Structure
- Relevance
- Credibility
- Differentiation

必要时增加格式维度：

- Process Visibility
- Scoping Quality
- Tradeoff Quality
- Mode-Switching Fluidity
- Interviewer Adaptation

## Step 4: Evidence

每个评分都要有证据：

- 原回答中的具体句子。
- 缺失的信息。
- 面试官追问或转向。
- 与 JD / storybank 的匹配或不匹配。

## Step 5: Triage

按优先级选择主瓶颈：

1. Relevance
2. Substance
3. Structure
4. Credibility
5. Differentiation

## Step 6: Rewrite

至少重写最低分回答：

- 保留候选人真实经历。
- 不编造事实。
- 说明改了哪里。
- 缺少数据处用占位符。

## Step 7: Save

更新：

- `## Score History`
- `## Interview Intelligence`
- `### Question Bank`
- `## Active Coaching Strategy`
- `## Session Log`

## Rules

- 不要被候选人自评带偏。
- 文字稿质量差时降低 Confidence。
- 分析必须可追溯到原文。
