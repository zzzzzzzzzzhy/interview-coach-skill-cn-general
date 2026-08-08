# practice — Targeted Drill Workflow

本文件用于 `practice` 命令。目标是进行单题或单能力训练，而不是完整模拟面试。用户可见内容用中文；命令名、状态章节和 Output Schema 标题保持英文。

## Logic

先读取 `coaching_state.md`。如果存在目标岗位、JD、故事库、项目库或弱项记录，练习题必须贴合当前状态。

如果用户只说“练一下”，先问一个问题：

“你想练哪一类：自我介绍、项目/经历、行为题、专业题、压力追问，还是按目标岗位随机来一题？”

不要一次给一大串问题。每轮只问一题，等待回答，然后反馈。

## Drill Types

可识别以下练习模式：

- `practice ladder`：约束阶梯，从 30 秒到 90 秒，再到追问。
- `practice pushback`：面试官质疑/反问训练。
- `practice pivot`：把不熟的问题转回强证据。
- `practice gap`：没有直接经历时如何诚实回答。
- `practice retrieval`：快速把问题匹配到故事/项目 ID。
- `practice role`：按目标岗位做专业问题。
- `practice panel`：多面试官、多视角追问。
- `practice stress`：高压、打断、连续追问。
- `practice technical`：技术表达、系统设计、项目原理、代码口述。

如果用户没有指定模式，根据状态选择：

- 故事库薄弱：`practice retrieval`
- 项目讲不清：`practice pushback` 或 `practice technical`
- 一面挂：`practice ladder`
- 终面/HR 面：动机、稳定性、冲突、压力题
- 产品/运营/市场：案例拆解、数据复盘、协作推动
- 销售/客户成功：异议处理、客户需求、推进节奏
- 设计：作品集讲述和设计取舍

## Per-Round Flow

1. 出一题。
2. 等候选人回答。
3. 先复述 `What I Heard`。
4. 给 `What Is Working`。
5. 给 `Gaps To Close`。
6. 按岗位维度评分。
7. 给一个更强版本或修改方向。
8. 追问一题或建议下一轮。
9. 必要时更新 `coaching_state.md`。

## Scorecard

通用练习用：

- Content Quality
- Structure
- Role Relevance
- Credibility
- Differentiation

技术练习用：

- Technical Accuracy
- Project Depth
- Personal Contribution
- Expression Structure
- JD Match

算法专项使用 `algorithm` 命令，不在这里完整解题。

写入 `## Score History` 时，按 `references/cross-cutting.md` 的 Score Mapping Module 映射到 `Sub`、`Str`、`Rel`、`Cred`、`Diff`，不要新增中文表头。

## Output Schema

```markdown
## Practice Round（练习轮次）: [Topic]

## Question（问题）
[只问一个问题]

## Candidate Answer（候选人回答）
[等待候选人回答后再继续]

## What I Heard（我听到的重点）
[中文复述候选人回答]

## What Is Working（有效部分）
-

## Gaps To Close（需要补强）
-

## Scorecard（评分）
- 内容质量 / 技术准确性:
- 表达结构 / 项目深度:
- 岗位相关性 / 个人贡献:
- 可信度 / 表达结构:
- 差异化 / JD 匹配:

## Interviewer Read（面试官可能怎么理解）
[中文说明面试官可能怎么理解这个回答]

## Stronger Version（更强版本）
[中文示范版本。不得编造候选人没有提供的事实。缺事实处用占位提示。]

## Next Rep（下一轮练习）
[下一题或同题重答要求]

## Save
Update:
- Score History:
- Drill Progression:
- Weak Topics, if applicable:
- Coaching Notes, if applicable:
- Session Log:

**Recommended next**: `practice` — 同一模式再练一轮，把结构稳定下来。 **Alternatives**: `mock`, `stories`, `project`
```

## Rules

- 不要在候选人未回答前先给标准答案，除非用户明确要求“直接讲解”。
- 每轮只练一个问题或一个追问链。
- 反馈要具体到句子、证据和结构，不要只说“表达不够好”。
- 候选人卡壳时给提示，不要马上替他完成整段。
- Directness Level 5 可以更直接，但仍然给可执行修改。
- 面向用户的练习反馈字段用中文标签；状态写入仍保持英文协议字段。
