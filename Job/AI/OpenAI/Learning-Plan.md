# OpenAI Agent Development 学习计划

**资料索引：** [OpenAI 官方资料](References.md)  
**学习指引：** [Job 共享技术学习指引](../../instructions/learning.md)  
**状态：** 计划已建立，尚无本计划下的学习表现记录。

## 学习目标

能够用 OpenAI 的代码式工具构建一个小型 Agent，解释 Agent、工具、handoff 与运行 turn 的关系，检查 tracing，并用数据集或 trace grading 评估行为。

## 学习路线

| 阶段 | 资料与主题 | 学习产出 |
|---|---|---|
| 1. 概念与选型 | Building agents guide | 说明 Agents SDK、Agents API 与直接模型调用适用的任务范围 |
| 2. 最小实现 | SDK quickstart、Agent definitions | 运行单 Agent，描述 instructions、tools 和输出约束 |
| 3. 工具执行与编排 | Running agents、SDK 的 orchestration/handoffs | 追踪一次工具调用与一次 handoff，明确实际执行方和停止条件 |
| 4. 集成与可观测性 | Integrations and observability | 读取 trace，定位模型调用、工具调用、审批或 handoff 的问题 |
| 5. 评估与改进 | Evaluate agent workflows、Trace grading | 建立小型评估集，比较行为并基于 trace 归因失败 |

## 每次学习

1. 从本计划 checkpoint 恢复，并读取本次指定的官方页面。
2. 用中文讲清机制、实现例子和限制，一次提出一个练习或迁移问题。
3. 把少量关键英语术语、搭配或句式自然嵌入相关说明，现场解释含义和用法。必要时给短技术例句，不另开英语环节、不列词表、不凑数量。
4. 对值得长期复习的表达检查 English study inbox 并去重后再添加。
5. 将实际理解证据与下一步记入本文件。按 Learning Skill 与 Agent Tutor skill 的适用方法组织学习，但遵循 Learning Hub 的进度规则。

## 进度与 checkpoint

本文件是本课程的唯一进度主档。使用 Planned、Introduced、Practiced、Demonstrated、Retention checked 标记；记录来源、回答/实践证据、疑问、英语 inbox 项目和下一步。未被实际回答或实践验证的概念不标为掌握。

### 当前 checkpoint

- **状态：** Planned。尚无本计划下的学习表现记录。
- **下一步：** 阅读 Building agents guide，说明何时需要 Agent 编排而非单次模型调用。
- **English inbox：** 后续按需选择表达并去重。
