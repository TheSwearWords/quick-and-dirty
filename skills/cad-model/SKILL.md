---
name: cad-model
description: Build a dimensioned parametric model in Autodesk Fusion for print or production, with STEP/STL/3MF exports and a drawing. Use when the user wants a CAD part.
---

# CAD Model

Deliverable: the Fusion file, exports in exports/, and a dimensioned drawing.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks.

| Needs | Skill |
|---|---|
| prereqs/part-spec.md | `part-spec` |
| prereqs/model-reference.md | `model-reference` |

Never guess a production dimension. If one is missing, ask.

## Steps
1. Build parametrically, with the spec's key dimensions as named parameters. Send screenshots with key dimensions after each round and wait for notes.
2. Check against the spec: dimensions, tolerances, wall thickness for the process.
3. Once approved, export what the spec asks for (STEP for production, STL or 3MF for printing) and a simple dimensioned drawing.

Hand off: the files, plus notes on anything that differs from the spec.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
