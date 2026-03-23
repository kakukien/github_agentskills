# Agent Orchestration

## What this skill does

This skill packages the operating patterns used to coordinate multiple agents on one task.

It focuses on structure before output:
- route the task
- split the work
- assign ownership
- run independent steps in parallel when possible
- preserve order when steps depend on each other
- synthesize outputs without losing provenance

## Why it matters

Many multi-agent systems fail for predictable reasons:
- too many agents are used too early
- decomposition starts before the output is defined
- dependent steps are parallelized by mistake
- synthesis collapses disagreement into vague summaries

This skill exists to make multi-agent execution more stable, more legible, and easier to reuse.

## Best use cases

Use this skill when you need to:
- investigate a codebase across multiple files
- route work to different specialist agents
- run orchestrator-worker pipelines
- build chained workflows
- add evaluator-optimizer loops to improve output quality

## Included patterns

### Routing

Choose the right owner before execution begins.

### Orchestrator-Workers

One coordinator breaks the task into smaller units and later merges the outputs.

### Chaining

One step feeds the next when the workflow is sequential.

### Evaluator-Optimizer

One agent generates. Another evaluates. The generator revises until the result is strong enough or the retry budget is exhausted.

## Minimal output shape

A practical worker output usually contains:

```text
{
  owner,
  task,
  findings,
  confidence,
  open_questions,
  artifacts
}
```

## When not to use it

Do not use this skill when:
- the task is simple enough for one agent
- the objective is still vague and needs clarification first
- coordination overhead costs more than it saves

## Files

- `SKILL.md` - compact instructions for agent use
- `README.md` - public explanation for human readers
