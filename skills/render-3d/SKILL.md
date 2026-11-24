---
name: render-3d
description: Model in Blender from sketches or references, then render stills or trailers or export glTF for the web. Use when the user wants 3D models, product renders or 3D animation.
---

# 3D Render

Deliverable: the model, and the stills, trailer or web files made from it.

## Prerequisites
Check `prereqs/` in the project. For each one that is missing, run its skill first; it builds its own prerequisites. Each is built once per project and shared, so never rebuild one that exists unless the user asks.

| Needs | Skill |
|---|---|
| prereqs/brand-spec.md | `brand-spec` |
| prereqs/model-reference.md | `model-reference` |

Blender must be running with its MCP add-on. If it isn't, stop and say so.

## Steps
1. Model in rounds: a blockout (proportions only), then detail. After each round, render front, side and three-quarter views and wait for the user's notes. Real-world scale, named parts, clean topology.
2. Do materials, lighting and the output the user asked for:
   - Stills: a few sample angles at preview quality first.
   - Trailer: write `prereqs/shot-list.md` first (per shot: length, camera, objects, materials, beats, effects). Blockout, then a pilot of the hardest shot, then each shot.
   - Web: glTF/GLB with baked materials and compressed textures; report the file size and triangle count.
3. Full-resolution or long renders only after the user approves sample frames and the render time. Prefer cheap approximations (particles over fluid sims).

Hand off: model files, render or export paths in exports/, short notes.

## Ground rules
- Ask the user before art-direction choices, anything outward-facing (publishing, sending, deploying) and deleting or overwriting files. One question, options, your recommendation.
- Never change the user's originals; copy them. Back up before bulk changes.
- The brand kit only grows. If it lacks something, propose an addition and log it in prereqs/kit-changelog.md; never make a one-off style or change existing kit pieces without approval.
- Figma: plan first, make few small calls, set light/dark mode explicitly on each wrapper frame, and stop and report if a call fails.
- After each finished step, update notes/<this skill>.md: done, next, open questions.
