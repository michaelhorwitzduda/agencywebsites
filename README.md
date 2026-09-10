# Agency Websites: Marketing Automation (password-protected)

A single encrypted page over 1,567 Duda agency/studio partners from the
marketing automation research. `index.html` at the repo root is the only
published file: a self-contained page encrypted client-side with
[pagecrypt](https://github.com/Greenheart/pagecrypt) (AES-GCM via WebCrypto,
PBKDF2 with 2,000,000 iterations). Nothing here is readable without the
password, which is **not** stored in this repo (`password.txt` is gitignored).

Live: https://michaelhorwitzduda.github.io/agencywebsites/

## Source of truth

This repo is a publish target, not the source. The dashboard is built and
published from `C:/Projects/MarketingAutomationResearch/dashboard/` — edit
and refresh data there, then run `npm run release` in that repo's `dashboard/`
directory. See that repo's `dashboard/README.md` for the full workflow.

## Provenance

Every publish writes `dashboard-provenance.json` here, recording which
research-repo commit and which input data files (with sha256 hashes)
produced the published `index.html`. Use it to trace a live dashboard back
to an exact state of the research repo.

## Magic link

A pagecrypt magic link (`<this url>#<password>`) opens the dashboard already
unlocked. The Customer Insights Hub links here with such a link so anyone
who has unlocked the hub can open this dashboard without typing another
password.

## GitHub Pages

Settings, Pages, Deploy from a branch, `main`, folder `/ (root)`. Only the
encrypted `index.html` is served (plus this README and provenance, which
hold no secrets); source files are never published here.
