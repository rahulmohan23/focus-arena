# PRD: FocusFlow — Ambient Productivity Companion

**Status:** Draft
**Owner:** Rahul Mohan
**Last Updated:** 2026-04-16
**Target Release:** TBD
**Availability:** Free tier (core features) + Pro tier (advanced scenes, full achievements, analytics history)
**Rationale:** Freemium drives adoption; Pro unlocks the habit-forming and data layers that power-users pay for.

---

## Context

*What I know from your description:*

- **Roadmap:** Brand new product — not iterating on anything existing.
- **Persona pain:** Users with extended/dual-monitor setups have an underused second screen that currently adds distraction rather than focus. The user (and likely others) have personally validated that lo-fi music, calming ambient visuals, Pomodoro timing, and body-doubling cues meaningfully improve their own focus and output.
- **Strategic fit:** Combines five proven productivity techniques (ambient music, body-doubling, Pomodoro, task management, streak rewards) into a single cohesive second-screen experience — rather than cobbling together YouTube, Toggl, a timer app, and sticky notes.
- **Competitive landscape:** ⚠️ *Assumed* — Tools like Lofi.cafe, Focus@Will, Forest, and Notion exist but none combine ambient visual scenes + Pomodoro + sticky-note tasks + streaks + end-of-day insights in one screen-takeover experience. This is a meaningful white space.

---

## Problem

Knowledge workers and students with dual monitors use their second screen as an afterthought — another browser window, social media overflow, or just wallpaper. This is a missed opportunity: research on body-doubling, ambient noise, and time-boxing consistently shows these environmental cues significantly improve sustained focus and task completion.

There is no single, beautifully designed tool that occupies that second screen with purpose — combining calming visuals, ambient audio, task tracking, a Pomodoro timer, break enforcement, and end-of-day reflection in one place.

**Who has this problem:** All users — students, remote workers, freelancers, creators — who regularly sit at a desk with an extended display and struggle to maintain deep focus sessions.

---

## Evidence

- ✅ **Validated (personal):** Rahul has personally observed higher productivity when combining lo-fi music, calming visuals, and Pomodoro timing.
- ✅ **Validated (science):** Body-doubling is a documented focus technique, particularly studied in ADHD research (Virtual Body Doubling has grown significantly post-COVID). Pomodoro Technique has decades of adoption data.
- ✅ **Validated (proxy):** Lofi Girl's YouTube stream consistently attracts 20,000–30,000 concurrent viewers — a strong signal of demand for ambient focus audio+visual experiences.
- ⚠️ **Assumed:** Dual-monitor adoption is high enough among the target demographic (knowledge workers) to represent a meaningful addressable audience.
- ⚠️ **Assumed:** Users will prefer an all-in-one experience over their current patchwork of tools (needs validation via user interviews).

---

## Success Criteria

### Lagging Indicators (post-launch outcomes)

| Metric | Current | Target | Timeframe |
|--------|---------|--------|-----------|
| Daily Active Users (DAU) | 0 | 1,000 | 3 months post-launch |
| D7 Retention | 0 | 35% | 3 months post-launch |
| Average session length | 0 | ≥ 45 min | 3 months post-launch |
| Pro tier conversion | 0 | 5% of MAU | 6 months post-launch |
| Streak ≥ 7 days maintained | 0 | 20% of active users | 3 months post-launch |

> 💡 All baselines are `[PLACEHOLDER — need actual baseline post-launch]`

### Leading Indicators (pre-launch signals)

| Metric | Target | What This Predicts |
|--------|--------|--------------------|
| Beta user Pomodoro completion rate | ≥ 60% sessions fully completed | Predicts D7 retention |
| Avg tasks added per session in beta | ≥ 2 sticky note tasks | Predicts daily habit formation |
| Beta support tickets on audio/visual | < 5% of sessions | Predicts quality at scale |
| Time-to-first-Pomodoro (onboarding) | < 90 seconds | Predicts activation rate |

> 💡 Leading indicators help you course-correct before launch.

---

## Proposed Solution

### How It Works

FocusFlow is a full-screen ambient productivity app designed for a second monitor. When a user opens it, they're immediately placed inside a beautifully rendered scene — a highway at sunset, a mountain café, a New Zealand waterfront — with lo-fi or white noise audio playing softly underneath. A minimal floating UI lets them:

1. **Pick and customize their scene** (location + time of day)
2. **Start a Pomodoro timer** that nudges them silently when done
3. **Track tasks** with draggable sticky notes on the canvas
4. **Take a structured break** with a full-screen break mode
5. **End the day** with a generated insights card
6. **Earn achievements** via streaks and focus milestones

Everything lives on one screen. No switching apps.

---

### Feature Breakdown

#### 🌅 Ambient Scenes
Six hand-crafted scenes, each with 4 time-of-day variants:

| Scene | Morning | Noon | Sunset | Night |
|-------|---------|------|--------|-------|
| Highway Drive | Morning mist, low sun | Bright highway | Golden hour drive | City lights, dark sky |
| Café | Opening, few people | Busy lunch rush | Warm afternoon light | Evening ambience |
| Mountain Retreat | Sunrise peaks | Clear sky | Alpenglow | Stars, campfire glow |
| New Zealand Waters | Calm misty lake | Bright open water | Pink reflections | Moonlit water |
| Taj Mahal Garden | Dawn light | High sun, tourists | Deep orange glow | Floodlit monument |
| Desert Campfire | Cold blue dawn | Heat haze | Ember sunset | Full fire, dark sky |

Visuals use **minimal motion** (subtle parallax, gentle particle effects — no jarring animation). Time-of-day can be set manually or synced to the user's local clock.

#### 🎵 Audio Layer
- **Lo-fi music:** Soft lo-fi hip-hop, jazz lo-fi, ambient piano (curated playlists)
- **White noise options:** Café chatter, rain, fireplace crackle, flowing water, train carriage
- Users can mix music + noise, or use one only
- Independent volume sliders for music and ambient noise

#### 📝 Sticky Note Task Tracker
- Floating sticky notes the user can drag anywhere on the canvas
- Add a task (text input), check it off, delete it
- Notes persist across sessions (tied to account)
- Color variants for organization (optional)
- Notes stay "in scene" — styled to feel part of the environment

#### ⏱️ Pomodoro Timer
- Default: 25 min work / 5 min short break / 15 min long break (after 4 cycles)
- User can customize durations in settings
- Start / Pause / Reset controls
- On completion: silent screen flash + soft chime (non-disruptive)
- Timer visible as a minimal floating element in the corner

#### ☕ Break Mode
- Triggered manually ("Take a Break") or automatically at Pomodoro break time
- User sets break duration (or accepts the Pomodoro default)
- Full-screen takeover with soft ambient BG and music
- "Break is over" prompt with smooth transition back to focus mode
- Break time logged for end-of-day summary

#### 🏆 Achievements & Streaks
- **Daily streak:** Complete ≥ 1 Pomodoro per day to maintain streak
- **Milestone achievements** themed around self-motivation:
  - *"First Flame"* — Complete your first Pomodoro
  - *"Deep Diver"* — 90 uninterrupted focus minutes
  - *"Mountain Mind"* — 7-day streak
  - *"Summit Seeker"* — 30-day streak
  - *"Task Terminator"* — Complete 50 tasks total
  - *"Wanderer"* — Use all 6 scenes
  - *(and more to be designed with a reward designer)*
- Achievements displayed on profile as collectible badges
- Streak counter visible in the header at all times

#### 📊 End-of-Day Summary ("Clock Out")
- CTA in the header: **"End My Day"**
- Generates a beautiful full-screen summary card showing:
  - Total focus time
  - Pomodoros completed (with a visual ring/chart)
  - Tasks added vs. tasks completed
  - Breaks taken + total break time
  - Streak status
  - A motivational quote tied to the day's performance
- Summary is shareable (screenshot-friendly card layout)
- History stored on account (view past days in profile)

#### 👤 User Account
- Sign up / log in (email + password, Google SSO)
- Profile page: display name, avatar, joined date
- Account settings: email, password, notification preferences
- Streak and achievement history
- Session history (past end-of-day summaries)

---

### User Stories

**Story 1 — The Late Afternoon Worker**
- **As a** remote software engineer with a dual-monitor setup,
- **I want to** open FocusFlow on my second screen, pick the "Café at Sunset" scene, and start a 25-minute Pomodoro,
- **So that** I can stay in a focused headspace during my last deep-work block of the day without being distracted by other browser tabs.

**Story 2 — The Structured Task Tracker**
- **As a** freelance designer starting my morning,
- **I want to** drag sticky notes onto my scene and list out my 3 tasks for the day, checking them off as I go,
- **So that** I always have my to-dos visible without needing to open a separate task app.

**Story 3 — The Streak Chaser**
- **As a** student who struggles with consistency,
- **I want to** see my daily streak counter grow and unlock the "Mountain Mind" badge after 7 days,
- **So that** I feel genuinely rewarded for showing up consistently — not just for finishing tasks.

**Story 4 — The Intentional Break-Taker**
- **As a** remote worker prone to skipping breaks,
- **I want to** click "Take a Break" and have the screen lock me into a 10-minute break mode with calming audio,
- **So that** I'm actually forced to step away rather than just minimizing the timer.

---

## Non-Goals

- **Not a full task management system** — No subtasks, due dates, priority labels, or project hierarchies. This is a lightweight sticky-note layer, not a replacement for Notion or Todoist.
- **Not a music streaming app** — Audio is curated background tracks, not a personal library or playlist builder.
- **Not a screen time monitor** — No surveillance of what the user does outside FocusFlow.
- **Not mobile-first** — Designed specifically for desktop/extended screen use. Mobile may come later but is out of scope for v1.
- **Not a social/team app** — No multiplayer body-doubling rooms, shared sessions, or social feeds in v1.
- **Not a video background** — Visuals are high-quality illustrated/rendered scenes with subtle motion, not live video streams.

---

## Dependencies

### Feature Dependencies
- **Authentication system** (Google SSO + email/password): Required before account features, streak tracking, or data persistence can ship.
- **Data persistence layer** (user sessions, tasks, streaks): Required for sticky notes, streaks, and end-of-day history to be meaningful.
- **Asset pipeline for scenes**: All 6 scenes × 4 time-of-day variants = 24 visual assets needed before launch. This is the highest-effort creative dependency.
- **Audio licensing/hosting**: Lo-fi tracks and white noise must be either licensed, royalty-free, or self-hosted before launch.

### Team Dependencies
- **Visual/Motion Designer**: Scene creation and time-of-day variants (likely the critical path item).
- **Audio Curator / Licensing**: Sourcing and clearing lo-fi and ambient audio tracks.

### External Dependencies
- **Authentication provider** (e.g., Firebase Auth, Auth0, Supabase): Low risk, well-trodden.
- **Audio CDN**: For streaming ambient tracks without performance issues.
- **Analytics platform** (e.g., PostHog, Mixpanel): For tracking session lengths, Pomodoro completions, DAU, and retention.

**Critical Path:** Scene asset creation. If the visual assets aren't ready, the core product has no soul. Everything else (timer, sticky notes, auth) can be built in parallel — but scenes must start immediately.

---

## Risks

| Risk | Type | Impact | Mitigation |
|------|------|--------|------------|
| Visual assets take longer than expected and delay launch | Feasibility | High | Start with 2–3 scenes at launch, expand post-launch |
| Audio licensing is expensive or complex | Viability | Medium | Prioritize royalty-free / CC sources; budget for licensing early |
| Users don't want an all-in-one tool — they prefer their existing setup | Value | High | Run 5 user interviews before building; validate with a no-code prototype |
| Second-screen use case is too niche to reach critical mass | Value | Medium | Test with productivity communities (Reddit r/productivity, Twitter/X) pre-launch |
| Users find minimal motion visuals boring vs. YouTube lo-fi | Usability | Medium | A/B test motion level in beta; offer a "more motion" toggle |
| Sticky notes feel clunky or get lost behind the visual | Usability | Medium | Prototype drag interaction early; test with 5 users before building |
| Streak pressure creates anxiety rather than motivation | Value | Low-Med | Make streaks opt-in; include a "streak shield" mechanic for off days |

---

## Open Questions

| Question | Assumption | How to Validate | Timeline |
|----------|-----------|-----------------|----------|
| Will users actually leave FocusFlow open on their second monitor all day, or open it just for Pomodoro sessions? | All-day ambient use | Session length data from beta + user interviews | Before v1 launch |
| Do users want manual time-of-day control or automatic clock-sync? | Manual preferred for intentionality | Quick survey in beta / settings toggle + usage data | Before launch |
| Should the Pomodoro timer be visible at all times, or hide when not running? | Always visible | Beta feedback | Sprint 1 |
| What is the right business model — ads on free tier, or pure freemium? | Ads-free freemium | Validate willingness to pay with landing page + waitlist | Pre-build |
| Does the achievement system need social proof (leaderboards, shareable badges) to drive engagement? | Private achievements are sufficient for v1 | Beta DAU and streak data | 4 weeks post-beta |

---

## Before Finalizing
- [ ] Validate the "all-in-one vs. current patchwork tools" assumption with 5 user interviews
- [ ] Confirm audio licensing approach and budget before scoping engineering
- [ ] Prototype at least 1 scene + timer interaction to test "does the canvas feel right?"
- [ ] Decide on launch scope: 2–3 scenes at launch vs. all 6
- [ ] Define what "Pro tier" unlocks specifically (suggested: extra scenes, full achievement history, analytics export, custom Pomodoro durations)

---

## Sign-off

| Role | Name | Approved |
|------|------|----------|
| Product | Rahul Mohan | ⬜ |
| Engineering | | ⬜ |
| Design | | ⬜ |

---

*Generated by PRD Generator skill · FocusFlow v0.1 · 2026-04-16*
