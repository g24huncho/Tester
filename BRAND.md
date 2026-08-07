# DP Combat — Brand Identity

> **Train smarter. Fight better.**

DP Combat is a serious fighter's tool. Not a game. Not childish. Every screen,
sound and word should feel like walking into a professional gym: dark, focused,
earned.

## Core values

| Value | How it shows up |
|---|---|
| **Discipline** | Restrained UI. Few options on screen. Nothing decorative without purpose. |
| **Performance** | Fast, responsive, zero friction between the fighter and the work. |
| **Progression** | The app reveals depth as the fighter earns it — never all at once. |

## The opening experience

First impressions are emotional, not informational. The app never opens on a menu.

**Sequence** (~5 seconds, always skippable):

1. **Dark.** The screen begins near-black — the gym before the lights.
2. **Spotlight.** A single warm overhead beam fades in. Dust motes drift through it.
3. **Impact.** A punch lands: white flash, shockwave ring, camera shake, deep thump.
4. **Reveal.** The DP Combat mark appears — polished championship metal.
5. **Sweep.** Light travels across the logo like a hand wiping a belt clean.
6. **Settle.** The mark locks in. Tagline fades up. *Enter the gym.*

Rules:
- A visible **Skip** control from frame one.
- `prefers-reduced-motion` bypasses the cinema entirely — straight to home.
- The bell rings on *entry* (a user gesture), never on autoplay.

## Visual language

**Palette** — the gym after hours, under one tungsten lamp:

| Token | Hex | Use |
|---|---|---|
| Black / coal / smoke | `#080606` / `#0e0b0a` / `#17120f` | The room. Warm-cast, never neutral grey. |
| Bone / dust | `#ede5d8` / `#9a8d7c` | Copy under tungsten light |
| Brass | `#9b7a2e` → `#c9a24a` → `#ecd28c` | The Corner, championship metal, readiness |
| Red | `#b3140e` → `#e8271f` → `#ff5a45` | The logo's D. One job: the "go" action. |
| Leather | `#2a130d` → `#7c3f28` | The bag. Material, not UI chrome. |

Every metal is a gradient ramp with a travelling sheen; every background carries
light (radial tungsten glow + film grain overlay), never a flat fill.
Red is scarce — if red appears twice on one screen, remove one.

**Type** — restrained, product-first. System text face for reading; Oswald
(embedded) for labels, session names and clock digits — engraved small caps and
tabular numerals; Anton (embedded) reserved for the wordmark and the training
phase word only. Display type never substitutes for hierarchy.

**Motion** — everything settles like hung metal: fast attack, long decisive
ease-out (`cubic-bezier(.16,.84,.3,1)`). Nothing bounces. Nothing is cute.

## Sound design

All synthesized (no assets), all **optional** — a persistent toggle lives in the
header, and the choice is remembered.

| Cue | Character |
|---|---|
| Boxing bell | Inharmonic metal partials (523–2890 Hz), hard strike, ~2s decay |
| Round impact | 130→38 Hz sine drop + low-passed noise snap |
| 10-second warning / round end | (next build) double-strike bell variants |

## User journey — progressive depth

A beginner understands the app in seconds; a professional finds depth.

| | New fighter (< 3 sessions) | Experienced fighter |
|---|---|---|
| Hero | "Step into the ring." | "Pick up where you left off." |
| Primary CTA | **Start your first round** | **Create custom fight simulation** |
| Advanced modules | Present but unbadged | "Pro" badges surface |

Session count is tracked locally; the interface graduates with the fighter.

## Home screen

Six doors, nothing else:

🥊 Start Training · ⚔️ Fight Simulation · 🔥 Conditioning ·
🧠 Fight IQ · 📈 Progress · 👤 Fighter Profile

Plus a fixed **Quick Start** bar — one thumb-sized red button, always reachable,
so a fighter at the gym starts a session in one tap.

## Accessibility — gloves on

- Every tap target ≥ **64px** (`--tap-min`); toggles ≥ 48px.
- No nested menus between the fighter and starting a session.
- Large type, high contrast on near-black.
- Full `prefers-reduced-motion` support; visible focus rings for keyboard use.

## Modes — two workspaces, one product

DP Combat adapts to the user's role. This is architecture, not a menu option.

| | Fighter Mode | Coach Mode |
|---|---|---|
| Room | Fight Camp (tungsten, red accent) | Coach's Office (cooler light, steel accent) |
| Voice | **The Corner** briefs the fighter | **Assistant** briefs the coach |
| Home | Corner briefing, next session, camp timeline, camp rounds ring, streak | Tonight's schedule, athlete roster rows, review queue with AI notes |
| Primary action | Begin Training | Plan Session |

Switching modes is a workspace transition: the current room exits downward, the
lighting hue crossfades, and the new room enters with staged choreography.

## Signature interactions

- The Corner greets on every open — briefing lines speak in sequence, waveform live.
- A pre-session briefing (opponent, plan, goal) plays before every session, then the bell.
- The camp rounds ring fills like championship rounds — twelve segments, one per session won.
- The fight camp timeline is a line of nights ending at a fight-night flag, never a calendar.
- Bells, corner clacks and haptics mark every round transition.
