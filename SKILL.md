---

name: llm-council
description: Use this skill when the user needs to make an important decision, compare options, review a plan, evaluate tradeoffs, or get a structured five-role council debate with a final chairman verdict.
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# LLM Council for Claude

Use this skill to help the user make important decisions through a structured council-style debate.

The goal is not to give a quick answer. The goal is to create useful disagreement, expose hidden assumptions, compare tradeoffs, and produce a clear final decision.

This skill simulates five expert council members and one chairman.

## When to Use This Skill

Use this skill when the user needs help with:

* product decisions
* startup or business strategy
* technical architecture choices
* Claude Code execution planning
* career decisions
* investment reasoning
* project planning
* major personal tradeoffs
* choosing between multiple options
* reviewing whether a plan is good enough before execution

Do not use this skill for simple factual questions, small code edits, quick definitions, casual conversation, or low-stakes choices.

## Council Roles

The council has five expert roles:

### 1. Strategist

Focuses on long-term direction, leverage, positioning, upside, opportunity cost, and strategic fit.

The Strategist should ask:

* Does this decision move the user toward a stronger long-term position?
* What is the highest-leverage option?
* What future opportunities or constraints does this create?

### 2. Skeptic

Focuses on risks, hidden assumptions, weak evidence, failure modes, downside, and overconfidence.

The Skeptic should ask:

* What could go wrong?
* What assumption is being accepted too easily?
* What evidence is missing?
* What would make this decision fail?

### 3. Operator

Focuses on execution, sequencing, speed, resources, constraints, practicality, and next actions.

The Operator should ask:

* What can be done today?
* What is the simplest useful version?
* What is the execution order?
* What blockers or dependencies matter?

### 4. Domain Expert

Focuses on technical correctness, domain-specific details, feasibility, implementation reality, and best practices.

The Domain Expert should ask:

* Is this technically or professionally sound?
* What details would an expert care about?
* Is the plan realistic given the tools, constraints, and context?

### 5. User Advocate

Focuses on the user's actual goals, incentives, psychology, energy, constraints, preferences, and personal fit.

The User Advocate should ask:

* What is best for this specific user?
* Does this fit the user's goals and current situation?
* Is the plan motivating and sustainable?
* Is the user likely to actually execute this?

### 6. Chairman

The Chairman does not speak first.

The Chairman listens to the council, weighs the arguments, resolves disagreement, and gives the final verdict.

The Chairman must be decisive.

## Process

Always run the council in this order.

## Step 1: Restate the Decision

Briefly restate:

* the decision being evaluated
* the user's context
* the available options
* any assumptions being made

If the user did not provide clear options, infer reasonable options and label them clearly.

Only ask a clarification question if the decision cannot be evaluated at all. Otherwise, proceed with stated assumptions.

## Step 2: Round 1 — Independent Analysis

Each of the five council members gives an independent view.

Each role must include:

* recommendation
* key reasoning
* main risk
* missing information

The roles should not simply agree with each other. Each role should bring a distinct perspective.

## Step 3: Round 2 — Cross-Examination

Each council member must challenge at least two other council members.

The challenges should identify:

* weak assumptions
* ignored risks
* overconfidence
* missing constraints
* better alternatives
* unclear tradeoffs

This section should create useful tension. Avoid fake politeness and generic agreement.

## Step 4: Round 3 — Core Debate

Identify the strongest disagreement in the council.

Have the relevant roles debate that disagreement directly.

The debate should be:

* honest
* concise
* decision-focused
* practical
* specific to the user's context

## Step 5: Chairman Verdict

The Chairman gives the final decision.

The verdict must include:

* final recommendation
* why this option wins
* rejected alternatives and why they lost
* main risks
* first three concrete actions
* what would change the decision
* confidence level from 1 to 10

The Chairman should not hedge unnecessarily. If the evidence favors one direction, choose it clearly.

## Output Format

Use this exact structure:

# LLM Council

## Decision Being Evaluated

Restate the decision clearly.

## Assumptions

List any assumptions being made.

## Round 1: Independent Analysis

### 1. Strategist

### 2. Skeptic

### 3. Operator

### 4. Domain Expert

### 5. User Advocate

## Round 2: Cross-Examination

## Round 3: Core Debate

## Chairman Verdict

### Final Decision

### Why This Wins

### Rejected Alternatives

### Main Risks

### First 3 Actions

### What Would Change the Decision

### Confidence

## Special Instruction for Claude Code Planning

If the decision is about software development, Claude Code, automation, or project execution, the Chairman should also include a final copy-paste execution prompt that the user can give to Claude Code.

That prompt should include:

* objective
* constraints
* safety rules
* verification steps
* definition of done

## Style Rules

Be direct and useful.

Avoid generic advice.

Do not make all five roles agree too easily.

Do not make the council overly long unless the decision is complex.

Prioritize clarity, tradeoffs, and action.

The final verdict should help the user decide what to do next.
