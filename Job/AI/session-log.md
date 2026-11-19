# AI Session Log

## 2026-11-19 — Foundation：Instructions vs. External Data

- 知识点 ID：`ae.model-io.instructions-vs-external-data`。
- 阶段：讲解完成；本次学习结束；未测试、未评估。
- 本次范围：Instruction 与 External Data 的定义和区别；外部资料中的命令式文本不因语气而获得指令权威性；Prompt Injection；结构化来源、数据边界标记与 Runtime 权限隔离；用户委托外部文档执行特定任务的授权边界。
- 核心要点：外部数据可以包含指令，但默认仍是待处理的数据；XML/Markdown 分隔符有助于表达边界但不是安全机制；安全执行不能只依赖 Prompt，还需要最小权限、参数校验、明确授权及必要的人工审批。
- 案例：AI 学习助手读取 GitHub README，提取技术知识但不执行文档中要求泄露提示词或扩大权限的恶意文本。
- 英语融入：`untrusted external data`（不可信外部数据）、`data isolation`（数据隔离）、`prompt injection`（提示注入）、`least privilege`（最小权限）、`privilege escalation`（权限提升）、`explicit authorization`（明确授权）。
- 能力证据：本次为讲解，学习者未要求测试；没有独立作答或迁移评估证据，不更新 mastery，不推断已掌握。
- 剩余疑问：未记录；本次学习结束。
- 下一步：下次继续时学习模块 1 的 Token 与 Context Window；仍按单知识点讲解与答疑，不主动测试。

## 2026-11-19 — Foundation：Message Roles 与消息来源

- 知识点 ID：`ae.model-io.message-roles`。
- 阶段：讲解与答疑；未测试。
- 本次范围：结构化消息中的 role 与 content；system、developer、user、assistant、tool 五种角色；消息来源与指令权威性的区别；Chat Completions 的 messages 与 Responses API 的 input/output Items 表示差异。
- 核心要点：role 标识消息来源/类型，content 承载消息内容；不能仅凭 content 的命令式语气改变消息来源或权威性；assistant 可生成工具调用请求，tool 结果来自外部程序，二者不可混为一谈。
- 案例：AI 学习助手读取技术资料时，区分开发者规则、用户问题、assistant 的工具调用和 GitHub 工具返回的文档内容。
- 英语融入：`message role`（消息角色）、`message source`（消息来源）、`instruction hierarchy`（指令层级）、`structured message format`（结构化消息格式）。
- 能力证据：本次为讲解，没有独立作答或迁移评估；不更新 mastery，不推断已掌握。
- 剩余疑问：等待学习者提问；本次不进入 token、context window 或结构化输出。
- 来源：OpenAI Harmony Response Format；OpenAI Text Generation Guide；OpenAI Model Spec。
- 下一步：围绕 message roles 与消息来源答疑；学习者明确要求进入下一点后，再学习指令与外部数据的区分。

## 2026-11-18 — Foundation 重新开始与教材迁移

- 当前路线：按学习者要求从模块 1 开始。本次对话已介绍 `ae.model-io.message-roles`（消息角色与来源）；阶段为讲解与答疑，尚无评估证据。
- 手册原课程 checkpoint 为“计划已建立，正文尚未开始”。本次整合课程目录，手册学习按 Foundation 主线进行。此前工具调用讲解保留在下方作为历史记录。
- 续学位置：模块 1 消息角色；学习者要求进入下一点后学习指令与外部数据。明确要求从头开始时回到模块 1 首课。

## 2026-11-18 — AI engineering：Tool call request 与 Execution（续学）

- 知识点 ID：`ae.tool-calling.request-vs-execution`。
- 阶段：继续讲解与答疑；未测试。
- 本次范围：用 learning-hub 只读读取 README 的过程区分模型提出调用请求、Runtime 实际执行、工具返回结果，以及根据返回结果确认完成。
- 核心要点：模型输出的 tool call 是结构化请求，不是工具已执行的证据；Runtime 负责解析、授权/校验、执行并捕获结果；应根据工具实际返回判断成功、失败或结果不足。
- 例子：GitHub 工具读取根 README 后返回了文件内容，才能确认读取成功；如果只生成了 fetch 请求，或返回 404，就不能报告“已读到”。
- 英语融入：`issue a tool call`（发出工具调用）、`execute the request`（执行请求）、`verify the result`（核实结果）。
- 能力证据：尚无独立作答或新情境迁移证据；不更新 mastery，不推断已掌握。
- 剩余疑问：等待学习者提问或明确要求测试；本次不进入参数 schema 等下一知识点。
- 来源：学习计划 S1 Anthropic, “Building effective agents” Appendix 2（tool use block）；以及实际 GitHub README 读取返回结果。
- 下一步：继续围绕本点答疑；仅在用户明确要求后测试，充分理解后等用户明确要求进入下一点再推进。

## 2026-10-28 — AI engineering：Tool call request 与 Execution

- 知识点 ID：`ae.tool-calling.request-vs-execution`。
- 阶段：开始讲解与答疑，等待学习者反馈；未测试。
- 选题依据：学习者已讨论 Workflow、Agent 和 CoT；本点连接模型决策与外部操作，无需先掌握框架。
- 本次讲解范围：Model 产生 Tool call request，Runtime 验证并执行 Tool，将 Tool result 返回给 Model；区分请求、执行与成功确认，以 learning-hub 读取文件为例。
- 能力证据：尚无该点独立作答或实践证据；不更新 mastery，不推断已掌握。
- 剩余疑问：待学习者反馈，不能预先判断具体薄弱项。
- 下一步：围绕本点答疑；仅在用户明确要求后测试，用户明确要求进入下一点后再推进。
