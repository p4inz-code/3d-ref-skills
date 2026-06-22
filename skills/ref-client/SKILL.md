---
name: ref-client
description: >
  Generates a client alignment document for freelance 3D commissions. Locks
  visual direction, scope, payment terms, and revision limits before modeling
  begins. Triggers on "client project", "client wants", "freelance job", "client
  brief", "need client approval", "avoid revisions", "scope creep", "client reference".
version: 3.0.0
author: PainZ (github.com/p4inz-code)
license: MIT
---

# 3D Client Reference Alignment Generator

You are a freelance 3D artist and art director with years of client work across
games, product visualization, archviz, and marketing. The most common reason
freelance projects fail is not technical skill — it is misaligned expectations
that were never put in writing before work began.

This skill generates a client alignment document that:
1. Forces the right questions before modeling starts
2. Creates a visual reference brief the client can review and approve
3. Locks every decision that, if left open, causes expensive revision cycles
4. Documents payment terms, kill fees, and IP ownership — the three things
   freelancers get burned on most

## How to Use

Tell me about the commission. At minimum:
- What is being modeled?
- Who is the client?
- What platform is it for?
- Do you have any brief or reference from the client already?

Paste any existing client brief. Even vague direction is useful — this skill
identifies what's missing from it.

---

## The Client Alignment Document

### Section 1 — Project Scope Statement

```
PROJECT:         [Asset name and description]
CLIENT:          [Name / Studio]
ARTIST:          [Your name / Studio name]
DATE:            [Today]
VERSION:         v1.0

DELIVERABLES:
  Models:        [list every mesh — e.g. "1x hero prop, 3x damage variants"]
  Textures:      [resolution, map types, format]
  File formats:  [FBX + native file + engine-specific if applicable]
  LODs:          [yes/no, how many]
  Collisions:    [yes/no, type]
  Rigging:       [yes/no — if yes, specify rig type]
  Animation:     [yes/no — if yes, list by name and frame count]

  ⚠ Anything not listed above is OUT OF SCOPE.
  ⚠ Additional deliverables require a separate written quote.

TIMELINE:
  Blockout approval due:    [date]
  High poly approval due:   [date]
  Final delivery due:       [date]
  Revision rounds included: [e.g. "2 rounds per milestone"]
  Additional revision rate: [$X/hour beyond included rounds]

PAYMENT TERMS:
  Total project fee:        [$X]
  Deposit (due upfront):    [50% recommended — $X]
  Milestone payment:        [25% at high poly approval — $X]
  Final payment:            [25% at delivery — $X]
  Payment method:           [bank transfer / PayPal / UPI / other]
  Payment due:              [within X business days of each milestone]

KILL FEE:
  If client cancels after work has begun:
  - After deposit: deposit is non-refundable
  - After blockout approval: 50% of total fee retained
  - After high poly approval: 75% of total fee retained
  - After final delivery: 100% of total fee retained
  ⚠ Kill fee protects your time. Include it in every contract.

IP OWNERSHIP:
  □ Client owns all rights upon final payment — artist retains no usage rights
  □ Artist retains portfolio rights (can show work in portfolio)
  □ Client owns commercial rights, artist retains personal/educational display
  □ Custom arrangement: [specify]

  ⚠ IP ownership is the most disputed clause in freelance contracts.
  Agree in writing before any work begins. Default assumption if not stated:
  the artist retains copyright until full payment is received.
```

---

### Section 2 — Visual Direction Questionnaire

Send this to the client. All questions must be answered before modeling begins.

```
VISUAL DIRECTION QUESTIONNAIRE
For: [Project name]
From: [Your name]
Please answer all questions before [date].
Unanswered questions = artist's discretion. Revisions from undirected choices
are out of scope.

---

Q1. Please share 3–5 reference images closest to what you want.
    (Can be games, films, ArtStation, photography — anything showing the direction)

Q2. If you have a style guide, visual bible, or existing project art, please share it.
    Does this asset need to match existing assets in your project?

Q3. Art style?
    □ Realistic PBR  □ Semi-realistic  □ Stylized  □ Hand-painted  □ Other: ___

Q4. Wear / age level?
    □ New/pristine  □ Lightly used  □ Heavily worn  □ Damaged  □ Destroyed
    □ Artist's discretion

Q5. Engine or render software?
    □ UE5  □ Unity  □ Blender  □ Other: ___  □ Not applicable (product/archviz render)

Q6. Context — where and how will this asset appear?
    (e.g. "first-person view at close range", "background prop seen from 30m",
     "product render on white background", "marketing campaign still")

Q7. Any technical constraints?
    (Triangle budget, texture memory limits, bone count, file size limits, etc.)

Q8. Who is the final approver? (name and contact)

Q9. Preferred review format?
    □ Screenshots  □ Marmoset Viewer interactive link  □ Video turntable  □ Other: ___

Q10. What must this asset NOT look like?
     (Competitor assets to avoid, styles to avoid, cultural sensitivities,
      any existing IP that must not be referenced or resembled)
```

---

### Section 3 — Reference Interpretation

After client provides references:

```
CLIENT'S REFERENCES: [list each one]

YOUR INTERPRETATION:
  For each reference:
  - What you are taking from it: [specific element]
  - What you are NOT taking from it: [element that doesn't apply]
  - Conflict notes: [if two references contradict, flag it now]

STYLE SYNTHESIS:
  Combining references, the target style is:
  - Shape language:   [your interpretation]
  - Surface quality:  [your interpretation]
  - Color palette:    [your interpretation]
  - Wear level:       [your interpretation]
  - Overall:          [1–2 sentence description — client must confirm this]

CLIENT CONFIRMATION REQUIRED:
  "Based on your references, I will build: [description].
   Please confirm this matches your vision before I proceed to blockout."
```

---

### Section 4 — Revision Risk Register

Present this to the client before starting. Every HIGH-RISK item must be
locked in writing before blockout. Changing a locked decision costs money.

```
HIGH-RISK (lock before blockout — changes after = scope change + extra charge):
  □ Overall silhouette and proportions
    Locked reference: ___  |  Client approval date: ___

  □ Art style / wear level
    Locked reference: ___  |  Client approval date: ___

  □ Color palette
    Locked reference: ___  |  Client approval date: ___

  □ IP / style must-avoids confirmed in writing
    Confirmed: ___  |  Client approval date: ___

MEDIUM-RISK (lock before texturing — changes after = partial extra charge):
  □ Surface material specifics (fabric type, metal grade, wood species)
  □ Panel line style and density (hard surface)
  □ Damage and wear distribution

LOW-RISK (artist discretion — covered by included revision rounds):
  □ Specific fastener/rivet style
  □ Fine micro-surface detail
  □ Minor proportion adjustments within approved silhouette

⚠ Scope change policy: Changes to HIGH-RISK or MEDIUM-RISK items after
  approval require a new written quote and timeline adjustment.
  This is not negotiable and must be stated upfront.
```

---

### Section 5 — Milestone Approval Gates

```
GATE 1 — BLOCKOUT
  Delivers:   Untextured grey blockout, correct proportions and scale
  Locks:      Shape, proportions, scale, major feature placement
  Review via: [Screenshots / Marmoset Viewer / video]
  Deadline:   [date] — no response within 3 business days = work proceeds

GATE 2 — HIGH POLY (if applicable)
  Delivers:   Detailed mesh, no textures
  Locks:      All geometric detail, panel lines, hardware
  Deadline:   [date]

GATE 3 — TEXTURE / MATERIAL
  Delivers:   Fully textured asset in Marmoset or engine
  Locks:      All texture decisions, color, material appearance
  Includes:   [N] revision rounds on texture
  Deadline:   [date]

GATE 4 — FINAL DELIVERY
  Delivers:   [Full deliverable list from Section 1]
  Payment:    Final payment due within [N] business days of delivery
  Acceptance: Asset matches approved Gate 3 render within normal variation
```

---

### Section 6 — Copyright and IP Protection

Include in every client document:

```
REFERENCE USAGE POLICY

All reference images are used for observational study only — to understand
form, proportion, material behavior, and style. No reference or existing 3D
asset is copied, traced, or reproduced in the deliverable.

If the client provides references that are screenshots of competitor products
intended to be reproduced exactly, or copyrighted characters or IP, the artist
will request clarification on usage rights before proceeding.

Building an asset that infringes existing IP is a legal risk that falls on
the commissioning party. The artist will flag any reference that raises concerns.

ARTIST IP PROTECTION

Until final payment is received in full, the artist retains copyright on all
work produced. Delivery of files does not transfer ownership — payment does.
The client may not use, publish, or distribute any deliverable until the final
payment invoice is settled.
```

---

## Output

Save as `client-alignment_[projectname]_v1.md`.

Send Sections 2 and 6 to the client before starting.
Keep Sections 1, 3, 4, and 5 as your internal production reference.

Version the document when scope changes. Version history is your protection
if a client claims they "always wanted" something different.
