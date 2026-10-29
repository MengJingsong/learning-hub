# AI Infrastructure 岗位定位与学习方向

更新日期：2026-10-28。本文记录当前目标假设，供后续选择学习主题；它不是对已掌握能力或岗位级别的评估。

## 当前定位

用户目前主要研究分布式系统，已有一些 AI 基础。研究更偏资源分配：研究分布式系统配置（configuration）和 throttling 如何改变系统资源使用，并分析可能影响资源消耗的隐藏因素。

**目标定位：AI 计算基础设施方向的系统工程师（AI/ML Infrastructure 或 ML Systems），重点在资源效率、配置分析、容量规划、调度与系统性能。**

工作核心仍是分布式系统与性能工程；AI 是重要的工作负载背景。不同团队对模型、GPU 和训练/推理细节的要求差异很大，因此以具体职位描述为准。

## 优先关注的岗位类型

1. **Capacity / Compute Efficiency Engineering**：资源分配、容量规划、利用率监测、成本归因、配置基线。
2. **Systems Performance / Performance Engineering**：通过测量和实验解释配置、throttling、工作负载对吞吐、延迟和资源消耗的影响。
3. **Resource Management / Cluster Scheduling / Control Plane**：调度、配额、限流、排队、任务放置与集群资源管理。
4. **ML Infrastructure / ML Systems**：为训练、推理和评估任务建设可扩展的底层平台。
5. **Inference Systems Performance**：请求调度、负载均衡、扩缩容、缓存、服务吞吐与尾延迟；若进一步深入，可补充加速器性能。

职位标题可能是 Software Engineer、Systems Engineer、Performance Engineer、Capacity Engineer 或 ML Infrastructure Engineer，不一定包含 “Machine Learning Engineer”。

## 研究经验如何迁移

| 已有研究经验 | AI 基础设施中的对应问题 |
|---|---|
| 比较系统 configurations | 比较训练/推理任务的运行参数、资源请求和服务配置 |
| 研究 throttling | 研究速率限制、配额、并发度和排队策略对效率与 SLO 的影响 |
| 寻找影响资源使用的 hidden factors | 用遥测、追踪和受控实验定位利用率、吞吐或延迟差异的来源 |
| 分析资源分配 | 研究加速器/CPU/内存/网络资源分配、调度、碎片和公平性 |

迁移时要把“观察到关联”与“配置导致变化”区分开：定义可重复的负载与指标，控制关键变量，报告不确定性，并用 profiling/telemetry 验证机制。

## 建议的学习路线

### 第一阶段：把系统研究转成可验证的性能分析

- 复习分布式系统、操作系统、队列/调度、并发与资源隔离。
- 练习实验设计：固定工作负载，改变一个配置因素，记录吞吐、延迟（含 p95/p99）、利用率、错误率和资源成本。
- 学习 tracing、metrics、profiling、基准测试和可复现实验；注意 warmup、重复次数、置信区间与混杂因素。
- 把一个已有研究案例整理成工程报告：问题、假设、实验设计、结果、机制解释、trade-offs。

### 第二阶段：补齐 AI workload 与平台基础

- 理解训练与推理各自的计算/内存/网络特征；掌握 GPU/加速器、显存、批处理及多 GPU 通信的基础概念。
- 了解 Kubernetes 或同类集群平台中的 resource requests/limits、配额、调度、优先级和监控。
- 实践可复现的性能实验；从一个系统瓶颈开始，不必一开始就钻研自定义 GPU kernels。

### 第三阶段：按目标岗位分支深入

- **容量/调度**：容量预测、placement、队列、碎片、利用率、公平性和成本归因。
- **训练系统性能**：多 GPU/多节点通信、数据加载、检查点、扩展效率和故障恢复。
- **推理服务性能**：并发、batching、请求路由、缓存、autoscaling、TTFT/TPOT 与尾延迟。
- **低层 GPU 性能**：仅在目标职位要求时深入 CUDA/Triton、内存带宽、kernel profiling 与编译器。

## 当前三本书的用途

- **Distributed Systems — van Steen & Tanenbaum**：分布式系统机制、资源与协调等基础；按研究短板选读。
- **Designing Data-Intensive Applications — Kleppmann**：数据系统、存储、复制与分区；适合补 AI 平台的数据面基础。
- **AI Engineering — Chip Huyen**：第 2 章理解基础模型，第 9 章了解推理优化，第 10 章理解应用架构与反馈。它是 AI 应用工程补充，不能替代 ML systems、GPU 和集群性能方面的专项材料。

具体在线课程、官方文档和动手实验见 [AI Infrastructure 学习资料索引](ai-infrastructure-resources.md)。

## 后续调整依据

投递前结合真实职位描述调整路线。若岗位反复要求 CUDA/kernel 或 GPU cluster networking，再加深低层性能；若岗位强调 capacity planning、Kubernetes、telemetry、cost/utilization，则先深化资源管理与观测。岗位名称和要求会变化，以上方向不等于某公司当前对候选人的统一要求。

待补充的信息：研究中的具体系统、配置变量、实验指标和实现语言。拿到这些信息后，可把路线改成有先修关系的周计划和作品集项目。
