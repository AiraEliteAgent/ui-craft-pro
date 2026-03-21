# UI Craft Pro

<p align="center">
  <b>An OpenClaw-compatible skill for turning UI direction into real implementation.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/OpenClaw-Agent%20Skill-2563EB?style=for-the-badge" alt="OpenClaw Agent Skill">
  <img src="https://img.shields.io/badge/python-3.x-F59E0B?style=for-the-badge&logo=python&logoColor=white" alt="Python 3.x">
  <img src="https://img.shields.io/badge/status-private-111827?style=for-the-badge" alt="Private Repo">
  <img src="https://img.shields.io/badge/focus-design%20to%20implementation-10B981?style=for-the-badge" alt="Design to Implementation">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/workflow-direction%20%E2%86%92%20tokens%20%E2%86%92%20code%20%E2%86%92%20review-64748B?style=flat-square" alt="Workflow">
  <img src="https://img.shields.io/badge/agent%20ready-yes-22C55E?style=flat-square" alt="Agent Ready">
  <img src="https://img.shields.io/badge/OpenClaw-packaged%20.skill-9333EA?style=flat-square" alt="Packaged Skill">
</p>

---

## Overview

`ui-craft-pro` is built for one specific job:

> help an AI agent produce UI that feels intentional, coherent, and product-aware — not just “good enough”.

A lot of AI-generated UI fails in predictable ways:
- it looks generic
- it chooses the wrong emotional tone
- it mixes visual systems without noticing
- it stops at style ideas instead of following through into implementation
- it ships before checking whether the final result still matches the chosen direction

This skill exists to reduce that drift.

It pushes an agent through a stricter path:

**product intent → design direction → implementation choices → real UI → review**

That sounds simple, but in practice this is the difference between:
- “some AI-made landing page”
- and a page that actually feels like it belongs to the product it was made for

---

## Philosophy

`ui-craft-pro` is not a gallery of styles.
It is not just a dataset of palettes and fonts.
It is not a prompt pack for making screens look prettier.

The real value is in the behavior it teaches:

1. **Understand the product first**
2. **Choose a direction that fits the product**
3. **Correct the direction if the first pass is emotionally wrong**
4. **Lock implementation decisions before coding**
5. **Build the interface to match the system**
6. **Review the output before presenting it as done**

That is why the workflow matters more than the raw assets.

---

## What this project contains

### Core skill
- **`SKILL.md`** — trigger description and core instructions for the agent

### Local design knowledge base
- **`data/`** — bundled design data for styles, colors, typography, landing patterns, UX guidance, chart choices, product mappings, and reasoning support

### Search and generation tools
- **`scripts/search.py`** — search interface and design-system generation entry point
- **`scripts/core.py`** — local search engine over the bundled design data
- **`scripts/design_system.py`** — design-system generation logic

### Practical references
- **`references/implementation-patterns.md`** — how to map direction into tokens, components, layout, and stack-aware decisions
- **`references/review-checklist.md`** — how to run a final UI quality pass
- **`references/product-archetypes.md`** — how to detect and correct emotionally wrong first-pass outputs

---

## What makes this different

Most “UI skills” can help with:
- picking a style
- choosing a palette
- finding a font pairing
- suggesting a page structure

That is useful, but incomplete.

`ui-craft-pro` focuses on what usually breaks after that:
- the implementation drifts away from the original design direction
- the page looks fine in pieces but inconsistent as a whole
- the first generated direction is technically valid but wrong for the product
- the final result is never reviewed against the intended vibe

This project is built around solving those exact failures.

---

## Workflow

### 1) Understand the product
Identify:
- what the product is
- who it is for
- what emotional tone it should create
- what kind of trust, energy, clarity, or restraint it needs

### 2) Generate a first design direction
Use the bundled tools to get an initial design system.

### 3) Correct drift when needed
If the first generated system is plausible but wrong, do not follow it blindly.
Narrow the search, identify the real archetype, and correct the direction.

### 4) Lock implementation choices
Before coding, decide:
- tokens
- typography roles
- section structure
- component family treatment
- motion intensity
- anti-patterns to avoid

### 5) Implement the UI
Translate the chosen design system into real code.

### 6) Review before shipping
Check whether the built result is still:
- coherent
- readable
- product-appropriate
- visually intentional
- consistent with the original direction

---

## Quick usage

### Generate a design system

```bash
python3 skills/ui-craft-pro/scripts/search.py "gaming landing page bold neon competitive" --design-system -p "Neon Rift"
```

```bash
python3 skills/ui-craft-pro/scripts/search.py "fintech dashboard minimal premium trustworthy" --design-system -p "VaultFlow"
```

### Narrow the search when the first result is wrong

```bash
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain style
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain color
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain typography
python3 skills/ui-craft-pro/scripts/search.py "privacy app landing minimal premium proof features calm" --domain landing
```

---

## Best use cases

This skill is most useful when an agent needs to work on:
- landing pages
- product marketing pages
- dashboards
- admin/operator tools
- app interfaces
- UI polish or refinement passes
- product-specific direction setting before implementation
- tasks where the real brief is “make this feel right, not just functional”

---

## Reference files

### Implementation mapping
[`references/implementation-patterns.md`](references/implementation-patterns.md)

Use this when moving from direction into code.
It helps the agent map:
- style → tokens
- design system → component rules
- product vibe → actual implementation behavior

### Review pass
[`references/review-checklist.md`](references/review-checklist.md)

Use this after coding.
It helps catch:
- generic output
- weak hierarchy
- inconsistent component families
- weak UX detail
- overused visual effects

### Product correction
[`references/product-archetypes.md`](references/product-archetypes.md)

Use this when the first generated direction is technically valid but emotionally wrong.
Especially useful for:
- privacy-first tools
- journaling / reflection products
- calm / wellness software
- trust-heavy enterprise tools

---

## Example lessons from testing

This project was not shaped in theory alone.
It has already been iterated through practical demos and cross-agent testing.

### Gaming landing page test
Used to build a high-energy gaming landing page with stronger structure, more deliberate typography, and a clearer visual rhythm than default AI output.

### Fintech / treasury control test
Used to build a cleaner premium interface with minimal structure, liquid-glass treatment, and stronger CTA discipline.

### Privacy journaling cross-agent test
This test exposed one of the most important lessons in the project:
- the first generated design system can still drift toward a generic mobile-app pattern
- but the skill was strong enough to let another agent detect that mismatch, narrow the search, correct the direction, and build something calmer and more product-appropriate

That lesson is now part of the skill itself.

---

## Repository structure

```text
ui-craft-pro/
├── SKILL.md
├── README.md
├── CHANGELOG.md
├── data/
├── scripts/
└── references/
```

---

## Packaging

To package the skill into a distributable `.skill` file:

```bash
python3 ~/.npm-global/lib/node_modules/openclaw/skills/skill-creator/scripts/package_skill.py /path/to/ui-craft-pro ./dist
```

---

## Roadmap direction

Near-term improvements that matter most:
- stronger product-archetype correction for calm / reflective / trust-heavy products
- better first-pass design-system matching for less generic output
- more stack-aware implementation patterns
- continued iteration from real production tasks instead of theory-only expansion

---

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

---

## Credits

This project is an OpenClaw-oriented adaptation inspired by the ideas and structure of:
- **UI UX Pro Max Skill** by Next Level Builder
- Source project: <https://github.com/nextlevelbuilder/ui-ux-pro-max-skill>

This repository is **not** a mirror of the original project.
It is a focused adaptation shaped around:
- OpenClaw usage
- agent workflow
- design-to-implementation discipline
- post-build review behavior
- practical correction of emotionally wrong first-pass output

---

## Thanks

Special thanks to the original project for the inspiration and the initial data/search structure that made this adaptation possible.
