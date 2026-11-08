# Sparky Dance Rig (installable web app)

Static files only: no build step, no server code. Works offline after the first visit.

| File | What it is |
|---|---|
| index.html | the whole app |
| three.min.js | the 3D engine (three.js r128, MIT license), bundled so it works offline |
| manifest.webmanifest | name, colors and icons for "Add to Home Screen" |
| sw.js | service worker: saves the files on the device so it runs offline |
| icons/ | app icons |

## Put it on GitHub Pages
1. Make a repo (for example `sparky`), or a `sparky/` folder in your website repo, and upload all of these files.
2. Repo Settings → Pages → Source: "Deploy from a branch" → `main` / root (or the folder) → Save.
3. After a minute it is live at `https://<your-account>.github.io/sparky/`.

## Install on iPhone
Open the link in Safari → Share → Add to Home Screen. It opens full-screen, like an app, and works offline.

## Updating
Upload the new index.html, then change `VERSION` in sw.js (sparky-v1 → sparky-v2) so phones fetch the new copy.

Note: the home-screen app keeps its own saved routine, separate from Safari's.
