# English Study

This folder stores learning state, temporary study intake, task-specific instructions, testing history, and the rules ChatGPT should use when helping with this repository.

## Repository structure

- `/english/study-materials/` is the complete study corpus. Unless the user explicitly asks otherwise, items to teach/test should come from that folder.
- `/english/study-materials/vocabulary.md` stores individual words.
- `/english/study-materials/phrases.md` stores reusable phrases, collocations, phrasal verbs, and general-purpose chunks.
- `/english/study-materials/sentence-patterns.md` stores reusable sentence frames and structures.
- `/english/study-materials/everyday-english.md` stores North American daily, campus, workplace, and conversational English.
- `/english/study-materials/academic-english.md` stores academic writing, presentations, research discussion, and evidence/argumentation language.
- `/english/study-materials/cs-research-english.md` stores computer-science and technical research English.
- `/english/study-materials/pronunciation-listening.md` stores listening-specific pronunciation targets such as reductions, linking, stress, and rhythm.
- Study-material entries should remain lightweight. Detailed meaning, register, context, pronunciation, and examples may be researched or generated dynamically during study; preserve permanent notes only when they are important for correct use.
- Every study-material file uses three priority tiers: **Core**, **Useful**, and **Specialized**.
- **Core** items are high-frequency and highly transferable; prioritize active mastery.
- **Useful** items are common but more context-dependent; review them regularly with lower weight.
- **Specialized** items are narrower, more technical, or lower-frequency; review them mainly when due, weak, or relevant to the current task.
- Priority and mastery are independent. Do not treat a Core label as evidence of mastery or a Specialized label as permission to ignore an overdue weak item.
- `/english/english-study/inbox.md` is a temporary intake queue for promising new items discovered during lookup. Inbox items are not formal study material until curated.
- `/english/english-study/instructions/` stores task-specific instructions. Use `router.md` to select the smallest relevant instruction file for the current task.
- `/english/english-study/project-instructions.md` contains concise long-term Project-level routing instructions.
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

Prefer active recall over recognition. Progress from meaning/recognition to contextual discrimination, translation or completion, unprompted production, listening recognition, and integrated situational use.

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

When the user says “听力训练”, output only the English passage(s) intended to be heard. Do not add headings, explanations, translations, instructions, or commentary, because all extra text may be read aloud. Base passages primarily on `/english/study-materials/` and use natural, relatively fast conversational English.

## State files

- `mastery.md`: current per-item learning state. This is the primary state file.
- `session-log.md`: concise record of meaningful tests/reviews and notable errors or improvements.

Update state after meaningful testing. Avoid bloating the log with every trivial interaction.

## Default workflow for ChatGPT

At the beginning of a study/review session, read this README and the relevant study materials plus `mastery.md`. Select exercises based on current mastery rather than randomly. After testing, update mastery conservatively and add a concise session-log entry when useful.


## Instruction routing

See `/english/english-study/instructions/router.md` for the authoritative mode map, activation rules, and default routing.

Named session modes:
- `查词模式` → `lookup.md`
- `学习模式` → `study.md`
- `复习模式` → `review.md`
- `测试模式` → `test.md`
- `听力模式` → `listening.md`
- `整理模式` → `curate-inbox.md`
- `默认模式` → clear the named mode; use `router.md`

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
6. remove processed inbox entries.

This keeps lookup sessions fast and keeps the formal study corpus curated.
