---
name: part-spec
description: Write prereqs/part-spec.md: a part's production spec (dimensions, material, tolerances, process, export formats). Use before CAD modeling.
---

# Part Spec (prerequisite)

Output: `prereqs/part-spec.md`. Needs: nothing.

Built once per project and shared. If the output already exists, show it and ask whether to reuse it (default) or redo it. Build any missing needs first by running their skills. Mark anything inferred as "(assumed)" and end with the questions the user needs to answer.

Inputs: the user's sketches, measurements and notes, and how they plan to make it (3D print, CNC, injection molding and so on). Cover every dimension with units, material, process, tolerances, wall thickness or other process limits, and the export formats needed. Never invent a dimension; list missing ones as questions.
