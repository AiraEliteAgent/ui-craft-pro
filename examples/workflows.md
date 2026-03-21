# Example Workflows

These examples are written for **OpenClaw** usage.

## 1) Build a gaming landing page

Goal:
- high energy
- stronger typography
- clear CTA rhythm
- less generic AI landing-page feel

Suggested flow:
1. Generate a design system
2. Lock colors, type, spacing, and section structure
3. Implement hero, feature blocks, and CTA
4. Review for visual coherence and readability

Example command:

```bash
python3 skills/ui-craft-pro/scripts/search.py "gaming landing page bold neon competitive" --design-system -p "Neon Rift"
```

## 2) Build a fintech dashboard or landing page

Goal:
- premium trust
- cleaner hierarchy
- less startup noise
- stronger product credibility

Example command:

```bash
python3 skills/ui-craft-pro/scripts/search.py "fintech dashboard minimal premium trustworthy" --design-system -p "VaultFlow"
```

## 3) Correct a wrong first-pass output

Case:
- the first result is technically fine
- but emotionally wrong for the product

Example:
- privacy journaling app gets pushed toward app-store / generic SaaS styling

Correction flow:
1. identify the real archetype
2. run narrower domain searches
3. pick a calmer, more fitting direction
4. then code

Example commands:

```bash
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain style
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain color
python3 skills/ui-craft-pro/scripts/search.py "privacy focused journaling calm minimal" --domain typography
python3 skills/ui-craft-pro/scripts/search.py "privacy app landing minimal premium proof features calm" --domain landing
```

## 4) Improve an existing page

Use the skill to:
- tighten hierarchy
- improve typography
- reduce visual drift
- improve CTA focus
- make the result feel more intentional

Recommended process:
1. identify what feels wrong
2. infer the page’s intended direction
3. refine tokens and component rules
4. patch implementation
5. run review checklist
