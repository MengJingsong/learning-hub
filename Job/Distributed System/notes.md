# Distributed Systems — Review Notes / 分布式系统复习笔记

本文件用于快速复习：只保留每个知识点最值得记住的定义、结论、边界和易混点。完整讲解过程与每次学习记录见 [Session Log](session-log.md)；评估结果见 [Mastery](mastery.md)。

This file is for focused review. It keeps only the most important definitions, conclusions, limitations, and commonly confused points for each topic. See the [Session Log](session-log.md) for lesson history and [Mastery](mastery.md) for assessment evidence.

## 使用规则 / How to Use These Notes

- 每次完成一个知识点的讲解后，追加一节；答疑只有在形成值得长期保留的新结论时才更新。
  Add a section after each completed topic. Update it after Q&A only when a durable new takeaway emerges.
- 每个核心知识点采用中英双语：先用中文准确表达，再给出自然、简洁的英文对应表述；保留教材中的英文术语。
  Present each key point in both Chinese and English: state it accurately in Chinese, followed by a concise, natural English equivalent. Preserve the textbook's English terminology.
- 以教材原意为准，保留教材术语；标明教材出处。
  Follow the textbook's meaning and terminology, and identify the source section or page.
- 区分 **教材结论**、**自拟案例/解释** 和 **外部资料补充**，不把例子误写成教材原话。
  Distinguish **textbook conclusions**, **Learning Hub examples/explanations**, and **external additions**. Never present an example as a claim made by the textbook.
- 优先写“结论 + 为什么 + 适用边界”，避免复制整段讲解。
  Prefer “takeaway + why + limitation” over reproducing the full lesson.
- 每个知识点控制在约 5–10 条核心 bullet；必要时加一张小表或一段简短流程。
  Aim for about 5–10 key bullets per topic. Add a small table or short process only when it improves understanding.
- 不在这里记录学习日期、课堂过程、掌握度或评估成绩：日期和过程在 Session Log，评估证据在 Mastery。
  Do not record lesson dates, classroom process, mastery levels, or assessment scores here. Keep lesson history in Session Log and assessment evidence in Mastery.
- 复习时先尝试用自己的话解释每条结论；需要正式测试时再按学习计划的测试规则进行。
  During review, first explain each takeaway in your own words. Follow the learning plan's assessment rules for formal testing.

---

## 模块 1：基础与设计目标 / Module 1: Foundations and Design Goals

### 分布透明性的程度与代价 / Degree and Cost of Distribution Transparency

- **教材出处 / Textbook source**：DS §1.2.2, “Degree of distribution transparency” (printed pp. 14–15); Note 1.2, “Against distribution transparency” (printed p. 15).
- **核心结论 / Main takeaway**：透明性（transparency）是设计目标，不是越高越好的绝对指标；完全的分布透明性既无法实现，也未必值得追求。
  Transparency is a design goal, not an absolute measure to maximize. Full distribution transparency is neither achievable nor necessarily desirable.
- **位置与上下文 / Location and context**：隐藏位置可能同时隐藏应用真正需要的上下文，例如用户所在时区或当前位置。
  Hiding location may also hide context an application genuinely needs, such as a user's time zone or current location.
- **延迟与物理限制 / Latency and physical limits**：透明接口不能消除远程通信的传播延迟、处理延迟和实际网络开销；本地调用与远程调用的性能不可能因此变得完全相同。
  A transparent interface cannot eliminate propagation delay, processing delay, or network overhead. It cannot make a remote call perform exactly like a local call.
- **故障屏蔽的代价 / Cost of failure masking**：自动重试和恢复可以减少故障暴露，但也可能延长等待时间；用户有时需要取消仍在进行的请求。
  Automatic retries and recovery can hide failures, but may also increase response time. Users may need the option to cancel a request that is still in progress.
- **复制与一致性的代价 / Cost of replication and consistency**：若采用等待所有副本同步完成后才继续的严格方案，跨地域更新会承担显著通信延迟。此例说明同步保证的成本，不代表所有系统都必须等待所有副本。
  A strict strategy that waits for all replicas to synchronize before proceeding can impose substantial communication latency on cross-region updates. This illustrates the cost of synchronization; it does not mean every system must wait for every replica.
- **显式分布信息可能有价值 / When explicit distribution information helps**：位置服务等应用本来就需要位置；隐藏分布信息反而可能妨碍功能。
  Applications such as location services inherently need location information. Hiding distribution-related information may therefore get in the way of the application's function.
- **RPC 的语义边界 / Semantic limits of RPC**：远程调用不能完全等同于本地调用。请求丢失、响应丢失、服务器故障和不确定延迟会使调用结果难以判断；假装网络不存在会造成难以理解的语义。
  A remote call cannot be made fully equivalent to a local call. Lost requests or responses, server failures, and unpredictable delays make outcomes uncertain. Pretending the network does not exist can create poorly understood semantics.
- **先复制再使用原则 / Copy-before-use principle**：Note 1.2 提及的观点，主张先复制数据到本地再使用，并通过新版本表达修改；它减少对远程实时访问的依赖，但引入版本、更新传播和并发修改等问题。
  The principle discussed in Note 1.2 advocates copying data locally before using it and expressing modifications through new versions. It reduces dependence on real-time remote access, but introduces issues involving versions, update propagation, and concurrent changes.
- **设计原则 / Design principle**：在透明性、性能、可靠性和可理解性之间权衡；明确哪些分布细节应该隐藏，哪些应该暴露。
  Balance transparency against performance, reliability, and understandability. Decide deliberately which distribution details to hide and which to expose.

#### 易记的英文表达 / Useful English Expressions

| English | 中文 |
|---|---|
| degree of distribution transparency | 分布透明性的程度 |
| propagation delay | 传播延迟 |
| processing delay | 处理延迟 |
| make distribution explicit | 显式呈现分布信息 |
| poorly understood semantics | 难以正确理解的语义 |
| copy-before-use principle | 先复制再使用原则 |
| trade-off between A and B | A 与 B 之间的权衡 |

#### Hadoop / Cassandra 对照 / Hadoop and Cassandra Comparison

**Learning Hub 自拟案例，不是 DS 原文案例。 / Learning Hub examples; not examples from the DS textbook.**

- **HDFS**：文件 API 隐藏部分块位置和副本管理细节，但不会消除网络延迟、节点故障或恢复成本。
  **HDFS**: Its file API hides some block-location and replica-management details, but it does not eliminate network latency, node failures, or recovery costs.
- **Cassandra**：隐藏部分副本通信细节，同时通过 consistency level 等接口把部分一致性取舍暴露给应用。
  **Cassandra**: It hides some replica-communication details while exposing some consistency trade-offs to applications through interfaces such as consistency levels.

#### 复习时应能解释 / Review Questions

1. 为什么更高的分布透明性不一定更好？ / Why is greater distribution transparency not always better?
2. 为什么统一 API 无法让远程调用拥有本地调用的延迟与故障语义？ / Why can't a uniform API give remote calls the same latency and failure semantics as local calls?
3. 故障屏蔽为什么可能增加响应时间？ / Why can failure masking increase response time?
4. 为什么严格同步所有副本会增加跨地域更新延迟？ / Why can strict synchronization of all replicas increase cross-region update latency?
5. 为什么某些应用应该主动知道位置或其他分布信息？ / Why should some applications explicitly know location or other distribution information?
6. RPC 为什么不能真正把远程调用变成普通本地调用？ / Why can't RPC truly turn a remote call into an ordinary local call?

---

*后续知识点按本节格式追加；不要把讲解记录或未经评估的内容标记为“已掌握”。*
*Append future topics using this format. Do not label a topic as “mastered” merely because it has been discussed or noted.*
