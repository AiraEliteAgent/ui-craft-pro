# Quick Start

This repository is optimized for **OpenClaw**.

## 1) Copy the skill into your OpenClaw workspace

Place the skill folder at:

```text
<workspace>/skills/ui-craft-pro/
```

If you are using the same workspace layout as Aira:

```text
/home/aira/.openclaw/workspace/skills/ui-craft-pro/
```

## 2) Use the skill on a real UI task

Ask OpenClaw to work on UI tasks such as:
- build a landing page
- improve a dashboard
- redesign a page that feels generic
- create a design direction before coding
- refine a product UI that needs stronger hierarchy

The skill is designed to help with:
- design direction
- implementation mapping
- post-build review

## 3) Generate a design system directly

```bash
python3 skills/ui-craft-pro/scripts/search.py "gaming landing page bold neon competitive" --design-system -p "Neon Rift"
```

```bash
python3 skills/ui-craft-pro/scripts/search.py "fintech dashboard minimal premium trustworthy" --design-system -p "VaultFlow"
```

## 4) Narrow the search if the first result is wrong

```bash
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain style
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain color
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain typography
```

## 5) Package into a distributable `.skill`

```bash
python3 ~/.npm-global/lib/node_modules/openclaw/skills/skill-creator/scripts/package_skill.py /path/to/ui-craft-pro ./dist
```

## Recommended workflow

1. generate a direction
2. correct drift if needed
3. lock implementation choices
4. code the UI
5. review before shipping
