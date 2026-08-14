# Cursor brief — DOO DAW + XY (Astra Matrix)

You are working in the **DOO DAW** monorepo: a browser DAW that hosts the **XY** wavetable synthesizer as a first-class instrument device.

## Product

- **Company:** Astra Matrix (two words)
- **DAW:** DOO DAW
- **Instrument:** XY

## Stack

React 19, TypeScript, Vite, TanStack Start/Router, Zustand, Tailwind v4, Web Audio.

## Architecture

- One shared `AudioContext` owned by `DawAudio`
- XY `AudioEngine.init(sharedCtx)` + `connectToTrack(trackGain)` routes into the instrument bus
- Session clips schedule MIDI into XY and samples into track gains
- Master record via `MediaStreamDestination` + `MediaRecorder`

## Do not

- Do not claim VST3 works from this codebase (needs native JUCE rewrite)
- Do not store cloud OAuth tokens; folder link only
- Do not break the shared audio graph (XY must stay on DAW context when hosted)

## Priority work

1. Harden transport / MIDI scheduling
2. Piano roll / clip editor
3. More factory samples + preset packs
4. Tauri desktop shell
5. Formal DSP spec for VST3 port (see docs/)
