# Versions

本文件记录中文版通用面试教练 Skill 的版本变化。

## v1-cn-general

当前公开 MVP 版本。

### 主要变化

- 将项目定位改为中文通用面试教练。
- 默认中文交流，支持校招、实习、社招、转岗和复试。
- 支持技术、产品、运营、市场、销售、设计、职能、金融、咨询、教育、制造业等方向。
- 保留原项目核心能力：候选人画像、JD 分析、简历优化、故事库、项目库、模拟面试、真实面试复盘、进度追踪。
- 新增 `references/translation-policy.md`，明确“协议层不翻译，展示层中文化”。
- 删除公开副本中的真实 `coaching_state.md`。
- 新增 `coaching_state.example.md`。

### 已中文化的命令

- `kickoff`
- `help`
- `decode`
- `resume`
- `stories`
- `project`
- `practice`
- `mock`
- `analyze`
- `debrief`
- `feedback`
- `progress`
- `prep`
- `research`
- `concerns`
- `questions`
- `pitch`
- `present`
- `basics`
- `algorithm`
- `hr`
- `written`
- `school`
- `apply`
- `hype`
- `thankyou`
- `reflect`
- `salary`
- `negotiate`
- `linkedin`
- `outreach`

### 已中文化的参考规则

- `archival-rules.md`
- `calibration-engine.md`
- `challenge-protocol.md`
- `coaching-state-schema.md`
- `coaching-voice.md`
- `cross-cutting.md`
- `differentiation.md`
- `evidence-sourcing.md`
- `examples.md`
- `mode-detection.md`
- `role-drills.md`
- `rubrics-detailed.md`
- `schema-migration.md`
- `state-update-triggers.md`
- `storybank-guide.md`
- `story-mapping-engine.md`
- `transcript-formats.md`
- `transcript-processing.md`

### 兼容性约定

以下内容保持英文：

- 命令名。
- 文件名。
- `coaching_state.md` 章节标题。
- Output Schema 标题。
- 状态表头、ID、枚举值。

这样可以避免翻译导致跨文件引用和状态读写失效。

## Upstream

本项目基于 [noamseg/interview-coach-skill](https://github.com/noamseg/interview-coach-skill) 改造。原项目采用 MIT License。
