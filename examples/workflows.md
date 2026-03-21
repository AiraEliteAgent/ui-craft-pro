# Example Workflows

These examples are written for **OpenClaw** usage.

## 1) Build a gaming landing page

Goal:
- high energy
- stronger typography
- clear CTA rhythm
- less generic AI landing-page feel

Suggested flow:
1. generate a design system
2. lock colors, type, spacing, and section structure
3. implement hero, feature blocks, and CTA
4. review for visual coherence and readability

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

## 4) Use style cloning safely

Case:
- the user wants a stronger product vibe
- but does not want a shallow visual copy

Example asks:
- make this docs page feel more GitHub-like
- make this launch page more Vercel-like
- make this AI answer UI more Perplexity-like

Suggested flow:
1. extract a style signature
2. identify the shell/pattern that fits the product
3. lock tokens, hierarchy, and surface rules
4. implement with your own brand details
5. run anti-generic review

Example commands:

```bash
python3 skills/ui-craft-pro/scripts/style_signature.py "developer docs premium monochrome"
python3 skills/ui-craft-pro/scripts/search.py "github-like developer docs" --domain style-signatures
python3 skills/ui-craft-pro/scripts/search.py "developer docs shell sidebar toc" --domain patterns-shells
```

## 5) Build an AI answer/search shell

Goal:
- calm, content-first UI
- low chrome
- strong readability
- visible sources and follow-up actions

Suggested flow:
1. search for a suitable shell pattern
2. extract the style signature
3. lock prompt, answer, and source-chip treatment
4. implement and reduce decorative noise

Example commands:

```bash
python3 skills/ui-craft-pro/scripts/search.py "ai answer prompt sources" --domain patterns-shells
python3 skills/ui-craft-pro/scripts/style_signature.py "ai search knowledge calm minimal"
python3 skills/ui-craft-pro/scripts/search.py "generic ai ui too loud content first" --domain anti-generic-ui
```

## 6) Improve an existing page

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
5. run review checklist and anti-generic pass
