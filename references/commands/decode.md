# decode — JD Analysis and Fit Triage

本文件用于 `decode` 命令。目标是把岗位 JD 拆成“面试和简历该证明什么”。用户可见内容用中文；命令名、状态章节和 Output Schema 标题保持英文。

## Logic

如果用户没有提供 JD，第一问：

“把 JD 粘过来。如果你有 2-5 个岗位想比较，也可以一起粘。”

如果用户只给公司名，不要编造 JD。可以建议提供岗位链接或岗位描述；如需要公司信息，再转 `research [company]`。

## Decode Lenses

分析 JD 时使用六个镜头：

1. Repetition：反复出现的词通常是核心要求。
2. Order and emphasis：靠前、加粗、单独成段的要求优先级更高。
3. Required vs nice-to-have：区分硬门槛和加分项。
4. Verb choices：动词暴露岗位真实工作方式，如“搭建”“推动”“分析”“交付”“维护”。
5. Between-the-lines signals：从职责组合推断压力点，但必须标置信心。
6. What is missing：JD 没写但面试可能会问的基础能力。

## Fit Assessment

结合 `coaching_state.md`、简历、故事库、项目库判断匹配：

- Strong Fit：核心要求大多有证据。
- Investable Stretch：有差距，但可以通过材料和准备补足表达。
- Long-Shot Stretch：差距明显，适合少量冲刺，不宜投入过多。
- Weak Fit：缺关键硬条件，除非有特殊渠道或强动机，否则不优先。

每个判断都给 Confidence：High / Medium / Low。

## Batch Triage

如果用户提供 2-5 个 JD，做批量比较：

- 哪个最适合投
- 哪个需要定制简历
- 哪个是冲刺
- 哪个暂时不值得花时间

不要只按公司名排序，要按候选人证据和岗位要求匹配排序。

## Output Schema

```markdown
## JD Analysis（JD 分析）: [Company] — [Role]
- 日期:
- 分析深度:
- 匹配判断: [中文判断 + 英文协议值，如 强匹配（Strong Fit）]
- 判断置信度: [高（High）/ 中（Medium）/ 低（Low）]

## What This Role Really Wants（这个岗位真正想要什么）
1.
2.
3.

## Competency Map（能力匹配表）
| 能力项 | 岗位需要的证据 | 候选人已有证据 | 差距 | 置信度 |
|---|---|---|---|---|

## Hidden Signals（隐藏信号）
| JD 信号 | 可能意味着什么 | 置信度 | 如何验证 |
|---|---|---|---|

## Fit Assessment（匹配判断）
- 强匹配信号:
- 可包装/可弥补差距:
- 结构性差距:
- 整体判断:

## Resume Targeting（简历定向）
- 需要露出的关键词:
- 应重点突出的经历/项目:
- 建议重写的 bullet:
- 没准备好前避免写的主张:

## Interview Prep Implications（面试准备重点）
- 可能被问的问题:
- 需要准备的故事/项目:
- 需要提前回应的顾虑:

## Recruiter Verification Questions（给招聘方/面试官的确认问题）
1.
2.
3.

## Save To Coaching State
Update:
- JD Analysis: [Company] — [Role]
- Interview Loops (active), if the candidate is applying or interviewing
- Active Coaching Strategy
- Session Log

**Recommended next**: `resume` — 先按 JD 信号定制简历，再进入练习。 **Alternatives**: `project`, `stories`, `prep [company]`
```

## Batch Output Schema

```markdown
## JD Batch Triage

| Rank | Company / Role | Fit verdict | Why | Best next action |
|---|---|---|---|---|

## Best Bet
[中文说明最值得优先投入的岗位]

## Stretch Bets
[中文说明可冲刺但需要补证据的岗位]

## Low-ROI Targets
[中文说明暂时不建议重点投入的岗位]

**Recommended next**: `resume` — 先针对排序最高的 JD 定制简历。 **Alternatives**: `decode`, `project`, `stories`
```

## Rules

- 不要编造公司文化、面试流程或岗位细节。
- JD 推断必须标 Confidence。
- 区分“可包装差距”和“硬性结构差距”。
- 对通用岗位也要落到可执行动作：改哪段简历、准备哪类故事、练哪类问题。
- 面向用户的 JD 分析字段用中文标签；写入状态时保持 `## JD Analysis: [Company] — [Role]` 英文协议格式。
