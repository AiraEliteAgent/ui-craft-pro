# ui-craft-pro

`ui-craft-pro` is an OpenClaw-compatible skill for turning UI direction into actual implementation.

It is built for agents that need to do more than say _“this style looks good”_. The goal is to help an agent:

1. understand the product and mood
2. generate or correct a design direction
3. lock visual implementation choices
4. build UI that follows that direction
5. review the result before calling it done

## What it includes

- **`SKILL.md`** — main skill instructions and trigger description
- **`data/`** — local design knowledge base (styles, palettes, typography, landing patterns, UX guidance, chart choices, product mappings)
- **`scripts/`** — local Python search and design-system generation tools
- **`references/`** — practical guidance for implementation mapping, review, and product-archetype correction

## Why this exists

A lot of AI-generated UI has the same problem:
- visually generic
- wrong mood for the product
- weak hierarchy
- good ideas, poor execution

`ui-craft-pro` tries to fix that by teaching an agent to go from:

**product intent → design direction → implementation choices → real UI**

instead of stopping at a vague style suggestion.

## Workflow

The intended workflow is:

1. **Generate a first design direction**
2. **Correct drift** if the first pass is emotionally wrong for the product
3. **Lock tokens and component rules**
4. **Implement the UI**
5. **Run a review pass** to check style fit, hierarchy, consistency, and UX quality

## Quick usage

### Generate a design system

```bash
python3 skills/ui-craft-pro/scripts/search.py "gaming landing page bold neon competitive" --design-system -p "Neon Rift"
```

```bash
python3 skills/ui-craft-pro/scripts/search.py "fintech dashboard minimal premium trustworthy" --design-system -p "VaultFlow"
```

### Search a narrower domain

```bash
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain style
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain color
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain typography
```

## Best use cases

This skill is most useful when an agent needs to work on:
- landing pages
- dashboards
- admin tools
- SaaS marketing pages
- app interfaces
- UI polish/refinement passes
- product-specific design direction before coding

## Reference files

- [`references/implementation-patterns.md`](references/implementation-patterns.md) — map a chosen design system into tokens, components, and stack-aware implementation
- [`references/review-checklist.md`](references/review-checklist.md) — review the built UI before shipping
- [`references/product-archetypes.md`](references/product-archetypes.md) — correct emotionally wrong first-pass outputs for product types like privacy, journaling, calm/wellness, enterprise, and trust-heavy software

## Packaging

To package this skill into a distributable `.skill` file:

```bash
python3 ~/.npm-global/lib/node_modules/openclaw/skills/skill-creator/scripts/package_skill.py /path/to/ui-craft-pro ./dist
```

## Current status

- Tested on internal demo tasks
- Used to build multiple demo pages with different vibes
- Iterated based on real output drift and correction behavior

## Credits

This project was adapted and expanded from ideas and assets inspired by:
- **UI UX Pro Max Skill** by Next Level Builder
- Source inspiration: <https://github.com/nextlevelbuilder/ui-ux-pro-max-skill>

This repository is **not** a mirror of the original project.
It is an OpenClaw-oriented adaptation focused on agent workflow, implementation mapping, and review discipline.

## Thanks

Special thanks to the original project for the inspiration and the initial data/search structure that made this adaptation possible.
