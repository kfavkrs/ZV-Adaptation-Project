# Core Game Loop
## Alien Anthropologist Mission Program

**Status:** Cadence decided. Couple mechanic decided. Pending: authoring and authentication design.

---

## The Loop

**Summons → Authentication → Briefing → Research → Field Work → Debrief → Log → Narrative Progression → Next Mission**

---

## Step by Step

### 1. Summons
A Telegram notification reaches the player in real life. The game initiates contact — you don't have to remember to open anything. The summons breaks into your day and pulls you into the mission world.

#### Cadence — Decided

**Base rate: 2 missions per week, all stages including culture shock.**

Frequency stays constant across the full adaptation arc. What changes is mission intensity — the system defaults to lighter missions during harder stages, not fewer of them. The game stays present and supportive throughout; it bends to your capacity rather than going quiet.

**System manages stage defaults. Players adjust at login** by selecting their current capacity:
- **Light** — reflection, observation, a brief note. 15 minutes or less. For hard weeks.
- **Medium** — neighborhood exploration, a research task, a Dutch social encounter. ~1 hour.
- **Heavy** — attend an event, navigate a system, travel somewhere. Half a day or more.

The system reads your current adaptation stage and defaults to an appropriate intensity mix. You override it at any login.

**Telegram thread as control interface.** At any time, you can text the mission Telegram thread to request a status update or signal that you want a new mission. The thread is a two-way channel — not just a notification pipe.

**Three flexibility mechanics:**

| Mechanic | What it means | What happens |
|---|---|---|
| **Going undercover** | Not ready — pause, don't abandon | Mission goes dormant. Resumes when you return. No penalty. |
| **Opt out** | Skip this one entirely | Mission is released. Next summons brings something lighter. No penalty. |
| **Intensity selection** | Signal your capacity at login | System serves a mission at the level you chose. |

**Culture shock mission types (Light defaults):**
When the system is in culture shock stage and you've selected Light, missions draw from a pool designed to support rather than demand:
- *Reflection:* Sit somewhere and write three observations about this week
- *Recognition:* Name one thing that felt easier than last month
- *Connection:* Reach out to someone you miss. Log how it felt.
- *Partner check-in:* Tell each other one hard thing right now. File it.

These missions still advance the log, still feed the narrative, still count. They just don't ask you to go anywhere on a week when getting out of bed was the achievement.

**Re-entry after going dark:** After 14 days of no activity, the system sends an automatic "field communications interrupted" summons. The mission is reconstruction — what happened while you were offline? This turns the gap into content rather than failure. No streaks, no damage, no shame.

### 2. Authentication
A password protocol confirms you're entering the mission console. This is the threshold between ordinary life and the game world — the moment you step into the alien anthropologist identity. The friction is intentional: even a small ritual makes the transition feel real.

**Open question:** What is the authentication mechanic? A rotating passphrase? A code delivered separately? Something that changes by chapter?

### 3. Personalized Mission Briefing
A Mission Impossible-style briefing greets you by agent designation, acknowledges recent completed missions, and introduces the new assignment. The brief is written, visual, and authored — it feels like someone is running your mission, not like a notification.

**Open question:** How is the briefing personalized? Template system with variable fills (name, recent mission, current adaptation stage)? Human-authored in advance? AI-generated from mission log data?

### 4. Research & Mini-Games
Supporting materials are embedded in the brief to prepare for the field mission. Format varies by mission and learning style:
- **Visual:** YouTube clips, photo essays, infographics
- **Audio:** Podcast excerpts, language recordings, ambient sound
- **Kinesthetic:** Mini-games (crossword, matching, scenario quiz) built around mission-specific content

*Example: A mission about Utrecht's emergency services includes a crossword with Dutch firefighting vocabulary before you visit a fire station.*

**Open question:** Who builds the mini-games? These are significant production assets. For the alpha, simpler formats (linked articles, embedded video) may stand in while custom mini-games are built for specific high-value missions.

### 5. Real-World Field Work
You go do the thing. Attend the event, visit the location, have the conversation, navigate the system. The app stays with you — you collect data as you go: photos, voice notes, written observations, coordinates.

This is the core of the experience. Everything else is in service of this step.

### 6. Debrief Submission
Back in the app, you hit "Complete Mission" and submit a summary brief. Format is flexible — could be a few sentences, a photo with caption, a voice memo transcript. The brief is your field report: what you observed, what surprised you, what you'd tell another agent going into the same mission.

The debrief is the field note. It is the artifact that makes the experience permanent.

### 7. Mission Log Update
The debrief is written to the permanent mission log — a running record of the full adaptation journey. Each entry is timestamped, tagged by domain and adaptation stage, and linked to the mission that generated it.

Over years, the log becomes the record of who you were becoming and when. It is the most valuable long-term asset the system produces.

### 8. Narrative Progression
Completing the mission advances two tracks:
- **Short-term plot:** The current chapter arc moves forward. Something is revealed, a new thread opens, the story reacts to what you did.
- **Long-term arc:** The executive narrative — the alien anthropologists' multi-year mission — accumulates evidence and evolves.

The narrative responds to completion, not just to the passage of time. This is what makes it a game and not a journal.

### 9. Next Mission Unlocked
Completion unlocks the next available mission. Some missions are linear (this unlocks that). Some are parallel (completing domain A unlocks options in domains B and C). Some are stage-gated (only available once you've self-reported entering a new adaptation stage).

---

## What Makes This a Game and Not a Checklist

- The summons comes to you — you don't manage a backlog
- Authentication creates a ritual boundary between ordinary life and mission mode
- The briefing is addressed to you, acknowledges your history, tells a story
- Research and mini-games make preparation feel like play
- The real-world action is the mission, not a task attached to a mission
- The debrief creates a permanent artifact that accumulates meaning over time
- Narrative progression means each completion changes something — the world responds

---

## Open Design Questions (in priority order)

| # | Question | Status |
|---|---|---|
| 1 | What controls summons cadence? | ✓ Decided — see Summons section |
| 2 | How does the couple mechanic work? | ✓ Decided — see Couple Mechanic section |
| 3 | How is the briefing personalized? | Open — template vs. AI-generated vs. human-authored |
| 4 | What is the authentication mechanic? | Open — rotating passphrase, chapter-specific code, other |
| 5 | Who authors missions, and how far in advance? | Open — human-curated vs. AI-assisted vs. template-driven |
| 6 | What is the mini-game production plan for the alpha? | Open — custom builds vs. linked external content for Chapter 1 |

---

## Couple Mechanic — Decided

**Core principle:** The most valuable thing this game produces for a couple is the record of how differently two people experience the same thing. The divergence between two partners' debriefs of the same mission *is* the couple narrative.

**Mission weighting: heavily Joint.** Most missions are designed for both partners. Individual and split missions exist but are the exception, not the rule.

**Four mission types:**

| Type | Weight | Who receives it | Who debriefs | How it works |
|---|---|---|---|---|
| **Joint** | Dominant | Both partners | Together | Done together as a team. One shared experience, one shared debrief. |
| **Split** | Occasional | Both partners | Both, independently | Arrive together, divide with different objectives, a time limit, and a rendezvous point. Each collects observations independently. Reconvene and compare what you found — the divergence between two accounts is the content. |
| **Individual** | Rare | One partner only | That partner only | Used when the domain calls for it — a solo language challenge, a social situation one partner needs to navigate alone. |
| **Agent-to-agent** | Occasional | One partner only | Receiving partner → sender first, then shared log | One partner sends a mission to the other. Sender sets the objective; receiver doesn't have full context. Debrief goes to the sender privately first, then surfaces in the shared log. Partners become co-authors of each other's experience. |

**Why Split missions work:** Two agents, one location, different targets. You don't know what the other person found until the rendezvous. The surprise of comparing observations makes a single place feel twice as rich — and the divergence between your two accounts is the story.

**Why Agent-to-agent works:** The sender has information the receiver doesn't. The receiver files a report back to the sender before it becomes shared. This is the only mission type where one partner sees something first — which makes the reveal to the shared log a small narrative event.

**Chapter progression:** Certain story milestones require both partners to have filed their debrief before the next chapter unlocks. Neither partner can advance the narrative alone. The story waits for both of you.

**Scaling beyond the couple:** Additional participants (family members, close friends) join as *extended crew* with their own mission types — observation, support, curiosity-based — that feed into the primary couple's arc without displacing it. The couple remains the center; crew members are supporting cast with real roles.

*See `game-design-survey.md` Section 5 for full scaling architecture.*
