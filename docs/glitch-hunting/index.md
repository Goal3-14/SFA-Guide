---
tags:
  - advanced
---

# Glitch Hunting

Deep technical writeups for people investigating new tech. This section is **not** beginner-friendly &mdash; assume the reader is comfortable with memory editing, debuggers, and reading disassembly.

Concrete user-facing setups belong in [Glitches](../glitches/index.md) and [Skips](../skips/index.md). This section is for the *why* and the *how-it-was-found*.

## What goes here

- Detailed engine analysis (collision handling, cutscene state machines, memory layout).
- Investigation logs and dead-ends &mdash; documenting what didn't work is valuable.
- Tooling notes for finding new tech (Dolphin hooks, RAM watch setups, useful breakpoints).
- Frame-data tables, address maps, decomp references.

## Pages

<!-- TODO: link writeups as they are added. One md file per topic. -->

- <!-- e.g. - [Out-of-bounds geometry analysis](out-of-bounds-geometry.md) -->
- <!-- e.g. - [Save/load state side effects](save-load-state-side-effects.md) -->
- <!-- TODO -->

## Adding a writeup

1. New `.md` in this folder. Descriptive lowercase-hyphen name.
2. Link from the list above and from any related [Glitch](../glitches/index.md) page (the "See also" section).
3. Add to `mkdocs.yml` `nav:`.
4. No content rules &mdash; write long, include raw notes, link external resources freely.
