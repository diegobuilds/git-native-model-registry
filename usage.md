# Usage

This docs portal is MkDocs-ready and designed to be the single source of truth for terminology.

## Local preview
1. `pip install mkdocs mkdocs-material`
2. `mkdocs serve`
3. Open `http://127.0.0.1:8000`

## Publish
- For GitHub Pages: `mkdocs gh-deploy`
- For internal hosting: build static site with `mkdocs build` and serve the `site/` directory.

## Updating the glossary
- Edit `docs/glossary.md` or `glossary.csv`.
- Open a PR with the change and include:
  - Rationale (1 sentence)
  - Example usage (1–2 lines)
  - Reviewer from engineering and compliance

Keep entries concise and business-facing.
