# V2 STRUCTURE — 3d-ref-skills
Designed: 2026-06-20

---

## Repository Hierarchy

```
3d-ref-skills/
│
├── README.md                          ← Product landing page. 5-second hook. Workflow diagram.
├── LICENSE                            ← MIT
├── CHANGELOG.md                       ← Living version history
├── CONTRIBUTING.md                    ← Contributor guide with skill template
├── .gitattributes                     ← Line ending consistency
│
├── REFERENCE_ENGINEERING.md           ← Discipline definition. The "why" behind everything.
├── REFERENCE_SYSTEM.md                ← How the skills connect as a workflow system.
├── REFERENCE_PYRAMID.md               ← Visual hierarchy of reference types.
├── REFERENCE_CHECKLIST.md             ← Standalone quick-reference card. No AI required.
├── REFERENCE_MISTAKES.md              ← Common mistakes, symptoms, and fixes.
│
├── skills/
│   ├── ref-brief/                     ← Pre-production reference brief generator
│   │   ├── SKILL.md
│   │   └── examples/
│   │       └── zombie-barricade-crate-brief.md
│   │
│   ├── ref-style-decode/              ← Style deconstruction framework
│   │   ├── SKILL.md
│   │   └── examples/
│   │       └── scifi-weapon-style-decode.md
│   │
│   ├── ref-audit/                     ← Mid-production reference board audit
│   │   ├── SKILL.md
│   │   └── examples/
│   │       └── zombie-survivor-character-audit.md
│   │
│   ├── ref-marketplace/               ← Modeling + marketing reference for marketplace
│   │   ├── SKILL.md
│   │   └── examples/
│   │       └── modular-ruins-kit-fab-brief.md
│   │
│   ├── ref-client/                    ← Client scope and visual alignment for freelance
│   │   ├── SKILL.md
│   │   └── examples/
│   │       └── scifi-pistol-client-alignment.md
│   │
│   ├── ref-vfx/                       ← VFX simulation reference brief [v2.1 NEW]
│   │   ├── SKILL.md
│   │   └── examples/
│   │       └── fire-explosion-vfx-brief.md
│   │
│   └── ref-texture/                   ← Texture and material reference brief [v2.1 NEW]
│       ├── SKILL.md
│       └── examples/
│           └── concrete-pbr-texture-brief.md
│
└── docs/
    ├── sources.md                     ← Curated reference source directory
    ├── KANVAZ_WORKFLOW.md             ← Step-by-step Kanvaz + 3d-ref-skills integration
    ├── VFX_REFERENCE_WORKFLOW.md      ← Standalone VFX reference guide [v2.1 NEW]
    └── TEXTURE_REFERENCE_WORKFLOW.md  ← Standalone texture reference guide [v2.1 NEW]
```

---

## Skill Hierarchy

Skills are organized by production phase, not by asset type.

```
PRE-PRODUCTION PHASE
├── ref-brief          → What references do I need before I start?
├── ref-style-decode   → How do I understand a reference deeply enough to apply it?
└── ref-vfx            → What references do I need for a VFX element? [v2.1]

MID-PRODUCTION PHASE
├── ref-audit          → What is missing from my reference board right now?
└── ref-texture        → What references do I need before I start texturing? [v2.1]

DELIVERY PHASE
├── ref-marketplace    → How do I reference both the asset AND its marketing?
└── ref-client         → How do I align with a client before I start?
```

**Skill naming convention:** All skills use the `ref-` prefix. This makes them easy to search, easy to tab-complete, and clearly scoped to the Reference Engineering discipline.

**Future skill naming:** Any skill added by contributors must follow the `ref-[noun]` pattern. The noun describes the output type, not the asset type. `ref-character` (output: character reference brief) not `ref-modeling-character` (describes process, not output).

---

## Documentation Hierarchy

Documents are organized by purpose: discipline → system → workflow → reference.

```
DISCIPLINE LAYER (why this exists)
├── REFERENCE_ENGINEERING.md    ← Definition of the discipline
└── REFERENCE_PYRAMID.md        ← Visual hierarchy of reference types

SYSTEM LAYER (how it connects)
├── REFERENCE_SYSTEM.md         ← How skills connect as a workflow
└── REFERENCE_MISTAKES.md       ← Named failure modes of reference gathering

TOOL LAYER (how to use it)
├── REFERENCE_CHECKLIST.md      ← Standalone checklist, no AI required
└── CONTRIBUTING.md             ← How to extend the system

INTEGRATION LAYER (works with)
├── docs/KANVAZ_WORKFLOW.md                  ← Kanvaz integration
├── docs/VFX_REFERENCE_WORKFLOW.md           ← VFX standalone guide
└── docs/TEXTURE_REFERENCE_WORKFLOW.md       ← Texture standalone guide

SOURCE LAYER (where to gather)
└── docs/sources.md             ← Curated reference source directory
```

---

## Workflow Hierarchy

The Reference Engineering workflow in order:

```
1. BRIEF (ref-brief / ref-vfx / ref-texture)
   ↓ Produces: structured reference brief document
   
2. GATHER (manual + Kanvaz / PureRef)
   ↓ Produces: organized reference board with labeled zones
   
3. DECODE (ref-style-decode)
   ↓ Produces: style decode document with "apply this" actions
   
4. AUDIT (ref-audit)
   ↓ Produces: audit report with PASS/PARTIAL/FAIL per check
   
5. MODEL (DCC)
   ↓ Re-audit at blockout and pre-UV
   
6. DELIVER (ref-marketplace / ref-client)
   ↓ Produces: marketplace brief or client alignment document
```

---

## Examples Hierarchy

Examples are organized by skill, named by asset type.

**Naming convention:** `[asset-type]-[descriptor]-[skill-type].md`

Examples demonstrate:
- One real-world asset type per skill (existing)
- Range: at least one hard surface and one organic across the pack (target)
- The complete output format, not a shortened version

Examples are never:
- Shortened to save space
- Generic or hypothetical
- Produced for fictional asset types that don't exist in real production

---

## Future Expansion Hierarchy

Skills can be added in three tiers:

**Tier 1 — Production Phase Skills (highest priority)**
Skills that address a distinct production phase with unique reference needs not covered by existing skills.
- `ref-character` — Character reference deep-dive (anatomy, facial topology, deformation)
- `ref-archviz` — Architecture and visualization reference
- `ref-hardsurface` — Hard surface reference specialist (panel systems, greebling, industrial design)
- `ref-creature` — Creature design reference (anatomy departure rules, surface variation)

**Tier 2 — Specialist Skills (medium priority)**
Skills for specific communities with unique reference workflows.
- `ref-concept` — Concept-to-3D reference translation
- `ref-vehicle` — Vehicle-specific reference (blueprints, mechanical reference, LOD strategy)
- `ref-environment-kit` — Modular kit design reference (grid planning, hero vs filler ratio)

**Tier 3 — Integration Skills (lower priority, requires ecosystem)**
Skills that integrate with specific tools beyond PureRef/Kanvaz.
- `ref-substance` — Substance Designer-specific reference workflow
- `ref-zbrush` — ZBrush sculptural reference (plane breaks, form language, noise reference)

**Rejection criteria for new skills:**
- Duplicates reference type already covered by existing skill
- Asset-type specific without a unique reference workflow distinction
- Addresses modeling, texturing, or rendering technique rather than reference
- Written as a tutorial rather than a reference engineering framework
