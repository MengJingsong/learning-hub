# Session Instruction Router

Use `/english/english-study/README.md` for English-category rules. Read only the task-specific instruction file needed for the current task.

## Supported session modes

| Activation command | Mode | Instruction file |
|---|---|---|
| 查词模式 | Lookup | `lookup.md` |
| 学习模式 | Study | `study.md` |
| 复习模式 | Review | `review.md` |
| 测试模式 | Test | `test.md` |
| 听力模式 | Listening | `listening.md` |
| 整理模式 | Curate Inbox | `curate-inbox.md` |
| 默认模式 | Default | `router.md` |

## Mode activation and persistence

When the user activates a named mode, read that mode's instruction file, then apply it to subsequent messages in the **current conversation**. Do not require quotation marks or repeated activation commands while a mode is active.

An explicit mode switch replaces the previous mode. `默认模式` clears the named mode and resumes per-message intent routing. A clear request for a different task takes precedence for that task; do not ignore explicit requests merely because a mode is active. A new conversation does not inherit the mode of another conversation.

If the relevant instruction file cannot be accessed, do not claim to have loaded it. Use the already available English-category rules and explain material limitations where necessary.

## Default routing (no named mode active)

- Quoted Chinese or English input, wrapped in `""`, `''`, `“”`, or `‘’` → `lookup.md`.
- A request to learn new material → `study.md`.
- “复习” → `review.md`.
- “测试” → `test.md`.
- “听力训练” → `listening.md`.
- “整理 inbox” → `curate-inbox.md`.
- Unquoted English input → proofread and rephrase naturally, unless another task was requested.

Use the smallest relevant instruction set. The active task's instructions control formatting, including the English-only output rule for Listening Mode.

## Learning Hub integration

The root `/router.md` selects the category before this router runs. `默认模式` clears both category and task mode and returns to root routing. Generic study/review/test commands use this router only when English is selected or chosen by root routing.
