# llm-question-pipeline

Validation, correction and narration layer for math and portuguese questions converted to JSON by an LLM.
Business rules live in YAML and the engine is generic. An LLM only handles errors no rule can fix, and a human only reviews what is left.

## The problem

Questions written in Word are converted to JSON automatically and loaded into a mobile app. LLM conversion gets the content right but the structure wrong: text in the wrong field, symbols that break LaTeX, context and question swapped. Each error only shows up when the question renders, and manual review is slow and misses cases. Questions for 1st and 2nd grade also need a narrated audio track.