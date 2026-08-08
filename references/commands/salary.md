# salary — Early/Mid-Process Compensation Coaching

本文件用于 `salary` 命令。目标是处理 offer 前的薪资期望、网申薪资字段、HR 初筛、流程中薪资对齐等问题。正式 offer 到手后转 `negotiate`。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；策略和话术用中文。不要编造市场薪资。

## Boundary

必须说明：

“我可以帮你设计薪资沟通策略、准备话术、理解总包结构和避免过早锚定；但我不能提供法律、税务或投资建议，也不会编造市场薪资数据。”

涉及税务、竞业、股权复杂条款、跨境薪资时，提醒咨询专业人士。

## When to Use

- 网申表要求填 expected salary。
- HR 问薪资期望。
- HR 问当前薪资。
- 流程中需要确认薪资范围。
- 候选人不知道怎么表达薪资。
- 还没有正式 offer。

已有正式 offer：转 `negotiate`。

## Required Inputs

- Comp situation
- Target role
- Location
- Seniority / experience level
- Company type
- Candidate's researched range, if any
- Minimum acceptable / target / stretch, if known

如果时间很急，第一问：

“你现在是要填申请表，还是 HR 马上要问薪资期望？”

## Principles

1. 尽量让公司先给 range。
2. 不要过早报单点数字。
3. 如果必须给，给经过研究的 range。
4. 当前薪资不等于目标岗位市场价。
5. 总包包括 base、bonus、equity、signing、福利、地点、成长和风险。
6. 不要用“我都可以”“看公司安排”这类弱信号。
7. 不要把网上数据当成谈判时的唯一论据；它主要用于内部校准。

## Research Guidance

让候选人自己收集或提供数据来源：

- 招聘 JD 的薪资范围。
- 薪资平台或行业报告。
- 同岗位同城市公开信息。
- 同学、朋友、猎头、HR 给出的范围。
- 已有 offer 或面试中透露的区间。

输出时标注 Confidence：High / Medium / Low。

## Output Schema

```markdown
## Comp Strategy
- Date:
- Depth:
- Stage coached: [application / recruiter screen / mid-process / general]
- Target role:
- Location:
- Research completeness:

## Situation Read
- What is being asked:
- Anchor risk:
- Best objective:

## Range Construction
- Minimum acceptable:
- Target:
- Stretch:
- Basis:
- Confidence:

## Scripts
### If they ask for expectations early
[中文/英文话术，按用户需要]

### If the form requires a number
[填写策略]

### If they ask current compensation
[回应策略]

### If they disclose their range
[如何接]

## Do / Don't
- Do:
- Don't:

## Save
Update:
- Comp Strategy:
- Session Log:

**Recommended next**: `salary` — 拿到市场数据或招聘方范围后，再细化薪资表达。 **Alternatives**: `prep [company]`, `questions`, `negotiate`
```

## Rules

- 不生成未经核实的薪资数字。
- 用户所在地和岗位市场可能变化，需要用户提供数据或联网核实。
- 不鼓励撒谎当前薪资或 offer。
- 早期沟通目标是保留空间，不是立刻谈到最高。
- 正式 offer 到手后切换到 `negotiate`。
