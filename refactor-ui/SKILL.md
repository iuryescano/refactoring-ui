---
name: refactor-ui
description: Practical UI refactoring and visual design review for web apps, dashboards, forms, product screens, landing pages, component libraries, and screenshots. Use when an AI coding agent needs to improve an existing interface, audit visual polish, redesign a rough UI, review frontend code for hierarchy/spacing/typography/color/depth/image issues, or turn a plain implementation into a cleaner product-quality screen.
---

# Refactor UI

## Overview

Refactor interfaces by diagnosing visual communication first, then applying focused changes to hierarchy, spacing, typography, color, depth, imagery, states, and polish. Favor small, high-leverage improvements that make the UI easier to understand and more deliberate.

This skill is an original operational playbook derived from UI refactoring principles. Do not reproduce long passages from source material; use the references here as working heuristics.

## Core Workflow

1. Identify the user's job, the main object on the screen, and the one or two primary actions.
2. Audit the current UI in this order: hierarchy, grouping, spacing, typography, action priority, color, depth, imagery, states, and final polish.
3. Read `references/heuristics.md` when you need the full checklist for a screen or component.
4. Read `references/recipes.md` when you need concrete refactoring moves for common weak UI patterns.
5. Implement changes in the codebase using existing design tokens, components, CSS utilities, and local conventions first.
6. Verify at desktop and mobile widths. If a browser is available, inspect screenshots for overlap, cramped spacing, weak contrast, broken line lengths, awkward empty states, and unintended layout shifts.
7. Report the most important visual changes and any remaining tradeoffs.

## Refactoring Priorities

Use this priority order unless the user asks for a specific visual area:

1. Clarify importance: make the primary content/action visually dominant and de-emphasize supporting material.
2. Make grouping obvious: use spacing, background contrast, and structure before adding borders.
3. Constrain choices: reuse a small scale for font sizes, spacing, radii, shadows, and colors.
4. Improve readability: control line length, line height, alignment, labels, and numerical data.
5. Make color systematic: use palette shades intentionally and preserve accessible contrast.
6. Add depth only when it communicates layering, elevation, focus, or interaction.
7. Handle images deliberately: crop, size, mask, overlay, and protect text contrast.
8. Polish default states: empty, loading, disabled, selected, hover, focus, error, and success states.

## Implementation Guidance

- Prefer removing competition over adding decoration.
- Use semantic markup for accessibility, then style independently for visual hierarchy.
- Avoid arbitrary one-off values when an existing spacing, type, color, radius, or shadow scale exists.
- For Tailwind projects, prefer existing theme tokens and utility patterns; add custom values only when the local system clearly lacks a needed step.
- For component libraries, extend nearby variants and states instead of creating parallel styling systems.
- Keep dense operational UIs efficient. Better polish does not mean larger hero-like sections, oversized cards, or decorative clutter.
- Preserve functional behavior and test selectors while changing presentation.

## Output Expectations

When auditing only, lead with the highest-impact issues and concrete fixes. When implementing, make the UI visibly cleaner, run the relevant checks, and summarize the finished changes briefly.
