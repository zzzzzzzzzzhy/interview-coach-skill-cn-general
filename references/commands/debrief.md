# debrief — Post-Interview Rapid Capture Workflow

本文件用于 `debrief` 命令。目标是在真实面试后尽快捕捉事实、问题、面试官信号和候选人主观感受。它是 `analyze` 的前置输入；如果没有文字稿，它也可以作为低置信度复盘的数据来源。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；提问和反馈用中文。

## When to Use

- 刚结束真实面试，最好 1-2 小时内。
- 没有文字稿，但还记得问题和感受。
- 有文字稿，但想先记录当下主观感受。
- 面试后情绪很强，需要先稳定再做技术分析。

## Sequence

一次只问一个问题。不要一开始就让候选人填完整表。

1. Emotional check：先问  
   “先别分析，给我一个词：你现在感觉怎么样？”
2. Rapid question capture：  
   “他们问了哪些问题？不用精确复述，先尽量列出来。”
3. Per-question self-assessment：对每个问题记录 strong / okay / rough。
4. Signal reading：记录面试官追问、点头、质疑、打断、转移话题、介绍岗位、时间控制等信号。
5. Surprises：记录没预料到的问题、形式、面试官风格或环境。
6. Story usage：记录用了哪些故事/项目，对应 `S###` 或 `P###`。
7. Immediate tactical notes：候选人自己觉得下次要改什么。
8. Positioning performance：自我介绍或开场是否有效。
9. Feedback capture：是否有 HR、面试官或招聘方反馈。
10. Transcript availability：是否有录音、转写或手动整理稿。

## Signal Interpretation Guide

| Signal | Likely Meaning | Confidence |
|---|---|---|
| 对某个点连续追问 | 可能是真感兴趣，也可能在测深度；无论如何都很重要 | HIGH |
| 很快切到下一题 | 可能已满意，也可能没听到想要的信息，要结合语气和后续判断 | MEDIUM |
| “这个挺有意思”并继续追问 | 通常是正向信号 | HIGH |
| 频繁看时间 | 可能是流程赶时间，不一定是不感兴趣；如果伴随打断，说明回答可能偏长 | MEDIUM |
| 明确 push back | 多数是在测判断和抗压，不一定是负面 | HIGH |
| 开始主动介绍岗位/团队 | 偏正向，说明想提高候选人兴趣 | HIGH |
| 只问封闭式短问题 | 可能已经形成判断，偏中性到负面 | MEDIUM |
| “后续会联系” | 标准结束语，不要过度解读 | LOW |

必须加 caveat：这些是方向性信号，不是结果预测。

## With vs. Without Transcript

有 transcript：

- 先保存 debrief。
- 告诉候选人后续跑 `analyze`，我会比较“当时感觉”和“文字稿实际表现”。

无 transcript：

- 使用轻量分析。
- 明确置信度较低。
- 更重视问题回忆、面试官信号和候选人自己的复盘。

## Emotional Triage

- 感觉不错且有 transcript：正常收集信息，建议 `analyze` 或 `thankyou`。
- 感觉不错但没有 transcript：正常收集信息，建议先 `progress` 更新训练判断，或用 `practice` 复练印象最深的问题。
- 感觉很糟：先接住情绪，不急着打分。重点是保存信息。
- 感觉不确定：告诉候选人不确定很正常，先把事实抓住。

## Output Schema

```markdown
## Interview Debrief: [Company] - [Round]
- Date:
- Interviewer(s):
- Format:
- Emotional read:

## Questions Recalled
1. [Question as remembered]
   - Self-assessment: [strong / okay / rough]
   - Story used: [S### / P### / none]
   - Notes:

## Interviewer Signals Observed
- Positive signals:
- Negative signals:
- Neutral/ambiguous:

## Surprises
-

## Stories Used
| Story | Question | How It Landed (candidate read) |
|-------|----------|-------------------------------|

## Candidate's Own Takeaways
- What to do differently:
- What worked:

## Feedback Received
- Date:
- Company:
- Source:
- Feedback:
- Linked dimension:

## Intelligence Notes
- Questions matched from past interviews:
- Company pattern observations:

## Transcript Status
- [ ] Transcript available -> run `analyze` when ready
- [ ] No transcript -> directional analysis above is what we have

**Recommended next**:
- 有 transcript：`analyze` — 趁记忆还新，把文字稿逐题分析并和现场感受对照。 **Alternatives**: `thankyou`, `progress`
- 无 transcript：`progress` — 先把回忆问题、面试官信号和候选人自评沉淀到后续训练计划。 **Alternatives**: `practice`, `thankyou`, `hype`
```

## Coaching State Integration

更新 `coaching_state.md`：

- `## Outcome Log`：新增 pending 记录。
- `## Interview Loops (active)`：更新轮次、形式、信号、下一轮。
- `## Interview Intelligence` / `### Question Bank`：加入回忆问题，Score 写 `recall-only`。
- `### Recruiter/Interviewer Feedback`：保存外部反馈。
- `## Storybank`：更新故事使用次数和 Last Used。
- `## Session Log`：记录本次 debrief。

## Rules

- `debrief` 先保存事实，不急着做重分析。
- 不要把面试官信号当成确定结果。
- 用户情绪很差时，先捕捉信息，再建议休息或后续分析。
- 有 transcript 时，`debrief` 不替代 `analyze`。
