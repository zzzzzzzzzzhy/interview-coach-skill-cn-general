# basics - Technical Fundamentals / Bagua Practice

本文件用于 `basics` 命令。适合技术岗基础知识、八股、项目关联追问训练。命令名、状态章节和 Output Schema 标题保持英文；讲解和反馈用中文。

## Required Inputs

- Target role
- Main language
- Topic or weak area
- Timeline

如果信息不够，第一问：

“你现在准备哪个技术方向：后端、前端、C++、测试、安全、数据、算法，还是其他？”

## Workflow

1. 判断目标岗位、时间线和当前薄弱点。
2. 建立优先级：优先练和项目/JD 强相关的基础。
3. 一次只问一个问题。
4. 候选人回答后先纠错，再打磨表达。
5. 用技术岗评分维度打分。
6. 生成一版可直接面试使用的中文回答。
7. 把弱点和修正版保存到 `coaching_state.md` 的 `## China Campus Technical Prep`。

## Answer Standard

强回答通常包含：

1. 一句话定义。
2. 核心机制。
3. 工程价值。
4. 项目/业务场景。
5. 常见坑或取舍。

不要停在“Redis 很快因为在内存里”这种层级。要继续追到事件模型、数据结构、持久化、淘汰策略、网络模型和项目使用边界。

## Output Schema

```markdown
## Basics Drill: [Topic]

## Priority Map
| Topic | Priority | Why it matters | Linked project/JD |
|---|---|---|---|

## Question 1
[只问一个问题，等待候选人回答]

## After Candidate Answers
### Scorecard
- Technical Accuracy:
- Project Depth:
- Personal Contribution:
- Expression Structure:
- JD Match:

### What Is Correct
-

### Corrections
-

### Interview-Ready Version
[中文回答：结论 -> 机制 -> 项目/场景 -> 坑点/取舍]

### Follow-Up Chain
1.
2.
3.

### Save
- Weak topic:
- Fixed answer:
- Linked project:

**Recommended next**: `basics` — 继续沿着追问链练到这个知识点稳定为止。 **Alternatives**: `project`, `algorithm`, `mock technical`
```

## Rules

- 准确性优先于流畅度。
- 错概念必须直接纠正。
- 尽量关联候选人的项目。
- 72 小时内有面试时，只练高频和项目相关问题。
