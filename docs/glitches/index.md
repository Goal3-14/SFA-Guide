# Glitches

The **mechanics** of every known glitch &mdash; what it is, how to trigger it, and why it works at the engine level. Concrete applications (which skip uses which glitch, where in the run) live under [Skips](../skips/index.md).

## How this section is organized

- **One `.md` file per glitch** in this folder. No subfolders.
- Images for a glitch go in [`docs/glitches/images/`](images/) using the glitch's name as a prefix: `out-of-bounds-wall-clip-alignment.png`.
- Deep mechanical analysis (memory addresses, debug-menu traces, frame data tables) belongs under [Glitch Hunting](../glitch-hunting/index.md), not here. This section should stay readable for a runner trying to learn the trick.

## Known glitches

<!-- TODO: link a page per glitch as they are written. See out-of-bounds.md for the template shape. -->

- [Out of Bounds](out-of-bounds.md) &mdash; _example file showing the page template_
- <!-- e.g. - [RBA](rba.md) — if applicable to SFA -->
- <!-- e.g. - [Cutscene Storage](cutscene-storage.md) -->
- <!-- TODO: list real SFA glitches here -->

## Adding a new glitch

1. Copy [`out-of-bounds.md`](out-of-bounds.md) as a starting template.
2. Rename it to the glitch's community name (lowercase, hyphens).
3. Fill in the sections. The mandatory sections are **What it is**, **Setup**, and **Video**.
4. Drop any screenshots into `images/` with a matching prefix.
5. Link it from the list above and add it to `mkdocs.yml` `nav:`.
6. Link to it from any [Skip](../skips/index.md) that uses it.
