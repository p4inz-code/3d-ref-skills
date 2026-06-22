# Contributing to 3d-ref-skills

First — thank you. This pack exists to help 3D artists work better with AI,
and the best people to extend it are 3D artists who know what they're missing.

You don't need to know how to code. If you know 3D production, you can write a skill.

---

## What makes a good skill for this pack

A good `3d-ref-skills` skill does one thing the artist would otherwise do slowly,
inconsistently, or forget entirely — in the pre-production and reference phase
of 3D work. Not modeling advice. Not rendering advice. Reference and preparation.

Good candidates:
- Reference workflows for a specific asset category (characters, vehicles, archviz)
- Reference workflows for a specific DCC that has unique needs
- Reference workflows for a specific output (game engine, film, print)
- Research and brief generation for niche communities (concept artists, texture artists)

Not a good fit:
- Modeling tutorials or technique advice
- Rendering or compositing guidance
- General productivity skills unrelated to 3D reference work

---

## Skill format

Every skill in this pack follows the same format. Copy the template below
and fill it in.

```markdown
---
name: ref-[yourskillname]
description: >
  One to four sentences. What does this skill do? When should the agent
  activate it? What trigger phrases? What asset types or DCCs does it
  support?
version: 1.0.0
author: Your Name (github.com/yourusername)
license: MIT
---

# [Skill Title]

[Opening paragraph — who you are in the context of this skill. What expertise
are you drawing on? What problem does this solve and why does it matter?]

## [Main Framework Section]

[The structured framework the AI uses. Be specific. Be opinionated. Tell the
AI exactly what to ask, what to check, what to output, and what common mistakes
to flag.]

## Output

[What file does this skill produce? What should it be named? Where should it
be saved?]
```

---

## Submitting a skill

1. Fork this repository
2. Create a new folder: `skills/ref-[yourskillname]/`
3. Add your `SKILL.md` following the format above
4. Add at least one real example output in `skills/ref-[yourskillname]/examples/`
   — a filled, realistic output for a real asset type. This is the most important
   part. Skills without examples don't get used.
5. Open a pull request with:
   - A one-sentence description of what the skill does
   - What gap it fills that existing skills don't cover
   - A link to your example output

---

## Example ideas we'd love to see

> `ref-character` and `ref-hardsurface` were community-requested and shipped in v3.0.0.
> See them in `skills/ref-character/` and `skills/ref-hardsurface/` as examples of what a completed skill looks like.

| Skill idea | What it would cover |
|------------|-------------------|
| `ref-archviz` | Architecture and interior visualization: building material reference, human scale anchors, lighting reference for interior/exterior, client presentation reference for non-artist approval |

| `ref-concept` | Concept-to-3D pipeline: translating a 2D concept into a buildable reference brief |
| `ref-vehicle` | Vehicle-specific: orthographic blueprint sourcing, mechanical reference, LOD strategy for large assets |
| `ref-creature` | Creature and monster design: anatomy departure rules, surface variation, deformation priority zones |
| `ref-environment-kit` | Environment kit design: modular grid planning, hero vs filler asset ratio, tiling reference strategy |
| `ref-vfx-sim` | VFX simulation reference: real-world footage sources per effect type, motion breakdown, phase documentation |

---

## Code of conduct

Be direct, be specific, and be useful. This pack exists to give 3D artists
real production guidance — not vague encouragement. If you're reviewing a PR,
focus on whether the skill produces output an artist would actually use.

Questions? Open an issue or reach out at [github.com/p4inz-code](https://github.com/p4inz-code).
