# Learning Hub Router

Default repository: `MengJingsong/learning-hub`. All slash-prefixed paths below are relative to the repository root.

## Category routing

1. Follow an explicit category selection or clear task request.
2. Otherwise continue the active category in this conversation.
3. With no active category, infer the learning objective: language → English; computer-science concepts → CS; interview practice → interview.
4. If the objective is genuinely ambiguous, ask one brief clarification. Do not treat quoted code or an English technical question as vocabulary lookup merely because it contains quotes or English.

| Selection | Read first | Then read |
|---|---|---|
| `英语模式`, `English模式`, standalone `english` | `/english/english-study/README.md` | `/english/instructions/router.md` |
| `CS模式`, `计算机模式`, standalone `CS` | `/CS/README.md` | `/CS/instructions/router.md` |
| `面试模式`, standalone `interview` | `/interview/README.md` | `/interview/instructions/router.md` |

`知识点复习` explicitly selects CS and its book-based review workflow; read `/CS/README.md`, `/CS/instructions/router.md`, and `/CS/instructions/book-review.md`. This specific command takes precedence over generic review routing, including when another category is active. A book already named in the request need not be requested again.

Legacy commands `查词模式`, `学习模式`, `复习模式`, `测试模式`, `听力模式`, and `整理模式` select English and activate its matching mode when no category is active. Within English they retain their existing meaning. Within CS or interview, generic learning/review/testing requests follow that category's router; English-specific lookup/listening/inbox commands explicitly select English.

## Persistence and overrides

Category and task-mode state are scoped to this conversation. An explicit category switch clears the prior category's task mode. `默认模式` clears both category and task mode and resumes intent routing. Explicit requests for another task override the active selection for that request without silently changing the persistent selection.

Requests to manage the repository are repository tasks; do not proofread them or run a learning exercise. Do not apply English-only fallback proofreading to a clear CS or interview question.

## Boundaries

- English: wording, translation, pronunciation, technical language.
- CS: mechanisms, theory, implementation, research, and engineering tradeoffs.
- Interview: job-oriented retrieval, coding exercises, timed reasoning, system-design answers, and behavioral practice.
- For a mixed request, follow the primary objective and consult the second category only when needed. Keep learning evidence in the category actually assessed.
- Read only the relevant instructions and materials. Never claim a read or write succeeded without tool confirmation.
- Learning state is evidence-based; do not infer mastery from explanations or migration.
- Listening Mode outputs only the English passages intended to be heard, with no headings, translations, explanations, or commentary.
