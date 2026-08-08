# State Update Triggers

本文件定义什么时候必须写入 `coaching_state.md`。中文化时，状态章节名保持英文协议，写入内容可以是中文。

## Core Rule

只要命令产生了可复用信息，就必须保存。不要只在对话里说完就丢。

写入前遵守：

- 保留 `coaching_state.md` 的英文标题。
- 不删除已有历史，除非用户明确要求。
- 新信息追加到对应章节。
- 旧策略被替换时，记录到 Previous approaches。
- 不把用户隐私写入公开模板。

## Command Triggers

- `kickoff`：创建 `## Profile`、`## Resume Analysis`、`## Storybank`、`## Project Bank`、`## Score History`、`## Outcome Log`、`## Interview Intelligence`、`## Drill Progression`、`## Active Coaching Strategy`、`## Calibration State`、`## Session Log`、`## Coaching Notes`。
- `research`：更新 `## Interview Loops (active)`，记录 Status、Fit verdict、Fit confidence、Fit signals、Structural gaps、Date researched。
- `decode`：新增或更新 `## JD Analysis: [Company] — [Role]`，并同步 `Interview Loops`。
- `prep`：更新 `Interview Loops` 的轮次、format、fit verdict、concerns、prepared questions、next round。
- `resume`：更新 `## Resume Analysis` 和 `## Resume Optimization`。
- `pitch`：更新 `## Positioning Statement`。
- `stories`：更新 `## Storybank` 和 `### Story Details`，必须保存完整 STAR，不只保存索引。
- `project`：更新 `## Project Bank` 和 `### Project Details`；如能转成行为故事，也更新 `Storybank`。
- `practice` / `mock` / `analyze`：产生分数时写入 `## Score History`；同时更新弱项、策略和 `Session Log`。
- `analyze`：额外更新 `## Interview Intelligence` / `### Question Bank`、Effective/Ineffective Patterns、Company Patterns、`## Active Coaching Strategy`、`## Calibration State`。
- `debrief`：更新 `Outcome Log` 为 pending，记录 recalled questions、signals、stories used、feedback。
- `feedback`：按类型更新 Outcome Log、Recruiter/Interviewer Feedback、Calibration State、Coaching Notes 或 Meta-Check Log。
- `progress`：更新 `Active Coaching Strategy`、`Calibration State`、归档过长历史、记录 meta-check。
- `concerns`：写入对应公司 `Interview Loops` 的 Concerns surfaced，或写入 `Active Coaching Strategy`。
- `questions`：写入对应公司 `Interview Loops` 的 Prepared questions。
- `hype`：必要时更新 Anxiety profile 和 Session Log。
- `basics`：更新 `## China Campus Technical Prep` / `### Fundamentals / Bagua`。
- `algorithm`：更新 `### Algorithm Practice`。
- `hr`：更新 `### HR Prep`。
- `written`：更新 `### Written Test Tracker`。
- `school`：更新 `### Campus Application Tracker` 和相关 profile 字段。
- `present`：更新 `## Presentation Prep: [Topic / Company]`。
- `salary`：更新 `## Comp Strategy`。
- `negotiate`：将 offer 写入 `## Outcome Log`，并更新 `Comp Strategy`。
- `apply`：保存到 `job-search/[company]_application.md`，并更新 `Session Log`。
- `linkedin`：更新 `## LinkedIn Analysis`。
- `outreach`：更新 `## Outreach Strategy`。
- `thankyou`：更新 `Interview Loops` 或 `Session Log`。
- `reflect`：标记状态 archived，不删除 `coaching_state.md`。

## Always Save

以下情况也要保存：

- 用户报告真实面试结果。
- 用户提供招聘方反馈。
- 用户纠正教练判断。
- 用户透露会影响辅导方式的偏好、焦虑、时间安排或沟通习惯。
- 每次 meta-check 的反馈和调整。

## Archival

当 `Score History`、`Session Log`、`Question Bank` 等过长时，按 `archival-rules.md` 压缩旧记录。压缩时保留趋势、拐点和原因，不要只删数据。
