# English

This category is a long-term English study corpus and learning-state tracker.

The goal is **active mastery**, not simple recognition: listening, speaking, writing, comprehension, and natural use in North American daily life, academic work, and computer-science research.

## Repository structure

### `/english/study-materials/`

This folder is the complete study corpus.

- `vocabulary.md` — individual words worth mastering.
- `phrases.md` — reusable phrases, collocations, phrasal verbs, and general-purpose chunks.
- `sentence-patterns.md` — reusable sentence frames and structures.
- `everyday-english.md` — North American daily conversation, workplace/campus interaction, and natural spoken expressions.
- `academic-english.md` — academic writing, presentations, research discussion, evidence, argumentation, and conference/lab communication.
- `cs-research-english.md` — computer-science and software/systems research terminology and technical expressions.
- `pronunciation-listening.md` — listening-specific targets such as reductions, linking, stress, rhythm, and pronunciation patterns.

Study-material entries should stay lightweight. Detailed meaning, register, context, pronunciation, collocations, and examples can be researched or generated dynamically when an item is studied. Add permanent notes only when a distinction is important for correct use.

### Priority tiers

Every study-material file is organized into three priority tiers:

- **Core** — high-frequency, highly transferable items that are especially valuable for a computer-science PhD in North American daily life, academic communication, and research. These should receive the most practice and should ideally reach spontaneous active use.
- **Useful** — common and worthwhile items whose value is more context-dependent. Practice them regularly, but less heavily than Core items.
- **Specialized** — lower-frequency, more technical, narrower, or context-specific items. Keep them available for targeted learning and periodic review rather than giving them equal review weight.

Priority is separate from mastery. A Specialized item can still be weak or due for review, and a Core item can eventually require only occasional retention checks. When other factors are equal, use the order **Core > Useful > Specialized**.

### `/english/english-study/`

This folder stores learning-state metadata, study rules, and temporary intake rather than formal study material.

- `README.md` — English-category study rules and workflow.
- `project-instructions.md` — copy-ready ChatGPT Project Instructions with all seven mode commands and session persistence.
- `inbox.md` — temporary queue for newly discovered items; not part of the formal study corpus until curated.
- `mastery.md` — current mastery state for formal study items.
- `session-log.md` — concise history of meaningful reviews and tests.

### `/english/instructions/`

This folder stores task-specific instructions:

- `router.md`
- `lookup.md`
- `study.md`
- `review.md`
- `test.md`
- `listening.md`
- `curate-inbox.md`

To activate a persistent mode in a new chat, send one of: `查词模式`, `学习模式`, `复习模式`, `测试模式`, `听力模式`, `整理模式`, or `默认模式`. Modes apply only to that chat; see [instructions/router.md](instructions/router.md).

## Study workflow

When studying or reviewing, use `english/study-materials/` as the source corpus and `english/english-study/mastery.md` to choose what needs practice. Due/weak items take precedence; among items with similar mastery and review status, prefer Core over Useful over Specialized.

When useful, outside resources may be consulted dynamically for authentic usage, pronunciation, register, technical context, and current examples.

New candidate items discovered during ordinary lookup should first go to `english/english-study/inbox.md`. They enter the formal `english/study-materials/` corpus only during inbox curation, when they are normalized, deduplicated, classified, and assigned a priority tier.

The root `README.md` is documentation only and is not part of the study corpus.
