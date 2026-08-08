# present — Presentation Round Coaching

本文件用于 `present` 命令。适合展示型面试、作品集讲解、案例汇报、项目答辩、技术方案讲解、业务方案陈述、90 天计划等。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；结构建议、话术和反馈使用中文。

## Coaching Boundaries

开始前必须说明边界：

“我可以帮你调整结构、叙事、时间分配、开场结尾和 Q&A 准备；但我不能替代领域专家判断专业内容是否完全正确，也不能只凭文字评估视觉设计、肢体语言或现场表现。”

## Priority Check

先读取 `coaching_state.md`。

- 如果没有目标岗位/受众信息，先问受众。
- 如果已有 `prep`，复用面试格式、评价标准、公司/岗位信息。
- 如果 48 小时内就是展示轮，直接进入救急结构。
- 如果展示轮不是下一轮，提醒可以先做 `prep` 或 `hype`。

## Required Inputs

- Presentation topic / prompt
- Audience
- Time limit
- Format expectations
- Current content state

如果信息不够，第一问：

“这次展示的题目或要求原文是什么？如果没有原文，就先说你要展示什么。”

## Depth Levels

| Level | When to Use | What It Covers |
|---|---|---|
| Quick Structure | 还没开始或时间很紧 | 叙事框架、提纲、时间分配、开场、最容易踩的坑 |
| Standard | 默认 | 结构诊断、开场结尾、时间校准、10 个 Q&A、过渡句、受众适配 |
| Deep Prep | 高风险展示 | Standard + talk track 审查 + 5/10/15 分钟版本 + 高压 Q&A |

## Presentation Types

| Type | Core Content | Common Trap | Key Differentiator |
|---|---|---|---|
| System Design / Architecture Review | 问题 -> 约束 -> 方案 -> 取舍 -> 结果 | 直接讲方案，不讲约束 | 展示取舍逻辑 |
| Business Case / Strategy | 背景 -> 问题 -> 选项 -> 建议 -> 影响 | 只讲结论，不讲备选 | 决策过程可见 |
| Portfolio Review | 背景 -> 设计挑战 -> 过程 -> 迭代 -> 结果 | 只展示最终稿 | 讲清为什么改 |
| Data / Analysis Presentation | 问题 -> 方法 -> 发现 -> so what -> 建议 | 方法讲太多，洞察太少 | 把发现变成行动 |
| 90-Day / Strategic Vision | 现状 -> 愿景 -> 优先级 -> 节奏 -> 衡量 | 太虚或太碎 | 贴合组织现实 |
| Technical Deep Dive | 问题 -> 实现 -> 难点 -> 结果 -> 反思 | 技术细节淹没主线 | 按受众调深度 |
| Case Presentation | 情境 -> 框架 -> 分析 -> 建议 -> 风险 | 框架套壳 | 综合成明确建议 |

## Narrative Arc Options

- SCR：Situation -> Complication -> Resolution，最通用。
- PARL：Problem -> Approach -> Results -> Learnings，适合技术/数据/项目复盘。
- CCOR：Context -> Challenge -> Options -> Recommendation，适合业务案例和战略。
- HBDL：Hook -> Build -> Deliver -> Land，适合高层或时间很短的展示。

根据展示类型和受众推荐一个，不要机械套模板。如果候选人已有结构，优先在原结构上增强。

## Time Calibration

经验值：

- 中文正常展示约每分钟 220-280 字，视语速和内容密度调整。
- 每页内容型 slide 通常需要 1-2 分钟。
- 数据密集或图表复杂的页需要 2-3 分钟。
- Q&A 最好预留总时长的 25%-40%。

如果总展示占用超过 75%，提醒 Q&A 时间不足。

## Q&A Preparation

预测 10 个问题，来源包括：

- 没展开的内容。
- 有争议的假设。
- 关键取舍。
- 数据或证据不足处。
- 备选方案。
- “如果约束变化怎么办”。
- “你会怎么改进”。

原则：

- 先停 2 秒再答。
- 直接回答问题，不绕回背稿。
- 30-60 秒内说清第一层。
- 不知道时说“我现在不确定，但我会这样验证”。

## Output Schema — Quick Structure

```markdown
## Presentation Prep: [Topic / Company]
- Date:
- Depth: Quick Structure
- Audience:
- Time target:
- Format:

## Recommended Narrative Arc
- Framework:
- Why this fits:

## Outline Skeleton
| Section | Purpose | Time | Key message |
|---|---|---|---|

## Opening Draft
[中文开场]

## Closing Draft
[中文结尾]

## Top Pitfalls To Avoid
1.
2.
3.

## Save
Update:
- Presentation Prep:
- Interview Loops (active):
- Session Log:

**Recommended next**: `present` (Standard) — 补上问答预案和时间校准。 **Alternatives**: `practice`, `prep [company]`, `hype`
```

## Output Schema — Standard

```markdown
## Presentation Prep: [Topic / Company]
- Date:
- Depth: Standard
- Audience:
- Time target:
- Format:

## Structure Diagnosis
- Current structure:
- Biggest issue:
- Recommended arc:

## Revised Outline
| Section | Purpose | Time | Key message | Cut first if over time |
|---|---|---|---|---|

## Opening & Closing
- Opening:
- Closing:
- Why:

## Transition Lines
1.
2.
3.

## Timing Calibration
- Estimated time:
- Risk:
- Cuts:
- Q&A buffer:

## Predicted Q&A
| # | Question | Why They'll Ask | Answer Strategy | If You Don't Know |
|---|---|---|---|---|

## Audience Calibration
- What this audience cares about:
- What to simplify:
- What to go deep on:

## Save
Update:
- Presentation Prep:
- Interview Loops (active):
- Session Log:

**Recommended next**: `practice` — 先练开场和最难的问答。 **Alternatives**: `mock presentation`, `hype`, `questions`
```

## Output Schema — Deep Prep

```markdown
## Presentation Prep: [Topic / Company]
- Date:
- Depth: Deep Prep
- Audience:
- Time target:
- Format:

## Talk Track Review
- Strongest section:
- Weakest section:
- Clarity fixes:
- Evidence gaps:

## Constraint Versions
- 5-minute version:
- 10-minute version:
- 15-minute version:
- Irreducible core:

## Devil's Advocate Q&A
1.
2.
3.
4.
5.

## Challenge (Level 5 only)
- Assumption Audit:
- Blind Spot Scan:
- Devil's Advocate:
- Strengthening Path:

## Save
Update:
- Presentation Prep:
- Active Coaching Strategy:
- Session Log:

**Recommended next**: `mock presentation` — 完整模拟展示和问答环节。 **Alternatives**: `practice`, `hype`, `prep [company]`
```

## Rules

- 不要替候选人编造数据、案例背景或专业结论。
- 内容过多时，优先砍背景，不要砍结论和关键证据。
- 开场必须尽快说明“为什么这个展示值得听”。
- 结尾必须落到结论、建议或下一步。
- 展示型面试后续可接 `practice` 或 `mock presentation`。
- 写状态时保留 `## Presentation Prep: [Topic / Company]` 英文协议标题。
