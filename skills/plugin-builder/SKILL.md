---
name: plugin-builder
description: Build a new Orchestra plugin (manifest, about, playbooks, spec, README) by interview, or audit an existing plugin against the plugin requirements. Use when the user wants to make a new deliverable plugin, turn a skill or tool into a plugin, or check what a plugin is missing.
---

# Plugin Builder

Deliverable: a plugin folder that meets the Orchestra plugin contract (draft v0), plus a checklist report. Two modes:

- **Build:** interview the user, draft, check, write the folder.
- **Audit:** read an existing plugin or tool folder and report what it's missing against the checklist below. Change nothing unless the user asks.

The contract is still a draft. If the user has `plugin-spec.md` (Orchestra repo), read it first; it wins over anything here. Note every place where the plugin needed something the contract doesn't cover. Those notes shape contract v0.

## 1. Interview (build mode)

Ask one question at a time, with a suggestion for each answer. Skip anything the user already said.

1. **What it makes.** The deliverable(s), and for whom. One plugin can hold several deliverables if they share a canvas and a foundation (for example Interfaces: website, web app, mobile app).
2. **Where the work lives.** Its own files (`own`), or a tool it drives through an MCP (`mcp:figma`, `mcp:blender`, ...). Can it offer both?
3. **Kind.** `agent` (playbook only; the canvas tool is the editor) or `full` (its own UI and usually an engine). If full, why the canvas tool isn't enough.
4. **Inputs.** For each: what it is, its port type, whether it's **required** (blocks a run) or just improves the result, and how it can be sourced: *bring your own* (existing files, a URL, frames from any Figma file), *quick-make* (a short interview that writes a light version), or *supplied* by another plugin in Orchestra.
5. **Outputs.** What it hands on, and their port types.
6. **Works best with.** What makes the result better: this becomes `best_with`.
7. **How it works.** The order of work, through the five phases: ground (inputs), shape (structure the user edits), prove (one hard piece for direction), build (the rest, one unit at a time), hand off (exports).
8. **Where it stops for direction.** Gates: `approve`, `pick` (2-4 options + a recommendation), `direction` (options + notes), `notes`. Always gate art direction, anything outward-facing, anything destructive, and slow or paid work.
9. **Checks.** The craft rules each unit is checked against.
10. **Needs.** MCPs, providers and API keys, GPU, network hosts, whether it runs programs.

Then show a one-screen summary and get the user's OK before writing anything.

## 2. Write the folder

Ask where it goes (suggest `Desktop\Claude Projects\<id>`, its own git repo). Never overwrite an existing folder; if it exists, switch to audit mode.

```
<id>/
  orchestra.plugin.json
  playbooks/<deliverable>.yaml     one per deliverable
  playbooks/<deliverable>.md       the craft guidance the agent reads while working
  spec.md                          the plugin's spec
  README.md
  ui/  engine/                     full plugins only: leave a README stub saying what goes there
```

### orchestra.plugin.json

```json
{
  "contract": "0.1",
  "id": "<kebab-case, stable>",
  "name": "<Name>",
  "version": "0.1.0",
  "kind": "agent | full",
  "category": "Brand | Product | Web | Motion | 3D | Code | Audio",
  "description": "<one sentence>",
  "canvas": [
    { "target": "own" },
    { "target": "mcp:figma", "mcp": "figma", "thumbnail": "<tool that screenshots a unit>", "selection": "<tool that reads the current selection>" }
  ],
  "deliverables": [ { "id": "<deliverable>", "playbook": "playbooks/<deliverable>.yaml" } ],
  "inputs":  [ { "port": "<name>", "type": "<registry type or x-...>", "required": false, "many": false } ],
  "outputs": [ { "port": "<name>", "type": "<registry type or x-...>" } ],
  "ui":     { "entry": "ui/index.html" },
  "engine": { "command": ["..."], "protocol": "jsonrpc-stdio" },
  "actions": [ { "name": "<step id>", "description": "...", "params": {} } ],
  "requires":    { "providers": [], "gpu": "no | optional | yes", "mcps": [] },
  "permissions": { "fs": "slot", "network": [], "exec": false }
}
```

Leave out `ui` and `engine` for agent plugins. Actions default to one per playbook step.

Port types in the registry so far: `research/md`, `brief/md`, `brand/tokens`, `brand/logo`, `storyboard/json`, `video/mp4`, `audio/wav`, `audio/stems`, `audio/cuesheet+json`, `deck/pdf`, `figma/frames`, `model/glb`, `cad/step`. Anything else gets an `x-` prefix.

### playbooks/<deliverable>.yaml

```yaml
deliverable: <id>
about:
  does: <one line: what it makes>
  how: <one line: the order of work>
  best_with: <one line: what gives the best results>
needs:
  - { port: <name>, required: false, quick_make: <prereq>, bring: [url, figma, file] }
steps:
  - { id: <shape step>, makes: <file>, gate: approve }
  - { id: <prove step>, makes: "<units[0..2]>", gate: direction }
  - { id: <build step>, each: <unit>, checks: [<rule>, <rule>] }
  - { id: <hand-off step>, makes: [<exports>] }
guidance: <deliverable>.md
```

### playbooks/<deliverable>.md

The craft voice: how a senior practitioner would do this job. Reuse an existing quick-and-dirty skill or Orchestra Musician as the starting text when one fits.

### spec.md

The nine headings: Deliverables (with the `about` lines) · Kind and where the work lives · Canvas targets · Ports · Playbook per deliverable · Actions · UI (full only) · Engine (if any) · Build order and open questions.

## 3. Check (both modes)

Report each line as pass, missing or n/a. **Must** lines block; **should** lines are warnings.

**Package**
- [ ] must: manifest with contract, stable id, semver version, kind, category, description
- [ ] must: spec.md and README.md
- [ ] should: an icon

**What it does**
- [ ] must: a playbook (yaml + md) per deliverable
- [ ] must: `about` (does, how, best_with) per deliverable
- [ ] must: canvas declared (`own` and/or `mcp:<tool>`)

**Inputs and outputs**
- [ ] must: every port uses a registry type or an `x-` type
- [ ] must: every input says whether it's required; the playbook works without the optional ones and says what was missing
- [ ] should: each input offers bring-your-own and/or quick-make
- [ ] must: outputs go to `out/<port>/` and are listed in `outputs.json` (port, path, created, status draft | approved)

**Playbook**
- [ ] must: follows ground → shape → prove → build → hand off, or says why not
- [ ] must: gates before art direction, outward-facing, destructive, and slow or paid steps
- [ ] must: every step can run headless as an action, with no UI open
- [ ] must: state in `state/`, resumable after a restart, with a handoff note in `state/notes.md`

**Canvas (MCP targets)**
- [ ] must: names its MCP, a thumbnail tool and a selection tool
- [ ] must: mirrors canvas work into `out/<port>/` as references + thumbnails
- [ ] must: never edits the user's originals; works only in the file or page the user names

**Runtime (full plugins)**
- [ ] must: UI talks only through `window.orchestra` and runs on the standalone shim unchanged
- [ ] must: engine speaks JSON-RPC (`describe`, `run`, `status`, `cancel`; events `progress`, `needs_you`, `artifact_written`, `log`)
- [ ] should: uses `--orc-*` theme variables with its own fallbacks

**Safety**
- [ ] must: declares fs scope, every network host, providers, GPU, exec
- [ ] must: writes only inside its slot folder; no secrets in it
- [ ] must: treats downloaded and bring-your-own files as untrusted

**Tests**
- [ ] should: one fixture run: a sample slot folder in, expected artifacts out

End the report with **Contract gaps**: anything this plugin needed that the contract doesn't cover yet.

## Ground rules
- Ask before overwriting or deleting anything, and before creating a GitHub repo or pushing.
- Don't invent what the plugin does. Unknowns go in the spec's open questions.
- After each finished step, update notes/plugin-builder.md: done, next, open questions.
