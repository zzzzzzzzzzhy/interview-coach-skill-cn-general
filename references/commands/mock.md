# mock — Full Simulated Interview Workflow

本文件用于 `mock [format]` 命令。目标是进行 4-6 题完整模拟面试，并在结束后给整体弧线反馈。用户可见内容用中文；命令名、状态章节和 Output Schema 标题保持英文。

## Logic

先读取 `coaching_state.md`。如果有目标 JD、项目库、故事库、面试流程或弱项记录，模拟题必须贴合这些信息。

生成模拟题前必须检查 `## Candidate Constraints`。被候选人明确排除或降权的内容，不得作为开场题、主线题或默认深挖题。不要只因为简历里有论文、竞赛、项目名或课程设计，就自动把它当成高频面试重点；题目优先级应由目标岗位、JD、面试轮次、候选人约束和已有面试情报共同决定。

如果候选人曾说“这个岗位不会问论文/不要练论文”，模拟面试应避开论文主线，改问更可能出现的岗位相关问题。只有以下情况可以重新启用该主题：

- 用户明确要求本轮练该主题。
- JD 或面试通知明确提到该主题。
- 真实面试情报显示该公司/岗位问过该主题。

如果用户没有指定 format，先问一个问题：

“这次想模拟哪种面试：综合面、HR 面、技术面、产品/运营/市场专业面、案例面、作品集/展示面，还是按目标岗位混合模拟？”

## Supported Formats

英文 format 可以保留，中文解释如下：

- `behavioral screen`：行为/经历初面
- `deep behavioral`：深度行为面
- `technical`：技术面/专业面
- `technical+behavioral mix`：技术或专业 + 行为混合面
- `case study`：案例分析
- `system design`：系统设计或方案设计
- `panel`：多面试官/多维度面试
- `bar raiser`：高标准综合评估
- `hr`：HR/终面
- `portfolio review`：作品集/项目展示

## Format Adaptation

技术岗：

- 项目深挖
- 基础知识/八股
- 算法或代码口述
- 架构、取舍、问题定位

产品岗：

- 产品判断
- 需求分析
- 指标设计
- 竞品和业务理解
- 推动协作

运营/市场：

- 目标拆解
- 用户/渠道/内容/活动策略
- 数据复盘
- 资源协调
- 增长或传播结果

销售/客户成功：

- 客户需求
- 异议处理
- 推进路径
- 续约/成交/满意度
- 复杂沟通

设计：

- 作品集叙事
- 用户问题
- 设计取舍
- 验证方式
- 与产品/研发协作

职能/金融/咨询/管培：

- 专业基础
- 案例判断
- 结构化表达
- 稳定性和动机
- 风险意识

## Interview Flow

1. 说明模拟格式、题数和评价维度。
2. 一次只问一题。
3. 不在每题后长篇反馈，只做必要追问，保持真实面试节奏。
4. 4-6 题结束后做整体复盘。
5. 输出分数、强项、主要风险、面试官视角和下一步训练。
6. 更新 `coaching_state.md`。

如果用户中途要求反馈，可以暂停并转为 `practice` 模式。

## Scoring

通用模拟：

- Content Quality
- Structure
- Role Relevance
- Credibility
- Differentiation

技术模拟：

- Technical Accuracy
- Project Depth
- Personal Contribution
- Expression Structure
- JD Match

HR 模拟：

- Motivation Authenticity
- Stability
- Communication Maturity
- Pressure / Review Ability
- Expectation Fit

## Output Schema

```markdown
## Mock Interview: [Format]
- Target role:
- Interview type:
- Question count:
- Calibration:

## Opening
[中文说明规则：一次一题，候选人回答后继续]

## Question 1
[问题]

## Question 2
[问题]

## Question 3
[问题]

## Question 4
[问题]

## Question 5 (optional)
[问题]

## Question 6 (optional)
[问题]

## Overall Read
[中文总结这场模拟给面试官留下的整体信号]

## Scorecard
- Content Quality / Technical Accuracy / Motivation Authenticity:
- Structure / Project Depth / Stability:
- Role Relevance / Personal Contribution / Communication Maturity:
- Credibility / Expression Structure / Pressure Ability:
- Differentiation / JD Match / Expectation Fit:

## What Is Working
-

## Gaps To Close
-

## Interviewer Inner Monologue
[用中文模拟面试官可能在想什么：认可点、疑虑点、想继续追问的点]

## Best Answer To Rebuild First
- Question:
- Why this one:
- Rewrite direction:

## Training Plan
1.
2.
3.

## Save
Update:
- Score History:
- Interview Intelligence:
- Drill Progression:
- Candidate Constraints, if candidate corrected relevance:
- Active Coaching Strategy:
- Coaching Notes:
- Session Log:

**Recommended next**: `practice` — 把本轮模拟里最弱的模式单独拎出来专项练。 **Alternatives**: `stories`, `project`, `progress`
```

## Rules

- 模拟期间保持真实节奏，不要每题都立刻教学，除非用户要求。
- 问题要贴合候选人目标岗位和材料。
- 问题还必须贴合 `## Candidate Constraints`；已被候选人降权的内容不要作为默认重点。
- 不编造候选人经历；示范答案缺事实处用占位提示。
- 如果格式是系统设计、案例、专业面，要说明教练能训练表达、结构和取舍，但不能替代真实行业专家评审。
- 结束后必须给一个最优先重练的问题。
