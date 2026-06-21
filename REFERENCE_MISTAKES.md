# Reference Mistakes

The most common quality problems in 3D production are reference problems.
Not modeling problems. Not texturing problems. Reference problems.

This document names the failure modes, their symptoms, and their fixes.
Use it when your work looks wrong and you can't identify why.

---

## MISTAKE 1 — Modeling From a Single Perspective Reference

**What happens:**
The artist finds one good 3/4 view photo of the asset and models from it.

**Symptom:**
The model looks correct from the front-left angle and wrong from every other angle.
Proportions that seem right in the working view reveal themselves as distorted
at delivery when the asset is rotated.

**Why it happens:**
A perspective photo embeds the camera's lens distortion and viewing angle into
the artist's mental model of the object. They are not modeling the object —
they are modeling the photo.

**The fix:**
Orthographic views (front / side / top) before modeling begins. If no blueprint
exists, find at least three photographs of the object from three different angles
and use them simultaneously. Never model from a single image.

**This mistake costs:** Full rework of proportions at delivery.

---

## MISTAKE 2 — The Mood Board Instead of a Reference Board

**What happens:**
The artist collects images of things that "feel right" — atmospheric shots,
color-matched photos, vibe-establishing images. The board looks great.
It provides almost no production value.

**Symptom:**
The artist opens the DCC and immediately gets stuck. The board is full of
images but none of them show what the model should look like from the front,
what the material looks like up close, or what the correct proportions are.

**Why it happens:**
Mood gathering is enjoyable and feels productive. It produces a board that
looks organized. It does not produce a board that supports modeling decisions.

**The fix:**
Separate mood reference (for atmosphere, color direction, emotional register)
from production reference (for shape, proportion, material, detail). Both
are valid. They are not the same. A production board needs close-up photographs
of real surfaces, measured drawings, and scale anchors — not aesthetic photography.

**This mistake costs:** Hours of modeling without direction, followed by rework
when the mood board can't answer the question "what does the edge bevel look like."

---

## MISTAKE 3 — No Scale Anchor

**What happens:**
The artist models the asset at a size that "looks right" in the viewport
without establishing real-world dimensions or verifying scale in-engine.

**Symptom:**
The asset looks correct in isolation. When placed next to a character or
environment piece in-engine, it reads as the wrong size — often too small.
The asset is delivered and fails QA for scale.

**Why it happens:**
Viewport modeling is scale-agnostic. The viewport shows you what you're making,
not how large it is. Without a reference object at known size, every size
decision is made by eye — and the eye has no absolute scale reference.

**The fix:**
Document real-world dimensions (H × W × D in cm or m) before modeling.
Place a 1.75m reference cube or UE5 mannequin in the scene before the first
polygon. Check scale in-engine before detailing begins.

**This mistake costs:** Scale rework after delivery, or worse — an asset that
ships at the wrong size and breaks scene composition.

---

## MISTAKE 4 — One Reference For All Surfaces

**What happens:**
The artist finds a single overview photo of the entire asset and uses it
as reference for all surface materials.

**Symptom:**
Surfaces that read correctly at distance but lose all material conviction
at close range. The concrete looks like grey plastic. The metal looks like
painted wood. The fabric looks like rubber. No surface reads as what it is.

**Why it happens:**
An overview photo shows the object. It does not show the material. A photo
of a crate from 3 meters away shows the shape of the crate — but not the
grain direction of the wood, the oxidation pattern at the nail heads,
or the fiber texture of the rope handles.

**The fix:**
One reference cluster per material. Not one cluster for the whole asset —
one cluster for each distinct surface type. Concrete gets concrete macro photos.
Metal gets metal macro photos. Every surface type, separately.

**This mistake costs:** Textures that pass at first review and read as fake
in final delivery. Re-texturing entire surfaces.

---

## MISTAKE 5 — Random Imperfection

**What happens:**
The artist adds wear, damage, and dirt to the surface without reference
for how those imperfections actually form and distribute on this material.

**Symptom:**
Scratches that run in random directions. Rust that appears uniformly across
the surface. Dirt that doesn't follow gravity. Cracks that go wherever the
artist's brush went. The surface looks "worn" but not physically convincing.

**Why it happens:**
Artists know that real surfaces have imperfections. Without reference showing
the specific logic of how those imperfections form on this specific material,
they approximate — and the approximation is always random.

Real imperfection is never random. It follows physical law:
- Rust forms where metal meets moisture
- Scratches run with grain direction on brushed surfaces
- Dirt accumulates where geometry creates shelter from rain
- Paint cracks at stress points and peels at edges, not in the middle of a panel
- Moss grows where there is shade and moisture, not on south-facing dry surfaces
- Water staining runs strictly downward from every horizontal surface

**The fix:**
Gather imperfection reference specific to this material type and this wear
condition. Study where imperfections concentrate — not just what they look like.
Understand the physical logic before applying anything.

**This mistake costs:** Surfaces that fail believability at close range.
The brain recognizes physically incorrect imperfection before the artist can
consciously identify what is wrong.

---

## MISTAKE 6 — Copying Instead of Understanding

**What happens:**
The artist uses a reference to copy the visual result — matching colors, shapes,
and details from the reference directly — rather than understanding the principles
that make the reference work.

**Symptom:**
The asset looks like a copy of the reference at the matching angle and reveals
its lack of understanding from any other angle. When the reference is a competitor
or copyrighted asset, this creates legal exposure.

**Why it happens:**
Copying is faster than understanding. The result of copying looks correct
immediately. The understanding-based result takes longer to get right but
produces something original.

**The fix:**
Before gathering any reference, ask: "What am I trying to understand from this?"
Use `ref-style-decode` to break the reference into transferable principles —
shape language, surface quality, detail density, color architecture — and apply
those principles to your own original design. The result will be better than
a copy because you understand why it works.

**This mistake costs:** Assets that look derivative, or worse — assets that
are legally problematic copies of existing IP.

---

## MISTAKE 7 — Gathering References After Modeling Begins

**What happens:**
The artist starts modeling immediately and gathers reference "as needed"
when they get stuck.

**Symptom:**
Constant interruption of the modeling flow to search for references.
Discoveries mid-model that require reworking already-completed sections.
The model grows in one direction while reference suggests a different direction.

**Why it happens:**
Starting feels productive. Gathering feels like preparation. Artists who are
eager to build find pre-production reference gathering feels like delay.

**The fix:**
Pre-production reference engineering is not delay. It is acceleration.
30 minutes of structured reference gathering before opening the DCC prevents
3 hours of mid-model searching, rework, and uncertainty.

Run `ref-brief` before the first polygon. Run `ref-audit` before opening the DCC.
Every minute spent in pre-production reference saves 5 minutes in production.

**This mistake costs:** Fragmented modeling sessions, mid-production rework,
and assets that accumulate reference-driven inconsistencies throughout the build.

---

## MISTAKE 8 — No Lighting Reference

**What happens:**
The artist models and textures the asset without reference for the specific
lighting environment it will live in at delivery.

**Symptom:**
The asset looks correct in the modeling viewport or in a studio light setup,
and reads differently — sometimes dramatically so — in the destination engine
with its actual HDRI, Lumen setup, or cinematic lighting.

Surface roughness that produces a beautiful specular in three-point lighting
becomes a matte mudflat under overcast sky HDRI. A high-contrast asset that
reads powerfully in studio lighting disappears into noise under golden hour.

**Why it happens:**
Modeling and texturing tools show assets under generic lighting. Artists
optimize for what they see, which is the tool's default light — not the
destination environment's actual light.

**The fix:**
Gather lighting reference specific to the destination environment before
texturing begins. Import the target HDRI into Marmoset or the destination
engine early. Make a roughness test sphere visible in the working environment
and calibrate surface values against actual destination lighting, not default.

**This mistake costs:** Texture rework after final lighting is established.
In production pipelines, this is expensive — lighting artists don't want to
adjust their rigs for incorrectly calibrated assets.

---

## MISTAKE 9 — Wrong Scale of Detail

**What happens:**
The artist gathers close-up macro reference but references it at the wrong
scale relative to the asset's actual texel density.

**Symptom:**
Panel lines that are too wide. Rivets that are too large. Surface grain that
tiles obviously. Thread counts on fabric that look like rope rather than cloth.
Every detail is wrong by the same factor — because the reference was the right
detail at the wrong scale.

**Why it happens:**
A close-up photo of a rivet looks like a certain size on screen. Without
knowing the real-world size of the rivet in the photo, the artist scales
their modeled rivet to match the photo — but the photo might be showing
a 3mm rivet at 20× magnification.

**The fix:**
For every piece of macro detail reference, identify the real-world scale of
what you're looking at. A 3mm rivet at 512px/m texel density should be
approximately 1.5px on a 1K texture. Know the math before modeling the detail.

**This mistake costs:** Detail that reads at the wrong scale, requiring either
scale correction (fast) or re-texturing (slow) depending on whether it's
geometry or baked detail.

---

## MISTAKE 10 — VFX Without Motion Reference

**What happens:**
The VFX artist builds a fire, explosion, or smoke simulation based on what
they think it should look like — adjusting parameters until it "looks good"
in the viewport — without reference for how the real-world effect actually moves.

**Symptom:**
Fire that doesn't rise. Smoke that dissipates too fast. Explosions that expand
too slowly and fade too quickly. Effects that are visually interesting but
physically unconvincing. The brain recognizes wrong motion before the artist
identifies what specifically is wrong.

**Why it happens:**
VFX parameters are abstract (turbulence intensity, drag coefficient, lifetime).
Without motion reference showing the target behavior, every parameter becomes
a guess. Artists iterate by aesthetic preference rather than physical target.

**The fix:**
Real-world motion reference per phase (onset / peak / dissipation) before
opening any simulation tool. High-speed camera footage, slow-motion video,
and real-world photography. Know what the effect does in reality at the target
scale before setting a single simulation parameter.

**This mistake costs:** Endless parameter iteration with no physical target.
VFX that ships and is described by players as "not feeling right" — feedback
that is correct and unactionable without a reference-grounded rebuild.

---

## THE ROOT CAUSE

Every mistake above has the same root cause:

**Production began before understanding was established.**

Reference engineering is not about having more images.
It is about building understanding before building geometry.

Understanding cannot be rushed. It requires the right reference, gathered in
the right order, studied long enough to internalize.

When understanding precedes production, every decision feels obvious.
When production precedes understanding, every decision feels uncertain.

---

*Reference Mistakes v2.1.0*
*github.com/p4inz-code/3d-ref-skills — MIT License*
