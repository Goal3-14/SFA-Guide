# Skips

Concrete, applied uses of glitches and tech &mdash; the **where and when**. Each skip is one `.md` file. A single skip can be referenced from multiple [Categories](../categories/index.md) and from the [Location](../locations/index.md) where it happens.

## How this section is organized

- **One `.md` per skip**. No subfolders.
- Tag each skip with the categories that allow it: `any%`, `100%`, `glitchless`. A skip in two categories is just two tags.
- Tag with `glitch` if the skip relies on a glitch (and link the [Glitch](../glitches/index.md) page).
- Images go in [`docs/skips/images/`](images/) prefixed with the skip name.

## Known skips

<!-- TODO: list each skip's md file here. See example-skip.md for the template. -->

- [Example Skip](example-skip.md) &mdash; _template file_

## Browsing skips

You usually arrive at a skip from one of three places:

- A **[Category route](../categories/index.md)** lists skips in run order.
- A **[Location](../locations/index.md)** page lists skips in that area.
- The **[Tags](../tags.md)** index lets you see every `any%` skip, every `glitchless` skip, etc.

## Adding a new skip

1. Copy [`example-skip.md`](example-skip.md).
2. Rename to the community name (lowercase, hyphens).
3. Set the category tags in frontmatter.
4. Link the [Glitch](../glitches/index.md) it relies on, if any.
5. Link the [Location](../locations/index.md) it happens in.
6. Add it to this index, to the relevant location's "Skips" section, and to any category route that uses it.
7. Update `mkdocs.yml` `nav:`.
