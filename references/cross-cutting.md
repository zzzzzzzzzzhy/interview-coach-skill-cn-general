# Cross-Cutting Modules

本文件定义所有命令共享的通用模块。模块名保留英文；说明和话术使用中文。

## State Context Gate

执行任何会生成建议、简历内容、练习题、模拟题或追问的命令前，先读取 `coaching_state.md`。读取后按以下顺序判断：

1. `## Candidate Constraints`
2. `## Profile`
3. `## JD Analysis` / `## Interview Loops (active)`
4. `## Resume Analysis` / `## Resume Optimization`
5. `## Storybank` / `## Project Bank`
6. `## Score History` / `## Coaching Notes`

`## Candidate Constraints` 的优先级高于简历中显眼但已被候选人降权的内容。除非 JD、面试通知或候选人新回答明确推翻旧约束，不要把被排除/降权的信息作为默认重点。

典型写法：

| ID | Constraint | Applies To | Priority | Source | Last Confirmed | Handling Rule |
|----|------------|------------|----------|--------|----------------|---------------|
| C001 | 论文经历不作为发电集团岗位面试主线 | resume, mock, practice | high | candidate correction | 2026-08-08 | 简历中可保留为教育/科研背景，但模拟面试不要作为开场或核心追问；仅当 JD 明确要求科研能力时再轻量提及。 |

如果候选人纠正教练判断，例如“这个方向不会问论文”，必须：

1. 承认并更新判断。
2. 写入 `## Candidate Constraints`。
3. 调整当前输出，不要继续沿用被纠正的方向。
4. 后续命令生成问题前先检查该约束。

## Differentiation Module

Differentiation 是通用五维评分之一，不是附加项。

触发条件：

- Differentiation < 3。
- 回答换成另一个同级候选人也成立。
- 只讲框架、术语或套话，没有个人洞察。
- 故事缺少 earned secret。

处理：

1. 问：这段经历让你知道了什么别人不知道的东西？
2. 找：候选人做过的取舍、反直觉判断、失败后的方法变化。
3. 写入 Storybank / Project Bank。
4. 用 `practice` 或 `mock` 压力测试。

## Gap-Handling Module

候选人不可能对每个问题都有完美故事。目标不是假装有，而是诚实桥接。

可用模式：

- Adjacent Bridge：没有完全一样的经历，但有相邻经历。
- Hypothetical with Self-Awareness：没做过，说明会如何上手和验证。
- Reframe to Strength：承认不是强项，转向能满足底层需求的优势。
- Growth Narrative：这是成长项，说明已经如何补。

禁忌：

- 编造经历。
- 只说“没有”然后停住。
- 过度解释为什么没有。
- 用“我们做过”遮掩自己没做过。

## Signal-Reading Module

面试是双向互动，候选人要读信号。

正向信号：

- 继续追问细节。
- 对方开始分享自己的经验。
- 主动介绍团队或岗位。

需要调整的信号：

- 中途打断并换题。
- 问“所以结果是什么？”
- 频繁看时间。
- 重新解释问题。

中性信号：

- 沉默。
- 照稿问。
- “后续会联系”。

规则：信号只做方向判断，不当成结果预测。

## Psychological Readiness Module

面试失败常常不是只因为不会答，也可能是状态问题。

面前：

- 读 3x3。
- 练一个 60 秒强回答。
- 做身体 reset。
- 把面试重构成双向匹配，不是审判。

面中：

- 卡住时说：“我整理一下思路。”
- 答坏一题后，不要把情绪带到下一题。
- 没有故事时用 Gap-Handling。

面后：

- 先 `debrief` 保存事实。
- 有文字稿再 `analyze`。
- 不要用刚出门的情绪直接判断成败。

## Cultural and Linguistic Awareness Module

文化和语言差异不是能力缺陷。辅导目标是适配面试场景，而不是抹掉候选人风格。

常见适配：

- 含蓄表达 -> 面试中需要更早给结论。
- 谦虚习惯 -> 准确描述个人贡献不是吹牛。
- 过度正式 -> 调整到自然、清楚、职业。
- 中文面试 -> 用更直接的“结论先行 -> 证据 -> 反思”。

## Role-Fit Assessment Module

用于 `research`、`decode`、`prep`、`progress`。

五个维度：

- Requirement Coverage：硬要求覆盖。
- Seniority Alignment：级别匹配。
- Domain Relevance：行业/场景相关性。
- Competency Overlap：能力重合度。
- Trajectory Coherence：职业路径是否说得通。

Fit verdict：

- Strong Fit
- Investable Stretch
- Long-Shot Stretch
- Weak Fit

差距分两类：

- Frameable gaps：可以用叙事和证据解释。
- Structural gaps：短期难补的硬差距。

## Score Mapping Module

用户可见评分可以中文化，但写入 `## Score History` 时必须映射到固定列：

| Score History column | 通用中文展示 | 技术岗中文展示 | 英文别名 |
|---|---|---|---|
| `Sub` | 内容质量 | 技术准确性 | Substance / Content Quality / Technical Accuracy |
| `Str` | 表达结构 | 项目深度 | Structure / Project Depth |
| `Rel` | 岗位相关性 | 个人贡献 | Relevance / Role Relevance / Personal Contribution |
| `Cred` | 可信度 | 表达结构 | Credibility / Expression Structure |
| `Diff` | 差异化 | JD 匹配 | Differentiation / JD Match |

规则：

- 面向用户输出时优先用中文标签，如“内容质量”“技术准确性”。
- 写入 `Score History` 时只写 `Sub`、`Str`、`Rel`、`Cred`、`Diff` 五列。
- 如果一次练习使用技术岗维度，仍按上表映射，不新增表头。
- 如果某维度不适用，留空或写 `n/a`，不要改表结构。

## Recommendation Module

每个完整工作流结尾必须给：

`**Recommended next**: [command] — [reason]. **Alternatives**: [command], [command].`

推荐必须来自当前状态，而不是固定菜单。

## Rules

- 所有模块都要证据优先。
- 不编造候选人经历。
- 不把公司信息说成确定事实，除非有来源。
- 中文输出时保留英文协议名。
