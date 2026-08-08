# stories — Storybank Workflow

本文件用于 `stories` 命令。目标是把候选人的经历沉淀成可复用的面试故事库。命令名、ID、状态章节名和 Output Schema 标题保持英文；故事正文和反馈用中文。

## Logic

先读取 `coaching_state.md` 和 `references/storybank-guide.md`。如果没有状态文件，提醒先运行 `kickoff`，但如果候选人已经主动提供故事，也可以先帮他整理，并在之后创建状态。

## Menu

```text
Storybank Menu
1) View
2) Add
3) Improve
4) Find gaps
5) Retire/archive
6) Drill — rapid-fire retrieval practice
7) Narrative identity — extract your career themes and see how stories connect
```

向中文用户解释菜单时可以写：

- `View`：查看故事库
- `Add`：新增经历故事
- `Improve`：打磨已有故事
- `Find gaps`：找能力覆盖缺口
- `Retire/archive`：归档弱故事
- `Drill`：快速匹配题目和故事
- `Narrative identity`：提炼个人核心叙事

## Adding Stories

候选人选择 `Add` 时，不要直接要求 STAR。大多数人一上来讲不出好故事。先用引导问题找素材，一次只问一个：

- 最近一次你觉得“我真的解决了问题”的经历是什么？
- 有没有一次你被迫扛起责任、协调别人或推动结果？
- 有没有一次失败、返工、被质疑、压力很大的经历？
- 有没有一次你做了一个别人没想到的判断？
- 有没有一个项目/活动/任务，结果比预期好或差很多？

听到有价值的素材后，说：

“这个可以沉淀成一个故事。我们先把它按 STAR 拆出来。”

然后收集：

- Situation：背景和约束
- Task：你的目标/责任
- Action：你具体做了什么
- Result：结果和证据
- Earned Secret：这段经历让你形成了什么独特判断
- Deploy for：适合回答哪类问题

必须把完整故事写入 `## Storybank` 和 `### Story Details`，不要只写表格索引。

## Improving Stories

候选人选择 `Improve` 时，先读已有故事，再评分并诊断：

- 1-2 分：素材不足。追问真实细节、难点、结果和个人动作。
- 3 分：骨架有了，但证据不够。补指标、取舍、冲突、反馈。
- 4 分：已经可信，但不够有记忆点。补 Earned Secret、反直觉判断、个人方法论。
- 5 分：可用于高压面试。训练压缩版本和追问回应。

不要整篇大改。优先修改最拖分的一段，并展示 before/after。

## Find Gaps

做故事库缺口分析时，要结合目标岗位/JD，而不是泛泛列能力。

按重要程度分：

- Critical Gaps：目标岗位高概率问到，但没有可用故事。
- Important Gaps：有故事但太弱，或只能勉强覆盖。
- Nice-to-Have：可能问到，但不是决定性。

如果已有故事能迁移，要建议重新包装；如果没有真实经历，使用诚实的 gap-handling 策略，不编造。

## Drill

`stories drill` 是快速检索训练：

1. 连续给 10 个常见面试问题。
2. 候选人每题 10 秒内回答：故事 ID + 开场句。
3. 记录卡壳、重复使用、错配和没有故事覆盖的问题。
4. 更新 `coaching_state.md` 的 Storybank、Drill Progression 和 Coaching Notes。

## Narrative Identity

当候选人有 5 个以上故事时，可以做个人核心叙事提炼：

1. 阅读所有故事的完整 STAR 和 Earned Secret。
2. 找 2-3 个跨故事重复出现的深层主题。
3. 找最有记忆点的 sharpest edge。
4. 标出孤立故事和脆弱主题。
5. 给出如何在自我介绍、简历、面试回答中统一表达的建议。

## Output Schema

**After `stories add`:**

```markdown
## Story Added: [Title]
- ID: S###
- Primary Skill:
- Earned Secret:
- Strength: [1-5]
- Deploy for:

## Story Red Team (Level 5 only)
- Assumption:
- Blind spot:
- Failure mode:
- Attack surface:
- Fix:

**Recommended next**: `stories improve S###` — 根据红队发现补强这个故事。 **Alternatives**: `stories find gaps`, `practice retrieval`, `concerns`
```

**After `stories improve`:**

```markdown
## Story Improved: [Title] (S###)
- Previous strength: __ -> New strength: __
- What changed:
- Version history updated

## Story Red Team (Level 5 only)
- Assumption:
- Blind spot:
- Failure mode:
- Attack surface:
- Fix:

**Recommended next**: `practice` — 把改好的故事放到压力追问里测试。 **Alternatives**: `stories view`, `stories improve S###`, `analyze`
```

**After `stories find gaps`:**

```markdown
## Storybank Gap Analysis
### Critical Gaps (must fill for target roles)
1. [competency] — [why it matters]. Recommended: [surface new story / reframe existing S###]

### Important Gaps (likely to come up)
1. [competency] — [current coverage and weakness]

### Nice-to-Have (might come up)
1. [competency]

**Recommended next**: `stories add` — 先补最高优先级的故事缺口。 **Alternatives**: `practice gap`, `prep [company]`
```

**After `stories narrative identity`:**

```markdown
## Your Narrative Identity

### Core Themes
1. **[Theme]** — [one-line description]. Stories: S###, S###
2. **[Theme]** — [one-line description]. Stories: S###, S###

### Your Sharpest Edge
[中文说明最有辨识度的主题]

### Theme Coverage
- Stories reinforcing a theme:
- Orphan stories:
- Fragile themes:

### How To Use This
- **In answers**:
- **In questions you ask**:
- **In positioning**:

**Recommended next**: `stories improve S###` — 优先打磨最有辨识度、也最容易被追问的故事。 **Alternatives**: `stories add`, `practice`, `prep [company]`
```

## Rules

- 不编造故事。
- 每个故事必须有候选人个人动作。
- 尽量补充结果证据；没有量化指标时，说明证据不足并寻找替代证明。
- 不要把所有故事都包装成“领导力”，要贴合岗位。
- 写状态时保留 `## Storybank`、`### Story Details`、`S###` 等英文协议。
