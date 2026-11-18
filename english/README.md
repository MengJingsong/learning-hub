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
- `explanations/` — durable companion explanations, stored in files matching the primary study-material filenames and keyed by exact item headings.

Primary study-material files stay lightweight, with one item per line. Every formal entry has a durable explanation in the matching file under `study-materials/explanations/`, keyed by its exact heading. Before teaching an entry, consult that explanation for meaning, pronunciation, collocations, usage notes, and examples; add context-specific teaching when useful.

### Priority tiers

Every study-material file is organized into three priority tiers:

- **Core** — high-frequency, highly transferable items that are especially valuable for a computer-science PhD in North American daily life, academic communication, and research. These should receive the most practice and should ideally reach spontaneous active use.
- **Useful** — common and worthwhile items whose value is more context-dependent. Practice them regularly, but less heavily than Core items.
- **Specialized** — lower-frequency, more technical, narrower, or context-specific items. Keep them available for targeted learning and periodic review rather than giving them equal review weight.

Priority is separate from mastery. A Specialized item can still be weak or due for review, and a Core item can eventually require only occasional retention checks. When other factors are equal, use the order **Core > Useful > Specialized**.

### `/english/english-study/`

This folder stores learning-state metadata, study rules, and temporary intake rather than formal study material.

- `README.md` — English-category study rules and workflow.
- `project-instructions.md` — copy-ready ChatGPT Project Instructions for session modes and direct requests.
- `learning-plan.md` — current learning preference, walkthrough order, and explanation coverage.
- `inbox.md` — temporary queue for newly discovered items; not part of the formal study corpus until curated.
- `mastery.md` — current mastery state for formal study items.
- `session-log.md` — concise history of meaningful reviews and tests.

### `/english/instructions/`

This folder stores task-specific instructions:

- `router.md`
- `lookup.md`
- `refine.md`
- `coaching.md` — shared coaching, material selection, and learning-record rules.
- `study.md` — vocabulary, phrases, and grammar with `english-learning-coach`.
- `speaking.md` — conversation and shadowing with `english-speaking-coach`.
- `review.md`
- `test.md`
- `listening.md` — listening passages and feedback with `english-speaking-coach`.
- `curate-inbox.md`

Use `查词模式` / `翻译模式`, `优化模式` / `refine模式`, or `整理模式` to activate a mode for the current chat. Send `默认模式` to clear the current category and mode. To study, review, test, or practice listening, ask directly, for example `学习这些短语`, `复习`, `测试`, `口语练习`, `听力训练`, or `听力复盘`. See [instructions/router.md](instructions/router.md).

## Study workflow

When studying or reviewing, use `english/study-materials/` as the source corpus and `english/english-study/mastery.md` to choose what needs practice. Due/weak items take precedence; among items with similar mastery and review status, prefer Core over Useful over Specialized.

When useful, outside resources may be consulted dynamically for authentic usage, pronunciation, register, technical context, and current examples.

`english-learning-coach` guides word, phrase, and grammar practice. `english-speaking-coach` guides speaking and listening. Read [coaching.md](instructions/coaching.md) for shared rules and source versions. Install these skills in the runtime where practice takes place. Learning Hub stores the authoritative learning progress under the learner's standing authorization, using `mastery.md`, `session-log.md`, and `inbox.md` after meaningful practice.

New candidate items discovered during ordinary lookup should first go to `english/english-study/inbox.md`. They enter the formal `english/study-materials/` corpus only during inbox curation, when they are normalized, deduplicated, classified, assigned a priority tier, and given a matching durable explanation.

The root `README.md` is documentation only and is not part of the study corpus.
