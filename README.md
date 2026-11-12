# Wake Up &amp; Breathe — SAT/SBT Escape Room

A browser-based critical-care escape room for the Keck Critical Care RN Residency.
Patient: **Mr. Raymond Keller** (COPD + pneumonia, vent day 5). Clinical anchor: CP 3-162 Awakening &amp; Breathing Trials.
All HTML, no install, no Genially. **Simulation use only — not for clinical use.**

## What's here

| File | What it is |
|------|------------|
| `index.html` | Facilitator control hub — open screens, drive room state, tag URLs |
| `room.html` | The escape room itself — 7 locks, codes, countdown, piñata finale, debrief |
| `tags.html` | NFC tag activities (`#t1`…`#t7`) — the chips point here |
| `vent.html` | Ventilator display (secondary monitor) |
| `monitor.html` | Bedside monitor display (secondary monitor) |
| `pump.html` | Interactive infusion pump |
| `audio/` | Drop ElevenLabs mp3s here (room looks for `kel_01_handoff.mp3`) |

## Live URLs (after GitHub Pages is on)

Base: `https://<your-username>.github.io/wake-up-and-breathe/`

- Control hub: the base URL (opens `index.html`)
- Room: `…/room.html`  (no-cuff-leak branch: `…/room.html?b=nc`)
- Device screens: `…/vent.html` · `…/monitor.html` · `…/pump.html`
- **NFC chips** → write these:
  - `…/tags.html#t1` bed rail · `#t2` chart · `#t3` pumps · `#t4` monitor
  - `#t5` radio · `#t6` vent · `#t7` door
  - No-cuff-leak branch: point the vent + door chips at `#t6b` and `#t7b`

## Lock codes (clean run)

`RASS` → `AWAKE` → `COMMAND` → `125` → `830` → `065` → `0545`
No-cuff-leak branch: Lock 7 becomes `0730` and the correct piñata flips to RETRY TOMORROW.

## Keys on the device screens

`B` = vented (full support) · `S` = SBT (pressure support) · `P` = pain · `F11` = fullscreen.
All screens sync automatically (same site = same origin).

## Swapping in a new patient later

Open `room.html` and edit the `CFG` block at the top — title, handoff, bedside findings, and all seven riddles/hints/codes live there. No rebuild needed.
