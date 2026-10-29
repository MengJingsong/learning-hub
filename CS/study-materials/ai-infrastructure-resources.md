# AI Infrastructure 学习资料索引

整理日期：2026-10-28（America/New_York）。目标：AI infrastructure 面试准备。链接经本次检索核对；软件文档持续变化，实践时记录框架、CUDA、驱动与硬件版本。

本文件是资源目录与建议路线，不是已学习或已掌握的记录。概念学习记录在 /CS/mastery.md 和 /CS/session-log.md；面试练习见 [AI infrastructure 面试清单](../../interview/study-materials/ai-infrastructure.md)。本轮只保存网址与索引，未下载或上传下表中的第三方全文。

## 1. 先确定岗位分支

| 分支 | 优先知识 | 可证明能力的练习 |
|---|---|---|
| 分布式训练 | DDP、FSDP/ZeRO、TP/PP、collectives、拓扑、checkpoint 与恢复 | 解释显存构成；测扩展效率；定位通信瓶颈 |
| 推理与 serving | prefill/decode、KV cache、batching、调度、量化、SLO | 压测推理服务，比较吞吐、TTFT、TPOT 与尾延迟 |
| GPU kernel / 编译与性能 | CUDA/Triton、内存层次、tiling、fusion、同步、roofline | 正确实现并测量 softmax/GEMM，解释加速来源 |
| 平台与集群 | Linux、网络、容器、Kubernetes、资源调度、隔离、可靠性 | 设计多租户 GPU 平台与故障恢复流程 |

以上为建议分流，不代表所有岗位都考察所有模块。具体深度以职位描述为准。Python、算法、并发与网络是通用基础；C++ 深度随岗位变化。保留反向传播、优化器和 Transformer 基础，不需要先学完全部传统 ML 算法再开始系统学习。

## 2. 可下载资料与保存方式

“可下载”不等于“可公开转载”。将第三方全文提交 GitHub 前，核对该版本的许可，保留作者、来源和许可；未确认再分发权限的资源保存链接与自己的笔记即可。

| 资源 | 官方入口 / 下载入口 | 重点 | 保存建议 |
|---|---|---|---|
| Dive into Deep Learning / 动手学深度学习 | [英文](https://d2l.ai/) · [中文](https://zh.d2l.ai/) · [英文 PDF](https://d2l.ai/d2l-en.pdf) · [源仓库及许可](https://github.com/d2l-ai/d2l-en) | 自动求导、优化、Transformer、计算性能、多 GPU | 文本采用 CC BY-SA 4.0；转载时保留署名与许可，代码核对对应许可。优先保存自己的代码与笔记 |
| Introduction to Machine Learning Systems | [官网](https://mlsysbook.ai/) · [Volume I](https://mlsysbook.ai/vol1/index.html) · [许可说明](https://mlsysbook.ai/about/) | 系统约束、硬件、优化与部署 | 官网提供 PDF；教材当前为 CC BY-NC-ND 4.0，教学材料另用 CC BY-NC-SA 4.0。满足条件时可保存未修改教材并附来源许可；不要混淆两种许可。Volume II 为 preview |
| OSTEP | [作者网站及分章 PDF](https://pages.cs.wisc.edu/~remzi/OSTEP/) | 虚拟内存、线程、锁、条件变量、I/O | 可从作者网站下载阅读；本索引不主张已获得 GitHub 再分发权限，建议链接与自写笔记 |
| CUDA Programming Guide | [在线](https://docs.nvidia.com/cuda/cuda-programming-guide/) · [PDF](https://docs.nvidia.com/cuda/cuda-programming-guide/pdf/cuda-programming-guide.pdf) | 执行模型、内存、streams、同步 | 可下载阅读；仓库优先保留官方链接及所用版本 |
| Stanford CS336 | [课程与作业](https://cs336.stanford.edu/) | 模型实现、性能、训练系统、数据 | 课程提供讲义/作业资源；逐项检查许可，优先链接官方文件，自己的实现放独立目录 |
| Triton tutorials | [教程及代码下载入口](https://triton-lang.org/main/getting-started/tutorials/) | vector add、softmax、GEMM、attention | 官网提供 Python/notebook 打包下载；复制代码时保留对应源码许可与来源 |
| ZeRO (2019/2020) | [论文页](https://arxiv.org/abs/1910.02054) · [PDF](https://arxiv.org/pdf/1910.02054) | optimizer state、gradient、parameter 分片 | 下载阅读；公开镜像前核对论文页许可，默认保存链接 |
| FlashAttention (2022) | [论文页](https://arxiv.org/abs/2205.14135) · [PDF](https://arxiv.org/pdf/2205.14135) | IO-aware attention、tiling、在线 softmax | 同上；重点理解机制，不背历史硬件的性能数字 |
| PagedAttention / vLLM (2023) | [论文页](https://arxiv.org/abs/2309.06180) · [PDF](https://arxiv.org/pdf/2309.06180) | KV cache、碎片与分页、共享 | 同上；论文设计与当前 vLLM 实现分开学习 |

已有仓库 PDF：DDIA 与 Distributed Systems。用于补充复制、分区、容错、存储和通信等系统原理；不是 GPU/训练/推理专项教材。下载大文件后可通过本地 Git/GitHub Desktop 提交；当前连接器 16 MiB 请求限制还包含编码与封装开销，不能按原始文件 16 MB 判断能否上传。

## 3. 在线主线：按需要选，不必全部通读

P0 = 通用基础或该分支首选；P1 = 定向深入。优先级不是掌握程度。

| ID | 优先级 | 在线资料 | 本轮建议范围 / 复习目标 |
|---|---|---|---|
| ai-foundations | P0 | [D2L](https://d2l.ai/) / [中文](https://zh.d2l.ai/) | autograd、优化器、Transformer、批处理；解释一次训练 step 的计算与内存 |
| ai-parallel | P0 | [CMU 15-418/618](https://www.cs.cmu.edu/~418/) · [课表](https://www.cs.cmu.edu/~418/schedule.html) | 并行模型、GPU、内存层次、性能；解释速度为何不随设备数线性增长 |
| ai-training | P0-训练 | [PyTorch Distributed Overview](https://docs.pytorch.org/tutorials/beginner/dist_overview.html) | DDP、FSDP2、TP、PP 的适用条件；再从该入口进入具体教程 |
| ai-communication | P0-训练 | [NCCL User Guide](https://docs.nvidia.com/deeplearning/nccl/user-guide/docs/index.html) | AllReduce、AllGather、ReduceScatter、执行顺序与故障；理解而非背 API |
| ai-serving | P0-推理 | [vLLM docs](https://docs.vllm.ai/en/latest/) | Quickstart、benchmarking、metrics、prefix cache、parallelism；结合 PagedAttention |
| ai-gpu | P0-kernel | [CUDA Programming Guide](https://docs.nvidia.com/cuda/cuda-programming-guide/) | thread/block/warp、内存访问、同步与异步执行 |
| ai-triton | P1-kernel | [Triton tutorials](https://triton-lang.org/main/getting-started/tutorials/) | 按 vector add → fused softmax → matmul 练习；比较正确性与带宽/算力瓶颈 |
| ai-profiling | P0 | [PyTorch Profiler](https://docs.pytorch.org/tutorials/recipes/recipes/profiler_recipe.html) · [Nsight Systems](https://docs.nvidia.com/nsight-systems/UserGuide/index.html) | CPU/GPU 时间线、数据等待、kernel launch、同步、通信重叠 |
| ai-llm-systems | P1 | [Stanford CS336](https://cs336.stanford.edu/) | 有训练循环和 Transformer 基础后，选系统相关讲义与作业；无需先做完全部课程 |
| ai-platform | P0-平台 | [Kubernetes GPU scheduling](https://kubernetes.io/docs/tasks/manage-gpus/scheduling-gpus/) · [Device plugins](https://kubernetes.io/docs/concepts/extend-kubernetes/compute-storage-net/device-plugins/) · [Scheduling](https://kubernetes.io/docs/concepts/scheduling-eviction/) | GPU 资源声明、设备插件、调度/抢占/驱逐；进阶研究拓扑与多租户隔离 |
| ai-systems-overview | P1 | [MLSys Book](https://mlsysbook.ai/) | 把计算、内存、网络和运维组织成统一系统视角 |
| ai-os | 按短板补 | [OSTEP](https://pages.cs.wisc.edu/~remzi/OSTEP/) | 进程线程、虚拟内存、并发、持久化 |

主线建议：D2L 必要基础 → CUDA/并行计算 + profiler → PyTorch 分布式或 vLLM → 相关论文 → 选一个专项实验。平台岗位可将 Kubernetes 与 Linux/分布式基础提前。

## 4. 复习单元与先修关系

| 概念 ID | 知识点 | 先修 | 复习时应解释的问题 |
|---|---|---|---|
| ai.memory-budget | 训练显存预算 | Tensor、dtype、autograd、optimizer | 参数、梯度、状态、activation 各占多少？为什么不能只按参数量估算？ |
| ai.roofline | 计算/带宽瓶颈 | GPU 内存层次、FLOPs | 增加算力何时无效？如何用测量验证？ |
| ai.collectives | 集合通信 | 多进程、网络 | AllReduce 与 ReduceScatter + AllGather 的关系和代价是什么？ |
| ai.sharding | DDP、ZeRO、FSDP | memory-budget、collectives | 分片省了什么、增加了哪些通信？ |
| ai.model-parallel | TP、PP | Transformer、collectives | 层内与层间划分有何代价？bubble 和拓扑如何影响选择？ |
| ai.kv-cache | prefill/decode 与 KV cache | Attention、生成循环 | 长上下文和并发如何影响容量、带宽与延迟？ |
| ai.serving-slo | batching、调度与 SLO | kv-cache、排队基础 | 吞吐提高为何可能损害 TTFT/p99？如何公平比较？ |
| ai.kernel-fusion | tiling、fusion、FlashAttention | gpu、roofline | 为什么少读写比少做几次运算更重要？ |
| ai.recovery | checkpoint 与失败恢复 | 分布式系统、存储 | 保存哪些状态才能恢复？如何权衡频率、开销与重算？ |
| ai.gpu-scheduling | 多租户 GPU 调度 | Linux、Kubernetes、网络 | 如何兼顾配额、碎片、拓扑、隔离和故障？ |

## 5. 实验建议

1. 单 GPU：用 profiler 检查训练循环，比较 batch size / precision / 数据加载；记录硬件、版本、warmup、同步、正确性和重复测量。
2. 两张以上 GPU 可用时：比较单卡与 DDP；报告相同任务口径下的吞吐与扩展效率，再研究 FSDP 的显存/通信取舍。无多卡时先做通信预算和 trace 分析，不能声称完成多卡实验。
3. 推理：用合适的小模型运行 vLLM，变化并发、输入/输出长度和 batching；记录吞吐、TTFT、TPOT、p50/p99、失败率和显存，同时固定模型质量/精度口径。
4. kernel：做 Triton softmax 或 matmul；包含不规则 shape、数值误差、warmup 和重复测量，解释何种形状会失去优势。

## 6. 以后如何复习

- 概念学习：说“CS模式，依据 AI infrastructure 索引复习 ai.sharding，先讲解，等我要求后测试”。
- 书籍复习：说“知识点复习”，沿用先选书的既有流程；本索引不改变该指令。
- 岗位面试：说“面试模式，AI infrastructure 分布式训练方向，围绕显存预算做一次模拟面试”。
- 每次选题读取所属类别的当前历史记录；不能把资源收录或勾选阅读等同于掌握。概念与面试能力分开记录。

## 来源与维护

所有外部条目链接原作者、课程或官方文档。下载全文时额外记录具体版本、下载日期、作者/机构、原始 URL、许可与 SHA-256；软件例子固定版本。遇到失效深层链接先回官方入口，不假称读过未能访问的内容。新资料优先补充薄弱主题，不无限扩充清单。
