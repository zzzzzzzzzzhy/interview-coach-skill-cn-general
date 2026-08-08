# feedback — Capture Feedback, Outcomes, and Corrections

本文件用于 `feedback` 命令。它负责捕捉新信息，不负责完整分析。真正的分析发生在 `analyze`、`progress`、`prep` 中。

中文化规则：命令名、状态章节名、表头和 Output Schema 标题保持英文；确认、解释和建议使用中文。

## When to Use

- HR、面试官或招聘方给了反馈。
- 候选人知道了面试结果：advanced、rejected、offer、withdrawn、pending。
- 候选人想纠正之前的教练判断。
- 候选人又想起面试中的问题、细节或信号。
- 候选人想反馈教练方式本身。

## Input Type Detection

先把输入分成五类。如果不确定，只问一个问题：

“这是招聘方反馈、面试结果更新，还是你想补充/纠正一条信息？”

### Type A: Recruiter/Interviewer Feedback

触发：候选人转述 HR、面试官、leader 或招聘方反馈。

处理：

1. 尽量按原话记录。可以问：  
   “他们原话大概怎么说？哪怕不完整也比概括更有价值。”
2. 记录来源：recruiter / interviewer / hiring manager / other。
3. 映射到维度，但不要过度确定。  
   例：“表达有点散” -> Structure；“项目深度不足” -> Substance / Project Depth；“经验不匹配”可能是外部匹配问题，不一定是表现问题。
4. 如果外部反馈和教练评分冲突，记录为 calibration signal，不要直接忽略。

状态更新：

- `## Interview Intelligence` -> `### Recruiter/Interviewer Feedback`
- `## Calibration State` -> `### Scoring Drift Log`，如果反馈和评分明显冲突
- `## Interview Loops (active)`，如果关联具体公司/轮次
- `## Session Log`

输出：简短确认记录了什么、映射到什么维度、是否需要后续行动。

### Type B: Outcome Report

触发：候选人报告推进、拒绝、offer、撤回、等待中。

处理：

1. 确认 company、role、round。
2. 记录 result：advanced / rejected / offer / withdrawn / pending。
3. 如果 rejected，问是否有原因。
4. 如果 advanced，问下一轮形式、时间、面试官信息。
5. 如果 offer，建议后续转 `negotiate`。

状态更新：

- `## Outcome Log`
- `## Interview Loops (active)`
- `## Interview Intelligence` / `### Question Bank` 的 Outcome 字段
- `## Calibration State`，当真实结果达到 3 个以上时，标记可以做校准

输出：确认更新，并推荐 `prep`、`progress`、`negotiate` 或 `debrief`。

### Type C: Coaching Correction

触发：候选人认为之前的评分、判断或建议不准。

处理：

1. 先理解候选人补充了什么新信息。
2. 如果新信息改变判断，明确承认并修正。
3. 如果证据仍不支持候选人的看法，保留原判断，但解释依据。
4. 如果不确定，记录双方视角，降低置信度。

状态更新：

- 修改相关 Score History、Storybank、Project Bank 或 Coaching Notes。
- 如果多次出现自评偏差，更新 `Active Coaching Strategy` 的 self-assessment tendency。

输出：不防御，不硬拗，说明“改了什么/为什么没改/还缺什么证据”。

### Type D: Post-Session Memory

触发：候选人补充之前忘记的问题、故事细节、面试官信号或公司信息。

处理：

- 忘记的问题 -> `Question Bank`
- 故事细节 -> `Storybank`，必要时建议 `stories improve`
- 项目细节 -> `Project Bank`，必要时建议 `project`
- 面试官信号 -> `Interview Loops`
- 公司观察 -> `Company Patterns`

输出：确认保存位置。如果它改变了之前判断，明确说出来。

### Type E: Coaching Meta-Feedback

触发：候选人反馈教练方式，如太直接、不够直接、太散、太结构化、重点不对。

处理：

1. 接住反馈，不防御。
2. 判断是 delivery、content 还是 process 问题。
3. 给出后续调整。

状态更新：

- `## Meta-Check Log`
- `## Coaching Notes`
- 必要时更新 `## Profile` 的 Feedback directness
- 必要时更新 `## Active Coaching Strategy`

## Output Schema

`feedback` 可以轻量输出，不强制长报告。默认格式：

```markdown
## Feedback Captured
- Type:
- Source:
- Company / Role / Round:
- What was captured:
- Linked dimension:
- Confidence:

## State Updates
- Outcome Log:
- Interview Intelligence:
- Calibration State:
- Coaching Notes:

## What This Changes
[中文说明这条反馈是否改变当前判断；如果不改变，也说明原因]

## Recommended Next Step
**Recommended next**: `[command]` — [根据反馈类型写一句中文理由]. **Alternatives**: `debrief`, `analyze`, `progress`, `prep [company]`
```

## Rules

- Capture first, analyze later。
- 不要把一句模糊反馈过度解释成确定结论。
- 外部反馈比教练猜测更重要，但也要看来源和具体程度。
- 如果用户其实在做完整面后复盘，建议转 `debrief`。
- 如果用户提供了完整文字稿，建议转 `analyze`。
