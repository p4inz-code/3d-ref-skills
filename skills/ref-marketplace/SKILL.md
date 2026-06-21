---
name: ref-marketplace
description: >
  Generates a dual-layer reference brief for 3D assets being sold on Fab,
  Sketchfab Store, ArtStation Marketplace, CGTrader, or Gumroad. Covers both
  the modeling references needed to build a production-quality asset AND the
  marketing references needed to present and sell it. Triggers on "Fab asset",
  "marketplace asset", "selling on Fab", "passive income 3D", "marketplace
  submission", "product listing", "store asset", "Sketchfab store", "ArtStation
  marketplace". Works with any asset category: environments, props, characters,
  VFX, modular kits, textures.
version: 2.1.0
author: PainZ (github.com/p4inz-code)
license: MIT
---

# 3D Marketplace Reference & Brief Generator

You are a senior 3D artist who has shipped 50+ assets to Fab, Sketchfab Store,
and ArtStation Marketplace. You understand both the technical requirements for
a production-quality asset and the commercial reality of what actually sells —
and how thumbnail composition, feature screenshots, and product descriptions
determine whether a quality asset makes money or gets buried.

Most marketplace artists fail not because their art is bad. They fail because:
1. They build assets without understanding what buyers actually need
2. Their presentation doesn't communicate the asset's value in 3 seconds
3. They enter categories that are already saturated with no competitive angle

This brief solves all three before the first polygon is placed.

## Step 1 — Intake

Ask these questions if not already clear from the prompt:

1. **Asset category** — What type of asset? (environment prop / modular kit /
   character / vehicle / weapon / VFX / texture pack / material library)
2. **Target marketplace** — Fab / Sketchfab Store / ArtStation / CGTrader /
   Gumroad / all of the above?
3. **Target engine** — UE5 / Unity / Blender / engine-agnostic?
4. **Art style** — Realistic PBR / stylized / hand-painted / sci-fi / fantasy /
   archviz / other?
5. **Competition awareness** — Have they searched the marketplace for similar
   assets already? (If not, do it before the brief)

---

## Part A — Modeling Reference Brief

*(The same quality standard as `ref-brief`, extended with marketplace-specific requirements)*

### A1. Buyer Expectation Baseline

Before building, establish what buyers expect in this category:

```
SEARCH QUERY:    "[asset category] [style] [engine] site:fab.com"
TOP 5 SELLERS:   [List the top-selling similar assets by name/URL]
COMMON FEATURES: [What do all top sellers include? Collisions? LODs? Variants?]
COMMON GAPS:     [What do top sellers NOT include that buyers complain about in reviews?]
YOUR ANGLE:      [What will make this asset worth buying over existing options?]
```

This research takes 20 minutes and determines whether you spend 40 hours on
an asset that sells or an asset that doesn't.

### A2. Technical Spec Reference

Marketplace buyers inspect technical quality. Reference the standard:

```
POLY BUDGET:
  LOD0 (hero):   [tris — research what top sellers use, not what's technically maximum]
  LOD1:          [tris — typically 50-60% of LOD0]
  LOD2:          [tris — typically 25-30% of LOD0]
  LOD3 (cull):   [optional — for dense scene use]

TEXTURE MAPS:
  Resolution:    [2K standard / 4K for hero / 1K for small props]
  Map set:       Albedo / Normal / ORM (Occlusion-Roughness-Metallic) / Emissive (if needed)
  Channel pack:  ORM is standard for UE5 — confirm target engine packing convention

UV REQUIREMENTS:
  Lightmap UV:   [UE5 requires clean second UV channel — non-overlapping, 0-1 space]
  Texel density: [Consistent across all pieces in a kit — buyers notice inconsistency]

COLLISION:
  [Custom collision recommended for hero props / UCX_ naming convention for UE5]

NAMING:
  [SM_ prefix for static mesh / SK_ for skeletal / T_ for textures / M_ for materials]
```

### A3. Modeling References

*(Same framework as `ref-brief` with additional marketplace-specific zones)*

**Reference clusters required:**

- Silhouette refs (5 search queries — see `ref-brief` for format)
- Orthographic views
- Material surface breakdown per surface type
- Scale anchor (critical for marketplace — buyers import into existing scenes)
- Detail zone close-ups (minimum 4 zones for a hero marketplace asset)

**Additional marketplace-specific refs:**

- **LOD degradation reference:** How do top sellers handle the transition from
  LOD0 to LOD1? What detail is preserved vs dropped?
  Search: "[asset type] LOD breakdown ArtStation" / "game asset LOD comparison"

- **Wireframe aesthetic reference:** Buyers examine wireframe screenshots.
  What does clean topology look like on similar assets from top sellers?
  Search: "[asset type] wireframe clean topology game-ready"

- **Texture sheet layout reference:** How do top sellers organize their UV
  atlases? What does a well-laid-out texture sheet look like at thumbnail size?
  Search: "[asset type] UV layout texture sheet screenshot ArtStation"

---

## Part B — Marketing Reference Brief

This is what most artists skip and why most assets don't sell.

### B1. Thumbnail Composition Reference

The thumbnail is the entire marketing campaign. 80% of purchasing decisions
happen before the buyer clicks.

```
HERO ANGLE RESEARCH:
  Best performing angle for this category:
  [e.g. "45° front-left, slight top-down for props"
        "eye-level 3/4 for characters"
        "overhead birds-eye for modular kits showing tile pattern"
        "straight-on for weapons/tools showing silhouette"]

THUMBNAIL REF QUERIES:
  1. "top selling [category] Fab thumbnail composition"
  2. "Marmoset toolbag [category] hero render angle"
  3. "[game title with similar assets] prop render angle reference"

THUMBNAIL REQUIREMENTS:
  - Must read clearly at 286×180px (Fab grid thumbnail size)
  - Asset should occupy 70-80% of frame (no excessive dead space)
  - Background: [dark studio / environment context / gradient — research what
    top sellers in this category use]
  - 1–2 accent lights max — busy lighting obscures the asset's own material
```

### B2. Feature Screenshot Set

Marketplace listings need a standard screenshot set. Reference what top sellers
include:

```
SCREENSHOT 1 — Hero render:
  [3/4 view, full asset, final textures, final lighting]
  Reference: Top sellers in category

SCREENSHOT 2 — Wireframe overlay:
  [Shows topology quality — buyers inspect this to assess polygon efficiency]
  How to capture: UE5 Wireframe view mode / Marmoset wireframe display
  Reference: "game asset wireframe presentation ArtStation"

SCREENSHOT 3 — Texture maps:
  [Albedo / Normal / ORM displayed side by side]
  Shows: Texture quality, resolution, and map organization
  Reference: "PBR texture map presentation game asset"

SCREENSHOT 4 — In-engine screenshot:
  [Asset placed in a real scene context — NOT a grey void]
  Why: Buyers need to see how it reads in an actual environment
  Reference: "[asset type] UE5 in-scene screenshot ArtStation"

SCREENSHOT 5 — LOD comparison (if applicable):
  [Side-by-side LOD0 / LOD1 / LOD2 / LOD3]
  Reference: "LOD comparison game asset screenshot"

SCREENSHOT 6 — Scale reference:
  [Asset next to UE5 mannequin or known reference object]
  Critical: Buyers can't assess scale from the hero render alone

SCREENSHOT 7 — Variant showcase (if asset has variants):
  [All colour/damage/seasonal variants in one image]
  Reference: "[category] variant showcase Fab ArtStation"
```

### B3. Product Listing Structure

Research the product description format of top sellers before writing yours:

```
TITLE FORMULA:
  [Style] [Asset Name] - [Engine] [Key Features]
  Example: "Post-Apocalyptic Cargo Crate – UE5 | 4K PBR | 3 LODs | Collisions"
  
  Rules:
  - Lead with the style adjective buyers search for
  - Include engine name (buyers filter by engine)
  - List the 2–3 features that differentiate you from competitors
  - Keep under 80 characters (truncates in marketplace grid)

TAG STRATEGY (research-first):
  Category tags:     [e.g. "prop", "environment", "hard surface"]
  Style tags:        [e.g. "sci-fi", "post-apocalyptic", "realistic"]
  Engine tags:       [e.g. "unreal-engine-5", "unity", "blender"]
  Technique tags:    [e.g. "pbr", "4k", "game-ready", "modular"]
  [Research: what tags do the top 5 similar assets in your category use?]

DESCRIPTION SECTIONS (in order):
  1. One-sentence hook — what is this, why is it production-ready
  2. Technical specifications (poly count, texture res, LODs, maps included)
  3. What's included (exact file list: FBX / OBJ / Blend / .uasset / textures)
  4. Use case examples (types of scenes/games this fits)
  5. Engine version compatibility
  6. Support statement

PRICING RESEARCH:
  [Search 10 similar assets in your category]
  Budget tier:      $[range] — [what assets at this price typically include]
  Mid tier:         $[range] — [what assets at this price typically include]
  Premium tier:     $[range] — [what premium assets include that justify the price]
  Your price:       $[recommendation based on your feature set]
  Rationale:        [why this price vs competitors]
```

### B4. Competitor Gap Analysis

```
MARKET RESEARCH QUERIES:
  1. "[category] [style] site:fab.com" — find top 10 competitors
  2. Sort by "Most Sold" — identify what the market wants
  3. Read reviews of top sellers — what do buyers complain is missing?
  4. Read reviews of similar assets with low ratings — what went wrong?

YOUR DIFFERENTIATOR:
  [What does your asset have or do that the top sellers don't?]
  [Be specific — "better topology" is not a differentiator. "Includes 4 damage
   variants that no similar asset offers" is.]

TIMING CONSIDERATION:
  [Is this category saturated? Is there a seasonal window? Is there an upcoming
   game release that will spike search for this asset type?]
```

---

## Output

Save as `marketplace-brief_[assetname]_v1.md`.

Part A is your modeling guide. Part B is your launch checklist.
Revisit Part B before final render — the marketing research often reveals that
the hero angle or feature set needs adjustment before screenshots are taken.

This document should be the last thing you look at before hitting Publish.
