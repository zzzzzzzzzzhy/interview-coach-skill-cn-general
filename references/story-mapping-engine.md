# Story Mapping Engine

本文件定义如何把 Storybank / Project Bank 映射到预测问题和岗位能力。

## Fit Levels

| Fit | Meaning |
|---|---|
| Strong Fit | 故事直接回答问题，能力信号强，证据充分 |
| Workable | 能回答，但需要调整 framing |
| Stretch | 只能间接回答，有风险 |
| Gap | 没有合适故事，需要 gap-handling |

## Mapping Process

1. 读取目标 JD 或 `prep` 的 top competencies。
2. 读取 `## Storybank` 和 `## Project Bank`。
3. 同时检查 Primary Skill 和 Secondary Skill。
4. 对每个预测问题列出 1-2 个候选故事/项目。
5. 检查 freshness：同家公司是否已经用过。
6. 检查 overuse：Use Count 是否过高。
7. 如果多个问题都依赖同一个故事，做 portfolio optimization，避免全场重复。
8. 对没有故事的问题，指定 Gap-Handling Pattern。

## Output Pattern

```markdown
| Question | Competency | Best story/project | Fit | Risk | Backup |
|---|---|---|---|---|---|
```

## Portfolio Rules

- 一场面试不要所有问题都用同一个故事。
- 强故事优先给最高风险问题。
- 新鲜度比机械匹配更重要：同家公司前一轮刚用过的故事，下一轮慎用。
- 项目可以服务技术深挖，故事可以服务行为题；有时同一素材可以两用，但表达角度不同。

## Gap Handling

如果 Fit = Gap：

- 有相邻经历：Adjacent Bridge。
- 没有经历但有思考：Hypothetical with Self-Awareness。
- 是成长项：Growth Narrative。
- 可以转向强项：Reframe to Strength。

## Rules

- 不要强行把无关故事塞给问题。
- 不要自动选择故事后不解释原因。
- 映射结果要能指导 `practice` 和 `mock`。
