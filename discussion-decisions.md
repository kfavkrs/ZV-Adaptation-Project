# Discussion Decisions — Adaptation Blueprint

**Date:** 2026-05-27
**Status:** All layers confirmed, pending roadmap approval and GSD artifact writes

---

## Who This Is For

- A couple in their late 40s (man and woman), relocating from the US to Utrecht, Netherlands
- Two small dogs
- No children — schooling/childcare domains excluded
- Key domains: partner dynamics, social network building as a couple, pet logistics, career/purpose

---

## Scope (Layer 1 — Confirmed)

### Included
- Universal cross-cultural adaptation research (psychology/anthropology) as structural foundation
- Netherlands-specific cultural research layered on top — Dutch social norms, integration systems, US-to-NL cultural delta
- Source hierarchy: peer-reviewed academic research as the floor, experiential/practitioner sources layered on — each tagged with type and credibility level
- Life domains scoped to couple profile: social/community, linguistic, emotional/psychological, professional/purpose, financial, healthcare, housing, legal/civic, pet logistics, daily life/practical
- Temporal adaptation arc — documented psychological stages with approximate timelines, woven into each domain
- Pre-move phase kept light — teaser/primer, not heavy workload

### Excluded (for now)
- The actual bingo game / gamification design — future milestone
- Children/schooling domains
- Software or app development — this is a document

### Deferred
- Utrecht-specific local resource mapping (cafes, meetup groups, vet clinics) — belongs in gamification phase
- Deep professional/purpose domain treatment — included but lighter, expanded later

### Boundary
The deliverable is a structured research document answering: "What do we need to know, how do we know it, where did it come from, and when in the adaptation timeline does it matter?"

---

## Architecture (Layer 2 — Confirmed)

### Framework: Composite Model
- **Primary structure:** Black, Mendenhall & Oddou's Expatriate Adjustment dimensions (self-oriented / others-oriented / perceptual)
- **Woven within:** Ward's ABC Model (Affect / Behavior / Cognition) to distinguish feeling vs. doing vs. thinking
- **Meta-narrative:** Kim's Stress-Adaptation-Growth Dynamic — adaptation spirals, doesn't proceed linearly
- **Temporal overlay:** Oberg's U-Curve / W-Curve — psychological stages with approximate month markers
- **Omitted:** Berry's Acculturation Framework — integration strategy already understood

See `framework-survey.md` for detailed evaluation of all five frameworks.

### US-NL Delta Placement
- **Embedded in narrative** per domain (not separated into "What's Different" subsections)
- Rationale: reads more naturally; trade-off is harder to scan, but better for the narrative document style

### Source Tagging Format
- Every claim tagged: `[Academic]`, `[Government]`, or `[Experiential]`
- Clickable reference links at the bottom of each section
- Where sources conflict, both presented — reader decides what to weight

### Document Structure
- Organized by life domains, with framework dimensions woven in
- Each domain section includes: academic grounding, experiential insight, US-NL contrast embedded in narrative, timeline markers for when that domain peaks in difficulty

---

## Error Handling Defaults (Layer 3 — Confirmed)

- **Source conflicts:** Present both sides with tags; reader decides based on their situation
- **Timeline variance:** U-Curve stages are population averages; document notes expected variance and suggests tracking your own arc
- **NL-specific gaps:** Where solid research doesn't exist, say so explicitly rather than padding
- **Stale information:** Government policies and practical logistics flagged as "verify closer to move date"

---

## Quality Bar (Layer 4 — Confirmed)

- Every life domain has at least one academic source and one experiential/practical source
- Temporal markers woven into each domain — when difficulty typically peaks, mapped to U-Curve stages
- US-to-NL deltas embedded in every domain where meaningful cultural difference exists
- Source traceability — every claim tagged and linked; no unsourced assertions
- Covers full scope of living for couple in late 40s with dogs relocating to Utrecht
- Document is usable as a spec — someone could design a gamified system from it without this conversation

---

## Research Findings (Pre-Roadmap)

- Black et al.'s three-dimension model (general/interactional/work adjustment) is the most validated expatriate framework
- U-Curve timeline: honeymoon lasts days to ~6 months; culture shock deepest at months 1-6; meaningful social integration averages 2.5 years for Americans in NL
- Dutch-specific challenges: social circle closure, directness norms, expat bubble phenomenon (65% of Americans still socializing primarily with internationals after 5+ years)

---

## Requirements (Confirmed)

| ID | Title | Status | Owner | Source |
|---|---|---|---|---|
| R001 | Composite adaptation framework structure | active | M001/S01 | collaborative |
| R002 | Life domain identification and coverage | active | M001/S02 | collaborative |
| R003 | Temporal adaptation arc with timeline markers | active | M001/S01 | user |
| R004 | US-to-NL cultural delta per domain | active | M001/S02-S03 | user |
| R005 | Source traceability with credibility tagging | active | M001/S01 | user |
| R006 | Couple-specific adaptation framing | active | M001/S02 | user |
| R007 | Pet logistics domain coverage | active | M001/S03 | user |
| R008 | Professional/purpose domain (light treatment) | active | M001/S03 | user |
| R009 | Pre-move teaser phase content | active | M001/S04 | user |
| R010 | Document usable as gamification spec | active | M001/S04 | user |
| R011 | Gamification/bingo system design | deferred | none | user |
| R012 | Utrecht-specific local resource mapping | deferred | none | inferred |
| R013 | Children/schooling domains | out-of-scope | none | user |
| R014 | Software/app development | out-of-scope | none | user |

---

## Roadmap Preview (Pending Final Approval)

| Slice | Title | Risk | Depends | Demo |
|---|---|---|---|---|
| S01 | Framework Foundation & Temporal Arc | medium | — | Composite framework structure with adaptation stages documented, source template established |
| S02 | Core Life Domains — Social, Emotional, Linguistic | high | S01 | Three highest-impact domains fully researched with sources, US-NL deltas, timeline markers |
| S03 | Extended Life Domains — Practical, Professional, Pet | medium | S01 | Healthcare, housing, financial, legal/civic, professional/purpose, pet logistics, daily life completed |
| S04 | Integration, Pre-Move Teaser & Spec Readiness | low | S02, S03 | Complete document with pre-move primer, cross-domain synthesis, gamification-ready structure |

---

## File Index

| File | Purpose |
|---|---|
| `AI in May/project-one-pager.md` | Marketing-style overview for sharing with others |
| `AI in May/framework-survey.md` | Detailed evaluation of 5 frameworks + composite decision |
| `AI in May/discussion-decisions.md` | This file — all discussion decisions captured |
