# pitch — Core Positioning Statement

本文件用于 `pitch` 命令。目标是打磨候选人的核心定位：我是谁、我适合什么岗位、我和普通候选人有什么不同。

`pitch` 产出的 Positioning Statement 会被 `resume`、`linkedin`、`outreach`、`prep` 和 `mock` 复用，所以必须稳定、真实、可证明。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；定位表达和解释使用中文。

## Priority Check

执行前先读取 `coaching_state.md`。

- 没有 `kickoff`：可以继续，但提醒缺少完整上下文。
- 48 小时内有面试：建议优先 `prep` / `hype`，除非用户明确要改自我介绍。
- `Storybank` / `Project Bank` 为空：可以基于简历做初版，但标注证据不足。
- 已有 `Positioning Statement`：先判断是优化、改目标岗位，还是生成新场景版本。

## Required Inputs

- Target role context
- Candidate background
- Strongest evidence
- Intended audience

如果信息不足，第一问：

“这版 pitch 主要给谁听：面试官、HR、招聘会、社交介绍，还是简历/主页开头？”

## Depth Levels

| Level | When to Use | What It Covers |
|---|---|---|
| Quick Draft | 急用，需要马上有一版 | Core Statement + Hook + 1-2 个场景版本 |
| Standard | 默认 | Core Statement + 5 个场景版本 + 一致性检查 |
| Deep Positioning | 转岗、重定位、高风险求职 | Standard + 差异化审计 + 15/30/60/90 秒压缩梯度 |

## Positioning Principles

1. 不要按时间顺序复述简历。
2. 第一秒要让人知道你和岗位的关系。
3. 先讲当前定位，再讲过去证据，最后连接未来目标。
4. 差异化必须来自真实经历，不要写空泛人设。
5. 好 pitch 像谈话开场，不像背稿。

推荐结构：

`Hook -> Evidence -> Bridge`

- Hook：一句话打开兴趣。
- Evidence：用经历、项目、成果或方法证明。
- Bridge：连接到目标岗位/公司/场景。

面试自我介绍可用：

`Present -> Past -> Future`

- Present：我现在是谁，主能力是什么。
- Past：我为什么可信，有什么证据。
- Future：我为什么来这个岗位。

## Diagnostic Dimensions

如果候选人提供了已有 pitch，按 1-5 分评估：

- Hook strength
- Differentiation
- Specificity
- Audience fit
- Memorability

## Output Schema — Quick Draft

```markdown
## Positioning Statement — Quick Draft

## Core Statement (30-45s)
[中文完整版本]

## Hook (10s)
[一句话钩子]

## Key Differentiator
[一句话说明候选人最不同的地方]

## Context Variants

### Interview TMAY (60-90s)
[面试自我介绍版本]

### [Requested Context] ([duration])
[指定场景版本]

## Save
Update:
- Positioning Statement:
- Session Log:

## Next Step
**Recommended next**: `pitch` (Standard) — 补齐 5 个场景版本，并检查个人定位是否一致。 **Alternatives**: `stories`, `prep [company]`, `resume`
```

## Output Schema — Standard

```markdown
## Positioning Statement: [Name]

## Core Statement (30-45s)
[Hook + Evidence + Bridge]

## Hook (10s)
[最短版本]

## Key Differentiator
[候选人的核心差异化]

## Earned Secret Anchor
[来自 Storybank / Project Bank / Resume Analysis 的真实证据]

## Pitch Diagnostic (if existing pitch was provided)
| Dimension | Score (1-5) | Notes |
|---|---|---|
| Hook strength | | |
| Differentiation | | |
| Specificity | | |
| Audience fit | | |
| Memorability | | |
- Primary weakness:

## Context Variants

### 1. Interview TMAY (60-90s)
[Present-Past-Future]

### 2. Networking Event (30-45s)
[Hook-Context-Ask]

### 3. Recruiter Call (30-60s)
[关键词清晰，说明目标]

### 4. Career Fair (30-60s)
[高密度、好记、能引发下一问]

### 5. LinkedIn Summary Hook (~300 chars)
[适合阅读的中文/中英版本，视用户需求]

## Positioning Consistency Check
- Resume:
- LinkedIn:
- Storybank / Project Bank:
- Interview answers:

## Save
Update:
- Positioning Statement:
- Active Coaching Strategy:
- Session Log:

**Recommended next**: `resume` — 把简历开头和经历 bullet 对齐到这个定位。 **Alternatives**: `stories`, `practice`, `prep [company]`
```

## Output Schema — Deep Positioning

```markdown
## Positioning Statement: [Name]

## Core Statement
[中文核心定位]

## Constraint Ladder
- 10s:
- 30s:
- 60s:
- 90s:
- Irreducible core:

## Differentiation Audit
- Is the differentiator defensible:
- Spiky enough:
- Earned vs. borrowed:
- Substitution test:
- Biggest weakness:

## Challenge (Level 5 only)
- Assumption Audit:
- Blind Spot Scan:
- Devil's Advocate:
- Strengthening Path:

## Save
Update:
- Positioning Statement:
- Active Coaching Strategy:
- Coaching Notes:
- Session Log:

**Recommended next**: `practice` — 把 60-90 秒版本练到像自己的话，而不是背稿。 **Alternatives**: `resume`, `stories`, `mock`
```

## Rules

- 不要写候选人无法自然说出口的话。
- 不要为了高级感堆抽象词。
- 不编造成果、身份、行业洞察或个人方法论。
- 如果定位听起来任何候选人都能说，必须重写。
- 写入状态时保留 `## Positioning Statement` 英文标题。
