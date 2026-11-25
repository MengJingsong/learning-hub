# Distributed System Session Log

按 [分布式系统学习计划](Distributed-Systems-Learning-Plan.md) 记录每次讲解。评估证据记入 [Mastery](mastery.md)。

## 当前 checkpoint

- **状态**：模块 1 进行中；已讲解 `ds.intro.distributed-vs-decentralized`、`ds.intro.why-distinction-matters`、`ds.intro.eight-perspectives`、`ds.intro.resource-sharing`、`ds.intro.distribution-transparency`（基本含义与中间件）、`ds.intro.access-transparency`、`ds.intro.location-transparency`、`ds.intro.relocation-transparency`、`ds.intro.replication-transparency`、`ds.intro.concurrency-transparency`、`ds.intro.failure-transparency`、`ds.intro.degree-of-transparency`；已对照引入 `ds.intro.migration-transparency`。
- **下一步**：模块 1 后续知识点：DS §1.2.3 Openness（开放性）；或继续答疑本课。
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

## 2026-11-24 — 模块 1：故障透明性与超时的不确定性

- 知识点 ID：ds.intro.failure-transparency
- 教材出处：DS §1.2.2 pp.13–14；DDIA Ch.8「Unreliable Networks」pp.278–279、Figure 8-1；「Timeouts and Unbounded Delays」p.281。
- 阶段：讲解
- 本次范围：自动屏蔽故障与恢复；无法仅凭无响应区分崩溃、延迟、请求/响应丢失；超时不等于未执行；重试与幂等性；超时长短的取舍。
- 核心要点：客户端超时只表示期限内没有收到响应，不撤销远端操作；自动重试须考虑重复副作用；透明性是有故障模型与保证边界的目标。
- 案例（Hadoop / Cassandra）：HDFS 校验失败后读取另一副本；Cassandra Java driver 根据请求幂等性约束重试。依据 Apache 官方文档；另用自拟扣款例子说明响应丢失后重复执行。
- 图表：原图 DDIA Figure 8-1（印刷页 278 / PDF 300），直接从项目 PDF 裁剪并核验；未提交教材图到 GitHub。
- 英语融入与 inbox 新增：failure transparency、indistinguishable、unresponsive、idempotent、deduplication、side effect；结合正文解释 congested、transient、timeout。
- 能力证据：无（仅讲解；未评估）
- 剩余疑问：待学习者反馈
- 下一步：ds.intro.degree-of-transparency（DS §1.2.2：透明性的程度与代价）

## 2026-11-24 — 模块 1：并发透明性；验证两本原 PDF 截图

- 知识点 ID：ds.intro.concurrency-transparency
- 教材出处：DS §1.2.2 p.13；DDIA Ch.7「Isolation」pp.225–226、Figure 7-1，以及「Single-object writes」p.230
- 阶段：讲解
- 本次范围：并发与并行、交错执行、计数器丢失更新、整个读改写操作的保护、锁/原子递增/事务隔离边界。
- 核心要点：各个读写成功不保证复合操作正确；事务不自动等于可串行化；透明性不保证没有等待。
- 案例（Hadoop / Cassandra）：HDFS 同一文件单写者；Cassandra CAS/LWT 需显式使用，普通读后写不自动受保护。依据 Apache 官方资料。
- 图表：原图 DS Figure 1.3（印刷页 12 / PDF 28）、DDIA Figure 7-1（印刷页 226 / PDF 248），从本次上传原 PDF 渲染裁剪并检查；未提交教材图到 GitHub。
- 英语融入与 inbox 新增：concurrency transparency、interleaving、race condition、lost update、exclusive access、serializability；正文增加 increment、overwrite、isolation 等中英对照。
- 能力证据：无（仅讲解；未评估）
- 剩余疑问：待学习者反馈
- 下一步：ds.intro.failure-transparency（DS §1.2.2：故障透明性）
- 教材访问：已实际打开 DS 685 页、DDIA 613 页，文字提取与截图成功。同步更新学习计划来源、图表状态和生词对照规则。

## 2026-11-24 — 模块 1：复制透明性；本地 PDF 访问复核

- 知识点 ID：`ds.intro.replication-transparency`
- 教材出处：DS §1.2.2（印刷页 13）；已读取上传教材对应页
- 阶段：讲解
- 本次范围：一个逻辑资源与多个物理副本 → 复制动机 → 公共名称与位置透明性 → 更新传播及陈旧读取边界 → HDFS/Cassandra 对照
- 核心要点：应用通过共同逻辑名称访问，系统管理副本；隐藏副本选择不自动保证最新读取或任意故障下可用；副本内部可有独立地址与身份。
- 案例（Hadoop / Cassandra，learning-hub 自拟）：HDFS 块副本与统一文件路径；Cassandra 统一键与显式一致性级别；自拟 x 从 10 更新为 11 时副本传播滞后表。
- 图表：无教材原图；自拟副本状态表。实测 G:\My Drive\books\Distributed Systems -- Maarten van Steen & Andrew Tanenbaum.pdf 返回拒绝访问，未能从本地 PDF 截图，不能据此判定文件不存在。
- 英语融入与 inbox 新增：replication transparency、replica、stale read；教材 all replicas have the same name 的含义。
- 能力证据：无（仅讲解；未评估）
- 剩余疑问：本地教材访问仍受限
- 下一步：`ds.intro.concurrency-transparency`（DS §1.2.2：并发透明性），或继续复制透明性答疑。

## 2026-11-24 — 模块 1：重定位透明性与 migration 的区别

- 知识点 ID：`ds.intro.relocation-transparency`；对照引入 `ds.intro.migration-transparency`
- 教材出处：DS §1.2.2（印刷页 12–13，Figure 1.3 定义及其后正文）
- 阶段：讲解
- 本次范围：使用中的资源移动 → 只改名称映射的不足 → 不可变文件读取的自拟切换流程 → 状态与在途请求 → 与 migration 的教材术语区别 → 实现成本
- 核心要点：名称稳定不足以保证现有操作连续；系统需要处理已有连接、读取位置与在途请求。图表强调 relocation 的 while in use；v4.02 正文另以系统发起 relocation 与用户发起 mobility 区分，不应简化为 migration 只能离线。
- 案例（Hadoop / Cassandra，learning-hub 自拟）：HDFS Balancer 的块移动、Cassandra 拓扑变化中的 streaming；说明这些是移动场景，不据此承诺任意操作零中断。自拟只读不可变文件先复制、验证、切换新请求并排空旧请求的方案。
- 图表：无教材图；自拟阶段表及术语对照表。
- 英语融入与 inbox 新增：relocation transparency、migration transparency、in-flight request；教材 while in use 省略结构解析。
- 能力证据：无（仅讲解；未评估）
- 剩余疑问：待学习者反馈
- 下一步：`ds.intro.replication-transparency`（DS §1.2.2：复制透明性），或继续重定位与迁移答疑。

## 2026-11-24 — 模块 1：位置透明性

- 知识点 ID：`ds.intro.location-transparency`
- 教材出处：DS §1.2.2 位置透明性段落（印刷页 12）；本课未引用 DDIA
- 阶段：讲解
- 本次范围：逻辑名称与物理位置分离 → 命名与解析 → 自拟文件名到节点映射 → HDFS 与 Cassandra 对照 → 与访问/重定位透明性的边界及映射维护成本
- 核心要点：应用按逻辑名称指定资源，底层解析或路由到实际位置；名字不能只是把物理位置换成易读形式；透明性针对特定观察层，不表示安全保密或延迟相同；位置隐藏不自动保证移动期间操作不中断。
- 案例（Hadoop / Cassandra，learning-hub 自拟）：HDFS 文件路径/块/DataNode 映射；Cassandra partition key/token/副本节点映射；逻辑名称 /datasets/run-17 与 node-7 本地路径对照。产品依据此前读取的 Apache 官方架构文档。
- 图表：无教材图；自拟名称/位置对照表，本课不展开 Figure 1.3 全表。
- 英语融入与 inbox 新增：location transparency、logical name、name resolution；教材短句 Naming plays an important role in achieving location transparency。
- 能力证据：无（仅讲解；未评估）
- 剩余疑问：待学习者反馈
- 下一步：`ds.intro.relocation-transparency`（DS §1.2.2：重定位透明性），并按教材区分 migration transparency。

## 2026-11-24 — 模块 1：访问透明性

- 知识点 ID：`ds.intro.access-transparency`
- 教材出处：DS §1.2.2，访问透明性段落（印刷页 11–12）；本课未引用 DDIA
- 阶段：讲解
- 本次范围：数据表示与访问机制两类差异 → 整数端序及规范化编码的分步案例 → 统一接口与适配 → Hadoop FileSystem、Cassandra native protocol → 与位置透明性及语义边界的区别
- 核心要点：访问透明性隐藏表示和访问机制差异；双方仍须遵守协议；字节传递成功不等于正确解释数据；访问透明性不保证位置、性能或故障透明性。
- 案例（Hadoop / Cassandra，learning-hub 自拟）：Hadoop FileSystem 的公共访问抽象；Cassandra native protocol 的数据序列化约定；自拟 32 位整数 1 的大小端表示和编码/解码流程。产品事实参考 Apache 官方资料。
- 图表：无教材图；使用自拟数据表示表和 access/location 对照表，本课不展开 Figure 1.3 全表。
- 英语融入与 inbox 新增：access transparency、data representation、byte order；原句拆解 deals with hiding ... and the way that ...。
- 能力证据：无（仅讲解；Mastery 保持未评估）
- 剩余疑问：待学习者反馈
- 下一步：`ds.intro.location-transparency`（DS §1.2.2：位置透明性），或继续本课答疑。

## 2026-11-23 — 模块 1：分布透明性的基本含义与中间件

- 知识点 ID：`ds.intro.distribution-transparency`
- 教材出处：DS §1.2.2 开头及 Figure 1.2（印刷页 11）；边界预告参考同节 pp.14–15
- 阶段：讲解
- 本次范围：transparent to 的技术含义 → 应用视角与实现视角 → 中间件提供统一接口 → HDFS 分步读取案例与 Cassandra 对照 → 统一接口不等于相同延迟和故障语义
- 核心要点：透明性隐藏选定的分布细节；中间件承接复杂度而非消除复杂度；须说明对谁透明、隐藏什么；完全透明并非总能或值得实现。
- 案例（Hadoop / Cassandra，learning-hub 自拟）：HDFS 应用按文件路径读取，由客户端与 NameNode/DataNode 协作完成；Cassandra 隐藏部分副本通信细节但显式提供一致性级别。参考 Apache 官方资料。
- 图表：重画，依据 DS Figure 1.2 的正文及图注，简化为跨两台机器的中间件层；原 PDF 的 G 盘路径本次无读取权限。
- 英语融入与 inbox 新增：distribution transparency、transparent to、middleware；拆解 what applications get to see is the same interface everywhere。
- 能力证据：无（仅讲解；未测试）
- 剩余疑问：待学习者反馈
- 下一步：`ds.intro.access-transparency`（DS §1.2.2：访问透明性）；其余透明性类型和程度尚未逐项讲解。

## 2026-11-22 — 模块 1：资源共享

- 知识点 ID：`ds.intro.resource-sharing`
- 教材出处：DS §1.2.1（第 4 版 v4.02，印刷页 10–11）；DDIA 本课未引用
- 阶段：讲解
- 本次范围：远程资源的含义 → 经济性与协作动机 → 共享数据与有限容量的区别 → Hadoop/Cassandra 自拟案例 → 竞争、排队与资源限制 → 与分布透明性的边界
- 核心要点：共享让多个用户或应用访问远程资源；共享不要求单一物理副本，也不等于分布式共享内存；容量仍有限，提高利用率需要权衡竞争、网络和管理成本。
- 案例（Hadoop / Cassandra，learning-hub 自拟）：HDFS 共享数据集与 YARN 分配计算资源；Cassandra 多应用共享数据库服务但竞争节点内存、I/O 与处理能力。基础架构对照 Apache 官方资料，不涉及配置默认值。
- 图表：无（本节无教材图；用自拟表格对照资源类型与案例）
- 英语融入与 inbox 新增：share remote resources、resource contention、make it easy for ... to ...；原句拆解资源共享目标中的形式宾语 it。
- 能力证据：无（仅讲解；Mastery 保持未评估）
- 剩余疑问：待学习者反馈
- 下一步：`ds.intro.distribution-transparency`（DS §1.2.2），或继续本课答疑

## 2026-11-22 — 模块 1：八个研究视角

- 知识点 ID：`ds.intro.eight-perspectives`
- 教材出处：DS §1.1.3；DDIA 无直接对应
- 阶段：讲解
- 本次范围：为什么要按视角研究（显式与隐式依赖交织，没有独立的通信或安全模块）→ 八个视角：架构、进程、通信、协调、命名、一致性与复制、容错、安全 → 与本计划模块的对应
- 核心要点：视角是观察同一系统的不同切面，不是可拆开的组件；复制是效率与可依赖性的共同手段，更新使“看起来像单机”变难；完全掩盖故障及其恢复可证明不可能
- 案例（Hadoop / Cassandra，learning-hub 自拟）：用八个视角各问一个问题，对照 HDFS/YARN 与 Cassandra
- 图表：无（本节无图）
- 英语融入与 inbox 新增：get a first grip on、be they A, B, or C、keep up the appearance of、at stake；长难句（容错视角“It has proven to be one of the toughest…”）、省略句（“a limited number, yet different perspectives”）
- 能力证据：无（仅讲解）
- 剩余疑问：无
- 下一步：DS §1.2.1

## 2026-11-22 — 模块 1：为什么要区分分布式与去中心化

- 知识点 ID：`ds.intro.why-distinction-matters`
- 教材出处：DS §1.1.2；DDIA 无直接对应
- 阶段：讲解
- 本次范围：集中式更简单 → 分布式/去中心化的四个固有难点（意外依赖、部分失效、动态成员、安全）→ 作者立场：去中心化本身不是目标，分散“越少越好”、够用即可 → 偏好简单方案、少谈优化
- 核心要点：sufficiency vs necessity 是设计取舍的出发点；每多一份分散就多一份部分失效与协调成本；复杂度的代价常常超过优化的性能收益
- 案例（Hadoop / Cassandra，learning-hub 自拟）：HDFS 把元数据集中到 NameNode，换取简单一致的命名空间，再用 HA 加固单点；Cassandra 无主，消除单点但把复杂度推到 gossip、故障检测、hinted handoff、read repair、一致性级别选择上
- 图表：无（本节无图）；已确认可从本地 PDF 截原图
- 英语融入与 inbox 新增：inherently difficult、mask a failure、come and go、a goal in itself、outweigh、the less ..., the better；长难句（“firmly believing that the impact of their negative contribution…”）、省略句（“In principle, the less spreading, the better.”）
- 能力证据：无（仅讲解）
- 剩余疑问：无
- 下一步：DS §1.1.3

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
