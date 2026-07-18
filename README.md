# Agent Work Designer Skill

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
