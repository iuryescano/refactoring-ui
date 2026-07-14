# Refactoring UI Skill

An unofficial Agent Skill inspired by *Refactoring UI* by Steve Schoger and Adam Wathan.

This project turns the book's visual refactoring mindset into an original, Markdown-first skill for AI coding agents working on web apps, dashboards, forms, product screens, landing pages, component libraries, and screenshots. It is not affiliated with the authors and does not reproduce the book text.

The skill helps an agent diagnose visual communication first, then make focused improvements to hierarchy, grouping, spacing, typography, action priority, color, depth, imagery, states, and finishing polish.

## What's Included

```text
refactor-ui/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── heuristics.md
    └── recipes.md
```

- `SKILL.md` is the main agent-facing playbook.
- `references/heuristics.md` is the full visual audit checklist.
- `references/recipes.md` contains concrete refactoring moves for common UI problems.
- `agents/openai.yaml` is optional metadata for OpenAI/Codex-style skill UIs.

## Install With Your Agent

If you are using an Agent Skills-compatible tool such as Codex, Claude Code, Cursor, Kilo Code, or another coding agent, you can ask the agent to install this skill for you:

```text
Install the refactor-ui skill from https://github.com/iuryescano/refactoring-ui.
Configure it for this agent environment, keep the references/ directory intact, reload or restart the agent if required, and confirm that the skill is available.
```

The agent should handle the correct local setup for its environment, such as copying `refactor-ui/` into the appropriate skills directory, preserving bundled references, and making the skill available as `refactor-ui`.

## Manual Install For Codex

Clone the repo and copy the skill folder into your Codex skills directory:

```bash
git clone https://github.com/iuryescano/refactoring-ui.git
cp -R refactoring-ui/refactor-ui ~/.codex/skills/
```

Then invoke it explicitly:

```text
Use $refactor-ui to audit and refactor this interface.
```

## Use With Any Agent

This repository is intentionally Markdown-first. Any capable coding agent can use it by reading `refactor-ui/SKILL.md` before working on UI refactoring tasks.

Suggested agent instruction:

```text
Use the UI refactoring playbook at refactor-ui/SKILL.md. Read the linked references only when needed, preserve the existing product behavior, and verify the result at desktop and mobile widths.
```

For agent systems that support reusable instructions, copy the whole `refactor-ui/` directory into that system's skill, rule, memory, or prompt-library format. Keep the relative paths intact so `SKILL.md` can point to `references/heuristics.md` and `references/recipes.md`.

## Design Philosophy

- Improve clarity before adding decoration.
- Reuse the local design system before inventing new styles.
- Make the main object and primary action obvious.
- Prefer small, high-leverage visual changes over broad rewrites.
- Verify responsiveness, contrast, interaction states, and layout polish.

## License

MIT
