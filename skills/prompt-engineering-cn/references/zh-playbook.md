# Chinese Prompt Playbook

This reference is a Chinese-oriented adaptation of the DAIR Prompt Engineering Guide techniques.

## Recommended escalation order

1. Clarify task and output schema.
2. Write a clean zero-shot prompt.
3. Add one or two few-shot examples only if format or label boundaries drift.
4. Add decomposition if multiple jobs are mixed together.
5. Add grounding and uncertainty rules if facts matter.
6. Add injection defense if third-party text is involved.

## Default Chinese prompt skeleton

```text
你是[角色]。

任务：
[一句话说明目标]

输入说明：
[输入数据是什么，边界是什么]

执行要求：
1. [要求 1]
2. [要求 2]
3. 如果信息不足，明确说明“信息不足”，不要猜测。

输出格式：
[明确字段、顺序、JSON schema 或模板]

输入数据：
<<<
[原始输入]
>>>
```

## Common failure modes

### Output not stable

- schema not explicit
- optional fields not defined
- empty-value behavior missing
- examples inconsistent

### Hallucinations

- prompt asks for completion instead of evidence-bound answer
- uncertainty behavior not specified
- source boundary not defined

### Prompt injection risk

- retrieved text mixed with instructions
- no statement that external content is data only
- no fallback when sources conflict with task rules

## Chinese evaluation checklist

- Is the task restated correctly?
- Is the output format explicit enough to parse?
- Are unsupported claims handled safely?
- Would a Chinese-speaking operator copy this prompt without extra editing?
- Are labels, field names, and examples easy to understand?
