# 进阶专题：LLM 上下文缓存与推理系统

归属主计划：[AI Engineering 与 Agent 系统开发](AI-Engineering-Agent-Learning-Plan.md)。
整理日期：2026-11-18（America/New_York）
目标：在理解 Agent 应用主线后，深入上下文管理、缓存层级和模型架构的系统取舍。
状态：可选进阶专题，尚未执行；资料登记、阅读或听过讲解均不代表已掌握。

## 1. 与主线的关系

本文件是主计划的进阶专题材料，不单独构成一条学习进度或学习记录。主线的模块 1（模型调用）、3（Agent loop）、5（上下文工程）是先修；RAG 的基本流程按需复习模块 6。

上下文压缩、RAG 和 harness 基础仍以主计划对应模块为唯一讲解主线。本专题只在必要处回顾这些概念，进一步学习 Claude Code 可观察到的上下文行为、Prompt cache 与 KV cache 的区别、缓存测量，以及 MoE/MLA。

- 每次只选一个具体知识点；先讲解和答疑，只有学习者明确要求后才测试。
- 沿用主计划的 [AI Mastery](../mastery.md) 与 [AI Session Log](../session-log.md)，不另建重复 tracker。
- 阅读入口不代表已读或已掌握；进度只依据实际学习和评估证据更新。
- 仓库保存链接与自制笔记，不复制第三方教材全文。

## 2. 学习资料

| 编号 | 资料 | 用途 |
|---|---|---|
| S9 | [AI Engineering by Chip Huyen（Google Drive）](https://drive.google.com/file/d/15Pwt3CEDpGdzp7lwzjKyxRQpAmUVsBRq/view) | 第 5、6、9 章：提示、上下文构建、RAG/Agent 与推理优化。 |
| S10 | [AI Systems Performance Engineering（Google Drive）](https://drive.google.com/file/d/175CT7Ev1RHGyy8BLY9XBc5mQR3vXdLS_/view) · [O'Reilly](https://www.oreilly.com/library/view/ai-systems-performance/9798341627772/) · [配套代码](https://github.com/cfregly/ai-performance-engineering) | KV cache、Prefix sharing/reuse、专家并行及 MLA/FlashMLA 的系统实现与性能视角；按实际版本目录定位相关小节。 |
| S11 | [Claude Code context management](https://code.claude.com/docs/en/claude-code-on-the-web) | Claude Code 的上下文命令和自动压缩；注意页面所述 cloud session 行为不一定适用于本地 CLI/IDE。 |
| S12 | [Anthropic Prompt Caching](https://platform.claude.com/docs/en/build-with-claude/prompt-caching) · [OpenAI Prompt Caching](https://developers.openai.com/api/docs/guides/prompt-caching) | 对照平台的前缀匹配、缓存边界/有效期与可观测指标，按实际使用的 API 核对当前规范。 |
| S13 | [DeepSeek-V2 论文](https://arxiv.org/abs/2405.04434) · [DeepSeekMoE 论文](https://arxiv.org/abs/2401.06066) | MLA、DeepSeekMoE 的一手资料；阅读时区分联合系统实验与单项技术效果。 |
| S2 | [Anthropic — Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) | 作为上下文组织和长程 Agent 的桥接阅读；概念基础仍归主计划模块 5。 |

## 3. 专题路线

完成先修后按顺序学习。每行可以拆成多个单知识点；一次只处理一个。

| 顺序 | 知识点 | 阅读入口 | 练习与完成证据 |
|---|---|---|---|
| 1 | Claude Code 的上下文管理行为 | S11；必要时回看主计划模块 5 | 区分上下文查看、手动压缩、自动压缩和清空会话的作用；指出哪些是文档明确行为，哪些属于实现细节未知。 |
| 2 | Prompt cache 与 KV cache 分别缓存什么 | S10、S12 | 用分层图说明 API 前缀缓存与模型推理 KV 状态所在位置、作用和差异。 |
| 3 | 怎样测量并改善 prompt-cache 命中 | S12 | 固定系统提示/工具定义，改变请求后缀；记录缓存 token、未缓存 token、延迟和费用，并解释一次不命中的可能原因。 |
| 4 | MoE 的路由、激活参数与专家并行 | S10、S13 DeepSeekMoE | 说明总参数、每 token 激活参数、设备通信与服务成本并非同一个量；画出 token 路由示意。 |
| 5 | MLA 如何压缩注意力 KV 表示 | S10、S13 DeepSeek-V2 | 说明 MLA 的模型层机制及其对 KV cache 的影响；区分它与 harness 对话摘要。 |
| 6 | 长时 coding agent 的端到端设计 | S9、S10–S13；结合主计划模块 4–6、9 | 设计按需加载/摘要/检索策略与稳定缓存前缀，并说明 MoE/MLA 可改善及无法解决的瓶颈。 |

### 完成标准

能解释机制、在新案例中判断其所在层次，并说明一个关键代价或限制。缓存实验需依据 API 实际返回的 usage 指标，而不是只看响应快慢；MoE/MLA 的性能结论需注明比较对象和实验范围。

## 4. 建议起点

可以从“Prompt cache 与 KV cache 分别缓存什么”开始。它只是建议起点，不代表已有学习或评估证据；学习者可以指定其他知识点。
