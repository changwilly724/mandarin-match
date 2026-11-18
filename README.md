# Mandarin Match — Rising Rows (prototype v2)

A working, single-player Mandarin Pinyin puzzle game. No accounts, API keys or backend required.

## Play immediately on Windows/Mac

Open `Mandarin_Match_Play_Now.html` from the accompanying download (or open `index.html` in a modern browser).

## Rules

- Six columns and seven rows. At first, three rows contain cards.
- Match an English word with its Pinyin translation to remove both tiles. Any two tiles can be paired, but choosing matches within a row often helps you clear it.
- Clear all six tiles in a row for an 80-point bonus.
- New rows enter **from below** after every three successful pairs (daily/balanced mode), pushing existing rows upward. Do not leave tiles in the top row when the next row rises.
- A daily challenge ends successfully when eight rows are cleared. Endless mode can be played at gentle (4 pairs/new row), balanced (3 pairs/new row) or challenging (2 pairs/new row) speed.
- There is no timer. Hints reveal a pair, at a 10-point cost. Undo reverses a successful match.
- Word bank shows translations for words currently visible. Audio uses your browser's speech synthesizer and the original Chinese text internally; the interface shows Pinyin only.
- Progress is kept in localStorage on the browser/device being used (not synced, and can be erased if browser data is cleared). Refreshing should resume progress.

## Install on iPhone

1. Create a new GitHub repository (for instance `mandarin-match`).
2. Upload the contents of the `mandarin-match-v2` folder to the repository root (`index.html`, `app.js`, `style.css`, `manifest.webmanifest`, service-worker file and both icons).
3. Configure **Settings → Pages → Deploy from a branch → main / root**, then save. The resulting URL will be similar to `https://YOUR-USERNAME.github.io/mandarin-match/` (the real URL is shown in Pages settings).
4. Open that actual URL in **Safari** on your iPhone. Tap Share → Add to Home Screen → Add.
5. This prototype requires no account or server for game data. GitHub Pages hosting is public by default. Do not store private information in the repository.

The service worker automatically caches the app files after their first successful load on an HTTPS host, so the puzzle can subsequently open offline. Spoken audio depends on available device voices. Note that updates to the app may require a reload.

## Security/privacy

No analytics, remote services or data upload are included. The pronunciation feature runs through device speech synthesis; its exact available voice depends on iOS and the browser. This prototype is a learning experiment: the starter vocabulary is hand-curated and does not replace professional pronunciation instruction.

## Design scope

This replaces v1's path drawing and full-grid coverage requirement. Row removal is now achieved by matching pairs. Later candidates include mixed English/Pinyin group puzzles, sentence tile ordering, and audio puzzles, all built on shared vocabulary.
