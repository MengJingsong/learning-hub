# Anthropic AI Agent Development 学习计划

**资料索引：** [Anthropic 官方资料](References.md)  
**学习指引：** [Job 共享技术学习指引](../../instructions/learning.md)  
**状态：** 计划已建立，尚无本计划下的学习表现记录。

## 学习目标

能够解释 Anthropic 资料中的 Agent/workflow 架构取舍，设计上下文和工具接口，分析长程执行的恢复问题，并用可重复评估检查 Agent 行为。

## 学习路线

| 阶段 | 资料与主题 | 学习产出 |
|---|---|---|
| 1. 架构基础 | Building effective AI agents：augmented LLM、workflow、agent 及常用模式 | 用同一任务说明何时用固定 workflow，何时需要 Agent 自主决策 |
| 2. 工具与上下文 | 上述文章的工具设计；Effective context engineering | 设计一个边界明确的工具接口，并说明上下文保留、检索和压缩策略 |
| 3. 长程任务 | Effective harnesses for long-running agents | 画出跨上下文窗口的任务状态、文件/记忆、恢复与验证流程 |
| 4. 评估 | Demystifying evals for AI agents | 为一个任务设计代表性样本、评分标准和失败归因方法 |
| 5. 连接标准 | MCP 文档及按需查阅 Claude Platform 文档 | 说明 MCP 解决的连接问题，并实现或审查一个工具连接示例 |

按阶段推进，每次聚焦一个概念或紧密相关的一小组概念。API 实作应以当前官方文档为准。

## 每次学习

1. 从本计划 checkpoint 恢复，必要时简短回忆上次概念。
2. 读取指定原文，区分 Anthropic 的明确建议、案例观察和自己的推论。
3. 用中文说明机制、假设、例子和权衡，一次提出一个解释或迁移问题。
4. 将少量关键英文表达自然放在对应技术解释旁，说明词义和实际用法；必要时给简短技术例句。不单独列词表或另开英语环节，不硬凑数量。
5. 检查 English study inbox 重复项，仅加入值得长期复习的表达。
6. 按证据更新下方 checkpoint。沿用 Learning Skill 和 Agent Tutor skill 中适用的教学/计划方法，遵守 Learning Hub 现有的进度规范。

## 进度与 checkpoint

本文件是本课程的唯一进度主档。记录章节/来源、概念状态、实际作答证据、待回顾问题、英语 inbox 项目和下一步。状态采用 Planned、Introduced、Practiced、Demonstrated、Retention checked。听过讲解或表示理解不等于掌握。遵循 [Job 共享技术学习指引](../../instructions/learning.md)。

### 当前 checkpoint

- **状态：** Planned。尚无本计划下的学习表现记录。
- **下一步：** 阅读 Building effective AI agents，先辨析 workflow 与 agent 的控制方式。
- **English inbox：** 后续按需选择表达并去重。
