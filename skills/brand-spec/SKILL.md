---
name: brand-spec
description: Write prereqs/brand-spec.md and prereqs/tokens.json: the written brand system (color, type, spacing, components, motion). Use when a visual deliverable needs the brand spec or the user asks for one.
---

# Brand Spec (prerequisite)

Output: `prereqs/brand-spec.md` and `prereqs/tokens.json`. Needs: `prereqs/product-brief.md` (skill `product-brief`).

Built once per project and shared. If the output already exists, show it and ask whether to reuse it (default) or redo it. Build any missing needs first by running their skills. Mark anything inferred as "(assumed)" and end with the questions the user needs to answer.

Read the product brief, concept.md, research, references, and any existing logos, fonts and colors. Ask for the light/dark preference if it isn't stated.

Cover: colors (primitives, semantic tokens, light and dark modes), logo rules, type scale, spacing, radius, elevation, buttons and boxes with every state, backgrounds, icons, inputs and tags, grid, slide masters and motion rules (easing, duration, overshoot). Write the token values to tokens.json too.

Nothing gets built from the spec until the user signs it off. Ask for sign-off at the end.
