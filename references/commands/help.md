# help — Command Reference Workflow

本文件用于 `help` 命令。面向用户的说明默认中文，但命令名、文件名、状态章节名和 Output Schema 的英文标题保持不变。

## Logic

当用户输入 `help` 时，不要只给静态菜单。先读取 `coaching_state.md`，判断候选人当前阶段，再给出 2-3 个最值得做的命令。

优先级：

1. 没有 `coaching_state.md`：推荐 `kickoff`。
2. 有 JD 或正在比较岗位：推荐 `decode`。
3. 已经有目标岗位但简历未优化：推荐 `resume`。
4. 经历库为空：推荐 `stories`。
5. 项目/作品/案例讲不清：推荐 `project`。
6. 面试在 48 小时内：推荐 `prep` 和 `hype`。
7. 有面试文字稿未分析：推荐 `analyze`。
8. 刚面完但没有复盘：推荐 `debrief`。
9. 做过 3 次以上训练或面试：推荐 `progress`。
10. 技术岗基础薄弱：推荐 `basics`。
11. 算法/笔试薄弱：推荐 `algorithm` 或 `written`。
12. HR/终面临近：推荐 `hr`。
13. 有 offer 或薪资问题：推荐 `salary` 或 `negotiate`。

如果用户描述的是问题而不是命令，做诊断路由：

- “不知道从哪开始” -> `kickoff`
- “简历没回音” -> `resume` 或 `decode`
- “岗位不知道适不适合” -> `decode`
- “项目讲得很浅” -> `project`
- “不会讲经历” -> `stories`
- “一面老挂” -> `practice` 或 `analyze`
- “面试会紧张/卡壳” -> `practice` + `hype`
- “刚面完” -> `debrief`
- “有文字稿” -> `analyze`
- “要做展示/作品集讲解” -> `present`
- “薪资怎么说” -> `salary`
- “offer 怎么谈” -> `negotiate`

解释推荐理由时，必须结合候选人的状态，而不是泛泛列菜单。

## Output Schema

```markdown
## Command Guide

### Getting Started
| Command | What It Does |
|---|---|
| `kickoff` | 建立候选人画像，确认目标岗位、行业、时间线、风险点和第一阶段计划 |
| `help` | 查看命令菜单，并根据当前状态推荐下一步 |

### Application Materials
| Command | What It Does |
|---|---|
| `decode` | 分析 JD，提取岗位要求、隐藏信号、匹配度、风险点和简历调整方向 |
| `research [company]` | 调研公司/机构，判断是否值得投入，并准备投递或面试背景 |
| `resume` | 优化简历，检查结构、关键词、经历表达、岗位匹配和可追问性 |
| `pitch` | 打磨自我介绍、职业定位和不同场景下的短版本表达 |
| `stories` | 建立经历故事库，沉淀 STAR、贡献、结果、反思和可复用素材 |
| `project` | 深挖项目、作品、案例或代表性经历，准备 30 秒/90 秒/3 分钟版本和追问 |
| `apply [company]` | 起草网申开放题、申请表或筛选题回答 |

### Interview Round Prep
| Command | What It Does |
|---|---|
| `prep [company]` | 针对公司/岗位做面试准备，生成重点能力、预测问题、故事匹配和临场清单 |
| `concerns` | 预测面试官对候选人的顾虑，并准备证据和回应 |
| `questions` | 准备反问面试官的问题 |
| `present` | 准备展示型面试、作品集讲解、案例汇报或方案陈述 |
| `hype` | 面试前快速提振，整理 3 个优势、3 个风险回应和 3 个反问 |

### Practice and Simulation
| Command | What It Does |
|---|---|
| `practice` | 单题练习，训练结构、内容、追问、压力场景和表达稳定性 |
| `mock [format]` | 完整模拟面试，支持综合面、行为面、技术面、案例面、群面/多面官等形式 |

### Analysis and Tracking
| Command | What It Does |
|---|---|
| `debrief` | 面后快速复盘，记录问题、表现、面试官信号和下一轮风险 |
| `analyze` | 分析面试文字稿或问答记录，逐题评分并定位根因 |
| `feedback` | 记录 HR/面试官反馈、推进/拒绝/offer 结果，修正后续训练判断 |
| `progress` | 阶段复盘，查看分数趋势、故事库健康度、目标匹配和下一阶段计划 |

### Technical / Campus Add-ons
| Command | What It Does |
|---|---|
| `basics` | 技术基础/八股练习，适合 Java、C++、OS、网络、数据库、Redis、Spring、测试、安全等 |
| `algorithm` | 算法题、笔试编程和口述解题训练 |
| `written` | 笔试、在线测评、行测、SQL、选择题和错题规划 |
| `school` | 校招批次、投递节奏、公司梯队和周计划 |
| `hr` | HR 面准备，覆盖动机、稳定性、职业规划、优缺点、压力、薪资期望 |

### Compensation and Closing
| Command | What It Does |
|---|---|
| `salary` | 早期薪资期望表达，避免过早锚定低价 |
| `negotiate` | offer 后谈薪策略、话术和备选方案 |
| `thankyou` | 面后感谢/跟进消息 |
| `linkedin` | 优化 LinkedIn、脉脉、BOSS 或个人主页 |
| `outreach` | 写内推、私信、邮件、HR 回复和跟进消息 |
| `reflect` | 求职阶段复盘和归档 |

---

## Where You Are Now
[用中文总结当前状态：目标岗位、阶段、故事/项目数量、最近训练、活跃面试流程。若没有状态文件，写：No coaching state found. Run `kickoff` to get started.]

## Recommended Next
**Recommended next**: `[command]` — [中文说明为什么现在做它最划算]. **Alternatives**: `[command]`, `[command]`, `[command]`

---

## Tips
- 第一次使用先跑 `kickoff`。
- 有 JD 先跑 `decode`，不要盲目改简历。
- 有真实面试后当天跑 `debrief`，信息最鲜。
- 有文字稿就跑 `analyze`，不要只凭感觉复盘。
- 技术岗先把 `project` 讲深，再补 `basics` 和 `algorithm`。
- 所有个人数据默认保存到 `coaching_state.md`，公开仓库不要上传这个文件。

What would you like to work on?
```

## Rules

- 用户可见说明用中文。
- 命令名、文件名、状态章节名不翻译。
- 推荐必须基于 `coaching_state.md` 或用户刚提供的信息。
- 不确定时给出置信度，不编造状态。
