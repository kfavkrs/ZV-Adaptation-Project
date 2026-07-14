# Claude Design Prompt — Investor/Collaborator Explainer Page

**Purpose:** One-shot prompt for Claude Design to generate a single-page site pitching
the Adaptation Blueprint / Alien Anthropologist Mission Program to potential
collaborators and investors. Drafted conversationally in Claude chat, finalized 2026-07-13.

---

Build a single-page site pitching "The Adaptation Blueprint / Alien Anthropologist Mission Program" to potential collaborators and investors. Audience is sophisticated — they need to come away believing this is a rigorous, research-grounded framework with a genuinely novel product on top of it, not a personal relocation diary with a game skin.

## THE STORY (research → product, one throughline)

**Part 1 — The Research.** A couple is relocating from Austin, TX to Utrecht, Netherlands (2025–2026). Instead of winging it via expat forums, they built a research framework synthesizing four established cross-cultural psychology models:
- Black, Mendenhall & Oddou's Expatriate Adjustment Model — the structural backbone: self-oriented (internal resilience), others-oriented (relationship-building across cultures), perceptual (understanding why locals act as they do)
- Ward's ABC Model — separates Affect (how you feel), Behavior (what you do), Cognition (how you think about yourself)
- Kim's Stress-Adaptation-Growth Dynamic — adaptation isn't linear, it spirals: stress → learning → growth → new stress at a higher level
- Oberg's U-Curve — the temporal arc: honeymoon phase, then culture shock bottoming out around month 4, recovery, adjustment, mastery — with meaningful integration averaging 2.5 years

These map onto 10 life domains (social & community, language, emotional/psychological, professional/purpose, healthcare, housing, financial, legal/civic, pet logistics, daily life). Four of these — social, language, emotional, daily life — peak in difficulty during the culture-shock window (roughly months 2–6); the rest peak earlier or later. Every claim in the underlying research is source-tagged as [Academic], [Government], or [Experiential] — nothing is asserted without a credibility level attached.

**Part 2 — The Product.** This research becomes the backbone of "Alien Anthropologist," a mission-based app spanning the full 2.5-year integration arc — the same timeline the U-curve research says meaningful integration actually takes. The product is designed to run the whole journey, not just the hard opening months.

The core mechanic is a live prioritization engine, not a fixed quest chain: at any point, the quests offered are continuously audited against all four psychological models and all ten life domains simultaneously, then ranked by three live inputs — the player's current energy level, their current felt alienation, and how much a given task would actually ease day-to-day life right now. Mission generation itself is powered by multiple AI agents orchestrated via API calls (not a scripted decision tree) — these agents read the player's reported energy, available resources, and details the player has actually written in past debriefs and journal entries, and use that to shape what mission or narrative text comes next. The system is always solving for "what's the single most valuable thing for this person to do today," and it's genuinely responsive to what the player says, not just where they are on a timeline.

The app is also a long-term personal journal, not just a task list. As missions complete — big or small, weekly — the player files a field report, and these accumulate into a running, timestamped, domain-tagged archive of the entire relocation. Over 2.5 years this log becomes the most durable output of the whole experience: a real record of the adaptation journey, generated as a byproduct of actually living it rather than a separate journaling habit.

The core loop wrapping this engine: Summons (a Telegram message pulls you in) → Authentication (a small ritual marking the threshold into mission mode) → Briefing (personalized, acknowledges your history) → Research (mini-games, clips, prep material) → Field Work (you actually go do the real-world thing) → Debrief (you file a field report — the journal entry) → Mission Log (permanent, timestamped, domain-tagged) → Narrative Progression (the story reacts to what you actually did and wrote) → Next Mission unlocked.

Design specifics worth surfacing: missions run at 2/week, with intensity (light/medium/heavy) adapting to which U-curve stage the player is in — during culture shock the system defaults to light, supportive missions, not fewer missions. No penalties for pausing ("going undercover") or opting out. Many distinct quest/task types are planned (this catalog is still in design — don't invent specifics, gesture at it as an open, expanding library rather than a fixed list). For couples specifically, most missions are Joint (done together), with occasional Split (same location, different objectives, compare notes after), Individual, and Agent-to-agent (one partner sends the other a mission blind) types.

The whole thing is built as a PWA — deliberately platform-agnostic, installable on any device, and designed to be fully usable from a phone mid-mission out in the field, not just at a desk planning one.

The game design was also audited against Yu-kai Chou's Octalysis framework: Epic Meaning and Unpredictability are fully activated, Development and Social Influence are partial, and Creativity/Feedback plus Ownership/Possession are identified as open gaps — the clearest opportunity for a next design pass.

Status: Phase 1 (research) is complete. Phase 2 (building the actual mission program) hasn't started — this is the open opportunity being pitched.

## WHAT THE PAGE NEEDS TO DO

- Open with a hero that states the thesis in one clear line: rigorous psychology research turned into a real product for a genuinely hard, underserved problem (cross-cultural relocation).
- Walk through the four research models and the U-curve timeline visually — this is the credibility layer, it should feel like real research, not marketing.
- Show the 10 domains and which four are hardest earliest.
- Bridge clearly into the product: emphasize the live prioritization engine (multi-agent, reading energy / alienation / life-ease and the player's own written debriefs) as the core IP, then the mission loop, the journal/archive angle, couple mechanics, PWA/mobile-field angle, and the Octalysis gap analysis.
- Make the 2.5-year arc visible as the product's actual scope, not just a research factoid — the app is built to last the whole journey and become a long-term personal record.
- Close with the Phase 1 complete / Phase 2 open status as a clear call to action for collaborators.

## DESIGN DIRECTION

Take a real point of view — don't default to cream-background-serif-terracotta, dark-mode-with-one-neon-accent, or broadsheet-hairline-rules, these are the three looks every AI-generated page converges on. The material already has its own vocabulary (summons, briefing, debrief, mission log, field agent, dossier) — build the visual identity out of that world, but keep it credible and polished enough for an investor audience, not gimmicky or costume-y. One bold, well-justified signature element is better than several timid ones. Fully responsive, real content throughout (no lorem ipsum), respect reduced-motion preferences.
