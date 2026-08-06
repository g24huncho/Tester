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

**Palette** — the dark gym and the belt:

| Token | Hex | Use |
|---|---|---|
| Ink | `#07070a` | Canvas. The room. |
| Ink 2/3 | `#0d0d12` / `#14141b` | Surfaces, cards |
| Gold deep → hi | `#6d5518` → `#c9a24a` → `#f7e7ae` | Championship metal. Wordmark, accents, focus. |
| Corner red | `#d7263d` | One job only: the primary "go" action. |
| Text | `#f2f0ea` / `#8d8c96` | Copy / secondary |

Gold is *metal*, never flat: always a gradient ramp with a moving or resting sheen.
Red is scarce — if red appears twice on one screen, remove one.

**Type** — condensed, heavy, uppercase for the brand voice; wide letter-spacing
(`.14em`–`.52em`) evokes engraved nameplates and fight posters. Body copy stays
sentence-case and calm.

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
