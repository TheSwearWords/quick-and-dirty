---
name: brand-copy
description: Write slogans, taglines, headlines and product descriptions in the brand's voice, saved to prereqs/copy.md for reuse. Use when the user wants marketing copy.
---

# Brand Copy

Deliverable: the brand's words, saved where websites, decks and motion reuse them.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks.

| Needs | Skill |
|---|---|
| prereqs/product-brief.md | `product-brief` |
| prereqs/voice-guide.md | `voice-guide` |

## Steps
1. Draft each piece with options (taglines: at least 5). Mark a recommendation for each.
2. Check against the voice guide, then let the user pick.
3. Save the approved lines to `prereqs/copy.md`, with the unpicked options below them.

No filler ("unlock", "seamless", "elevate"). Be specific to this product.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
