# research — Company / Organization Research Workflow

本文件用于 `research` 命令。目标是在正式 `prep` 前，帮助候选人了解目标公司、机构、团队或岗位方向，判断是否值得投入准备。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；研究结论和建议使用中文。

## When to Use Research vs. Prep

| Situation | Use |
|---|---|
| 还在判断要不要投 | `research` |
| 正在建立目标公司清单 | `research` |
| 已经有面试安排 | `prep` |
| 想了解公司/机构风格再决定是否联系 | `research` |
| 需要预测问题、故事匹配和临场清单 | `prep` |

## Logic

1. 确认 company / organization 和 target role type。
2. 优先读取 `coaching_state.md`，结合候选人画像判断 fit。
3. 调研公开信息。若需要最新信息，必须联网核实。
4. 所有公司特定结论必须标注来源强度。
5. 输出 research brief，并保存轻量记录到 `## Interview Loops (active)`。

## Research Depth Levels

| Level | When to Use | What to Do |
|---|---|---|
| Quick Scan | 批量筛公司、初步判断是否值得投 | 官网、招聘页、近期新闻，快速判断 fit |
| Standard | 默认 | 官网、招聘页、JD、新闻、员工/社区信息，形成完整简报 |
| Deep Dive | 高优先级目标或已有面试 | Standard + 高管/团队公开内容、产品/业务、竞品、员工经验 |

默认 `Standard`。

## Claim Verification Protocol

每条公司特定判断都要落到来源层级：

- Tier 1 — Verified：公司官网、招聘页、官方博客、候选人提供的 JD 或正式材料。
- Tier 2 — Public / Crowd-sourced：公开报道、Glassdoor/脉脉/牛客/LinkedIn 等社区信息，必须标注“非官方”。
- Tier 3 — Unknown：找不到可靠来源时明确说不知道。

规则：

- 信息冲突时同时列出，不做假共识。
- 超过 12 个月的信息标注可能过期。
- 不编造公司文化、面试流程、薪资、HC 或业务变化。

## Fit Assessment

没有 JD 时，只能做有限匹配判断：

- Seniority Alignment
- Domain Relevance
- Trajectory Coherence

不能完整判断：

- Requirement Coverage
- Competency Overlap

Fit verdict 使用：

- Strong Fit
- Investable Stretch
- Long-Shot Stretch
- Weak Fit

并给 Confidence：High / Medium / Low。

## Output Schema

```markdown
## Company Research: [Company]

## Company Snapshot
- Stage:
- Size:
- Industry:
- Recent signals:
- Sources:

## Culture Signals
- Public values/principles:
- What they seem to optimize for:
- Red flags or concerns:
- What I couldn't find:
- Confidence: High / Medium / Low

## Fit Assessment (vs. your profile)
- Verdict: [Strong Fit / Investable Stretch / Long-Shot Stretch / Weak Fit]
- Seniority Alignment:
- Domain Relevance:
- Trajectory Coherence:
- Cannot assess without JD: Requirement Coverage, Competency Overlap
- Key gaps:
- Better-fit alternatives:

## If You Decide to Apply
- Recommended next steps:
- Key things to research further before interviewing:
- Networking angle:

## Save
Update:
- Interview Loops (active):
- Active Coaching Strategy:
- Session Log:

**Recommended next**: `prep [company]` — 有 JD 或面试安排后，进一步生成完整面试准备简报。 **Alternatives**: `decode`, `research [another company]`, `stories`
```

## Staleness Detection

如果 `coaching_state.md` 已有该公司 research：

- 2 周内：询问是否刷新。
- 2-8 周：建议刷新变化信息。
- 8 周以上：默认视为过期，需要刷新。

刷新时保留旧 verdict，并说明这次是否改变。

## Rules

- 对公司现状、岗位开放、面试流程等可能变化的信息，必须联网核实或明确缺少来源。
- 没有 JD 时，不要做完整 fit assessment。
- research 是判断是否投入；prep 才是正式面试准备。
