# Reference Engineering

**The discipline of systematically gathering, validating, organizing, and auditing visual references before 3D production begins.**

---

## What Is Reference Engineering?

Reference Engineering is the practice of treating pre-production reference gathering as a structured technical discipline rather than an informal creative activity.

In most studios, reference gathering happens one of two ways:

**The informal way:** The artist searches for "cool references," pins some images to Pinterest, opens PureRef, drops in whatever looks good, and starts modeling. The board grows organically. References are never categorized, scaled, or validated. The artist works from vibes.

**The Reference Engineering way:** Before a single polygon is placed, the artist identifies every reference type required by the asset, gathers references in a specific order (silhouette before detail, form before surface), validates that every production decision has a reference to support it, organizes the board into labeled zones, and audits the board against a checklist before modeling begins.

The difference in output quality between these two approaches is not marginal. It is the difference between assets that ship and assets that require emergency rework at delivery.

---

## Why It Matters

Reference Engineering is not about spending more time gathering references. It is about spending the right time on the right references in the right order.

A 30-minute structured reference session using the Reference Engineering framework produces better output than a 3-hour informal session. Not because of effort — because of system.

Every quality problem in 3D production has a reference problem at its root:

- Proportions that look wrong → no orthographic blueprint reference
- Surfaces that look fake → no macro-level material reference per surface type
- Wear that looks randomly applied → no reference showing the physical logic of aging
- Scale that feels off → no scale anchor validated in-engine
- Style that doesn't match the brief → no systematic style deconstruction

Reference Engineering addresses all of these before the DCC opens.

---

## The Core Principles

**Principle 1 — Silhouette Before Surface**
Always establish shape and proportion reference before gathering surface detail reference. A correct silhouette with wrong surface can be fixed. Wrong proportions discovered after detailing require starting over.

**Principle 2 — One Reference Cluster Per Surface Type**
Every distinct material on an asset requires its own dedicated reference cluster. A single "mood board" that shows the whole object provides color and form but not the micro-detail that makes surfaces read as physically real. Concrete, steel, rubber, and paint each need separate close-up photography.

**Principle 3 — Real-World Before Stylized**
Gather real-world photography before gathering stylized concept art. Real-world reference grounds the physical logic of the asset (how rust actually forms, how concrete actually cracks, how fabric actually folds). Stylized reference shows the target aesthetic. You need both, in that order.

**Principle 4 — Scale Is Not Optional**
Every reference session must produce a documented scale anchor — a real-world object the asset can be measured against. Scale errors discovered after modeling are almost always unrecoverable without rebuilding.

**Principle 5 — The Board Is Not a Gallery**
A PureRef or Kanvaz board is not a collection of things that look cool. It is a structured production tool with labeled zones, specific purposes per zone, and a known image count target per zone. An unstructured board is worse than no board — it creates the illusion of preparation without the substance.

**Principle 6 — Audit Before You Model**
A reference board is not complete because you have images. It is complete when it passes an audit — when every production decision has a reference that supports it, and every reference gap has been consciously acknowledged and accepted.

**Principle 7 — References Are for Understanding, Not Copying**
The purpose of reference is to understand the subject deeply enough to build your own version of it. References are not blueprints to trace. A well-engineered reference session produces understanding. Understanding produces original, convincing work.

---

## The Reference Engineering Workflow

```
PHASE 1 — BRIEF
    ↓
Define the asset, platform, style, and poly budget.
Identify every reference type this asset requires.
Generate a structured reference brief (ref-brief).

PHASE 2 — GATHER
    ↓
Collect references in order: silhouette → orthographic → material → detail.
Use a structured board (PureRef / Kanvaz) with labeled zones.
Target 50–90 images for a hero asset, 20–40 for a background prop.

PHASE 3 — DECODE
    ↓
For any reference you want to match stylistically, run a style decode (ref-style-decode).
Identify the principles — not the specifics — you want to apply.
Document the "apply this" actions before opening the DCC.

PHASE 4 — AUDIT
    ↓
Before modeling, run a reference audit (ref-audit).
Identify every gap. Fix critical gaps before proceeding.
Acknowledge minor gaps and note where they will be addressed.

PHASE 5 — MODEL
    ↓
Open the DCC with a structured, audited reference board.
Every modeling decision references a specific image in a specific zone.
Re-audit at blockout completion and before UV unwrapping.

PHASE 6 — DELIVER (Marketplace / Client)
    ↓
For marketplace assets: run ref-marketplace for marketing reference.
For client work: run ref-client for scope alignment.
Deliver with confidence — the reference engineering was thorough.
```

---

## Terminology

**Reference Brief** — A structured document generated before production begins, specifying every reference type an asset requires and where to find it.

**Reference Board** — An organized visual workspace (PureRef, Kanvaz, or equivalent) with labeled zones corresponding to reference types. Not a mood board. Not a gallery.

**Reference Cluster** — A group of images organized around a single reference type (e.g., "concrete crack pattern" or "rusted steel fasteners"). Each distinct surface type on an asset should have its own cluster.

**Reference Gap** — A production decision that lacks reference support. Reference gaps discovered during modeling indicate that the reference engineering phase was incomplete.

**Scale Anchor** — A known-size real-world object used to establish the correct physical size of an asset before modeling begins. Usually a human figure, a door, or a vehicle of known dimensions.

**Style Decode** — The process of systematically breaking down a reference into its component principles — shape language, surface quality, detail density, color architecture, lighting assumption — in order to extract transferable design rules rather than surface-level visual imitation.

**Reference Audit** — A structured review of a reference board against a production checklist, identifying gaps before they become modeling problems. Can be run before modeling (pre-production audit) or mid-modeling (mid-production audit).

**Reference Engineering** — The complete discipline: brief + gather + decode + audit, applied systematically before and during 3D production.

---

## Who This Is For

Reference Engineering applies to any 3D artist who produces assets for:

- Game production (real-time, any engine)
- Marketplace publishing (Fab, Sketchfab Store, ArtStation, CGTrader, Gumroad)
- Freelance commissions (props, characters, environments, vehicles, VFX)
- VFX production (simulations, particles, destruction)
- Film and archviz (offline rendering pipelines)
- Personal portfolio (students, career-changers, generalists)

The discipline scales from a beginner modeling their first prop to a senior artist running a production pipeline. The principles are the same. The depth of application scales with experience and asset complexity.

---

## This Repository

`3d-ref-skills` implements the Reference Engineering workflow as a set of AI skills for Claude Code, Cursor, Codex CLI, and Gemini CLI. Each skill corresponds to a phase of the workflow:

| Phase | Skill |
|-------|-------|
| Brief | `ref-brief` |
| Decode | `ref-style-decode` |
| Audit | `ref-audit` |
| Marketplace delivery | `ref-marketplace` |
| Client delivery | `ref-client` |
| VFX brief | `ref-vfx` |
| Texture brief | `ref-texture` |

The skills automate the framework. The framework exists independently of the skills. A 3D artist without any AI tooling can apply Reference Engineering manually using the documentation in this repository.

---

*Reference Engineering — coined and documented by Atharva Patil, Northbyte Studios, 2026.*
*github.com/p4inz-code/3d-ref-skills — MIT License*
