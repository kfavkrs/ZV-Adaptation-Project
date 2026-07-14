# Design Rationale — Investor/Collaborator Explainer Page

How the Claude Design prompt (`claude-design-investor-page-prompt.md`) came together,
and why. Reconstructed from a Claude chat conversation, 2026-07-13.

---

## Starting point

The ask began as "make an HTML page explaining the concept from zero understanding."
Before generating anything, the brief was clarified through a short back-and-forth
rather than assumed — three axes mattered most for a page like this:

- **Audience** → Potential collaborators/investors (not personal reference, not a public
  showcase). This decision shaped everything downstream: the page needed to read as
  credible research + real product, not a relocation diary with a game skin.
- **Scope** → Both halves of the project as one throughline — the psychology research
  *and* the game product — rather than either in isolation. The pitch only works if the
  research is visibly the foundation the product stands on.
- **Aesthetic** → Left open rather than pre-specified, on the logic that the subject's own
  vocabulary (summons, dossier, debrief, field agent) should generate the visual identity,
  rather than reaching for a generic look and decorating it with mission-themed copy.

## Iteration 1 — Research + basic game loop

The first full draft covered:
- The four psychology models (Black/Mendenhall/Oddou, Ward's ABC, Kim's
  Stress-Adaptation-Growth, Oberg's U-Curve) and how they stack into one framework
- The 10 life domains and which four cluster hardest in the culture-shock window
- The Alien Anthropologist mission loop as originally scoped: Summons → Authentication →
  Briefing → Research → Field Work → Debrief → Log → Narrative → Next Mission
- Couple mechanics (Joint/Split/Individual/Agent-to-agent missions)
- The Octalysis gap analysis (Epic Meaning & Unpredictability activated; Development &
  Social Influence partial; Creativity/Feedback and Ownership/Possession open gaps)

## Iteration 2 — The 2.5-year arc as product scope, not just research trivia

Correction: the U-curve's 2.5-year meaningful-integration timeline isn't just a research
citation — it's the actual designed lifespan of the app. Two things followed from this:

- The mission engine isn't a fixed quest chain. Quests are continuously re-audited against
  all four models and all ten domains *simultaneously*, then ranked by three live signals:
  current energy, current felt alienation, and life-ease impact. This reframes the product's
  core IP as a live prioritization engine, not a content library.
- The PWA / mobile-field angle was added: platform-agnostic, installable, and usable
  mid-mission from a phone — not just a planning tool used at a desk.

This changed the prompt's instruction from "show the mission loop" to "make the 2.5-year
arc visible as the product's actual scope" — the timeline had to read as a commitment the
product is built to honor, not a stat in a chart.

## Iteration 3 — Multi-agent generation and the journal layer

Two more corrections, both about what actually generates a mission and what a mission
leaves behind:

- **Generation isn't scripted.** Missions are produced by multiple AI agents called via
  API, not a decision tree — reading the player's live energy/resource state *and* the
  actual text of past debriefs and journal entries. This is a materially different claim
  than "content adapts to your stage"; it's "content adapts to what you specifically wrote."
- **The app is a journal, not just a task list.** Weekly field reports — big or small —
  accumulate into a permanent, timestamped, domain-tagged archive. Over 2.5 years this log
  becomes a durable personal record, generated as a byproduct of playing rather than a
  separate habit the player has to maintain.

Both were folded into the "core IP" framing in the final prompt: the live prioritization
engine, the multi-agent generation, and the journal/archive were positioned as the three
things the page needs to make an investor believe are real and hard to copy — with the
mission loop, couple mechanics, and PWA/field angle as supporting mechanics underneath.

## Iteration 4 — What changed during the actual build in Claude Design

The prompt above was the brief going in. The generated page (`index.html`) went further
than the brief in several places — real product decisions surfaced in the writing itself,
not just aesthetic choices. Worth memorializing because these read as genuine additions to
the product concept, not just copywriting:

- **The live prioritization engine became an interactive demo, not just a description.**
  The page lets you move Energy, Felt Alienation, and Life-Ease Need sliders and watch a
  ranked mission queue re-sort in real time, with an "engine verdict" explaining the top
  pick. This makes the core IP something a reader can *feel*, not just read about.

- **Multi-mode field capture ("Transmission") is now a named, explicit feature.**
  Debriefs aren't just "a field report" — the page specifies three capture modes (Photo,
  Audio — two minutes, unedited, Written) and frames the phone as "your communicator to
  the mothership." Each capture is auto geo-stamped and domain-tagged the instant it's
  transmitted. This is more concrete than the original "file a debrief" framing.

- **Mission architecture is named as its own design space.** Beyond the original
  Joint/Split/Individual/Agent-to-agent list, the page introduces a labeled library of
  interaction shapes: Simultaneous-apart, Asynchronous, Geo-triggered, Out loud,
  Relay/handoff, and Blind send — with Split-and-Regroup featured as the flagship example.
  Framed explicitly as "a design space, not a format," with the library positioned as
  open and expanding.

- **Party size became an explicit, generalized parameter.** The original brief scoped
  mission types to a couple. The page reframes this: "built first for two, designed for
  any number" — Solo (1), Duo (2), and Family (3+) are named as parameters the same engine
  scales across, not separate builds.

- **A new feature appeared: the consented co-op network.** Not present in any earlier
  draft — the page introduces matching with opted-in locals and other expats on the same
  curve (Native-guided, Agent-to-agent, Cohort ops), gated by a strict mutual-opt-in
  "Handshake Protocol" (nothing shared before all parties accept, revocable anytime,
  engine-matched so invites only surface when they fit everyone's stage). The page ties
  this directly back to the Octalysis analysis: this network is framed as the lever that
  moves "Social Influence & Relatedness" from partial toward activated.

- **The Octalysis gaps became deliberate design stances, not just open items.** "Loss &
  Avoidance" is described as intentionally kept soft (no penalty mechanics, matching the
  "pause don't lose" philosophy), and "Scarcity & Impatience" is described as intentionally
  left unmapped — reframing what read as two open gaps in the prompt as one active choice
  and one true gap.

- **Framing shift on the debrief archive:** described in the page as "not a scoreboard, a
  memory book" — same underlying journal/archive concept from the prompt, but the emotional
  framing (an accomplishment log you'd actually want to reread) is new and sharper than the
  prompt's "durable output" language.

- **One inconsistency worth resolving:** the hero stat card reads "Seattle → Utrecht" while
  the footer reads "Austin → Utrecht." Worth a fix pass before this goes out to anyone —
  pick one origin city and correct the other.

## What stayed constant throughout

- Every research claim keeping its [Academic] / [Government] / [Experiential] tag — the
  credibility layer was never negotiable.
- The instruction to avoid the three converging "AI-generated page" looks (cream/serif/
  terracotta, dark-mode/single-neon-accent, broadsheet/hairline-rules) and instead build
  the visual identity out of the project's own field-agent vocabulary.
- Phase 1 complete / Phase 2 open as the closing call to action — the page's job is to
  make Phase 2 look like an opportunity, not a pitch for something already finished.
