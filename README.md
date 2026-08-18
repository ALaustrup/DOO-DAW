# DOO DAW — Astra Matrix

**DOO DAW** is a next-generation browser (and desktop-ready) DAW with **XY** as a first-class wavetable instrument.

Built by [Astra Matrix](https://github.com/ALaustrup).

## Features

- **Session + Arrangement** views (Ableton-style clip grid)
- **XY instrument** hosted on a shared Web Audio graph (not a VST wrapper)
- **Transport** — play, stop, loop, metronome, tempo, record master bus
- **Mixer** — volume, mute, solo, record-arm, peak meters
- **Sample browser** — factory procedural drums/loops + Import + Link folder
- **Cloud folders** — link desktop-synced Drive / OneDrive / iCloud folders (File System Access API; no OAuth tokens)
- **Keyboard jam** — A–K plays XY; Space = transport

## Quick start

```bash
npm install
npm run dev
```

Open http://localhost:8080 → **Power On** → **Play**.

Demo project: *DOO Session — Cyber Night* (XY lead + drums + bass + perc @ 124 BPM).

## Stack

- React 19 · TypeScript · Vite · TanStack Start
- Zustand · Tailwind CSS v4 · Web Audio API
- Lucide icons

## Repo layout

```
src/
  daw/           # DOO DAW (store, audio graph, UI)
  synth/         # XY instrument (engine, UI, presets)
  routes/        # App shell → DawApp
docs/            # Architecture, DSP, VST3 / Tauri port notes
```

## Honest scope

This is a **demo-quality coherent DAW**, not full Ableton Live 12 parity.

| Topic | Reality |
| --- | --- |
| XY “plugin” | In-process instrument on the DOO audio graph — mixable & recordable. True VST3 needs a native C++/JUCE port. |
| Cloud samples | Link a *locally synced* cloud folder. No cloud API tokens stored. |
| Desktop | Same UI/DSP; Tauri wrap is documented in `docs/PORTING_TAURI.md`. |

## Related

- Standalone XY synth: [ALaustrup/XY](https://github.com/ALaustrup/XY)
- VST3 roadmap: `docs/PORTING_VST3.md`

## License

UNLICENSED — Astra Matrix, Inc.

---

by ASTRA MATRIX
