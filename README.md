# Prompt Engineering Skills

Codex skills derived from the [DAIR Prompt Engineering Guide](https://github.com/dair-ai/Prompt-Engineering-Guide), adapted for practical assistant workflows.

This repository ships two installable skills:

- `prompt-engineering-guide`
  General-purpose prompt engineering for prompt design, critique, reliability, grounding, and prompt-injection defense.
- `prompt-engineering-cn`
  Chinese-first prompt engineering for Chinese and bilingual workflows, Chinese deliverables, and business-style prompt requests.

## What is included

- Source skills in `skills/`
- Packaged `.skill` artifacts in `packages/`
- Reference notes and eval prompts for future iteration

## Repository layout

```text
skills/
  prompt-engineering-guide/
  prompt-engineering-cn/

packages/
  prompt-engineering-guide.skill
  prompt-engineering-cn.skill
```

## Install

Option 1: copy a source folder into your Codex skills directory.

```powershell
Copy-Item -Recurse -Force .\skills\prompt-engineering-guide C:\Users\<you>\.codex\skills\
Copy-Item -Recurse -Force .\skills\prompt-engineering-cn C:\Users\<you>\.codex\skills\
```

Option 2: import a packaged `.skill` artifact if your Codex environment supports package import.

## Which skill to use

Use `prompt-engineering-guide` when:

- the task is mainly in English
- you want a general prompt engineering playbook
- you need help with grounding, few-shot design, structured output, or prompt injection defense

Use `prompt-engineering-cn` when:

- the user works mainly in Chinese
- the final prompt should be Chinese or bilingual
- examples, schemas, or output labels should feel natural in Chinese business workflows

## Source basis

These skills are adaptations, not verbatim copies. The main source is:

- [dair-ai/Prompt-Engineering-Guide](https://github.com/dair-ai/Prompt-Engineering-Guide)

Some older prompt patterns were intentionally modernized for assistant products, with more emphasis on:

- decomposition instead of verbose exposed reasoning
- grounded outputs
- prompt-injection defense
- practical prompt evaluation

## Notes

- Packaged `.skill` files intentionally exclude `evals/`, matching typical skill packaging behavior.
- Source skill folders in `skills/` keep `evals/` and references for editing and iteration.
