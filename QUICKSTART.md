# Quick Start

This repository is optimized for **OpenClaw** and is most useful when you want an agent to go beyond “pick a pretty style” and actually preserve design logic through implementation.

## 1) Install or copy the skill into your workspace

Place the skill folder at:

```text
<workspace>/skills/ui-craft-pro/
```

If you are using the same workspace layout as Aira:

```text
/home/aira/.openclaw/workspace/skills/ui-craft-pro/
```

Or install from ClawHub:

```bash
clawhub install ui-craft-pro
```

## 2) Use it on a real UI problem

Good task types:
- build a landing page
- improve a dashboard
- redesign a page that feels generic
- choose a visual direction before coding
- make a page feel more like a strong known product/system without copying it blindly

The skill is designed to help with:
- design direction
- style-cloning briefs
- implementation mapping
- anti-generic correction
- post-build review

## 3) Generate a design system first

```bash
python3 skills/ui-craft-pro/scripts/search.py "gaming landing page bold neon competitive" --design-system -p "Neon Rift"
```

```bash
python3 skills/ui-craft-pro/scripts/search.py "fintech dashboard minimal premium trustworthy" --design-system -p "VaultFlow"
```

## 4) Use style signatures for “X-like, but mine” work

```bash
python3 skills/ui-craft-pro/scripts/style_signature.py "developer docs premium monochrome"
python3 skills/ui-craft-pro/scripts/style_signature.py "commerce admin friendly operational"
python3 skills/ui-craft-pro/scripts/style_signature.py "ai search knowledge calm minimal"
```

Use this when the real request is something like:
- make this feel more GitHub-like
- give this a Vercel-ish premium developer vibe
- move this toward Perplexity-like calm knowledge UI
- make this more Shopify-like for merchant/admin workflows

## 5) Search the new reference layers directly

```bash
python3 skills/ui-craft-pro/scripts/search.py "github-like developer docs" --domain style-signatures
python3 skills/ui-craft-pro/scripts/search.py "enterprise workflow collaboration" --domain design-systems
python3 skills/ui-craft-pro/scripts/search.py "ai answer prompt sources" --domain patterns-shells
python3 skills/ui-craft-pro/scripts/search.py "too many gradients fake premium" --domain anti-generic-ui
```

## 6) Narrow the search if the first result is wrong

```bash
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain style
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain color
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain typography
```

## 7) Package into a distributable `.skill`

```bash
python3 ~/.npm-global/lib/node_modules/openclaw/skills/skill-creator/scripts/package_skill.py /path/to/ui-craft-pro ./dist
```

## Recommended workflow

1. understand the product
2. generate or infer a direction
3. correct drift if needed
4. extract a style signature if a reference vibe matters
5. lock implementation choices
6. code the UI
7. run anti-generic + review passes before shipping
