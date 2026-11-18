# Learning Hub Coaching

Use this shared instruction with `study.md`, `speaking.md`, or `listening.md` for English coaching in `MengJingsong/learning-hub`.

## Skill selection

| Learning objective | Skill | Task instruction |
|---|---|---|
| Words, phrases, collocations, and grammar | `english-learning-coach` | `study.md` |
| Speaking, conversation, and shadowing | `english-speaking-coach` | `speaking.md` |
| Listening and listening feedback | `english-speaking-coach` | `listening.md` |

Read the selected skill from the current runtime's available skill source. Use an installed skill when it is available. If the runtime cannot load it, explain that limitation and use this repository's task instructions. Installing a skill on one computer makes it available in that local environment. A GitHub reference records its source.

## Materials and context

Read `/english/english-study/README.md`, `/english/english-study/learning-plan.md`, `/english/english-study/mastery.md`, and recent relevant entries in `/english/english-study/session-log.md` before choosing a task. Reuse known goals and preferences and collect only the missing context needed to start. The learner's current teaching preference takes priority over the upstream skills' default production, quiz, and retry loops.

Use material or topics explicitly selected by the learner. Otherwise select from `/english/study-materials/`, prioritizing due and weak items, then Core items when review needs are similar. For every selected formal corpus entry, read its exact-heading note in `/english/study-materials/explanations/` before teaching it; use that durable explanation as the basis for the walkthrough, and add context-specific teaching as needed. In the explanation-led walkthrough, retain the learner's Chinese translation of the first-pass passage and compare each target item during the second pass. Record only demonstrated comprehension evidence; do not infer other skill dimensions from translation. External material can supplement authentic usage and examples. Retain a source link or repository path when it matters for continuing the lesson.

Use `sentence-patterns.md` for reusable grammatical structures and essential usage distinctions. New grammar targets can enter `inbox.md` as normalized `[pattern]` candidates and be curated into the formal corpus later.

## Explanation feedback and revisions

If the learner identifies a factual error, missing sense, misleading example, or other concrete issue in a durable explanation, update the corresponding exact-heading entry in `/english/study-materials/explanations/`. Preserve sound material, incorporate the correction, and verify relevant lexical claims against both Oxford Advanced American Dictionary and Cambridge Dictionary when each has an applicable entry; use an authoritative domain source when a technical sense is not adequately covered. Add links to the entries actually consulted. Preference feedback about presentation alone changes the teaching approach; revise the durable note only when it improves the note itself. Confirm the repository update.

## Learning records

The learner has authorized English learning progress to be recorded in Learning Hub. After meaningful practice, write the evidence directly to the repository using the available GitHub tools or local checkout. This authorization covers normal learning records in future Learning Hub sessions, subject to later user instructions.

Use the following authoritative files.

- `/english/english-study/mastery.md` holds per-item state for formal study items. Match existing headings and identifiers, preserve earlier evidence, and update only assessed dimensions on the existing 0–5 scale. Use `not assessed` for dimensions without evidence. Record the task, input modality, cue level, retry result, test date, and an appropriate next review date in the existing fields. Immediate corrected repetition is prompted practice. Delayed independent use supports stronger retention evidence.
- `/english/english-study/session-log.md` holds concise session evidence, including date, objective, material or target, observed response, important correction, retry result, and next task. A short excerpt is enough to substantiate a recurring problem. Grammar or external-material practice can be recorded here before its target enters the formal corpus.
- `/english/english-study/inbox.md` receives worthwhile new words, phrases, grammatical structures, and pronunciation targets after checking the formal corpus and inbox for duplicates. Follow its lightweight format and the curation workflow.

Use repository storage for the upstream skills' learning records, saved vocabulary, recurring errors, and next-session goals. Adapt their Agent-memory save question and manual Project-source archive step to the learner's standing authorization to write to Learning Hub.

Read current state before writing, merge new evidence with existing records, and avoid duplicate entries on retry. Commit related record updates together when supported. Confirm successful writes. If writing fails, preserve the pending update in the reply and state what remains unsaved.

Track explanation coverage and the continuation point in `/english/english-study/learning-plan.md`. Record changes of learning preference there and note the change in `session-log.md` when needed for continuity.

Installation, planning, explanations, passage delivery, and simply revealing an answer provide no assessment evidence. Update mastery only after an observed attempt or a clearly attributed learner report. Identify self-reported evidence as such.

## Audio and session boundaries

Base speaking and listening assessments on the input actually available. Text or a transcript can support feedback on wording and grammar. Evaluate pronunciation, rhythm, and listening recognition only when the audio interaction supplies relevant evidence. For listening responses, record whether the learner had access to the transcript or other cues.

Use the host's existing audio capabilities when available. Optional TTS setup follows the learner's choice. Generated audio and transcripts carry no automatic evidence of the learner's performance.

On wrap-up, give a compact review and next task, save meaningful evidence, and offer a short shadowing task if useful. Follow the learner's request to end or skip shadowing. During the initial listening-passage response, follow `listening.md`'s English-only output rule and defer feedback and record confirmation to the response after the learner's attempt.

## Installed sources

The initial local installation uses these upstream versions. They supply the coaching workflow. This repository supplies the category routing, material selection, output rules, and learning-record destination.

- [english-learning-coach, fe84b342](https://github.com/zhouwei713/english-learning-coach-skill/tree/fe84b34287fa4385d4ab69cb064b57208d2b4058)
- [english-speaking-coach, bab43875](https://github.com/lolopodcast/english-speaking-coach-plugin/tree/bab43875834243fad1147c2304e209a20cbcd5c3/skills/english-speaking-coach)
