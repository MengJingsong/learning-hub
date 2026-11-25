# Distributed Systems — Review Notes / 分布式系统核心笔记

## 模块 1：基础与设计目标 / Module 1: Foundations and Design Goals

### 分布透明性的程度 / Degree of Distribution Transparency

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

### 开放性 / Openness

- **开放性要求组件易于使用、集成、添加和替换。**  
  **Openness makes components easy to use, integrate, add, and replace.**
- **互操作性关注不同实现能否协作；可移植性关注应用能否不修改就迁移到另一个兼容系统。**  
  **Interoperability is about different implementations working together; portability is about running an application on another compatible system without modification.**
- **接口规范不仅要定义语法，还要尽可能明确语义；好的规范应完整且中立。**  
  **Interface specifications must address semantics as well as syntax; good specifications should be complete and neutral.**
- **分离策略与机制能提高灵活性，但过多机制和参数会增加配置复杂度。**  
  **Separating policy from mechanism improves flexibility, but too many mechanisms and parameters increase configuration complexity.**

**术语 / Key terms:** interoperability（互操作性）；portability（可移植性）；extensibility（可扩展性）；semantics（语义）；policy（策略）；mechanism（机制）。
