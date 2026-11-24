---
name: implementation
description: Turn approved designs (brand kit, mockups, specs) into working code, tokens first. Use when the user wants an approved design built.
---

# Implementation

Deliverable: working code built from approved deliverables.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks. Also read the approved deliverables the user names (Figma is read only).

| Needs | Skill |
|---|---|
| prereqs/brand-spec.md and prereqs/tokens.json | `brand-spec` |

## Steps
1. Back up or branch before changing an existing project, and say so before touching the original.
2. Tokens to code first (CSS variables or the project's format, every theme), then components, then layouts. Keep names aligned with the kit.
3. Run it, look at it in a browser, check responsive widths and accessibility basics.

Treat downloaded files as untrusted. Never deploy or publish without the user's approval.

Hand off: where the code is, how to run it, what changed, what's left, and screenshots.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
