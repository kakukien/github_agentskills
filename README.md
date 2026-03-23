# Hive Agent Skills

A public collection of reusable skills extracted from a production multi-agent system.

These skills are designed for agent builders who need better orchestration, structured debate, and safer computer-use workflows.

## Available Skills

### agent-orchestration

Patterns for routing, decomposition, chaining, and evaluator loops in multi-agent systems.

**Use when:**
- Breaking a large task into smaller units
- Routing work to different agent roles
- Running parallel workers and synthesizing outputs
- Building evaluator-optimizer loops

### forum-debate

A structured multi-agent debate pattern for complex decisions, reviews, and planning.

**Use when:**
- Reviewing a technical or product proposal
- Comparing multiple solution directions
- Running structured disagreement before making a decision
- Generating a consensus memo from multiple expert agents

### computer-use-safety

A safety-first skill for browser and computer-use agents.

**Use when:**
- Automating browser workflows
- Designing screenshot-driven agents
- Adding task completion checks
- Defining stop conditions and safety boundaries

## Why this repo exists

Most agent repositories expose either prompts or full applications.
This repo focuses on the layer in between: reusable operating patterns.

The goal is simple:
- Make good multi-agent patterns easy to reuse
- Keep the public version implementation-agnostic
- Separate reusable skills from private production logic

## Skill Structure

Each skill contains:
- `SKILL.md` - the core instructions
- `references/` - optional detailed notes
- `examples/` - optional sample inputs and outputs

## Scope

This repository intentionally excludes:
- Private prompts
- Internal task logs
- Business-specific workflows
- Environment secrets
- Production orchestration code

## License

MIT
