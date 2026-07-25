# The Wellington Wave

Public website for **The Wellington Wave**, a data-informed publication covering
the Wellington Waves swim team. This repository holds only approved,
publication-ready HTML — it is not where editorial or data work happens.

## Purpose

This repo exists solely to host and serve finished issues via GitHub Pages.
Each issue is a single self-contained HTML file (styles and images embedded
inline) dropped into place and published as-is.

## Where issue files live

```text
/
├── index.html              → homepage, links to the latest issue
├── issues/
│   └── YYYY-MM-DD/
│       └── index.html      → one folder per issue
├── README.md
└── .gitignore
```

Each issue lives at `issues/YYYY-MM-DD/index.html`, and is served at the
permanent URL `/issues/YYYY-MM-DD/`.

Special editions may use a descriptive folder name instead of a date, e.g.:

```text
issues/2026-championship-edition/
issues/2026-annual/
```

## Naming convention

```text
issues/YYYY-MM-DD/index.html
```

Use the date the issue is published, not the date of the meet it covers, if
the two ever differ.

## Publishing a new weekly issue

1. Receive the approved, self-contained HTML file for the issue (editorial
   and data work happens outside this repo, in `moore-ops`).
2. Confirm the file includes `<meta name="robots" content="noindex, nofollow">`
   in `<head>`. Add it if missing — this discourages routine search-engine
   indexing without making the page private.
3. Create a new folder: `issues/YYYY-MM-DD/`.
4. Save the file there as `index.html`.
5. Update `index.html` at the repo root so the "Latest Issue" card links to
   the new issue and shows its title/date.
6. Commit and push to `main`.

GitHub Pages redeploys automatically on every push to `main` — no manual
publish step beyond the push itself.

## GitHub Pages configuration

- **Branch:** `main`
- **Folder:** `/` (repository root)

## Scope

This repository intentionally contains **only** finished, approved HTML for
public issues, plus the homepage and this documentation. It does not contain:

- source data, scripts, or parsers
- unpublished drafts or editorial working files
- PDFs or raw newsroom materials

All of that lives in the `moore-ops` repository under `docs/editorial/`,
which is where editorial and data decisions are made before an issue is
approved and handed off here as finished HTML.
