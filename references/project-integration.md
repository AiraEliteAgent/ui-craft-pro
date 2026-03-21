# Project Integration

Use this file when applying `ui-craft-pro` inside a real OpenClaw project.

## Goal

The point is not to generate design ideas in isolation.
The point is to make those ideas survive contact with a real codebase.

## In a real project

Use this skill when a page or interface needs one or more of these:
- stronger design direction
- better hierarchy
- more coherent tokens and component treatment
- a calmer or more premium tone
- correction after an emotionally wrong first pass

## Recommended integration flow

1. Identify the product and the specific UI problem.
2. Generate or infer the design direction.
3. Correct the direction if the first pass is wrong.
4. Lock implementation choices:
   - colors
   - typography
   - spacing
   - radius/shadow
   - section structure
   - component treatment
5. Apply the changes in the real project.
6. Run a review pass before calling it done.

## For Astro projects

- Keep design tokens centralized.
- Prefer reusable sections/components over repeated one-off page patterns.
- Preserve consistency between homepage, feature sections, article views, and supporting pages.

## For React/Tailwind projects

- Convert the chosen direction into reusable tokens/utilities.
- Avoid component-by-component drift.
- If the project already has a UI library, align it with the chosen direction instead of mixing default library styling with custom sections.

## For existing products

When refining an existing site:
- do not rewrite everything if the product already has useful structure
- identify what is weak first:
  - hierarchy
  - typography
  - CTA rhythm
  - section flow
  - visual coherence
- then patch the system, not just isolated pixels

## Final rule

In project use, the skill should lead to better implementation decisions.
If it only produces nice-looking notes and the shipped UI still feels generic, the workflow was not followed deeply enough.
