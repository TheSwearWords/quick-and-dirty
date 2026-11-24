---
name: mobile-app
description: Design iOS and Android app screens and flows in Figma from the brand kit and a screen inventory. Use when the user wants mobile app screens.
---

# Mobile App

Deliverable: mobile screens in Figma, flow by flow.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks. The brand kit must exist too; if it doesn't, run `brand-kit` first.

| Needs | Skill |
|---|---|
| prereqs/product-brief.md | `product-brief` |
| prereqs/brand-spec.md | `brand-spec` |
| prereqs/screen-inventory.md | `screen-inventory` |

## Steps
1. Turn the inventory's gaps into kit addition requests (mobile often needs tab bars, sheets and larger touch targets).
2. Build the main flow end to end, then the rest. Review each flow before the next.
3. Platform rules: safe areas, 44pt iOS / 48dp Android touch targets, native navigation, readable type at phone size.

Hand off: Figma frame links per flow, a prototype link if built, and the kit additions requested.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
