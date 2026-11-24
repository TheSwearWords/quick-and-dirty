---
name: logo
description: Make the logo, from 3 to 5 written directions to final vector files in prereqs/logo/. Also a prerequisite for brand-kit and motion. Use when the user wants a logo, mark or wordmark.
---

# Logo

Deliverable: the logo, from directions to final files in every format the brand needs.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks.

| Needs | Skill |
|---|---|
| prereqs/product-brief.md | `product-brief` |

If `prereqs/logo/` already has final files, show them and ask whether to reuse them.

## Steps
1. Read the brief, concept.md and research. Write 3 to 5 genuinely different directions to `prereqs/logo-concepts.md` (name, idea, rough sketch in Figma, type pairing, risk). The user picks one or two.
2. Draw the chosen direction in Figma. Get notes, refine, repeat until the user approves.
3. Export to `prereqs/logo/`: SVG and PNG; color, one-color and reversed; mark and wordmark.

Hand off: the Figma frame link, the files, and a short note on the idea behind the mark.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
