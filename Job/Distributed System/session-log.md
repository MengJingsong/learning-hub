# Distributed System Session Log

按 [分布式系统学习计划](Distributed-Systems-Learning-Plan.md) 记录每次讲解。评估证据记入 [Mastery](mastery.md)。

## 当前 checkpoint

- **状态**：模块 1 已开始；已讲解 `ds.intro.distributed-vs-decentralized`（2026-11-20）。
- **下一步**：`ds.intro.why-distinction-matters`（DS §1.1.2：为什么要区分，以及集中式方案为何更简单），或先答疑本课。
- **图表**：当前无法提取原图，默认重画；见计划第 4 节。
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

## 2026-11-20 — 模块 1：分布式与去中心化（distributed vs. decentralized）

- 知识点 ID：`ds.intro.distributed-vs-decentralized`
- 教材出处：DS §1.1.1（含 Figure 1.1、Note 1.1）；DDIA 无直接对应
- 阶段：讲解
- 本次范围：两种视角（integrative / expansive）→ 两个定义（necessarily / sufficiently spread）→ 去中心化的三类“必须”来源（管理/政策、信任、地理）→ 分布式的例子（Gmail、CDN、NAS）→ Note 1.1 逻辑集中 vs 物理集中
- 核心要点：区分标准是“分散的原因”，不是拓扑形状；去中心化是被约束逼出来的分散，分布式是为性能/可依赖性而做的“够用即可”的分散；集中式不必然不可扩展或必然有单点故障
- 案例（Hadoop / Cassandra，learning-hub 自拟）：HDFS/YARN 集群属于分布式系统，NameNode 是逻辑集中点；Cassandra 虽为对等无主结构，按本书定义仍是分布式而非去中心化；多数据中心若出于数据驻留法规则带有“必须分散”的成分
- 图表：重画（依据 DS Figure 1.1，文字示意）+ 自拟的两视角对照图
- 英语融入与 inbox 新增：necessarily/sufficiently spread、integrative/expansive view、administrative boundary、logically centralized、single point of failure、boil down to；长难句（expansive view 定义句）、省略句（“More often, however, is that…”，“yet only to where it makes sense”）
- 能力证据：无（仅讲解）
- 剩余疑问：无
- 下一步：DS §1.1.2
