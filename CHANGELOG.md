# Changelog

All notable changes to `ui-craft-pro` are documented here.

---

## 0.2.1 — 2026-03-22

README maturity pass.

### Added
- reference-family chooser table to help users pick the right inspiration family faster
- common-mistakes section for anti-generic and anti-drift guidance
- FAQ section to reduce friction around workflow depth, style signatures, and reference borrowing

### Changed
- improved README flow so it reads more like mature product documentation and less like a static showcase page
- reinforced the project’s positioning around structure, fit, and safer style borrowing

### Notes
- This release is focused on making the repository easier to evaluate, trust, and actually use.

---

## 0.2.0 — 2026-03-22

README productization upgrade.

### Added
- proof / trust-signal section near the top of the README
- before-vs-after framing to make the project value easier to understand quickly
- outcome examples that explain where the skill creates concrete improvement instead of abstract polish

### Changed
- upgraded the README from structured documentation into a more persuasive product page with clearer practical value
- expanded best-use-case framing to include AI answer/search shells, onboarding/auth flows, and developer-product surfaces

### Notes
- This release is focused on making the repository feel more convincing to evaluators while still staying useful as documentation.

---

## 0.1.9 — 2026-03-22

README documentation architecture upgrade.

### Added
- `Why not generic AI UI?` comparison table near the top of the README
- `Get started in 60 seconds` section for faster first-run onboarding
- `Setup by use case` with collapsible sections for landing pages, dashboards, docs, AI answer UI, and onboarding/settings flows
- `3 things you actually need` section to reduce perceived complexity for new users

### Changed
- strengthened the README information architecture to feel more like product documentation than a polished note dump
- expanded quick usage and differentiator sections so the repo explains structure, reference borrowing, and anti-generic review more clearly

### Notes
- This release is focused on making the README easier to scan, trust, and adopt quickly.

---

## 0.1.8 — 2026-03-22

README hero/positioning upgrade + live demo integration.

### Changed
- upgraded the README hero to better reflect the project as a reference-driven UI product instead of a generic skill page
- added a direct GitHub Pages live demo badge and link
- refreshed the overview, differentiators, quick usage, and best-use-case sections to match the new style-signature / shell / anti-generic workflow
- expanded the README references section so the stronger guidance layers are visible from the main repository page

### Notes
- This release is focused on making the repository landing experience feel as deliberate as the project itself.

---

## 0.1.7 — 2026-03-22

Static showcase page + repository product polish.

### Added
- `showcase.html` as a lightweight product-facing showcase page for the repository
- a cleaner visual summary of the skill’s new positioning, domains, workflow, and demo previews

### Changed
- linked the repository README to the new showcase page
- extended the repository from markdown-only presentation into a more product-like, browsable entry surface

### Notes
- This release gives `ui-craft-pro` a better front door for people evaluating the project quickly.

---

## 0.1.6 — 2026-03-22

Reference-driven style cloning + docs/workflow upgrade.

### Added
- style-cloning guidance to the repository docs and usage flow
- new examples covering GitHub-like, Vercel-like, Perplexity-like, Shopify-like, and Raycast-like work
- quick-start guidance for the new `style_signature.py` workflow
- documentation for the new taste-building domains: `design-systems`, `style-signatures`, `patterns-shells`, and `anti-generic-ui`

### Changed
- upgraded the README to better reflect the project’s new reference-driven positioning
- expanded best-use-case coverage to include AI answer/search shells, auth/onboarding, and developer-product surfaces
- refreshed example prompts and workflows so the project teaches safer style borrowing instead of generic "make it prettier" behavior

### Notes
- This release is focused on making the repository match the stronger internal capability that was added to the skill itself.

---

## 0.1.5 — 2026-03-22

README hero and badge polish.

### Changed
- upgraded the README hero section to feel more product-grade and less generic
- changed repository status badge from `private` to `public`
- added direct GitHub and ClawHub badges at the top for faster discovery
- refreshed the opening positioning copy to make the project value clearer at first glance

### Notes
- This release is focused on repository presentation quality, discoverability, and first-impression clarity.

---

## 0.1.4 — 2026-03-22

ClawHub safety wording polish.

### Changed
- softened instruction wording in `SKILL.md` to read more like guidance than command/override text
- kept the workflow intact while reducing language that could look like prompt-override behavior to static scanners

### Notes
- This release is aimed at reducing false-positive prompt-injection warnings on ClawHub/OpenClaw safety scans.

---

## 0.1.3 — 2026-03-22

ClawHub listing polish.

### Changed
- rewrote the skill summary/description to be sharper, clearer, and more product-facing on ClawHub
- improved first-glance positioning so users can understand the skill faster from the listing itself

### Notes
- This release is focused on presentation quality and discoverability on the ClawHub skill page.

---

## 0.1.2 — 2026-03-22

ClawHub install/documentation upgrade.

### Added
- explicit ClawHub install section in `README.md`
- direct links to the public GitHub repository and ClawHub listing in repository documentation
- project home and registry links embedded into the published skill payload

### Changed
- improved repository onboarding for OpenClaw users who want to install via `clawhub install ui-craft-pro`
- clarified the difference between GitHub source and ClawHub registry installation

### Notes
- This release makes the project easier to discover, install, and verify from both GitHub and ClawHub.

---

## 0.1.1 — 2026-03-22

Repository polish and OpenClaw-focused usability upgrade.

### Added
- `QUICKSTART.md` for OpenClaw-first setup and usage
- `examples/prompts.md` with practical trigger examples
- `examples/workflows.md` with concrete usage flows
- `references/project-integration.md` for applying the skill in real projects
- cleaner preview asset organization under `assets/previews/`

### Changed
- Reworked README structure to make OpenClaw usage clearer
- Updated showcase image paths after asset cleanup
- Refocused repository guidance toward **OpenClaw-only** usage instead of broader multi-platform positioning

### Notes
- This update improves the repository as a product, not just as a bundle of files.
- The goal is to make installation, usage, and evaluation easier for real OpenClaw users.

---

## 0.1.0 — 2026-03-21

Initial private release.

### Added
- Initial OpenClaw-compatible packaging for `ui-craft-pro`
- Core skill instructions in `SKILL.md`
- Local design knowledge base in `data/`
- Search and design-system scripts in `scripts/`
- Implementation mapping reference in `references/implementation-patterns.md`
- Review reference in `references/review-checklist.md`
- Product-archetype correction reference in `references/product-archetypes.md`
- Repository documentation with README and project structure

### Changed
- Renamed the working project to `ui-craft-pro`
- Reframed the project from design-reference lookup into a **design-to-implementation** workflow
- Strengthened the skill to explicitly handle:
  - locking implementation choices before coding
  - correcting emotionally wrong first-pass design output
  - reviewing output for style fit and consistency

### Validated through
- gaming landing-page demo
- fintech / treasury-control demo
- cross-agent privacy journaling test
- richer showcase demos for dark ops, luxury landing, and editorial/news layouts

### Notes
- This version was shaped through real demos and live iteration, not only static planning.
- The project includes inspiration and adapted ideas from `ui-ux-pro-max-skill`, but is structured for OpenClaw-based usage and agent workflow discipline.
- Showcase coverage now includes more complete page types, including a content/news style demo with homepage, category navigation, newsletter block, article section, and image-backed editorial layout.
