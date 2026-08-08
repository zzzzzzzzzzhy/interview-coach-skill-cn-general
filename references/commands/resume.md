# resume — Resume Optimization Workflow

本文件用于 `resume` 命令。目标是把简历从“信息堆叠”改成“岗位匹配证据”。用户可见内容用中文；状态章节、命令名、Output Schema 标题保持英文。

## Logic

先读取：

- `coaching_state.md`，如果存在
- `references/differentiation.md`
- `references/storybank-guide.md`，如果故事库或项目库存在

如果用户没有粘贴简历，第一问：

“把你当前简历文本粘过来，或者先粘你最想改的一段。”

如果有 JD，同时做 JD-targeted 优化；如果没有 JD，做通用版优化。

## Review Lenses

从以下角度检查：

1. ATS compatibility：格式、关键词、岗位硬要求是否容易被系统识别。
2. Recruiter scan：7-15 秒内能否看出目标岗位、强信号和匹配点。
3. Positioning：简历是否有清晰主线，而不是多个方向并列堆叠。
4. Bullet quality：每条经历是否有动作、对象、方法、结果。
5. Evidence density：是否有指标、规模、反馈、交付物或可验证证明。
6. Role relevance：内容是否服务目标岗位。
7. Concern management：是否主动降低面试官疑虑。
8. Interview defensibility：写上去的内容是否能被追问三层。
9. Cross-surface consistency：简历、故事库、项目库、pitch 是否一致。

## Depth Levels

- Quick Audit：快速指出 3-5 个最高优先级问题。
- Standard：逐段分析并重写关键 bullet。
- Deep Optimization：结合 JD、故事库和项目库，重构定位、关键词和经历顺序。

候选人没指定深度时，默认 `Standard`。

## Bullet Rewrite Standard

优秀 bullet 通常包含：

`动作 + 对象/场景 + 方法/工具 + 结果/影响`

例：

- 弱：负责用户运营，提高用户活跃。
- 强：针对新用户 7 日留存偏低问题，设计分层触达和内容引导流程，推动 3 个渠道联动执行，使新用户次周活跃率提升 X%。

没有真实指标时，不要编造。可以改为：

- “支持 X 人团队使用”
- “覆盖 X 个流程/模块”
- “交付 X 份报告/页面/活动/功能”
- “获得导师/主管/客户反馈”
- “作为课程/竞赛/实习交付物完成”

## Output Schema

```markdown
## Resume Optimization（简历优化）
- 日期:
- 分析深度:
- 是否针对 JD:
- 整体判断:

## Top Findings（最优先问题）
1.
2.
3.

## ATS / Keyword Read（ATS 与关键词）
- 优势:
- 缺口:
- 修改建议:

## Recruiter Scan（招聘方快速浏览）
- 10 秒内清楚的信息:
- 容易困惑的信息:
- 修改建议:

## Positioning（定位）
- 当前信号:
- 更好的定位:
- 原因:

## Bullet Rewrite（经历改写）
| 模块 | 当前写法 | 更好写法 | 为什么 |
|---|---|---|---|

## Interview Defensibility（可追问性）
| 简历主张 | 可能追问 | 风险 | 补强方式 |
|---|---|---|---|

## Storybank / Project Bank Pull-Through（故事库/项目库联动）
- 应该露出的强素材:
- 需要补充的证据:
- 下一步要打磨的故事/项目:

## Scorecard（评分）
- ATS 兼容性:
- 招聘方快速浏览:
- Bullet 质量:
- 岗位相关性:
- 可信度:

## Save To Coaching State
Update:
- Resume Optimization:
- Resume Analysis:
- Active Coaching Strategy:
- Session Log:

**Recommended next**: `project` — 先把最能决定面试表现的经历讲深，再继续润色。 **Alternatives**: `decode`, `stories`, `practice`
```

## Rules

- 不编造学历、经历、公司、指标、技术栈或结果。
- 不要只润色语言；必须指出岗位匹配和可追问风险。
- 中文简历避免空泛形容词，如“优秀”“良好”“熟悉”，除非后面有证据。
- 技术岗特别检查项目名词是否能讲清；非技术岗特别检查结果、过程和个人贡献。
- 面向用户的简历分析字段用中文标签；状态写入保持 `## Resume Analysis` 和 `## Resume Optimization` 英文标题。
