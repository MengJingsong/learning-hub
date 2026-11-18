# English Corpus Walkthrough

Updated 2026-11-18.

## Learning preference and two-pass workflow

Ordinary corpus learning follows two passes. The default batch is 15 words or phrases; use a different batch size when the learner specifies N.

**Pass one — English reading and learner translation.** Select the current N target entries and weave every one into a few fluent, natural English paragraphs. Bold each target word or phrase in Markdown. Give only the English paragraphs, without a title, translation, definitions, vocabulary notes, or other commentary. Preserve each target form where natural; adjust grammar only when needed for fluent English. Prefer coherent prose over sentence-by-sentence stuffing. Include long or complex sentences and elliptical sentences when they sound natural. The learner then writes a Chinese translation of the passage. After receiving it, retain it with the current batch and briefly acknowledge receipt; do not reveal the reference translation or detailed corrections before the second pass. The learner's request allows drawing on patterns in `study-materials/sentence-patterns.md`; adapt patterns to the passage rather than forcing them.

**Pass two — documented explanations and translation feedback.** After the learner submits the Chinese translation, the next `继续` begins the explanation pass for that same batch. Explain every entry one at a time. Before each explanation, open the matching file in `study-materials/explanations/` and use the exact-heading section as the authoritative source; include the explanation already documented there rather than replacing it with a new, shorter account. Use Chinese meaning/translation together with a clear English explanation where helpful, plus relevant pronunciation, register, usage, collocations, and examples. Relate the entry to its use in the passage. Compare the learner's translation item by item: identify what was accurate, partly accurate, or incorrect, and explain any missed meaning or nuance with a correction. Treat this as evidence of comprehension for the translated entries only; update only the assessed comprehension fields in `mastery.md`, following its scale and the shared evidence rules. Do not infer speaking, listening, or English-writing mastery from Chinese translation. Do not omit an entry because it seems familiar; finish one entry before moving to the next. Do not force uncommon combinations. Add a direct contrast only for a confusion the learner has identified.

The learner's `继续` advances the sequence: first-pass paragraphs, learner's Chinese translation, documented explanation with translation feedback, then the next batch's paragraphs. If the learner asks a direct question between stages, answer it and retain the current batch and translation. Follow explicit requests to skip or change a pass.

The previous police speed-limit translation retry is cancelled.

## Reference dictionaries and AI explanations

Use the [Oxford Advanced American Dictionary](https://www.oxfordlearnersdictionaries.com/us/) as the preferred first reference for American English meanings, usage, and pronunciation. Use the [Cambridge Dictionary](https://dictionary.cambridge.org/us/) as a useful cross-check, especially for its US/UK pronunciation audio and additional examples. Dictionaries are references, not a requirement to force a lookup for every straightforward item. For specialized or context-dependent senses, consult a reliable domain source when needed.

AI may synthesize the source note and passage context into a concise Chinese translation plus an English explanation, examples, and usage cues. Keep source-backed definitions distinct from contextual inference; verify uncertain technical or fine-grained claims against a dictionary or domain source.

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

Completed explanation batch on 2026-11-18 — `vocabulary.md`: Precedent, Tier, Adapt, Adopt, Rubric, Magnitude, Demote, Goalposts, Excerpt, Moot, Canary, defer, withhold, breach, and exhaustion. Resume by checking the conversation and coverage log, then select the next uncovered entries in the stated tier and corpus order.
