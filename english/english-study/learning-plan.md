# English Corpus Walkthrough

Updated 2026-11-18.

## Learning preference and two-pass workflow

Ordinary corpus learning follows two passes. The default batch is 15 words or phrases; use a different batch size when the learner specifies N.

**Pass one — English reading.** Select the current N target entries and weave every one into a few fluent, natural English paragraphs. Bold each target word or phrase in Markdown. Give only the English paragraphs, without a title, translation, definitions, vocabulary notes, or other commentary. Preserve each target form where natural; adjust grammar only when needed for fluent English. Prefer coherent prose over sentence-by-sentence stuffing. Include long or complex sentences and elliptical sentences when they sound natural. The learner's request allows drawing on patterns in `study-materials/sentence-patterns.md`; adapt patterns to the passage rather than forcing them.

**Pass two — documented explanations.** When the learner next says `继续` after a first-pass passage, explain that same batch in Chinese, one entry at a time. Before explaining each entry, open the matching file in `study-materials/explanations/` and use the section with the exact entry heading as the authoritative durable note. Cover its documented meanings, pronunciation, register, usage, collocations, and examples as relevant, then explain how the entry works in the passage and add context-specific clarification. Do not omit an entry because it seems familiar; finish one entry before moving to the next. Do not force uncommon combinations. Add a direct contrast only for a confusion the learner has identified. Do not test the learner or require them to produce sentences.

The learner's `继续` advances the two-pass sequence: first-pass paragraphs, then their detailed explanations, then the next batch's paragraphs. If the learner asks a direct question between passes, answer it and retain the current batch for its second pass. Follow explicit requests to skip or change a pass.

The previous police speed-limit translation retry is cancelled.

## Coverage order

Complete the current batch, then cover the remaining Core entries, followed by Useful and Specialized. Within each tier, follow the existing order in vocabulary, phrases, sentence patterns, everyday English, academic English, CS research English, and pronunciation/listening. Select N uncovered entries (15 by default) and check coverage before repeating an item. Present each batch using the two-pass workflow above.

The formal corpus snapshot contains 677 item-lines across seven files. All 677 entries have a matching exact-heading durable explanation in the seven companion files under `study-materials/explanations/` (coverage checked 2026-11-18). Preserve entries at their authoritative source paths. During each walkthrough, consult the documented explanation for every selected item and explain each item individually. Explanation coverage below records what has actually been delivered in conversation; it is separate from whether the written explanation exists.

## Consolidation queue and confusing items

Track requested reinforcement in [`consolidation-queue.md`](consolidation-queue.md). Keep one item per line with its source corpus entry and a short note when the learner identifies a specific confusion.

Resolve pending queue items before moving on to new corpus entries. Explain every item individually with fresh examples, common usage, and a concise usage cue. Do not group items by theme. When the learner explicitly identifies confusion between particular terms, add a focused contrast between those terms with distinct examples; do not invent extra confusing pairs. Mark an item complete only after its detailed second-pass explanation has been delivered.

Do not add quizzes or require learner production during consolidation. This queue records requested reinforcement, not assessed mastery; keep it separate from explanation coverage and mastery scores.

## Explanation coverage

This list tracks detailed second-pass explanations supplied in the conversation, based on each entry's durable companion note in `study-materials/explanations/`. It is separate from written-note coverage, English-only first-pass exposure, and the evidence-based scores in `mastery.md`. Record a batch as explained only after every entry's documented second-pass explanation has been delivered; use the conversation to confirm which pass is next when resuming.

Earlier explanation on 2026-11-17

- `vocabulary.md` — enforce, including its distinction from implement.

Earlier explanation batch on 2026-11-17

- `vocabulary.md` — threshold.
- `vocabulary.md` — ceiling.
- `vocabulary.md` — constraint.
- `phrases.md` — by default.
- `phrases.md` — take effect.

Earlier explanation batch on 2026-11-17

- `vocabulary.md` — Informative, Rigor, Fidelity, Hedging, Footprint, Hinge, Upshot, Boilerplate, Arguably, Triage, Verdict, Provenance, Caveat, Reconcile, and Conflate.

Earlier explanation batch on 2026-11-17

- `vocabulary.md` — Corroboration, Counterfactual, allocation, backlog, throughput, latency, contention, transient, sustained, aggregate, propagate, implicit, explicit, empirical, and hypothesis.

Earlier explanation batch on 2026-11-17

- `vocabulary.md` — infer, attribute, baseline, outlier, heuristic, criterion, fallback, backpressure, outage, robustness, scalability, deployment, workload, benchmark, and mitigate.

Earlier explanation batch on 2026-11-17

- `vocabulary.md` — validate, uncertainty, traditional, conventional, eligible, representative, typical, characteristic, clue, Stash, Emit, Under-tested, Provably, Reclaim, and Overshoot.

Current explanation batch on 2026-11-17

- `vocabulary.md` — Backfill, Pedagogical, Vague, Inert, Under-provisioned, Self-containment, Proliferation, Wrinkle, Hygiene, Terse, Dangling, Churn, Accounting, Load-bearing, and Scaffold.

Continue next with Precedent, Tier, Adapt, Adopt, Rubric, Magnitude, Demote, Goalposts, Excerpt, Moot, Canary, defer, withhold, breach, and exhaustion. Skip entries already covered and check the corpus and latest conversation before selecting the next batch.
