# 开放大模型：学习计划

建立日期：2026-11-17（America/New_York）。  
资料索引：[References.md](References.md)。  
学习指引：[Job 技术学习指引](../../instructions/learning.md)。  
状态：Planned；尚无本计划下的实际学习或测评证据。

## 学习目标

能够沿着一个具体模型解释输入 token、模型结构、训练目标、数据、评估与输出之间的关系；从论文和代码定位证据；比较不同模型的工程取舍，并明确公开信息的边界。

参考 [Anthropic 学习计划](../Anthropic/Learning-Plan.md) 的阶段产出与 checkpoint，以及 [AI Engineering 学习计划](../Foundation/AI-Engineering-Agent-Learning-Plan.md) 的单知识点推进和评估规则。主线为 Pythia → OLMo 3 → DeepSeek-V3，Llama 4 为选学扩展。

## 学习方式与先修

- 不设置硬性周数，每次只选一个具体知识点，充分答疑后由学习者决定是否进入下一点。
- 开始时读取本 checkpoint、[AI Mastery](../mastery.md) 和 [AI Session Log](../session-log.md)。未评估表示未知，不能据此默认零基础。
- 先修包括 token、向量与矩阵、概率、梯度下降、Python 基础；读实现时按需补 PyTorch 张量操作。仅补当前知识点需要的内容，通用笔记链接到 [Foundation](../Foundation/README.md)。
- 中文讲解配合关键 English 术语：直觉 → 定义与机制 → 具体例子 → 假设、限制与取舍。区分作者结论、实验观察和自己的推论。
- 以下练习是用户要求练习或测试时的题目设计。先讲解与答疑，只有用户明确要求后才测试；一次一题，先作答再给反馈或渐进提示。
- 用户说“懂了”不等于掌握。测试通过后也等用户明确要求再进入下一点；用户选择不测试而继续时保留未评估状态。
- 当前可用运行时没有 Learning Skill 或 Agent Tutor 专用技能时，直接遵循仓库流程；后续若可用，参考其适用教学方法，不建立额外记录系统。
- 实践先选小模型或缩小机制示例；实施前确认设备和资源条件。完整预训练和部署大型模型不作为学习前提。

## 学习路线

编号对应 [资料索引](References.md)。每个表格单元中的知识点分别学习，不作为一次课的任务清单。

| 阶段 | 单知识点 ID 与主题 | 资料与阅读位置 | 可观察产出／练习设计 |
|---|---|---|---|
| 0. 认识模型产物 | `om.artifacts`：权重、配置、tokenizer、训练 checkpoint；`om.openness`：开放范围 | P2 模型与加载说明；O2 阶段产物 | 用自己的话说明各产物作用；根据官方材料列出已公开和未确认的部分 |
| 1. Pythia：训练目标与结构 | `om.pythia.next-token`：next-token prediction；`om.pythia.forward`：token 到 logits；`om.pythia.causal-mask`：因果遮罩 | P1 模型设计与训练设置；P2 链接的配置和实现 | 用短序列写出训练输入与标签；追踪一次前向计算，解释为何不能读取未来 token |
| 2. Pythia：训练动态 | `om.pythia.checkpoints`：训练步数与检查点；`om.pythia.controls`：比较中的控制变量；`om.pythia.evidence`：损失与能力证据 | P1 受控模型套件与案例；P2 checkpoint 示例 | 固定同一小模型、输入与生成设置，对比两个 checkpoint；解释哪些变化可观察、哪些结论还缺证据 |
| 3. OLMo：预训练流程 | `om.olmo.data`：数据过滤、去重与混合；`om.olmo.pretraining`：目标与训练配置；`om.olmo.stages`：不同训练阶段 | O1 数据、预训练与模型流程；O2 数据和代码入口 | 画出所选模型的“数据 → 训练 → 检查点 → 评估”流程，并给各节点标注来源 |
| 4. OLMo：后训练与评估 | `om.olmo.sft`：监督微调；`om.olmo.dpo`：偏好优化；`om.olmo.rlvr`：可验证奖励；`om.olmo.eval`：评估条件与污染 | O1 对应 Instruct/Think 分支的后训练和评估部分；O2 阶段模型 | 用一个任务比较不同训练目标的监督信号；制定 Base 与后训练 checkpoint 的公平比较方案 |
| 5. DeepSeek-V3：架构与效率 | `om.deepseek.moe`：专家路由与总／激活参数；`om.deepseek.balance`：负载均衡；`om.deepseek.mla`：MLA 与 KV cache；`om.deepseek.mtp`：多 token 预测 | D1 架构、训练和实验；D2 推理实现 | 追踪一个 token 的专家选择；解释计算量、显存与通信的区别；选择一个机制做简化算例或实现 |
| 6. 综合比较 | `om.comparison`：架构、数据、训练与评估证据 | P1/P2、O1/O2、D1/D2 | 为一个明确任务写模型比较笔记，保留版本、评估条件和未知项；说明学习或实验选择的理由 |
| 7. 选学：Llama 4 | `om.llama.multimodal`：多模态融合；`om.llama.moe`：MoE 对照 | L1 架构与训练概览，必要时从官方页面进入模型卡 | 解释图像信息如何进入模型；对比与文本模型的差异，区分官方披露和未披露细节 |

阶段 1 如有先修缺口，先补 next-token prediction 和基础 Transformer 数据流。阶段 5 的 MLA 需先理解 attention 与 KV cache；MoE 需先理解 dense FFN。阶段 4 各后训练方法分别学习，不假设所有模型分支遵循同一流水线。

实验可先采用配置阅读、手工算例或伪代码；有合适设备时再加载 Pythia 小模型。实验报告保留模型版本、checkpoint、输入、参数、资源与失败记录，不用一次输出推断整体能力。

## 进度记录规范

本文件维护课程路线与唯一续学 checkpoint；实际教学事件保存在 [AI Session Log](../session-log.md)，评估证据保存在 [AI Mastery](../mastery.md)。通过知识点 ID 和记录链接关联，不在本目录另建 mastery 或 session log。

沿用阶段状态：

| 状态 | 所需证据 |
|---|---|
| Planned | 已列入计划，尚未开展该点学习 |
| Introduced | 已实际讲解或讨论；尚无有效应用证据 |
| Practiced | 已尝试练习，记录独立完成部分、提示与缺口 |
| Demonstrated | 在适当的新题或任务中独立展示理解与应用 |
| Retention checked | 在之后的复习中再次独立应用，记录日期和证据 |

状态按具体知识点记录，不把一个小点的表现推广到整个模型或阶段。创建计划、收录资料和表示理解都不能支持掌握度提升。

有意义的讲解或答疑后，写入 session log 并更新 checkpoint；评估后才据证据更新 mastery，注明独立或提示后完成。checkpoint 引用权威记录，记录下一步与待回顾问题；仅在写入成功后报告已保存。

技术解释中自然融入有帮助的英语表达。若值得长期复习，先按 English inbox 现有指引去重后添加，不为本计划新建词表。

## 当前 checkpoint

- **状态：** Planned。
- **当前知识点：** `om.artifacts`（待开始）。
- **来源：** P2 的模型配置与 checkpoint 加载说明。
- **实际学习／作答证据：** 尚无本计划下的记录；此前讨论资料选择和归档不构成掌握证据。
- **先修情况：** 待在学习中确认，未评估不等于不会。
- **剩余疑问／待回顾问题：** 尚未收集。
- **下一步：** 先讲解“下载一个模型时，权重、配置、tokenizer 与 checkpoint 分别是什么”，用 Pythia 作为具体例子；围绕本点答疑。
- **测试：** 尚未请求；等待学习者明确触发。
- **English inbox：** 本次仅建立计划，无新增表达。
- **证据链接：** 尚无；后续链接 AI session log 与 mastery 中对应记录。

## 续学指令

> AI模式，按 Job/AI/Open-Models/Learning-Plan.md 继续学习。先读 checkpoint 和 AI 学习记录，每次只讲一个知识点，等我要求后再测试；等我说进入下一个再推进。
