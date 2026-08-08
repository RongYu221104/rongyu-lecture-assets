# RongYu's Notes — Lecture Assets

Media repository for RongYu's Notes. This repository stores only the lecture
PDF files served by the website's PDF reader.

## Layout

- `public/lectures/maths/*.pdf` — mathematics lecture PDFs
- `public/lectures/physics/*.pdf` — physics lecture PDFs

Published at
`https://rongyu221104.github.io/rongyu-lecture-assets/lectures/<subject>/<filename>.pdf`

## Deployment

Pushed to `main`, the `Deploy assets to GitHub Pages` workflow publishes the
`public/` directory through GitHub Pages (Source: GitHub Actions). The
website repository is `RongYu221104/RongYu221104.github.io`; covers,
metadata, and reader code stay there.

## Adding Lectures

1. Put the original PDF into the website repo's local `input/maths/` or
   `input/phys/` (ignored).
2. Run `scripts/prepare_assets.py` in the website repo; it writes the PDF here.
3. Update `src/data/lectures.json` page count and dates in the website repo.
4. Commit and deploy this repository first, then the website repository.
