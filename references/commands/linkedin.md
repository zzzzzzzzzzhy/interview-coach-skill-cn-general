# linkedin — Online Profile Optimization

本文件用于 `linkedin` 命令。原项目主要针对 LinkedIn；中文版通用版将它扩展为“线上职业主页优化”，可用于 LinkedIn、脉脉、BOSS 直聘在线简历、个人主页、作品集首页等。

中文化规则：命令名保持 `linkedin`，状态章节 `## LinkedIn Analysis` 保持英文；分析和改写内容使用中文。

## Priority Check

先读取 `coaching_state.md`。

- 没有 `kickoff`：可以做通用审查，但提醒缺少目标岗位上下文。
- 48 小时内有面试：建议先 `prep` / `hype`。
- 没有 `Positioning Statement`：可基于简历分析，但建议后续 `pitch`。
- 如果用户不是海外求职，明确说明此命令也可用于国内职业主页。

## Required Inputs

- Profile URL or pasted profile text
- Target role context
- Platform

如果用户只给链接但无法访问，第一问：

“我可能无法直接读取这个平台页面。你把标题、简介、经历、技能这几段粘过来，我按目标岗位帮你改。”

## Review Lenses

1. Searchability：关键词是否能被招聘方搜到。
2. First impression：前 3 行是否清楚说明你是谁。
3. Positioning：是否和简历、pitch 一致。
4. Evidence：是否有项目、成果、作品、数据或证明。
5. Role relevance：是否贴合目标岗位。
6. Credibility：是否可信、不过度包装。
7. Differentiation：是否有记忆点。
8. Conversion：看完后对方是否知道该联系你做什么。

## Platform Adaptation

- LinkedIn：headline、about、skills、experience、featured、recommendations。
- 脉脉：个人标签、简介、经历、项目、动态表达。
- BOSS：在线简历标题、求职意向、项目/经历关键词、沟通开场。
- 个人主页/作品集：首屏定位、项目顺序、案例摘要、联系方式。
- GitHub/技术主页：README、Pinned repos、项目说明、技术栈和贡献证明。

## Depth Levels

| Level | When to Use | What It Covers |
|---|---|---|
| Quick Audit | 快速检查 | Top 3 fixes |
| Standard | 默认 | 分区审查 + 关键段落重写 |
| Deep Optimization | 求职主阵地 | 全面改写 + 定位一致性 + 内容策略 |

## Output Schema

```markdown
## LinkedIn Analysis
- Date:
- Platform:
- Depth:
- Target role:
- Overall:

## Profile Read
- First impression:
- Searchability:
- Credibility:
- Differentiation:

## Section Audit
| Section | Current issue | Better direction | Rewrite |
|---|---|---|---|

## Keyword Strategy
- Must-have keywords:
- Supporting keywords:
- Avoid / don't overclaim:

## About / Summary Rewrite
[中文或英文版本，按用户目标平台]

## Experience / Project Rewrite
| Item | Better version | Why |
|---|---|---|

## Consistency Check
- Resume:
- Pitch:
- Storybank / Project Bank:
- Outreach:

## Content / Activity Suggestions
- What to post or showcase:
- What to avoid:

## Save
Update:
- LinkedIn Analysis:
- Positioning Statement, if refined:
- Session Log:

**Recommended next**: `outreach` — 把刚优化好的主页定位用到私信、内推或邮件里。 **Alternatives**: `pitch`, `resume`, `stories`
```

## Rules

- 不要把主页写成简历复制版。
- 不要堆关键词到不自然。
- 不要写候选人没有证据支持的身份标签。
- 国内平台可以更直接突出求职意向和项目证据。
- 写状态时保留 `## LinkedIn Analysis` 英文标题，即使平台不是 LinkedIn。
