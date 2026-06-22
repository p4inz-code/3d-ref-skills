<div align="center">

# 3d-ref-skills

### Reference Engineering for 3D Artists

**The first AI skill pack built entirely for pre-production reference workflows.**

Nine skills. Free forever. MIT. Works with any DCC, any engine, any AI agent.

[![Version](https://img.shields.io/badge/version-3.0.0-blue)](./CHANGELOG.md)
[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE)
[![Skills](https://img.shields.io/badge/skills-9-orange)](./skills/)
[![Agents](https://img.shields.io/badge/agents-Claude%20%7C%20Cursor%20%7C%20Codex%20%7C%20Gemini-purple)](./README.md#-works-with)
[![DCC](https://img.shields.io/badge/DCC-Maya%20%7C%20Blender%20%7C%20ZBrush%20%7C%20Houdini%20%7C%20any-red)](./README.md#-works-with)

</div>

---

## The Real Reason Your Model Looks Wrong

Not your topology. Not your textures. Not your lighting.

Your reference board.

> Shallow silhouette refs. No scale anchor. One mood board for seven materials.
> Imperfections placed randomly. VFX tuned by guesswork.
> The model looks wrong. The artist blames their skill.
> **The real cause is always the reference.**

`3d-ref-skills` solves this before you open your DCC.

---

## What Is This?

Nine AI skills that implement **Reference Engineering** — the discipline of
systematically gathering, validating, and auditing references before production begins.

Run a skill. Get a structured document. Build the right board. Model with confidence.

→ [What is Reference Engineering?](./REFERENCE_ENGINEERING.md)
→ [What order should I gather in?](./REFERENCE_PYRAMID.md)
→ [How do the skills connect?](./REFERENCE_SYSTEM.md)

---

## The Workflow

```
 START
   │
   ├─ New 3D asset?     ──▶  ref-brief        "I'm starting a prop / character / environment"
   ├─ VFX effect?       ──▶  ref-vfx          "I'm building fire / smoke / explosion"
   └─ Texturing?        ──▶  ref-texture      "I'm about to open Substance"
                                    │
                                    ▼
                             GATHER REFERENCES
                          (PureRef / Kanvaz board)
                                    │
                                    ▼
                          ref-style-decode     "Why does this reference work?"
                                    │
                                    ▼
                          ref-audit            "Is my board complete?"
                                    │
                                    ▼
                              OPEN YOUR DCC
                        Every decision has a reference.
                                    │
                         ┌──────────┴──────────┐
                         ▼                     ▼
                  ref-marketplace         ref-client
                  "Selling on Fab"    "Freelance commission"
```

---

## See It in Action

<!-- GIF: 30-second screen recording of Claude Code generating a ref-brief output -->
<!-- Record: type "I'm about to model a rusted cargo crate for UE5" → show full brief generating -->
<!-- Replace this comment block with: ![ref-brief demo](./docs/demo.gif) -->

> **Demo coming soon.** In the meantime, see the full example outputs below.

---

## The 9 Skills

| Skill | When to use it | What you get |
|-------|---------------|--------------|
| [`ref-brief`](./skills/ref-brief/) | Before modeling any asset | Complete reference brief — silhouette, ortho, materials, scale, detail zones |
| [`ref-vfx`](./skills/ref-vfx/) | Before building any VFX | Per-phase motion reference, color channels, timing, pipeline setup |
| [`ref-texture`](./skills/ref-texture/) | Before texturing any surface | Macro/meso/micro framework, PBR calibration, tiling strategy |
| [`ref-style-decode`](./skills/ref-style-decode/) | When you want to match a style | 9-dimension decode — shape, surface, detail density, color, lighting, topology |
| [`ref-audit`](./skills/ref-audit/) | When something feels wrong | PASS/PARTIAL/FAIL audit — every gap named, every fix specified |
| [`ref-marketplace`](./skills/ref-marketplace/) | Before submitting to Fab/Sketchfab | Modeling brief + marketing brief in one document |
| [`ref-client`](./skills/ref-client/) | Before any freelance commission | Scope doc, visual questionnaire, revision risk register, milestone gates |

---

## See It Before You Install

Real outputs. Real asset types. Not shortened for the README.

| Skill | Example |
|-------|---------|
| `ref-brief` | [Zombie Barricade Crate — UE5 game prop](./skills/ref-brief/examples/zombie-barricade-crate-brief.md) |
| `ref-vfx` | [Molotov Explosion — HTML5 Dead Corps game](./skills/ref-vfx/examples/molotov-explosion-vfx-brief.md) |
| `ref-texture` | [Weathered Concrete PBR — Fab texture pack](./skills/ref-texture/examples/concrete-pbr-texture-brief.md) |
| `ref-style-decode` | [Halo MA40 Assault Rifle — style breakdown](./skills/ref-style-decode/examples/scifi-weapon-style-decode.md) |
| `ref-audit` | [Zombie Survivor Character — mid-model audit](./skills/ref-audit/examples/zombie-survivor-character-audit.md) |
| `ref-marketplace` | [Modular Ruins Kit — Fab launch brief](./skills/ref-marketplace/examples/modular-ruins-kit-fab-brief.md) |
| `ref-client` | [Sci-Fi Pistol Commission — client alignment](./skills/ref-client/examples/scifi-pistol-client-alignment.md) |
| `ref-character` | [Zombie Soldier Character — Dead Corps game](./skills/ref-character/examples/zombie-soldier-character-brief.md) |
| `ref-hardsurface` | [Volt-9 Energy Pistol — hard surface brief](./skills/ref-hardsurface/examples/volt9-energy-pistol-hardsurface-brief.md) |

---

## Install in 30 Seconds

> **What is Claude Code?** It's Anthropic's AI coding agent — a terminal tool that reads `SKILL.md` files and uses them to give context-aware assistance. Install it at [claude.ai/code](https://claude.ai/code). Cursor, Codex CLI, and Gemini CLI work the same way. If you don't use any of these, skip to the "No AI agent yet?" line below.

**Claude Code — global (recommended):**
```bash
claude skill add p4inz-code/3d-ref-skills
```

**Manual — Claude Code, Cursor, Codex, Gemini:**
```bash
git clone https://github.com/p4inz-code/3d-ref-skills.git
```
Then copy the `skills/` folder into your agent's skills directory.

**No AI agent yet?** [REFERENCE_CHECKLIST.md](./REFERENCE_CHECKLIST.md) works as a standalone print-and-pin checklist — no AI, no install, no account required. Start there →

| Agent | Directory |
|-------|-----------|
| Claude Code (global) | `~/.claude/skills/` |
| Claude Code (project) | `.claude/skills/` |
| Cursor | `.cursor/skills/` |
| Codex CLI / Gemini CLI | See your agent's docs |

---

## How to Trigger Each Skill

Just describe what you need. No commands. No syntax.

```
"I'm about to model a rusted sci-fi cargo crate for UE5."          → ref-brief
"I'm building a Molotov explosion effect for my game."              → ref-vfx
"I'm about to texture weathered urban concrete for Fab."            → ref-texture
"Decode this ArtStation piece — why does it look so good?"          → ref-style-decode
"My character's face looks flat. Audit my reference board."         → ref-audit
"I'm selling a modular ruins kit on Fab. Give me a launch brief."   → ref-marketplace
"I have a freelance commission for a sci-fi pistol."                → ref-client
```

---

## ✅ Works With

**AI Agents:** Claude Code · Cursor · GitHub Copilot / Codex CLI · Gemini CLI · any agent that reads SKILL.md

**DCC:** Maya · Blender · ZBrush · 3ds Max · Houdini · Cinema 4D · Modo · any DCC

**Engines:** UE5 · Unity · Godot · Blender Cycles · Arnold · Redshift · WebGL · film · archviz

---

## 📚 Documentation

Everything you need to understand and use the system — with or without AI.

| Document | What it is |
|----------|-----------|
| [REFERENCE_ENGINEERING.md](./REFERENCE_ENGINEERING.md) | The discipline — 7 principles, full workflow, terminology |
| [REFERENCE_PYRAMID.md](./REFERENCE_PYRAMID.md) | The hierarchy — what order to gather in and why |
| [REFERENCE_SYSTEM.md](./REFERENCE_SYSTEM.md) | The workflow — how all 9 skills connect |
| [REFERENCE_CHECKLIST.md](./REFERENCE_CHECKLIST.md) | Printable checklist — works without any AI |
| [REFERENCE_MISTAKES.md](./REFERENCE_MISTAKES.md) | The 10 most common failures — symptoms, causes, fixes |
| [docs/sources.md](./docs/sources.md) | Where to find references — curated, organized, copyright-noted |
| [docs/KANVAZ_WORKFLOW.md](./docs/KANVAZ_WORKFLOW.md) | Step-by-step Kanvaz + skills integration |

---

## 🖼 Reference Board Tool

**[Kanvaz](https://github.com/p4inz-code/kanvaz)** — free, offline, infinite-canvas reference board for 3D and VFX artists. No cloud. No telemetry. Your files never leave your machine.

These skills generate your brief → Kanvaz is where you build the board.
Full integration guide: [docs/KANVAZ_WORKFLOW.md](./docs/KANVAZ_WORKFLOW.md)

---

## 🗺 Repository Map

```
3d-ref-skills/
│
├── REFERENCE_ENGINEERING.md     ← Start here if you're new
├── REFERENCE_PYRAMID.md         ← The order that matters
├── REFERENCE_SYSTEM.md          ← How skills connect
├── REFERENCE_CHECKLIST.md       ← Print this and pin it
├── REFERENCE_MISTAKES.md        ← Read when something looks wrong
│
├── skills/
│   ├── ref-brief/               ← Before any asset
│   ├── ref-vfx/                 ← Before any VFX
│   ├── ref-texture/             ← Before texturing
│   ├── ref-style-decode/        ← To understand a reference
│   ├── ref-audit/               ← To check your board
│   ├── ref-marketplace/         ← To sell on Fab
│   ├── ref-client/              ← For commissions
│   ├── ref-character/           ← Character assets
│   └── ref-hardsurface/         ← Hard surface props, weapons
│
└── docs/
    ├── sources.md               ← Where to find refs
    └── KANVAZ_WORKFLOW.md       ← Kanvaz integration
```

---

## 🚀 Roadmap

**v3.0.0 — Current Release**
- ✅ 9 skills with full examples (2 new: ref-character, ref-hardsurface)
- ✅ All 7 existing skills upgraded — camera distance logic, deformation zones,
  weather VFX, fabric/skin/trim texture, 9-dimension style decode
- ✅ ref-client: payment terms, kill fee clause, IP ownership — freelance-ready
- ✅ ref-marketplace: platform-specific briefs for Fab, Sketchfab, ArtStation, CGTrader
- ✅ ref-vfx: weather effects, looping VFX, magic/stylized indirect reference strategy
- ✅ Planning docs moved to docs/meta/ — clean root

**Community-maintained (post v3.0.0)**
- `ref-creature` — Creature and monster reference
- `ref-vehicle` — Vehicle blueprints, mechanical, LOD strategy
- `ref-environment-kit` — Modular grid, hero vs filler, tiling strategy
- `docs/VFX_REFERENCE_WORKFLOW.md` — Standalone VFX guide
- `docs/TEXTURE_REFERENCE_WORKFLOW.md` — Standalone texture guide

[Watch this repo](https://github.com/p4inz-code/3d-ref-skills/watchers) to get notified.

---

## 🤝 Contributing

You don't need to know how to code. If you know 3D production, you can write a skill.

Skills needed by the community:
- `ref-archviz` · `ref-creature` · `ref-vehicle` · `ref-environment-kit`

See [CONTRIBUTING.md](./CONTRIBUTING.md) — includes a copy-paste skill template.

---

## ❓ FAQ

**Does this work offline / without AI?**
Yes. [REFERENCE_CHECKLIST.md](./REFERENCE_CHECKLIST.md) works standalone — no AI agent, no install, no account.
Print it, pin it above your monitor, and check each layer before opening your DCC.
The AI skills accelerate the workflow and go deeper, but the checklist is the foundation and it works for everyone.

**Does this work with Blender / Maya / ZBrush?**
Yes. Every skill is DCC-agnostic — they generate reference briefs, not tool-specific instructions.

**What's the difference between `ref-brief` and `ref-audit`?**
`ref-brief` tells you what to gather before you start.
`ref-audit` checks whether you gathered the right things.
Use both. In that order.

**Is this really free forever?**
MIT license. Free forever. Use it on paid work, marketplace assets, client commissions — anything.

**How do I contribute a skill?**
Fork → add your `SKILL.md` + at least one example → open a PR.
Full instructions in [CONTRIBUTING.md](./CONTRIBUTING.md).

---

<div align="center">

**MIT · Free Forever · No account required**

Made by [Atharva Patil](https://github.com/p4inz-code) — Northbyte Studios · Navi Mumbai, India

*If this saved you from a bad reference board, a ⭐ helps other artists find it.*

</div>
