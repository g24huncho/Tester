# DP Combat

**Train smarter. Fight better.**

A serious fighter's tool. This build delivers the opening experience and brand
identity: a cinematic launch sequence, the championship-metal visual language,
synthesized ring-side sound design, and the home screen.

## Run it

No build step, no dependencies — open `index.html` in any modern browser:

```sh
open index.html        # macOS
xdg-open index.html    # Linux
```

Or serve it: `python3 -m http.server` and visit `http://localhost:8000`.

## What's inside

- **`index.html`** — the app. Launch animation (dark → spotlight → punch impact
  → metallic logo reveal → light sweep), then the home screen with six training
  modules, an adaptive primary CTA, a fixed Quick Start bar, and an optional
  synthesized boxing bell / impact sound engine (Web Audio, no audio files).
- **`BRAND.md`** — the brand identity: values, palette, type, motion, sound
  spec, and the progressive-depth user journey.

## Notes

- The intro is always skippable and is bypassed entirely when the OS requests
  reduced motion.
- Sound is optional (header toggle, remembered) and only ever plays after a
  user gesture.
- Tap targets are glove-sized (≥ 64px) and the primary action is one tap away.
