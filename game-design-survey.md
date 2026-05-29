# Game Design Survey
## Pre-Research for the Alien Anthropologist Mission Program

**Purpose:** This document maps the game design landscape relevant to this project before design begins. It is the game design equivalent of `framework-survey.md` — a structured survey of concepts, frameworks, and reference systems, with evaluations of which are most applicable and why.

**Context:** The Alien Anthropologist Mission Program is a narrative-driven, multi-year gamification system for couples (and eventually groups) navigating cross-cultural relocation. Z & V are the alpha test. The system should eventually work for any relocation, any couple configuration, and any group size — with the research layer (the cultural adaptation framework) swappable per destination.

**What this document covers:**
1. Core game design concepts you need to understand
2. Relevant design frameworks — what they offer and whether we need them
3. Reference games and systems worth studying
4. Key design decisions specific to this project
5. Scaling architecture: from personal experience to usable product

---

## 1. Core Game Design Concepts

These are the foundational vocabulary items. You don't need to become a game designer, but you need to be able to speak this language when making design decisions.

### The Core Loop

The core loop is the fundamental repeating action in a game — the thing you do over and over. In chess it's "move, see the state change, decide next move." In Duolingo it's "lesson → feedback → streak update → next lesson." A game without a clear core loop is an activity, not a system.

**For this project, the unanswered question is:** what is the thing you do repeatedly? Open the mission console and check active missions? Receive a new mission? Complete an activity in the real world and log it? The answer shapes everything downstream.

### Feedback Loops

Games create two types of feedback loops:
- **Positive feedback loops:** Success generates resources that make future success easier (getting stronger as you level up). These accelerate momentum but can trivialize later play.
- **Negative feedback loops:** Falling behind creates catch-up mechanisms (Mario Kart's blue shell). These preserve tension and keep players engaged even when behind.

**For a behavior-change system**, negative feedback loops are important because they need to handle the real-world reality that life intervenes, motivation drops, and people disappear for weeks. A system that punishes absence heavily (Duolingo's streak loss) works for some users and drives others away entirely. A system that allows graceful re-entry matters for a multi-year program built around a genuinely difficult life transition.

### Progression Systems

Progression is how a player advances — the visible accumulation of change over time. The main types:

- **Linear progression:** You complete step 1, then step 2. Clear, legible, no ambiguity. Can feel like a checklist.
- **Branching progression:** Choices open different paths. Richer but harder to design and maintain.
- **Unlocking progression:** Completing certain missions unlocks access to new content. Matches the temporal arc of adaptation well — certain missions shouldn't be available in month one.
- **Leveling/stage progression:** Accumulating enough progress moves you into a new phase with different stakes and tone.

**For this project:** Unlocking progression tied to the temporal adaptation arc is the most natural fit. Missions that are only available during culture shock aren't available during the honeymoon — not because you haven't earned them, but because they aren't yet relevant.

### Intrinsic vs. Extrinsic Motivation

Extrinsic motivation comes from external rewards: points, badges, leaderboards, streaks. It works quickly and fades fast. Intrinsic motivation comes from the activity itself: curiosity, mastery, meaning, connection. It builds slowly and sustains longer.

Research on gamification for behavior change consistently shows that systems relying primarily on extrinsic reward produce short-term engagement spikes and long-term disengagement — especially for activities with real personal stakes. The Alien Anthropologist concept is explicitly designed around intrinsic motivation (the narrative frame, the sense of meaningful mission, the couple shared story) rather than points and badges. This is the right call for a multi-year system. `[Relevant framework: Self-Determination Theory — see Section 2]`

### The Magic Circle

Game designer Johan Huizinga's concept: a game creates a temporary boundary between ordinary life and the game world. Inside the magic circle, different rules apply. The alien anthropologist frame explicitly constructs a magic circle — you are not a stressed expat navigating bureaucracy, you are a field agent on a cultural observation mission. The reframe is not denial; it's a perspective mechanism. The magic circle makes hard things interesting by changing what they mean.

**Design implication:** The mission console (the web document) is the physical threshold of the magic circle. The design of that interface — its tone, its language, its visual register — needs to maintain the fiction that something more is happening here than a task list.

### Pacing and Session Design

Session design asks: what is the right unit of play? A session in Candy Crush is three minutes. A session in Civilization is four hours. A session in a year-long ARG might be one significant event per week.

**For this project:** There is no "session" in the traditional sense. The game is always running; real life is the game board. The design question is cadence: how often does new content appear, what is the expected engagement frequency, and what happens in the gaps? A system that requires daily interaction will exhaust participants in month four. A system that surfaces something interesting once or twice a week, with optional deeper engagement, fits better with a multi-year relocation arc.

---

## 2. Design Frameworks — What They Offer

### Self-Determination Theory (SDT) ✓ Most Relevant

SDT, developed by Deci and Ryan, identifies three core psychological needs that, when met by an activity, produce sustained intrinsic motivation:

- **Competence:** Feeling effective and capable. For this game: completing missions successfully, watching adaptation stages progress, becoming visibly better at Dutch life.
- **Autonomy:** Feeling that your choices are genuine. For this game: choosing which missions to take, the order of engagement, whether to deploy a redirect or complete a mission straight.
- **Relatedness:** Feeling connected to others. For this game: the couple shared experience, eventually the community of other couples using the system, and the felt connection to Utrecht itself as a place you're building a relationship with.

SDT is well-evidenced in gamification research and maps directly onto this project's design goals. It is the foundational motivational framework to design against. `[Academic: Deci & Ryan, 2000]`

### MDA Framework (Mechanics, Dynamics, Aesthetics) ✓ Use for Analysis

MDA is the standard analytical framework for game design, developed at Carnegie Mellon. It distinguishes:

- **Mechanics:** The rules and systems (what the game does)
- **Dynamics:** The behavior that emerges from mechanics in play (what players do)
- **Aesthetics:** The emotional experience the player has (what players feel)

MDA is most useful as a **design review tool** — a checklist for evaluating whether your mechanics are producing the dynamics and aesthetics you intend. Once the design is further along, running it through MDA will surface mismatches between intention and likely experience.

### Octalysis Framework (Yu-kai Chou) ◐ Useful for Gap Analysis

Octalysis organizes game motivation into eight "core drives":
1. Epic Meaning & Calling (you are part of something larger)
2. Development & Accomplishment (progress, achievement)
3. Empowerment of Creativity & Feedback (expression, experimentation)
4. Ownership & Possession (owning something, building it)
5. Social Influence & Relatedness (community, competition, mentorship)
6. Scarcity & Impatience (wanting what you can't immediately have)
7. Unpredictability & Curiosity (surprise, mystery)
8. Loss & Avoidance (fear of losing progress, FOMO)

The alien anthropologist concept already activates drives 1, 7, and partially 2 and 5. The Octalysis framework is useful for identifying which drives are *missing* from the current design concept — specifically drives 3 (player creativity and expression) and 4 (ownership of something being built). Both are worth considering.

### Flow Theory (Csikszentmihalyi) ◐ Orientation Only

Flow is the optimal engagement state: fully absorbed, not bored, not anxious, challenge matched to skill. It's most relevant for games played in single sessions. For a multi-year slow-burn system, flow is less useful as a design target — you're not designing for absorption, you're designing for sustained return over years. The more relevant analogy is habit formation, not flow.

### Bartle's Player Types ✗ Not Directly Applicable

Bartle's taxonomy (Achievers, Explorers, Socializers, Killers) was designed for competitive multiplayer games. Its relevance here is limited. The Alien Anthropologist system is cooperative and narrative-driven; Bartle's Killers don't exist in this context.

---

## 3. Reference Systems Worth Studying

These are not all "games" in the traditional sense. They are systems with structural relevance to specific design problems this project needs to solve.

### SuperBetter — Most Directly Relevant
**What it is:** A gamified resilience and behavior change system designed by Jane McGonigal, originally developed to help her recover from a concussion. Players complete "quests," defeat "bad guys" (obstacles), collect "power-ups" (real-world positive actions), and recruit "allies."

**Why it matters here:** SuperBetter is built explicitly around the premise that gamification can help people through genuinely difficult life transitions — not just habit formation, but recovery, grief, and major change. McGonigal's research shows measurable psychological benefits (reduced anxiety, increased resilience) from the system. The structural similarity to this project is direct.

**What to learn from it:** How SuperBetter structures quests that are simultaneously game actions and real-world behaviors. How it handles the "bad guy" mechanic (naming obstacles explicitly). How it supports solo play and cooperative play. How it avoids becoming a task manager.

**What's different:** SuperBetter is individual-focused and primarily extrinsic in structure. The Alien Anthropologist concept's narrative frame and couple-centric design are more sophisticated.

### Habitica — Closest Mechanical Analog
**What it is:** An RPG-style habit tracker. Daily tasks, habits, and to-dos become quests; missing them deals damage to your character.

**Why it matters here:** Habitica demonstrates what happens when real-world behavior is mapped to game mechanics at high resolution. It also demonstrates the failure mode: the mechanics become the point, the behavior change becomes secondary, and the system collapses when life disrupts the streak.

**What to learn from it:** The damage of over-mechanizing. Habitica's most engaged users love it; its dropout rate is high because the punishment loop (missing a day deals character damage) is psychologically unsustainable for people going through hard periods. This is directly relevant to designing for culture shock.

**What to avoid:** Making the mechanics so tight that real-world friction becomes game failure.

### Duolingo — The Engagement Loop Reference
**What it is:** Language learning app with heavy gamification: streaks, XP, leagues, hearts (lives), achievements.

**Why it matters here:** Duolingo is the most-studied gamification system for real behavior change (language acquisition), and it's directly relevant to one of the adaptation framework's domains. The streak mechanic produces extraordinary daily engagement — and equally extraordinary distress when broken.

**What to learn from it:** The streak is the most powerful engagement mechanic in consumer gamification, and also the most fragile point. Duolingo's "streak freeze" mechanic (you can protect a streak in advance) is an elegant solution to real-world interruption. The design of graceful forgiveness matters for a multi-year system built around life transitions.

**What to avoid:** The streak-as-identity problem, where the streak becomes more important than the learning. In a relocation game, adaptation is the point, not the game metrics.

### Geocaching — Real-World Exploration Reference
**What it is:** A global GPS-based treasure hunt. Players hide and seek physical containers, log finds, write field notes.

**Why it matters here:** Geocaching is one of the longest-running real-world exploration games, with active players maintaining engagement for 10+ years. It has solved specific problems this project needs to solve: how to make exploring a physical environment feel like a game, how to sustain engagement across years, and how field notes/logging creates a persistent narrative record.

**What to learn from it:** The field note mechanic — the habit of writing brief observations after completing a cache — creates both a personal record and a sense of contributing to something larger. This maps directly to the field-note mission type in the alien anthropologist concept.

### Night in the Woods / Oxenfree — Narrative Tone Reference
**What they are:** Narrative video games with strong voice, environmental storytelling, and low mechanical friction.

**Why they matter here:** The alien anthropologist concept's strongest asset is its narrative frame. These games demonstrate that a compelling voice and fictional world does more for sustained engagement than complex mechanics. The tone you establish in the mission console — the language of mission briefings, field notes, redirect overlays — is as important as the structure.

**What to learn from them:** Specific narrative devices: how to write a mission briefing that feels authored rather than administrative, how environmental observation becomes story, how to make a "log your observations" mechanic feel like discovery rather than homework.

### Pandemic / Forbidden Island — Cooperative Board Game Reference
**What they are:** Cooperative board games where all players work together against the game system, not against each other.

**Why they matter here:** Cooperative game design has solved the "alpha player problem" — the tendency in cooperative games for one player to dominate decisions while others follow. This is directly relevant to couple game design, where one partner being more engaged or more design-literate could turn the other into a passenger.

**What to learn from them:** Role differentiation — giving each player a distinct function that the group genuinely needs. Hidden information that each player holds separately — both players need to contribute because neither has the full picture. Both mechanics are applicable to the couple dynamic in relocation (partners adapting in different domains, both needing to contribute observations).

### Fog of Love — Couple-Specific Reference
**What it is:** A two-player board game specifically designed for couples, structured as a romantic comedy. Players create characters with conflicting traits and objectives and play through a relationship narrative.

**Why it matters here:** Fog of Love is the most direct existing example of game design for two people with asymmetric internal states and a shared narrative. It handles emotional complexity, disagreement, and different perspectives as game mechanics rather than obstacles to gameplay.

**What to learn from it:** How it structures shared and private objectives. How it handles the couple diverging and reconvening. How it makes both players feel seen and individually motivated rather than cooperative in a generic sense.

---

## 4. Key Design Decisions Specific to This Project

These are the decisions that cannot be made without the pre-research context above. They are in roughly the order they need to be made, because later decisions depend on earlier ones.

### Decision 1: What Is the Core Loop?

**The question:** What is the repeating unit of interaction? What do you actually *do* in this game?

**Options:**
- **Receive → Accept → Complete → Log:** You receive a mission, accept it, complete it in real life, log your field notes. This is the most structured option.
- **Open → Check → Explore:** You visit the mission console, see what's active, engage with whatever feels right. More ambient, less structured.
- **Trigger → Respond → Reflect:** Something in real life triggers a mission prompt (a new neighborhood, a Dutch social encounter, an adaptation stage transition), you respond, you reflect. The game world responds to real-world events.

**Recommendation direction:** A hybrid of the first and third — the console has active missions you can seek out, but real-world events also surface missions contextually. This requires thinking about what "triggers" look like in practice.

### Decision 2: How Does Temporal Locking Work?

**The question:** The research framework is organized around adaptation stages (Honeymoon, Culture Shock, Recovery, Mastery). Some missions are only relevant in specific stages. How does the game know what stage you're in?

**Options:**
- **Calendar-based:** Missions unlock on a schedule (month 1–2, month 3–6, etc.)
- **Self-reported stage:** Players declare their current adaptation stage; content responds accordingly
- **Event-triggered:** Specific real-world events (first Dutch friendship, completing inburgering, first trip back to the US) trigger stage transitions

**Recommendation direction:** Self-reported stage with optional calendar prompts. The research is explicit that individual timelines vary widely from population averages; locking to calendar dates would misalign many users. But calendar prompts ("it's been three months — does this still feel like where you are?") support reflection.

### Decision 3: How Does the Couple Mechanic Work?

**The question:** The research framework documents that partners adapt at different rates across different domains. How does the game represent and use this?

**Options:**
- **Shared account, individual missions:** Both partners see the same mission console but some missions are assigned individually
- **Asymmetric roles:** Each partner has a distinct function (one is the Field Agent, one is the Mission Analyst — or similar) with different but interdependent mission types
- **Separate tracks that converge:** Each partner has their own adaptation arc visible to both; certain missions require both tracks to reach a threshold before unlocking

**Recommendation direction:** Asymmetric roles with converging missions. This solves the alpha player problem, makes both contributions necessary, and mirrors the documented reality of couple adaptation (different domains, different rates, both essential).

### Decision 4: How Does Scaling to Other Users Work?

**The question:** Z & V are the alpha test for a US → Netherlands relocation. How does the system eventually work for a US → Germany couple, or a UK → Canada family of four?

**The architecture question:** Is the game system country-agnostic (the alien anthropologist mechanics work anywhere) with swappable research modules (the adaptation framework is destination-specific)? Or is it more tightly integrated?

**Recommendation direction:** The game system should be country-agnostic from the start, even in the alpha. The research layer (which country you're moving to, what cultural deltas apply, what the legal/civic setup looks like) is a module. This means designing the mission templates so they have placeholders for destination-specific content rather than hardcoding Netherlands specifics into the game mechanics.

**Group size:** The couple → family/friends expansion needs to define what additional participants can do. Options: additional players have their own missions within the shared arc, additional players are "field contacts" with a different but supporting role, additional players join as a separate crew with their own arc that intersects with the primary couple's.

### Decision 5: What Does "Done" Look Like for a Mission?

**The question:** How is a mission completed? Who decides? What is logged?

**Options:**
- **Self-declared:** You did it, you mark it done. No verification. High trust, low friction.
- **Logged evidence:** You write a field note (a brief observation, a reflection, a photo) that serves as the completion record. This is Geocaching's approach.
- **Partner-confirmed:** The other player confirms your completion. Creates accountability but also friction.

**Recommendation direction:** Logged field note as completion, self-declared. The field note is the artifact — it creates the persistent record that makes the game meaningful over years, and it's the mechanism by which a real-world activity becomes a narrative event. The alien anthropologist frame makes field notes feel natural: you completed a cultural observation mission, of course you filed a field report.

### Decision 6: How Does the System Handle Abandonment and Re-entry?

**The question:** Life will interrupt. Culture shock will make the game feel pointless. What happens when a couple goes dark for two months?

**The design imperative:** A multi-year system built around a genuinely difficult life transition cannot punish absence. Duolingo's streak model would be toxic here. The system needs graceful re-entry that acknowledges the gap without making it a failure state.

**Recommendation direction:** The gap becomes a mission. "Your field communications were interrupted. Mission: reconstruct what happened in your absence. What did you observe that you didn't have time to log?" This turns a real-world failure mode into a game mechanic — and also happens to produce exactly the kind of reflective processing that the adaptation research says is beneficial.

---

## 5. Scaling Architecture: From Personal to Product

This section maps the design decisions required to move from "a system built for Z & V going to Utrecht" to "a system any couple can use for any relocation."

### The Modular Research Layer

The adaptation research framework (`adaptation-research-framework.md`) is the first instance of a pattern. The underlying structure — composite theoretical framework, life domains, temporal arc, US-NL cultural delta, couple framing, source traceability — is replicable for any origin-destination pair.

**For the game system to be portable, the research layer must be treated as a module, not hardcoded content.** Specifically:
- Mission templates reference "the dominant cultural challenge in this domain" rather than "Dutch directness"
- Temporal markers reference "your current adaptation stage" rather than specific month ranges
- Cultural delta missions reference "the cultural gap you identified in pre-research" rather than "Dutch vs. American birthday culture"

The mission *structure* is universal. The mission *content* is destination-specific.

### Variable Group Configuration

The couple is the base unit of the alpha. Scaling to families and friend groups requires defining:

- **Core pair:** The primary relocation couple — always the center of the arc
- **Extended crew:** Family members, close friends who are following the relocation from afar — different mission types (observation, support, curiosity-based rather than adaptation-based)
- **Field contacts:** People the couple meets in the new country — missions that involve recruiting field contacts, deepening field contact relationships, converting contacts into local allies

This structure allows the system to grow without losing focus on the primary adaptation arc.

### Country/City Modularity

The research layer is currently built for US → Netherlands. A modular system needs:

- A **destination pack** structure: the cultural adaptation research, life domain specifics, and legal/civic information for a given destination
- A **base game layer** that works without any destination pack (the alien anthropologist narrative, the chapter structure, the mission types, the couple mechanic)
- A **destination research template** so that destination packs can be created using the same methodology as this one

The alpha design should not hardcode the Netherlands into the game mechanics — it should use the Netherlands content as the first destination pack.

### Privacy and Sharing

As the system scales, participants will need to decide what they share:
- Field notes are inherently personal — should they be private to the couple, shareable with the extended crew, or potentially (with consent) shareable with the broader community of users?
- The community layer — seeing that other couples at month eight are also finding social integration hard — has genuine psychological value (normalization) and needs to be considered early even if it's a later feature

---

## Summary: What You Now Know and What Comes Next

### What's already decided (from the Alien Anthropologist document)
- Narrative frame: alien anthropologists assessing human development
- Format: interactive web document / mission console
- Duration: 3–5 years, chapter-based
- Mission types: core / field-note / wildcard / redirect overlay
- Design principles: hidden utility, mixed portfolio, surprise without chaos

### What the pre-research has surfaced
- The core motivational framework to design against: Self-Determination Theory (competence, autonomy, relatedness)
- The key design decision still open: the core loop
- The couple mechanic recommendation: asymmetric roles with converging missions
- The scaling architecture requirement: research layer as a swappable module, not hardcoded content
- The failure mode to avoid: punishment-based systems (Duolingo streak model) applied to culture shock
- The field note as the central completion artifact
- Reference systems ranked by relevance: SuperBetter > Geocaching > Duolingo > Fog of Love > Pandemic > Habitica

### What comes next (the design phase)
1. Define the core loop explicitly
2. Design the asymmetric couple roles
3. Design the chapter template (what a chapter contains, how it transitions)
4. Design the mission template (what a mission contains, how it's written)
5. Build Chapter 1 for Z & V (Utrecht-specific, Honeymoon stage)
6. Build the mission console (the web document)

---

*This survey is the pre-research input for the game design phase. The design phase begins with the core loop decision — everything else depends on it.*
