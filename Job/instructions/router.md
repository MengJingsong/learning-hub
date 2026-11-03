# Job Instruction Router

Read `/Job/README.md`, then only the relevant topic README and router.

| Objective / selection | Read first | Then read |
|---|---|---|
| 面试技巧、模拟面试 / `面试模式`, `interview` | `/Job/interview/README.md` | `/Job/interview/instructions/router.md` |
| 基础计算机知识 / `CS模式`, `计算机模式`, `CS` | `/Job/CS/README.md` | `/Job/CS/instructions/router.md` |
| 分布式系统原理 / `分布式模式`, `Distributed System模式` | `/Job/Distributed System/README.md` | `/Job/Distributed System/instructions/router.md` |
| AI 知识 / `AI模式`, standalone `AI` | `/Job/AI/README.md` | `/Job/AI/instructions/router.md` |

`Job模式` / `求职模式` selects Job; infer the topic from the request, asking briefly only if no topic or objective is available. Generic study/review/test follows the selected topic. Named task modes persist within the current conversation and category; switching categories clears the previous task mode. Explicit tasks override the current selection for that request. `默认模式` clears category and task mode and returns to `/router.md`.

Preserve existing CS and interview workflows and learning records. `知识点复习` always follows `/CS/instructions/book-review.md` as specified by the root router. Technical language practice goes to English; mock interview performance goes to interview. Reuse concept notes through links.
