# Cast Cursors

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
- **Completion flash** — brief flash when a cast finishes
- **Orbiting sparkle dot**
- **Optional spell name label**
- **Full options panel** — Interface > AddOns > Cast Cursors, or `/cc`
- **Profile support** — per-character and per-spec configurations

## Installation

Install via the CurseForge app, WoWUp, or manually drop the `CastCursors` folder into:
```
World of Warcraft/_retail_/Interface/AddOns/
```

## Usage

Type `/cc` or `/castcursors` to open the options panel, or navigate to **Interface > AddOns > Cast Cursors**.

## Compatibility

Retail WoW (Midnight / 12.1) only.

Uses only `UnitCastingInfo("player")` and `UnitChannelInfo("player")` for cast data — both are explicitly permitted by Blizzard's addon API restrictions and are unaffected by Midnight's secret-value system, which targets combat-automation data rather than your own cast info. The addon is purely cosmetic and will never be affected by combat API changes.

Spell-school coloring listens to your own entries in the combat log to learn each spell's school (there's no direct lookup API for this in the WoW client). This works everywhere except that a spell seen for the very first time during a boss encounter or Mythic+ run won't get its school color until it's also been cast outside of one, since Midnight masks combat log data in those specific contexts.

## Credits

Built with [Ace3](https://www.wowace.com/projects/ace3) libraries.
