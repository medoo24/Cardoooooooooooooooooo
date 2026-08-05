# CardioThoracic Atlas — Exam 59 Group B Edition

## Open
Double-click `index.html`. For installable/PWA behavior, serve the folder locally:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Included data
- Source rows represented: 1057
- Study records: 924
- Original deduplicated bank: 894 items
- Added ordered exam collection: 30 questions — **Exam 59, Group B**
- Single-choice items: 922
- Multi-select items: 2
- Source answer-mask anomalies: 1 (flagged and excluded from scored quizzes)
- Visible collection tags: 41

## Exam 59 — Group B
- All 30 questions and the supplied model answers are included in their original order.
- Filter using **Tags → Exam 59 • Group B**.
- The questions are also available under **Past Exams** and **Group Banks**.
- Questions whose stems overlap the existing bank are marked internally with `duplicateOf`, but remain in the exam collection to preserve its numbering and sequence.
- Exam questions display a **Provided model answer** badge.

## Search and keyboard behavior
- Search now updates results in place and no longer rebuilds the whole Question Library after every character.
- Normal letters and numbers are never intercepted while typing.
- **Alt/Ctrl + A–H** or **Alt/Ctrl + 1–8**: choose an answer.
- **Ctrl + Enter**: check the answer or advance.
- **Alt/Ctrl + B**: bookmark.
- **Alt/Ctrl + C**: copy question and options.
- **Alt/Ctrl + N**: next after correction.
- **Esc**: exit a quiz.
- **Alt + S** or **Ctrl + K**: focus Question Library search.
- **Alt + R**: reveal/hide all visible library answers.

## Refined-text export audit
The supplied source bank contains exactly two legitimate questions mentioning **ulcerative colitis**. It was not stored as a suffix on every question. To prevent line carry-over when text is opened or re-extracted, refined-text exports now:

- sanitize hidden control and zero-width characters;
- normalize line endings and spacing;
- construct every question as an isolated text block;
- add explicit `QUESTION n OF total` boundaries and blank lines between records.

Details are recorded in `data-quality-report.json`.

## Existing project features
- Fast Pace is an optional toggle for Smart Review, New Questions, Mistakes, Bookmarks, Mixed Bank, and Customized Sprints.
- Instant correction and adjustable auto-next delay, defaulting to 2 seconds.
- Question Library global Reveal/Hide, individual answer controls, and Show All matching questions.
- JSON and refined-text exports for the full bank, filtered library, sprint pool, and completed sessions.
- Visible section, clinical topic, and source tags on every question.
- Copy question + options without answers or metadata.
- Twelve dark/bright themes, eight accent colors, local progress, bookmarks, backup/restore, print mode, and offline support.

## Files
- `index.html` — application shell
- `style.css` — responsive visual system
- `script.js` — application logic
- `data.js` — generated CardioThoracic question bank
- `data-quality-report.json` — source and import audit
- `manifest.webmanifest`, `sw.js` — installable/offline support when served over HTTP
- `sources/` — original supplied files plus the added Exam 59 Group B source text
