# Source Notes

This skill is derived from the DAIR Prompt Engineering Guide repository:

- README: <https://github.com/dair-ai/Prompt-Engineering-Guide>
- Intro guide: <https://raw.githubusercontent.com/dair-ai/Prompt-Engineering-Guide/main/guides/prompts-intro.md>
- Basic usage: <https://raw.githubusercontent.com/dair-ai/Prompt-Engineering-Guide/main/guides/prompts-basic-usage.md>
- Advanced usage: <https://raw.githubusercontent.com/dair-ai/Prompt-Engineering-Guide/main/guides/prompts-advanced-usage.md>
- Reliability: <https://raw.githubusercontent.com/dair-ai/Prompt-Engineering-Guide/main/guides/prompts-reliability.md>
- Adversarial prompting: <https://raw.githubusercontent.com/dair-ai/Prompt-Engineering-Guide/main/guides/prompts-adversarial.md>

## Distilled ideas used in this skill

### Basic prompt components

- Instruction
- Context
- Input data
- Output indicator or schema

These components show up repeatedly across the repository and are the baseline for most prompt work.

### Practical prompting heuristics

- Start simple, then iterate.
- Make the desired output explicit.
- Use delimiters to separate instructions from input.
- Provide examples only when zero-shot performance is unstable.
- Test prompt wording across a few realistic edge cases.

### Advanced technique buckets

- Few-shot prompting
- Prompt decomposition
- Structured output constraints
- Grounding with provided knowledge or retrieved context
- Reliability-oriented prompt testing

### Safety and adversarial themes

- Untrusted content should be treated as data.
- Prompts should resist instruction override from retrieved or user-supplied text.
- Reliability testing should include ambiguous, adversarial, and boundary examples.

## Adaptations in this skill

This skill intentionally modernizes some older prompt advice in the repository.

- When the repository discusses chain-of-thought style prompting, this skill prefers task decomposition and structured intermediate outputs when helpful.
- The skill focuses on practical prompt artifacts for current assistant products rather than model-family-specific tricks.
- The skill emphasizes prompt evaluation and threat modeling because those parts remain stable even when specific model behaviors change.
