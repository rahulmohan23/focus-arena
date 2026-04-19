# Jobs-to-be-Done Analysis: FocusFlow

**Source:** Founder research + self-documented personal experience + competitive landscape signals + community behavior (Lofi Girl 20–30K concurrent viewers, StudyStream usage patterns, Focusmate ADHD community testimonials)
**Product Context:** FocusFlow — ambient second-screen productivity companion for knowledge workers and students

---

## Context

*What I found:*
- **Existing personas:** None in context files — inferred from founder description and market signals.
- **Known jobs:** Founder explicitly articulated: focus environment, lo-fi audio, body-doubling cue, Pomodoro timing, task tracking, break enforcement, end-of-day reflection, achievement/streak motivation.
- **Product positioning:** Second-screen ambient productivity tool for dual-monitor knowledge workers and students.

> ⚠️ Importance and satisfaction scores are estimated from research context (founder observation + market signals). Validate with quantitative survey before making hard prioritization decisions.

---

## Jobs Identified

*Opportunity Score = Importance + (Importance − Satisfaction). Higher = bigger opportunity.*

---

### Functional Jobs

| Job Statement | Imp | Sat | Opp | Evidence |
|--------------|-----|-----|-----|----------|
| When I sit down to work, I want to create an environment that signals "focus mode" to my brain, so I can transition quickly from distracted to deep work. | 9 | 4 | **14** | Lofi Girl stream (20–30K live viewers) proves users actively seek this cue. Founder validated personally. |
| When I have a task list for the day, I want to keep it visible without switching apps, so I can stay on track without context-switching. | 8 | 5 | **11** | Users open Notion/sticky notes alongside timers — fragmented workflow evidence. |
| When I'm working, I want to time my focus sessions and take structured breaks, so I can sustain energy across a full workday. | 9 | 6 | **12** | Pomodoro apps have millions of downloads; built-in need. |
| When I've had a productive day, I want to see a clear summary of what I accomplished, so I can feel a sense of closure and measure my progress over time. | 8 | 2 | **14** | No tool in the category offers end-of-day summaries — massive unmet need. |
| When I take a break, I want something to guide the break and pull me away from screens intentionally, so I actually rest instead of opening Twitter. | 8 | 2 | **14** | Widespread awareness of "doom scrolling during breaks" — users explicitly fail at this. |
| When I want to track my consistency, I want to see a streak of how many days I've shown up, so I can build the habit of deep work over time. | 7 | 4 | **10** | StudyStream leaderboards and Forest streaks show strong demand signal. |

---

### Emotional Jobs

| Job Statement | Imp | Sat | Opp | Evidence |
|--------------|-----|-----|-----|----------|
| When I sit at my desk, I want to feel calm and collected (not stressed or scattered), so I can do my best thinking without anxiety. | 10 | 3 | **17** | Core reason people seek lo-fi music — mood regulation, not just background noise. Endel's entire value prop is here. |
| When I'm grinding through a hard project, I want to feel like I'm somewhere beautiful, so I can maintain a sense of wonder and not feel trapped at a desk. | 9 | 3 | **15** | Founder cited: highway sunset, NZ waterfront, mountain, café — escape destinations, not just wallpapers. This is escapism as productivity fuel. |
| When I finish a long work session, I want to feel proud and rewarded for showing up, so I can build a positive relationship with hard work instead of dreading it. | 9 | 3 | **15** | Achievement systems in Forest, StudyStream, and Duolingo all validate this emotional job. |
| When I struggle to start working, I want to feel like someone is "there" with me, so I don't feel so alone in the grind. | 8 | 5 | **11** | Focusmate's entire model proves this job — webcam body-doubling has 100K+ active users. FocusFlow's ambient "people in scene" visuals address a lighter version of this. |
| When I hit a focus streak, I want to feel like I'm building an identity ("I'm someone who does deep work"), so my self-image reinforces the habit. | 8 | 3 | **13** | Duolingo's identity-based streaks ("I'm a language learner") proven model. Aspiration-themed achievements directly serve this. |
| When I take a break, I want to feel genuinely refreshed (not guilty), so I can return to work with more energy. | 7 | 3 | **11** | Break Lock concept addresses this — users feel guilt for unstructured breaks, which reduces productivity. |

---

### Social Jobs

| Job Statement | Imp | Sat | Opp | Evidence |
|--------------|-----|-----|-----|----------|
| When I share my setup or work session online, I want my workspace to look beautiful and intentional, so I can be seen as someone who takes their craft seriously. | 7 | 4 | **10** | "Desk setup" and "study with me" content is enormous on TikTok, YouTube, Instagram. End-of-day summary card is a shareable artifact. |
| When I complete a focus milestone, I want something shareable to show my streak or achievement, so I can signal discipline and inspire others. | 6 | 3 | **9** | Duolingo streak sharing, Forest's tree-sharing features validate this social job. |
| When I'm part of a team or community, I want to be seen as the person who shows up consistently, so I can earn respect and accountability from my peers. | 6 | 4 | **8** | Focusmate's "favourite partner" feature and StudyStream leaderboards validate this — less relevant for v1 FocusFlow (solo tool). |

---

## Top Opportunities Ranked

### 1. 🧠 The Mood Regulation Job — *Opp Score: 17*
**Job:** When I sit at my desk, I want to feel calm and collected (not stressed or scattered), so I can do my best thinking without anxiety.

**Why Underserved:** Spotify and YouTube serve this partially but with friction (ads, recommendations, rabbit holes). Dedicated ambient tools (Endel) exist but are audio-only or lack visual depth.

**Desired Outcomes:**
- Immediate physiological shift within 30 seconds of opening the app
- Sustained calm for 45–90 minute sessions without interruption
- No decision fatigue from choosing what to play/watch

**Solution Space:** High-quality cinematic scenes with carefully tuned default audio. Scene + sound pairings that feel matched and intentional. One-click "start session" that puts the environment up instantly.

**FocusFlow bet:** Scene + audio presets that launch in one click. No configuration needed.

---

### 2. 🌅 The Escape Job — *Opp Score: 15*
**Job:** When I'm grinding through a hard project, I want to feel like I'm somewhere beautiful, so I can maintain a sense of wonder and not feel trapped at a desk.

**Why Underserved:** Lofi Girl's YouTube stream (the most direct analog) only has one scene and no interactivity. Lofi.co has 40+ scenes but no time-of-day transitions — they feel static.

**Desired Outcomes:**
- Scenes change organically with time of day (sunrise feels like sunrise)
- Visual quality is cinematic — not stock footage or illustration
- The "place" feels real enough to mentally transport the user

**Solution Space:** Time-of-day scene variants that sync to real clock. Scene selection that matches mood/intention (energizing vs. calming). Short, looping animations with high production quality.

**FocusFlow bet:** This is your most differentiable visual feature. It must be executed at film-quality.

---

### 3. 🏆 The Identity + Pride Job — *Opp Score: 15*
**Job:** When I finish a long work session, I want to feel proud and rewarded for showing up, so I can build a positive relationship with hard work instead of dreading it.

**Why Underserved:** Most tools offer stats (numbers) but not *narrative*. A Pomodoro count is data; "You completed 6 deep sessions and hit a 5-day streak — you're a Summit Seeker" is identity.

**Desired Outcomes:**
- Daily sense of accomplishment (not just a number)
- Aspirational badge/achievement that feels earned, not gamified for its own sake
- End-of-day moment that creates positive reinforcement for the next morning's return

**Solution Space:** End-of-day summary card with beautiful data visualization. Aspirational achievement themes tied to the visual world (travel, nature, exploration). Streaks with streak-shields to reduce anxiety.

**FocusFlow bet:** The End-of-Day clock-out ritual is your retention engine. It must feel like a gift, not a report.

---

### 4. ☕ The Break Enforcement Job — *Opp Score: 14*
**Job:** When I take a break, I want something to guide the break and pull me away from screens intentionally, so I actually rest instead of opening Twitter.

**Why Underserved:** Nobody in the category has solved this. Forest punishes you for leaving the app. Pomodoro timers beep at you. Neither actually locks you into a break.

**Desired Outcomes:**
- Full-screen takeover that makes it *harder* to go back to work
- Break feels like a mini-vacation, not a countdown
- Return to work feels fresh, not interrupted

**Solution Space:** Break Lock mode with full-screen ambient scene + gentle audio. Countdown visible but not aggressive. "Welcome back" transition that feels like returning from somewhere beautiful.

**FocusFlow bet:** This is a feature nobody has. Own it.

---

### 5. 📋 The End-of-Day Closure Job — *Opp Score: 14*
**Job:** When I've had a productive day, I want to see a clear summary of what I accomplished, so I can feel a sense of closure and measure my progress over time.

**Why Underserved:** Tools track stats but don't *surface them as a ritual*. Toggl and RescueTime have reports, but nobody wraps them in an emotionally resonant end-of-day moment.

**Desired Outcomes:**
- One beautiful screen that summarizes the day in under 30 seconds
- Data feels celebratory, not clinical
- Summary is shareable as a "proof of work" artifact

**Solution Space:** Clock-Out button that generates a stunning summary card. Metrics: focus time, Pomodoros, tasks done, breaks taken, streak status. Shareable image format for social/community proof.

**FocusFlow bet:** Make this card so beautiful that users screenshot it organically. That's your acquisition flywheel.

---

## Feature Request Translation

| What Users Say / Do | The Real Job Behind It |
|---------------------|------------------------|
| "I play Lofi Girl on my second monitor" | "I need a focus cue + escape signal, not just music" |
| "I have 5 apps open for one focus session" | "I want one intentional workspace, not a fragmented setup" |
| "I can't take breaks properly" | "I need someone/something to enforce the break for me" |
| "I always forget what I accomplished today" | "I need a daily ritual that gives me closure and pride" |
| "I love Forest but it's too simple" | "I want gamification that builds identity, not just a timer" |
| "I can't start working in the morning" | "I need an environmental trigger that signals 'work mode' begins now" |
| "My second screen is wasted space" | "I want that surface to be doing something useful + beautiful" |

---

## Personas Implied by JTBD

Three distinct users emerge from the job analysis:

**Persona 1 — "The Desk-Bound Professional"**
Knowledge worker, dual monitor setup, remote or hybrid. Struggles with mood management and the work/rest boundary. Needs FocusFlow as their "second screen ritual companion." Values: aesthetics, calm, daily closure.

**Persona 2 — "The Focused Student"**
University or self-study. Single or dual screen. Pomodoro-native. Motivated by streaks and community proof. Needs FocusFlow as their "study space that travels." Values: identity, streaks, beautiful environments.

**Persona 3 — "The Burnout-Aware Creator"**
Freelancer or creative. Aware of their own tendency to overwork or under-rest. Specifically seeking break enforcement and intentional work rhythms. Needs FocusFlow as their "self-care productivity tool." Values: break structure, wellness framing, end-of-day ritual.

---

## Recommendations

1. **Lead with the Escape + Mood jobs** — These have the highest opportunity scores and map directly to scene quality and audio design. Every design decision should ask "does this make users feel transported?"

2. **Design the End-of-Day card as a marketing artifact** — Make it so visually beautiful that users want to share it. This is your organic acquisition loop.

3. **Brand Break Lock as wellness, not restriction** — Position it as "a real break" not "a forced pause." The ADHD and burnout-prevention communities will champion this if the language is right.

4. **Validate the Identity job quantitatively** — Survey 50 target users: "On a scale of 1–10, how important is it that your productivity tool makes you feel like 'someone who does deep work'?" If >7 average, double down on aspirational achievement themes.

5. **Don't skip the Social job** — Even in v1, a shareable end-of-day card serves the social job passively. This is low-effort, high-signal for growth.

---

## Suggested Next Steps
- [ ] Conduct 5–8 user interviews across the three personas to validate importance/satisfaction scores
- [ ] Add these personas to a `context/personas.md` file to inform future feature decisions
- [ ] Validate: "Does the identity job drive return visits more than the functional job?" (cohort analysis after beta)
- [ ] Quantitative survey: importance + satisfaction for top 5 jobs (100 respondents, Typeform)

---

⚠️ **Note:** All importance and satisfaction scores are inferred from market behavior, competitor signals, and founder-reported personal experience. Validate with primary user research before committing large engineering investment.

*Generated by JTBD Extractor · FocusFlow discovery · 2026-04-16*
