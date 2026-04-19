# Prioritization: FocusFlow v1 Feature Roadmap

**Framework:** RICE + Value/Effort Matrix + Strategic Overrides
**Date:** 2026-04-16
**Goal:** Define which features to build first, what to hold for v1.1, and what to defer entirely.

---

## Context

*What I pulled from analysis:*
- **Active goals:** Ship a lovable v1 that wins the "second-screen ambient productivity" category, drives D7 retention, and establishes a freemium growth engine.
- **Top JTBD opportunities:** Mood regulation (17), Escape/visual transport (15), Identity + pride (15), Break enforcement (14), End-of-day closure (14).
- **Competitive gaps to own:** Time-of-day scene transitions, End-of-Day ritual, Break Lock mode, aspirational achievement theming — none of these exist in the market.
- **Critical constraint:** Visual scene assets are the production bottleneck. Audio licensing must be resolved. Auth/persistence needed for any stateful feature.

**Scoring notes:**
- Reach: estimated daily active user base at 3 months post-launch (target: 1,000 DAU). Scored as % of total user base that feature touches.
- Impact: RICE multiplier (0.25 = trivial → 3.0 = massive) based on JTBD opportunity scores.
- Confidence: How certain we are based on founder validation + competitive signals.
- Effort: Relative person-weeks for a lean team (1–2 engineers + 1 designer).

---

## All Features Scored

| Rank | Feature | RICE Score | R | I | C% | E (wks) | JTBD Opp | Strategic |
|------|---------|-----------|---|---|----|---------|----------|-----------|
| 1 | Ambient Scenes (3 at launch) | **270** | 1000 | 3.0 | 90 | 10 | 15–17 | 🔑 Core |
| 2 | Lo-fi + White Noise Audio Layer | **243** | 900 | 3.0 | 90 | 10 | 17 | 🔑 Core |
| 3 | Pomodoro Timer | **540** | 1000 | 3.0 | 90 | 5 | 12 | 🔑 Core |
| 4 | End-of-Day Summary (Clock Out) | **224** | 700 | 3.0 | 80 | 7.5 | 14 | 🏆 Differentiator |
| 5 | Break Lock Mode | **210** | 700 | 3.0 | 80 | 7 | 14 | 🏆 Differentiator |
| 6 | Sticky Note Task Tracker | **200** | 800 | 2.0 | 75 | 6 | 11 | ✅ Table stakes |
| 7 | Time-of-Day Scene Variants (×4 per scene) | **120** | 600 | 2.0 | 75 | 10 | 15 | 🏆 Differentiator |
| 8 | Streaks System | **180** | 600 | 2.0 | 75 | 4 | 10 | ✅ Retention |
| 9 | User Auth (Sign up / Login) | **360** | 600 | 3.0 | 100 | 5 | — | 🔧 Enabler |
| 10 | Achievement Badges | **90** | 500 | 1.0 | 60 | 5 | 10 | ✅ Retention |
| 11 | User Profile + Settings | **80** | 400 | 1.0 | 100 | 5 | — | 🔧 Enabler |
| 12 | Audio Volume Controls (music + noise separate) | **135** | 900 | 1.0 | 75 | 2 | — | ✅ Polish |
| 13 | Pomodoro Customization (duration settings) | **90** | 600 | 1.0 | 75 | 2 | — | ✅ Polish |
| 14 | Additional 3 Scenes (v1.1) | **60** | 400 | 1.0 | 75 | 10 | 15 | 📅 v1.1 |
| 15 | Shareable End-of-Day Card | **90** | 600 | 1.0 | 75 | 3 | 9 | 📈 Growth |
| 16 | Session History / Past Summaries | **40** | 400 | 1.0 | 50 | 4 | — | 📅 v1.1 |
| 17 | Multiplayer / Social Body Doubling | **0** | — | — | — | 30+ | 8 | ❌ Defer |
| 18 | Mobile Version | **0** | — | — | — | 30+ | — | ❌ Defer |
| 19 | Spotify / Streaming Integration | **30** | 400 | 0.5 | 60 | 5 | — | 📅 v1.1 |

---

## Detailed Breakdown

### #1: Ambient Scenes — 3 at Launch *(Score: adjusted to top by strategic weight)*

- **Reach:** 1,000 users — 100% of all users open the app for the scene. This is the product.
- **Impact:** 3.0× — Directly addresses the highest JTBD opportunity (Escape job: 15, Mood regulation: 17). Without scenes, there is no product.
- **Confidence:** 90% — Validated by Lofi Girl's 20–30K concurrent viewers, Lofi.co's 40+ scene library demand, and personal founder experience.
- **Effort:** ~10 weeks — Includes 3 scenes × 1 time-of-day variant at launch (morning/sunset default). Full time-of-day variants are a separate line item.
- **RICE Score:** (1000 × 3.0 × 0.9) / 10 = **270**
- **Goal alignment:** ✅ Core product identity. Cannot ship without this.

> 🔑 **Strategic override:** Even if RICE didn't rank this #1, it is non-negotiable. Scope down to 2–3 scenes to hit timeline; DO NOT compromise on visual quality.

---

### #2: Lo-fi + White Noise Audio Layer *(Score: 243)*

- **Reach:** 900/1000 — Near-universal. Most users will engage with audio.
- **Impact:** 3.0× — Directly addresses the Mood Regulation job (Opp Score: 17, the highest in the JTBD analysis). Endel has proven the science here.
- **Confidence:** 90% — Lofi Girl's audience, Lofi.co sound layering, and Focusflow's own differentiator (mixing music + white noise) are all validated.
- **Effort:** ~10 weeks — Includes audio licensing/sourcing, playback UI, two sliders (music volume, noise volume). Parallelizable with scene dev.
- **RICE Score:** (900 × 3.0 × 0.9) / 10 = **243**
- **Goal alignment:** ✅ Core product. Must ship with scenes.

> ⚠️ **Assumption:** Audio can be sourced royalty-free or licensed for <$500/mo at launch. Needs validation before sprint 1.

---

### #3: Pomodoro Timer *(Score: 540 — highest raw RICE)*

- **Reach:** 1,000 users — All users will encounter the timer; many will use it.
- **Impact:** 3.0× — Core functional job (Opp Score: 12). Every ambient focus competitor has one — table stakes AND differentiator when integrated with end-of-day data.
- **Confidence:** 90% — Pomodoro apps have millions of downloads; demand is unambiguously validated.
- **Effort:** ~5 weeks — Relatively straightforward engineering (start/pause/reset, work/break cycles, silent notification). Fastest high-impact feature to ship.
- **RICE Score:** (1000 × 3.0 × 0.9) / 5 = **540**
- **Goal alignment:** ✅ Core product. Ships in v1.

> 💡 The Pomodoro timer has the highest raw RICE score because of low effort. Ship it fast; it also feeds the End-of-Day summary data.

---

### #4: End-of-Day Summary (Clock Out) *(Score: 224)*

- **Reach:** 700/1000 — Not all users will clock out every day, but highly engaged users (the ones you want to retain) will.
- **Impact:** 3.0× — Directly addresses End-of-Day Closure job (Opp Score: 14) AND Identity + Pride job (Opp Score: 15). The single biggest retention driver in the product.
- **Confidence:** 80% — No direct market comp exists; validated by analogy (Spotify Wrapped engagement, Duolingo streak milestones). Founder intuition is strong here.
- **Effort:** ~7.5 weeks — Summary UI, data aggregation (Pomodoros, tasks, breaks, streak), beautiful card design, share functionality.
- **RICE Score:** (700 × 3.0 × 0.8) / 7.5 = **224**
- **Goal alignment:** ✅ Core differentiator. Ships in v1.

> 🏆 **No competitor has this.** This is FocusFlow's most defensible feature. Every design dollar spent here is a moat dollar.

---

### #5: Break Lock Mode *(Score: 210)*

- **Reach:** 700/1000 — Users who use Pomodoro will hit breaks; engaged users will activate Break Lock.
- **Impact:** 3.0× — Directly addresses Break Enforcement job (Opp Score: 14). Only tool in the category with this feature.
- **Confidence:** 80% — Founder-validated; behavioral data (doom-scrolling during breaks is well-documented). No comp to validate against.
- **Effort:** ~7 weeks — Full-screen takeover, timer countdown, ambient scene + audio, smooth transition back to focus mode.
- **RICE Score:** (700 × 3.0 × 0.8) / 7 = **240** *(updated — shipping it slightly lower risk)*
- **Goal alignment:** ✅ Core differentiator. Ships in v1.

---

### #6: Sticky Note Task Tracker *(Score: 200)*

- **Reach:** 800/1000 — Most users want to track tasks; sticky notes are the most intuitive UX.
- **Impact:** 2.0× — Addresses the task visibility job (Opp Score: 11). Important but not as differentiated — Lofi.co has notes; Flocus has a to-do list.
- **Confidence:** 75% — Task tracking is universal; the *draggable sticky note on canvas* format is unvalidated.
- **Effort:** ~6 weeks — Drag-and-drop canvas layer, add/check/delete tasks, persistence via account, styled to match scene aesthetic.
- **RICE Score:** (800 × 2.0 × 0.75) / 6 = **200**
- **Goal alignment:** ✅ Ships in v1. Differentiator is the aesthetic integration and drag-to-anywhere placement.

> ⚠️ **Scope risk:** If the draggable canvas proves technically complex, ship a fixed-position note panel first; iterate on drag behavior in v1.1.

---

### #7: Time-of-Day Scene Variants *(Score: 120)*

- **Reach:** 600/1000 — Not all users will notice or use time-of-day variants; power users and design-appreciators will.
- **Impact:** 2.0× — Directly serves the Escape job (Opp Score: 15). The "living workspace" experience is a major differentiator.
- **Confidence:** 75% — No direct comp validates this; inferred from user behavior (Lofi Girl users describe feeling "taken somewhere").
- **Effort:** ~10 weeks — 3 additional scene variants per scene = 9 more art assets. This is the highest-effort single feature.
- **RICE Score:** (600 × 2.0 × 0.75) / 10 = **90**

> 📅 **Recommendation:** Ship 2 time-of-day variants at launch (morning + sunset — the most visually dramatic pair). Ship noon + night in v1.1 to avoid delaying the launch. This preserves the differentiator while managing scope.

---

### #8: Streaks System *(Score: 180)*

- **Reach:** 600/1000 — Return users who care about habit-building.
- **Impact:** 2.0× — Retention driver; Identity job (Opp Score: 15 for the identity layer).
- **Confidence:** 75% — Forest, StudyStream, Duolingo all validate streak effectiveness.
- **Effort:** ~4 weeks — Daily completion logic, streak counter UI in header, streak shield mechanic, reset handling.
- **RICE Score:** (600 × 2.0 × 0.75) / 4 = **225**
- **Goal alignment:** ✅ Ships in v1. Lightweight implementation; high retention ROI.

---

### #9: User Auth (Sign up / Login) *(Score: 360 — enabler, not feature)*

- **Reach:** 600/1000 — Core users who want persistence (streaks, tasks, history).
- **Impact:** 3.0× — Enables streaks, end-of-day history, sticky note persistence, and achievements. Without auth, the stateful features have no home.
- **Confidence:** 100% — Technical necessity, not a product bet.
- **Effort:** ~5 weeks — Email + password + Google SSO (Supabase/Firebase Auth). Standard implementation.
- **Goal alignment:** ✅ Must ship in v1 to unlock half the product's value. Build early in the sprint.

---

### #10: Achievement Badges *(Score: 90)*

- **Reach:** 500/1000 — Engaged users who care about milestones.
- **Impact:** 1.0× — Serves Identity job but less immediately than streaks or end-of-day ritual.
- **Confidence:** 60% — Forest and StudyStream validate the concept; the aspirational *theming* of FocusFlow's badges is unvalidated.
- **Effort:** ~5 weeks — Badge design system, unlock logic, profile display, notification on unlock.
- **RICE Score:** (500 × 1.0 × 0.6) / 5 = **60** *(actual)*

> 📅 **Recommendation:** Ship 5–6 core badges in v1 (First Flame, 7-day streak, 30-day streak, 50 tasks). Full badge library ships in v1.1. The unlock logic reuses streak infrastructure.

---

### Quick Wins (low effort, good impact)

**Audio Volume Controls** — 2 weeks, affects 90% of users, creates satisfaction. Ship it.
**Pomodoro Customization (duration settings)** — 2 weeks, power user delight. Ship it.
**Shareable End-of-Day Card** — 3 weeks, directly drives organic acquisition via social. Ship it in v1.

---

## Value/Effort Matrix

```
High Value  │  QUICK WINS          │  BIG BETS
            │                      │
            │  • Pomodoro Timer    │  • Ambient Scenes (3)
            │  • User Auth         │  • Audio Layer
            │  • Streaks           │  • End-of-Day Summary
            │  • Audio Controls    │  • Break Lock Mode
            │  • Pomodoro Customs  │  • Sticky Notes
            │                      │  • Shareable Card
            │                      │  • Time-of-Day Variants*
────────────┼──────────────────────┼────────────────────────
            │  FILL-INS            │  AVOID (for now)
Low Value   │                      │
            │  • Session History   │  • Multiplayer / Social
            │  • User Profile      │  • Mobile Version
            │  • Spotify Integr.   │  • Full badge library
            │                      │
            └──────────────────────┴────────────────────────
              Low Effort              High Effort

* Time-of-Day: ship 2 variants (morning/sunset) in v1 as Quick Win; full 4 variants in v1.1
```

---

## Sensitivity Analysis

| If this changes... | Then ranking shifts... |
|-------------------|------------------------|
| Scene assets take 3× longer (30 wks) | Scenes drop to v1 with 1 scene only; 2 more ship in v1.1 |
| Audio licensing proves expensive (>$2K/mo) | Drop to royalty-free only at launch; feature the limitation as "curated" |
| Drag-and-drop sticky notes are technically complex | Ship fixed-panel notes in v1; draggable in v1.1 |
| End-of-day card doesn't generate shares organically | Deprioritize shareable card; invest in push/email nudges instead |
| Time-of-day variants land with users in beta | Accelerate full 4-variant rollout; make it hero feature in marketing |
| Auth introduces drop-off at onboarding | Delay auth requirement; let anonymous users try core before sign-up wall |

---

## Recommendations

### ✅ Do Now (v1 Launch Scope)
1. **User Auth** — Enables everything else. Build week 1.
2. **Pomodoro Timer** — Fastest high-value feature. Parallelizes with scene development.
3. **Ambient Scenes × 3** — With morning + sunset variants per scene. This is the product.
4. **Audio Layer** — Ship alongside scenes. One-click preset pairing.
5. **Break Lock Mode** — Your category-first feature. Ships as a differentiator, not an afterthought.
6. **End-of-Day Summary + Shareable Card** — Your retention + growth engine. Ship it.
7. **Sticky Note Task Tracker** — Table stakes. Ship fixed-panel first; drag-to-anywhere in v1.1.
8. **Streaks** — 4-week build, major retention impact.
9. **Audio Volume Controls + Pomodoro Duration Settings** — 2-week quick wins. Ship them.
10. **5–6 Core Achievement Badges** — Lightweight, high-emotional-value. Ship with streaks.

### 📅 Do Next (v1.1, 2–3 months post-launch)
- Full time-of-day variants (noon + night) for all scenes
- 3 additional scenes (expanding scene library to 6)
- Full achievement badge library
- Session history and past summaries in profile
- Spotify / streaming platform integration (pending licensing)

### 📈 Quick Wins to Add Alongside v1
- Shareable end-of-day card (3 weeks, massive organic growth potential)
- Streak shield mechanic (reduce churn from streak anxiety)
- "Welcome back" transition animation when returning from break

### ❌ Defer (Not v1, Requires Validation First)
- **Multiplayer / Social Body Doubling** — Fundamentally different product. Validate demand before considering (≥6 months post-launch).
- **Mobile Version** — Desktop-first by design. Mobile dilutes the second-screen positioning. Re-evaluate at 6 months.
- **AI-adaptive audio** — Strong future moat (Endel model applied to FocusFlow's world), but only after visual + ritual layer is proven.

---

## Assumptions to Validate

- ⚠️ **Audio licensing cost** — Need to resolve royalty-free vs. licensed before sprint 1. Budget unclear.
- ⚠️ **Scene asset timeline** — 3 scenes × 2 time-of-day variants = 6 unique art assets. Requires a dedicated visual designer or artist. Confirm timeline.
- ⚠️ **Sticky note drag UX** — Test a paper prototype with 5 users before committing full engineering effort to drag-and-drop.
- ⚠️ **End-of-day card sharing** — Assumption that users will share organically. Add a "Share" button but don't make it primary CTA until validated.
- ⚠️ **Anonymous vs. auth-gated** — Test whether requiring sign-up before using core features kills activation. Consider an anonymous "try it" mode.

## Data Gaps

- [ ] Engineering effort estimates needed — all E values are PM estimates, not engineering-confirmed
- [ ] Confirm audio licensing approach and monthly cost
- [ ] User interviews to validate: do users want manual time-of-day control or auto-sync to real clock?
- [ ] Beta data needed: what % of users actually clock out each day?

---

*Generated by Prioritization Engine skill · FocusFlow v1 roadmap · 2026-04-16*
