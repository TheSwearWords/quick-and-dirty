# quick-and-dirty

Orchestra's deliverables as a Claude Code plugin. One skill per deliverable (the Musician), one skill per prerequisite. Run a deliverable and it checks `prereqs/` in your project, builds whatever is missing first, then does the work. Prerequisites are built once and shared, so a website and a deck reuse the same product brief and brand spec.

No Orchestrator, no app: you talk to the skill directly, and it asks you at the same points Orchestra would (art direction, sign-off, anything outward-facing).

## Install

```
/plugin marketplace add TheSwearWords/quick-and-dirty
/plugin install quick-and-dirty@quick-and-dirty
```

Then run, for example, `/quick-and-dirty:website` inside a project folder.

## Deliverables

| Skill | Makes | Needs |
|---|---|---|
| `logo` | logo directions → final files in `prereqs/logo/` | product-brief |
| `brand-kit` | Figma variables, styles, components, slide masters | brand-spec (signed off), logo |
| `brand-copy` | taglines, headlines → `prereqs/copy.md` | product-brief, voice-guide |
| `slide-deck` | deck in Figma + PDF | product-brief, brand-spec, voice-guide, deck-outline, brand kit |
| `website` | marketing site in Figma, desktop + mobile | product-brief, brand-spec, voice-guide, sitemap, brand kit |
| `app-ui` | app screens, light + dark | product-brief, brand-spec, screen-inventory, brand kit |
| `mobile-app` | iOS/Android flows | product-brief, brand-spec, screen-inventory, brand kit |
| `social-graphics` | social formats → `exports/social/` | brand-spec, voice-guide, brand kit |
| `motion` | logo animations in Figma | brand-spec, logo |
| `render-3d` | Blender model, renders, glTF | brand-spec, model-reference |
| `cad-model` | Fusion part, STEP/STL, drawing | part-spec, model-reference |
| `implementation` | working code from approved designs | brand-spec |

## Prerequisites

| Skill | Writes | Needs |
|---|---|---|
| `product-brief` | `prereqs/product-brief.md` | — |
| `voice-guide` | `prereqs/voice-guide.md` | product-brief |
| `brand-spec` | `prereqs/brand-spec.md`, `prereqs/tokens.json` | product-brief |
| `deck-outline` | `prereqs/deck-outline.md` | product-brief |
| `sitemap` | `prereqs/sitemap.md` | product-brief |
| `screen-inventory` | `prereqs/screen-inventory.md` | — |
| `part-spec` | `prereqs/part-spec.md` | — |
| `model-reference` | `prereqs/model-reference.md` | — |

## Project layout

Same as an Orchestra project, so work moves between the two:

```
concept.md, research.md or research/*.md   your inputs
prereqs/                                    shared prerequisites, kit-changelog.md, copy.md
exports/                                    renders and exported files
notes/<skill>.md                            handoff notes, so a fresh session can continue
```

## Adding a deliverable

Copy a folder in `skills/`, change the name, description, prerequisites table and steps. A new prerequisite is a skill that writes one file to `prereqs/` and lists its own needs.
