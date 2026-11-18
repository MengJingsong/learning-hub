# Sentence Pattern Explanations

Examples use natural North American English. Each entry gives the pattern's meaning or use, a related frame, and two translated examples.

## Core

### It's less X and more Y
**意思/用法：** 温和地修正分类：与其说是 X，不如说更像 Y。类似：*It's not so much X as Y.*
1. It's less a bug and more a design limitation. — 与其说这是程序错误，不如说是设计限制。
2. The change is less about speed and more about reliability. — 这项改动与其说是为了速度，不如说是为了可靠性。

### X is separate from Y
**意思/用法：** 说明 X 与 Y 是不同问题或维度。类似：*X is distinct from Y.*
1. Model accuracy is separate from response time. — 模型准确率与响应时间是两个不同方面。
2. The login service is separate from the billing system. — 登录服务与计费系统彼此独立。

### The important number is that X
**意思/用法：** 引出关键数值或定量事实；X 通常是完整从句。类似：*The key figure is X.*
1. The important number is that only 3% of requests timed out. — 关键数据是只有 3% 的请求超时。
2. The important number is that costs fell by half. — 关键数字是成本下降了一半。

### The actual work is A, not B
**意思/用法：** 对比真正要做的工作和容易误解的部分。类似：*What we need to do is A rather than B.*
1. The actual work is validating the inputs, not rewriting the parser. — 实际要做的是验证输入，而不是重写解析器。
2. The actual work is comparing the two conditions, not collecting more data. — 真正的工作是比较两个条件，而不是收集更多数据。

### The risk of X is that Y
**意思/用法：** 指出 X 带来的风险，并用 that 从句说明后果。类似：*One concern with X is that Y.*
1. The risk of caching this result is that stale data may persist. — 缓存这个结果的风险是过期数据可能一直存在。
2. The risk of skipping the control is that we cannot isolate the cause. — 跳过对照的风险是我们无法确定原因。

### X implies Y
**意思/用法：** 表示 X 逻辑上意味着 Y；比 *suggests* 更强。类似：*X entails Y.*
1. A zero error rate implies that every request succeeded in this sample. — 零错误率意味着这个样本中的每个请求都成功了。
2. A higher score does not imply better calibration. — 分数更高并不意味着校准更好。

### X is ..., not Y
**意思/用法：** 用补充说明明确 X 的性质，并排除 Y 这种解释。类似：*X means ..., rather than Y.*
1. This is a temporary workaround, not a permanent fix. — 这是临时绕行方案，不是永久修复。
2. The estimate is conditional, not universal. — 这个估算有条件限制，并非普遍适用。

### X only if Y
**意思/用法：** 表示只有满足 Y，X 才成立；only 强调必要条件。类似：*X provided that Y.*
1. The job runs only if the input file exists. — 只有输入文件存在时，任务才会运行。
2. We can claim causality only if the assumptions hold. — 只有假设成立，我们才能声称存在因果关系。

### Without X, Y will ...
**意思/用法：** 说明缺少 X 时会出现 Y；常用于风险或必要条件。类似：*Unless we have X, Y will ...*
1. Without a timeout, the client will wait indefinitely. — 没有超时设置，客户端会一直等待。
2. Without more controls, the result will remain ambiguous. — 没有更多控制条件，结果仍会有歧义。

### If X ..., Y ...; otherwise, Z ... .
**意思/用法：** 给出条件分支；otherwise 指前一条件不成立时的替代结果。类似：*If not, ...*
1. If the cache is warm, use the fast path; otherwise, read from disk. — 如果缓存已热，就走快速路径；否则从磁盘读取。
2. If the evidence is strong, report the effect; otherwise, describe it as tentative. — 如果证据充分，就报告该效应；否则说明结论仍属暂定。

### Because X ..., Y ... .
**意思/用法：** Because 从句说明原因，主句说明结果。类似：*Since X, Y ...*
1. Because the sample is small, the confidence interval is wide. — 因为样本量小，置信区间很宽。
2. Because the service restarted, the connection was reset. — 因为服务重启了，连接被重置。

### X ..., which means that Y ... .
**意思/用法：** which means that 补充解释前面事实的含义或结果。类似：*This means that ...*
1. The limit is per user, which means that separate users have separate quotas. — 限额按用户计算，这意味着不同用户各有配额。
2. The value is cached, which means that updates may take a moment to appear. — 该值经过缓存，所以更新可能需要一点时间才会显示。

### X depends on both A and B.
**意思/用法：** 表示 X 同时取决于两个条件；both强调缺一不可。类似：*X is determined by A as well as B.*
1. Latency depends on both network distance and server load. — 延迟同时取决于网络距离和服务器负载。
2. The conclusion depends on both the measurement and the baseline. — 结论同时取决于测量结果和基线。

### X may ..., but that does not mean Y ... .
**意思/用法：** 承认 X 可能成立，同时提醒不能据此推出 Y。类似：*Although X, it doesn't follow that Y.*
1. The trend may be real, but that does not mean it is statistically significant. — 趋势可能是真实的，但这不代表它具有统计显著性。
2. The patch may reduce memory use, but that does not mean it improves throughput. — 补丁可能减少内存使用，但不代表它提高了吞吐量。

### X is consistent with Y, but does not establish Y.
**意思/用法：** 说明证据与 Y 相符，却不足以证明 Y。类似：*X supports Y without proving it.*
1. The survey is consistent with increased interest, but does not establish a causal effect. — 调查结果与兴趣上升相符，但不能证明因果效应。
2. This trace is consistent with a lock bottleneck, but does not establish one. — 这段跟踪记录与锁竞争瓶颈相符，但还不能据此认定存在该瓶颈。

### X alone is not proof, because Y could also ... .
**意思/用法：** 提醒单一证据不充分，因为也存在其他解释。类似：*X by itself does not show Y.*
1. A high correlation alone is not proof, because a third factor could affect both variables. — 高相关性本身不是证明，因为第三个因素可能同时影响两个变量。
2. One failed run alone is not proof, because the environment could also be unstable. — 一次运行失败本身不能证明问题存在，因为环境也可能不稳定。

### To distinguish A from B, measure C.
**意思/用法：** 指出区分两个解释所需的观测指标。类似：*Measure C to tell whether A or B is responsible.*
1. To distinguish network delay from queueing, measure both components. — 要区分网络延迟和排队延迟，就分别测量这两部分。
2. To distinguish recall from precision, report both metrics. — 要区分召回率和精确率，就报告这两个指标。

### Without X, we cannot tell whether A or B.
**意思/用法：** 说明缺少 X 时无法在 A 与 B 之间作判断。类似：*X is needed to determine whether A or B.*
1. Without a control group, we cannot tell whether the treatment caused the change. — 没有对照组，我们无法判断变化是否由处理造成。
2. Without timestamps, we cannot tell whether the events were simultaneous or sequential. — 没有时间戳，我们无法判断这些事件是同时还是先后发生的。

### Hold A fixed while varying B.
**意思/用法：** 实验中保持 A 不变，同时改变 B，以观察 B 的影响。类似：*Keep A constant as you change B.*
1. Hold the input size fixed while varying the thread count. — 固定输入大小，同时改变线程数。
2. Hold the training data fixed while varying the model architecture. — 固定训练数据，同时改变模型架构。

### X was observed; Y was inferred from Z.
**意思/用法：** 区分直接观察到的事实与依据 Z 推断的 Y。类似：*We observed X and inferred Y based on Z.*
1. A latency spike was observed; queue saturation was inferred from the logs. — 观察到了延迟峰值；根据日志推断队列已饱和。
2. The behavior was observed in two runs; instability was inferred from the variance. — 两次运行中都观察到该行为；根据方差推断系统不稳定。

### The result applies to X; it does not establish Y.
**意思/用法：** 限定结果的适用范围，避免过度外推。类似：*The finding is limited to X.*
1. The result applies to this workload; it does not establish performance on all workloads. — 结果适用于这个工作负载，不能证明对所有负载都成立。
2. The result applies to adults; it does not establish the same effect in children. — 结果适用于成年人，不能证明儿童中也有相同效应。

### X differs from Y in that ... .
**意思/用法：** 通过 in that 从句说明 X 与 Y 的具体差别。类似：*The difference is that ...*
1. The two protocols differ in that one retries automatically. — 两种协议的区别在于其中一种会自动重试。
2. This estimate differs from the earlier one in that it includes setup cost. — 这个估算与之前的不同，因为它计入了初始化成本。

### Even if X ..., Y may still ... .
**意思/用法：** 表示即使 X 成立，Y 仍可能发生；even if 引导让步条件。类似：*Although X, Y can still ...*
1. Even if the average is low, the tail latency may still be unacceptable. — 即使平均值低，尾延迟仍可能无法接受。
2. Even if the code compiles, the configuration may still be wrong. — 即使代码能够编译，配置仍可能有误。

### A possible explanation for X is that Y.
**意思/用法：** 提出一种可能原因，语气保持谨慎。类似：*X may be explained by Y.*
1. A possible explanation for the drop is that the cache was cold. — 性能下降的一种可能解释是缓存尚未预热。
2. A possible explanation for the mismatch is that the datasets use different filters. — 结果不一致的一种可能解释是数据集使用了不同筛选条件。

### These results should be interpreted with caution.
**意思/用法：** 提醒读者谨慎解读结果，常见于有限样本或不确定证据。类似：*The findings are tentative.*
1. These results should be interpreted with caution because the sample is small. — 由于样本量小，应谨慎解读这些结果。
2. These results should be interpreted with caution until the study is replicated. — 在研究得到重复验证前，应谨慎解读这些结果。

### Taken together, these results suggest that X.
**意思/用法：** 综合多项结果后提出一个谨慎推断。类似：*Overall, the findings point to X.*
1. Taken together, these results suggest that the intervention may help. — 综合来看，这些结果表明该干预可能有帮助。
2. Taken together, these results suggest that contention is the main bottleneck. — 综合来看，这些结果表明竞争可能是主要瓶颈。

### Further work is needed to determine whether X.
**意思/用法：** 指出仍需进一步研究才能判定 X。类似：*More research is needed to establish whether X.*
1. Further work is needed to determine whether the effect persists over time. — 还需要进一步研究来确定这种效应是否会持续。
2. Further work is needed to determine whether the approach scales to larger clusters. — 还需要进一步研究来确定该方法能否扩展到更大的集群。

### The results indicate that X.
**意思/用法：** 直接陈述结果所指向的结论；强度通常低于 *prove*. 类似：*The findings show/suggest that X.*
1. The results indicate that the new index reduces lookup time. — 结果表明新索引减少了查找时间。
2. The results indicate that most participants preferred the shorter version. — 结果表明大多数参与者更喜欢较短版本。

### It is worth noting that X.
**意思/用法：** 提醒读者注意一个相关事实；不要频繁用于每个段落开头。类似：*Note that X.*
1. It is worth noting that the baseline uses a different compiler. — 值得注意的是，基线使用了不同的编译器。
2. It is worth noting that no participants withdrew from the study. — 值得注意的是，没有参与者退出研究。

### One limitation of X is that Y.
**意思/用法：** 指出 X 的一个局限，并用 that 从句具体说明。类似：*A drawback of X is Y.*
1. One limitation of the model is that it requires labeled data. — 这个模型的一个局限是需要标注数据。
2. One limitation of the experiment is that it covers only one region. — 这个实验的一个局限是只覆盖一个地区。

### X remains an open question.
**意思/用法：** 表示 X 尚未解决或确认。类似：*It is still unclear whether X.*
1. Whether the trend generalizes remains an open question. — 这种趋势能否推广仍是一个悬而未决的问题。
2. The cause of the outage remains an open question. — 故障原因仍未确定。

### The key idea here is that X.
**意思/用法：** 突出解释中的核心观点。类似：*The main point is that X.*
1. The key idea here is that retries can amplify load. — 这里的关键点是重试可能放大负载。
2. The key idea here is that correlation does not establish causation. — 这里的核心思想是相关性不能证明因果关系。

### Let's walk through X.
**意思/用法：** 邀请对方按步骤查看或解释 X，语气自然、合作。类似：*Let's go over X.*
1. Let's walk through the setup first. — 我们先一步步看一下设置。
2. Let's walk through what happens after a timeout. — 我们来梳理一下超时后会发生什么。

### It turns out that X.
**意思/用法：** 引出后来发现的事实，常带有意外或纠正预期的意味。类似：*As it turned out, X.*
1. It turns out that the file was already in the cache. — 后来发现文件已经在缓存中了。
2. It turns out that both methods produce the same result. — 结果发现两种方法产生的结果相同。

### might as well + base verb
**意思/用法：** 表示在当前情况下某事是合理、方便的选择，常含“既然如此，不妨”。类似：*may as well + base verb.*
1. We might as well rerun the test while the machine is free. — 既然机器空着，我们不妨重跑一次测试。
2. You might as well ask her directly. — 你不妨直接问她。

## Useful

### X instead of Y
**意思/用法：** 用 X 替代 Y；instead of 后接名词或动名词。类似：*rather than Y.*
1. Use a queue instead of polling repeatedly. — 使用队列，而不是反复轮询。
2. We measured throughput instead of counting requests. — 我们测量了吞吐量，而不是只数请求数。

### X is in scope now
**意思/用法：** 表示 X 当前属于讨论、计划或工作范围。类似：*X is included in the current scope.*
1. Migration testing is in scope now. — 迁移测试现在在范围之内。
2. The user interface is not in scope for this phase. — 用户界面不属于这一阶段的范围。

### X is a property of Y, not of Z
**意思/用法：** 指出某属性归属于 Y，而非 Z。类似：*Y has property X; Z does not.*
1. Consistency is a property of the storage system, not of the client. — 一致性是存储系统的属性，不是客户端的属性。
2. This limit is a property of the account, not of the device. — 这个限制属于账户，不属于设备。

### The unit of work is X
**意思/用法：** 指明系统或分析中一次处理的基本工作单位。类似：*X is the basic work item.*
1. The unit of work is one batch, not one request. — 工作单位是一整个批次，而不是单个请求。
2. In this experiment, the unit of work is a participant session. — 在这个实验中，工作单位是一次参与者会话。

### X is split into A and B
**意思/用法：** 表示 X 被划分为 A、B 两部分；split into 强调分割结果。类似：*X consists of A and B.*
1. The pipeline is split into ingestion and validation. — 流水线分为摄取和验证两部分。
2. The score is split into accuracy and latency components. — 分数分为准确度和延迟两个部分。

### X alone is not proof, because Y also Z
**意思/用法：** 用 Y 的替代解释说明 X 本身不足以证明某结论。类似：*X by itself does not demonstrate Y.*
1. A faster run alone is not proof, because reduced logging also lowers overhead. — 单次运行更快并不能证明改进有效，因为减少日志也会降低开销。
2. A positive result alone is not proof, because random variation also produces positives. — 单个阳性结果不能单独作为证明，因为随机波动也会产生阳性结果。

### X ..., so no Y is required
**意思/用法：** 说明 X 带来的结果使 Y 不再必要。类似：*Because of X, we do not need Y.*
1. The token is refreshed automatically, so no manual reset is required. — 令牌会自动刷新，因此无需手动重置。
2. The API retries failed requests, so no extra retry loop is required. — API 会重试失败请求，因此不需要额外的重试循环。

### Have + object + verb
**意思/用法：** *have + 宾语 + 动词原形* 表示安排或要求某人做事；*have + 宾语 + 过去分词* 表示让某物被处理。类似：*get + object + to verb / have + object + past participle.*
1. I'll have the team review the patch. — 我会安排团队审查这个补丁。
2. We had the server restarted overnight. — 我们安排服务器在夜间重启了。

### Be worth + V-ing
**意思/用法：** 表示某事值得做；worth 后接名词或动名词，不接不定式。类似：*be worthwhile to do.*
1. This result is worth checking again. — 这个结果值得再核查一次。
2. The paper is worth reading for its evaluation method. — 这篇论文的评估方法值得一读。

### X is not complete until Y.
**意思/用法：** 表示直到 Y 发生，X 才算完成。类似：*X remains incomplete until Y.*
1. The migration is not complete until the checks pass. — 检查通过后，迁移才算完成。
2. A review is not complete until the author responds to the comments. — 作者回应意见后，审查才算完成。

### Before doing X, check whether Y.
**意思/用法：** 提醒先检查 Y，再做 X。类似：*Check Y before you do X.*
1. Before merging the patch, check whether the tests pass. — 合并补丁前，先检查测试是否通过。
2. Before deleting the cache, check whether another service uses it. — 删除缓存前，先确认是否有其他服务在使用它。

### X ..., so that Y can ... .
**意思/用法：** so that 引导目的，说明做 X 是为了让 Y 能够做某事。类似：*X in order that Y can ...*
1. Add a request ID so that we can trace failures. — 加上请求 ID，这样我们就能追踪故障。
2. Store the timestamp so that later analyses can align the events. — 保存时间戳，以便后续分析对齐事件。

### What remains is X.
**意思/用法：** 表示完成其他事项后，剩下要处理的是 X。类似：*The remaining task is X.*
1. What remains is to document the assumptions. — 剩下的工作是记录这些假设。
2. The data are clean; what remains is the final analysis. — 数据已经清理好，剩下的是最后的分析。

### X ..., rather than Y ... .
**意思/用法：** 对比两个行为或选择，强调前者而非后者。类似：*X instead of Y.*
1. We report the median, rather than averaging the measurements. — 我们报告中位数，而不是对测量值求平均。
2. The system queues requests rather than dropping them. — 系统会把请求排队，而不是丢弃它们。

### X cannot be ruled out.
**意思/用法：** 表示尚不能排除 X；常用于科学讨论，语气谨慎。类似：*X remains possible.*
1. A measurement error cannot be ruled out. — 目前还不能排除测量误差。
2. The effect of temperature cannot be ruled out. — 温度的影响尚不能排除。

### What happens if X?
**意思/用法：** 询问假设条件 X 下会发生什么；可用于讨论边界情况。类似：*What would happen if X?*
1. What happens if the queue reaches its limit? — 如果队列达到上限会怎样？
2. What happens if a worker fails halfway through? — 如果一个工作进程中途失败会怎样？

### wouldn't put it past someone to do something
**意思/用法：** 表示认为某人确实可能做某事，常暗示这种行为符合其一贯作风。类似：*would not be surprised if someone did ...*
1. I wouldn't put it past the vendor to change the API without notice. — 我觉得供应商确实可能不提前通知就改 API。
2. She wouldn't put it past him to spot the bug immediately. — 她觉得他确实可能马上就发现这个 bug。

### X takes a lot of effort but yields little Y.
**意思/用法：** 表示 X 很费力，但产出的 Y 很少。类似：*X is effort-intensive with little return.*
1. Manual labeling takes a lot of effort but yields little additional data. — 手工标注很费力，却只能多得到少量数据。
2. This optimization takes a lot of effort but yields little speedup. — 这项优化很费力，却几乎没有带来加速。

### notify X of Y
**意思/用法：** 正式表达“通知 X 有关 Y 的事”；被通知的人是宾语，信息用 of 引出。类似：*inform X about Y.*
1. Please notify the team of any schedule changes. — 如有日程变动，请通知团队。
2. The system notified users of the outage. — 系统通知了用户发生故障。

### X is spread across Y.
**意思/用法：** 表示 X 分散在多个 Y 中或跨越 Y。类似：*X is distributed across Y.*
1. The logs are spread across several machines. — 日志分散在多台机器上。
2. Responsibility is spread across three teams. — 职责由三个团队分担。

### Any comments on X?
**意思/用法：** 征求对 X 的意见；在会议、文档或评审中常用。类似：*Do you have any feedback on X?*
1. Any comments on the revised draft? — 对修改后的草稿有什么意见吗？
2. Any comments on how we should handle retries? — 对重试处理方式有什么建议吗？

## Specialized

### This is X kicking in before Y
**意思/用法：** 用口语化方式说明 X 在 Y 之前开始生效。类似：*X takes effect before Y.*
1. This is the rate limit kicking in before the queue fills. — 这是限流在队列填满前先起作用了。
2. This is the fallback kicking in before the primary service recovers. — 这是主服务恢复前备用方案先启动了。

### X must wait out Y rather than deadlock on Y
**意思/用法：** 强调 X 应等待 Y 完成，而不应因相互等待造成死锁。类似：*X should wait for Y to finish without blocking progress.*
1. The worker must wait out the lease rather than deadlock on the lock. — 工作进程必须等租约到期，而不是卡在锁上造成死锁。
2. The client should wait out the retry window rather than deadlock on a response. — 客户端应等待重试窗口结束，而不是因等待响应陷入死锁。

### Without X, Y can't tell whether A predates or postdates B
**意思/用法：** 说明缺少 X 时，Y 无法判断 A 与 B 的先后顺序。类似：*X is needed to establish whether A occurred before B.*
1. Without sequence numbers, the replica can't tell whether the update predates or postdates the snapshot. — 没有序列号，副本无法判断更新是在快照之前还是之后发生的。
2. Without timestamps, the monitor can't tell whether the alert predates or postdates the restart. — 没有时间戳，监控器无法判断告警是在重启之前还是之后出现的。

### X is consistent with what's documented in Y
**意思/用法：** 表示 X 与 Y 中记录的内容相符，但不一定表示 Y 已证明 X。类似：*X agrees with the account in Y.*
1. The observed delay is consistent with what's documented in the incident report. — 观察到的延迟与事故报告中的记录相符。
2. Her description is consistent with what's documented in the protocol. — 她的描述与协议中的记载一致。

### Instrument X, not Y
**意思/用法：** 指示对 X 进行仪器测量或插桩，而不是 Y。类似：*Measure X rather than Y.*
1. Instrument queue wait time, not just total request time. — 对队列等待时间进行插桩测量，而不只是测总请求时间。
2. Instrument the client path, not the dashboard. — 对客户端路径进行插桩，而不是仪表板。

### X is the binding constraint
**意思/用法：** 表示 X 是当前真正限制性能、规模或结果的约束。类似：*X is the limiting factor.*
1. Memory bandwidth is the binding constraint in this workload. — 在这个工作负载中，内存带宽是主要瓶颈。
2. Reviewer time is the binding constraint for the project. — 审稿人时间是这个项目的关键限制因素。

### Start with X and expand only if X justifies it
**意思/用法：** 先从 X 开始，只有证据或需要足够时才扩大范围。类似：*Begin with X; scale up when warranted.*
1. Start with one region and expand only if demand justifies it. — 先从一个区域开始，只有需求足够时才扩展。
2. Start with a simple model and expand only if the data justify it. — 先用简单模型，只有数据支持时才增加复杂度。

### X remains ... unless Y ... .
**意思/用法：** 表示除非 Y 发生，否则 X 仍保持某状态。类似：*X will continue to ... until Y.*
1. The feature remains disabled unless an administrator enables it. — 除非管理员启用，否则该功能会继续保持关闭。
2. The estimate remains provisional unless new evidence changes it. — 除非新证据改变结论，否则该估算仍属暂定。

### By the time X happens, Y has already happened.
**意思/用法：** 强调到 X 发生时，Y 已经先发生；常用过去完成时或现在完成时。类似：*Y happens before X.*
1. By the time the alert fires, the queue has already overflowed. — 告警触发时，队列其实已经溢出了。
2. By the time we arrived, the seminar had already started. — 我们到达时，研讨会已经开始了。

### The more X ..., the more Y ... .
**意思/用法：** 表示 X 增加时 Y 也随之增加；比较级结构常省略重复动词。类似：*As X increases, Y increases.*
1. The more threads we add, the more contention we see. — 增加的线程越多，观察到的竞争就越多。
2. The more clearly you define the question, the easier it is to answer. — 问题定义得越清楚，就越容易回答。

### X is refuted if Y ... .
**意思/用法：** 说明若观察到 Y，则 X 的主张被反驳；适用于可检验论断。类似：*Y would falsify X.*
1. The claim is refuted if the effect disappears in a controlled trial. — 如果效应在对照试验中消失，这个主张就被反驳。
2. The hypothesis is refuted if the predicted ordering is reversed. — 如果预测的排序相反，这个假设就被否定。

### X is bounded by A, not by B.
**意思/用法：** 明确 X 的上下界由 A 决定，而不是 B。类似：*A sets the bound on X.*
1. Throughput is bounded by disk bandwidth, not by CPU capacity. — 吞吐量受磁盘带宽限制，而不是 CPU 容量。
2. The estimate is bounded by the observed range, not by the theoretical maximum. — 这个估算的上界由观察范围决定，而非理论最大值。

### This discrepancy could be attributed to X.
**意思/用法：** 谨慎提出 X 可能是差异的原因；could 保留不确定性。类似：*X may account for the discrepancy.*
1. This discrepancy could be attributed to different sampling windows. — 这种差异可能是由不同的采样窗口造成的。
2. The mismatch could be attributed to rounding. — 这种不匹配可能源于舍入误差。

### No evidence was found that X.
**意思/用法：** 报告没有找到支持 X 的证据；不等于证明 X 一定为假。类似：*We found no evidence that X.*
1. No evidence was found that the treatment increased risk. — 没有发现该处理会增加风险的证据。
2. No evidence was found that the service lost any records. — 没有发现该服务丢失记录的证据。

### In contrast to X, Y.
**意思/用法：** 将 Y 与 X 对照，突出两者差异。类似：*Unlike X, Y ...*
1. In contrast to the baseline, the new version keeps latency stable under load. — 与基线相比，新版本在负载下保持了稳定的延迟。
2. In contrast to older studies, this analysis includes rural participants. — 与早期研究不同，这项分析纳入了农村参与者。

### X raises the possibility that Y.
**意思/用法：** 表示 X 使 Y 成为一种可能解释，但尚未证实。类似：*X suggests that Y might be possible.*
1. The spike raises the possibility that a retry storm occurred. — 这次峰值让人怀疑可能发生了重试风暴。
2. The survey raises the possibility that expectations changed. — 这项调查提出了一种可能：人们的预期发生了变化。

### Suppose we have X.
**意思/用法：** 引入假设情境 X，以便推演或举例。类似：*Assume that X.*
1. Suppose we have two workers competing for one lock. — 假设有两个工作进程竞争同一把锁。
2. Suppose we have a sample with several missing values. — 假设我们的样本中有几个缺失值。
