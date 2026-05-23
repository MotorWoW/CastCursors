# Cast Cursors

<img width="817" height="537" alt="Screenshot_20260522_122350" src="https://github.com/user-attachments/assets/21e2f170-8fa9-4eb6-b311-c1d79b1fe1d6" />

A lightweight World of Warcraft addon that draws a glowing ring around your mouse cursor, with optional cast bar visualization.

Originally built as an accessibility aid — the ring makes it much easier to keep track of your cursor during busy combat encounters.

## Features

- **Persistent cursor ring** — a glowing ring follows your cursor at all times
- **Cast animations** — the ring animates while you cast or channel:
  - **Sweep** — ring drains clockwise (or counter-clockwise) as the cast progresses, then snaps back full on completion
  - **Shrink** — ring collapses inward as the cast progresses
  - **Expand** — ring grows outward as the cast progresses
  - **Pulse** — ring pulses, faster as the cast nears completion
  - **None** — ring stays constant (pure cursor aid, no cast indication)
- **Separate modes for casts and channels**
- **Optional completion flash** — brief flash when a cast finishes
- **Optional orbiting sparkle dot**
- **Optional spell name label**
- **Full options panel** — Interface > AddOns > Cast Cursors, or `/cc`
- **Profile support** — per-character and per-spec configurations

## Installation

Install via the CurseForge app or manually drop the `CastCursors` folder into:
```
World of Warcraft/_retail_/Interface/AddOns/
```

## Usage

Type `/cc` or `/castcursors` to open the options panel, or navigate to **Interface > AddOns > Cast Cursors**.

## Compatibility

Works in Retail WoW (Midnight / 12.x), Classic, Burning Crusade Classic, Wrath Classic, Cata Classic, and MoP Classic.

Uses only `UnitCastingInfo("player")` and `UnitChannelInfo("player")` for cast data — both are explicitly permitted by Blizzard's addon API restrictions. The addon is purely cosmetic and will never be affected by combat API changes.

## Credits

Built with [Ace3](https://www.wowace.com/projects/ace3) libraries.
