# metis-lang-dev.github.io

The one-page site for **metis** and its stack — the language (LLP), the catalog and the loop, the agent — as the three papers frame it. Served by GitHub Pages from this repository's default branch root at https://metis-lang-dev.github.io/.

## What is here

- `index.html` — the whole page: plain HTML, CSS and a little JavaScript. No framework, no build step, no tracker, no external script or font. Phone width, dark mode (`prefers-color-scheme`), and the animation honours `prefers-reduced-motion` (a static frame) and has a Pause control.
- `README.md` — this file.

## How to edit

Edit `index.html` and push. Pages redeploys the default branch on its own; no Actions workflow is needed.

Rules the content follows (website s-d21379cd, the architect's content design):

- **Every number names its source.** Each figure on the page is preceded by an HTML comment `<!-- source: … -->` naming the committed report or doc it comes from. A number without a source is dropped, not rounded or guessed.
- **Every code fragment is copied from a committed file** and says which, in its caption. The fragments: `metis-catalog/domains/plant/plant.llp`, `metis-catalog/domains/plant/extensions/visitor.llp`, `metis-catalog/domains/three_pigs/three_pigs.llp` with `goldens/traces/three_pigs.txt`, the dog's `intent/dog-corpus.tsv` and intent.yaml with the recorded turns of `metis-agent/go/internal/dagent/testdata/days/dog.out.jsonl`, and the READMEs' shell lines. The gate fragment is the loop SDK's own output (`python -m metis_loop_sdk.catalog apply plant --extension visitor=… --dry-run`).
- **The papers are the references.** The language paper's PDF is linked from `metis-lang/paper/`. The two usage papers are linked as "draft, in preparation" until their PDFs are committed (`metis-catalog/paper/`, `metis-agent/paper/`); update the Papers section then.
- Copy may be rewritten for rhythm; facts, numbers and fragments stay sourced. No "always"; no benchmark the repos don't have.

## Checking a change locally

Open `index.html` in a browser. For the phone layout, use the browser's device toolbar at 390 px; for dark mode, the OS setting or the devtools rendering emulation; for reduced motion, the devtools rendering emulation (`prefers-reduced-motion: reduce`) — the animation must show its last frame, still.

© 2026 Robofortis. metis is research software, pre-release.
