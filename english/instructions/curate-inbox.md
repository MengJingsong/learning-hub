# Curate Inbox Mode

Trigger: the user says “整理 inbox”, “整理” while Curate Inbox Mode is active, or explicitly asks to organize pending study items.

Read `/english/english-study/inbox.md`, then process pending items in batch.

For each item:
1. correct or normalize it if necessary;
2. remove duplicates and near-duplicates;
3. discard low-value, one-off, unnatural, or overly context-specific items;
4. classify retained items into the most appropriate file:
   - `vocabulary.md`
   - `phrases.md`
   - `sentence-patterns.md`
   - `everyday-english.md`
   - `academic-english.md`
   - `cs-research-english.md`
   - `pronunciation-listening.md`
5. assign one tier: Core, Useful, or Specialized;
6. write each retained item only once, to its best primary location;
7. add a complete explanation for every retained item in the matching companion file under `/english/study-materials/explanations/`. Use the same filename as the primary study-material file and an exact item heading so the note can be matched reliably. Every formal corpus entry must have exactly one matching explanation heading; check coverage before removing processed items from the inbox. Keep the primary study-material files as lightweight one-item-per-line lists; do not put multi-line explanations there;
8. remove processed items from the inbox only after the item and its explanation have both been recorded.

## Dictionary and English-explanation rules

For word entries, consult both Oxford Advanced American Dictionary and Cambridge Dictionary when explaining meanings. Prefer the American English sense and pronunciation. Write a concise, learner-friendly English explanation of the relevant sense alongside the Chinese meaning; explain collocations, register, and context as needed. Use original wording rather than copying dictionary definitions or examples. No source links or additional domain-source lookup are required. Apply the same principle to phrases, patterns, grammar, and pronunciation points: include a clear English explanation as well as Chinese teaching.

## Explanation requirements

Classify each item by what it is, not only by the file it is stored in. If one inbox line combines independently useful items (for example, slash-separated alternatives or a word plus a phrase), split it into separate primary entries and give each its own explanation. Preserve the assigned tier for each resulting entry as appropriate.

- **Word:** Give American English IPA, a concise English explanation of each relevant sense, Chinese meaning(s), common collocations, context-appropriate synonyms and antonyms, and two natural example sentences with Chinese translations. Do not force an antonym when none is useful; say “无常用反义词” instead.
- **Phrase or sentence pattern:** Give a clear English explanation plus the Chinese meaning and usage, similar phrases or patterns, and two natural example sentences with Chinese translations. For sentence patterns, explain the structure and what can fill each slot.
- **Grammar:** Explain the form, meaning, usage, constraints, and common pitfalls in English and Chinese in enough detail to use it accurately; give two example sentences with Chinese translations.
- **Pronunciation or listening rule:** Explain in English and Chinese the sound change or listening cue, when it occurs, and any important limits; give two examples showing the relevant pronunciation/listening form, with Chinese translations.

Use examples that fit the item's register and likely context. Prefer natural North American English and, where relevant, the learner's academic, computer-science, and everyday contexts. IPA should be American English IPA. Use the two dictionaries to inform lexical explanations; do not add source links. Distinguish synonyms and antonyms by sense and register when needed; never imply that near-synonyms are interchangeable if they are not.

The formal corpus should contain only items worth long-term active mastery. Keep the source lists machine-readable and lightweight; store durable explanations in the companion files.
