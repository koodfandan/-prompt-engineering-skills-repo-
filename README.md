# Prompt Engineering Skills

This repository contains two Codex skills derived from the DAIR Prompt Engineering Guide and adapted for practical assistant workflows.

## Included skills

- `prompt-engineering-guide`
  - General-purpose prompt engineering skill
  - Focuses on prompt design, critique, reliability, grounding, and prompt injection defense

- `prompt-engineering-cn`
  - Chinese-first prompt engineering skill
  - Focuses on Chinese prompt workflows, Chinese deliverables, and bilingual prompt design

## Repository layout

- `skills/prompt-engineering-guide/`
- `skills/prompt-engineering-cn/`
- `packages/prompt-engineering-guide.skill`
- `packages/prompt-engineering-cn.skill`

## Source basis

The skills were created from the DAIR Prompt Engineering Guide:

- <https://github.com/dair-ai/Prompt-Engineering-Guide>

They are adaptations, not verbatim copies. In particular, some older prompt patterns were rewritten for modern assistant products, with more emphasis on decomposition, grounded outputs, and prompt-injection defense.

## Install

You can install a skill by copying the folder into your Codex skills directory, or by using the packaged `.skill` artifact if your environment supports importing packaged skills.

## Notes

- The packaged `.skill` files exclude `evals/` on purpose, matching the typical packaging behavior for skills.
- The source folders in `skills/` include `evals/` and references for further iteration.
