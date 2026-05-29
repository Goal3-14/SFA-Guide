# Star Fox Adventures Speedrun Guide

Community-maintained speedrun guide and resource site for **Star Fox Adventures** (GameCube), built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) and hosted on GitHub Pages.

**Live site:** https://goal3-14.github.io/SFA-Guide/

This site is the **canonical source of truth** for SFA speedrun routes, tech, and glitches. The [speedrun.com guides](https://www.speedrun.com/sfa/guides) are the casual entry point and link back here for the current versions.

## Contributing

The fastest path is the **pencil icon** in the top-right of any page on the live site &mdash; it opens GitHub's web editor and walks you through a PR. See [CONTRIBUTING.md](CONTRIBUTING.md) for image rules, tag conventions, file placement, and the review process.

## Local preview

You need Python 3.10+.

```bash
# 1. Create and activate a virtualenv (optional but recommended)
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
source .venv/bin/activate

# 2. Install dependencies
pip install -r requirements.txt

# 3. Serve with live-reload at http://127.0.0.1:8000
mkdocs serve

# 4. (Optional) build the static site into ./site
mkdocs build --strict
```

`mkdocs serve` rebuilds on every save, so you can preview changes as you edit.

## How deploys work

Pushes to `main` trigger [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml), which builds with `mkdocs build --strict` and publishes via the official `actions/deploy-pages` action. No manual deploy step.

The `--strict` flag fails the build on broken internal links and unrecognized nav entries &mdash; if CI is red, run `mkdocs build --strict` locally to see the same error.

## Maintainership and succession

This project is currently maintained solo by [@Goal3-14](https://github.com/Goal3-14).

**If the maintainer goes inactive:** the content is CC BY-SA 4.0 and the code is MIT. Fork the repo freely and continue it &mdash; that is the explicit succession plan. Drop a note in the SFA speedrunning community so others know where the active fork lives.

**Wanted:** one or two trusted co-maintainers to make this more durable. Open an issue or reach out if interested.

## Repository layout

```
SFA-Guide/
├── .github/
│   ├── workflows/deploy.yml      # Build + deploy to GitHub Pages on push to main
│   └── ISSUE_TEMPLATE/           # Guide request, correction, new trick templates
├── docs/                         # All site content (Markdown). Flat: one .md per topic.
│   ├── index.md                  # Homepage
│   │
│   │ ── Intro / beginner ─────────
│   ├── intro/                    # Game + guide overview
│   ├── general-info/             # Versions, timing, emulator, how to read a route page
│   ├── categories/               # Any%, 100%, Glitchless route walkthroughs
│   │
│   │ ── Core reference ───────────
│   ├── tech/                     # General useful skills (movement, camera, staff)
│   ├── glitches/                 # One .md per glitch — what it is, why it works
│   ├── skips/                    # One .md per applied skip — where in the run
│   ├── locations/                # One .md per area — what happens there, which skips apply
│   │
│   │ ── Bonus ────────────────────
│   ├── tools/                    # Emulators, timers, capture, practice
│   ├── glitch-hunting/           # Deep technical writeups
│   ├── cool-stuff/               # Curated community videos
│   │
│   └── contributing.md           # Pointer to root CONTRIBUTING.md
│
├── mkdocs.yml                    # Site config (theme, plugins, nav)
├── requirements.txt              # Python deps (MkDocs Material + plugins)
├── CONTRIBUTING.md               # How to add/edit guides and images
├── LICENSE                       # CC BY-SA 4.0 (content) + MIT (code)
└── README.md                     # This file
```

Each `docs/<section>/` folder holds flat `.md` files plus one `images/` subfolder. No deeper nesting &mdash; adding a page means dropping one file in one place.

## Why MkDocs Material

Top priority is **fast search**. Material has excellent built-in client-side search (instant, highlighted, no extra services). The "edit this page" pencil and tag plugin lower the contribution barrier without bolting on third-party tools.

## License

- Documentation under `docs/` &mdash; [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- Site config and workflow code &mdash; MIT

See [LICENSE](LICENSE) for the full text.

Star Fox Adventures is the property of Nintendo / Rare. This is an unofficial fan-made resource; no game assets are distributed in this repository.
