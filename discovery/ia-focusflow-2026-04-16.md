# Information Architecture: FocusFlow V1

**Date:** 2026-04-16
**Product:** FocusFlow — Ambient Second-Screen Productivity Companion
**Scope:** V1 web app (desktop-first) + marketing landing page

---

## Design Principles for IA

1. **Zero friction to first session** — A new user must reach a running ambient scene + Pomodoro timer in under 90 seconds from landing page.
2. **The canvas is king** — The ambient scene is the primary UI surface. Everything else floats on top of it minimally.
3. **Progressive disclosure** — Core tools (timer, tasks, audio) are always visible. Settings, profile, achievements are one layer deeper.
4. **Ritual over features** — The IA is designed around daily rituals (start session, break, end day) not around feature categories.
5. **Second-screen native** — Controls are minimal, non-distracting, and designed to live at the edges of a wide display.

---

## Site Map

```
focusflow.app
│
├── / (Landing Page — Marketing)
│   ├── Hero: Live ambient scene preview + tagline
│   ├── Features: Scenes · Timer · Tasks · Break Lock · End-of-Day
│   ├── How It Works: 3-step visual walkthrough
│   ├── Personas: "For remote workers" / "For students" / "For creators"
│   ├── Scenes Preview: Gallery / carousel
│   ├── Achievements Preview: Badge showcase
│   ├── Social Proof: Shared end-of-day cards
│   ├── Pricing: Free vs. Pro
│   └── CTA: "Open FocusFlow" → /app
│
├── /app (Main Application — Desktop)
│   ├── [Scene Canvas] ← Full-screen ambient background
│   ├── Header Bar (always visible, minimal)
│   │   ├── Scene Selector
│   │   ├── Time-of-Day Toggle
│   │   ├── Streak Counter 🔥
│   │   ├── "End My Day" CTA
│   │   └── User Avatar → Profile Menu
│   ├── Audio Controls (floating panel, bottom-left)
│   │   ├── Music Toggle + Volume Slider
│   │   └── Noise Toggle + Volume Slider
│   ├── Pomodoro Timer (floating widget, bottom-center)
│   │   ├── Start / Pause / Reset
│   │   ├── Session type indicator (Focus / Short Break / Long Break)
│   │   └── Session counter (e.g., 3/4)
│   ├── Sticky Notes Canvas (draggable, anywhere on scene)
│   │   ├── Add Task Button (+ icon)
│   │   ├── Note Card: text · checkbox · delete
│   │   └── Notes persist across sessions
│   └── Break Lock Screen (full-screen overlay)
│       ├── Ambient Scene (same or softer variant)
│       ├── Break Countdown Timer
│       ├── Soft Audio
│       ├── "Skip Break" (escape hatch, unobtrusive)
│       └── "Welcome Back" transition → return to focus scene
│
├── /app/end-of-day (End-of-Day Summary)
│   ├── Summary Card (full-screen, beautiful)
│   │   ├── Focus Time Total
│   │   ├── Pomodoros Completed (visual ring chart)
│   │   ├── Tasks Added vs. Completed
│   │   ├── Breaks Taken + Duration
│   │   ├── Current Streak
│   │   ├── Personalized Message (persona-aware copy)
│   │   └── Achievement Unlocked? (if applicable)
│   ├── Share Button → generates image card
│   ├── "See Past Days" link → /app/profile#history
│   └── "See You Tomorrow" → closes and returns to home
│
├── /app/profile
│   ├── Profile Overview
│   │   ├── Name + Avatar
│   │   ├── Member Since
│   │   └── Current Streak + Best Streak
│   ├── Achievements Gallery
│   │   ├── Earned Badges (with unlock date)
│   │   └── Locked Badges (preview with progress)
│   ├── Session History (Pro)
│   │   ├── Calendar heatmap of activity
│   │   └── Past End-of-Day summaries (list)
│   └── Account Settings → /app/settings
│
├── /app/settings
│   ├── Pomodoro Durations
│   │   ├── Focus Session Length (default: 25 min)
│   │   ├── Short Break Length (default: 5 min)
│   │   └── Long Break Length (default: 15 min)
│   ├── Audio Preferences
│   │   ├── Default Music Genre
│   │   └── Default Noise Type
│   ├── Scene Preferences
│   │   ├── Default Scene
│   │   └── Time-of-Day: Auto-sync to clock vs. Manual
│   ├── Notifications
│   │   └── Pomodoro end sound: On/Off + Volume
│   └── Account
│       ├── Email / Password
│       ├── Connected accounts (Google)
│       └── Delete Account
│
├── /login
├── /signup
└── /forgot-password
```

---

## Screen-by-Screen Breakdown

---

### 1. Landing Page `/`

**Purpose:** Convert first-time visitors into app users. Communicate the second-screen value prop in under 10 seconds.

**Layout:**

```
┌─────────────────────────────────────────────────────────────┐
│  NAVBAR: Logo | Features | Pricing | Log In | [Open Free →] │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  HERO                                                       │
│  ┌─────────────────────────────────────────────────────┐   │
│  │  [Live ambient scene playing — autoplay, muted]      │   │
│  │                                                       │   │
│  │  "Your second screen,                                 │   │
│  │   finally doing something beautiful."                 │   │
│  │                                                       │   │
│  │         [Open FocusFlow Free →]                       │   │
│  │     No sign-up needed to start                        │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  FEATURES ROW (icon + headline + 1 line description)        │
│  🌅 6 Scenes  ⏱ Pomodoro  📝 Tasks  ☕ Break Lock  📊 Day End│
│                                                             │
│  SCENE GALLERY (scrollable carousel, 3 scenes shown)        │
│                                                             │
│  HOW IT WORKS (3 steps)                                     │
│  1. Pick your scene  2. Start your session  3. End your day │
│                                                             │
│  PERSONA SECTIONS (tab or scroll)                           │
│  For Remote Workers | For Students | For Creators           │
│                                                             │
│  SHARED CARDS WALL (real end-of-day cards, social proof)    │
│                                                             │
│  PRICING                                                    │
│  Free: Core features | Pro: $X/mo (extra scenes, history)   │
│                                                             │
│  FINAL CTA                                                  │
│  "Open your second screen →"                                │
│                                                             │
│  FOOTER: Links | Privacy | @focusflow                       │
└─────────────────────────────────────────────────────────────┘
```

**Key decisions:**
- Hero scene autoplays (muted) — no interaction required to feel the product
- Primary CTA is "Open FocusFlow Free" — no email gate at this step
- "No sign-up needed to start" removes friction objection immediately

---

### 2. Main App Canvas `/app`

**Purpose:** The daily workspace. Must feel clean, immersive, and non-distracting.

**Layout (wide 16:9 second-screen optimised):**

```
┌──────────────────────────────────────────────────────────────────────┐
│ HEADER BAR (semi-transparent, 40px tall)                             │
│ [🌅 Scene] [☀ Time] ─────────────────── [🔥 5] [End My Day] [👤]    │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│                                                                      │
│         [FULL-SCREEN AMBIENT SCENE — 80% of UI surface]              │
│                                                                      │
│                  [Draggable Sticky Notes float here]                 │
│                                                                      │
│                                                                      │
│                                                                      │
│                                                                      │
├──── AUDIO PANEL ────────────────── POMODORO TIMER ───────────────────┤
│ 🎵 Lo-fi ●──────○  25:00                                             │
│ ☁️ Rain  ●────────○  FOCUS · Session 1/4                             │
│                      [▶ Start]  [⏸ Pause]  [↩ Reset]                │
└──────────────────────────────────────────────────────────────────────┘
```

**Floating elements behaviour:**
- Header bar: always visible, minimal opacity when not hovered
- Audio controls: bottom-left floating panel, collapsible
- Pomodoro timer: bottom-center, always visible during session
- Sticky notes: draggable anywhere on the scene canvas
- Break prompt: appears as a soft overlay when timer ends

**Header elements:**
- **Scene Selector:** Click to expand a scene + time-of-day picker overlay
- **Time Toggle:** Sun icons cycling Morning → Noon → Sunset → Night (or "Auto" = clock-synced)
- **Streak Counter:** 🔥 N — hover shows "Your current streak. Complete 1 session/day to maintain."
- **End My Day:** Primary CTA — routes to `/app/end-of-day`
- **User Avatar:** Click opens profile quick-menu (Profile / Settings / Log Out)

---

### 3. Scene Selector (Overlay)

**Trigger:** Click on current scene name in header

**Layout:**

```
┌────────────────────────────────────┐
│  Choose Your Scene                 │
│                                    │
│  [Highway] [Café] [Mountain]       │
│  [NZ Waters] [Taj Mahal] [Desert]  │
│                                    │
│  Time of Day:                      │
│  [🌅 Morning] [☀ Noon] [🌇 Sunset] [🌙 Night]  or  [⏰ Auto] │
│                                    │
│  [Apply →]                         │
└────────────────────────────────────┘
```

Scene thumbnails show a small preview image for each time-of-day variant. Selected scene + time highlighted. Apply closes overlay and transitions scene (crossfade).

---

### 4. Sticky Note Component

**States:**
- **Empty canvas:** Faint "+ Add task" ghost note in corner, dismissible
- **Note card:** Small card with text, checkbox, delete (×) icon
- **Checked state:** Text struck through, card slightly faded
- **Dragging:** Note lifts with a subtle shadow

**Add Task flow:**
1. Click "+" button (bottom of canvas or floating action button)
2. New note appears in default position, text field auto-focused
3. Type task → Enter to save → note pins to canvas

---

### 5. Pomodoro Timer Component

**States:**
- **Idle (not started):** Displays default duration. [▶ Start] button prominent.
- **Running (Focus):** Countdown active. [⏸ Pause] visible. Subtle progress ring.
- **Running (Break):** Timer shows break duration. "Break" label. [Skip] escape hatch small.
- **Break Lock triggered:** Timer transitions to full-screen Break Lock overlay.
- **Completed:** Soft chime + screen flash. Prompt: *"Session complete. Take a break?"*

**Session progress indicator:** 4 dots below timer → filled as sessions complete → dot 4 complete = long break

---

### 6. Break Lock Screen (Full-Screen Overlay)

**Trigger:** Break Lock button clicked from break prompt

**Layout:**

```
┌──────────────────────────────────────────────────────────┐
│                                                          │
│         [AMBIENT SCENE — same or softer variant]         │
│                   with even slower motion                │
│                                                          │
│              ┌─────────────┐                             │
│              │  ☕ Break    │                             │
│              │  09:47      │                             │
│              │             │                             │
│              │ "Step away. │                             │
│              │  You earned │                             │
│              │  this."     │                             │
│              └─────────────┘                             │
│                                                          │
│                        [ Skip Break ]  (small, grey)    │
│                                                          │
└──────────────────────────────────────────────────────────┘
```

On break end: scene brightens, "Welcome back" fades in for 2 seconds, transitions smoothly back to focus mode.

---

### 7. End-of-Day Summary `/app/end-of-day`

**Trigger:** "End My Day" button in header

**Layout:**

```
┌──────────────────────────────────────────────────────────┐
│  [Scene-matched ambient background — muted, slow motion] │
│                                                          │
│          ┌──────────────────────────────────┐           │
│          │  Thursday, April 16              │           │
│          │                                  │           │
│          │  🕐 3h 45m    Total focus         │           │
│          │  🍅 6         Pomodoros           │           │
│          │  ✅ 8 / 10    Tasks done          │           │
│          │  ☕ 3         Real breaks         │           │
│          │  🔥 5-day streak                  │           │
│          │                                  │           │
│          │  ──────────────────────────────  │           │
│          │                                  │           │
│          │  "You showed up 5 days in a row. │           │
│          │   That's not a habit. That's     │           │
│          │   an identity."                  │           │
│          │                          — 🏔️    │           │
│          │  ──────────────────────────────  │           │
│          │                                  │           │
│          │  [📤 Share Today] [→ See Profile] │           │
│          └──────────────────────────────────┘           │
│                                                          │
│                  [ See you tomorrow →]                   │
└──────────────────────────────────────────────────────────┘
```

**Copy system:**
- Message varies based on streak length, tasks completed, and breaks taken
- Signed off with a scene-matched icon (🏔️ Mountain, 🌊 Water, 🔥 Campfire, 🚗 Highway)
- If break was skipped: *"Tomorrow, let the campfire hold you. Take your breaks."*

---

### 8. Profile Page `/app/profile`

**Layout:**

```
┌────────────────────────────────────────────────┐
│  [←] Profile                                   │
├──────────────────┬─────────────────────────────┤
│  👤 Avatar       │  Arjun M.                   │
│  [Edit]          │  Member since March 2026     │
│                  │  🔥 5 · Best: 12 days        │
├──────────────────┴─────────────────────────────┤
│  ACHIEVEMENTS                                  │
│  ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐          │
│  │ 🔥 │ │ 🏔️ │ │ 🔒 │ │ 🔒 │ │ 🔒 │          │
│  └────┘ └────┘ └────┘ └────┘ └────┘          │
│  Earned       Locked (tap to preview)          │
├────────────────────────────────────────────────┤
│  SESSION HISTORY  [Pro]                        │
│  [Calendar heatmap — green intensity = focus]  │
│  April 2026  ░░▒▒▒▓███▓▒░░░░░░░░░░             │
│                                                │
│  [ View Past Summaries ]                       │
└────────────────────────────────────────────────┘
```

---

### 9. Auth Screens `/login` `/signup`

**Design principle:** These should *feel* like the app — ambient scene background (muted, non-distracting), minimal form.

**Sign Up:**
- Name + Email + Password
- OR: Continue with Google
- Below: *"By signing up you get streaks, achievements, and your end-of-day history. Try the app first →"*

**Log In:**
- Email + Password
- OR: Continue with Google
- Forgot password link

**Onboarding (post-signup, first-time):**
1. *"What's your vibe?"* → Scene selection (picks default)
2. *"Set your Pomodoro rhythm"* → Duration picker (default 25/5)
3. *"You're ready. Start your first session →"*

---

## User Flow Diagrams

---

### Flow 1: New Visitor → First Session (Target: <90 seconds)

```
Landing Page
    │
    ▼
[Open FocusFlow Free →]
    │
    ▼
App Canvas (anonymous)
Scene auto-loads (time-matched)  ←── ≤2s load target
    │
    ▼
User picks audio preset (optional)
    │
    ▼
User adds 1–3 sticky note tasks (optional)
    │
    ▼
[▶ Start] Pomodoro
    │
    ▼
🎉 IN SESSION  ←── ≤90s from landing page click
```

---

### Flow 2: End-of-Day Ritual

```
In Session → Timer ends
    │
    ▼
Prompt: "All done for today? End your day."
    │
    ├──→ [Not Yet] → Continue session
    │
    ▼
[End My Day] → /app/end-of-day
    │
    ▼
Summary card animates in (2s)
    │
    ├──→ [Share] → image card generated → clipboard / Twitter
    ├──→ [See Profile] → /app/profile
    └──→ [See you tomorrow →] → returns to /app (scene dims)
```

---

### Flow 3: Break Lock

```
Pomodoro ends (work session)
    │
    ▼
Non-intrusive overlay: "Session complete 🍅"
"Take a 5-min break? [Lock Break] [Skip]"
    │
    ├──→ [Skip] → immediately starts next Pomodoro
    │
    ▼
[Lock Break] → Full-screen Break Lock
    │
    ▼
Countdown runs (ambient scene, soft audio)
    │
    ▼
Break ends → "Welcome back ✨" → crossfade to focus scene
    │
    ▼
New Pomodoro starts (or user clicks Start)
```

---

### Flow 4: Sign-Up Gate (Progressive)

```
Anonymous user using app
    │
    ▼
Trigger: user completes first Pomodoro
    │
    ▼
Soft prompt (banner, non-blocking):
"Great session! Sign up to save your streak 🔥"
[Sign Up Free] [Maybe Later]
    │
    ├──→ [Maybe Later] → continues as anonymous
    │                     (shown again after 3rd session)
    ▼
/signup → 3-step onboarding → back to /app
```

---

### Flow 5: Returning User (Daily Ritual)

```
Opens FocusFlow (bookmark / browser startup)
    │
    ▼
App loads:
- Scene auto-matches time of day
- Streak counter shows current streak
- Yesterday's incomplete tasks still on canvas
    │
    ▼
User reviews sticky notes, updates tasks
    │
    ▼
Starts Pomodoro → works
    │
    ▼
[Repeat: Pomodoro → Break Lock → Pomodoro]
    │
    ▼
End of day → End-of-Day ritual
    │
    ▼
Streak increments → "🔥 6 days"
```

---

## Navigation Model

**Global nav (header bar — always visible in app):**
- Scene selector | Time-of-day toggle | Streak | End My Day | Profile

**No sidebar, no tabs.** Everything is either on the canvas or accessible from the header. This is intentional — sidebars create visual noise that breaks immersion.

**Escape routes (for power users):**
- `Esc` key → dismisses any overlay (Break Lock, Scene Selector, End-of-Day)
- Profile menu → Settings / Profile / Log Out
- Keyboard shortcut reference (future): `Space` = start/pause timer, `B` = start break

---

## Content Hierarchy (Visual Priority)

```
Z-index / Visual Dominance:

1 (Bottom)   ── Ambient Scene (background — 100% canvas)
2            ── Sticky Notes (float on scene, semi-transparent border)
3            ── Audio Controls (bottom-left, low opacity)
4            ── Pomodoro Timer (bottom-center, slightly more prominent)
5            ── Header Bar (top, semi-transparent)
6            ── Scene Selector Overlay (when open)
7            ── Break Lock (full-screen, highest priority)
8 (Top)      ── End-of-Day Card (full-screen, highest priority)
```

The scene is always visible. UI elements are layered *on* the scene, not *replacing* it.

---

## Responsive Strategy

| Device | Experience |
|--------|-----------|
| **Desktop (1440px+)** | Full app experience — second-screen optimised |
| **Laptop (1024–1440px)** | Full app experience — single screen use |
| **Tablet (768–1024px)** | App works but not optimised — nudge to desktop |
| **Mobile (<768px)** | Marketing landing page only — "Open on desktop for full experience" |

The mobile landing page must be beautiful and convert visitors to desktop opens. A "Send to computer" email link or "Copy app link" CTA bridges the gap.

---

## V1 Page Inventory

| Page/Screen | Route | Auth Required | V1 |
|------------|-------|--------------|-----|
| Landing page | `/` | No | ✅ |
| Main app canvas | `/app` | No (anonymous) | ✅ |
| Scene selector overlay | (in `/app`) | No | ✅ |
| Break Lock screen | (in `/app`) | No | ✅ |
| End-of-Day summary | `/app/end-of-day` | Yes (for saving) | ✅ |
| Profile page | `/app/profile` | Yes | ✅ |
| Settings | `/app/settings` | Yes | ✅ |
| Log In | `/login` | No | ✅ |
| Sign Up + Onboarding | `/signup` | No | ✅ |
| Forgot Password | `/forgot-password` | No | ✅ |
| Session History detail | `/app/profile#history` | Yes + Pro | 📅 v1.1 |
| Achievement detail view | `/app/achievements` | Yes | 📅 v1.1 |

---

*Information Architecture · FocusFlow V1 · 2026-04-16*
