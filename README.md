# Hive Pheromones Agent Skills

## English

A public repository of reusable skills extracted from a production multi-agent system.

This repository is built around a simple idea: strong agent systems are not made only of prompts or tools. They also depend on operating patterns.

In our internal system, these patterns are treated like pheromones in a hive:
- they guide routing
- they preserve working habits
- they make collaboration repeatable
- they keep multi-agent work from collapsing into noise

This public repository contains the reusable part of that layer.

It focuses on method, not on private implementation.

## What this repository is

This is a skills library for agent builders who want stronger collaboration patterns in real work.

It is designed for workflows such as:
- task decomposition
- agent routing
- structured disagreement
- consensus building
- browser and computer-use safety
- context layering and memory-oriented collaboration

## What is public here

This repository includes:
- reusable `SKILL.md` files
- public operating patterns
- framework-agnostic instructions
- patterns that can be adapted into other agent systems

## What is intentionally not public

This repository does not include:
- private prompts
- production task logs
- internal orchestration code
- business-specific workflows
- secrets or environment configuration
- private memory traces or project state

The boundary is deliberate.

The public layer should be reusable.
The private layer should remain operational.

## Current Skills

### 1. agent-orchestration

Patterns for routing, decomposition, chaining, and evaluator loops in multi-agent systems.

Best for:
- breaking large tasks into smaller units
- assigning clear ownership across agents
- running parallel workers without losing structure
- building revision loops with explicit evaluation

### 2. forum-debate

A structured multi-agent debate pattern for complex decisions, reviews, and planning.

Best for:
- comparing competing solution directions
- surfacing disagreement before making a decision
- forcing evidence-based argument instead of shallow aggregation
- producing a usable consensus memo from multiple agents

### 3. computer-use-safety

A safety-first skill for browser and computer-use agents.

Best for:
- browser automation workflows
- screenshot-driven action loops
- defining stop conditions
- adding completion checks and safety boundaries

## Why this repository exists

Many agent repositories fall into two extremes:
- raw prompt dumps
- full applications that are hard to extract patterns from

This repository sits in the middle.

It packages the transferable layer:
- how agents split work
- how they challenge each other
- how they preserve context
- how they avoid unsafe or low-signal execution

## Core Capabilities

The direction of this repository is shaped around five capability groups:

### 1. Orchestration

How one agent breaks down work and coordinates specialists.

### 2. Debate

How multiple agents disagree productively and converge on something usable.

### 3. Safety

How agent systems stop before unsafe computer actions or false success states.

### 4. Context

How working context is layered, filtered, and carried across tasks.

### 5. Memory Signals

How recurring knowledge becomes operational guidance instead of dead documentation.

## Intended Audience

This repository is useful for:
- developers building agent systems
- teams experimenting with multi-agent workflows
- researchers studying coordination patterns
- product builders who want more than single-agent chat wrappers

## Roadmap

Planned additions include skills around:
- context layering
- memory retrieval patterns
- review and critique loops
- task-board execution
- swarm-style planning
- longer creative pipelines

## Repository Structure

Each skill can contain:
- `SKILL.md` for the core instructions
- `references/` for deeper notes
- `examples/` for sample inputs and outputs

## Chinese

这是一个从真实生产型多智能体系统中抽出来的公开技能仓库。

我想公开的，不是某一套私有提示词，也不是整套内部实现，而是那层更有复用价值的东西：**协作方式本身**。

在蜂巢体系里，我把这层东西理解成“信息素”。

信息素不是结果物。
它更像一种可重复传播的工作信号：
- 哪类任务该怎么拆
- 哪些工蜂该先上
- 分歧该怎么撞开
- 上下文该怎么保留
- 风险动作该在哪一步停下

这个仓库公开的，就是这部分可以迁移、可以复用、可以被别的团队吸收的方法层。

## 这个仓库是什么

它不是聊天壳子。
也不是演示性质的 prompt dump。

它更接近一个多智能体工作模式库，重点放在：
- 编排
- 辩论
- 安全
- 上下文组织
- 记忆信号沉淀

如果你在做 agent system、workflow automation、multi-agent collaboration，这个仓库应该能给你一些真正可落的结构，而不是只有概念。

## 这里公开了什么

当前公开的是：
- 可复用的 `SKILL.md`
- 抽象后的协作模式
- 与具体框架弱绑定的方法说明
- 可以迁移到其他智能体系统里的工作结构

## 这里没有公开什么

我刻意没有放这些内容：
- 私有 prompt
- 生产任务日志
- 内部编排代码
- 强业务绑定 workflow
- 环境密钥和部署配置
- 项目态记忆、私有信息素轨迹

边界是故意保留的。

公开层应该让别人拿去复用。  
私有层应该继续服务真实生产。

## 当前 Skills

### 1. agent-orchestration

这是多智能体编排技能。

适合处理：
- 大任务拆分
- 角色路由
- 并行执行
- 链式任务
- 评估-重写循环

如果你不想让多个 agent 变成“各说各话”，这类 skill 基本是底座。

### 2. forum-debate

这是结构化辩论技能。

它解决的不是“让多个 agent 同时回答”，而是“让它们先发生有效碰撞，再给出结论”。

适合处理：
- 方案评审
- 架构争议
- 产品方向比较
- 多视角分析后形成共识

### 3. computer-use-safety

这是面向浏览器和 computer-use agent 的安全技能。

重点不是教模型怎么点按钮，而是规定：
- 什么动作能做
- 什么动作必须停
- 什么算完成
- 什么算假完成

如果没有这一层，computer-use 很容易在“看起来完成了”和“真的完成了”之间出事故。

## 为什么要做这个仓库

很多 agent 项目有两个问题。

一个问题是太虚。只有概念，没有能拿来复用的结构。  
另一个问题是太重。直接扔整套系统，别人很难抽取出可迁移的方法。

我想做的是中间这一层。

把真正有复用价值的协作模式单独抽出来，做成 skill，让外部开发者、研究者、团队都能快速理解：一个更稳的多智能体系统，到底靠什么站住。

## 我认为必要的能力层

这个仓库后续会围绕五类能力继续扩展。

### 1. 编排层

解决任务如何拆、谁先做、谁后做、怎么汇总。

### 2. 辩论层

解决多 agent 不是简单拼接输出，而是先碰撞、再收敛。

### 3. 安全层

解决 computer-use、浏览器自动化、执行型 agent 的停手边界。

### 4. 上下文层

解决不同任务、不同阶段、不同角色之间，上下文如何分层注入。

### 5. 记忆信号层

解决记忆不只是存档，而是变成后续任务还能继续调用的工作信号。

## 适合谁看

这个仓库更适合这些人：
- 在做多智能体系统的开发者
- 想把 agent 从聊天壳子推进到工作流的人
- 在研究协作结构、记忆层、调度层的人
- 想让 agent 在真实任务里更稳一点的团队

## 接下来会补什么

后续准备继续补的 skill 包括：
- context layering
- memory retrieval patterns
- review / critique loops
- task-board execution
- swarm-style planning
- 更长链路的创作型 workflow

## 仓库结构

每个 skill 后续都可以包含：
- `SKILL.md`：核心说明
- `references/`：深入资料
- `examples/`：输入输出示例

## License

MIT
