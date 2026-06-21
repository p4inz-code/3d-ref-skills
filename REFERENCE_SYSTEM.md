# Reference System — How the Skills Connect

The skills in this repository are not independent tools. They are phases of a single workflow.
This document explains what each skill produces, what it consumes, and how they chain together.

---

## The Workflow

```
┌─────────────────────────────────────────────────────────────────────┐
│                     REFERENCE ENGINEERING WORKFLOW                  │
├──────────────┬──────────────────────────────────────────────────────┤
│   TRIGGER    │  "I'm starting a new 3D asset"                       │
└──────────────┴──────────────────────────────────────────────────────┘
        │
        ▼
┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 1 — BRIEF                                                    │
│                                                                     │
│  ref-brief       → Any 3D asset (prop, character, environment)      │
│  ref-vfx         → VFX element (fire, smoke, explosion, particles)  │
│  ref-texture     → Texture / material (tiling, trim, Fab pack)      │
│                                                                     │
│  INPUT:   Asset description (type, platform, style)                 │
│  OUTPUT:  Structured reference brief document                       │
│           — silhouette queries, orthographic sources,               │
│             material breakdown, scale anchor, detail zones          │
└─────────────────────────────────────────────────────────────────────┘
        │
        ▼
┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 2 — GATHER (manual — in PureRef or Kanvaz)                  │
│                                                                     │
│  Use the brief to collect references in order:                      │
│    1. Silhouette and shape (form before surface)                    │
│    2. Orthographic views (blueprints, technical drawings)           │
│    3. Material clusters (one per surface type)                      │
│    4. Detail zone close-ups (macro photography)                     │
│    5. Lighting and render reference                                  │
│                                                                     │
│  INPUT:   Reference brief from Phase 1                              │
│  OUTPUT:  Organized reference board with labeled zones              │
│           — target 50–90 images for a hero asset                    │
└─────────────────────────────────────────────────────────────────────┘
        │
        ▼
┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 3 — DECODE (optional but recommended for style-matched work) │
│                                                                     │
│  ref-style-decode → Any reference you want to match or understand   │
│                                                                     │
│  INPUT:   Reference image, ArtStation piece, or style description   │
│  OUTPUT:  8-dimension style decode document                         │
│           — shape language, surface quality, detail density,        │
│             color architecture, lighting assumption, topology hints  │
│           — "Apply This" actions for your specific asset            │
└─────────────────────────────────────────────────────────────────────┘
        │
        ▼
┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 4 — AUDIT (before modeling begins and again at blockout)     │
│                                                                     │
│  ref-audit → Any asset type at any stage                            │
│                                                                     │
│  INPUT:   Description of current reference board                    │
│  OUTPUT:  PASS/PARTIAL/FAIL audit report                            │
│           — critical gaps (fix before modeling)                     │
│           — important gaps (fix before texturing)                   │
│           — low priority gaps (can address during texturing)        │
│           — immediate action: the one thing to do right now         │
└─────────────────────────────────────────────────────────────────────┘
        │
        ▼
┌─────────────────────────────────────────────────────────────────────┐
│  PHASE 5 — MODEL (in DCC)                                           │
│                                                                     │
│  Open Maya, Blender, ZBrush, or your DCC of choice.                │
│  Every modeling decision references a specific image.               │
│  Re-run ref-audit at blockout completion and again pre-UV.          │
└─────────────────────────────────────────────────────────────────────┘
        │
        ├──────────────────────────┐
        ▼                          ▼
┌──────────────────────┐  ┌────────────────────────────────────────┐
│  DELIVERY —          │  │  DELIVERY —                            │
│  MARKETPLACE         │  │  FREELANCE CLIENT                      │
│                      │  │                                        │
│  ref-marketplace     │  │  ref-client                            │
│                      │  │                                        │
│  INPUT:  Asset +     │  │  INPUT:  Commission details +          │
│          category    │  │          client references             │
│  OUTPUT: Dual brief  │  │  OUTPUT: Scope document,               │
│          modeling +  │  │          visual direction Q&A,         │
│          marketing   │  │          milestone gates,              │
│          reference   │  │          revision risk register        │
└──────────────────────┘  └────────────────────────────────────────┘
```

---

## What Each Skill Produces and Consumes

| Skill | Consumes | Produces | Next skill uses it |
|-------|----------|----------|-------------------|
| `ref-brief` | Asset description | Reference brief document | `ref-audit` validates it |
| `ref-vfx` | Effect description | VFX reference brief | `ref-audit` validates motion ref |
| `ref-texture` | Material description | Texture reference brief | Used directly in texturing |
| `ref-style-decode` | Reference image or description | Style decode + Apply This actions | Feeds back into `ref-brief` |
| `ref-audit` | Reference board description | Audit report with gaps | Feeds back into gather phase |
| `ref-marketplace` | Asset + marketplace target | Modeling + marketing brief | Terminal — used at delivery |
| `ref-client` | Commission + client references | Scope alignment document | Terminal — used at delivery |

---

## When to Re-Run Skills

Skills are not single-use. Run them at multiple stages of production:

**ref-brief:**
- Run once at project start
- Update to v2 at blockout completion (you will have found gaps)

**ref-style-decode:**
- Run whenever you find a new reference that changes your direction
- Run when a client provides a new direction mid-project

**ref-audit:**
- Run before opening the DCC (pre-production audit)
- Run at blockout completion (mid-production audit)
- Run before UV unwrapping (pre-texture audit)
- Run when something feels wrong but you can't identify what

**ref-vfx:**
- Run once per VFX effect before simulation begins
- Update after first sim iteration

**ref-texture:**
- Run once per material before texturing begins
- Update after first texturing pass

**ref-marketplace:**
- Run once before final renders and product listing

**ref-client:**
- Run at project start, before any production work
- Version-update whenever scope changes

---

## The Compounding Effect

Each skill makes the next skill more effective:

A thorough `ref-brief` means `ref-audit` finds fewer gaps.
A thorough `ref-audit` means modeling proceeds with fewer interruptions.
A thorough `ref-style-decode` means `ref-brief` produces more targeted queries.
A thorough `ref-marketplace` means the asset's marketing references align with its modeling references.

Artists who use the skills in sequence consistently report fewer mid-production revisions,
fewer delivery failures, and more confidence during modeling — because every decision
has a reference that supports it.

---

## Quick Reference — Which Skill Do I Need Right Now?

| Situation | Skill |
|-----------|-------|
| Starting a new 3D asset | `ref-brief` |
| Starting a VFX effect | `ref-vfx` |
| Starting texture work | `ref-texture` |
| I want to match a specific style | `ref-style-decode` |
| Something feels wrong with my model | `ref-audit` |
| My reference board feels shallow | `ref-audit` |
| I'm selling this on Fab / Sketchfab | `ref-marketplace` |
| I have a freelance commission | `ref-client` |
| I don't know where to start | `ref-brief` — always start here |
