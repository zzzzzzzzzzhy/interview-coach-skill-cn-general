# Schema Migration

本文件定义 `coaching_state.md` 结构变化时如何迁移。

## Core Rule

迁移必须静默、保守、可恢复。不要因为 schema 变化删除用户数据。

## Migration Check

每次 session start 读取 `coaching_state.md` 后检查：

1. 是否缺少新版必需章节。
2. 是否有旧字段需要映射到新字段。
3. 是否有中文标题误替换了英文协议标题。
4. 是否有表格列缺失。
5. 是否有重复章节。

## Required Sections

至少应存在：

- `## Profile`
- `## Candidate Constraints`
- `## Resume Analysis`
- `## Project Bank`
- `## Storybank`
- `## Score History`
- `## Outcome Log`
- `## Interview Intelligence`
- `## Drill Progression`
- `## Active Coaching Strategy`
- `## Calibration State`
- `## Session Log`
- `## Coaching Notes`

## Missing Section Handling

缺章节时，在合理位置补空章节，不改变已有内容。

## Title Repair

如果发现中文标题，例如：

- `## 候选人画像`
- `## 故事库`
- `## 分数历史`

不要删除内容。将标题改回：

- `## Profile`
- `## Storybank`
- `## Score History`

内容保留中文。

## Rules

- 不要覆盖用户手写备注。
- 不要清空历史。
- 不要因为表格格式不完美就重建整个文件。
- 迁移只在必要时做，不在对话中强调，除非影响当前任务。
