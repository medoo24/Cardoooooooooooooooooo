# CardioThoracic Atlas — Enhanced Offline Project

## Open
Double-click `index.html`. For installable/PWA behavior, serve the folder with a local server:

```bash
python -m http.server 8000
```
Then open `http://localhost:8000`.

## Included data
- Source rows combined: 1027
- Deduplicated study items: 894
- Single-choice items: 892
- Multi-select items: 2
- Source answer-mask anomalies: 1 (flagged and excluded from scored quizzes)
- Original collection tags: 40

## Enhancements
- Old Pediatric data removed completely.
- Exact duplicate questions merged across both supplied files.
- Original hierarchical Anki tags preserved and grouped into source sections.
- Added clinical-topic navigation without replacing source tags.
- Browse/search/filter, Smart Review, Fast Pace, unseen/mistake/bookmark modes, multi-select support.
- Fast Pace gives instant correction on single-answer items and auto-advances after an adjustable delay (2 seconds by default).
- Every browse and quiz question visibly shows section, clinical topic, and original source tags together.
- Local progress, bookmarks, dark/light themes, backup/restore, print mode.
- Offline-first: no external libraries or internet connection required.

## Files
- `index.html` — app shell
- `style.css` — responsive visual system
- `script.js` — app logic
- `data.js` — generated CardioThoracic bank
- `manifest.webmanifest`, `sw.js` — installable/offline support when served over HTTP
- `sources/` — original supplied text files
