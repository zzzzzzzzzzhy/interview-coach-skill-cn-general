# reflect — Post-Search Retrospective Workflow

本文件用于 `reflect` 命令。目标是在候选人拿到 offer、暂停求职、转向新目标或完成一段长期训练后，做完整复盘和归档。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；复盘叙事和建议使用中文。

## When to Trigger

- 候选人接受 offer。
- 候选人决定暂停或停止求职。
- 长期训练后想总结。
- 候选人问“我这一轮到底学到了什么？”
- 8+ sessions 后很久没有新动作。

## Logic

1. 承认节点：offer、暂停、转向或阶段结束。
2. 读取完整 `coaching_state.md`。
3. 复盘开始状态：目标、担心点、初始分数、故事库。
4. 复盘变化轨迹：分数、故事/项目、真实面试结果、自评校准。
5. 找 breakthrough：哪几次训练真正改变了表现。
6. 找 persistent challenges：哪些问题还没解决。
7. 如果拿到 offer，分析什么起了作用。
8. 如果没有 offer 或暂停，给诚实诊断。
9. 提炼可迁移能力：表达、结构化思考、自我校准、抗压。
10. 标记状态为 archived，但不要删除。

## Output Schema

```markdown
## Retrospective: [Name]'s Interview Journey

## The Arc
- Duration:
- Sessions completed:
- Real interviews:
- Outcomes:
- Final result:

## Where You Started
- Initial scores:
- Initial storybank:
- Initial assessment:
- Biggest concern at start:

## Where You Are Now
- Current scores:
- Storybank health:
- Overall change:

## Breakthroughs
1.
2.
3.

## Persistent Challenges
1.
2.

## What Made the Difference (if offer received)
- The dimensions that predicted your advances:
- The stories that landed:
- The change between early rounds and later rounds:

## What's Still Open (if no offer / pausing)
- Remaining gaps:
- Honest diagnosis:
- If you resume, start here:

## Transferable Skills
- Storytelling and communication:
- Self-awareness and calibration:
- Thinking under pressure:
- Other:

## Storybank Snapshot (archived)
[Final state of storybank for future reference]

## Coaching State Archived
[Note that coaching_state.md is being preserved, not deleted]

**Recommended next**: `kickoff` — 如果要开始新一轮求职，先重新建立候选人画像。 **Alternatives**: `help`
```

## Coaching State Handling

- 不删除 `coaching_state.md`。
- 在顶部或 `Session Log` 标记：`Status: Archived [date] — [reason]`。
- 如果候选人以后再次 `kickoff`，询问是继承旧状态还是重新开始。

## Rules

- 不要把普通结果包装成虚假成功。
- 有 offer 就总结成功模式。
- 没 offer 也要给可执行复盘，不责备候选人。
- 归档是保存，不是清空。
