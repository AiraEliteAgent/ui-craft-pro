# Changelog

All notable changes to `ui-craft-pro` are documented here.

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
