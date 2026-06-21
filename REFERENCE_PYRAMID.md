# The Reference Pyramid

The Reference Pyramid is the core framework of Reference Engineering.
It defines the order in which references must be gathered — and why that order matters.

```
                              ╔═══════════╗
                              ║  DELIVER  ║
                              ║ Render/   ║
                              ║ Present   ║
                             ╔╩═══════════╩╗
                             ║   DETAIL    ║
                             ║ Macro photo ║
                             ║ Fasteners   ║
                             ║ Micro-tex   ║
                            ╔╩═════════════╩╗
                            ║   MATERIAL    ║
                            ║ Per surface   ║
                            ║ Wear logic    ║
                            ║ PBR channels  ║
                           ╔╩═══════════════╩╗
                           ║     SCALE        ║
                           ║ Real dimensions  ║
                           ║ Anchor object    ║
                           ║ In-engine check  ║
                          ╔╩═════════════════╩╗
                          ║    ORTHOGRAPHIC    ║
                          ║ Front / Side / Top ║
                          ║ Blueprints / Plans ║
                          ║ Technical drawings ║
                         ╔╩═══════════════════╩╗
                         ║     SILHOUETTE       ║
                         ║  Shape language      ║
                         ║  Proportions         ║
                         ║  Primary forms       ║
                        ╔╩═════════════════════╩╗
                        ║       CONCEPT          ║
                        ║  Asset definition      ║
                        ║  Platform / Style      ║
                        ║  Production context    ║
                        ╚════════════════════════╝
```

---

## Layer 1 — Concept (Foundation)

**What it is:** The definition of the asset before any reference gathering begins.

**What you establish:**
- What is this asset?
- What is it for? (game, film, marketplace, client)
- What style? (realistic, stylized, hand-painted)
- What are the production constraints? (poly budget, texture resolution, pipeline)

**Why it's the foundation:**
Every reference you gather will be filtered through these decisions. A sci-fi weapon
reference is wrong for a medieval prop. A film-quality reference is misleading for
a mobile game. Establish the concept before gathering anything.

**If you skip this layer:**
You will gather beautiful references that are wrong for your production context,
and discover this only after modeling is complete.

---

## Layer 2 — Silhouette

**What it is:** Shape and proportion reference showing what the asset looks like at distance.

**What you gather:**
- The 2–3 primary forms that make up the silhouette
- How the asset reads as a black shape at thumbnail size
- The proportion ratio (tall vs wide, heavy vs light)
- The shape rhythm (does a form repeat at multiple scales?)

**Why it comes before orthographic:**
You must understand the overall shape before you look at the technical specifics.
Orthographic blueprints lock in proportions — those proportions must be the right ones.
Gather silhouette reference first so you know what proportions you're committing to.

**If you skip this layer:**
You will use orthographic blueprints to build technically accurate proportions
that don't match the visual direction of your project. Technically correct. Visually wrong.

---

## Layer 3 — Orthographic

**What it is:** Technical front/side/top views, blueprints, or measured drawings.

**What you gather:**
- Front elevation
- Side (left) elevation
- Top plan view
- Cross-section (for complex internal structures)
- Manufacturer specifications or measured drawings when available

**Why it comes after silhouette:**
You use silhouette reference to select the right orthographic references.
If you find blueprints first, you may commit to proportions that don't match your visual direction.
Select blueprints that match the silhouette you've already validated.

**If you skip this layer:**
Proportions that look correct in your primary working angle will be wrong from every other angle.
This error compounds through the entire build and is almost impossible to fix after detailing.

---

## Layer 4 — Scale

**What it is:** Real-world dimensional reference establishing the physical size of the asset.

**What you establish:**
- Real-world H × W × D in cm or m
- A known-size anchor object for comparison
- How to verify scale in-engine before continuing

**Why it comes before material:**
Scale determines everything: poly budget, texel density, level of detail appropriate for the asset,
and how it reads next to other objects in-scene. Material reference gathered before scale is
established may show detail at the wrong resolution for the asset's actual screen size.

**If you skip this layer:**
Your asset will look correct in isolation and wrong in-scene. Scale mismatches are
the #1 reason assets fail QA and the hardest problem to fix after production is complete.

---

## Layer 5 — Material

**What it is:** Close-up photography and reference for each distinct surface type on the asset.

**What you gather:**
- Separate reference cluster per material (concrete, metal, rubber, paint — each separately)
- The physical logic of aging and wear for each material type
- PBR value calibration reference (albedo range, roughness behavior, metallic zones)
- The rules governing where wear concentrates and how it distributes

**Why it comes after scale:**
Material reference is gathered at the resolution appropriate for the asset's texel density,
which is determined by scale. A 1m prop at 512px/m needs different macro detail reference
than a 5m prop at the same density.

**If you skip this layer:**
Surfaces that look "3D" — technically correct but unconvincing. The micro-variation,
wear logic, and PBR calibration that make surfaces read as physically real are all in this layer.

---

## Layer 6 — Detail

**What it is:** Macro-level close-up photography of the specific features that give the asset its character.

**What you gather:**
- Individual fasteners, seams, panel lines — close enough to count individual threads
- Surface micro-texture at 1:1 with the model's texel density
- The areas that will receive the most visual attention in the hero angle
- Secondary details that add reading complexity at medium distance

**Why it comes after material:**
Detail reference is the most specific reference type — it narrows to individual elements.
You cannot correctly reference details without first understanding the material those
details exist within, and the scale at which they need to read.

**If you skip this layer:**
Fasteners that are the wrong size. Panel lines that are too deep or too shallow.
Surface detail that reads as pattern-stamped rather than physically motivated.

---

## Layer 7 — Deliver

**What it is:** Reference for how the asset will be presented — render angle, lighting, marketing.

**What you gather:**
- The hero presentation angle (3/4 view, top-down, eye-level)
- Lighting reference showing the asset under the intended render setup
- Competitor presentation analysis (how do top-selling similar assets present?)
- Marketing-specific references (thumbnail composition, screenshot types)

**Why it comes last:**
Delivery reference is informed by everything below it. You cannot choose the right
hero angle without knowing what the material looks like in that light. You cannot
judge thumbnail composition without knowing what the asset looks like textured and lit.

**If you skip this layer:**
Assets that look great in viewport and poor in the thumbnail. Presentation decisions
made at the end of production that contradict the modeling and texturing decisions made throughout.

---

## The Rule of the Pyramid

**Never gather a layer before the layer below it is complete.**

Skipping layers is the root cause of most 3D production failures. It feels faster.
It isn't. Every skipped layer is a debt that is paid — with interest — at delivery.

The pyramid is not about gathering more references. It is about gathering them in
the right order. A 45-minute pyramid session is more valuable than a 4-hour random gather.

---

## How to Use This Document

1. Start at Layer 1 (Concept). Do not proceed until it is clear.
2. Run `ref-brief` (or `ref-vfx` / `ref-texture`) to generate queries for each layer.
3. Gather each layer completely before starting the next.
4. Run `ref-audit` to verify each layer before modeling.
5. Return to this diagram whenever you feel uncertain about what to gather next.

---

*Part of the Reference Engineering framework — github.com/p4inz-code/3d-ref-skills*
