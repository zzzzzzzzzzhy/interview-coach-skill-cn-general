# apply — Job Application Question Drafting

本文件用于 `apply [company]` 命令。目标是帮助候选人回答网申、申请表、开放题和筛选问题。它生成的是“可粘贴的书面回答”，不是口语面试稿。

中文化规则：命令名、状态章节名、Output Schema 标题保持英文；草稿和解释使用中文。

## Inputs

- Company name
- Role
- Application questions
- Word / character limits
- JD
- Resume / Storybank / Project Bank

如果缺少问题，第一问：

“把申请表里的问题粘过来，最好连同字数/字符限制一起发。”

## Logic

1. 读取 `coaching_state.md`。
2. 解析每个问题类型：
   - Behavioral
   - Process / method
   - Tools / experience
   - Why us
   - Hypothetical / case
   - Other
3. 检查是否有证据：Storybank、Project Bank、Resume Analysis、用户提供的补充。
4. 缺证据时明确标出，不编造经历。
5. 行为题和方法题先选择故事/项目，再写答案。
6. Why us 必须基于 JD、research、prep 或候选人真实动机；没有公司信息时先问。
7. 按字数/字符限制写成书面语。
8. 保存到 `job-search/[company]_application.md`，如果目录存在或需要创建。
9. 更新 `Session Log`。

## Answer Style

- 结论先行。
- 书面语，紧凑，不像聊天。
- 第一人称，主动语态。
- 不要空泛热爱公司。
- 不要把没有做过的工具/行业经验写成做过。
- 没有明确指标时，用真实交付物、范围、反馈或职责边界替代。

## Output Schema

```markdown
## Application Draft: [Company] — [Role]
- Date:
- Source material:
- Limits:
- Confidence:

## Question Map
| Q | Type | Evidence source | Gap risk |
|---|---|---|---|

## Draft Answers

### Q1 [Type] — Story/project used: [S### / P### / none]
[ready-to-paste answer]

### Q2 [Type] — Story/project used: [S### / P### / none]
[ready-to-paste answer]

## Flagged Gaps
-

## Save
Update:
- job-search/[company]_application.md:
- Session Log:

**Recommended next**: `resume` — 把简历和网申回答统一到同一个岗位定位。 **Alternatives**: `decode`, `stories`, `project`
```

## Rules

- 不编造经历、工具、指标、动机或公司信息。
- 有字数限制时严格控制长度。
- 如果问题和已有答案相似，可以复用并改写，但不要让所有公司答案一模一样。
- 对中文网申，注意字符限制通常比英文 word limit 更紧。
