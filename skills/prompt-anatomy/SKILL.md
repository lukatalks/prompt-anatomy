---
name: prompt-anatomy
description: Restructures any user prompt into the 6-part Claude prompt anatomy (Role, Task, Context, Reasoning, Stop Conditions, Output). Identifies missing components and asks the user to fill gaps before producing a polished, copy-paste-ready prompt. Use when the user wants to improve, structure, or format a prompt for Claude or any LLM.
license: MIT
metadata:
  author: lukatalks
  version: "1.0.0"
  domain: productivity
  triggers: structure my prompt, format this prompt, prompt anatomy, improve my prompt, make this prompt better, rewrite this prompt, optimize prompt structure
  role: expert
  scope: design
  output-format: document
  related-skills: prompt-engineer, create-meta-prompts
---

# Prompt Anatomy Formatter

Restructure any prompt into the proven 6-part anatomy for maximum clarity and effectiveness.

## The 6 Components

Every well-structured prompt has up to six components. Not all are required for every prompt — simple tasks may only need 2-3. The skill judges which are relevant.

### 1. Role
Who Claude should act as. Sets expertise, perspective, and tone.
- Example: *"Act as a senior go-to-market strategist with deep expertise launching early-stage SaaS tools. Prioritize traction speed over brand perfection."*

### 2. Task
What to do. The core request — clear, specific, and scoped.
- Example: *"Build a 90-day launch plan for a new AI productivity tool for founders. Validate the core messaging, end with a launch-ready brief."*

### 3. Context
What the user already knows or has. Background info, constraints, data, team size, tools, prior decisions.
- Example: *"Product: AI task manager for founders (25-40). Team: 2-person. Resources: Lean budget, 15-20 beta users. Key Risks: Adoption, Retention, Positioning."*

### 4. Reasoning
Why this approach matters. Helps Claude understand intent and make better tradeoff decisions.
- Example: *"The goal is a crisp, launch-ready strategy. By locking in ICP clarity upfront and asking you to defend each step, the output will be truly actionable and founder-grade."*

### 5. Stop Conditions
When to stop. Defines completeness so Claude doesn't over- or under-deliver.
- Example: *"Only stop when: A 12-week roadmap with 3-4 actions/week. Every action links to the risk it addresses. Plan ends with a final Launch Decision Gate."*

### 6. Output
How to format the result. Structure, format, level of detail.
- Example: *"Present as a weekly sprint plan. For each action: Action, Owner, Risk, Rationale + Output."*

## Process

### Step 1: Analyze the user's prompt
Read the prompt and identify which of the 6 components are already present (even if informal or scattered). Map each sentence or phrase to its component.

### Step 2: Identify gaps
Determine which components are missing. Not every prompt needs all 6 — use judgment:

**Always needed:** Task
**Usually needed:** Role, Output
**Needed for complex tasks:** Context, Reasoning, Stop Conditions
**Rarely needed for simple asks:** Stop Conditions, Reasoning

### Step 3: Ask for missing information
For each missing component that would meaningfully improve the prompt, ask the user a specific question. Be concise — one question per component, not a wall of text.

Format questions as:

```
I've identified your prompt has: [list present components]

To strengthen it, I need a few details:

- **Role**: Who should I act as? (e.g., senior marketer, technical architect, startup advisor)
- **Context**: [specific question based on the task, e.g., "What's your team size and budget?"]
- **Stop Conditions**: How will you know the output is complete enough?
```

Only ask about components that matter for this specific prompt. Skip components that would be overkill.

### Step 4: Assemble the structured prompt
Once the user provides the missing info (or says to proceed without it), produce the final prompt with clear visual separation between components. Use this format:

```
Act as [Role].

[Task — what to do, clearly stated].

Here's what I know:
- [Context point 1]
- [Context point 2]
- [Context point 3]

[Reasoning — why this matters, what tradeoffs to make].

Only stop when:
- [Stop condition 1]
- [Stop condition 2]
- [Stop condition 3]

[Output — how to format the result].
```

## Rules

- Do NOT wrap the final prompt in a code block — present it as clean text the user can copy directly
- Keep the language natural, not robotic. Each section should flow, not read like a form
- If the user's original prompt is already well-structured, say so and only suggest minor improvements
- For simple prompts (e.g., "write me a tweet about X"), don't force all 6 components — just suggest the 1-2 additions that would help most
- Preserve the user's voice and intent. Restructure, don't rewrite their ideas
- After presenting the structured prompt, briefly explain what changed and why
