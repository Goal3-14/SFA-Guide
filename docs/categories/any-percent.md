---
tags:
  - any%
  - routing
  - advanced
---

# Any%

This category uses an SRM and precise memory manipulation to beat the game in **under an hour** (or just over an hour, depending on route). It contains some of the most precise tricks in the game with the lowest consistency out of any category.

**Required version:** v1.0 only. See [Versions](../general-info/versions.md) for why.

## Hardware requirements

For Any% you will need a v1.0 copy of the game. If you are able to run this game well on emulator, it is **highly recommended** that you learn this run on emulator due to the practice tools available &mdash; see the [Any% practice tool](../tools/any-practice-tool.md) and [Any% Heap Visualiser](../tools/any-heap-visualiser.md). These let you drill the memory manipulation without having to do the full swim each time.

## Overall glitch and route overview

Every map in the game is actually on one giant map, with the area separating the different main maps being referred to as **the void**. By air swimming, we should be able to swim between different maps as they are on the same map. We want to air swim from Ice Mountain to the 5th Krazoa Shrine, as collecting K5 is what triggers the game's end sequence.

However, if we leave the confines of any main map and enter the void, the game will immediately softlock us. To freely airswim in the void we need the game to think we are **riding an object** such as the bike or a mammoth &mdash; the void won't softlock you while mounted.

We use the [dismount glitch](../skips/bike-skip.md) to play as Fox while the game still thinks we're riding them, by starting a cutscene such as collecting a fuel cell or feeding Tricky. Once we do, we can freely [air swim](../glitches/air-swim.md) to anywhere in the game. See [Void Travel](../glitches/void-travel.md) for the deeper mechanics.

### Loading and trigger problems

There are issues to get around before we can play in these areas normally:

- While in the dismount state Fox is not able to hit any triggers, only the object the game thinks he's riding can. But this object is typically deloaded back where you first did dismount glitch and is unable to reach the area you arrived at, since the bike is still affected by gravity during the air swim.
- The areas we arrive at are in a deloaded state similar to memory leak &mdash; Fox is unable to interact with anything, and most importantly cannot start the Test of Knowledge without the game crashing.
- We need a way to hit a checkpoint to respawn in the area properly. Only the mount can hit checkpoint triggers, and the mount is unloaded once we leave the original map.

The solution: by manipulating memory, we can get random data or an object to replace the mount's coordinates with values that hit the K5 trigger. We can then die (or ESW) to respawn properly. See [K5E](../skips/k5e.md) for the full procedure.

### The full Any% loop

1. Play the game normally until IM.
2. Open the bike race cave door.
3. Do [Gate/Damage Clip](../skips/damage-clip.md) to get out of bounds &mdash; the cannon hits you while holding a barrel, you drop the barrel onto yourself, and the push clips you OOB.
4. Do [Seam Drop](../skips/seam-drop.md) &mdash; extremely precise position and angle to land on a specific pixel out of bounds, drop into the cave, and trigger [Bike Flag Glitch](../glitches/bike-flag-glitch.md) to drive the bike freely.
5. Get a fuel cell to dismount the bike, gain air swim, and swim to the K5 shrine.
6. Fire the fire blaster &mdash; the fire blast shots replace the mount object in memory.
7. Since the fire blast shot went through the trigger, the game gives us the checkpoint. Die and respawn in K5 to collect the 5th Krazoa Spirit.

## Required tricks

| Trick | Purpose |
|---|---|
| [Gate / Damage Clip](../skips/damage-clip.md) | Get OOB in IM |
| [Seam Drop](../skips/seam-drop.md) | Get into the cave for Bike Flag Glitch |
| [K5E](../skips/k5e.md) | Memory manipulation and void travelling to K5 |
| [WC Escape](../skips/wc-escape.md) | Escape WC after the game glitches (no Tricky) &mdash; **Normal Route only** |

## Routes

The category has 3 routes with significant differences in difficulty for Seam Drop, K5E, and WC Escape.

### 2 File Route

Allows you to **skip WC Escape entirely**. WC Escape has to be done back-to-back after K5E, and failing it requires you to redo the whole of K5E &mdash; so skipping it makes the route significantly easier. This route uses a second file and plays through the game up to Dark Ice Mines before doing K5E. **~20 minutes slower**, much safer, recommended for learning.

### Normal Route

Does WC Escape after K5E. More difficult, but allows a **sub-hour** finish (best ~52 minutes).

### TK5E

Doesn't open the cave door or watch the bike cutscene, but has to do Gate Clip and Seam Drop during the memory manipulation &mdash; meaning **all 3 big tricks in a row**, with Seam Drop on a strict time limit. Allows a ~**50 minute** PB on a perfect run.

The RTA memory manipulation for this route is currently in development, so this route cannot currently be done and isn't covered in this guide.

## Game versions

See [Versions](../general-info/versions.md). Any% **only runs on v1.0** because [Damage Clip](../skips/damage-clip.md) requires Fox's collision with explosive barrels, which only exists in v1.0.

JP text saves 4&ndash;5 seconds over English text.

## See also

- [Any% No K5E](any-percent-no-k5e.md) &mdash; the multi-file category for those who don't want to do K5E.
- [Any% WR History video by Zcanann](https://youtu.be/L8uDuCK6VnI)
- [Any% No K5E TAS (commentated)](https://youtu.be/a0L_ON_r8Mg)
