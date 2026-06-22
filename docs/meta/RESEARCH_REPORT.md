# RESEARCH REPORT — 3d-ref-skills v2 Audit
Conducted: 2026-06-20
Auditor: Senior QA / Senior Open Source Maintainer / Senior Technical Writer

---

## STRENGTHS

### Skills
- `ref-brief` — Complete, structured, production-accurate. The intake → brief → checklist flow is correct. The PureRef board layout diagram is unique and highly practical.
- `ref-audit` — The strongest skill in the pack. Asset-type branching (hard surface / organic / environment / character) is exactly how production pipelines think. The PASS/PARTIAL/FAIL system is clear and actionable.
- `ref-style-decode` — The 8-dimension framework is original and has no equivalent in any public AI skill pack. The "Apply This" closing section turns observation into action.
- `ref-marketplace` — The dual-layer (modeling + marketing) structure is genuinely unique. No competitor in the skill ecosystem covers the marketing reference gap.
- `ref-client` — The Revision Risk Register is the most practically valuable section in the entire pack. Freelancers will use this on every commission.

### Documentation
- `docs/sources.md` — Organized, current, opinionated. The copyright safety column is missing from most similar lists. This file is useful without the skills.
- `CONTRIBUTING.md` — Correctly structured. The "you don't need to code" opening removes the primary barrier for 3D artist contributors.
- Examples — All 5 skills have filled real-world examples. This is the single biggest trust signal in any open-source skill pack.

### Repository
- Cross-repo Kanvaz link creates an ecosystem narrative — rare for a v1 release.
- `.gitattributes` present — signals maintained repo.
- MIT license — zero friction for adoption.
- GitHub topics set — discoverable.

---

## WEAKNESSES

### Critical
1. **No concept of Reference Engineering as a discipline** — the repo presents skills as isolated tools rather than a unified workflow. There is no document that explains the philosophy, the system, or why these skills exist in a specific order. A first-time visitor sees 5 skills with no mental model for how they connect.

2. **README fails the 5-second test** — current README answers "what" but not "why this matters" or "what problem does this solve" in the first 5 seconds. The hero section is a badge row and a single sentence. A developer landing here for the first time has no immediate emotional hook.

3. **No workflow diagram** — there is no visual showing how ref-brief → ref-style-decode → ref-audit → ref-marketplace / ref-client flow together. A diagram would make the system immediately obvious.

4. **No system-level documentation** — there is no document explaining what Reference Engineering is, what the Reference Pyramid is, or what the common mistakes in reference gathering are. These are the documents that get shared independently and drive GitHub traffic.

5. **No VFX skill** — VFX artists are the most underserved community in AI tooling. `ref-vfx` is completely missing. This is the highest-value addition.

6. **No texture skill** — Texture artists (Substance, Fab texture packs, trim sheets) have no dedicated skill. `ref-texture` is missing.

### Important
7. **Skill descriptions in frontmatter are too long** — some agents truncate long descriptions. The `ref-client` description is 4 lines, `ref-brief` is 6 lines. Should be 2–3 lines maximum, with the most critical trigger phrase first.

8. **No KANVAZ_WORKFLOW.md** — the Kanvaz cross-link in the README is a single sentence. There is no document showing how the two tools work together step by step.

9. **No REFERENCE_CHECKLIST.md** — a standalone quick-reference checklist that works without the AI skills. This is the file that gets bookmarked and shared independently on forums and Discord servers.

10. **No REFERENCE_MISTAKES.md** — a document listing the most common reference gathering mistakes and what goes wrong as a result. This is highly shareable content that drives traffic.

11. **CONTRIBUTING.md lacks skill template** — the template block exists but the frontmatter fields are not explained. New contributors don't know what `description` triggers are or how the agent reads them.

12. **No FAQ** — common questions (does this work offline, does it work with Blender, what's the difference between ref-brief and ref-audit) are not answered anywhere in the repo.

### Minor
13. **CHANGELOG.md is sparse** — only v2.0.0. Should be treated as a living document.
14. **No skill for character reference** — missing from the pack despite being one of the most common 3D disciplines.
15. **No second example per skill** — each skill has one example. Two examples demonstrate range (e.g. one hard surface, one organic for ref-brief).
16. **Install command unverified** — `claude skill add p4inz-code/3d-ref-skills` is listed but the Claude Code skill registry may not have indexed this repo yet. Should note the manual install as primary until confirmed.

---

## MISSING WORKFLOWS

1. VFX simulation reference workflow (fire, smoke, water, destruction, Niagara, Houdini)
2. Texture reference workflow (tiling textures, trim sheets, Substance Designer/Painter)
3. Character reference deep-dive workflow (facial topology, anatomy, deformation)
4. The full pre-production workflow from concept → brief → board → audit → model

---

## MISSING DOCUMENTATION

1. `REFERENCE_ENGINEERING.md` — the discipline definition and philosophy
2. `REFERENCE_PYRAMID.md` — the hierarchy of reference types
3. `REFERENCE_SYSTEM.md` — how the skills connect as a system
4. `REFERENCE_CHECKLIST.md` — standalone quick-reference card
5. `REFERENCE_MISTAKES.md` — the most costly mistakes and their symptoms
6. `VFX_REFERENCE_WORKFLOW.md` — standalone VFX workflow guide
7. `TEXTURE_REFERENCE_WORKFLOW.md` — standalone texture workflow guide
8. `KANVAZ_WORKFLOW.md` — integration guide

---

## MISSING CONTRIBUTOR PATHWAYS

1. No skill template file contributors can copy and fill
2. No issue templates on GitHub (bug report, new skill proposal)
3. No PR checklist in CONTRIBUTING.md
4. No "good first contribution" guidance

---

## NAVIGATION ISSUES

1. No repo map — a visitor cannot see the full structure without clicking through folders
2. No internal cross-links between related skills (ref-brief links to ref-audit, etc.)
3. README does not link to docs/sources.md prominently enough
4. No index of all example outputs in one place

---

## RETENTION ISSUES

1. Nothing explains the progression — what order to use the skills in
2. No roadmap visible from the README — visitors don't know what's coming
3. No "star to follow progress" call to action beyond the footer line
4. The `docs/` folder is invisible — no README section dedicated to it

---

## CURRENT QUALITY SCORES (pre-v2)

| Category | Score | Reason |
|----------|-------|--------|
| Clarity | 7/10 | Skills are clear; system is not |
| Usefulness | 9/10 | Skills solve real problems |
| Navigation | 6/10 | No workflow, no map, no cross-links |
| Documentation | 6/10 | Skills documented; system undocumented |
| Shareability | 7/10 | Good skills; missing the shareable standalone docs |
| Retention | 6/10 | No progression, no roadmap, no system hooks |
| Professionalism | 8/10 | Clean structure; missing system layer |
| Beginner Value | 7/10 | Skills are usable but overwhelming without system context |
| Professional Value | 9/10 | ref-audit and ref-client are production grade |
| Contributor Experience | 6/10 | Template exists; guidance is thin |

**Overall pre-v2: 7.1/10**
**Target post-v2: 9.5/10**
