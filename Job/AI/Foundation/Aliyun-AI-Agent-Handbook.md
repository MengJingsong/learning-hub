# Aliyun AI Agent Handbook 阅读地图

**资料类型：** 外部开源手册  
**维护方：** 阿里云与社区贡献者  
**许可：** 网站标注 Apache-2.0  
**核对日期：** 2026-11-12

## 原始资料

- [AI Agent Handbook 首页](https://aliyun.github.io/ai-agent-handbook/)
- [全书目录](https://aliyun.github.io/ai-agent-handbook/contents.html)
- [GitHub 共建入口](https://github.com/alibaba/ai-agent-handbook)

手册首页介绍其目标是帮助读者理解企业级 Agent 如何从原型走向生产。网站目录显示全书有 30 章、7 个篇章，并持续更新；具体内容以在线目录为准。

## 知识地图

| 篇章 | 章节 | 主要主题 |
|---|---:|---|
| 架构篇 Architecture | 1–2 | AI 原生应用阶段；Agentic Application 参考架构 |
| 构建篇 Build | 3–6 | Harness；任务编排与长程推进；上下文、状态和可复用能力资产；受控行动与验证反馈 |
| 运行篇 Run | 7–12 | 运行时与沙箱；状态存储；AI 网关和路由；异步任务；多 Agent 协作；分布式通信 |
| 治理篇 Govern | 13–16 | 可观测性；安全；AI 资产管理；行为生成与质量验证 |
| 调优篇 Optimize | 17–24 | 模型调优；Agent 调优；轨迹数据；运行时数据处理；黄金数据集；Badcase；受控自进化；边缘运行时与全球优化 |
| 实践篇 Practice | 25–29 | 研发效能；设计工程；运维、安全和企业 IT；客户、销售与运营；多 Agent 基础设施实践 |
| 总结与展望 Outlook | 30 | 从 Agentic Application 到 Agentic OS |

此表依据网站目录整理，反映章节主题，不代替章节正文。

## 随 Foundation 主线阅读

[主学习计划](AI-Engineering-Agent-Learning-Plan.md) 决定授课顺序。第 3–6 章用于构建 Harness，第 7、10 章用于解释运行时如何承载长任务。每次选其中一个小节，围绕表中的一个问题展开。示例与验收方式由 learning-hub 课程设计，引用观点时回到手册正文。

| 手册章节 | 对应模块与阅读重点 | 观察证据或选读目的 |
|---|---|---|
| 1–2 架构 | 导论选读；理解应用、运行和治理的分工 | 画出模型、Harness、Runtime、Sandbox 的责任边界 |
| [3 构建方式](https://aliyun.github.io/ai-agent-handbook/build/chapter-03.html) | 模块 1 后读 §3.1.1；模块 3 后回读 §3.1.2；§3.1.3 比较构建入口 | 识别同一任务由谁决定下一步、授权和验证 |
| [4 任务](https://aliyun.github.io/ai-agent-handbook/build/chapter-04.html) | 3、4、8；§4.2.1–2 外置计划和阶段验收；§4.4.1 异步续行；§4.3.4 留到协作选学 | 从执行记录区分成功、耗尽预算和等待；说明父任务如何验收子结果 |
| [5 信息](https://aliyun.github.io/ai-agent-handbook/build/chapter-05.html) | 5、6、7、10；§5.1 组装上下文，§5.2 卸载和压缩；按需读 Workspace、Memory 与 Skill | 原始事实有保存位置，压缩后还能核对目标与引用 |
| [6 行动](https://aliyun.github.io/ai-agent-handbook/build/chapter-06.html) | 2、8、9；§6.1.3 行动边界，§6.2.2–3 工具设计与发现，§6.6.1 执行轨迹 | 定位实际执行身份、审批对象、工具结果和环境中的完成证据 |
| [7 沙箱](https://aliyun.github.io/ai-agent-handbook/run/chapter-07.html)、8 状态存储 | 7、8；重点读 §7.1.1，再按需选读第 8 章 | 区分持久工作区与临时资源，说明等待期间哪些资源可以释放 |
| 9 网关、[10 异步任务](https://aliyun.github.io/ai-agent-handbook/run/chapter-10.html)、11–12 协作与通信 | 8 必读 §10.1.1；网关、协作与通信在 9 后选读 | 同一任务在新会话恢复；分析重复交付、路由或协作开销 |
| 13–16 观测、安全、资产、验证 | 2、8、9；按工具身份、事件追踪、能力版本、结果验证选小节 | 能以失败轨迹定位责任，以外部事实验证结果 |
| 17–24 调优 | 9 后优先选读 19 轨迹、21 黄金数据集、22 Badcase；模型调优、受控自进化和边缘运行按需回查 | 从一次失败生成可重复的回归案例 |
| 25–30 实践与展望 | 完成综合项目后，选一个研发或运维案例；30 为展望 | 对照业务契约、失败模式和可观测证据，说明哪些结论可迁移 |

讲解时把专业英文放回原句和技术情境中。跨会话续学使用 [AI Session Log](../session-log.md)，记录知识点、手册小节、实际讲解和下一步；评估证据进入 [AI Mastery](../mastery.md)。
