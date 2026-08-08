# Mode Detection Priority

本文件定义用户没有输入明确命令时，如何判断该执行哪个命令。命令名保持英文。

## Priority

按顺序匹配，先命中的优先：

1. 明确命令：直接执行对应命令。
2. 粘贴了面试文字稿或大量问答记录：`analyze`。
3. 招聘方反馈、面试结果、纠正教练判断、补充面试记忆、反馈教练方式：`feedback`。
4. 刚面完、刚结束面试、想复盘但无文字稿：`debrief`。
5. 有具体公司 + JD + 面试准备意图：`prep`。
6. 只有公司名，想了解要不要投：`research`。
7. JD 分析、岗位适配、比较多个岗位、是否该投：`decode`。
8. 简历优化、中文简历、校招简历、项目经历写法：`resume`。
9. 自我介绍、个人定位、怎么介绍自己：`pitch`。
10. 经历故事、STAR、行为面素材：`stories`。
11. 项目/作品/案例讲解、项目亮点、难点、贡献：`project`。
12. 单题练习、追问、压力练习：`practice`。
13. 完整模拟面试：`mock [format]`。
14. 展示、作品集、案例汇报、PPT 面试：`present`。
15. 反问面试官：`questions`。
16. 面试官可能质疑什么：`concerns`。
17. 面试前很紧张、明天面试、临场清单：`hype`。
18. 技术基础、八股、Java/C++、OS、网络、数据库、Redis、Spring：`basics`。
19. 算法、LeetCode、牛客、笔试编程：`algorithm`。
20. 笔试、在线测评、行测、选择题：`written`。
21. 校招、秋招、春招、实习批次、投递节奏：`school`。
22. HR 面、终面、稳定性、职业规划、薪资期望：`hr`。
23. 网申开放题、申请表问题、筛选问题：`apply`。
24. 职业主页、LinkedIn、脉脉、BOSS 在线简历：`linkedin`。
25. 私信、内推、邮件、联系 HR、校友：`outreach`。
26. offer 前薪资期望：`salary`。
27. 已有正式 offer：`negotiate`。
28. 阶段复盘、趋势、最近进步：`progress`。
29. 求职结束、接受 offer、暂停求职：`reflect`。
30. 不确定：建议 `kickoff` 或 `help`。

## China Campus Recruiting Override

如果用户提到国内校招、秋招、春招、暑期实习、日常实习、牛客、笔试、八股、HR 面、技术面，优先使用：

- 项目深挖 -> `project`
- 八股/基础 -> `basics`
- 算法/笔试编程 -> `algorithm`
- HR 面 -> `hr`
- 笔试/测评 -> `written`
- 校招节奏 -> `school`
- 校招简历 -> `resume`

## Multi-Step Intent Detection

当用户表达的是一串目标时，说明路径并先执行第一步，不要一次性完成所有命令。

| Intent | Sequence |
|---|---|
| 开始找工作 | `kickoff` -> `stories` / `project` -> `pitch` -> `resume` |
| 准备某家公司面试 | `research` -> `prep` -> `concerns` -> `practice` -> `hype` |
| 有 JD 想判断 | `decode` -> `resume` -> `prep [company]` |
| 刚面完 | `debrief` -> `analyze` -> `feedback` / `progress` |
| 技术校招准备 | `kickoff` -> `project` -> `basics` -> `algorithm` -> `mock technical` |
| 展示轮 | `present` -> `practice` -> `mock presentation` -> `hype` |
| 薪资问题 | `salary` -> `negotiate` |
| 开始 networking | `pitch` -> `linkedin` -> `outreach` |

## Rules

- 显式命令优先于意图推断。
- transcript 优先于普通复盘。
- 用户如果纠正路由，立刻按用户意图调整。
- 多步骤流程每一步结束后推荐下一步，不强迫继续。
- 所有用户可见说明用中文。
