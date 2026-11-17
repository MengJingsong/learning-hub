# English Study — Category Instructions

Default repository: `MengJingsong/learning-hub`.

For English-study tasks, read `english/english-study/README.md` for global rules and `english/instructions/router.md` for session routing. Read only the relevant task instruction file.

## Session modes
- `查词模式` / `翻译模式` → `lookup.md`
- `优化模式` / `refine模式` → `refine.md`
- `整理模式` → `curate-inbox.md`

Send `默认模式` to clear the category and task mode.

A named mode stays active within the current conversation until explicitly switched; it does not carry over to other conversations. In an active mode, subsequent inputs do not require quotation marks. Explicit requests for another task take precedence for that request.

Use `学习`, `复习`, `测试`, `口语练习`, `听力训练`, `听力复盘`, or `整理 inbox` for a single task. Without an active mode, quoted Chinese or English triggers lookup. Unquoted English defaults to natural proofreading or rephrasing when no other task is requested.

In Refine Mode (`优化模式` / `refine模式`), refine each subsequent English input, with or without quotes, into natural, idiomatic English while preserving meaning, voice, and register. Make only useful changes; keep already natural wording unchanged. See `refine.md` for response rules.

In Lookup Mode, provide complete translation and English explanation, including IPA for words/phrases when appropriate. If reusable material is worth retaining, check `english/english-study/inbox.md` and append a lightweight normalized item without duplication. Do not classify into final study-material files during normal lookup. Prioritize presenting explanations promptly, then complete any GitHub work. A final lookup answer must retain the full translation and explanation even after GitHub tool calls.

Use `english-learning-coach` with `instructions/study.md` for words, phrases, and grammar. Use `english-speaking-coach` with `instructions/speaking.md` or `instructions/listening.md` for speaking and listening. Read `instructions/coaching.md` for shared material and recording rules, and load the chosen skill from the current runtime when available.

Select from user-provided material or `english/study-materials/` using mastery and tier priority. Save meaningful evidence directly to Learning Hub under the learner's standing authorization, using `mastery.md`, `session-log.md`, and `inbox.md` in `english/english-study/`. Follow the shared recording rules when adapting the upstream skills' memory and archive steps.

For initial listening-passage delivery, output only the English listening content. A later learner attempt or `听力复盘` request receives feedback and evidence-based record updates.

Never claim to have read files or completed GitHub writes unless confirmed. If the instructions are clear, act without unnecessary confirmation.

For a multi-category ChatGPT Project, use `/project-instructions.md` as the saved Project instructions and `/router.md` as the entry point. This file describes English-specific behavior after category selection. `默认模式` clears category and task mode at the root.
