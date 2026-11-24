---
name: slide-deck
description: Build a presentation in Figma on the brand kit's slide masters (pitch, product or client deck), with a PDF export. Use when the user wants slides or a deck.
---

# Slide Deck

Deliverable: a deck in Figma on the kit's slide masters.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks. The brand kit must exist too; if it doesn't, run `brand-kit` first.

| Needs | Skill |
|---|---|
| prereqs/product-brief.md | `product-brief` |
| prereqs/brand-spec.md | `brand-spec` |
| prereqs/voice-guide.md | `voice-guide` |
| prereqs/deck-outline.md | `deck-outline` |

## Steps
1. Write each slide's text from the outline, reusing `prereqs/copy.md`: one idea per slide, short headlines.
2. Build the first three slides on the masters and get the user's direction. Then the rest.
3. Missing layouts become kit addition requests.

Hand off: the Figma link, a PDF export, and speaker notes if the outline asked for them.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
