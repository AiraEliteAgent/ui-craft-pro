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

`ui-craft-pro` exists to solve a very specific problem:

> most AI-generated UI can produce something “fine”, but not something that feels truly intentional.

This skill helps an agent go beyond vague style suggestions and move through a stricter path:

**product intent → design direction → implementation choices → real UI → review**

---

## Why this skill exists

A lot of AI-built UI falls into the same traps:
- generic visual language
- wrong emotional tone for the product
- weak hierarchy
- decent ideas, sloppy execution
- good-looking pieces that do not belong to the same system

`ui-craft-pro` is built to reduce that drift.

It teaches an agent to:
1. pick a direction that actually fits the product
2. correct emotionally wrong first-pass results
3. lock design decisions before coding
4. implement UI that follows the chosen system
5. review the result before calling it done

---

## What it contains

### Core skill
- **`SKILL.md`** — trigger description and working instructions for the agent

### Local design knowledge base
- **`data/`** — styles, colors, typography, landing patterns, UX guidance, chart choices, product mappings, and reasoning support data

### Search + generation tools
- **`scripts/search.py`** — search interface and design-system generation entry point
- **`scripts/core.py`** — local search engine over the bundled design data
- **`scripts/design_system.py`** — design-system generation logic

### Practical references
- **`references/implementation-patterns.md`** — how to translate a chosen design direction into code
- **`references/review-checklist.md`** — how to review built UI for style fit, consistency, and UX quality
- **`references/product-archetypes.md`** — how to correct wrong first-pass output for products that need calmer, more specific, or more trust-heavy treatment

---

## What makes this different

This is **not** just a “UI ideas” skill.

The important part is not:
- “search a style”
- “pick a font”
- “suggest a palette”

The important part is:
- choosing a direction
- locking implementation choices
- building to that direction
- reviewing whether the final page still matches it

That is why the workflow matters more than the raw dataset.

---

## Workflow

### 1) Understand the product
Figure out:
- what the product is
- who it is for
- what emotional tone it should give off
- what should feel obvious, calm, premium, energetic, or trustworthy

### 2) Generate a first design direction
Use the local search/design-system tooling to get a strong first pass.

### 3) Correct drift when needed
If the first result is technically plausible but emotionally wrong, do not follow it blindly.
Use narrower domain searches and product archetype correction.

### 4) Lock implementation choices
Before coding, decide:
- tokens
- typography roles
- section structure
- component family treatment
- motion intensity
- anti-patterns to avoid

### 5) Implement the UI
Turn the design system into real interface code.

### 6) Review before shipping
Check whether the result still feels intentional, coherent, readable, and product-appropriate.

---

## Quick usage

### Generate a design system

```bash
python3 skills/ui-craft-pro/scripts/search.py "gaming landing page bold neon competitive" --design-system -p "Neon Rift"
```

```bash
python3 skills/ui-craft-pro/scripts/search.py "fintech dashboard minimal premium trustworthy" --design-system -p "VaultFlow"
```

### Search narrower when the first result is wrong

```bash
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain style
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain color
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain typography
python3 skills/ui-craft-pro/scripts/search.py "privacy app landing minimal premium proof features calm" --domain landing
```

---

## Best use cases

`ui-craft-pro` is most useful when an agent needs to work on:
- landing pages
- product marketing pages
- dashboards
- admin/operator tools
- app interfaces
- UI polish/refinement tasks
- design direction before implementation
- “make this look less generic” style tasks

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
- broken hierarchy
- inconsistent component families
- weak UX details
- overused effects

### Product correction
[`references/product-archetypes.md`](references/product-archetypes.md)

Use this when the first generated direction is technically valid but emotionally wrong.
Especially useful for:
- privacy-first products
- journaling / reflection tools
- calm / wellness software
- trust-heavy enterprise tools

---

## Example lessons from testing

The skill has already been iterated through practical demos.

### Gaming landing page test
Used to build a high-energy gaming landing page with stronger structure, more deliberate typography, and less “default AI UI” feeling.

### Fintech / treasury control test
Used to build a cleaner premium interface with minimal structure, liquid-glass surfaces, and more focused CTA discipline.

### Privacy journaling test
Cross-agent testing showed an important lesson:
- the first generated design system can still drift toward a generic mobile-app pattern
- but the skill was strong enough to let another agent detect the mismatch, narrow the search, correct the style, and build a calmer paper-like result

That lesson is now built back into the skill.

---

## Packaging

To package the skill into a distributable `.skill` file:

```bash
python3 ~/.npm-global/lib/node_modules/openclaw/skills/skill-creator/scripts/package_skill.py /path/to/ui-craft-pro ./dist
```

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

---

## Thanks

Special thanks to the original project for the inspiration and the initial data/search approach that made this adaptation possible.
