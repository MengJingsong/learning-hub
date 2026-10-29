# AI Infrastructure 面试复习清单

目标方向由用户明确为 AI infrastructure。以下为建议练习范围，不是对现有能力的评估，也不是某家公司的固定题库。

知识与在线/下载资源统一维护在 [CS 资料索引](../../CS/study-materials/ai-infrastructure-resources.md)，避免重复维护。先按 JD 选择训练、推理、kernel/编译或平台分支，再决定深度。

## 通用与专项

| 主题 | 面试练习提示 | 应观察的证据 |
|---|---|---|
| 编程与系统 | 实现有界队列/并发任务处理；分析内存、锁、异常和复杂度 | 正确性、边界、可测试性；语言按岗位选 Python/C++/Go |
| 性能排查 | GPU utilization 低但任务很慢，如何定位？ | 区分数据、CPU、通信、同步、kernel；提出测量而非猜测 |
| 训练显存 | 估算一个模型的训练显存；OOM 后如何处理？ | 明确 dtype/optimizer/activation 等假设；量化策略代价 |
| 分布式训练 | DDP/FSDP/TP/PP 如何组合？扩展效率为何下降？ | 通信量、显存、拓扑、负载不均与重叠 |
| 故障恢复 | 设计长时间多节点训练的 checkpoint/restart | 模型/优化器/RNG/数据进度；一致性、保存成本与恢复 |
| 推理服务 | 设计满足 TTFT 与尾延迟目标的 LLM serving | 容量估算、KV cache、batching、排队、隔离和观测 |
| GPU kernel | 优化 softmax/GEMM，何时受内存带宽限制？ | 正确性、访存、tiling/fusion、profiling 与数值误差 |
| 平台 | 多租户 GPU 集群如何调度、配额和隔离？ | 碎片、拓扑、抢占、故障域、控制面与可观测性 |
| 项目深挖 | 描述一次性能优化或故障排查 | 真实贡献、基线、测量、失败尝试、取舍和可复现证据 |

## 模拟流程

遵循 ../instructions/preparation.md，一次一题；先让学习者澄清需求、陈述假设并作答，再追问。评价技术正确性、定量估算、调试方法、工程取舍及表达，不因英语流利而推断技术掌握。

围绕岗位只选少数主题深入；训练、推理、kernel 和平台题不要求每次全覆盖。能力证据不足时标为未知，不默认从零开始。面试表现记录在 /interview/mastery.md 与 /interview/session-log.md，概念知识引用 CS 记录，不复制两份主状态。

可用启动语：“面试模式，AI infrastructure，推理方向；先进行一次不提示答案的诊断面试。”
