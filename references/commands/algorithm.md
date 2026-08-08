# algorithm - Algorithm Interview Practice

本文件用于 `algorithm` 命令。适合 LeetCode、牛客、笔试编程题、现场编码和解题口述训练。命令名、状态章节和 Output Schema 标题保持英文；讲解和反馈用中文。

## Required Inputs

- Problem statement or topic
- Language
- Mode

Mode 可选：

- explain approach
- debug code
- mock interview
- written-test speed

如果用户只说“练算法”，第一问：

“你想用什么语言练：Java、C++、Python、JavaScript，还是其他？”

## Workflow

1. 明确题目、输入输出、约束和例子。
2. 先让候选人说暴力思路。
3. 通过提示引导到优化思路，不要一上来给完整答案。
4. 要求候选人说清数据结构、循环不变量、复杂度和边界。
5. 如果候选人给代码，先审实际代码行为，再给修改。
6. 评分并记录弱模式，如不会定义不变量、边界漏掉、直接写代码、不讲复杂度。

## Scoring

Score 1-5:

- Problem Understanding
- Approach Quality
- Code Correctness
- Complexity Analysis
- Explanation Clarity

更新状态时，可把 Explanation Clarity 映射到 Expression Structure。

## Output Schema

```markdown
## Algorithm Drill: [Problem/Topic]

## Clarifying Questions
1. [如有必要，只问一个澄清问题]

## Candidate Attempt
[等待候选人给思路或代码，除非用户要求直接讲解]

## Review
### What Is Working
-

### Bugs / Gaps
-

### Correct Approach
- Core idea:
- Data structure:
- Invariant:
- Edge cases:
- Complexity:

### Interview Narration
[中文口述模板：我会如何向面试官解释]

### Code Review
[指出正确性、边界、复杂度、可读性问题]

## Scorecard
- Problem Understanding:
- Approach Quality:
- Code Correctness:
- Complexity Analysis:
- Explanation Clarity:

## Pattern To Carry Forward
-

**Recommended next**: `algorithm` — 再练一道同类型题，把解题模式稳定下来。 **Alternatives**: `written`, `basics`, `mock technical`
```

## Rules

- mock interview 模式下不要直接泄题解。
- written-test speed 模式优先训练题型识别和稳定实现。
- interview 模式优先训练“澄清 -> 思路 -> 证明 -> 编码 -> 测试”的口述。
- 如果有代码，先分析原代码，不要直接替换成新答案。
