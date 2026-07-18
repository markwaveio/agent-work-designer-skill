# Agent Work Designer Skill

## 中文简介

Agent Work Designer 是一个用于「设计 AI Agent 工作说明书」的 Codex Skill。

它不直接替用户完成任务，而是先把模糊的自然语言需求整理成一份结构完整、可执行、可验收的 Agent Work Prompt，帮助 Agent 明确背景、目标、输入资料、执行流程、输出格式、验收标准和权限边界。

适合用于以下场景：

- 把一个粗略想法改写成 Agent 可以执行的工作提示词
- 在执行复杂任务前，先澄清目标、资料和交付标准
- 为研究、内容创作、竞品分析、自动化流程等任务设计工作说明书
- 给高质量任务加入自查、迭代和停止条件
- 将高频任务沉淀为可复用的 Skill 或自动化流程

Agent Work Designer is a Codex skill for turning fuzzy natural-language requests into structured, executable, and evaluable Agent Work Prompts.

It is designed for moments when a user does not yet need the agent to execute the work. Instead, they need the work itself to be clarified: goal, inputs, workflow, output, evaluation, permissions, and quality loop.

## What It Does

This skill helps an agent convert a rough request into a complete work specification:

```text
Background
Goal
Input
Workflow
Evaluation
Permission
Output
```

It also decides whether the task needs iterative loop logic and scores the resulting prompt out of 100.

## When To Use

Use this skill when you want to:

- Turn a vague idea into an executable agent prompt
- Improve or rewrite a prompt for better agent execution
- Clarify a task before asking an AI agent to run it
- Define acceptance criteria and permission boundaries
- Design repeatable work for content, research, analysis, automation, or operations

Example requests:

```text
帮我把这个需求整理成一个 AI Agent 可以执行的 Work Prompt。
```

```text
Design a work prompt for an agent that monitors competitor launches every week.
```

```text
把“帮我分析一下这个产品方向”改成一个可执行、可验收的任务说明。
```

## Output Pattern

The skill guides the agent to produce:

1. Task type diagnosis
2. Clarification questions when required
3. A structured Work Prompt
4. Loop logic when the task is complex or high-impact
5. A prompt quality score
6. Assumptions or missing information

## Installation

Copy this repository folder into your Codex skills directory:

```bash
~/.codex/skills/agent-work-designer
```

The required files are:

```text
agent-work-designer/
├── SKILL.md
└── agents/
    └── openai.yaml
```

Restart Codex or reload skills if needed so the new skill is discovered.

## Files

- `SKILL.md`: The actual skill instructions and trigger metadata
- `agents/openai.yaml`: UI metadata for display name, short description, and default prompt

## Core Idea

```text
Prompt: tell AI what to do.
Skill: tell AI how to do it well.
Loop: tell AI when the work is good enough to stop.
Work: define what is worth giving to AI.
```
