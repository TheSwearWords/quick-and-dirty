---
name: brand-kit
description: Build the brand kit in Figma (variables, styles, components, slide masters) from the signed-off brand spec, and add to it later. Build it before decks, UI, websites, social and motion.
---

# Brand Kit

Deliverable: the brand's visual source of truth in Figma. Every visual deliverable builds from it.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks.

| Needs | Skill |
|---|---|
| prereqs/brand-spec.md (signed off) | `brand-spec` |
| prereqs/logo/ | `logo` |

## First build
1. Don't build before the user has signed off the brand spec.
2. Build the spec in the Figma file the user names, one section at a time. Review each section before the next.
3. Final check: every color, type and spacing value bound to a variable or style, no placeholder text, components named consistently.

## Additions
Other deliverables will ask for things the kit lacks. Look for something close first and propose using or extending it. Otherwise build the addition from existing tokens and styles in the matching section, get approval, and log it in `prereqs/kit-changelog.md` (date, what, which deliverable asked).

Hand off: the Figma file link and a short summary of what's in it or what was added.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
