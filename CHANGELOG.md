# Changelog

All notable changes to `3d-ref-skills` are documented here.

---

## [3.0.0] — 2026-06-20 — Final Release

### Added — New Skills
- `ref-character` — Complete character reference brief covering proportion,
  anatomy, facial topology, deformation zones, costume, hair, and skin
- `ref-hardsurface` — Specialist hard surface brief covering design language,
  panel systems, bevel calibration, fastener reference, and greebling density

### Upgraded — All Existing Skills to v3.0.0
- `ref-brief` — Added camera distance consideration (FPS/TPS/isometric/cinematic),
  modular kit section, 4th intake question, image count targets per distance
- `ref-style-decode` — Added 9th dimension: production era detection
  (pre-PBR / early-PBR / modern-PBR / path-traced) with platform-specific guidance
- `ref-audit` — Added VFX asset type checks (V1–V4): phase motion, scale,
  color zones, timing reference
- `ref-marketplace` — Added platform-specific thumbnail requirements per store
  (Fab / Sketchfab / ArtStation / CGTrader / Gumroad), bundle strategy section
- `ref-client` — Added payment terms, deposit structure, kill fee clause,
  IP ownership clause — the three things freelancers get burned on most
- `ref-vfx` — Added weather/environmental effects (rain, snow, lightning, wind),
  looping VFX section, magic/stylized effects section with indirect reference strategy
- `ref-texture` — Added fabric/cloth section, skin/organic section with SSS guidance,
  trim sheet specific workflow

### Repository
- All 9 skills on version 3.0.0
- README updated: skills badge 9, new skills in skill table and examples table
- FINAL_REPOSITORY_TREE.md updated for v3 structure

---

## [2.1.0] — 2026-06-20 — Reference Engineering Release
- Added ref-vfx, ref-texture
- Added full Reference Engineering documentation suite
- README rebuilt as product landing page

## [2.0.0] — 2026-06-20 — Initial Public Release
- ref-brief, ref-style-decode, ref-audit, ref-marketplace, ref-client
- Full examples for all 5 skills
- docs/sources.md, CONTRIBUTING.md, LICENSE

---

## Future (community-maintained after v3.0.0)
- ref-creature, ref-vehicle, ref-environment-kit
- docs/VFX_REFERENCE_WORKFLOW.md, docs/TEXTURE_REFERENCE_WORKFLOW.md
- GLOSSARY.md, QUICKSTART.md, SECURITY.md
- GitHub issue templates

---

## [3.1.0] — 2026-06-22 — Persona Audit Fixes

### Fixed — Tier 1 (trust-critical)
- README version badge: `v2.1.0` → `v3.0.0`
- README hero tagline: "Seven skills" → "Nine skills" (2 instances)
- README skills table: "8-dimension decode" → "9-dimension decode"
- CONTRIBUTING.md: removed ref-character and ref-hardsurface from wanted list
  (they shipped in v3.0.0) — added note pointing to them as examples

### Fixed — Tier 2 (stale docs)
- OPEN_ISSUES.md: archived resolved issues, added current v3-era open items
- FUTURE_ROADMAP.md: marked ref-character and ref-hardsurface as COMPLETED v3.0.0
- FINAL_REPOSITORY_TREE.md: updated to v3.0.0 showing all 9 skills
- Moved 6 planning/audit docs from root to docs/meta/:
  RESEARCH_REPORT.md, FIVE_WHYS_ANALYSIS.md, V2_STRUCTURE.md,
  AUDIT_TECHNICAL.md, AUDIT_USER_VALUE.md, AUDIT_PUBLIC_RELEASE.md
  Root now has 12 files (down from 18)

### Improved — Tier 3 (retention)
- README install section: added "No AI agent yet?" entry point → REFERENCE_CHECKLIST.md
- README roadmap: replaced stale v2.1.0/v3.0.0 planned section with accurate
  v3.0.0 current release summary highlighting key upgrades
- README FAQ: expanded offline/no-AI answer from 1 line to 3 lines
