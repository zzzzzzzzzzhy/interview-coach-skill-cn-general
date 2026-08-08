# prep — Prep Brief Workflow

本文件用于 `prep [company]` 命令。目标是在候选人已有具体公司/岗位/面试前，生成一份可执行的面试准备简报。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；简报内容、解释、问题和建议使用中文。

## Required Inputs

- Company
- Role title/seniority
- Job description

## Optional Inputs

- Interviewer profile links
- Stage format
- Company values / recruiter notes
- Interview date
- Existing resume / storybank / project bank

如果缺 JD，第一问：

“把这个岗位的 JD 粘过来。没有 JD 的话，我可以先做轻量 `research`，但预测问题和匹配度会低置信。”

## Logic

1. 读取 `coaching_state.md`。
2. 确认 company、role、stage、format、timeline。
3. 如果有 `decode` 结果，复用 `## JD Analysis: [Company] — [Role]`；如果 JD 已变，重新解析。
4. 如果需要最新公司信息，先做或刷新 `research`，并标注来源。
5. 识别面试格式：behavioral screen、deep behavioral、technical、case study、presentation、panel、hr、portfolio review 等。
6. 做 Role-Fit Assessment：Requirement Coverage、Seniority Alignment、Domain Relevance、Competency Overlap、Trajectory Coherence。
7. 检查 Storybank / Project Bank 健康度。
8. 生成预测问题，并映射故事/项目。如果没有故事库，标出需要准备的能力证据。
9. 生成 concerns 和 counters。
10. 生成 questions to ask。
11. 输出 day-of cheat sheet。
12. 更新 `Interview Loops (active)` 和 `Session Log`。

## Interview Format Taxonomy

| Format | What changes | Scoring weight shift |
|---|---|---|
| behavioral screen | 题多、时间短，重点是命中问题和表达效率 | Structure + Relevance |
| deep behavioral | 追问深，需要故事厚度和可信度 | Substance + Credibility |
| technical / specialist | 专业准确性、项目/案例深度、思考过程 | Technical Accuracy + Project Depth |
| technical+behavioral mix | 需要在专业和经历之间切换 | Substance + Structure |
| system design / case study | 更看过程可见性、范围界定、取舍 | Process Visibility + Structure |
| presentation / portfolio review | 准备内容 + Q&A 抗压 | Structure + Differentiation |
| panel | 多人、多视角、能量管理 | Relevance + Adaptation |
| hr / final | 动机、稳定性、成熟度、期望匹配 | Credibility + Fit |

如果 format 不明确，不要假装知道。先问：

“这轮是 HR、业务面、技术/专业面、案例面、作品集展示，还是综合面？大概多长时间？”

## Role-Fit Assessment

输出 verdict：

- Strong Fit
- Investable Stretch
- Long-Shot Stretch
- Weak Fit

并区分：

- Frameable gaps：可以通过叙事和证据解释的差距。
- Structural gaps：短期很难补的硬差距。

## Storybank / Project Bank Health

检查：

- 数量是否够。
- 是否有 4+ 强故事/强项目。
- 是否覆盖 JD top competencies。
- 是否有过度使用的故事。
- 是否有候选人写了但讲不清的内容。

没有故事库时，不要编造映射。写：

“当前没有 Storybank / Project Bank，我只能按能力维度提示要准备什么。建议后续跑 `stories` 或 `project`。”

## Output Schema

```markdown
## Prep Brief: [Company] — [Role]
- Interview date:
- Stage:
- Format:
- Confidence:

## Interview Format
- Detected format:
- What this means:
- Scoring emphasis:
- Coaching scope:

## Company / Role Read
- What they likely care about:
- Recent or verified company signals:
- Source confidence:

## Role-Fit Assessment
- Verdict: [Strong Fit / Investable Stretch / Long-Shot Stretch / Weak Fit]
- Requirement Coverage:
- Seniority Alignment:
- Domain Relevance:
- Competency Overlap:
- Trajectory Coherence:
- Frameable gaps:
- Structural gaps:

## Storybank / Project Bank Health
- Available strong materials:
- Missing coverage:
- Overuse / freshness risks:
- Must-patch before interview:

## Predicted Questions
| Question | What it tests | Best story/project | Risk | Prep note |
|---|---|---|---|---|

## Likely Concerns + Counters
| Concern | Severity | Counter | Evidence to use |
|---|---|---|---|

## Questions To Ask Them
1.
2.
3.

## Day-Of Cheat Sheet
- 3 strengths to land:
- 3 risks to avoid:
- 3 questions to ask:
- One sentence positioning:

## Save
Update:
- Interview Loops (active):
- Active Coaching Strategy:
- Session Log:

**Recommended next**: `practice` — 面试前先练最高风险预测题。 **Alternatives**: `concerns`, `questions`, `hype`, `present`
```

## Rules

- 不要编造公司文化、面试流程或面试官信息。
- 公司和岗位信息可能变化，必要时联网核实。
- 没有 JD 时，明确降低 Confidence。
- `prep` 给策略，`practice` 负责练回答，`present` 负责展示型内容结构。
- 对系统设计、案例和专业面，说明教练主要训练表达结构和思考过程，不替代专业评审。
