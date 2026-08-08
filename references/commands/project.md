# project - Project / Case Deep Dive

本文件用于 `project` 命令。它不只服务技术项目，也可以用于产品项目、运营案例、市场活动、销售项目、设计作品、咨询案例、职能流程优化等代表性经历。

命令名和 Output Schema 标题保持英文；面向候选人的解释和示例用中文。

## Required Inputs

最低需要：

- Project name
- Target role
- Context / background
- What the candidate personally did
- Current resume bullet or rough project description

不同方向可补充：

- 技术岗：tech stack、architecture、data flow、hard problems、metrics、follow-up fundamentals
- 产品岗：user/problem、requirement analysis、tradeoffs、metrics、stakeholders
- 运营/市场：goal、audience、channel、execution、conversion/retention/traffic metrics
- 销售/客户成功：client type、need、objection、deal/progress result、renewal/retention evidence
- 设计岗：brief、user insight、design choices、validation、portfolio narrative
- 职能/咨询：problem, analysis, process, stakeholders, risk, business impact

如果信息不够，一次只问一个问题。默认第一问：

“先把这个项目/案例/作品在简历上的描述粘过来。”

## Deep-Dive Axes

从以下角度深挖：

1. Background：解决什么真实问题，为什么值得做。
2. Goal：目标是什么，成功标准是什么。
3. Approach：你采用了什么方案，为什么。
4. Personal contribution：你个人具体做了什么，不要只说“我们”。
5. Hard part：最难的地方是什么，难在哪里。
6. Tradeoffs：有哪些备选方案，为什么没选。
7. Debugging / iteration：中间遇到什么问题，如何定位和调整。
8. Metrics / proof：结果、指标、反馈、上线、奖项、复用、业务影响。
9. Role relevance：这段经历如何证明目标岗位需要的能力。
10. Follow-up risks：哪些地方容易被追问但候选人还讲不清。

## Scorecard

通用项目/案例用：

- Content Quality
- Structure
- Role Relevance
- Credibility
- Differentiation

技术岗可切换为：

- Technical Accuracy
- Project Depth
- Personal Contribution
- Expression Structure
- JD Match

Confidence: High / Medium / Low，取决于候选人提供的证据密度。

## Project Interview Drill Mode

如果用户说“模拟项目面试”“开始面试”“你提问我回答”“追问我这个项目”，不要只输出项目整理稿。先以面试官身份只问一个项目问题，等待候选人回答；候选人回答后，必须使用练习反馈结构：

```markdown
## Practice Round（练习轮次）: [Project Name] - [Question Topic]

## What I Heard（我听到的重点）
[复述候选人回答的核心内容]

## What Is Working（有效部分）
-

## Gaps To Close（需要补强）
-

## Scorecard（评分）
- 技术准确性 / 内容质量:
- 项目深度 / 表达结构:
- 个人贡献 / 岗位相关性:
- 表达结构 / 可信度:
- JD 匹配 / 差异化:

## Interviewer Read（面试官可能怎么理解）
[说明面试官会如何判断这个回答]

## Stronger Version（更稳回答）
[在不编造事实的前提下，给一版更稳表达；缺事实处用占位提示]

## Next Follow-Up（下一道追问）
[继续追问一个问题，或要求同题重答]
```

项目面试练习时，`What Is Working` 和 `Gaps To Close` 不能省略；评分必须给出，哪怕置信度较低。

## Output Schema

```markdown
## Project Deep Dive（项目深挖）: [Project Name]

## One-Sentence Positioning（一句话定位）
[一句话说明这个项目是什么，以及它证明了候选人的什么能力]

## Interview-Ready Explanation（面试可用讲法）
### 30 Seconds（30 秒）
[中文短版本]

### 90 Seconds（90 秒）
[中文标准面试版本]

### 3 Minutes（3 分钟）
[中文扩展版本，包含背景、方案、个人贡献、难点、结果和反思]

## Architecture Map（架构/流程图）
- 核心模块:
- 数据流:
- 关键依赖:
- 存储/缓存/消息:
- 部署/运行环境:

## Personal Contribution（个人贡献）
- 设计:
- 实现:
- 调试:
- 优化:
- 验证/度量:

## Technical Depth（技术深度）
| 领域 | 应该怎么说 | 可能追问 | 当前风险 |
|---|---|---|---|

## High-Frequency Follow-Up Questions（高频追问）
1.
2.
3.
4.
5.

## Weak Spots To Patch（需要补的弱点）
1. [gap] -> [what to review or rewrite]
2. [gap] -> [what to review or rewrite]
3. [gap] -> [what to review or rewrite]

## Scorecard（评分）
- 内容质量 / 技术准确性:
- 表达结构 / 项目深度:
- 岗位相关性 / 个人贡献:
- 可信度 / 表达结构:
- 差异化 / JD 匹配:

## Resume Bullet Upgrade（简历 bullet 升级）
- 当前写法:
- 更好写法:
- 为什么:

## Save To Project Bank
Add/update:
- Project ID:
- Name:
- Target role:
- Stack:
- Strongest selling point:
- Risk points:
- Linked fundamentals:
- Follow-up questions:

**Recommended next**: `practice` — 把这版项目讲法放到追问压力下测试。 **Alternatives**: `resume`, `stories`, `mock`
```

## Rules

- 不编造指标。没有指标时，建议候选人补充可验证证据或使用范围/反馈/交付物作为 proxy。
- 区分“参与过”和“能讲清”。候选人讲不清的点要标为风险。
- 必须追问个人贡献。
- 项目表达默认使用“结论先行 -> 背景 -> 方案 -> 个人贡献 -> 结果 -> 反思/取舍”。
- 技术项目可以保留 `Architecture Map`、`Technical Depth`；非技术项目也可以把它们解释为流程图和专业深度。
