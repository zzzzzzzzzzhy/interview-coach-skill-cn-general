# kickoff — Setup Workflow

本文件用于 `kickoff` 命令。目标是初始化候选人画像，并创建或更新 `coaching_state.md`。面向用户的提问和反馈使用中文；状态文件的章节标题和字段名保持英文 schema。

## Logic

`kickoff` 不是一次性问卷。必须一次只问一个问题，根据回答继续追问。不要一口气列 8 个问题。

### Step 1: Coaching Configuration

依次收集：

1. 目标岗位/方向。
2. 求职阶段：校招 / 实习 / 社招 / 转岗 / 复试 / 海外。
3. 时间线：近期是否有笔试、面试、投递截止。
4. 当前最大担心点。
5. 反馈直接程度：1-5，默认 5。
6. 面试历史：是否已经面过，结果如何，卡在哪一轮。
7. 训练模式：`Quick Prep` 或 `Full System`。

如果候选人不知道怎么选，按时间线判断：

- 48 小时内有面试：`Quick Prep`
- 1-2 周内有面试或笔试：`Quick Prep`
- 3 周以上准备周期：`Full System`
- 没有明确面试但想系统提升：`Full System`

### Step 1.5: Domain Context

根据岗位类型补充不同信息：

技术岗：

- 主语言和技术栈
- 项目/实习/科研/竞赛
- 基础知识薄弱点
- 算法/笔试水平
- 是否需要校招批次规划

产品岗：

- 产品经历、项目、实习、作品
- 是否做过需求分析、竞品分析、数据复盘
- 目标行业和产品类型

运营/市场/销售：

- 活动、内容、用户、社群、增长、客户或成交经历
- 可量化结果
- 目标行业和业务类型

设计岗：

- 作品集状态
- 设计流程、用户研究、方案取舍和验证证据

职能/金融/咨询/管培：

- 专业背景
- 实习或项目经历
- 案例分析、结构化表达、稳定性和职业动机

### Step 2: Candidate Context

强烈建议候选人提供：

- 简历文本或简历摘要
- 目标 JD
- 1-3 个代表性经历、项目或作品
- 已经发生的面试反馈

如果用户没有材料，不要卡住。先创建基础状态，并推荐下一步补材料。

### Step 2.5: Resume / Profile Analysis

如果候选人提供了简历或经历摘要，做初步画像：

1. **Positioning strengths**：30 秒内最容易被看到的优势信号。
2. **Likely interviewer concerns**：面试官可能担心的点，如经历不连续、目标不清、项目过浅、岗位跨度大、缺关键技能。
3. **Career narrative gaps**：职业叙事断点，如转岗、行业切换、学历/经验和岗位不匹配。
4. **Story seeds**：值得深挖成故事或项目的素材。

不要编造简历里没有的指标。没有证据就写“待补充”。

### Step 2.55: Career Transition Detection

如果目标岗位和过往经历存在明显切换，记录转型类型：

- function change
- domain shift
- IC↔management
- industry pivot
- career restart
- none

当转型存在时，后续优先训练桥接叙事：为什么转、旧经验如何迁移、新岗位为什么可信。

### Step 2.6: Target Reality Check

只在明显不匹配时触发，不要制造焦虑。

触发条件：

- 岗位级别跨度过大
- 完全没有目标行业/职能的桥接证据
- JD 硬性要求的能力在简历中完全看不到
- 转型理由明显空缺

表达方式：

“从你目前材料看，目标 [role] 有一个明确风险：[gap]。这不等于不能投，但需要专门准备证据和说法。我们可以继续冲这个方向，也可以同时准备更稳的备选目标。”

### Step 3: Initialize Coaching State

创建或更新 `coaching_state.md`，必须使用 `references/coaching-state-schema.md` 的英文标题。

至少写入：

- `## Profile`
- `## Resume Analysis`
- `## Project Bank`
- `## Storybank`
- `## Score History`
- `## Outcome Log`
- `## Interview Intelligence`
- `## Drill Progression`
- `## Active Coaching Strategy`
- `## Calibration State`
- `## Session Log`
- `## Coaching Notes`

若是技术/校招场景，也初始化 `## China Campus Technical Prep`。

### Mid-Search Profile Update

如果候选人已经有 `coaching_state.md`，但目标变了，不要重建全部状态。先问：

“这次主要变化是什么：目标岗位、行业、城市、时间线，还是你手上的面试机会变了？”

然后更新 Profile，并说明哪些内容保留，哪些命令需要重跑。

### Time-Aware Coaching

按时间线调节建议：

- 48 小时内：只做高收益救急，`prep`、`hype`、关键问题练习。
- 1-2 周：针对 JD 和最大短板做集中训练。
- 3 周以上：建立完整系统，补故事库、项目库、模拟和复盘。

## Output Schema

```markdown
## Kickoff Summary（启动总结）
- 训练模式: [快速准备（Quick Prep）/ 系统训练（Full System）]
- 目标岗位:
- 经验阶段:
- 准备时间线:
- 面试历史: [第一次面试 / 正在面但推进不顺 / 有经验但状态生疏]
- 目标匹配判断: [现实可投 / 有挑战但可准备 — 见下方说明 / 存在明显风险 — 见下方说明]
- 反馈直接程度:
- 时间策略: [救急冲刺（triage）/ 集中准备（focused）/ 系统训练（full）]

## Profile Snapshot（画像快照）
- 最容易被看见的优势:
- 面试官可能担心:
- 职业叙事缺口:
- 值得深挖的素材:

## Interview Readiness Assessment（面试准备度判断）
根据面试历史和候选人画像判断：
- 当前准备度:
- 最大风险:
- 最大优势:

## Target Reality Check（目标现实校准，仅在存在明显风险时输出）
- 目标:
- 已识别差距:
- 差距类型:
- 建议:

## First Plan
[根据时间线、岗位和材料状态，用中文给出第一阶段计划]

### Immediate (this session or next)
1. [specific action with command]

### This week
2. [specific action with command]
3. [specific action with command]

### Before first interview (or ongoing)
4. [specific action with command]

**Recommended next**: `[command]` — [根据时间线和面试历史写一句中文理由]. **Alternatives**: `decode`, `resume`, `stories`, `project`, `practice`, `help`
```

## Rules

- 一次只问一个问题。
- 不要在没有简历/JD/经历证据时做强结论。
- 写 `coaching_state.md` 时，标题和字段名保持英文 schema。
- 面向用户的摘要字段用中文标签；写入 `coaching_state.md` 时才使用英文 schema 字段。
- 中文候选人默认中文输出。
- 完成后自然提醒：不确定命令时可以输入 `help`。
