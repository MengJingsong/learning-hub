# Book-based Knowledge Review

## Entry and book selection

Trigger: `知识点复习`. This explicitly selects CS and activates book-based review for the current conversation. Read `/CS/README.md`, `/CS/instructions/router.md`, and `/CS/instructions/learning.md`.

At the start of each requested book-review session, ask which book's concepts the learner wants to review. List the actual available books in `/CS/study-materials/`; do not select a book silently. If the request already names the book, use it without asking again. Accept unambiguous short titles such as DDIA; clarify only genuinely ambiguous names. Preserve the selected book and topic through follow-up questions and the subsequent test within this conversation.

## Select one suitable concept

After book selection:
1. Read the current `/CS/mastery.md`, `/CS/session-log.md`, relevant reusable notes, and the selected book's contents and relevant section. Use the actual available edition; cite its chapter/section and verified page location where useful. Do not invent source access or page numbers.
2. Choose exactly one focused concept from that book using relevant learning history. Prioritize due/overdue review, unresolved misconceptions or failed topics, weak understanding, and topics not tested recently. Respect prerequisites, demonstrated ability, and the learner's stated goals; choose a manageable next step when no suitable previous topic exists. Cross-book evidence about the same concept may inform selection, but identify the selected book as the source and preserve book-specific progress.
3. Briefly state the concept, source location, and why it fits the recorded evidence. Do not ask the learner to choose the concept after they have chosen a book.
4. If history is empty or insufficient, say that prior mastery is unknown and choose an accessible foundational concept from the book. Do not infer that the learner knows nothing or require a preliminary test.

Use stable concept IDs with book/edition and chapter/section references. Link equivalent concepts across books instead of duplicating conceptual notes.

## Explain, then answer questions

Explain in Chinese by default with English technical terms. Cover intuition, a precise definition, assumptions, mechanism, a worked example, common misconceptions, and relevant tradeoffs or failure cases. Adapt depth to actual evidence and the learner's follow-up questions. Paraphrase the source; distinguish book content from added examples or extensions.

Anticipate likely questions while preparing the explanation, especially why the mechanism works, when it fails, and how it differs from related concepts. Remain available for iterative questions on the selected topic; do not flood the learner with a speculative FAQ or advance automatically to another concept.

This workflow starts with explanation and discussion. Wait until the learner explicitly requests testing (for example, `测试我`, `开始测试`, or `测试模式`) before asking assessment questions. Do not replace the initial explanation with a quiz or automatically start testing after the explanation.

## Test on request

Test the current book and concept unless the learner requests a different scope. Ask one question at a time, wait for an answer, and withhold the solution until an attempt or a request for help. Use new examples and progressive questions to assess explanation, causal reasoning, application, and transfer; avoid merely repeating the worked example. Give graduated hints when requested and record assistance.

Use enough evidence to distinguish partial understanding from independent application; do not impose a fixed question count. After the test ends, explain what was correct, remaining misconceptions, the level supported by the answers, and the next review recommendation. Immediate success after teaching is not evidence of delayed retention.

## Record progress

After meaningful explanation/discussion, add or update a concise dated entry in `/CS/session-log.md` with book/edition, source location, concept ID/title, covered material, observed questions or difficulties, and next step. If no test occurred, explicitly mark `explained/discussed; unassessed` and do not increase mastery.

After meaningful testing, update `/CS/mastery.md` conservatively and finalize the session-log entry. Record:
- concept ID/title and book/edition/chapter/section;
- learning/review and test dates, brief answer evidence, errors, and hints;
- independent versus prompted performance;
- supported mastery level, unresolved weaknesses, and next review date or condition.

Use the existing 0-5 CS scale: 0 unfamiliar, 1 recognized, 2 understood, 3 applied with help, 4 independently applied, 5 retained and transferred after delayed review. Unassessed is unknown, not zero. Preserve previous evidence and never lower an established level merely because the learner starts a new session. Distinguish exposure, immediate performance, and delayed retention. Update existing topic/session entries rather than duplicating them for every follow-up.

Keep records exclusively in CS. Verify GitHub writes before claiming progress was saved; if a write fails, state that the record remains unsaved.

## Source Retrieval Optimization

- For each Knowledge Point, locate the relevant chapter/section first and retrieve only the necessary passages, rather than repeatedly fetching an entire PDF. Use the chapter index and previously verified references when available.
- Prefer an accessible ChatGPT Project File for the selected book. If the Project File is unavailable or the required passage cannot be retrieved, fall back to the authorized Google Drive copy. If neither source is accessible, disclose the limitation and ask for the relevant excerpt; never pretend to have read it.
- Minimize redundant retrieval across follow-up questions, while re-checking the source when accuracy or context requires it. Preserve chapter/edition attribution and distinguish source-supported statements from added explanations.
- This is a retrieval-efficiency guideline, not a guarantee of lower token usage; token consumption depends on the actual material placed into model context.
