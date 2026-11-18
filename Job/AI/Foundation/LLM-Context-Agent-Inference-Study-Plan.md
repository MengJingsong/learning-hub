# LLM 上下文、Agent 与推理系统：学习计划

整理日期：2026-11-18（America/New_York）
目标：结合应用工程与模型服务系统两个视角，理解上下文选择与压缩、RAG、Agent harness、提示缓存、KV cache、MoE 和 MLA 的机制、边界与取舍。
状态：学习计划，尚未执行；资源登记、阅读或听过讲解均不代表已掌握。

## 1. 学习约定

- 每次只学习一个具体知识点，先解释、举例和答疑；只有学习者明确要求后才测试。
- 不按日历赶进度。每个单元通过可观察的解释或应用练习后，再由学习者决定是否进入下一点。
- 开始前读取 [AI 学习记录](../mastery.md) 与 [AI Session Log](../session-log.md)，确认先修和未完成主题；讲解与掌握证据分开记录。
- 中文讲解，保留常用 English 技术术语。章节是阅读入口，不表示已读或已掌握。
- 只保存书目链接和自制笔记，不把第三方教材全文提交到仓库。

## 2. 学习资料

| ID | 资料 | 主要用途 |
|---|---|---|
| S1 | [AI Engineering by Chip Huyen（Google Drive）](https://drive.google.com/file/d/15Pwt3CEDpGdzp7lwzjKyxRQpAmUVsBRq/view) | AI 应用工程：prompt engineering、上下文构建、RAG、agentic pattern 与推理优化。重点参考第 5、6、9 章；第 6 章涉及 RAG 与 agentic 上下文构建，第 9 章讨论模型及推理服务层优化。 |
| S2 | [AI Systems Performance Engineering（Google Drive）](https://drive.google.com/file/d/175CT7Ev1RHGyy8BLY9XBc5mQR3vXdLS_/view) | 推理系统和模型执行：KV cache 管理、prefix sharing/reuse、MoE 专家并行、MLA/FlashMLA 等目录主题。配合[官方书籍页面](https://www.oreilly.com/library/view/ai-systems-performance/9798341627772/)和[作者配套仓库](https://github.com/cfregly/ai-performance-engineering)使用；小节位置按实际版本目录定位。 |
| S3 | [AI Engineering 与 Agent 系统开发计划](AI-Engineering-Agent-Learning-Plan.md) | 已有应用层主线；本计划补足推理缓存与模型架构的系统视角，避免重复维护 Agent 基础内容。 |
| S4 | [AI Infrastructure 资料索引](../Infrastructure/Resources.md) | CUDA、推理服务与系统性能的延伸资料。 |
| S5 | [Claude Code context management](https://code.claude.com/docs/en/claude-code-on-the-web) | 官方命令与自动压缩说明；所引页面描述 cloud sessions，使用时注意云端与本地 CLI/IDE 的差异。 |
| S6 | [Anthropic Prompt Caching](https://platform.claude.com/docs/en/build-with-claude/prompt-caching)；[OpenAI Prompt Caching](https://developers.openai.com/api/docs/guides/prompt-caching) | 对照前缀缓存、缓存边界/有效期及命中 token 指标；实现细节按实际服务商文档确认。 |
| S7 | [DeepSeek-V2 论文](https://arxiv.org/abs/2405.04434)；[DeepSeekMoE 论文](https://arxiv.org/abs/2401.06066) | 用原始研究理解 MLA 与 DeepSeekMoE 的机制；将论文报告的整套系统结果与单项技术效果区分。 |

个人 Drive 文件供本人阅读使用；仓库只链接资料，不表示其授权公开再分发。

## 3. 学习路线

按先修逐项推进。表中每行是一个学习单元；单元内各项是独立知识点，一次学习只选一个。

| 顺序 | 单元 / 知识点 | 阅读入口 | 练习与完成证据 |
|---|---|---|---|
| 1 | **系统分层**：模型、harness、推理服务分别负责什么 | S1 第 2、6、9 章；S2 总体架构与目录 | 画出“模型生成 → harness 组装上下文并执行工具 → 推理服务计算”的数据流；能把 MoE/MLA 与上下文压缩放到正确层次。 |
| 2 | **上下文窗口与上下文工程**：token 预算、近期对话、摘要、按需加载 | S1 第 5–6 章；S3 模块 5；S5 Claude Code context management 文档 | 给长任务列出必须保留的约束、可摘要的信息和可按需检索的细节；解释压缩可能损失什么。 |
| 3 | **RAG 与向量检索**：切块、embedding、向量数据库、重排及引用 | S1 第 6 章；S3 模块 6 | 为一个问题标注“查询 → 命中片段 → 生成答案”的来源链；区分语义召回和重要性/权限元数据的作用。 |
| 4 | **Agent harness 与上下文管理**：工具循环、检索、摘要、恢复 | S1 第 6 章及 Agent 章节；S3 模块 2–5、7–9 | 为 coding agent 画出 harness 与模型的职责边界；说明压缩后的信息如何与文件检索、状态记录配合。 |
| 5 | **Prompt cache 与 KV cache**：缓存对象、前缀复用、命中率影响因素 | S1 第 5、9 章；S2 KV Cache Management、KV Cache Reuse and Prefix Sharing（目录列于第 18 章）；S6 两家 API 的 Prompt Caching 文档 | 对比两类缓存各自缓存什么；设计固定前缀、动态内容靠后的请求；分别读取平台返回的 cached-token 用量，比较缓存命中、未命中时的输入 token、延迟和费用；解释摘要改写为何可能影响前缀复用。 |
| 6 | **MoE**：路由器、专家、激活参数与专家并行成本 | S2 中 MoE / Expert Parallelism 相关章节或小节，按实际版本目录定位；S7 DeepSeekMoE 与 DeepSeek-V2 论文 | 解释总参数量、每 token 激活参数量与实际显存/通信成本的区别；画出 token 路由到专家的示意。 |
| 7 | **MLA 与 KV cache 表示**：潜在表示如何减少缓存负担 | S2 第 18 章 FlashMLA / Multi-Head Latent Attention 相关内容；S7 DeepSeek-V2 论文 | 解释 MLA 优化的对象及其与 KV cache 的关系；与 harness 的对话压缩比较，指出两者发生在不同层。 |
| 8 | **综合设计**：从对话策略到模型/服务优化 | S1 第 9 章；S2 KV cache 和模型执行相关章节 | 为长时 coding agent 写一页设计说明：哪些上下文保留、摘要或检索，哪些前缀保持稳定，何时选择更强模型，MoE/MLA 能缓解哪些资源限制；列出尚未解决的问题。 |

### 单知识点完成标准

能用自己的话说明机制，能在新例子中正确判断其所在层次，并能说出至少一个取舍或失效情形。练习或测试证据按 AI 学习记录规则登记；仅阅读不作为掌握证据。

## 4. 建议起点

结合本次对话，建议先学“**Prompt cache 和 KV cache 分别缓存什么**”，之后按先修推进。这只是建议起点，不视为已完成或已掌握；学习者也可指定其他单元。

## 5. 继续学习时可用的请求

- `AI模式，按 LLM 上下文、Agent 与推理系统计划，从 AI 学习记录确认先修后，一次只讲一个知识点；先从 prompt cache 和 KV cache 的区别开始，讲解并答疑，等我要求后再测试。`
- `继续上次的 AI 学习。先读计划和 session log，接着当前未完成的一个知识点。`
- `测试我刚学的知识点，一次一题，先不要给答案；按实际表现总结，不要从听过讲解推断掌握。`
