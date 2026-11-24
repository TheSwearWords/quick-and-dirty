---
name: social-graphics
description: Make brand graphics for social media in Figma (posts, stories, headers, banners), exported at each platform's size. Use when the user wants social media graphics.
---

# Social Graphics

Deliverable: one Figma frame per format on a "Social Graphics" page, exported to `exports/social/`.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks. The brand kit must exist too; if it doesn't, run `brand-kit` first.

| Needs | Skill |
|---|---|
| prereqs/brand-spec.md | `brand-spec` |
| prereqs/voice-guide.md | `voice-guide` |

## Steps
1. Agree the format list with the user: platforms and sizes (1:1, 4:5, 9:16, 3:1 and 4:1 headers, 16:9 with a safe centre), and whether each is a plain background or a finished graphic with mark and copy.
2. Write any on-graphic text from the voice guide: short, one line where possible.
3. Build the first format and get the user's direction. Then the rest, re-composing each ratio rather than cropping.
4. Check every frame against the kit and the platform's safe areas.

Nothing gets posted. Publishing is the user's call.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
