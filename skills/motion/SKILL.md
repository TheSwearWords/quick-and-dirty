---
name: motion
description: Make motion in Figma, starting with logo animations (reveals, loops, transitions), following the brand's motion rules. Use when the user wants animation or motion.
---

# Motion

Deliverable: animations in Figma, with exported frames and timing notes.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks.

| Needs | Skill |
|---|---|
| prereqs/brand-spec.md | `brand-spec` |
| prereqs/logo/ | `logo` |

## Steps
1. Copy the logo; never alter the original.
2. Write a short storyboard (beats, timing, easing) and get the user's OK.
3. Build in Figma following the spec's motion rules (easing, duration, overshoot). Review each animation before showing it.

Hand off: Figma frame or prototype links, exported frames, and a note on timing and easing choices.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
