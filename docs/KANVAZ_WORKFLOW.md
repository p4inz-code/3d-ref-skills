# Kanvaz + 3d-ref-skills Workflow

[Kanvaz](https://github.com/p4inz-code/kanvaz) is a free, offline, infinite-canvas
reference board application for 3D and VFX artists. It runs locally — no cloud,
no telemetry, no subscription.

These AI skills generate your reference brief. Kanvaz is where you build the board.
This document shows the complete workflow from start to finish.

---

## The Two Tools

| Tool | Role |
|------|------|
| **3d-ref-skills** (this repo) | Tells you what references to gather and where to find them |
| **[Kanvaz](https://github.com/p4inz-code/kanvaz)** | The canvas where you organize and study those references |

They are designed to work together. The skills produce structured briefs with
labeled zones — Kanvaz provides labeled zones on an infinite canvas.
The workflow locks together.

---

## Complete Workflow — Step by Step

### Step 1 — Run ref-brief in Claude Code

Before opening Kanvaz, generate your reference brief:

```
"I'm about to model a rusted post-apocalyptic cargo crate for UE5 game-ready
 asset. Give me a reference brief."
```

Claude returns a full structured brief including:
- Silhouette queries (5 specific search queries)
- Orthographic view checklist
- Material surface breakdown with separate search queries per surface
- Scale anchor
- Detail zone close-ups with search queries
- PureRef board layout diagram

**Save the brief** as `ref-brief_[assetname]_v1.md` in your project folder.

---

### Step 2 — Open Kanvaz and Create Zones

Open Kanvaz and create a new board named `[AssetName]_refs_v1`.

Set up zones matching the brief's board layout:

```
┌──────────────────────────┬──────────────────────────┐
│  SILHOUETTE &            │  ORTHOGRAPHIC            │
│  SHAPE LANGUAGE          │  VIEWS                   │
├──────────────────────────┼──────────────────────────┤
│  MATERIAL DETAIL         │  SCALE ANCHORS           │
│  (one zone per surface)  │  & PROPORTIONS           │
├──────────────────────────┼──────────────────────────┤
│  DETAIL ZONES            │  LIGHTING &              │
│  (macro close-ups)       │  RENDER MOOD             │
└──────────────────────────┴──────────────────────────┘
```

Label each zone. In Kanvaz, you can add text labels directly on the canvas.
Use the brief's zone names exactly — this lets you quickly find references
when modeling and you need to check a specific detail.

---

### Step 3 — Gather Using the Brief's Queries

Open your browser alongside Kanvaz (side by side or on a second monitor).

Work through the brief zone by zone, in order:

**Zone 1 — Silhouette and Shape Language:**
Use the 5 search queries from the brief. Sources: ArtStation, Pinterest, Google Images.
Target: 8–15 images per zone.
Drag images directly from the browser into the Kanvaz zone.

**Zone 2 — Orthographic Views:**
Use the sources specified in the brief's orthographic checklist.
Blueprints go here — clean, scaled, technical.
Target: all available views found or acknowledged unavailable.

**Zone 3 — Material Detail (one sub-zone per surface):**
Use the per-surface search queries from the brief's material breakdown.
Close-up macro photography only. No overview shots in this zone.
Target: 8–12 images per surface type.

**Zone 4 — Scale Anchors:**
The reference object from the brief's scale anchor section.
A photo of the scale anchor object (human figure, door, vehicle)
placed next to the asset in a real-world photo if possible.

**Zone 5 — Detail Zones:**
Use the search queries from the brief's detail focus zones.
These are macro close-ups — individual fasteners, seams, surface grain.
Target: 6–10 images per detail zone.

**Zone 6 — Lighting and Render Mood:**
The render and lighting reference from the brief's lighting section.
Images showing similar assets under the target light setup.
Target: 8–12 images.

---

### Step 4 — Run ref-audit Before Opening DCC

When the board is built, run the audit before touching your DCC:

```
"Audit my reference board. I have: [describe what's in each zone of your
 Kanvaz board]. I'm about to model a rusted post-apocalyptic cargo crate."
```

Claude checks your board against the production audit framework and returns:
- PASS / PARTIAL / FAIL per check
- Critical gaps (fix now)
- Important gaps (fix before texturing)
- Immediate action (the one thing to do before opening the DCC)

Fix every critical gap. Close the important gaps you can close quickly.
Acknowledge the rest and note where in the production process you'll address them.

---

### Step 5 — Model with Kanvaz Alongside Your DCC

Open Kanvaz on one monitor. Open Maya, Blender, or your DCC on the other.

During modeling:
- When making a silhouette decision → Kanvaz silhouette zone
- When checking proportions → Kanvaz orthographic zone
- When modeling a specific surface → Kanvaz material zone for that surface
- When adding a detail → Kanvaz detail zone for that feature

Never model a decision you don't have reference for. If you reach a decision point
without reference, stop, find the reference, add it to Kanvaz, continue.

---

### Step 6 — Re-Audit at Blockout Completion

When blockout is complete, run ref-audit again:

```
"Re-audit my references at blockout completion. My cargo crate blockout is done.
 The board has [describe current state]. What's missing before I go to detail?"
```

This second audit catches gaps that weren't obvious before modeling started —
edge bevel reference, specific fastener type, how a particular material transition
should look. These gaps are normal and expected. Address them before detailing begins.

---

### Step 7 — Delivery (Marketplace or Client)

**For marketplace assets:**
```
"Generate a ref-marketplace brief for this crate — it's going to Fab.com as
 part of a post-apocalyptic environment kit, UE5, $34.99 target price."
```

Add a new zone to your Kanvaz board: **MARKETPLACE / MARKETING REFERENCE**
Populate it with the marketing reference from the ref-marketplace brief:
- Thumbnail composition examples
- Competitor asset presentation analysis
- Feature screenshot style reference

**For client commissions:**
```
"Generate a ref-client document for this commission. Client wants: [brief]."
```

The ref-client output is a document to send to the client — not a Kanvaz zone.
Save it as `client-alignment_[projectname]_v1.md` and send Section 2 to the client.

---

## Kanvaz Tips for Reference Engineering

**Name your boards with version numbers:**
`CargoCrate_refs_v1` → `CargoCrate_refs_v2` (after blockout re-audit)
This preserves your reference history and shows your process if you're building a portfolio.

**Use Kanvaz's infinite canvas for zone expansion:**
If a material zone grows beyond 15 images, give it more horizontal space.
Some complex assets need large material zones — the canvas handles this.

**Keep the board open during texturing:**
The material and detail zones are equally valuable during texturing as during modeling.
Don't close the board when you move to Substance Painter or your texturing tool.

**Screenshot your final Kanvaz board:**
A screenshot of a well-organized reference board is portfolio content.
It demonstrates professional pre-production process — exactly what studios look for.

---

## Quick Start

1. Install Kanvaz: [github.com/p4inz-code/kanvaz](https://github.com/p4inz-code/kanvaz)
2. Install 3d-ref-skills: `claude skill add p4inz-code/3d-ref-skills`
3. Run `ref-brief` → build board in Kanvaz → run `ref-audit` → model

That's the workflow. Start with one asset. The system becomes habit.

---

*Kanvaz Workflow v2.1.0*
*3d-ref-skills: github.com/p4inz-code/3d-ref-skills*
*Kanvaz: github.com/p4inz-code/kanvaz*
*MIT License — Free Forever*
