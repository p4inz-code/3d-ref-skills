# 3d-ref-skills

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Skills](https://img.shields.io/badge/skills-5-orange)
![AI Agents](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Cursor%20%7C%20Codex%20CLI%20%7C%20Gemini%20CLI-purple)
![3D](https://img.shields.io/badge/for-3D%20Artists%20%7C%20VFX%20%7C%20Freelance-red)

**The first AI skill pack dedicated entirely to 3D pre-production reference workflows.**

Before you open Maya, Blender, ZBrush, or any DCC — you need references.
The right ones. Organized the right way. These skills make sure you never
model from a shallow reference board again.

Free. Forever. MIT.

---

## What's in the pack

| Skill | What it does | Use it when |
|-------|-------------|-------------|
| [`ref-brief`](./skills/ref-brief/) | Generates a complete pre-production reference document for any 3D asset | Starting a new model |
| [`ref-style-decode`](./skills/ref-style-decode/) | Deconstructs *why* a reference looks the way it does — principles you can apply without copying | You want to match a style |
| [`ref-audit`](./skills/ref-audit/) | Audits your reference board mid-modeling and finds exactly what's missing | Something feels wrong |
| [`ref-marketplace`](./skills/ref-marketplace/) | Dual reference brief — modeling *and* marketing — for Fab, Sketchfab Store, ArtStation | Selling an asset |
| [`ref-client`](./skills/ref-client/) | Client-facing scope and visual alignment document before modeling begins | Freelance commission |

All skills work with **any DCC** — Maya, Blender, ZBrush, 3ds Max, Houdini, Cinema 4D.
All skills work with **any engine** — UE5, Unity, Godot, web, film, archviz.

---

## Install

**Claude Code:**
```bash
claude skill add p4inz-code/3d-ref-skills
```

**Manual (Claude Code, Cursor, Codex CLI, Gemini CLI):**
```bash
git clone https://github.com/p4inz-code/3d-ref-skills.git
```
Copy the `skills/` folder contents into your agent's skills directory:
- Claude Code global: `~/.claude/skills/`
- Claude Code per-project: `.claude/skills/` in your project root
- Cursor: `.cursor/skills/`
- Gemini CLI: follow your agent's skill import docs

---

## Works with

| Agent | Supported |
|-------|-----------|
| Claude Code | ✅ Primary target |
| Cursor | ✅ Tested |
| GitHub Copilot (Codex CLI) | ✅ Compatible |
| Gemini CLI | ✅ Compatible |
| Any agent that reads SKILL.md | ✅ |

---

## How to use

Once installed, trigger any skill by describing what you need:

**ref-brief:**
> "I'm about to model a rusted sci-fi cargo crate for UE5. Give me a reference brief."

**ref-style-decode:**
> "Decode the style of this ArtStation piece — why does it look so good and how do I apply it to my weapon model?"

**ref-audit:**
> "My character's face looks flat. Audit my reference board and tell me what I'm missing."

**ref-marketplace:**
> "I'm selling a modular ruins kit on Fab. Give me a marketplace brief for modeling and marketing it."

**ref-client:**
> "I have a freelance commission for a sci-fi pistol. Generate a client alignment document."

See the `examples/` folder inside each skill for full real-world output samples.

---

## Real output examples

- [Zombie barricade crate brief](./skills/ref-brief/examples/zombie-barricade-crate-brief.md) — `ref-brief`
- [Halo MA40 style decode](./skills/ref-style-decode/examples/scifi-weapon-style-decode.md) — `ref-style-decode`
- [Zombie survivor character audit](./skills/ref-audit/examples/zombie-survivor-character-audit.md) — `ref-audit`
- [Modular ruins kit Fab brief](./skills/ref-marketplace/examples/modular-ruins-kit-fab-brief.md) — `ref-marketplace`
- [Sci-fi pistol client alignment](./skills/ref-client/examples/scifi-pistol-client-alignment.md) — `ref-client`

---

## Curated reference sources

[`docs/sources.md`](./docs/sources.md) — A maintained list of the best reference sources for 3D artists, organized by what you're looking for: silhouettes, blueprints, surface macros, anatomy, environment, VFX, marketplace research. Useful even without the AI skills.

---

## Canvas recommendation

Build your reference boards in **[Kanvaz](https://github.com/p4inz-code/kanvaz)** — a free, offline, infinite-canvas reference board built specifically for 3D and VFX artists. Drop images, GIFs, video, and audio. No telemetry. Your files never leave your machine.

These skills generate your reference brief → Kanvaz is where you build the board.

---

## Coming in v2.1

- `ref-vfx` — Reference briefs for VFX elements: fire, smoke, water, destruction, Niagara and Houdini workflows
- `ref-texture` — Reference briefs for texture artists: tiling textures, trim sheets, Substance workflows, Fab texture packs

[Watch this repo](https://github.com/p4inz-code/3d-ref-skills/watchers) to get notified when v2.1 drops.

---

## Contributing

All 3D artists welcome. You don't need to know how to code — if you know 3D, you can write a skill.

See [CONTRIBUTING.md](./CONTRIBUTING.md) to get started. Ideas for new skills:
- `ref-character` — Character-specific reference deep-dive
- `ref-archviz` — Architecture and visualization reference workflows
- `ref-hardsurface` — Dedicated hard surface reference framework
- `ref-concept` — Reference gathering from the concept art side

---

## License

MIT — use it, fork it, build on it, sell assets made with it.

Made by **Atharva Patil** — [Northbyte Studios](https://github.com/p4inz-code), Navi Mumbai, India.

If this saves you time, a ⭐ star helps more 3D artists find it.
