# LLM Council for Claude

A lightweight Claude Code skill that simulates a five-role expert council and chairman for structured decision-making.

Inspired by Andrej Karpathy’s LLM Council idea, this skill brings a council-style decision process directly into Claude Code. Instead of asking Claude for one quick answer, LLM Council creates multiple expert perspectives, forces them to challenge each other, and then produces a final chairman verdict.

This is not a multi-model OpenRouter app. It is a simple Claude Code skill designed to be copied, installed, and used inside Claude.

## Why

Most important decisions are not simple Q&A problems.

Good decisions require:

* multiple perspectives
* disagreement
* risk analysis
* tradeoff comparison
* execution planning
* a clear final decision

LLM Council helps you think through major decisions more clearly by simulating a structured council meeting inside Claude Code.

## How It Works

The council includes five expert roles and one chairman:

1. **Strategist** — long-term direction, leverage, positioning, and opportunity cost
2. **Skeptic** — risks, hidden assumptions, failure modes, and downside
3. **Operator** — execution, sequencing, resources, speed, and next steps
4. **Domain Expert** — technical/domain correctness, feasibility, and implementation reality
5. **User Advocate** — user goals, constraints, psychology, incentives, and personal fit
6. **Chairman** — listens to the council, resolves disagreement, and gives the final verdict

## Council Process

Each decision goes through four stages:

1. **Round 1: Independent Analysis**
   Each role gives its own recommendation, reasoning, risks, and missing information.

2. **Round 2: Cross-Examination**
   The roles challenge each other’s assumptions, weak points, and blind spots.

3. **Round 3: Core Debate**
   The strongest disagreement is debated directly.

4. **Chairman Verdict**
   The chairman produces the final recommendation, rejected alternatives, risks, next actions, and confidence level.

## Use Cases

LLM Council is useful for:

* product decisions
* startup strategy
* technical architecture
* career choices
* investment reasoning
* project planning
* Claude Code execution planning
* major personal tradeoffs

## Installation

Clone this repository into your Claude Code skills folder:

```bash
git clone https://github.com/YOUR_USERNAME/llm-council.git ~/.claude/skills/llm-council
```

Or copy `SKILL.md` manually into:

```text
~/.claude/skills/llm-council/SKILL.md
```

For a project-specific installation, copy it into:

```text
your-project/.claude/skills/llm-council/SKILL.md
```

Then use it in Claude Code:

```text
/llm-council
```

## Example

```text
/llm-council

Decision:
Should I build this project as a Claude Code skill or a full web app?

Context:
I want a lightweight open-source tool that helps me make better decisions inside Claude.

Options:
A. Claude Code skill
B. Web app
C. CLI tool
```

## Philosophy

The goal is not to replace human judgment.

The goal is to make important decisions more structured, less impulsive, and more honest by forcing useful disagreement before reaching a final verdict.
