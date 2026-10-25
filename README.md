# metis-lang-dev.github.io

The one-page site for **metis-lang** and its stack — the language (LLP), the catalog and the loop, the agent — as the three papers frame it. Served by GitHub Pages from this repository's default branch root at https://metis-lang-dev.github.io/.

## What is here

- `index.html` — the whole page: plain HTML, CSS and a little JavaScript. No framework, no build step, no tracker, no external script or font. Phone width, dark mode (`prefers-color-scheme`), and the animation honours `prefers-reduced-motion` (a static frame) and has a Pause control.
- `assets/` — the organization's avatar (`metis-lang.jpg`, the GitHub org picture, copied here so nothing is hotlinked: the header's mark and the link preview), and the favicon and touch icon: the metis mark (the circle, no word), made by metis-lang's `brand/make_icons.py` (`favicon-32.png`, `favicon-192.png`, `apple-touch-icon.png` on white).
- `README.md` — this file.

## How to edit

Edit `index.html` and push. Pages redeploys the default branch on its own; no Actions workflow is needed.

Rules the content follows (website s-d21379cd, the architect's content design):

- **Every number names its source.** Each figure on the page is preceded by an HTML comment `<!-- source: … -->` naming the committed report or doc it comes from. A number without a source is dropped, not rounded or guessed.
- **Every code fragment is copied from a committed file** and says which, in its caption. The fragments: `metis-catalog/domains/plant/plant.llp`, `metis-catalog/domains/plant/extensions/visitor.llp`, `metis-catalog/goldens/cases/plant.llp` with `goldens/traces/plant.case.txt`, the dog's `intent/dog-corpus.tsv` and intent.yaml with the recorded turns of `metis-agent/go/internal/dagent/testdata/days/dog.out.jsonl`, and the READMEs' shell lines. The gate fragment is the loop SDK's own output (`python -m metis_loop_sdk.catalog apply plant --extension visitor=… --dry-run`).
- **The papers are the references.** The three PDFs and their LaTeX sources are linked from the repositories (`metis-lang/paper/`, `metis-catalog/paper/`, `metis-agent/paper/`); update the Papers rows when a draft's version moves.
- Copy may be rewritten for rhythm; facts, numbers and fragments stay sourced. No "always"; no benchmark the repos don't have.
- **The Q&A is the author's text, verbatim.** Its three essays are `essays.md` of the perotheia-packages checkout, kept word for word; only the HTML structure (a heading per question, paragraphs, the lists) is the page's. To check: strip the tags from the `essays` block and diff against the file, whitespace and list markers aside.
- **The myth is cited.** The hero's caption paraphrases Hesiod, *Theogony* 886–900 and 924–926 and Apollodorus, *Library* 1.3.6; the armour-from-inside detail is hedged ("in some tellings": it is only in the lacuna after *Theogony* 929); keep the shape honest (Metis does not escape; Zeus is the one who swallows her).

## Checking a change locally

Open `index.html` in a browser. For the phone layout, use the browser's device toolbar at 390 px; for dark mode, the OS setting or the devtools rendering emulation; for reduced motion, the devtools rendering emulation (`prefers-reduced-motion: reduce`) — the animation must show its last frame, still.

© 2026 Robofortis. metis-lang is research software, pre-release.
