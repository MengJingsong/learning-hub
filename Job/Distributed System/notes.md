# Distributed Systems — Review Notes / 分布式系统核心笔记

## 模块 1：基础与设计目标 / Module 1: Foundations and Design Goals

### 分布透明性的程度 / Degree of Distribution Transparency

**教材 / Source:** DS §1.2.2, pp. 14–15; Note 1.2, p. 15.

- **透明性不是越高越好。** 完全的分布透明性既无法实现，也未必符合应用需求。  
  **Transparency is not always better at a higher degree.** Full distribution transparency is neither achievable nor always desirable.
- **透明性不能消除物理成本。** 远程调用仍然存在传播延迟、处理延迟和网络开销。  
  **Transparency cannot remove physical costs.** Remote calls still incur propagation delay, processing delay, and network overhead.
- **隐藏故障可能带来额外等待。** 自动重试和恢复可以屏蔽部分故障，但也可能增加响应时间。  
  **Hiding failures can add waiting time.** Retries and recovery may mask failures, but can also increase response time.
- **强同步有性能代价。** 等待副本同步完成可能增加跨地域更新延迟。  
  **Strong synchronization has a performance cost.** Waiting for replicas to synchronize can increase cross-region update latency.
- **有些应用需要显式分布信息。** 例如位置服务需要知道用户位置，过度隐藏信息反而妨碍功能。  
  **Some applications need explicit distribution information.** Location-based services need user location; hiding it can hinder functionality.
- **RPC 无法让远程调用真正等同于本地调用。** 请求或响应丢失、服务器故障和不确定延迟都会影响调用语义。  
  **RPC cannot make remote calls truly equivalent to local calls.** Lost requests or responses, server failures, and unpredictable delays affect call semantics.
- **设计应权衡透明性与性能、可靠性及可理解性。** 决定哪些分布细节应隐藏，哪些应暴露。  
  **Design should balance transparency with performance, reliability, and understandability.** Decide which distribution details to hide and which to expose.

**补充概念 / Additional concept — Copy-before-use principle:** 先复制到本地再使用可减少远程实时访问，但会引入版本管理、更新传播和并发修改问题。  
Copying data locally before use reduces dependence on real-time remote access, but introduces versioning, update propagation, and concurrent-modification concerns.

**术语 / Key terms:** propagation delay（传播延迟）；processing delay（处理延迟）；distribution transparency（分布透明性）；copy-before-use principle（先复制再使用原则）。

**复习问题 / Check:** 为什么分布透明性不可能完全实现，也不一定值得最大化？ / Why is full distribution transparency impossible and not always worth maximizing?
