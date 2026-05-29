# Contributing

Thanks for helping keep the SFA speedrun guide accurate and current. The site is built with [MkDocs Material](https://squidfunk.github.io/mkdocs-material/) from plain Markdown files in [`docs/`](docs/), so contributing is mostly just editing text.

## TL;DR

- **Small fix?** Click the pencil icon at the top-right of any page on the live site &rarr; edit in the browser &rarr; "Propose changes" &rarr; open a PR. No local setup needed.
- **New page or images?** Clone locally, follow the layout rules below, run `mkdocs serve` to preview, then open a PR.
- A maintainer will review &mdash; typically within a few days. Speed up review by including evidence (video link, timestamp, or screenshot) for any timing claim or new trick.

## Three ways to contribute

### 1. Browser edit (smallest changes)

Best for: typo fixes, small text edits, a single-page rewording.

1. Open the page on the live site.
2. Click the &#9998; pencil in the top-right.
3. Edit, then "Propose changes" &rarr; GitHub creates a fork and PR for you.

### 2. Local edit (recommended for anything bigger)

Best for: new pages, image uploads, nav changes, multi-page edits.

```bash
git clone https://github.com/Goal3-14/SFA-Guide.git
cd SFA-Guide
python -m venv .venv && .venv\Scripts\activate    # Windows
# source .venv/bin/activate                       # macOS / Linux
pip install -r requirements.txt
mkdocs serve
```

Open <http://127.0.0.1:8000> &mdash; it live-reloads on save.

Before opening a PR, run `mkdocs build --strict` &mdash; this is exactly what CI runs and will catch broken links and unknown nav entries.

### 3. Open an issue

If you don't want to write the change yourself, open an issue using one of the templates (guide request, correction, new trick/glitch). A maintainer or another contributor will pick it up.

## Where files go

Content lives under `docs/`. The structure is **flat and modular**: one `.md` file per glitch / skip / location / tech topic. No nested folders inside a section. This makes it easy to add a new page &mdash; just drop one file in one folder.

| Type of content | Where it goes |
|---|---|
| Game + guide intro | `docs/intro/index.md` |
| Beginner overview (versions, timing, emulator) | `docs/general-info/index.md` |
| A whole-category route walkthrough | `docs/categories/<category>.md` &mdash; links to skips and locations in order |
| A general movement / control technique | `docs/tech/<topic>.md` |
| A specific glitch &mdash; what it is, why it works | `docs/glitches/<glitch>.md` |
| A specific applied skip &mdash; where in the run, how to do it | `docs/skips/<skip>.md` |
| A game area &mdash; overview and which skips happen there | `docs/locations/<area>.md` |
| External tools and resources | `docs/tools/index.md` |
| Deep technical writeup for glitch hunters | `docs/glitch-hunting/<topic>.md` |
| Curated community videos | `docs/cool-stuff/index.md` |

### Images

Each section has its own `images/` folder. The `.md` files in the section are flat; the only subfolder is `images/`:

| Section | Image folder |
|---|---|
| Glitches | `docs/glitches/images/` |
| Skips    | `docs/skips/images/` |
| Locations | `docs/locations/images/` |
| Tech | `docs/tech/images/` |

Prefix each image with the name of the page that uses it: `dark-ice-mines-room-3.png` lives in `docs/locations/images/`.

### Glitches vs Skips &mdash; which goes where?

A common question. The split:

- A **Glitch** page documents the *mechanic* &mdash; what the glitch is, how to trigger it, and why it works at the engine level. Audience: someone learning the trick in isolation.
- A **Skip** page documents an *application* &mdash; "at this point in the run, in this area, you can use [glitch X] to skip [thing Y]". Audience: someone running the game.

One glitch can be used by many skips. One skip uses one (sometimes zero) glitches.

If a glitch is only ever used in one place, it's fine to fold it into the skip page and skip the glitch page. Split them later if a second use turns up.

### Updating the nav

**When you add a new page, update `mkdocs.yml`'s `nav:` block** so it appears in the sidebar. The build runs with `--strict`, so a page that exists but isn't in `nav` is fine; a `nav` entry that points to a missing file will fail CI.

## File naming

- Lowercase, hyphen-separated: `mole-skip.md`, not `Mole_Skip.md` or `moleSkip.md`.
- Use the in-game name when there is one. Use the community name when there isn't.
- Folder names follow the same rule: `dark-ice-mines/`, not `DarkIceMines/`.

## Tags (cross-cutting categories)

Tags let one page (e.g. an area walkthrough) appear under multiple categories without duplicating content. Add tags in the YAML frontmatter at the top of a page:

```markdown
---
tags:
  - any%
  - 100%
---
```

The full Tags page is auto-generated at [/tags/](tags.md).

### Canonical tag list

Only use tags from this list, lowercase exactly as written. Adding a new tag requires updating this list in the same PR so the vocabulary stays small.

- `any%`
- `100%`
- `glitchless`
- `rta` &mdash; real-time attack notes
- `igt` &mdash; in-game timer notes
- `glitch` &mdash; the page describes or relies on a glitch
- `cutscene-skip`
- `routing`
- `setup` &mdash; emulator / hardware / capture setup
- `beginner` &mdash; written assuming little prior knowledge
- `advanced` &mdash; assumes tech / route familiarity

> Don't see what you need? Open a PR that both uses the new tag **and** adds it to this list with a one-line description.

## Image rules

These rules keep the repo small, the site fast, and screenshots legible.

- **Per-section** images folder: `docs/<section>/images/`. There is no global `images/` folder, and no per-page subfolders. See the table under "Where files go" above.
- **Name** files with the page name as prefix: `dark-ice-mines-room-3-pixel-alignment.png` for a screenshot used by `docs/locations/dark-ice-mines.md`.
- **Resize** to ~1400px max width before committing. The site never displays larger than that.
- **Format:**
  - PNG for menus, HUD, anything pixel-precise, or anything with sharp edges.
  - JPG (quality 80&ndash;85) or WebP for in-game scenery / cutscene captures.
- **Compress** before committing &mdash; [pngquant](https://pngquant.org/), [oxipng](https://github.com/shssoichiro/oxipng), or [cwebp](https://developers.google.com/speed/webp/docs/cwebp). Aim for under 300 KB per image.
- **Crop tight** to the game viewport: no Dolphin window chrome, no Discord notifications, no OBS overlays.
- **No GIFs.** Use a YouTube embed for motion. If a tiny inline loop is essential, use an MP4 under 1 MB and under 3 seconds &mdash; and justify it in the PR.

### Embedding an image with a caption

```markdown
![Pixel alignment for the room 3 wall clip](images/room-3-pixel-alignment.png)
{ .caption }

*Stand with Krystal's right heel on the second floor tile seam. Camera-relative neutral on the C-stick.*
```

The `{ .caption }` attribute lets you style captions consistently (the `attr_list` extension is enabled). Click-to-zoom is handled automatically by the `glightbox` plugin &mdash; no extra markup needed.

## Video

- YouTube embeds (unlisted or public) for all motion content.
- Do **not** commit video files to the repo &mdash; GitHub Pages bandwidth and repo size both suffer.
- Link with a timestamp when referencing a specific moment: `https://youtu.be/VIDEO_ID?t=137`.

## Review process

1. Open a PR against `main`. Fill in the PR description &mdash; what changed and why.
2. For new tech or timing claims, include a video link or screenshot as evidence.
3. A maintainer reviews and either merges, requests changes, or asks for clarification.
4. CI must be green &mdash; if `mkdocs build --strict` fails, the PR cannot merge. Run it locally to debug.
5. Once merged, the site redeploys automatically within a few minutes.

## Style conventions

- One sentence per line in Markdown source is fine &mdash; it produces cleaner diffs.
- Prefer in-game names; introduce community names in parentheses on first use.
- Frame timing as ranges, not single numbers (`~4.2&ndash;4.5s`) unless you have a verified frame count.
- Mark anything uncertain with a callout:

  ```markdown
  !!! warning "Unverified"
      This setup works on Dolphin 5.0; console behavior not confirmed.
  ```

## Questions

Open an issue with the **guide request** template and a maintainer will respond.
