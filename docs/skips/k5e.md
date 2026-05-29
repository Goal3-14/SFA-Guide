---
tags:
  - any%
  - advanced
---

# K5E

**Location:** K5 Shrine via void travel &nbsp;&middot;&nbsp; **Glitch used:** [Void Travel](../glitches/void-travel.md)

The **Any% finisher**. Memory manipulation + void travelling to reach K5 and trigger the end sequence.

## The trick at a glance

1. From Ice Mountain (after [Damage Clip](damage-clip.md), [Seam Drop](seam-drop.md), and [Bike Flag Glitch](../glitches/bike-flag-glitch.md)), get a fuel cell to dismount the bike.
2. Gain [Air Swim](../glitches/air-swim.md) and swim to the K5 shrine via [Void Travel](../glitches/void-travel.md).
3. Fire the **fire blaster** &mdash; the fire blast shots replace the mount object in memory with values that will hit the K5 trigger.
4. Since the fire blast shot went through the trigger, the game gives us the checkpoint.
5. Die and respawn in K5 to collect the 5th Krazoa Spirit.

## Video

<https://www.youtube.com/watch?v=cz-9OFrwM78>

## Why memory manipulation is required

The areas we arrive at via void travel are in a deloaded state. Fox is unable to interact with anything; most importantly, he **cannot start the Test of Knowledge without crashing**.

We need a way to hit a checkpoint to respawn in this area properly. Only the mount can hit checkpoint triggers &mdash; but the mount is unloaded once you leave the map and start air swimming.

You are able to get a new object or random memory data to replace the mount coordinates, and the game will treat that replacement data as the mount's new coordinates. By **manipulating memory**, we can get random data or an object to replace the coordinates with values that will hit the K5 trigger, giving us the checkpoint to respawn at.

We can then either die or (if it happens to be an ESW trigger) [ESW](esw.md) a different file to that area.

See [Void Travel](../glitches/void-travel.md) for the deeper mechanics.

## Practice tooling

- [Any% practice tool](../tools/any-practice-tool.md)
- [Any% Heap Visualiser](../tools/any-heap-visualiser.md) &mdash; for emulator users to see memory values during practice.
- [Heap Mapper](../tools/heap-mapper.md) &mdash; for finding consistent SRM setups.

## Followup

In the Normal Route, immediately followed by [WC Escape](wc-escape.md). The 2-File Route skips WC Escape entirely.
