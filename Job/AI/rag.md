# RAG 与知识检索

本专题展开 [Agent 学习计划的模块 6](../CS/study-materials/ai-engineering-agent-learning-plan.md#模块-6rag-与知识检索)（`ae.rag`）。先修是 `ae.model-io`、`ae.context` 和基本搜索概念。每次选一个子知识点，先理解机制和取舍，再用新场景检验。清单用于安排学习，掌握程度以独立作答或实践证据为准。

## 待学清单

- [ ] [文档与索引](#文档与索引)：`ae.rag.pipeline`、`ae.rag.chunking`、`ae.rag.index-lifecycle`
- [ ] [检索与重排](#检索与重排)：`ae.rag.retrieval`、`ae.rag.hybrid-search`、`ae.rag.reranking`
- [ ] [基于证据生成](#基于证据生成)：`ae.rag.grounding`、`ae.rag.evidence-conflicts`
- [ ] [评估与排错](#评估与排错)：`ae.rag.retrieval-evaluation`、`ae.rag.answer-evaluation`、`ae.rag.failure-analysis`
- [ ] [Agentic RAG](#agentic-rag)：`ae.rag.agentic-retrieval`、`ae.rag.retrieval-budget`

## 文档与索引

- **链路（`ae.rag.pipeline`）**。离线解析文档、切分并建索引。在线根据问题检索证据、选择上下文并生成回答。RAG 可以使用关键词索引，外部知识可随索引更新。
- **切分（`ae.rag.chunking`）**。比较固定长度、按标题或段落切分和重叠窗口。切得太细会拆开规则与例外，切得太粗会带入无关内容。
- **索引生命周期（`ae.rag.index-lifecycle`）**。保留文档 ID、章节或页码、版本、生效日期和访问权限。明确更新、删除和重新索引后哪些版本仍能被哪些用户检索。

**面试题**　退款规则和例外条件分在相邻两段。如何切分以保留两者的关系？新版发布后，怎样让旧版退出默认检索，同时支持按订单日期查询历史政策？

**掌握标准**　能画出离线和在线两段链路，给出一种切分策略及其缺点，并解释如何验证版本更新和权限过滤。

资料：[RAG 原始论文](https://arxiv.org/abs/2005.11401) · [Microsoft Learn：RAG 架构](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview) · [Microsoft Learn：分块与元数据](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/rag/rag-enrichment-phase)

## 检索与重排

- **候选检索（`ae.rag.retrieval`）**。BM25 基于词项匹配与统计打分，适合错误码、型号和专有名词。向量检索通过 embedding 相似度找语义相近的表达。
- **混合检索（`ae.rag.hybrid-search`）**。两路各取候选，再用 RRF（Reciprocal Rank Fusion）等方法融合。RRF 根据各路名次计分，可以避免直接比较不同量纲的原始分数。
- **重排（`ae.rag.reranking`）**。用 cross-encoder 等方法细评查询与候选的相关性，再选少量片段给模型。初始候选数影响召回和延迟，最终片段数影响上下文预算。重排只能处理已召回的候选。

**面试题**　用户分别输入错误码和故障描述，你怎么设计检索？正确文档在候选集排第 30，但最终只送前 5 条给模型。若正确文档根本没进候选集，诊断会怎样改变？

**掌握标准**　能用具体查询解释三种检索方式的取舍，区分候选深度和上下文条数，并根据候选和最终排名决定先调哪个阶段。

资料：[Microsoft Learn：混合检索](https://learn.microsoft.com/en-us/azure/search/hybrid-search-overview) · [Microsoft Learn：候选检索与重排](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/rag/rag-information-retrieval)

## 基于证据生成

- **证据与引用（`ae.rag.grounding`）**。把片段和来源标识一起交给模型，让读者能追溯关键主张。检查引用是否真实存在，以及引用片段是否支持该主张。
- **证据不足或冲突（`ae.rag.evidence-conflicts`）**。按已定义的来源优先级和适用日期选择证据。缺少决定性信息时，说明不足或询问必要信息。

**面试题**　检索到了两版退款政策，用户问的是上月订单。你需要查明哪些适用条件？如果订单日期未知或两份来源冲突，系统怎么回答？

**掌握标准**　能为同一问题给出证据充分、缺失和冲突三种情况下的预期输出，并检查每条关键结论能否由引用支持。

资料：[Microsoft Learn：RAG 与答案依据](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview) · [Ragas：评估指标](https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/)

## 评估与排错

- **检索评估（`ae.rag.retrieval-evaluation`）**。对标注了相关证据的查询，Recall@K 衡量前 K 条找回的相关证据占比，nDCG@K 衡量高相关证据是否排在前面。可分别记录候选阶段和最终排序的结果。
- **答案评估（`ae.rag.answer-evaluation`）**。分别检查答案正确性、证据忠实度（faithfulness）和引用是否支持主张。准确复述一份过期政策，可以忠实于证据却答错业务问题。
- **失败定位（`ae.rag.failure-analysis`）**。依次核对正确版本是否入库、是否进入候选、是否通过重排和上下文筛选，以及模型是否正确使用了证据。把已知正确证据直接传给模型，可以辅助判断生成环节能否处理该案例。

**面试题**　客服 Agent 引用了过期退款政策。你会查看哪些中间结果？怎么构建回归集来判断修复是否有效？

**掌握标准**　能根据一次失败的索引、候选、重排和上下文记录，指出最早出错的环节。能为新旧政策并存、订单跨生效日期、无可用证据设计回归用例，并给出检索和答案各自的判定标准。

资料：[Microsoft Learn：检索阶段](https://learn.microsoft.com/en-us/azure/architecture/ai-ml/guide/rag/rag-information-retrieval) · [Ragas：评估指标](https://docs.ragas.io/en/stable/concepts/metrics/available_metrics/)

## Agentic RAG

- **检索控制（`ae.rag.agentic-retrieval`）**。两步 RAG 由程序固定先检索再生成。Agentic RAG 可让模型按需决定是否检索、选择数据源、改写查询、拆分问题或补查。比较两者的任务成功率、延迟和可预测性。
- **停止条件（`ae.rag.retrieval-budget`）**。设定证据充分的条件，以及检索次数、耗时或成本预算。连续查询没有增加有效证据时停止，保留来源和检索轨迹供评估。

**面试题**　“这个订单能不能退？”可能需要同时查订单记录和政策。哪些查询可以由程序固定执行？哪些要根据前一步结果决定？什么时候应停止补查或向用户提问？

**掌握标准**　能为同一场景设计两步 RAG 基线和按需检索版本，说明后者在什么输入下值得增加调用，并定义停止条件和对比指标。

资料：[LangChain：两步 RAG 与按需检索](https://docs.langchain.com/oss/python/deepagents/retrieval)
