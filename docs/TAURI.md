# DOO DAW — Tauri desktop path

Same React + Web Audio stack runs inside a Tauri webview.

1. `npm create tauri-app` (or add `src-tauri/` to this repo)
2. Point the webview at the Vite build
3. Grant folder access permissions for sample libraries
4. Optional: lower buffer size / exclusive audio via native layer later

No rewrite of the DSP or UI is required for a first desktop ship.
