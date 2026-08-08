# analyze — Transcript Analysis Workflow

本文件用于 `analyze` 命令。目标是分析真实面试文字稿、问答记录或候选人整理的复盘文本，找出表现强项、风险点、根因和下一步训练路径。

中文化规则：命令名、文件名、状态章节名、Output Schema 标题保持英文；分析正文、解释、反馈和示范回答使用中文。

## Logic

执行前读取：

- `coaching_state.md`，如果存在
- `references/transcript-processing.md`
- `references/transcript-formats.md`
- `references/rubrics-detailed.md`
- `references/calibration-engine.md`
- `references/cross-cutting.md`

如果这些参考文件仍是英文，吸收其流程，但向候选人输出中文。

## Cold Start

如果候选人直接粘贴文字稿，但没有 `coaching_state.md`，不要拒绝，也不要强制先 `kickoff`。

先做三件事：

1. 从文字稿里推断岗位、轮次、面试类型和候选人经验阶段，并明确标注“这是推断”。
2. 分析前只问一个关键问题：  
   “这个面试大概是什么岗位和级别？这会影响我怎么校准分数。”
3. 如果候选人无法补充，也可以继续分析，但把 `Confidence` 降低。

分析结束后建议：

“这次我已经能基于文字稿给你复盘，但还缺少完整画像、故事库和目标岗位上下文。后面建议跑一次 `kickoff`，这样分数和训练计划能持续沉淀。”

## Comp Call Detection

分析前先判断这是不是薪资/offer 沟通，而不是普通面试。

薪资标记包括：salary、base、equity、bonus、offer、package、counter、negotiate、compensation、vesting、sign-on、stock、RSU、range、budget，以及中文的薪资、base、股票、期权、奖金、总包、谈薪、反 offer、预算、职级、范围。

- 3 个以上薪资标记：转为薪资沟通分析，参考 `negotiate`，不要用普通面试五维评分。
- 1-2 个薪资标记：按普通面试分析，但加入 “Salary handling” 简评。
- 面试 + 薪资混合：分别分析面试部分和薪资部分。
- 纯行政沟通：标注为 administrative call，不做面试评分。

## Step Sequence

1. 检查 `coaching_state.md` 是否已有对应 `debrief` 数据。
2. 分析前先问自评：  
   “我正式分析前，先听你的直觉：你觉得哪一题答得最好？哪一题最弱？整体感觉如何？”
3. 自评只用于校准，不影响评分。评分必须基于文字稿证据。
4. 识别文字稿格式：behavioral、panel、system design、case study、technical+behavioral mix，或普通问答记录。
5. 清理文字稿：去掉时间戳、重复语气词、明显转写错误，但不要改变候选人的核心意思。
6. 做质量检查：如果说话人不清、内容缺失、转写质量差，先说明能分析什么、不能分析什么。
7. 按问答单元解析：行为面用 Q#，多面官用 E#，系统设计用 P#，案例面用 CS#。
8. 每个单元评分，并标出证据。
9. 比较候选人自评和教练评分，找出自我感知偏差。
10. 分析面试官信号：追问、打断、转向、认可、质疑、时间控制等。
11. 对 Relevance 低于 3 的回答，解释“这道题真正想考什么”。
12. 自动重写最低分回答，展示从原回答到 4-5 分回答的改法。不能编造事实，缺事实处用占位提示。
13. 输出 Interviewer's Inner Monologue，用中文还原面试官可能的实时想法。
14. 按 Triage Decision 找主瓶颈，并推荐一个最优先训练命令。
15. 更新 `coaching_state.md`：Score History、Question Bank、Interview Intelligence、Active Coaching Strategy、Session Log。

## Scoring

通用五维：

- Substance：内容、事实、证据和深度
- Structure：结构、顺序和可听懂程度
- Relevance：是否回答了问题，是否贴合岗位
- Credibility：个人贡献和真实性是否可信
- Differentiation：是否有辨识度，而不是模板化

技术或专业面可增加格式维度：

- Technical Accuracy
- Process Visibility
- Scoping Quality
- Tradeoff Quality
- Mode-Switching Fluidity
- Interviewer Adaptation

## Triage Decision

按优先级找主瓶颈：

1. Relevance 低：先练审题和答题匹配。
2. Substance 低：先补真实素材和证据。
3. Structure 低：练回答结构和压缩表达。
4. Credibility 低：补个人贡献、边界、证据，减少过度包装。
5. Differentiation 低：提炼独特经验、取舍和个人方法论。

多个维度都低时，先处理更上游的问题。例如 Substance 不足时，不急着优化 Differentiation。

## Per-Unit Format

```markdown
### [Q#/E#/P#/CS#]
- Scores: Substance __ / Structure __ / Relevance __ / Credibility __ / Differentiation __
- Format-specific scores:
- What worked:
- Biggest gap:
- Root cause pattern:
- Intelligence cross-reference:
- Tight rewrite direction:
- Evidence:
```

正文内容用中文填写，但字段名保持英文。

## Output Schema

```markdown
## Interview Delta

## Interview Format
- Detected format:
- Format source:
- Scoring weight adjustments:
- Format-specific dimensions scored:
- Coaching scope:

## Scorecard
- Substance:
- Structure:
- Relevance:
- Credibility:
- Differentiation:
- Format-specific scores:
- Calibration band used:
- Hire Signal: Strong Hire / Hire / Mixed / No Hire

## Triage Decision
- Primary bottleneck dimension:
- Coaching path chosen:

## What Is Working
1.
2.
3.

## Top 3 Gaps To Close (ordered by triage priority)
1. Gap:
   Why it matters:
   Root cause pattern:
   Drill:
2. Gap:
   Why it matters:
   Root cause pattern:
   Drill:
3. Gap:
   Why it matters:
   Root cause pattern:
   Drill:

## Weakest Answer Rebuild
- Original:
- Why it scored low:
- Stronger version:
- What changed:

## Storybank Changes
- Rework:
- Retire:
- Add:

## Carry Forward
- [One strong behavior from this interview to maintain]

## Priority Move (Next 72 Hours)
- One highest-leverage action:

## Reflection Prompts
- How does this feedback compare to your gut feeling about the interview?
- Of the growth areas above, which feels most within your control?

## Interviewer's Inner Monologue
[中文复盘面试官视角：哪些地方加分、哪些地方产生疑虑、印象在哪里发生变化。引用文字稿时只引用必要短句。]

## Challenge (Level 5 only)
- Assumptions this interview rested on:
- Blind spots:
- Pre-mortem:
- Devil's advocate:

## Intelligence Updates
- Questions added to Question Bank:
- Patterns observed:
- Company learning:

## Confidence
- Score confidence:
- Data quality notes:

## Recommended Next Step
**Recommended next**: `[command]` — [根据上面的优先级判断，写一句中文说明为什么现在做它最划算]. **Alternatives**: `practice`, `stories`, `progress`, `concerns`
```

## Recommended Next Logic

- Relevance 主瓶颈：推荐 `practice pivot`
- Substance 主瓶颈：推荐 `stories improve S###` 或 `stories add`
- Structure 主瓶颈：推荐 `practice ladder`
- Credibility 主瓶颈：推荐 `project` 或 `stories improve`
- Differentiation 主瓶颈：推荐 `stories narrative identity` 或 `pitch`
- 技术准确性主瓶颈：推荐 `basics` 或 `algorithm`
- 面试表现强但需要看趋势：推荐 `progress`

## Rules

- 不要把候选人自评当成评分依据。
- 不要凭零散片段给过高置信度。
- 低相关性回答必须解释问题真正考点。
- 至少重建一个最低分回答。
- 状态写入时保留 `## Score History`、`## Interview Intelligence`、`### Question Bank`、`## Active Coaching Strategy` 等英文协议标题。
