# school - Campus Recruiting Strategy

本文件用于 `school` 命令。适合校招、暑期实习、秋招、春招、日常实习和应届生投递策略。命令名、状态章节和 Output Schema 标题保持英文；规划内容用中文。

## Required Inputs

- Graduation year
- Target role
- Target batch
- Target company tiers
- Current assets
- Weekly available time

如果信息不够，第一问：

“你是哪一届，主要投什么方向？”

## Workflow

1. 明确批次：暑期实习、秋招、春招、日常实习、补录。
2. 明确公司梯队：大厂、中厂、银行科技、国企/央企、研究所、创业公司、外企、混投。
3. 评估当前资产：简历、项目、实习、竞赛、论文/专利、基础、算法、笔试。
4. 划分投递优先级：稳妥盘、主攻盘、冲刺盘。
5. 生成每周节奏：投递、笔试、项目复盘、基础、模拟面。
6. 更新 `## China Campus Technical Prep` 和 `## Active Coaching Strategy`。

## Output Schema

```markdown
## Campus Recruiting Plan
- Graduation year:
- Target role:
- Target batch:
- Company tiers:
- Timeline:

## Current Asset Read
- Strongest assets:
- Biggest risks:
- Missing materials:

## Target Tiers
| Tier | Company type | Strategy | Prep focus |
|---|---|---|---|

## Weekly Plan
### Applications
-

### Written Test Prep
-

### Interview Prep
-

### Resume / Project Work
-

## Tracker
| Company | Role | Batch | Status | Next action |
|---|---|---|---|---|

## Save
Update:
- Campus Application Tracker:
- Written Test Tracker:
- Active Coaching Strategy:
- Session Log:

**Recommended next**: `decode` — 先分析第一个目标 JD，再定制材料。 **Alternatives**: `resume`, `project`, `written`
```

## Rules

- 校招策略要现实：不要只列大厂。
- 时间紧时优先通过笔试和项目可讲性。
- 对普通候选人，稳妥盘和主攻盘比纯冲刺更重要。
- 不要编造公司开放批次；具体时间需要用户提供或联网核实。
