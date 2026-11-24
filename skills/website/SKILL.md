---
name: website
description: Design a marketing site in Figma (product, SaaS or app launch), desktop and mobile, from the brand kit and real copy. Use when the user wants a website or landing page designed.
---

# Website

Deliverable: every page in Figma at desktop and mobile, ready for implementation.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks. The brand kit must exist too; if it doesn't, run `brand-kit` first.

| Needs | Skill |
|---|---|
| prereqs/product-brief.md | `product-brief` |
| prereqs/brand-spec.md | `brand-spec` |
| prereqs/voice-guide.md | `voice-guide` |
| prereqs/sitemap.md | `sitemap` |

## Steps
1. Write each page's copy from the sitemap, reusing `prereqs/copy.md`. Real copy before layout, never lorem ipsum.
2. Design the home page, desktop then mobile. Get the user's direction before the other pages.
3. Design the remaining pages one at a time, reviewing each.
4. Anything the kit lacks becomes a kit addition request.

Hand off: Figma frame links per page at both widths, screenshots, and the kit additions requested.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
