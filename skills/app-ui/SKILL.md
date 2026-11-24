---
name: app-ui
description: Design desktop or web app screens in Figma, light and dark, from the brand kit and a screen inventory. Use when the user wants app, SaaS or dashboard screens.
---

# App UI

Deliverable: app screens in Figma, light and dark, built only from the kit.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks. The brand kit must exist too; if it doesn't, run `brand-kit` first.

| Needs | Skill |
|---|---|
| prereqs/product-brief.md | `product-brief` |
| prereqs/brand-spec.md | `brand-spec` |
| prereqs/screen-inventory.md | `screen-inventory` |

## Steps
1. Turn each item in the inventory's gap list into a kit addition request (what, which screens, a suggestion).
2. Build one screen at a time, light and dark, from kit components. Review each before the next.
3. Hidden children inside component instances can't be found by traversal; use the component's boolean properties.

Hand off: Figma frame links with screenshots, plus the kit additions requested.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
