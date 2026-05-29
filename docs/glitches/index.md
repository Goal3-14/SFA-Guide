# Glitches

The **mechanics** of every glitch &mdash; what it is, how to trigger it, and why it works. Concrete applications (which skip uses which glitch at which point in the run) live under [Skips](../skips/index.md).

## Pages

| Glitch | What it does |
|---|---|
| [Air Swim](air-swim.md) | Lets Fox swim in the air after going off the TTH waterfall at the right spot. Foundation for [CCE](../skips/cce.md), [DIME](../skips/dime.md), and most major glitched routes. |
| [Ball Entanglement](ball-entanglement.md) | Hotkey ball + frame-perfect pickup A/Y. Enables [FGL](../skips/fgl.md) and [Ball Hover](../skips/ball-hover.md). |
| [Bike Flag Glitch](bike-flag-glitch.md) | Lets you drive the IM bike freely outside the race. |
| [Camera Lock](camera-lock.md) | Freeze the camera; many triggers fire on camera position, not Fox. Enables [Beacon Skip](../skips/beacon-skip.md), [QE Cam Lock](../skips/qe-cam-lock.md), [GQE](../skips/gqe.md), [OFP Cam Lock](../skips/ofp-cam-lock.md). |
| [Damage Clip](damage-clip.md) | v1.0-only barrel collision lets you push yourself out of bounds in IM. Required for [Any%](../categories/any-percent.md). |
| [ESW Checkpoints](esw-checkpoints.md) | Persistent checkpoints that survive quitting to menu. Underpins [ESW](../skips/esw.md), [RESW](../skips/resw.md), [Layered ESW](../skips/esw-layered.md). |
| [Mammoth Clip](mammoth-clip.md) | The DIM mammoth can partial-clip into walls. Underpins [Cog Skip](../skips/cog-skip.md) and [Bike Skip](../skips/bike-skip.md). |
| [Void Travel](void-travel.md) | Mounted dismount lets Fox roam the void without softlocking. Underpins [K5E](../skips/k5e.md) and Any%. |
| [Void Walking](void-walking.md) | <!-- TODO: pending writeup --> |
| [Waterfall Jump](waterfall-jump.md) | Precise jump off the WC waterfall to land OOB. Underpins [REKE](../skips/reke.md), [ZGSS](../skips/zgss.md), [SGQL](../skips/sgql.md). |

## Adding a new glitch

1. New `.md` in this folder, lowercase-hyphen filename.
2. Add to the table above and the `nav:` in `mkdocs.yml`.
3. From every [Skip](../skips/index.md) that uses it, link back to this page in the **Glitch used** field at the top.
