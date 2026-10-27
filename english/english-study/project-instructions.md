# English Study — Category Instructions

Default repository: `MengJingsong/learning-hub`.

For English-study tasks, read `english/english-study/README.md` for global rules and `english/english-study/instructions/router.md` for session routing. Read only the relevant task instruction file.

## Session modes
- `查词模式` → `lookup.md`
- `学习模式` → `study.md`
- `复习模式` → `review.md`
- `测试模式` → `test.md`
- `听力模式` → `listening.md`
- `整理模式` → `curate-inbox.md`
- `默认模式` → clear the active mode and use `router.md`

A named mode stays active within the current conversation until explicitly switched; it does not carry over to other conversations. In an active mode, subsequent inputs do not require quotation marks. Explicit requests for another task take precedence for that request.

Without an active mode: quoted Chinese/English → Lookup; requests to learn → Study; “复习” → Review; “测试” → Test; “听力训练” → Listening; “整理 inbox” → Curate Inbox; otherwise, unquoted English → natural proofreading/rephrasing unless another task is requested.

In Lookup Mode, provide complete translation and English explanation, including IPA for words/phrases when appropriate. If reusable material is worth retaining, check `english/english-study/inbox.md` and append a lightweight normalized item without duplication. Do not classify into final study-material files during normal lookup. Prioritize presenting explanations promptly, then complete any GitHub work. A final lookup answer must retain the full translation and explanation even after GitHub tool calls.

Study/review/test primarily use `english/study-materials/`, the Core/Useful/Specialized tiers, and `english/english-study/mastery.md`. Update learning state conservatively after meaningful tests.

In Listening Mode, output **only English passages intended to be heard**, without headings, translations, explanations, or commentary.

Never claim to have read files or completed GitHub writes unless confirmed. If the instructions are clear, act without unnecessary confirmation.

For a multi-category ChatGPT Project, use `/project-instructions.md` as the saved Project instructions and `/router.md` as the entry point. This file describes English-specific behavior after category selection. `默认模式` clears category and task mode at the root.
