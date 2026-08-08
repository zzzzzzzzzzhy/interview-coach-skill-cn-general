# Translation Policy

本文件定义中文版改造的术语和兼容性规则。后续翻译任何 `.md` 文件时都按这里执行。

## Core Rule

协议层不翻译，展示层中文化。

也就是：系统用来路由、读写状态、跨文件引用的标识保持英文；候选人实际看到的解释、建议、示范回答和训练内容使用中文。

## Do Not Translate

以下内容保持英文：

- 命令名：`kickoff`、`help`、`decode`、`resume`、`stories`、`project`、`practice`、`mock`、`analyze`、`debrief`、`feedback`、`progress` 等。
- 文件名和路径：`AGENTS.md`、`SKILL.md`、`coaching_state.md`、`references/commands/*.md`。
- 状态章节标题：`## Profile`、`## Resume Analysis`、`## Project Bank`、`## Storybank`、`## Score History`、`## Outcome Log`、`## Interview Intelligence`、`## Active Coaching Strategy`、`## Calibration State`、`## Session Log`、`## Coaching Notes`。
- Output Schema 标题：如 `## Scorecard`、`## What Is Working`、`## Gaps To Close`、`## Recommended Next Step`。如果面向中文候选人，可以加中文括注，如 `## Kickoff Summary（启动总结）`。
- 状态表头和 ID：如 `S001`、`P001`、`Date`、`Company`、`Role`、`Result`。
- 状态枚举值：如 `Quick Prep`、`Full System`、`Strong Fit`、`Investable Stretch`、`High / Medium / Low`。用户可见输出可以写成中文 + 英文括注，如 `系统训练（Full System）`。

## Translate

以下内容可以翻译成中文：

- 面向用户的说明。
- 训练提问。
- 反馈正文。
- 示例回答。
- 诊断解释。
- 推荐理由。
- README 中的使用说明。
- 用户可见摘要字段名，例如把 `Track` 写成“训练模式”、把 `Timeline` 写成“准备时间线”。
- 用户可见分析字段名，例如把 `Strong signals` 写成“强匹配信号”、把 `ATS compatibility` 写成“ATS 兼容性”。

## Preferred Style

使用“英文协议名 + 中文解释”。如果某个标题是用户会频繁看到的分析块，优先加中文括注，字段名用中文：

- 好：`## Scorecard` 下用中文解释每个分数。
- 坏：把 `## Scorecard` 改成 `## 评分表`，但其他文件仍引用 `Scorecard`。
- 更好：`## Scorecard（评分）` 下写 `- ATS 兼容性: 4/5`、`- 岗位相关性: 5/5`。

保留英文标题时，正文不要生硬夹杂英文。必要术语可第一次出现时写成：

- `Relevance`：回答是否命中问题和岗位要求。
- `Credibility`：候选人个人贡献和真实性是否可信。
- `Differentiation`：回答是否有辨识度。

## Consistency Checks

每次翻译后至少检查：

1. 是否误翻命令名。
2. 是否误翻 `coaching_state.md` 的章节标题。
3. 是否误翻 Output Schema 标题。
4. 是否把用户个人状态文件或隐私信息带入公开副本。
5. 是否出现同一个概念一会儿中文、一会儿英文且没有解释。
