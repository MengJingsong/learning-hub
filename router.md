# Learning Hub Router

Default repository: `MengJingsong/learning-hub`. All slash-prefixed paths below are relative to the repository root.

## Category routing

1. Follow an explicit category selection or clear task request.
2. Otherwise continue the active category in this conversation.
3. With no active category, infer the learning objective: language → English; computer-science concepts → CS; interview practice → interview; distributed-system concepts → Distributed System; AI concepts → AI; general job preparation and career planning/development → Job.
4. If the objective is genuinely ambiguous, ask one brief clarification. Do not treat quoted code or an English technical question as vocabulary lookup merely because it contains quotes or English.

| Selection | Read first | Then read |
|---|---|---|
| `英语模式`, `English模式`, standalone `english` | `/english/english-study/README.md` | `/english/instructions/router.md` |
| `CS模式`, `计算机模式`, standalone `CS` | `/Job/CS/README.md` | `/Job/CS/instructions/router.md` |
| `面试模式`, standalone `interview` | `/Job/interview/README.md` | `/Job/interview/instructions/router.md` |
| 职业规划、职业发展、career planning/development / `职业规划模式` | `/Job/README.md` | `/Job/instructions/router.md` → `/Job/career-development.md` |
| `Job模式`, `求职模式`, standalone `Job` | `/Job/README.md` | `/Job/instructions/router.md` |
| `分布式模式`, `Distributed System模式` | `/Job/Distributed System/README.md` | `/Job/Distributed System/instructions/router.md` |
| `AI模式`, standalone `AI` | `/Job/AI/README.md` | `/Job/AI/instructions/router.md` |

`知识点复习` explicitly selects CS and its book-based review workflow; read `/Job/CS/README.md`, `/Job/CS/instructions/router.md`, and `/Job/CS/instructions/book-review.md`. This specific command takes precedence over generic review routing, including when another category is active. A book already named in the request need not be requested again.

`翻译模式` is an exact alias of `查词模式` in all routing and mode behavior; both activate `/english/instructions/lookup.md`.

Legacy commands `查词模式`, `学习模式`, `复习模式`, `测试模式`, `听力模式`, and `整理模式` select English and activate its matching mode when no category is active. Within English they retain their existing meaning. Within CS, interview, Job, Distributed System, or AI, generic learning/review/testing requests follow that category's router; English-specific lookup/listening/inbox commands explicitly select English. `优化模式` and `refine模式` always select English and activate `/english/instructions/refine.md`.

## Persistence and overrides

Category and task-mode state are scoped to this conversation. An explicit category switch clears the prior category's task mode. `默认模式` clears both category and task mode and resumes intent routing. Explicit requests for another task override the active selection for that request without silently changing the persistent selection.

Requests to manage the repository are repository tasks; do not proofread them or run a learning exercise. Do not apply English-only fallback proofreading to a clear CS or interview question.

## Learning skill use

At the start of a teaching, review, or testing session, check the skills actually available in the current runtime. If a relevant skill is available, use it to guide the session without requiring the user to name or invoke it. For English, use available vocabulary-explanation, synonym-comparison, and writing-feedback skills when they fit. For CS, Distributed System, AI, and interview learning, use an available tutoring or subject-specific skill when it fits.

Skills supplement this repository's workflow; they do not replace category routing, source materials, learning records, or evidence requirements. Ground teaching in the selected category's materials and mastery state. Keep assessment evidence in the category actually assessed, update records only under that category's rules, and preserve output constraints such as Listening Mode's English-only passages. If no relevant skill is available, use the repository's normal workflow. Never claim a skill is available unless it appears in the current runtime.

## Boundaries

- English: wording, translation, pronunciation, technical language.
- CS: mechanisms, theory, implementation, research, and engineering tradeoffs.
- Interview: job-oriented retrieval, coding exercises, timed reasoning, system-design answers, and behavioral practice.
- For a mixed request, follow the primary objective and consult the second category only when needed. Keep learning evidence in the category actually assessed.
- Read only the relevant instructions and materials. Never claim a read or write succeeded without tool confirmation.
- Learning state is evidence-based; do not infer mastery from explanations or migration.
- Listening Mode outputs only the English passage(s) intended to be heard, with no headings, translations, explanations, or commentary.

## Job preparation entry

`/Job/README.md` describes the four Job topics and instruction lookup. Use `/Job/instructions/router.md` to select a topic or career planning. Career goals, target-role and skill-gap planning, milestones, job-preparation plans, Networking actions, and career decisions/reviews route to `/Job/career-development.md`; do not invent personal information or completed actions. Distributed System and AI concept learning use their topic routers; interview drills use the interview router. All CS and interview instructions, materials, and learning records live under `/Job/CS/` and `/Job/interview/`. All prior commands and specific workflow precedence remain in effect.
