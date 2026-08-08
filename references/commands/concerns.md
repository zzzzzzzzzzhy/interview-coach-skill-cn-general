# concerns — Concern Anticipation Workflow

本文件用于 `concerns` 命令。目标是提前识别面试官可能担心什么，并准备直接问题、隐性试探和追问压力下的回应。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；诊断、回应话术和解释使用中文。

## Logic

先读取 `coaching_state.md`，不要凭空生成顾虑。顾虑来源包括：

- `## Resume Analysis`：空窗、短经历、转岗、学历/经验不匹配、简历主线混乱。
- `## Storybank` / `## Project Bank`：能力缺口、故事过弱、项目讲不深。
- `## Score History`：长期低分维度。
- `## Outcome Log`：真实拒绝或推进结果。
- `## Interview Intelligence`：面试官反馈、重复出现的问题。
- JD / prep brief：目标岗位明确要求但候选人证据不足的部分。

第一步仍然先问候选人：

“你自己最担心面试官质疑你哪一点？”

然后再补充候选人没看到的风险。

## Severity Ranking

每个 concern 必须分级：

- Dealbreaker：如果处理不好，可能单独导致失败。
- Significant：大概率会被问，需要强回应，但不是单点致命。
- Minor：可能被轻微试探，一句话回应即可。

## Counter Strategy

对 Dealbreaker 和 Significant，准备三种场景：

- Counter (direct question)：面试官直接问时怎么答。
- Counter (subtle probe)：面试官绕着问时怎么识别并回应。
- Counter (follow-up challenge)：面试官继续质疑时怎么稳住。

回答原则：

- 先承认事实，不逃避。
- 迅速转向证据和行动。
- 不防御，不甩锅，不卖惨。
- 用具体经历证明风险已经降低。

## Output Schema

```markdown
## Likely Interviewer Concerns (ranked by severity)

### Dealbreakers
1. Concern:
   Severity: Dealbreaker
   Source:
   Counter (direct question):
   Counter (subtle probe):
   Counter (follow-up challenge):
   Best story:

### Significant
2. Concern:
   Severity: Significant
   Source:
   Counter (direct question):
   Counter (subtle probe):
   Counter (follow-up challenge):
   Best story:

### Minor
3. Concern:
   Severity: Minor
   Source:
   Counter (one-liner):

## Practice Option
[中文说明是否建议立刻练 top concern]

## Save
Update:
- Interview Loops (active):
- Active Coaching Strategy:
- Session Log:

**Recommended next**: `practice pushback` — 把最高风险顾虑放到压力追问里练一遍。 **Alternatives**: `prep [company]`, `mock [format]`, `stories`
```

## Immediate Practice Option

生成 concerns 后，主动提供练习：

“最大的风险是 [X]。建议现在直接练一轮：我会先问直接版，再问隐性试探版，最后追问挑战版。”

如果候选人同意，转 `practice pushback`，练 2-3 轮。

## Rules

- 不要把普通弱点夸大成 Dealbreaker。
- 不要只给安慰，要给可说出口的回应。
- 不编造反证；没有反证时写“当前缺证据，需要补故事/项目”。
- 生成后的 top concerns 要写入对应公司 `Interview Loops` 或 `Active Coaching Strategy`。
