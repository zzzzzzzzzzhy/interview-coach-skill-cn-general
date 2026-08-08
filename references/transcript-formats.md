# Transcript Formats

本文件定义文字稿格式识别。用于 `analyze`。

## Supported Inputs

- Zoom / Teams / Google Meet 转写。
- Otter / Grain / Tactiq / Granola 等会议记录。
- 用户手动整理的 Q&A。
- 聊天记录式面试。
- 中文、英文或中英混合文字稿。

## Detection Signals

识别：

- 是否有 speaker labels。
- 是否有 timestamps。
- 是否多面试官。
- 是否 Q&A 结构明显。
- 是否有系统设计/案例/专业讨论阶段。
- 是否候选人发言占比异常低或异常高。

## Normalization

统一成内部表示：

```markdown
[Interviewer]:
[Candidate]:
```

或按单元：

```markdown
Q1:
Candidate answer:
Follow-ups:
```

## Quality Levels

- High：说话人清楚，问答完整。
- Medium：有少量缺失或标签混乱。
- Low：大量缺失、无法判断说话人或内容不完整。

Low quality 时可以分析，但必须降低 Confidence。

## Rules

- 清理格式不能改变候选人原意。
- 不要把转写错误当成候选人真实错误，除非上下文支持。
- 引用原文要短。
