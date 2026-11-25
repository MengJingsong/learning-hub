# Distributed System Session Log

按 [分布式系统学习计划](Distributed-Systems-Learning-Plan.md) 记录每次讲解。评估证据记入 [Mastery](mastery.md)。

## 当前 checkpoint

- **状态**：模块 1 进行中；已讲解 `ds.intro.distributed-vs-decentralized`、`ds.intro.why-distinction-matters`、`ds.intro.eight-perspectives`、`ds.intro.resource-sharing`、`ds.intro.distribution-transparency`（基本含义与中间件）、`ds.intro.access-transparency`、`ds.intro.location-transparency`、`ds.intro.relocation-transparency`、`ds.intro.replication-transparency`、`ds.intro.concurrency-transparency`、`ds.intro.failure-transparency`、`ds.intro.degree-of-transparency`、`ds.intro.openness`；已对照引入 `ds.intro.migration-transparency`。
- **下一步**：DS §1.2.4 Dependability（可依赖性）；或继续答疑本课。
- **图表**：2026-11-24 已验证上传的两本原 PDF 可直接读取、渲染和裁剪；优先提取原图，见计划第 4 节。
- **背景**：2026-11-17 至 2026-11-20 按旧计划讲过 DS §1.1–§1.3，记录在 [归档](session-log-archive-2026-11.md)。这些讲解没有评估证据，不计入本计划进度。

## 记录格式

每次讲解一条，最新的放在最上面：

```text
## YYYY-MM-DD — 模块：知识点标题

- 知识点 ID：
- 教材出处：
- 阶段：讲解 / 答疑 / 复习 / 测试
- 本次范围：
- 核心要点：
- 案例（Hadoop / Cassandra）：
- 图表：原图 / 重画 / 无
- 英语融入与 inbox 新增：
- 能力证据：
- 剩余疑问：
- 下一步：
```

## 记录

## 2026-11-25 — 模块 1：开放性（Openness）

- 知识点 ID：`ds.intro.openness`
- 教材出处：DS §1.2.3（印刷页 15–17；PDF 第 31–33 页）。
- 阶段：讲解
- 本次范围：开放分布式系统的定义；IDL 与接口语法/语义；规范的完整性与中立性；互操作性、可移植性、可扩展性；策略与机制分离及其配置复杂度。
- 核心要点：开放性要求组件易于使用、集成、添加和替换；互操作性强调不同实现协作，可移植性强调应用跨兼容系统运行；接口规范必须尽可能明确语义且完整、中立；策略与机制分离提高灵活性但会扩大配置空间。
- 案例（Hadoop / Cassandra，learning-hub 自拟）：以 Hadoop 组件接口协作和 Cassandra 客户端协议说明接口兼容是开放性的基础，但不自动保证跨实现或跨版本的无修改兼容。
- 图表：无（本节无依赖讲解的教材图表）。
- 英语融入与 inbox 新增：interoperability、portability、extensibility、semantics、complete、neutral、separate policy from mechanism；查重后新增值得长期复习的条目。
- 能力证据：无（仅讲解；未评估；Mastery 不变）。
- 剩余疑问：待学习者反馈。
- 下一步：DS §1.2.4 Dependability（可依赖性），或继续本课答疑。

## 2026-11-24 — 模块 1：分布透明性的程度与代价

- 知识点 ID：`ds.intro.degree-of-transparency`
- 教材出处：DS §1.2.2「Degree of distribution transparency」（印刷页 14–15；PDF 第 30–31 页）；Note 1.2「Against distribution transparency」（印刷页 15）。DDIA Ch.8「Unreliable Networks」仅作相关背景，不作为本课直接出处。
- 阶段：讲解
- 本次范围：时区与上下文；物理传播延迟；故障屏蔽与重试成本；跨地域副本同步的更新延迟；位置服务主动暴露分布信息；完全透明的局限；Waldo et al. 对 RPC 语义的批评；copy-before-use principle。
- 核心要点：透明性程度越高不一定越好；隐藏位置、延迟、故障和副本传播可能掩盖应用需要的信息或增加响应时间；完全透明既不可能，也未必值得追求；设计需同时考虑性能与可理解性。
- 案例（Hadoop / Cassandra，learning-hub 自拟）：HDFS 文件 API 隐藏部分块位置与副本管理细节，但不能消除网络和故障成本；Cassandra 隐藏部分副本通信，同时有意向应用暴露 consistency level 等选择。
- 图表：无（本节主要是正文中的五个论证例子，没有依赖特定图表的讲解）。
- 英语融入与 inbox 新增：propagation delay、processing delay、make distribution explicit、poorly understood semantics、copy-before-use principle；inbox 查重后新增。
- 能力证据：无（仅讲解；未测试；Mastery 不变）。
- 剩余疑问：待学习者反馈。
- 下一步：DS §1.2.3 Openness（开放性），或继续本课答疑。

