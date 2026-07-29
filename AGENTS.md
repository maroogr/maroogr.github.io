# Project agent memory

This file is the project's committed home for project-intrinsic agent knowledge: build, test, release, architecture, and sharp-edge notes that should travel with the code.

- Add durable project-specific notes here as they are discovered through real work.
- This is the captain's live marketing site (`maroogr.co.uk`). Any push to `main` deploys the whole repo root automatically via `.github/workflows/deploy.yml` (`actions/upload-pages-artifact` on `path: '.'` + `actions/deploy-pages`) — there is no build/staging step, so whatever lands on `main` is live immediately. No CNAME file is checked in; the custom domain is set in GitHub Pages settings directly.
- No test/lint tooling exists in this repo.
- Deal-analysis / valuation-snapshot exports (self-contained single-file HTML, e.g. Claude Artifact-style) go under `snapshots/<slug>/index.html`, kept separate from the marketing content at the repo root, giving clean URLs like `maroogr.co.uk/snapshots/<slug>/`. These files are typically large (~14.5MB each) — committing several adds real, effectively permanent weight to git history; flag that cost when adding more.
- `deals/index.html` (`maroogr.co.uk/deals/`) is a hand-written link list to every snapshot, labelled with each snapshot's `data-snapshot-field="hero-max-rent"` value. When adding a new snapshot, add a matching card here too.

## Maintaining this file

Keep this file for knowledge useful to almost every future agent session in this project.
Do not repeat what the codebase already shows; point to the authoritative file or command instead.
Prefer rewriting or pruning existing entries over appending new ones.
When updating this file, preserve this bar for all agents and keep entries concise.
