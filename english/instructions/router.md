# Session Instruction Router

Use `/english/english-study/README.md` for English-category rules. Read only the task-specific instruction file needed for the current task.

## Mode commands

| Command | Action | Instruction file |
|---|---|---|
| 查词模式 / 翻译模式 | Lookup | `lookup.md` |
| 优化模式 / refine模式 | Refine | `refine.md` |
| 整理模式 | Curate Inbox | `curate-inbox.md` |
| 默认模式 | Clear the category and task mode | `router.md` |

## Mode activation and persistence

When the user activates a named mode, read that mode's instruction file, then apply it to subsequent messages in the **current conversation**. Do not require quotation marks or repeated activation commands while a mode is active.

An explicit mode switch replaces the previous mode. `默认模式` clears the named mode and resumes per-message intent routing. A clear request for a different task takes precedence for that task; do not ignore explicit requests merely because a mode is active. A new conversation does not inherit the mode of another conversation.

If the relevant instruction file cannot be accessed, do not claim to have loaded it. Use the already available English-category rules and explain material limitations where necessary.

## Direct requests

These requests apply to the current task.

- `学习` with a vocabulary, phrase, or grammar objective → `study.md` with `english-learning-coach`.
- `口语练习`, spoken retelling, conversation, or shadowing → `speaking.md` with `english-speaking-coach`.
- `听力训练`, dictation, or `听力复盘` → `listening.md` with `english-speaking-coach`.
- `复习` → `review.md` plus the task instruction for the skill being practiced.
- `测试` → `test.md` plus the task instruction for the skill being assessed.
- `整理 inbox` → `curate-inbox.md`.

## Default routing (no named mode active)

- Quoted Chinese or English input, wrapped in `""`, `''`, `“”`, or `‘’` → `lookup.md`.
- Unquoted English input → proofread and rephrase naturally, unless another task was requested.

Use `coaching.md` for shared material selection, skill use, and progress persistence. A named coaching skill explicitly invoked for a Learning Hub task follows the same objective-based routing. Follow-up answers continue the active exercise until completion or a new request.

Use the smallest relevant instruction set. Initial listening-passage delivery outputs only English listening content. A subsequent listening attempt or feedback request follows the feedback section of `listening.md`.

## Learning Hub integration

The root `/router.md` selects the category before this router runs. `默认模式` clears both category and task mode and returns to root routing. Generic study/review/test commands use this router only when English is selected or chosen by root routing.
