# Open Issues — v2.1.0

Known gaps and planned improvements for the next release.

---

## Priority 1 — Fix Before Wide Distribution

### Issue 1 — Install command not verified
`claude skill add p4inz-code/3d-ref-skills` listed in README but not confirmed
indexed in Claude Code skill registry.
Action: Verify after GitHub push. Update README if manual install is required.

---

## Priority 2 — Add in v2.1.1

### Issue 2 — No GitHub issue templates
Visitors who want to report problems or propose skills have no guided path.
Action: Add `.github/ISSUE_TEMPLATE/bug_report.md` and `new_skill_proposal.md`

### Issue 3 — Planning documents at root level
RESEARCH_REPORT.md, FIVE_WHYS_ANALYSIS.md, V2_STRUCTURE.md are planning artifacts
visible at root. Valuable for contributors; potentially confusing for casual visitors.
Action: Move to `docs/meta/` in v3.0

---

## Priority 3 — Add in v3.0

### Issue 4 — Missing standalone workflow guides
`docs/VFX_REFERENCE_WORKFLOW.md` and `docs/TEXTURE_REFERENCE_WORKFLOW.md` planned but
not yet written. Both are noted in CHANGELOG and roadmap.

### Issue 5 — ref-character not yet built
Character reference deep-dive is the highest-requested missing skill category.
Action: v3.0 — `ref-character` covering anatomy, facial topology, deformation zones.

### Issue 6 — Second examples not yet added
Each skill has one example. Two examples would demonstrate range.
Action: v3.0 — add one organic / character example to ref-brief.
