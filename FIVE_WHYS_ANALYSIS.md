# FIVE WHYS ANALYSIS — 3d-ref-skills v2 Additions
Conducted: 2026-06-20

Every proposed addition is tested here. If the root value is weak, the addition is rejected.

---

## ADDITION 1 — `ref-vfx` skill

**Why does this exist?**
VFX artists need reference before building simulations in Niagara, Houdini, or any particle system.

**Why do they need reference before building simulations?**
Because VFX without reference produces simulations that look generic — fire that doesn't behave like real fire, smoke that doesn't move with the physical logic of the scene, explosions with the wrong timing and scale.

**Why does generic VFX happen even when artists are technically skilled?**
Because VFX artists typically gather reference informally — a YouTube video here, a screenshot there — without a structured framework for capturing motion phase, density, color temperature, emission behavior, and scale across multiple real-world sources simultaneously.

**Why does the lack of structure matter?**
Because a simulation has 6–12 parameters that all interact. Without structured reference per parameter, the artist iterates blindly — adjusting one value, watching the sim, adjusting another — rather than knowing what target they are tuning toward.

**Why is this a gap nobody else has filled?**
Because AI tooling for VFX is focused on code generation (writing Houdini VOPs, Niagara scripts) — not on the pre-production reference layer that determines whether the code produces something that looks right.

**Root value:** Eliminates blind iteration in VFX production by giving artists a structured reference framework before they open their simulation tool.

**Verdict: ACCEPT** — Root value is production-critical and completely unaddressed in the ecosystem.

---

## ADDITION 2 — `ref-texture` skill

**Why does this exist?**
Texture artists need reference before painting or generating textures in Substance Designer, Painter, or any texturing tool.

**Why do they need reference before texturing?**
Because texture work without reference produces surfaces that are either too uniform (no micro-variation), incorrectly worn (damage that doesn't follow physical logic), or tonally wrong for the intended lighting environment.

**Why is this different from the material reference in `ref-brief`?**
`ref-brief` covers material reference as part of a modeling brief — it tells the modeler what surfaces exist. `ref-texture` goes deeper into the texturing-specific layer: tiling pattern research, Substance graph reference, trim sheet layout reference, and PBR value range calibration. These are distinct needs that a modeler doesn't have.

**Why can't texture artists use `ref-brief` directly?**
Because `ref-brief` is asset-scoped — it generates a brief for one specific asset. `ref-texture` is surface-scoped — it generates a brief for one specific material that may appear across many assets. The research methodology is different.

**Why does this matter for the Fab marketplace use case specifically?**
Because texture packs and material libraries are a major Fab category. Artists selling textures need to research: what surface types are undersupplied on Fab, what tiling resolution buyers expect, what PBR map sets are standard, and what preview renders convert. None of this is covered by existing skills.

**Root value:** Fills the texturing pre-production gap between the modeling reference layer (`ref-brief`) and the final surface result — with specific coverage for the Fab texture marketplace.

**Verdict: ACCEPT** — Distinct from existing skills. Serves texture artists as a primary audience rather than as a secondary user of modeling skills.

---

## ADDITION 3 — `REFERENCE_ENGINEERING.md`

**Why does this exist?**
To define Reference Engineering as a discipline with its own terminology, principles, and methodology.

**Why does a discipline definition matter for a GitHub repo?**
Because repositories without a conceptual framework are tool collections. Tool collections get used once and forgotten. A discipline gives users a mental model that makes every tool feel like part of a larger system — increasing retention, return visits, and contribution.

**Why does Reference Engineering specifically need to be named and defined?**
Because the practice of systematic pre-production reference gathering exists in every professional studio but has never been codified as a named discipline. Naming it creates a shared vocabulary that the community can adopt — "I'm doing my ref engineering before I start modeling" is a phrase that doesn't exist yet.

**Why would naming a practice matter?**
Because named practices become searchable. When a 3D Discord server member says "reference engineering" and links this repo, it creates a discovery path that "reference gathering tips" does not.

**Why is this the right repo to define this term?**
Because it's the first repo systematically organized around this specific layer of 3D production. First-mover advantage in terminology is real in open source communities.

**Root value:** Transforms this repo from a tool collection into the canonical source for a named professional practice — driving long-term retention, citation, and community adoption.

**Verdict: ACCEPT** — Root value is strategic and compounds over time.

---

## ADDITION 4 — `REFERENCE_PYRAMID.md`

**Why does this exist?**
To visualize the hierarchy of reference types from foundational (silhouette) to surface-level (micro-detail).

**Why does a hierarchy matter?**
Because artists who gather references in the wrong order — collecting micro-detail before establishing silhouette and proportion — waste time on detail that gets discarded when the form changes.

**Why do artists gather in the wrong order?**
Because the order is never explicitly taught. Junior artists learn reference gathering by imitation — they do what they see senior artists do from the outside, without understanding why certain references come first.

**Why does a visual pyramid help more than a written explanation?**
Because the hierarchy needs to be seen at a glance to be remembered. A pyramid diagram communicates priority, dependency, and sequence in a single image. Written lists do not.

**Why would someone share this specific document?**
Because it answers a question that comes up in every 3D forum and Discord: "how do I know when I have enough references?" The pyramid gives a framework for that answer.

**Root value:** Provides the visual mental model that makes every other skill in the pack make sense — and creates the most shareable single document in the repository.

**Verdict: ACCEPT** — Root value is foundational to the entire system.

---

## ADDITION 5 — `REFERENCE_CHECKLIST.md`

**Why does this exist?**
To provide a single-page, print-ready reference checklist that works without the AI skills.

**Why does a no-AI version matter?**
Because not every artist uses Claude Code or any AI agent. A checklist that works standalone means the repo is useful to the entire 3D community, not just AI tooling users. This doubles the potential audience.

**Why would a professional use a checklist when they have the AI skills?**
Because in a production environment, running an AI skill for every asset is not always practical. A checklist that can be printed and pinned above a monitor, or saved as a PDF, provides value between AI sessions.

**Why would this file drive stars more than other additions?**
Because checklists are the most-shared format on Reddit, Discord, and forums. A well-designed checklist with a "from github.com/p4inz-code/3d-ref-skills" attribution line at the bottom creates passive ongoing discovery.

**Why is this better than the existing checklist inside `ref-brief`?**
Because the `ref-brief` checklist is asset-specific — it's filled out per model. `REFERENCE_CHECKLIST.md` is a master framework that applies to any asset type and any production context. It's the difference between a filled form and the blank form that generates it.

**Root value:** Standalone utility that doubles the repo's audience and creates a highly shareable artifact that drives passive discovery.

**Verdict: ACCEPT** — Root value is high and implementation is low-cost.

---

## ADDITION 6 — `REFERENCE_MISTAKES.md`

**Why does this exist?**
To document the most common reference gathering mistakes, their symptoms, and their consequences.

**Why document mistakes specifically?**
Because people search for solutions to problems they already have. "Why does my model look wrong" and "why does my texture look fake" are queries that a mistakes document answers directly. Skills documents answer "how to do it right" — mistakes documents answer "why did it go wrong."

**Why would this drive more traffic than a guide on doing it correctly?**
Because problem-first content converts better. A user who already has a broken model and is searching for why is more motivated than a user in pre-production who is following best practices. Both are served by this repo, but only one is actively searching.

**Why are reference mistakes specifically worth documenting over other 3D mistakes?**
Because reference mistakes are the root cause of most visible 3D quality problems but are almost never identified as such. Artists blame their modeling technique, their texturing, their lighting — almost never their reference. This document reframes the diagnosis.

**Why hasn't this been documented before?**
Because the industry teaches reference gathering as a soft skill passed through observation, not as a documented discipline with named failure modes. This is the gap.

**Root value:** Problem-first content that reframes the most common quality issues in 3D production as reference failures — the most shareable document in the repository for communities actively discussing "why does my work look bad."

**Verdict: ACCEPT** — Root value is unique and highly shareable.

---

## ADDITION 7 — `KANVAZ_WORKFLOW.md`

**Why does this exist?**
To show step by step how Kanvaz and 3d-ref-skills work together as a complete pre-production reference system.

**Why does a step-by-step integration guide matter?**
Because the connection between "AI generates your brief" and "you build your board in Kanvaz" is currently implied in one sentence in the README. An implied connection doesn't create behavior. A step-by-step workflow creates behavior.

**Why does creating this behavior matter for the repo?**
Because a user who completes the full workflow (runs ref-brief, opens Kanvaz, builds a structured board, runs ref-audit) is a user who understands the system — and users who understand the system become contributors, advocates, and repeat visitors.

**Why does this specifically benefit Kanvaz?**
Because Kanvaz's current README explains what it is but not how to use it in a professional workflow. This document provides the professional context that elevates Kanvaz from "infinite canvas app" to "the reference board tool for 3D artists."

**Why build this here rather than in the Kanvaz repo?**
Because this repo has the 3D production context. The workflow document lives here and links to Kanvaz — creating an inbound link from a repo with 3D topics to Kanvaz, which improves Kanvaz's GitHub topic discoverability.

**Root value:** Creates the behavioral loop that turns one-time users into system users — while providing cross-repo SEO and discovery benefits for Kanvaz.

**Verdict: ACCEPT** — Root value is ecosystem-building and practical simultaneously.

---

## ADDITION 8 — `REFERENCE_SYSTEM.md`

**Why does this exist?**
To explain how the 5 skills connect as a system, what order to use them in, and what each skill produces that the next skill consumes.

**Why does the connection between skills need to be documented?**
Because a visitor who installs all 5 skills and uses them independently is missing the compounding value of using them in sequence. ref-brief produces a document that ref-audit validates. ref-style-decode informs the brief. The system is more powerful than the sum of its parts.

**Why isn't this already obvious from the README?**
Because the README presents the skills as a table — parallel options, not a sequence. The table format implies "choose one" rather than "use in order."

**Why does explaining the system increase stars specifically?**
Because repositories with a clear system — not just tools — get cited in articles, tutorials, and course materials. "I use the 3d-ref-skills system" is a phrase that creates ongoing citation. "I use some of the 3d-ref-skills" does not.

**Why build this as a separate document rather than adding to the README?**
Because the README must remain scannable. A full system explanation in the README creates a wall of text that reduces conversion. A separate document keeps the README clean while giving depth-seekers a destination.

**Root value:** Transforms isolated tool usage into system usage — the difference between a tool people try once and a workflow people adopt permanently.

**Verdict: ACCEPT** — Root value is retention and citation.

---

## REJECTED ADDITIONS

### `ref-character` skill

**Root value test:**
Why 1: Character artists need reference before modeling.
Why 2: Character modeling has unique requirements (facial topology, deformation, anatomy).
Why 3: These requirements are not fully covered by `ref-brief`.
Why 4: But `ref-audit` already has a complete Character section with C1–C3 checks.
Why 5: The gap between `ref-brief` + `ref-audit` for characters is smaller than for VFX or textures.

**Root value:** Adding a character-specific brief skill would largely duplicate the character sections already in `ref-brief` (organic asset type) and `ref-audit` (C1–C3 checks).

**Verdict: REJECT for v2.1** — Address by adding a character example to `ref-brief` instead. Revisit as `ref-character` in v3.0 only if community feedback identifies gaps the existing skills don't cover.

### Second examples for all skills

**Root value test:**
Why: Range of examples demonstrates skill versatility.
Why: A single example might suggest the skill only works for that asset type.
Why: But examples are the most time-intensive content to produce correctly.
Why: And the existing examples already demonstrate the skills work across prop/character/environment/marketplace/freelance.
Why: Adding thin examples to hit a quantity target would lower quality.

**Root value:** Second examples add marginal value versus the cost of producing them correctly.

**Verdict: REJECT for v2.1** — Add second examples only when the community requests them for specific asset types not covered. Quality over quantity.
