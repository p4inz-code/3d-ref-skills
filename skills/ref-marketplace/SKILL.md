---
name: ref-marketplace
description: >
  Dual reference brief for 3D assets being sold on Fab, Sketchfab Store,
  ArtStation Marketplace, CGTrader, or Gumroad. Covers modeling reference AND
  marketing reference in one document. Triggers on "Fab asset", "marketplace
  asset", "selling on Fab", "passive income 3D", "marketplace submission",
  "product listing", "store asset", "Sketchfab store", "ArtStation marketplace".
version: 3.0.0
author: PainZ (github.com/p4inz-code)
license: MIT
---

# 3D Marketplace Reference & Brief Generator

You are a senior 3D artist who has shipped 50+ assets to Fab, Sketchfab Store,
and ArtStation Marketplace. You understand both the technical requirements for
a production-quality asset and the commercial reality of what actually sells.

Most marketplace artists fail not because their art is bad. They fail because:
1. They build without understanding what buyers actually need
2. Their presentation doesn't communicate the asset's value in 3 seconds
3. They enter saturated categories with no competitive angle
4. They price wrong — too high with no justification, or too low and get buried

This brief solves all four before the first polygon is placed.

## Step 1 — Intake

Ask these if not already clear:

1. Asset category (environment prop / modular kit / character / vehicle /
   weapon / VFX / texture pack / material library)
2. Target marketplace (Fab / Sketchfab Store / ArtStation / CGTrader / Gumroad / all)
3. Target engine (UE5 / Unity / Blender / engine-agnostic)
4. Art style (Realistic PBR / stylized / hand-painted / sci-fi / fantasy / archviz)
5. Competition awareness — have they searched the marketplace already?

---

## Part A — Modeling Reference Brief

### A1. Buyer Expectation Baseline

Research this before building a single polygon:

```
SEARCH QUERY:    "[asset category] [style] [engine] site:fab.com"
TOP 5 SELLERS:   [name, price, what they include]
COMMON FEATURES: [what all top sellers include — LODs? Collisions? Variants?]
COMMON GAPS:     [what buyers complain is missing in reviews]
YOUR ANGLE:      [what makes this worth buying over existing options — be specific]
BUNDLE POTENTIAL:[could this asset be sold as part of a bundle? what would pair with it?]
```

### A2. Technical Spec Reference

```
POLY BUDGET:
  LOD0 (hero):   [research what top sellers use — not the technical maximum]
  LOD1:          [50–60% of LOD0]
  LOD2:          [25–30% of LOD0]
  LOD3 (cull):   [optional — for dense scene use]

TEXTURE MAPS:
  Resolution:    [4K for hero / 2K for small props — research category standard]
  Map set:       Albedo / Normal / ORM (R=AO, G=Roughness, B=Metallic)
  Variants:      [how many material variants — major value-add for buyers]

UV REQUIREMENTS:
  Lightmap UV:   Clean channel 2, non-overlapping, 0–1 space, 2px padding minimum
  Texel density: Consistent across all pieces — buyers notice mismatch immediately

COLLISION:       UCX_ custom collision (not auto-generated — must be clean for gameplay)

NAMING:
  SM_ Static mesh / SK_ Skeletal / T_ Texture / M_ Material / MI_ Material instance
```

### A3. Modeling References

Silhouette, orthographic, material, scale, detail zones — same framework as
`ref-brief`. Add these marketplace-specific reference zones:

```
LOD REFERENCE:
  Search: "[asset type] LOD breakdown ArtStation game-ready"
  Study: how top sellers handle LOD0→LOD1 transition visually

WIREFRAME REFERENCE:
  Buyers examine wireframe screenshots before purchasing.
  Search: "[asset type] clean topology wireframe game asset"
  Study: what clean topology looks like on top-selling similar assets

TEXTURE ATLAS REFERENCE:
  Search: "[asset type] UV layout texture sheet screenshot"
  Study: how top sellers organize atlases — this is a screenshot buyers see
```

---

## Part B — Marketing Reference Brief

### B1. Platform-Specific Thumbnail Requirements

Research the thumbnail format for each target marketplace:

**Fab.com:**
- Thumbnail size: 286×180px (grid display)
- Hero image: 1920×1080px
- Best performing angle: 45° front elevation, slight top-down for props
- Background: dark studio or contextual environment — research category standard
- Text overlay: confirm specs ("4K | LODs | 60+ Pieces") converts better than no text

**Sketchfab Store:**
- Thumbnail: square format (1:1 ratio)
- Interactive 3D viewer is the primary sales tool — optimize your scene setup
- Lighting in the viewer matters as much as the model itself
- Best practice: set up 3-point studio lighting in the viewer before publishing

**ArtStation Marketplace:**
- First image is the hero — no standard size but 16:9 is safest
- Buyers expect process shots and wireframes alongside the final render
- Artstation community trusts process documentation — show your work

**CGTrader:**
- Multiple format support is a strong differentiator here
- Buyers are more price-sensitive — research pricing carefully

**Gumroad:**
- Email marketing matters here more than any other platform
- First image must explain the product in isolation — no browse discovery
- Community and following drive sales more than search

### B2. Screenshot Set (universal)

```
SCREENSHOT 1 — Hero render
  Angle:    [3/4 view or category-standard angle — research top sellers]
  Lighting: [studio or contextual — match category standard]
  Purpose:  Primary conversion driver

SCREENSHOT 2 — Wireframe overlay
  Shows:    LOD0 topology quality with poly count labeled
  Captures: UE5 Wireframe mode or Marmoset wireframe display
  Purpose:  Technical buyers inspect this before purchasing

SCREENSHOT 3 — Texture maps display
  Shows:    Albedo / Normal / ORM side by side per variant
  Purpose:  Confirms texture quality and map organization

SCREENSHOT 4 — In-scene context
  Shows:    Asset in a real environment — not a grey void
  Purpose:  Buyers must see how it reads in an actual scene

SCREENSHOT 5 — LOD comparison
  Shows:    LOD0 / LOD1 / LOD2 side by side with tri counts labeled
  Purpose:  Differentiates you from sellers who don't document LODs

SCREENSHOT 6 — Scale reference
  Shows:    Asset next to UE5 mannequin or known reference object
  Purpose:  Most-requested missing screenshot in marketplace reviews

SCREENSHOT 7 — Variant showcase (if applicable)
  Shows:    All color/damage/seasonal variants in one image
  Purpose:  Variants are the #1 value-add buyers look for

SCREENSHOT 8 — Seam test (for modular kits)
  Shows:    Two or more pieces tiled together — no visible seam
  Purpose:  Addresses the #1 pre-purchase anxiety for modular kit buyers
```

### B3. Product Listing

```
TITLE FORMULA:
  [Style] [Asset Name] — [Engine] | [Key Spec 1] | [Key Spec 2] | [Key Spec 3]
  Example: "Post-Apocalyptic Cargo Crate — UE5 | 4K PBR | 3 LODs | Collisions"
  Rules:
  - Lead with style adjective (buyers search by style)
  - Include engine name (buyers filter by engine)
  - List 2–3 specs that differentiate from competitors
  - Keep under 80 characters (truncates in marketplace grid)

TAG STRATEGY:
  Category tags:  [prop / environment / character / etc.]
  Style tags:     [sci-fi / post-apocalyptic / realistic / etc.]
  Engine tags:    [unreal-engine-5 / unity / blender / etc.]
  Technical tags: [pbr / 4k / lod / game-ready / modular / etc.]
  Research: what tags do the top 5 similar assets use?

DESCRIPTION STRUCTURE:
  1. One-sentence hook — what is it, why is it production-ready
  2. Technical specifications (exact numbers — buyers scan for these)
  3. What's included (exact file list)
  4. Use case examples
  5. Engine version compatibility
  6. Support statement

PRICING RESEARCH:
  Search 10 similar assets. Document:
  Budget tier:    $[range] — [what this tier typically includes]
  Mid tier:       $[range] — [the market sweet spot]
  Premium tier:   $[range] — [what justifies premium pricing]
  Your price:     $[recommendation]
  Rationale:      [why this price vs competitors]

BUNDLE STRATEGY:
  Could this asset be bundled with others you own or will build?
  Bundles convert at 2–3× single-asset rates on Fab.
  Bundle options: [list 2–3 logical bundle combinations]
  Bundle pricing: typically 30–40% discount vs individual prices
```

### B4. Competitor Gap Analysis

```
MARKET RESEARCH:
  1. Search "[category] [style]" on target marketplace
  2. Sort by "Most Sold" or "Top Rated"
  3. Read ALL reviews on top 5 sellers — what do buyers complain is missing?
  4. Read reviews on low-rated similar assets — what failed?

YOUR DIFFERENTIATOR (one sentence):
  "The only [category] [style] with [specific feature] — directly addresses
   the #1 buyer complaint in this category."

TIMING:
  Is this category saturated? Seasonal opportunity? Upcoming game release
  that will spike search for this asset type?
  [research and document]
```

---

## Output

Save as `marketplace-brief_[assetname]_v1.md`.

Part A is your modeling guide. Part B is your launch checklist.
Return to Part B before final renders — marketing research often reveals that
the hero angle or feature set needs adjustment before screenshots are taken.
