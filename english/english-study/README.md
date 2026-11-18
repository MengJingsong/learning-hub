# English Study

This folder stores learning state, temporary study intake, testing history, and English study rules. Task-specific instructions are stored separately in `/english/instructions/`.

## Repository structure

- `/english/study-materials/` is the complete study corpus. Unless the user explicitly asks otherwise, items to teach/test should come from that folder.
- `/english/study-materials/vocabulary.md` stores individual words.
- `/english/study-materials/phrases.md` stores reusable phrases, collocations, phrasal verbs, and general-purpose chunks.
- `/english/study-materials/sentence-patterns.md` stores reusable sentence frames and structures.
- `/english/study-materials/everyday-english.md` stores North American daily, campus, workplace, and conversational English.
- `/english/study-materials/academic-english.md` stores academic writing, presentations, research discussion, and evidence/argumentation language.
- `/english/study-materials/cs-research-english.md` stores computer-science and technical research English.
- `/english/study-materials/pronunciation-listening.md` stores listening-specific pronunciation targets such as reductions, linking, stress, and rhythm.
- Primary study-material files are lightweight lists: one item per line. Every formal entry must have a durable explanation in the matching file under `/english/study-materials/explanations/`, keyed by the exact item heading. Before teaching or reviewing an entry, consult its companion explanation as the source for meaning, pronunciation, usage, and examples, then add context-specific teaching as needed. Keep explanations complete under `/english/instructions/curate-inbox.md`.
- Every study-material file uses three priority tiers: **Core**, **Useful**, and **Specialized**.
- **Core** items are high-frequency and highly transferable; prioritize active mastery.
- **Useful** items are common but more context-dependent; review them regularly with lower weight.
- **Specialized** items are narrower, more technical, or lower-frequency; review them mainly when due, weak, or relevant to the current task.
- Priority and mastery are independent. Do not treat a Core label as evidence of mastery or a Specialized label as permission to ignore an overdue weak item.
- `/english/english-study/inbox.md` is a temporary intake queue for promising new items discovered during lookup. Inbox items are not formal study material until curated.
- `/english/instructions/` stores task-specific instructions. Use `router.md` to select the smallest relevant instruction file for the current task.
- `/english/english-study/project-instructions.md` contains concise long-term Project-level routing instructions.
- `/english/english-study/learning-plan.md` stores the learner's current teaching preference, corpus walkthrough order, and explanation coverage.
- `/english/english-study/` stores learning state and study-system metadata. It is not itself part of the study corpus.
- The repository root `README.md` is documentation only and is not study material.

## Goal

The goal is active mastery, not recognition alone. Training should develop:
- listening: recognize items in natural, relatively fast spoken English;
- speaking: recall and use items naturally without being given the target expression;
- writing: use items accurately and idiomatically;
- comprehension: understand meaning, nuance, register, and common contexts.

## Mastery scale

Use a 0–5 scale for each item:
- 0 = unfamiliar
- 1 = recognized but not usable
- 2 = understood in context
- 3 = usable with prompting
- 4 = usable spontaneously in new contexts
- 5 = retained and spontaneous across listening/speaking/writing after delayed review

Do not mark an item mastered from one immediate correct answer. Delayed, unprompted recall in a new context is stronger evidence.

## Testing principles

For requested practice or assessment, prefer active recall over recognition. Progress from meaning/recognition to contextual discrimination, translation or completion, unprompted production, listening recognition, and integrated situational use.

For mature items, hide the target word/phrase and test whether the learner independently retrieves it. Re-test items after delays. Give extra weight to unprompted correct use and to successful delayed review.

Track skill-specific weaknesses when useful: listening, speaking, writing, and comprehension.

## Review selection

When choosing what to review, prioritize:
1. due/overdue items;
2. recently failed or weak items;
3. low-mastery items;
4. items not tested for a long time;
5. priority tier when the above factors are similar: Core > Useful > Specialized;
6. a smaller sample of mastered items for retention checks.

For a balanced general review session, a useful default is roughly 60% Core, 30% Useful, and 10% Specialized. Override this distribution when mastery history or the user's current goal makes another mix more appropriate.

## Listening-training rule

For an initial “听力训练” request, output only the English passages intended to be heard. Base them on the selected material or formal corpus, using natural North American English. After the learner supplies an attempt or requests “听力复盘”, follow `/english/instructions/listening.md` for feedback and evidence-based progress updates.

## State files

- `mastery.md`: current per-item learning state. This is the primary state file.
- `session-log.md`: concise record of meaningful tests/reviews and notable errors or improvements.

Update state after meaningful testing. Avoid bloating the log with every trivial interaction.

English learning progress is authorized to be saved directly to this repository after meaningful practice. Follow `/english/instructions/coaching.md` for skill selection, evidence, inbox candidates, and write confirmation. New grammar structures use the sentence-pattern corpus and the same intake workflow.

## Default workflow for ChatGPT

At the beginning of a study/review session, read this README, `learning-plan.md`, the relevant study materials, and `mastery.md`. Follow the learner's current teaching preference and continuation point. For corpus walkthroughs, use the plan's English-passage → learner-translation → documented-explanation sequence, and track explanation coverage there. Use translation as comprehension evidence only and update mastery conservatively under the shared record rules. Revise the matching durable explanation when the learner gives substantive correction or content feedback.

## Instruction routing

See `/english/instructions/router.md` for the authoritative mode map, activation rules, and default routing.

Named session modes:
- `查词模式` / `翻译模式` → `lookup.md`
- `优化模式` / `refine模式` → `refine.md`
- `整理模式` → `curate-inbox.md`

Send `默认模式` to clear the category and task mode. Request learning, review, testing, speaking, or listening directly with `学习` (with a topic or material), `复习`, `测试`, `口语练习`, `听力训练`, or `听力复盘`.

A named mode persists only within its current conversation. While it is active, future messages do not require quotes. An explicit change of mode replaces it; clear requests for another task may override it for that request. Without an active mode, route each message by its intent and quotation marks.

Load only the smallest relevant set of instruction files for the current task.

## Inbox workflow

During ordinary quoted lookup, do not immediately classify new study candidates into `/english/study-materials/`.

Instead:
1. explain the language fully to the user;
2. if the item is worth long-term study, normalize it and append it to `/english/english-study/inbox.md` after checking for duplicates;
3. leave detailed classification and tiering for a later “整理 inbox” session.

During inbox curation:
1. correct/normalize;
2. deduplicate;
3. remove low-value or one-off items;
4. classify into the best formal study-material file;
5. assign Core / Useful / Specialized;
6. add the required durable explanation to the matching file under `/english/study-materials/explanations/`;
7. remove processed inbox entries.

See `/english/instructions/curate-inbox.md` for the explanation format and full curation rules. This keeps lookup sessions fast and keeps the formal study corpus curated.
