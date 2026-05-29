# Contributing

The full contributor guide lives at the repository root: **[CONTRIBUTING.md on GitHub](https://github.com/Goal3-14/SFA-Guide/blob/main/CONTRIBUTING.md)**.

It covers everything you need:

- How to suggest edits (pencil-icon flow vs local clone)
- The file layout (one `.md` per glitch / skip / location, flat folders)
- The canonical tag list (`any%`, `100%`, `glitchless`, etc.)
- Image rules (per-section `images/` folder, naming, compression)
- The review process

## Quick start

```bash
git clone https://github.com/Goal3-14/SFA-Guide.git
cd SFA-Guide
python -m venv .venv && .venv\Scripts\activate   # Windows
pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000> and edit. The site reloads on save.

Before opening a PR: `mkdocs build --strict` (this matches CI and catches broken links).

## The simplest possible contribution

1. Find a page you want to fix on this site.
2. Click the &#9998; pencil at the top-right.
3. Edit in the GitHub web editor.
4. "Propose changes" &rarr; opens a PR.

No clone, no setup. A maintainer will review.
