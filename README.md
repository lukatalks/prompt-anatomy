# Prompt Anatomy

A Claude Code skill that restructures any prompt into the proven 6-part anatomy for maximum clarity and effectiveness.

Inspired by [The Anatomy of a Claude Prompt](https://x.com).

## The 6 Components

| # | Component | Purpose |
|---|-----------|---------|
| 1 | **Role** | Who Claude should act as |
| 2 | **Task** | What to do — the core request |
| 3 | **Context** | Background info, constraints, data |
| 4 | **Reasoning** | Why this approach matters |
| 5 | **Stop Conditions** | When the output is complete |
| 6 | **Output** | How to format the result |

## How It Works

1. You give it any prompt
2. It identifies which components are present and which are missing
3. It asks targeted questions to fill gaps (only what matters — not all 6 for simple prompts)
4. It produces a clean, structured, copy-paste-ready prompt

## Installation

Copy `skills/prompt-anatomy/SKILL.md` to your Claude Code skills directory:

```bash
mkdir -p ~/.claude/skills/prompt-anatomy
cp skills/prompt-anatomy/SKILL.md ~/.claude/skills/prompt-anatomy/
```

## Usage

Just say things like:
- "Structure my prompt"
- "Format this prompt"
- "Improve my prompt"
- "Make this prompt better"

## License

MIT
