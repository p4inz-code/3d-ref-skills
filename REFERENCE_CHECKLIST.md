# Reference Engineering Checklist
**Standalone quick-reference — no AI required**

Print this. Pin it above your monitor. Check it before every new asset.

---

## BEFORE YOU OPEN YOUR DCC

### Layer 1 — Concept
- [ ] I know exactly what this asset is
- [ ] I know what it's for (game / film / marketplace / client)
- [ ] I know the art style (realistic / stylized / hand-painted)
- [ ] I know the poly budget and texture resolution
- [ ] I know what engine or pipeline this will live in

### Layer 2 — Silhouette
- [ ] I have 3–5 references showing the overall shape at distance
- [ ] I can draw the silhouette from memory as a black shape
- [ ] I know the primary forms (what 2–3 shapes make up the asset?)
- [ ] I know the proportion ratio (tall/wide, heavy/light, balanced/asymmetric)
- [ ] I know what makes this silhouette different from generic versions

### Layer 3 — Orthographic Views
- [ ] Front view — found / acknowledged unavailable
- [ ] Side (left) view — found / acknowledged unavailable
- [ ] Top view — found / acknowledged unavailable
- [ ] 3/4 hero angle — found (this is your presentation angle)
- [ ] If blueprints exist (vehicles, weapons, architecture): found and in PureRef

### Layer 4 — Scale
- [ ] Real-world H × W × D documented in cm or m
- [ ] Scale anchor object identified (human figure, door, vehicle, etc.)
- [ ] In-engine verification method planned (mannequin comparison, reference cube)
- [ ] Texel density calculated from scale (px/m for this asset)

### Layer 5 — Material (one cluster per surface)
- [ ] Every distinct surface type listed
- [ ] Each surface has its own reference cluster in PureRef / Kanvaz
- [ ] Dominant material identified (the one that sets the asset's read)
- [ ] Wear logic documented for each surface (where does damage concentrate?)
- [ ] PBR value range calibrated for each material type

### Layer 6 — Detail Zones
- [ ] Top 3–6 detail zones identified (areas of visual focus)
- [ ] Macro close-up photography gathered per zone
- [ ] Individual fasteners / seams / features referenced at correct scale
- [ ] Common mistake for this asset type noted and planned against

### Layer 7 — Deliver
- [ ] Hero angle identified and referenced
- [ ] Lighting setup reference gathered (what light this asset is designed for)
- [ ] 3–5 competitor / similar assets studied (what makes mine different?)
- [ ] Thumbnail composition researched (marketplace or client presentation)

---

## REFERENCE BOARD HEALTH CHECK

Run this before opening the DCC.

**Structure check:**
- [ ] Board has labeled zones (not a pile of images)
- [ ] Each zone corresponds to a layer in the pyramid
- [ ] I can navigate to any reference in under 10 seconds

**Coverage check:**
- [ ] Minimum 8–15 images per zone for a hero asset
- [ ] Total board: 50–90 images for hero / 20–40 for background prop
- [ ] No zone is represented by a single image

**Quality check:**
- [ ] Orthographic views: clean, measured or acknowledged unavailable
- [ ] Material references: macro close-up, not overview photos
- [ ] Scale reference: real-world anchor with known dimensions

**Diversity check:**
- [ ] I have both real-world photography AND style-matched 3D references
- [ ] I have not gathered 50 images of the same thing from the same angle
- [ ] I have references from multiple sources, not all from one artist or one era

---

## MID-MODELING CHECK (run at blockout completion)

- [ ] Proportions match orthographic reference from all 4 angles
- [ ] Scale verified in-engine against anchor object
- [ ] No major form changes expected — scale and shape locked
- [ ] Detail zones still have close-up reference ready for the detailing phase
- [ ] I know what the next reference gap will be and where to find it

---

## PRE-UV CHECK (run before UV unwrapping)

- [ ] Material reference is still accurate — nothing changed during modeling
- [ ] Texel density confirmed per surface
- [ ] Hero angle reference established — I know what the final render will look like
- [ ] Marketplace / client delivery reference ready (if applicable)

---

## COMMON REFERENCE GAPS BY ASSET TYPE

**Hard Surface (props, weapons, vehicles)**
- [ ] Panel line style and width reference
- [ ] Fastener/hardware macro reference
- [ ] Edge bevel width reference
- [ ] Material transition reference at every seam

**Organic (characters, creatures, plants)**
- [ ] Underlying anatomy/structure reference (not just surface)
- [ ] Deformation zone reference (joints, stretch, compression)
- [ ] Surface micro-variation reference (pores, scales, follicles)
- [ ] SSS zone reference (ears, fingers, nose for skin)

**Environment (architectural, modular, natural)**
- [ ] Human figure for scale context
- [ ] Modular tiling reference (assembled, not just individual pieces)
- [ ] Time-of-day / lighting context reference
- [ ] Weathering logic reference (gravity-driven, not random)

**VFX (particles, simulations, effects)**
- [ ] Real-world motion reference per phase (onset / peak / dissipation)
- [ ] Color gradient reference (core / mid / edge zones)
- [ ] Scale comparison reference
- [ ] Timing reference with frame counter

---

## QUICK SOURCE LIST

| Need | Go To |
|------|-------|
| Silhouette and style | ArtStation — filter "3D" |
| Blueprints | The-Blueprints.com / US Army field manuals (public domain) |
| Surface macro photos | AmbientCG / Texture.com / your phone camera |
| Scale reference | Wikipedia — search object + "dimensions" |
| Motion reference (VFX) | The Slow Mo Guys (YouTube) / USGS media library |
| Anatomy | Anatomy for Sculptors / Line of Action |
| Copyright-safe photography | Unsplash / Pexels / WikiMedia Commons |
| Competitor research | Fab.com / Sketchfab Store / ArtStation Marketplace |

---

## THE ONE RULE

**Gather in order: silhouette → orthographic → scale → material → detail → delivery.**

Skipping layers is not faster. It is a debt paid at delivery.

---

*Reference Engineering Checklist v2.1.0*
*github.com/p4inz-code/3d-ref-skills — MIT License — Free Forever*
*Made by Atharva Patil — Northbyte Studios*
