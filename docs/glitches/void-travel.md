---
tags:
  - glitch
  - any%
---

# Void Travel

The core mechanic underlying [Any%](../categories/any-percent.md).

## What it is

Every map in the game is on **one giant map**. The area separating the different main maps is referred to as the **void**. By [air swimming](air-swim.md) we should be able to swim between different maps as they're on the same map.

Normally, if we leave the confines of any main map and enter the void, the game immediately softlocks us. **Mounted state bypasses this** &mdash; the void doesn't softlock you while riding the bike or a mammoth.

## Dismount glitch

To freely airswim in the void, we need the game to think we're riding an object while playing as Fox. The **dismount glitch** does exactly that: start a cutscene such as collecting a fuel cell or feeding Tricky to get out of the mount, but the game still considers you mounted. From there you can freely [air swim](air-swim.md) anywhere.

## Two big caveats

### Triggers

While in the dismount state Fox is **not able to hit any triggers** &mdash; only the object the game thinks he's riding can. But that object is typically deloaded back where you first did the dismount glitch and can't reach the area you're at anyway.

### Deloaded state

The areas we arrive at are in a **deloaded state** similar to memory leak &mdash; Fox can't interact with anything, and most importantly cannot start the Test of Knowledge without crashing the game.

We need a checkpoint to respawn and load the area properly. Since only the mount can hit checkpoint triggers and the mount is unloaded, we get a new object or random memory data to replace the mount coordinates &mdash; the game treats this new data as the mount's coordinates. By manipulating memory, we can land those coordinates on a useful trigger to claim a checkpoint, then die (or [ESW](../skips/esw.md) a different file there). This is the [K5E](../skips/k5e.md) procedure.

<!-- TODO: deeper engine writeup of how the dismount + memory replacement actually works. Source guide had this as a placeholder for further detail. -->

## Used by

- [K5E](../skips/k5e.md) &mdash; the Any% finisher.
- [Any% route](../categories/any-percent.md)
