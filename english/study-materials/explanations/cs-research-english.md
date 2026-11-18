# Computer Science and Research English Explanations

Technical phrases are explained in their common software and systems sense. Similar expressions are not always interchangeable; examples show typical use.

## Core

### workaround
**词汇补充：** /ˈwɜrkəˌraʊnd/；常搭配 *temporary/practical workaround, find a workaround for*；近义 *stopgap, temporary fix*；反义 *permanent fix*。
**English explanation:** A temporary method of solving a problem when the normal solution is unavailable or does not work.
**意思：** 临时绕过问题的做法，不一定修复根因。类似：*temporary fix; stopgap.*
1. We used a workaround until the vendor fixed the bug. — 供应商修复 bug 前，我们用了临时绕行方案。
2. This workaround avoids the crash but adds latency. — 这个临时方案避免了崩溃，但增加了延迟。

### sanity check
**意思：** 快速检查结果是否合理。类似：*quick plausibility check; spot check.*
**English explanation:** A quick, basic check to see whether an idea, result, or system is reasonable.
1. Run a sanity check on the output before publishing. — 发布前快速检查一下输出是否合理。
2. The order of magnitude passed a sanity check. — 数量级检查结果合理。

### edge case
**意思：** 边界或少见情况，容易暴露缺陷。类似：*boundary case; corner case.*
**English explanation:** An unusual situation near the limits of expected input or operation.
1. Empty input is an important edge case. — 空输入是一个重要的边界情况。
2. We tested edge cases around the maximum size. — 我们测试了最大尺寸附近的边界情况。

### trade-off
**词汇补充：** /ˈtreɪdˌɔf/；常搭配 *make a trade-off, trade-off between A and B*；近义 *compromise, balance*；反义无固定反义词。
**English explanation:** A situation in which gaining one benefit requires accepting a disadvantage elsewhere.
**意思：** 取舍；改善一方面通常要付出另一方面的代价。类似：*compromise; balance.*
1. There is a trade-off between memory use and speed. — 内存使用和速度之间存在取舍。
2. The design trade-off favors reliability over simplicity. — 这个设计取舍更重视可靠性而非简单性。

### under the hood
**意思：** 在内部实现层面，用户看不到的部分。类似：*internally; behind the scenes.*
**English explanation:** Inside a system or process, where its internal operation is not usually visible.
1. The interface looks simple, but a lot happens under the hood. — 界面看起来简单，但内部做了很多工作。
2. Let's inspect what the library does under the hood. — 我们来看看这个库内部是怎么运作的。

### spin up
**意思：** 快速启动/创建服务、实例或环境。类似：*start up; provision.*
**English explanation:** To start or create a system, service, or virtual resource, often quickly.
1. We spun up a test cluster in minutes. — 我们几分钟就启动了测试集群。
2. Spin up a local database for the demo. — 为演示启动一个本地数据库。

### tear down
**意思：** 关闭并清理环境/资源；也可拆除。类似：*shut down and remove; dismantle.*
**English explanation:** To shut down and remove a system, environment, or component after use.
1. The script tears down the test environment afterward. — 脚本随后会关闭并清理测试环境。
2. We tore down the temporary cluster. — 我们拆除了临时集群。

### ramp up
**意思：** 逐步增加数量、强度或规模。类似：*increase gradually; scale up.*
**English explanation:** To increase activity, capacity, or resources gradually.
1. We ramped up traffic gradually. — 我们逐渐增加了流量。
2. The team is ramping up testing before launch. — 团队正在发布前逐步加强测试。

### scale up
**意思：** 扩大容量/规模，常指增加资源或处理能力。类似：*increase capacity; expand.*
**English explanation:** To increase a system's capacity, usually by adding more resources to a component.
1. We need to scale up the workers for peak demand. — 高峰需求下我们需要扩充工作进程。
2. The method scales up to millions of records. — 该方法可扩展到数百万条记录。

### pile up
**意思：** 堆积、累积，常指请求或待办事项。类似：*accumulate; build up.*
**English explanation:** To accumulate or collect in increasing amounts.
1. Requests piled up while the service was unavailable. — 服务不可用时请求不断积压。
2. Small delays can pile up over time. — 小延迟会逐渐累积。

### back up
**意思：** 备份；支持/佐证；堵塞（语境不同）。类似：*make a copy; support; become congested.*
**English explanation:** To create a copy for recovery; it can also mean support or obstruct, depending on context.
1. Back up the database before the migration. — 迁移前备份数据库。
2. The results back up our initial hypothesis. — 结果支持了我们的初步假设。

### bog down
**意思：** 使进展/系统变慢或陷入停滞。类似：*slow down; get stuck.*
**English explanation:** To become slow or difficult to move forward, often because of too much work or complexity.
1. Excessive logging bogged down the service. — 过多日志拖慢了服务。
2. The review bogged down over a minor detail. — 审查因一个小细节而陷入停滞。

### flush out
**意思：** 查出/暴露隐藏问题；也可冲洗排出。类似：*uncover; reveal.*
**English explanation:** To reveal, find, or remove something hidden or unwanted.
1. The stress test flushed out a race condition. — 压力测试暴露了一个竞态条件。
2. We need more logs to flush out the source of the leak. — 我们需要更多日志来查明泄漏源头。

### cap at
**意思：** 把上限设为……。类似：*limit to; set a maximum of.*
**English explanation:** To set or reach a maximum value of.
1. We cap retries at three attempts. — 我们把重试次数上限定为三次。
2. Memory use is capped at two gigabytes. — 内存使用上限为两 GB。

### short-circuit
**词汇补充：** /ˌʃɔrtˈsɜrkɪt/；常搭配 *short-circuit evaluation, short-circuit a lookup*；近义 *bypass, terminate early*；反义 *continue full evaluation*。
**English explanation:** To stop a process early when a condition makes further work unnecessary; also to bypass the normal route.
**意思：** 提前结束处理/逻辑求值；电路中为短路。类似：*skip remaining work; terminate early.*
1. The cache hit short-circuits the database lookup. — 缓存命中后就跳过数据库查询。
2. The condition short-circuits evaluation when the value is null. — 值为空时该条件会短路求值。

### guard against
**意思：** 采取措施防止某风险。类似：*protect against; prevent.*
**English explanation:** To take steps to prevent or reduce the chance of something harmful.
1. Validate the input to guard against injection. — 验证输入以防止注入攻击。
2. The retry limit guards against runaway traffic. — 重试上限可防止流量失控。

### fan out
**意思：** 将工作分发给多个目标/进程；也可指分支扩展。类似：*distribute; branch out.*
**English explanation:** To distribute work or requests across several destinations or parallel tasks.
1. The coordinator fans out requests to five workers. — 协调器把请求分发给五个工作进程。
2. The query fans out across several shards. — 查询会分散到多个分片上。

### wire up
**意思：** 连接并配置组件使其协同工作。类似：*connect; hook up.*
**English explanation:** To connect components so they can work together.
1. We wired up the metrics before the load test. — 负载测试前我们接好了指标监控。
2. The adapter wires the client up to the service. — 适配器把客户端连接到服务。

### surface
**词汇补充：** /ˈsɜrfɪs/（名词）；/ˈsɜrfəs/（动词）；常搭配 *surface an issue/error, surface information*；近义 *reveal, expose*；反义 *hide, conceal*。
**English explanation:** To make information or a problem visible or available.
**意思：** 显露/呈现问题、数据或功能；也可作名词“表面”。类似：*expose; reveal; make visible.*
1. The dashboard surfaces errors in real time. — 仪表板实时显示错误。
2. A race condition surfaced under load. — 高负载下暴露出了竞态条件。

### throttle
**词汇补充：** /ˈθrɑtəl/；常搭配 *throttle requests/traffic, rate-throttle*；近义 *limit, restrict*；反义 *unthrottle, accelerate*。
**English explanation:** To limit the rate or amount of activity, data, or requests.
**意思：** 限流、抑制速度或频率。类似：*rate-limit; slow down.*
1. The API throttles requests from each client. — API 对每个客户端的请求进行限流。
2. The CPU throttles when it overheats. — CPU 过热时会降低运行速度。

### back off
**意思：** 减少尝试/暂时停止；重试中常指延长间隔。类似：*ease off; wait before retrying.*
**English explanation:** To reduce pressure, activity, or the frequency of attempts.
1. Clients back off after a failed request. — 请求失败后客户端会延长等待再试。
2. Back off the polling interval when the server is busy. — 服务器繁忙时拉长轮询间隔。

### spike
**词汇补充：** /spaɪk/；常搭配 *a spike in latency/traffic, spike suddenly*；近义 *surge, jump*；反义 *drop, decline*。
**English explanation:** A sudden sharp increase in a quantity or level.
**意思：** 突增；尖峰。类似：*surge; sudden increase.*
1. We saw a spike in latency after deployment. — 部署后延迟突然升高。
2. Traffic spikes every Monday morning. — 每周一早上流量都会激增。

### overshoot
**词汇补充：** /ˌoʊvərˈʃut/；常搭配 *overshoot a target/limit*；近义 *exceed, go beyond*；反义 *undershoot, fall short*。
**English explanation:** To go beyond a target, limit, or expected amount.
**意思：** 超过目标/上限。类似：*exceed; go past the target.*
1. The controller overshot the target value. — 控制器超过了目标值。
2. The estimate overshot the actual cost by 15%. — 估算成本比实际高出 15%。

### reclaim
**词汇补充：** /rɪˈkleɪm/；常搭配 *reclaim memory/space, reclaim a resource*；近义 *recover, retrieve*；反义 *relinquish, release*（依语境）。
**English explanation:** To recover or make available again, especially memory, space, or other resources.
**意思：** 回收或重新获得资源。类似：*recover; retrieve.*
1. The garbage collector reclaims unused memory. — 垃圾回收器会回收未使用的内存。
2. The process reclaims the lock after a timeout. — 超时后进程会重新获取锁。

### headroom
**词汇补充：** /ˈhɛdˌrum/；常搭配 *leave/provide headroom, capacity headroom*；近义 *spare capacity, margin*；反义 *capacity limit*（概念对照）。
**English explanation:** Unused capacity or room available before a limit is reached.
**意思：** 剩余容量/余量，可供负载增长。类似：*spare capacity; margin.*
1. We need more CPU headroom for traffic spikes. — 我们需要更多 CPU 余量应对流量峰值。
2. The cluster has little headroom left. — 集群剩余容量不多了。

### hot path
**意思：** 被频繁执行、对性能影响很大的代码路径。类似：*critical path; frequently executed path.*
**English explanation:** A frequently executed part of a program where performance has a large effect.
1. Avoid allocations in the hot path. — 热路径中要避免内存分配。
2. We optimized the hot path after profiling. — 性能分析后我们优化了关键代码路径。

### flaky
**词汇补充：** /ˈfleɪki/；常搭配 *flaky test/connection, flaky behavior*；近义 *unreliable, intermittent*；反义 *reliable, stable*。
**English explanation:** Unreliable in an inconsistent way, sometimes working and sometimes failing.
**意思：** 时好时坏、不稳定的（常说测试/网络）。类似：*intermittent; unreliable.*
1. The test is flaky on the shared runner. — 这个测试在共享运行器上时好时坏。
2. A flaky connection caused the retries. — 不稳定的连接引发了重试。

### brittle
**词汇补充：** /ˈbrɪtəl/；常搭配 *brittle code/design, brittle dependency*；近义 *fragile, breakable*；反义 *robust, resilient*。
**English explanation:** Easily broken or made to fail by small changes.
**意思：** 脆弱的，容易因小变化而失效。类似：*fragile; easily broken.*
1. The parser is brittle when fields are reordered. — 字段顺序变化时解析器就容易出错。
2. This workaround is brittle and hard to maintain. — 这个临时方案很脆弱，也难维护。

### fail silently
**意思：** 失败却不报错/不给提示。类似：*fail without an error; fail invisibly.*
**English explanation:** To fail without producing a visible error message or warning.
1. The script can fail silently if the file is missing. — 文件缺失时脚本可能悄无声息地失败。
2. We added logging so invalid records don't fail silently. — 我们加了日志，避免无效记录静默失败。

### roll back
**意思：** 回退到先前版本/状态。类似：*revert; undo a deployment.*
**English explanation:** To restore an earlier version or state after a change causes a problem.
1. We rolled back the release after errors increased. — 错误增加后我们回滚了发布。
2. The transaction rolls back if validation fails. — 验证失败时事务会回滚。

### factor out
**意思：** 抽取共同逻辑/因素，使其独立处理。类似：*extract; separate.*
**English explanation:** To separate a common or shared part so it can be handled independently.
1. We factored out the shared validation code. — 我们抽取了共用的验证代码。
2. Factor out the setup cost before comparing runtimes. — 比较运行时间前先把初始化成本分离出来。

### mock out
**意思：** 用模拟对象替代真实依赖。类似：*stub; simulate a dependency.*
**English explanation:** To replace a real component with a simplified test substitute.
1. We mocked out the payment service in the unit test. — 单元测试中我们模拟了支付服务。
2. Mock out the network call to keep the test deterministic. — 模拟网络调用，让测试结果可重复。

### smoke test
**意思：** 快速基本测试，确认关键功能能启动/运行。类似：*basic sanity test; quick check.*
**English explanation:** A short initial test that checks whether the main functions work well enough for further testing.
1. Run a smoke test after deployment. — 部署后运行一次冒烟测试。
2. The smoke test confirmed that login still works. — 冒烟测试确认登录仍可使用。

### end-to-end
**词汇补充：** /ˌɛnd tə ˈɛnd/；常搭配 *end-to-end test/encryption/latency*；近义 *full-path, complete-pipeline*；反义 *unit-level, partial*（语境对照）。
**English explanation:** Covering the complete process from its initial input to its final output.
**意思：** 端到端的，覆盖完整流程。类似：*full-pipeline; from start to finish.*
1. We added an end-to-end test for checkout. — 我们为结账流程增加了端到端测试。
2. End-to-end latency includes network and processing time. — 端到端延迟包括网络和处理时间。

### overhead
**词汇补充：** /ˈoʊvərˌhɛd/；常搭配 *runtime/memory/protocol overhead*；近义 *extra cost, additional burden*；反义无固定反义词。
**English explanation:** Extra time, work, or resources required in addition to the main task.
/ˈoʊvərˌhɛd/ **n.** 额外开销（资源/时间）；也可指管理费用。搭配：runtime/memory overhead. 近：extra cost; 反：无常用反义词.
1. Encryption adds a small amount of overhead. — 加密会增加少量额外开销。
2. The framework's memory overhead is substantial. — 该框架的内存开销很大。

### footprint
**词汇补充：** /ˈfʊtˌprɪnt/；常搭配 *memory/disk/resource footprint*；近义 *resource usage, space requirement*；反义无固定反义词。
**English explanation:** The amount of memory, storage, energy, or other resources used by a system.
/ˈfʊtˌprɪnt/ **n.** 占用规模，尤指内存、磁盘或资源。类似：*resource usage; memory footprint.*
1. The container has a smaller disk footprint. — 这个容器占用的磁盘空间更少。
2. We measured the application's memory footprint. — 我们测量了应用的内存占用。

### amortize
**词汇补充：** /əˈmɔrˌtaɪz/；常搭配 *amortize a cost over time/across requests*；近义 *spread, distribute*（成本）；反义 *pay upfront*（概念对照）。
**English explanation:** To spread a cost or amount of work across multiple uses or over time.
/əˈmɔrˌtaɪz/ **v.** 将一次性成本分摊到多次操作。类似：*spread a cost over repeated operations.*
1. Batching amortizes the setup cost across many requests. — 批处理把初始化成本分摊到许多请求上。
2. We amortized the index build over a long run. — 我们把索引构建成本分摊到长时间运行中。

### bottleneck on
**意思：** 因……而受限/形成瓶颈。类似：*be limited by; be bottlenecked by.*
**English explanation:** To be limited in speed or capacity by a particular component or resource.
1. The pipeline bottlenecks on disk writes. — 流水线受磁盘写入限制。
2. The service is bottlenecked on a single database connection. — 服务瓶颈在于只有一个数据库连接。

### deploy in production
**意思：** 部署到真实生产环境。类似：*release to production; roll out live.*
**English explanation:** To put software into operation in the live environment used for real work.
1. We deployed the patch in production after the canary passed. — 金丝雀测试通过后，我们把补丁部署到了生产环境。
2. Never deploy an unreviewed change in production. — 不要把未经审查的改动部署到生产环境。

### production workload
**意思：** 生产环境中的实际工作负载。类似：*live traffic; real operational load.*
**English explanation:** The actual or representative work handled by a live system.
1. We replayed a production workload in staging. — 我们在预发布环境重放了生产工作负载。
2. The benchmark does not match our production workload. — 这个基准测试与我们的生产工作负载不匹配。

### representative workload
**意思：** 能代表真实使用情况的工作负载。类似：*typical workload; realistic workload.*
**English explanation:** A set of tasks or inputs that reflects typical real-world use.
1. We selected a representative workload for the benchmark. — 我们为基准测试选取了有代表性的工作负载。
2. A synthetic test may not be representative of production. — 合成测试可能无法代表生产环境。

### incur overhead
**意思：** 产生额外开销。类似：*add overhead; introduce extra cost.*
**English explanation:** To require or create extra costs in time, processing, or resources.
1. The extra logging incurs overhead. — 额外日志记录会产生开销。
2. Compression incurs CPU overhead but saves bandwidth. — 压缩增加 CPU 开销，但节省带宽。

### benchmark against X
**意思：** 以 X 为基准进行性能比较。类似：*compare with X; measure against X.*
**English explanation:** To measure performance and compare it with X.
1. We benchmarked the new engine against the previous version. — 我们以旧版本为基准测试新引擎。
2. Benchmark the method against a standard implementation. — 用标准实现作为基准测试该方法。

### outperform X
**意思：** 表现优于 X。类似：*do better than; exceed the performance of.*
**English explanation:** To perform better than X according to a relevant measure.
1. The optimized query outperformed the baseline. — 优化后的查询表现优于基线。
2. The model outperformed human reviewers on this task. — 在这项任务上，模型表现优于人工审查者。

### under contention
**意思：** 多个任务竞争共享资源时。类似：*under resource competition; when contended.*
**English explanation:** While multiple processes or users compete for a shared resource.
1. Throughput falls under contention. — 资源竞争时吞吐量会下降。
2. The lock behaves poorly under contention. — 锁在竞争激烈时表现不佳。

### design trade-off
**意思：** 设计选择中的利弊权衡。类似：*architectural compromise; design compromise.*
**English explanation:** A design choice in which improving one property requires compromising another.
1. This design trade-off favors throughput over fairness. — 这个设计取舍更重视吞吐量而非公平性。
2. We documented the design trade-off in the proposal. — 我们在提案中记录了设计权衡。

### performance bottleneck
**意思：** 限制系统性能的环节。类似：*limiting factor; performance constraint.*
**English explanation:** A component or step that limits the overall speed of a system.
1. Profiling identified serialization as the performance bottleneck. — 性能分析发现序列化是性能瓶颈。
2. The bottleneck shifted from CPU to storage. — 瓶颈从 CPU 转移到了存储。

### resource utilization
**意思：** 资源利用率/使用情况。类似：*resource usage; utilization level.*
**English explanation:** The proportion of available resources that a system is using.
1. We monitored CPU and memory utilization. — 我们监控了 CPU 和内存利用率。
2. Low resource utilization suggests the service is waiting on I/O. — 资源利用率低表明服务可能在等待 I/O。

### fault tolerance
**意思：** 容错能力；故障时继续运行或恢复的能力。类似：*resilience; failure tolerance.*
**English explanation:** The ability of a system to continue operating despite some component failures.
1. Replication improves fault tolerance. — 副本机制提升容错能力。
2. The design provides fault tolerance across two zones. — 该设计能容忍两个可用区中的故障。

### tail latency
**意思：** 延迟分布高分位部分的响应时间。类似：*high-percentile latency; slowest-request latency.*
**English explanation:** The response time of the slowest portion of requests, often summarized by a high percentile.
1. A retry storm can worsen tail latency. — 重试风暴会恶化尾延迟。
2. We report p99 tail latency. — 我们报告 p99 尾延迟。

### p99 latency
**意思：** 99% 的请求延迟不高于该值，另有 1% 更慢。类似：*99th-percentile latency.*
**English explanation:** The response-time value below which 99 percent of requests complete.
1. The cache reduced p99 latency by 30%. — 缓存使 p99 延迟降低了 30%。
2. Average latency improved, but p99 latency worsened. — 平均延迟改善了，但 p99 延迟变差了。

### scale to X
**意思：** 扩展到 X 的规模/容量。类似：*handle X at scale; grow to X.*
**English explanation:** To increase or support capacity until the system can handle X users, requests, or workload.
1. The design scales to thousands of nodes. — 该设计可扩展到数千个节点。
2. We need to know whether the method scales to larger inputs. — 我们需要知道该方法能否扩展到更大的输入。

### microbenchmark
**词汇补充：** /ˈmaɪkroʊˌbɛntʃˌmɑrk/；常搭配 *run/design a microbenchmark*；近义 *small-scale benchmark, component-level test*；反义无固定反义词。
**English explanation:** A small, focused performance test of a specific operation or component.
**意思：** 测量很小代码单元/操作性能的基准测试。类似：*small-scale benchmark; operation-level test.*
1. The microbenchmark measures hash lookup time. — 微基准测试测量哈希查找时间。
2. Microbenchmarks may miss system-level overhead. — 微基准测试可能忽略系统层面的开销。

### stress test
**意思：** 以极端/高负载检验稳定性和极限。类似：*extreme-load test; robustness test.*
**English explanation:** A test that pushes a system beyond normal conditions to reveal limits or failure behavior.
1. We ran a stress test overnight. — 我们夜间进行了压力测试。
2. The stress test exposed a memory leak. — 压力测试暴露了内存泄漏。

### load test
**意思：** 在预期或指定负载下测性能。类似：*performance test under load.*
**English explanation:** A test that measures how a system performs under a specified amount of work or traffic.
1. The load test simulated five thousand users. — 负载测试模拟了五千名用户。
2. Run a load test before increasing the traffic limit. — 提高流量上限前先做负载测试。

### regression test
**意思：** 确认新改动没有破坏已有功能的测试。类似：*test for regressions; re-test existing behavior.*
**English explanation:** A test that checks whether a change has broken behavior that previously worked.
1. We added a regression test for the parsing bug. — 我们为解析 bug 添加了回归测试。
2. The regression suite passed after the refactor. — 重构后回归测试套件通过了。

### root cause
**意思：** 根本原因，而非表面症状。类似：*underlying cause; primary cause.*
**English explanation:** The underlying reason that produced a problem, rather than a symptom of it.
1. The root cause was a stale configuration. — 根本原因是配置过期。
2. We fixed the symptom but not the root cause. — 我们修复了表面症状，却没有解决根本原因。

### failure mode
**意思：** 系统可能如何失败的具体方式/模式。类似：*mode of failure; failure scenario.*
**English explanation:** A particular way in which a system or component can fail.
1. We identified a failure mode involving network partitions. — 我们找到了涉及网络分区的一种故障模式。
2. Each failure mode needs a recovery strategy. — 每种故障模式都需要恢复策略。

### performance regression
**意思：** 改动导致性能变差。类似：*slowdown; performance degradation.*
**English explanation:** A reduction in speed or efficiency caused by a change.
1. The release introduced a performance regression. — 这次发布引入了性能退化。
2. We track performance regressions in CI. — 我们在 CI 中跟踪性能退化。

### memory footprint
**意思：** 程序/数据占用的内存规模。类似：*memory usage; resident memory.*
**English explanation:** The amount of memory a process or system occupies.
1. The new format cuts the memory footprint in half. — 新格式把内存占用减半。
2. We measured the peak memory footprint. — 我们测量了峰值内存占用。

### lock contention
**意思：** 多线程/进程竞争同一把锁。类似：*contention for a lock; lock competition.*
**English explanation:** Competition among threads or processes that need the same lock.
1. Lock contention increased as workers were added. — 增加工作进程后锁竞争加剧。
2. Sharding reduced lock contention. — 分片减少了锁竞争。

### cache hit rate
**意思：** 请求/查询中由缓存直接满足的比例。类似：*cache hit ratio.*
**English explanation:** The share of requests that find the needed data in a cache.
1. The cache hit rate rose after warm-up. — 预热后缓存命中率上升。
2. A low cache hit rate can increase database load. — 缓存命中率低会增加数据库负载。

### resource constraint
**意思：** 资源方面的限制。类似：*resource limit; capacity constraint.*
**English explanation:** A limit imposed by the amount of a resource that is available.
1. Power is the main resource constraint on the device. — 电力是这台设备面临的主要资源限制。
2. We redesigned the service under a memory constraint. — 我们在内存受限的条件下重新设计了服务。

### distributed system
**意思：** 多台独立计算机通过网络协作的系统。类似：*distributed computing system.*
**English explanation:** A set of networked computers that coordinate to provide a service or perform work.
1. A distributed system must handle partial failures. — 分布式系统必须处理局部故障。
2. Clock synchronization is difficult in a distributed system. — 分布式系统中的时钟同步很困难。

### dependency
**词汇补充：** /dɪˈpɛndənsi/；常搭配 *external/runtime dependency, dependency on X*；近义 *prerequisite, required component*；反义 *independence*。
**English explanation:** A component, service, or condition that another component relies on.
**意思：** 依赖项；一个组件所需的另一个组件。类似：*prerequisite; required component.*
1. The package has an outdated dependency. — 这个包有一个过时的依赖项。
2. We removed a dependency on the external service. — 我们移除了对外部服务的依赖。

### partial failure
**意思：** 系统一部分失败、其他部分仍正常。类似：*localized failure; component failure.*
**English explanation:** A failure in which some parts of a system stop working while other parts continue.
1. The service remained available during a partial failure. — 局部故障期间服务仍可用。
2. A partial failure can be harder to diagnose than a full outage. — 局部故障有时比完全中断更难诊断。

## Useful

### kick in
**意思：** 开始起作用/生效。类似：*take effect; start working.*
**English explanation:** To begin to operate or have an effect.
1. The retry limit kicks in after three failures. — 失败三次后重试上限开始生效。
2. The cache kicks in once the data are loaded. — 数据加载后缓存开始发挥作用。

### fall back to
**意思：** 主方案不可用时退回到备用方案。类似：*revert to; use as a backup.*
**English explanation:** To use a backup option when the preferred option is unavailable or fails.
1. The client falls back to a local copy. — 客户端退回使用本地副本。
2. If the GPU is unavailable, the code falls back to the CPU. — GPU 不可用时，代码会回退到 CPU。

### top out at
**意思：** 最高达到……；达到峰值后不再上升。类似：*peak at; max out at.*
**English explanation:** To reach a highest value or limit and not increase beyond it.
1. Throughput tops out at 800 requests per second. — 吞吐量最高达到每秒 800 个请求。
2. The cost tops out at fifty dollars a month. — 费用最高为每月 50 美元。

### level off
**意思：** 上升/下降后趋于平稳。类似：*stabilize; plateau.*
**English explanation:** To become stable after rising or falling.
1. CPU use levels off after warm-up. — 预热后 CPU 使用率趋于稳定。
2. The error rate leveled off near 2%. — 错误率稳定在约 2%。

### choke on
**意思：** 无法处理/被某类输入或负载拖垮。类似：*struggle with; fail under.*
**English explanation:** To be unable to process something successfully, often because it is too large or difficult.
1. The parser chokes on empty fields. — 解析器无法处理空字段。
2. The service choked on the sudden traffic spike. — 突发流量峰值压垮了服务。

### bubble up
**意思：** 从底层向上层传播/显现。类似：*propagate upward; surface.*
**English explanation:** To move from a lower level to a higher one, especially an error or event becoming visible upstream.
1. The exception bubbles up to the caller. — 异常会向上传递给调用者。
2. User-facing errors bubble up from the storage layer. — 面向用户的错误从存储层逐级传上来。

### kick off
**意思：** 启动、开始。类似：*start; launch.*
**English explanation:** To begin an activity, process, or event.
1. We kicked off the migration last night. — 我们昨晚启动了迁移。
2. The script kicks off a background job. — 脚本会启动一个后台任务。

### max out
**意思：** 达到最大容量/极限。类似：*reach capacity; hit the limit.*
**English explanation:** To reach the maximum amount or capacity.
1. The connection pool maxed out during the test. — 测试期间连接池达到上限。
2. The disk is nearly maxed out. — 磁盘空间快满了。

### feed into
**意思：** 输入到/成为后续步骤的依据。类似：*flow into; contribute to.*
**English explanation:** To contribute to or become an input for another process or result.
1. The cleaned data feed into the final model. — 清理后的数据会输入最终模型。
2. These metrics feed into the alerting system. — 这些指标会进入告警系统。

### noisy
**词汇补充：** /ˈnɔɪzi/；常搭配 *noisy data/signal/measurement*；近义 *variable, contaminated*（依语境）；反义 *clean, stable*。
**English explanation:** Containing irregular variation or unwanted signals that make a pattern harder to detect.
**意思：** 含噪声/波动大；也可指日志过多。类似：*variable; noisy signal.*
1. The measurements are noisy at low load. — 低负载时测量值波动较大。
2. The debug logs are too noisy to be useful. — 调试日志太多，反而不好用。

### hang
**词汇补充：** /hæŋ/；常搭配 *hang indefinitely, hang on startup*；近义 *freeze, become unresponsive*；反义 *respond, resume*。
**English explanation:** To stop responding while remaining active, often because it is waiting or stuck.
**意思：** 卡住、无响应；也可指挂载/悬挂。类似：*freeze; become unresponsive.*
1. The process hangs when the connection drops. — 连接断开时进程会卡住。
2. The test hangs indefinitely on Windows. — 这个测试在 Windows 上会一直卡住。

### stub out
**意思：** 用临时空实现/桩替代完整功能。类似：*mock; provide a placeholder implementation.*
**English explanation:** To replace a component temporarily with a simple placeholder during development or testing.
1. We stubbed out the network layer for unit tests. — 单元测试中我们用桩替代网络层。
2. Stub out the method until the API is finalized. — API 定稿前先给该方法写个占位实现。

### step through
**意思：** 逐步执行/检查，常指调试代码。类似：*trace through; debug step by step.*
**English explanation:** To examine or execute a program one instruction or stage at a time.
1. We stepped through the function in the debugger. — 我们在调试器中逐步执行了这个函数。
2. Let's step through the request path. — 我们逐步检查一下请求路径。

### real-world trace
**意思：** 从真实系统采集的运行轨迹/事件记录。类似：*production trace; operational trace.*
**English explanation:** A record of events or requests captured from actual system use.
1. We replayed a real-world trace in the simulator. — 我们在模拟器中重放了真实运行轨迹。
2. The benchmark uses a real-world trace of user requests. — 该基准测试使用了真实用户请求轨迹。

### design space
**意思：** 可供选择的设计方案范围。类似：*set of design options; solution space.*
**English explanation:** The set of possible design choices and their trade-offs.
1. We explored the design space for storage layouts. — 我们探索了存储布局的设计空间。
2. The design space is constrained by memory. — 内存限制了可选设计范围。

### state of the art
**意思：** 当前最先进水平/最佳已知方法。类似：*leading; best currently available.*
**English explanation:** The most advanced level currently achieved in a field.
1. The method approaches the state of the art. — 该方法接近当前最先进水平。
2. We compare against state-of-the-art baselines. — 我们与最先进的基线方法比较。

### round-trip
**词汇补充：** /ˈraʊndˌtrɪp/；常搭配 *round-trip time/latency, round-trip conversion*；近义 *request-response cycle*；反义无固定反义词。
**English explanation:** A complete journey from a starting point to a destination and back; in computing, an exchange that returns a response.
**意思：** 往返过程；请求发出并收到响应的完整周期；序列化后再还原。类似：*request-response cycle; encode-decode cycle.*
1. The round-trip takes about 40 milliseconds. — 一次往返大约需要 40 毫秒。
2. The parser preserves comments through a round-trip. — 经过解析再还原后，解析器仍保留注释。

### production cluster
**意思：** 承载真实生产流量的集群。类似：*live cluster; production environment.*
**English explanation:** A group of machines running a live service or real workload.
1. We cannot restart the production cluster during business hours. — 工作时间不能重启生产集群。
2. The patch was first tested outside the production cluster. — 这个补丁先在生产集群之外测试。

### bisect
**词汇补充：** /baɪˈsɛkt/；常搭配 *bisect a range/commit history*；近义 *divide in half, binary-search*；反义 *combine, merge*。
**English explanation:** To divide a range into two parts repeatedly; in debugging, to find a change by testing the midpoint of a sequence.
/baɪˈsɛkt/ **v.** 二分定位；常指用二分法找出引入故障的提交。类似：*narrow down by binary search.*
1. We bisected the commits to find the regression. — 我们用二分法定位了引入退化的提交。
2. Bisect the input range to isolate the failing case. — 对输入范围二分以定位失败案例。

### blast radius
**意思：** 故障/改动可能影响的范围。类似：*scope of impact; failure impact area.*
**English explanation:** The extent of damage or disruption caused when a failure occurs.
1. Feature flags reduce the blast radius of a bad release. — 功能开关能缩小错误发布的影响范围。
2. The outage had a large blast radius. — 这次中断影响范围很大。

### composability
**词汇补充：** /kəmˌpoʊzəˈbɪləti/；常搭配 *improve/enable composability*；近义 *modularity, interoperability*（相关概念）；反义 *rigidity, monolithic design*。
**English explanation:** The ability to combine components into larger systems while preserving useful behavior.
/ˌkɑmpoʊzəˈbɪləti/ **n.** 可组合性；组件能否灵活组合。类似：*modularity; ability to compose.*
1. The API improves composability across services. — 该 API 提高了服务间的可组合性。
2. Composability makes the pipeline easier to extend. — 可组合性让流水线更容易扩展。

### decentralized system
**意思：** 没有单一中心控制节点、由多个节点共同运作的系统。类似：*distributed system; peer-to-peer system*（含义不完全相同）.
**English explanation:** A system in which control or responsibility is distributed across multiple participants rather than held by one central authority.
1. A decentralized system can avoid a single point of control. — 去中心化系统可以避免单一控制点。
2. We studied coordination in a decentralized system. — 我们研究了去中心化系统中的协调机制。

### blob
**词汇补充：** /blɑb/；常搭配 *store/read a blob, binary large object (BLOB)*；近义 *opaque data object, data chunk*；反义无固定反义词。
**English explanation:** A large, undifferentiated block of data or binary content.
/blɑb/ **n.** 一大块/团；技术中泛指未结构化的数据对象。类似：*binary large object; opaque data chunk.*
1. The API stores the image as a blob. — API 把图像作为二进制对象存储。
2. The response returned one large blob of text. — 响应返回了一大块文本。

## Specialized

### Escape hatch
**意思：** 紧急绕行/手动覆盖机制，让用户在常规机制失效时脱身。类似：*fallback mechanism; manual override.*
**English explanation:** A fallback mechanism or alternate route used to get out of a difficult situation.
1. The admin endpoint is an escape hatch during outages. — 服务中断时管理员端点可作为紧急绕行机制。
2. Keep an escape hatch for reverting the configuration. — 保留一个回退配置的应急入口。

### Key off
**意思：** 以某个信号/字段作为判断或触发依据。类似：*use as a cue; base on.*
**English explanation:** To use something as the signal or condition that determines an action.
1. The scheduler keys off the priority field. — 调度器根据优先级字段作判断。
2. The alert keys off sustained CPU usage. — 告警由持续的 CPU 使用率触发。

### trace through
**意思：** 沿着代码/事件流程逐步追踪。类似：*follow; walk through.*
**English explanation:** To follow a sequence of operations or events in order to understand what happens.
1. We traced the request through three services. — 我们追踪了请求经过的三个服务。
2. Trace through the code to see where the value changes. — 沿着代码追踪这个值在哪里改变。

### get around
**意思：** 绕过限制/问题；也可表示四处走动。类似：*work around; bypass.*
**English explanation:** To avoid or find a way past a restriction or obstacle; also to move through a place.
1. The patch gets around a bug in the old driver. — 这个补丁绕过了旧驱动中的一个 bug。
2. There is no safe way to get around the access check. — 没有安全的方法可以绕过访问检查。

### hook into
**意思：** 接入/挂接到系统或流程中。类似：*integrate with; connect to.*
**English explanation:** To connect to an existing system, event, or interface so that a component can use it.
1. The plugin hooks into the build pipeline. — 插件接入了构建流水线。
2. We hooked the monitor into the alert system. — 我们把监控器接入告警系统。

### creep up
**意思：** 悄悄逐渐增加/上升。类似：*gradually rise; inch up.*
**English explanation:** To increase slowly, often without being noticed at first.
1. Memory use crept up over several hours. — 几小时内内存使用悄悄上升了。
2. Costs can creep up if usage is not monitored. — 如果不监控使用量，成本可能会逐渐增加。

### drain
**词汇补充：** /dreɪn/；常搭配 *drain a queue/pool/battery*；近义 *deplete, empty*；反义 *replenish, fill*。
**English explanation:** To gradually use up a resource; as a noun, the act or route by which something is removed.
**意思：** 耗尽/排空资源；也可排水。类似：*deplete; empty.*
1. The bug drained the connection pool. — 这个 bug 耗尽了连接池。
2. Drain the queue before shutting down the worker. — 关闭工作进程前先清空队列。

### catch up
**意思：** 赶上进度/补上落后部分。类似：*keep up; make up lost ground.*
**English explanation:** To reach the same level or position after being behind.
1. The replica caught up after the network recovered. — 网络恢复后副本追上了进度。
2. We need more workers to catch up with the backlog. — 我们需要更多工作进程来清理积压任务。

### bump up
**意思：** 稍微提高/增加。类似：*increase; raise.*
**English explanation:** To increase an amount or level slightly.
1. We bumped up the timeout to avoid false failures. — 我们稍微延长了超时，避免误报失败。
2. Bump up the memory limit for this test. — 把这项测试的内存上限调高一点。

### bottom out
**意思：** 降到最低点后停止下降。类似：*hit a low; reach the minimum.*
**English explanation:** To reach the lowest point and stop declining.
1. Error rates bottomed out after the rollback. — 回滚后错误率降到了最低点。
2. The queue bottoms out overnight. — 队列通常在夜间降到最低。

### swallow an exception
**意思：** 捕获异常却不处理/不报告，导致错误被隐藏。类似：*silently ignore an exception.*
**English explanation:** To catch an error condition without reporting or handling it visibly.
1. The handler swallows the exception and returns success. — 处理器吞掉了异常，却返回成功。
2. Never swallow an exception without logging it. — 不要在不记录日志的情况下吞掉异常。

### fire off
**意思：** 快速发出/启动请求、命令或消息。类似：*send quickly; launch.*
**English explanation:** To send or start something quickly, such as a request or command.
1. The client fired off several requests at once. — 客户端一次发出了多个请求。
2. Fire off an alert when the threshold is crossed. — 超过阈值时立即发出警报。

### expose
**词汇补充：** /ɪkˈspoʊz/；常搭配 *expose an API/endpoint, expose a flaw*；近义 *reveal, make accessible*；反义 *hide, conceal*。
**English explanation:** To make a feature, value, or interface available for others to use or observe.
/ɪkˈspoʊz/ **v.** 暴露/公开；提供接口供调用。类似：*reveal; make accessible.*
1. The service exposes a health-check endpoint. — 服务提供了健康检查端点。
2. The test exposed a race condition. — 测试暴露了一个竞态条件。

### clamp
**词汇补充：** /klæmp/；常搭配 *clamp a value/range, clamp to a limit*；近义 *cap, constrain*；反义 *unbound, release*（依语境）。
**English explanation:** To restrict a value so that it stays within specified upper and lower limits.
/klæmp/ **v./n.** 将数值限制在上下界内。类似：*cap; constrain to a range.*
1. Clamp the input between zero and one. — 将输入限制在 0 到 1 之间。
2. The controller clamps the output to a safe range. — 控制器把输出限制在安全范围内。

### leak through
**意思：** 泄漏/穿透到不该出现的层或范围。类似：*escape; propagate unintentionally.*
**English explanation:** To pass through a barrier or abstraction that was expected to contain it.
1. Internal errors should not leak through to users. — 内部错误不应泄漏给用户。
2. A configuration detail leaked through the public API. — 一个配置细节泄漏到了公共 API。

### hold up under
**意思：** 在压力/检验下仍能维持。类似：*withstand; remain valid under.*
**English explanation:** To remain effective or intact when subjected to a particular condition or pressure.
1. The design held up under heavy traffic. — 这个设计经受住了高流量考验。
2. The assumption does not hold up under scrutiny. — 这个假设经不起仔细审查。

### sidestep
**词汇补充：** /ˈsaɪdˌstɛp/；常搭配 *sidestep a limitation/issue*；近义 *bypass, avoid*；反义 *confront, address directly*。
**English explanation:** To avoid a problem, rule, or direct confrontation by taking another route.
/ˈsaɪdˌstɛp/ **v.** 巧妙绕开问题/障碍。类似：*avoid; bypass.*
1. The patch sidesteps the compatibility issue. — 这个补丁绕开了兼容性问题。
2. We cannot sidestep the need for access control. — 我们无法回避访问控制的必要性。

### cap
**词汇补充：** /kæp/；常搭配 *cap the rate/number at X, impose a cap*；近义 *limit, restrict*；反义 *uncap, remove the limit*。
**English explanation:** To set or reach a maximum limit; as a noun, an upper limit.
/kæp/ **v./n.** 限制上限；上限。类似：*limit; ceiling.*
1. We cap each batch at 500 records. — 每批最多处理 500 条记录。
2. The API has a strict rate cap. — API 有严格的速率上限。

### gate
**词汇补充：** /ɡeɪt/；常搭配 *gate access/requests, gate a feature behind a flag*；近义 *control, filter*；反义 *allow, open*。
**English explanation:** To control whether or when something is allowed to proceed.
/ɡeɪt/ **v./n.** 控制是否允许通过；门/闸。类似：*control access; filter.*
1. A feature flag gates access to the new path. — 功能开关控制是否允许使用新路径。
2. The scheduler gates requests during overload. — 过载时调度器会限制请求进入。

### plug in
**意思：** 插入/接入；把组件集成到系统。类似：*connect; integrate.*
**English explanation:** To connect a component so that it can be used; also to insert a value into a formula.
1. Plug in the new storage backend. — 接入新的存储后端。
2. You can plug in a custom scheduler. — 你可以集成自定义调度器。

### rip out
**意思：** 彻底移除某组件/代码。类似：*remove completely; tear out.*
**English explanation:** To remove a component or section completely.
1. We ripped out the obsolete dependency. — 我们彻底移除了过时依赖。
2. The team ripped out the old retry logic. — 团队删掉了旧的重试逻辑。

### layer on
**意思：** 在已有基础上叠加新功能/复杂性。类似：*add on top of; build upon.*
**English explanation:** To add a new feature or component on top of what already exists.
1. We layered authentication on top of the existing service. — 我们在现有服务上增加了认证层。
2. Avoid layering on extra abstractions too early. — 不要过早叠加额外抽象。

### piggyback on
**意思：** 借助已有机制/资源顺带实现。类似：*reuse; take advantage of.*
**English explanation:** To make use of an existing system, process, or resource for an additional purpose.
1. The metric piggybacks on the existing telemetry pipeline. — 该指标顺带复用了现有遥测流水线。
2. We piggybacked the check on the deployment step. — 我们把检查安排在部署步骤中一并执行。

### plumbing
**词汇补充：** /ˈplʌmɪŋ/；常搭配 *infrastructure/telemetry plumbing*；近义 *wiring, infrastructure*；反义无固定反义词。
**English explanation:** The underlying connections and infrastructure that allow parts of a system to work together.
/ˈplʌmɪŋ/ **n.** 管道系统；技术中指支撑功能运行的底层连接/基础设施。类似：*infrastructure; wiring.*
1. The feature works, but the plumbing still needs cleanup. — 功能能用，但底层连接代码还需要整理。
2. We added telemetry plumbing to the service. — 我们为服务增加了遥测基础设施。

### boilerplate
**词汇补充：** /ˈbɔɪlərˌpleɪt/；常搭配 *boilerplate code/text, reduce boilerplate*；近义 *template code, standard text*；反义 *custom implementation*。
**English explanation:** Standard code or text reused with little change across many places.
/ˈbɔɪlərˌpleɪt/ **n./adj.** 样板代码/固定模板。类似：*template code; standard setup.*
1. The framework generates the boilerplate for us. — 框架会为我们生成样板代码。
2. This repository has too much boilerplate. — 这个代码库有太多重复样板代码。

### heavyweight
**词汇补充：** /ˈhɛviˌweɪt/；常搭配 *heavyweight framework/client*；近义 *resource-intensive, full-featured*；反义 *lightweight*。
**English explanation:** Requiring substantial resources or effort, or having many features and components.
/ˈhɛviˌweɪt/ **adj./n.** 资源消耗大/复杂度高的；重量级的。类似：*resource-intensive; full-featured.*
1. The heavyweight runtime is unnecessary for this task. — 这项任务不需要重量级运行时。
2. We replaced the heavyweight client with a smaller library. — 我们用更轻量的库替换了重量级客户端。

### zoom in on
**意思：** 聚焦/仔细查看某一细节。类似：*focus on; examine closely.*
**English explanation:** To examine one detail or part more closely.
1. Let's zoom in on the slowest request. — 我们仔细看一下最慢的请求。
2. The paper zooms in on one failure mode. — 论文聚焦于一种故障模式。

### zoom out
**意思：** 拉远视角；从整体层面看。类似：*take a broader view; step back.*
**English explanation:** To consider a wider view or the overall situation.
1. Zoom out and consider the whole pipeline. — 把视角放大，考虑整条流水线。
2. If we zoom out, the trend is clear. — 从整体来看，趋势很明显。

### fall back on
**意思：** 依靠/转而采用备用办法，常在其他办法失败时。类似：*rely on as a last resort.*
**English explanation:** To rely on a backup method when the preferred one is unavailable.
1. We can fall back on the previous implementation. — 我们可以退回依靠先前的实现。
2. The service falls back on local storage during outages. — 服务中断时会转而使用本地存储。

### opt into
**意思：** 选择加入/启用。类似：*choose to participate; enable voluntarily.*
**English explanation:** To choose to participate in or enable something.
1. Users can opt into detailed logging. — 用户可以选择启用详细日志。
2. The team opted into the preview program. — 团队选择加入预览计划。

### opt out of
**意思：** 选择退出/不参加。类似：*choose not to participate; withdraw from.*
**English explanation:** To choose not to participate in or use something.
1. Users may opt out of data collection. — 用户可以选择退出数据收集。
2. The service opted out of the experiment. — 该服务选择不参加实验。

### phase in
**意思：** 分阶段逐步引入。类似：*introduce gradually; roll out in stages.*
**English explanation:** To introduce something gradually over time.
1. We phased in the new policy over a month. — 我们用了一个月分阶段实施新政策。
2. The feature will be phased in region by region. — 该功能将按地区逐步推出。

### recover gracefully from X
**意思：** 从 X 中以可控方式恢复，避免崩溃或数据损坏。类似：*handle X robustly; fail gracefully.*
**English explanation:** To return to a useful operating state after X occurs, while limiting disruption or data loss.
1. The worker can recover gracefully from a timeout. — 工作进程能从超时中平稳恢复。
2. The parser should recover gracefully from malformed input. — 解析器应能妥善处理格式错误的输入并恢复。

### failure recovery
**意思：** 故障后的恢复过程/机制。类似：*recovery procedure; fault recovery.*
**English explanation:** The process of restoring a system or service after a failure.
1. We tested failure recovery after losing a node. — 节点丢失后我们测试了故障恢复。
2. Failure recovery must preserve committed data. — 故障恢复必须保留已提交的数据。

### request-response
**词汇补充：** /rɪˈkwɛst rɪˈspɑns/；常搭配 *request-response protocol/pattern*；近义 *request-reply*；反义 *one-way messaging*（模式对照）。
**English explanation:** An interaction in which one component sends a request and another returns a response.
**意思：** 请求—响应式交互模式。类似：*request-reply pattern.*
1. The API uses a request-response protocol. — 该 API 使用请求—响应协议。
2. Request-response is unsuitable for long-running jobs. — 请求—响应模式不适合长时间运行的任务。

### throughput at peak
**意思：** 峰值负载时的吞吐量。类似：*peak throughput; maximum processing rate.*
**English explanation:** The amount of work a system processes per unit of time during its highest-demand period.
1. We measured throughput at peak traffic. — 我们测量了峰值流量时的吞吐量。
2. Throughput at peak fell below the service target. — 峰值吞吐量低于服务目标。

### end-to-end analysis
**意思：** 对完整流程/系统路径进行的端到端分析。类似：*full-pipeline analysis.*
**English explanation:** An examination of the entire process from its starting point through its final outcome.
1. The end-to-end analysis includes network and storage costs. — 端到端分析包含网络和存储成本。
2. We performed an end-to-end analysis of the training pipeline. — 我们对训练流水线进行了端到端分析。

### I/O amplification
**意思：** 实际发生的输入/输出量相对于有效数据量的放大。类似：*write/read amplification.*
**English explanation:** A condition in which one logical operation causes a larger amount of physical input/output work.
1. Compaction reduced write I/O amplification. — 压实操作降低了写入 I/O 放大。
2. Random updates can cause severe I/O amplification. — 随机更新可能造成严重的 I/O 放大。

### cron
**词汇补充：** /krɑn/；常搭配 *cron job, cron schedule*；近义 *scheduled task*；反义 *event-triggered task*（模式对照）。
**English explanation:** A time-based job scheduler commonly used to run commands or scripts at specified intervals.
/krɑn/ **n.** 定时任务调度工具/格式；也指由 cron 安排的作业。类似：*scheduled job; cron task.*
1. A cron job cleans temporary files every night. — 一个 cron 定时任务每晚清理临时文件。
2. We moved the report generation to cron. — 我们把报告生成改由 cron 定时执行。

### band steering
/ˈbænd ˌstɪrɪŋ/ **n.** Wi-Fi 中将客户端引导到不同频段的技术。类似：*Wi-Fi client band selection.*
**English explanation:** A network technique that guides wireless devices toward a suitable frequency band.
1. Band steering moved the device to the 5 GHz network. — 频段引导把设备切换到了 5 GHz 网络。
2. We disabled band steering to diagnose the connection issue. — 为诊断连接问题，我们关闭了频段引导。

### thrash
**词汇补充：** /θræʃ/；常搭配 *thrash under memory pressure, disk thrashing*；近义 *swap excessively, perform poorly under contention*；反义 *run smoothly*。
**English explanation:** To spend excessive time switching tasks or moving data, leaving little useful progress.
/θræʃ/ **v./n.** 因资源不足反复交换/重试而效率骤降；也指剧烈摆动。类似：*resource thrashing; excessive swapping.*
1. The machine thrashed once memory pressure increased. — 内存压力上升后机器开始频繁换页。
2. Repeated cache eviction caused the database to thrash. — 反复淘汰缓存导致数据库系统忙乱低效。

### distribution transparency
/ˌdɪstrəˈbjuʃən trænsˈpɛrənsi/ **n.** 分布式系统中隐藏节点位置/分布细节，使调用看起来统一的性质。类似：*location transparency; abstraction over distribution.*
**English explanation:** The property that lets users interact with a distributed system without needing to know where its components run.
1. Distribution transparency simplifies client code. — 分布透明性简化了客户端代码。
2. Full distribution transparency can hide important failure modes. — 完全的分布透明性可能掩盖重要故障模式。
