# written - Written Test / Online Assessment Planning

本文件用于 `written` 命令。适合笔试、在线测评、行测、SQL、选择题、性格测评和校园招聘筛选。命令名、状态章节和 Output Schema 标题保持英文；计划和反馈用中文。

## Required Inputs

- Company / role
- Test date
- Sections
- Weakest section
- Available daily prep time

如果信息不够，第一问：

“最近这场笔试/测评是什么岗位，大概什么时候考？”

## Workflow

1. 明确考试时间和板块。
2. 判断最高风险板块。
3. 生成 3-7 天或 2 周计划。
4. 建立错题记录方式。
5. 对技术岗，优先算法题型 + 高频基础选择题。
6. 对非技术岗，优先行测、性格测评、岗位案例题、专业基础。
7. 更新 `## China Campus Technical Prep` 或 `## Active Coaching Strategy`。

## Output Schema

```markdown
## Written Test Plan
- Company:
- Role:
- Date:
- Sections:
- Highest-risk section:

## Risk Triage
| Section | Risk | Why | Prep action |
|---|---|---|---|

## Prep Plan
### Today
1.
2.

### This Week
1.
2.
3.

## Mistake Log Template
| Date | Question/Topic | Mistake Type | Fix | Next Similar Problem |
|---|---|---|---|---|

## Save
Update:
- Written Test Tracker:
- Algorithm Practice, if applicable:
- Weak Topics:
- Session Log:

**Recommended next**: `algorithm` — 先练最高风险的编程题型。 **Alternatives**: `basics`, `school`, `practice`
```

## Rules

- 时间很近时只做高频和提分最快的部分。
- 不要给过长计划，要能当天执行。
- 性格测评不鼓励伪装极端人设，强调一致、真实、岗位匹配。
