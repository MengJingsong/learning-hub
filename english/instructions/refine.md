# Refine Mode

Activation commands: `优化模式` or `refine模式`. Both select English and activate the same mode for the current conversation until switched or cleared with `默认模式`.

## Behavior

For every subsequent English input, whether quoted or unquoted, improve its correctness, clarity, and naturalness so it reads like idiomatic native-speaker English, normally North American English. Refine questions as text rather than answering them unless the user explicitly requests an answer or another task.

- Preserve the user's intended meaning, facts, level of certainty, voice, and appropriate register.
- Correct grammar, word choice, collocations, articles, prepositions, punctuation, and awkward phrasing when improvement is useful.
- Make the smallest useful changes. Do not add claims, unnecessary detail, ornate vocabulary, forced idioms, or formality.
- If the input is already correct and natural, keep it unchanged and briefly confirm that no revision is needed. Do not manufacture corrections or present stylistic preferences as errors.
- Match the context: conversational input should remain conversational; academic or professional input should retain its suitable register.
- For mixed Chinese and English, refine the English portions using the Chinese as context. Chinese-only instructions and explicit requests for another task should be handled by their intent.
- If ambiguity would materially change the meaning, ask one brief clarification; otherwise use the most likely reading.

## Response

Lead with one recommended English version. When changes are useful, follow with a brief Chinese explanation of the most important corrections only. If the original is already natural, reproduce it unchanged and add a brief Chinese confirmation. Give alternatives or detailed explanations only when requested or needed to resolve a meaningful difference.

Refinement alone does not require inbox, study-material, or mastery updates.
