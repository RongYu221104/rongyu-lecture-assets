# Lecture Asset Repository Guidance

This public repository is the lecture PDF storage and GitHub Pages deployment
for RongYu's Notes. The sibling website repository is
`../RongYu221104.github.io`.

- Keep only lecture PDFs under `public/lectures/maths/` and
  `public/lectures/physics/`; website code, covers, and metadata belong in the
  website repository.
- Preserve the user-facing PDF filename. Prepare delivered lectures by running
  `scripts/prepare_assets.py` from the sibling website repository. Do not edit
  files in its ignored `input/` area.
- Before committing, reconcile filenames, page counts, and covers with the
  website's `src/data/lectures.json` by running `pnpm verify:assets` and
  `pnpm verify:lectures` there.
- Commit and deploy this repository before publishing website metadata that
  references a new or replaced lecture.
- Monitor `Deploy assets to GitHub Pages` and verify the exact production PDF
  URL returns `200`, `application/pdf`, and byte-range support.
- Remove an obsolete PDF from current `HEAD` when it is replaced. Git history
  rewriting or a force push requires separate explicit approval.
- Never commit credentials, raw input files, MP3 files, covers, or unrelated
  assets.
