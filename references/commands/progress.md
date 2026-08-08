# progress — Trend Review Workflow

本文件用于 `progress` 命令。目标是做阶段复盘：看分数趋势、真实面试结果、故事库/项目库健康度、自评校准、目标匹配和下一阶段训练策略。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；趋势解释、判断和建议使用中文。

## Minimum Data Thresholds

先读取 `coaching_state.md`，判断数据量。不要在数据不足时硬套完整报告。

| Data Available | What You Can Do | What You Can't Do |
|---|---|---|
| 0 scored sessions | 说明还没有可复盘数据，推荐 `practice` 或 `analyze` | 趋势分析、结果相关性、毕业判断 |
| 1 scored session | 建立 baseline，指出初始优先级 | 趋势叙事、稳定模式判断 |
| 2-3 scored sessions | 看早期方向：提升、持平、下降 | 强相关结论、长期趋势 |
| 4+ scored sessions | 做完整趋势叙事和平台期诊断 | 若真实面试少于 3 个，不能做 outcome correlation |
| 3+ real interview outcomes | 做结果相关性、目标匹配和校准分析 | 基本完整可用 |

数据少时要说：

“现在数据还不够做完整趋势复盘。我能看的是当前 baseline 和最高优先级；要做可靠趋势，至少还需要 2-3 次 `practice` 或 `analyze` 数据。”

## Sequence

1. 检查 `Score History`、`Session Log`、`Interview Intelligence` 是否太长。超过阈值时按 archival rules 压缩旧记录。
2. 检查数据量，决定 full review 还是 light review。
3. 先让候选人自评：  
   “你自己感觉最近进步最大的是哪块？最卡的是哪块？”
4. 独立读取历史分数，不被自评带偏。
5. 叙述趋势，不只列数字。
6. 比较自评分和教练评分，判断 over-rater / under-rater / well-calibrated。
7. 如果有 3+ 个真实面试结果，做 outcome correlation。
8. 分析故事库/项目库健康度。
9. 检查当前 `Active Coaching Strategy` 是否有效。
10. 如果目标岗位或结果显示方向不匹配，给 targeting insights。
11. 判断是否达到 interview-ready 或 competitive-ready。
12. 给下一阶段训练计划。
13. 每 3 次 session 或候选人明显卡住时，做 meta-check，并写入 `Meta-Check Log`。

## Trend Narration

趋势复盘必须讲成“轨迹”，不要只给表格。

要包含：

- Direction：提升、持平、下降。
- Inflection point：哪次训练或哪类问题导致变化。
- Plateau diagnosis：如果卡住，可能卡在哪里。
- Next unlock：下一次分数提升的具体抓手。
- Emotional context：如果候选人感觉和数据不一致，要指出。

例：

“Structure 从 2.8 到 3.6，主要提升来自你开始用‘结论先行 + 三段证据’回答。但最近两次停在 3.6 左右，说明结构框架已经够用，下一步不是继续背模板，而是补 Substance：每个回答要多一个真实细节或取舍。”

## Self-Assessment Calibration

比较候选人自评和实际评分：

- over-rater：自评长期高于实际表现，说明可能看不到面试官视角。
- under-rater：自评长期低于实际表现，说明可能有信心问题或面试焦虑。
- well-calibrated：自评和评分接近，可以把重点放在执行稳定性。

这个部分很重要，因为很多人不是不会答，而是不知道自己到底答得怎样。

## Outcome Correlation

当有 3+ 个真实面试结果时，分析：

- 哪些维度和推进相关。
- 哪些维度和拒绝相关。
- 外部反馈是否和评分一致。
- 是否存在未被评分覆盖的因素，如精神状态、语速、热情、反问质量、岗位不匹配。

不要把相关性说成因果。用“目前数据暗示”。

## Targeting Insights

当结果集中出现在某类公司、岗位、行业、轮次时，判断是否是目标选择问题，而不是单纯面试能力问题。

例：

- 简历无回音：可能是简历/JD 匹配问题。
- 一面反复挂：可能是基础表达、岗位理解或硬技能问题。
- 终面反复挂：可能是差异化、动机、稳定性或团队匹配问题。
- 某类公司全挂、另一类公司能进：可能是 target fit 问题。

## Graduation Criteria

Interview-ready：

- 近期多个维度达到 4 左右。
- 没有长期低于 3 的关键维度。
- 关键问题都有可用故事/项目。
- 能处理追问和 gap question。
- 自评基本校准。

Competitive-ready：

- 主要维度稳定 4+。
- 有 2-3 个强差异化故事或项目。
- 能压缩/展开回答。
- 能承受质疑而不慌。
- 真实面试推进率支持当前策略。

## Output Schema

```markdown
## Progress Snapshot
- Sessions analyzed:
- Real interviews completed:
- Real interview outcomes: __ advanced / __ rejected / __ pending
- Current trend: Improving / Flat / Regressing

## Your Trajectory (narrated, not just numbers)
- Substance:
- Structure:
- Relevance:
- Credibility:
- Differentiation:
- Format-specific / role-specific dimensions:

## Hard Truth (Level 5 only)
[一段中文直说当前最重要的不舒服事实。只在 Level 5 使用。]

## Self-Assessment Calibration
- Pattern: [over-rater / under-rater / well-calibrated / not enough data]
- Evidence:
- What this means for your prep:

## Outcome Correlation (if 3+ real interviews exist)
- Dimensions that predict advancement:
- Dimensions linked to rejections:
- Feedback-to-dimension mapping:
- Unmeasured factors to investigate:

## Targeting Insights (if 3+ outcomes exist)
- Rejection pattern:
- Stage analysis:
- Feedback signals:
- Fit assessment accuracy:
- Recommendation:

## Storybank / Project Bank Health
- Coverage:
- Strongest assets:
- Weak or overused materials:
- Critical gaps:

## Active Coaching Strategy Review
- Current strategy:
- Is it working:
- Keep / pivot:
- New strategy:

## Graduation Check
- Interview-ready criteria:
- Competitive-ready criteria:
- Current verdict:

## Next Training Plan
### Next 72 Hours
1.

### This Week
1.
2.
3.

### Evidence To Collect
-

## Meta-Check
[如果触发：Is this feedback useful? Are we working on the right things? What's not clicking?]

## Save
Update:
- Active Coaching Strategy:
- Calibration State:
- Score History summary, if archived:
- Session Log:
- Meta-Check Log, if used:
- Coaching Notes:

**Recommended next**: `[command]` — [写出当前收益最高的一步，并说明中文理由]. **Alternatives**: `practice`, `stories`, `project`, `mock`
```

## Recommended Next Logic

- 没有分数：`practice`
- 有文字稿没分析：`analyze`
- Relevance 低：`practice pivot`
- Substance 低：`stories` 或 `project`
- Structure 低：`practice ladder`
- 技术准确性低：`basics` 或 `algorithm`
- 故事/项目库空：`stories` 或 `project`
- 面试即将到来：`prep` 或 `hype`
- 目标匹配可疑：`decode`

## Rules

- 数据不足时不要假装有趋势。
- 趋势要讲原因，不只报分数。
- outcome correlation 至少需要 3 个真实面试结果。
- 如果当前策略连续 3 次不动，要建议 pivot。
- 状态写入保持 `## Active Coaching Strategy`、`## Calibration State`、`## Session Log` 等英文协议标题。
