# Ashfall Depths — hosted demo

Mobile-first, first-person grid dungeon crawler demo (Eye of the Beholder / Lands of Lore style UI).

## Play it

**https://mikailr.github.io/ashfall-depths/**

The production build is already committed to the [`gh-pages`](../../tree/gh-pages) branch. GitHub
does not let automation enable Pages on a fresh repository, so it needs one click:

1. Open **Settings → Pages** in this repository.
2. Under *Build and deployment*, set **Source** to *Deploy from a branch*.
3. Pick branch **`gh-pages`**, folder **`/ (root)`**, and press **Save**.

The site is live at the URL above about a minute later.

## How this repo works

- `gh-pages` — the static site (`index.html` + one JS and one CSS file with all sprites, textures
  and fonts inlined).
- `.github/workflows/deploy.yml` — imports the build tarball (hash-verified) and force-pushes it
  to `gh-pages`; it also tries the Pages API deploy, which succeeds once Pages is enabled.
- The game source (Vite + React + TypeScript) lives in the project repository, which also
  contains the same `dist/` build.

## Tips on a phone

Use *Add to Home Screen* for a chrome-less fullscreen experience. Tap a portrait's weapon or skill
icon to attack whatever stands in front of you; hold the D-pad to keep walking; tap a portrait to
open the character sheet and the pack.
