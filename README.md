# Prompt Engineering Skills

Codex skills derived from the [DAIR Prompt Engineering Guide](https://github.com/dair-ai/Prompt-Engineering-Guide), adapted for practical assistant workflows.

基于 [DAIR Prompt Engineering Guide](https://github.com/dair-ai/Prompt-Engineering-Guide) 改写的 Codex skills，面向真实助手工作流。

This repository ships two installable skills.
这个仓库包含两个可直接安装的 skill。

- `prompt-engineering-guide`
  General-purpose prompt engineering for prompt design, critique, reliability, grounding, and prompt-injection defense.
- `prompt-engineering-cn`
  Chinese-first prompt engineering for Chinese and bilingual workflows, Chinese deliverables, and business-style prompt requests.

- `prompt-engineering-guide`
  通用 Prompt Engineering skill，覆盖提示词设计、评审、稳定性、grounding 和 prompt injection 防御。
- `prompt-engineering-cn`
  中文优先的 Prompt Engineering skill，适合中文和中英双语工作流、中文业务交付和中文提示词设计。

## What is included

- Source skills in `skills/`
- Packaged `.skill` artifacts in `packages/`
- Reference notes and eval prompts for future iteration

## 内容说明

- `skills/` 里是源码版本，适合继续编辑和迭代
- `packages/` 里是打包后的 `.skill` 文件，适合分发和导入
- 每个源码目录里都保留了 references 和 evals，方便后续优化

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

### 安装方式

方式 1：直接复制 `skills/` 里的源码目录到你的 Codex skills 目录。  
方式 2：如果你的环境支持 `.skill` 导入，直接使用 `packages/` 里的打包产物。

## Which skill to use

Use `prompt-engineering-guide` when:

- the task is mainly in English
- you want a general prompt engineering playbook
- you need help with grounding, few-shot design, structured output, or prompt injection defense

Use `prompt-engineering-cn` when:

- the user works mainly in Chinese
- the final prompt should be Chinese or bilingual
- examples, schemas, or output labels should feel natural in Chinese business workflows

### 选择建议

优先用 `prompt-engineering-guide`：

- 主要是英文任务
- 想要一个通用的 Prompt 工程工作流
- 重点在 grounding、few-shot、结构化输出、注入防御

优先用 `prompt-engineering-cn`：

- 用户主要使用中文
- 最终提示词需要是中文或中英双语
- 字段名、标签、few-shot 示例需要贴近中文业务语境

## Source basis

These skills are adaptations, not verbatim copies. The main source is:

- [dair-ai/Prompt-Engineering-Guide](https://github.com/dair-ai/Prompt-Engineering-Guide)

Some older prompt patterns were intentionally modernized for assistant products, with more emphasis on:

- decomposition instead of verbose exposed reasoning
- grounded outputs
- prompt-injection defense
- practical prompt evaluation

## 来源与改写

这些 skill 不是原仓库内容的直接复制，而是基于原始 guide 的二次整理。主要改写方向：

- 更强调任务分解，而不是暴露冗长推理
- 更强调 grounded outputs
- 更强调 prompt injection 防御
- 更强调可执行的 prompt 评测

## Notes

- Packaged `.skill` files intentionally exclude `evals/`, matching typical skill packaging behavior.
- Source skill folders in `skills/` keep `evals/` and references for editing and iteration.

## Notes / 说明

- 打包产物默认不包含 `evals/`
- 源码目录保留 `evals/` 和 references，方便后续继续打磨
