# Despacho

A quiet browser-based compression bureau for passport scans, forms, and certificates. Trims oversized documents down to official ministry limits (5&nbsp;MB per file by default) — all in your browser, nothing uploaded.

Built for Spanish NIE paperwork and the consular document game in general.

## Live

**https://gochaavsajanishvili.github.io/despacho/**

## Languages

English · ქართული · Русский · Español · 中文

## How it works

- **PDFs** — each page is rendered to canvas at the chosen DPI (default 150), re-encoded as JPEG, and stitched back into a lean PDF via pdf-lib. Same profile family as Ghostscript's `/ebook` preset.
- **Images** — resized to ≤&nbsp;2400&nbsp;px on the longest edge, re-encoded as JPEG.
- **Adaptive** — if a file is still above the chosen cap, DPI and JPEG quality shrink until it fits (or the minimums are hit).
- **Output** — ZIP bundle with a small plaintext ledger of original-vs-compressed sizes, or individual downloads.

Everything runs locally in the tab — no file, page, or byte is transmitted.

## Stack

Vanilla HTML / CSS / JS. No build step. Libraries via CDN:

- [pdf.js](https://github.com/mozilla/pdf.js) — page rasterisation
- [pdf-lib](https://pdf-lib.js.org/) — PDF rebuilding
- [JSZip](https://stuk.github.io/jszip/) — bundling

## Run locally

Open `index.html` in any modern browser. That's the whole deployment story.

## License

Do whatever you like with it.
