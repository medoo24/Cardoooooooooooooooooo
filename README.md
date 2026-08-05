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
- Keyboard solving shortcuts: A–H or 1–8 select answers, Enter checks/moves next, B bookmarks, C copies, and Esc exits.
- Dedicated **Customized Sprint** page with mode, source section, clinical topic, original tag, count, pace, order, delay, live pool preview, and quick presets.
- Question Library includes a global **Reveal all answers / Hide all answers** control for every currently displayed result, while retaining individual card controls.
- Clear **Copy question + options** buttons in Library and Quiz; answers and tags are intentionally excluded from copied text, with a fallback for direct `file://` use.
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


## Fast Pace toggle and theme gallery

- Fast Pace is now an optional toggle, not a separate study mode. It applies to Smart Review, New Questions, Mistakes, Bookmarks, Mixed Bank, and Customized Sprints.
- The home page includes a global Fast Pace switch and quick starts for all learning goals.
- Includes six dark themes and six bright themes, plus eight accent colors.


## JSON, refined-text exports, and total counters

- Export the complete bank, the current filtered Question Library result, a live Customized Sprint pool, or a completed quiz session.
- JSON exports preserve question structure, answer keys, sections, topics, original tags, source provenance, and local progress status.
- Refined-text exports provide a clean readable layout with numbered questions, options, answers, tags, source files, and progress.
- Polished counters now appear across Home, Question Library, quiz setup, Customized Sprint, active quizzes, results, Insights, and Settings.
