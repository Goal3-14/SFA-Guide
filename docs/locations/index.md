# Locations

General info on each area &mdash; what happens there during the run, what skips apply, and what you should know when arriving fresh.

## How this section is organized

- **One `.md` per location**, flat. No subfolders &mdash; the file name *is* the location name (e.g. `dark-ice-mines.md`).
- Images go in [`docs/locations/images/`](images/) with the location name as a prefix: `dark-ice-mines-room-3.png`.
- Skip-specific writeups live under [Skips](../skips/index.md). Each location page links to skips that happen there; it does not re-document them.

## Areas

<!-- TODO: list every area as a flat link. Add as you migrate content. -->

- [Overworld](overworld.md) &mdash; _example file showing the template_
- <!-- e.g. - [Krazoa Palace](krazoa-palace.md) -->
- <!-- e.g. - [Dark Ice Mines](dark-ice-mines.md) -->
- <!-- TODO -->

## Adding a new location

1. Copy [`overworld.md`](overworld.md) as a template.
2. Rename to the in-game name (lowercase, hyphens). Use the official name where there is one.
3. Fill in the sections.
4. Link the [Skips](../skips/index.md) that happen in this area.
5. Add it to the list above and to `mkdocs.yml` `nav:`.
