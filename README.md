# Combat Meter for Champions Online

A lightweight, always-on-top damage meter for Champions Online, in the style of Details! and ACT. It reads the game's combat log live and shows who is doing what, themed to match the game's own UI.

**Download:** grab `CombatMeter.exe` from the [latest release](../../releases/latest). No install and no Python needed. Run CombatMeter.exe in it's own folder.

## Meters
- **Damage, Healing, Taken and Deaths** views, switched with buttons in the header.
- Ranked bars with total, DPS and percentage for each player.
- Smooth scrolling and a gold, stylized selected button.

## Breakdowns
Click a player to open a breakdown window (it can open to the left or right of the meter):
- **Abilities**: damage per ability with hits, average, damage type and Avg Resist.
- **Targets**: per-target damage, DPS and Avg Resist. Target DPS runs from your first non-zero hit to your last hit on that target.
- **Last 50 hits** on a target, including damage type.

## Segments (encounters)
- Combat is split automatically into segments after a configurable idle gap.
- Pick a segment, or Overall, from the segment dropdown.
- Combine, delete and rename segments, or clear them all. Shift+click selects a range, and deletes ask for confirmation.
- Starting the meter mid-combat immediately begins a new segment and shows it.

## Multiple windows
- **Create new window** opens another meter, for example Damage and Healing side by side.
- Place it above, left, right or below the main window.
- Extra windows are always on top and keep their own view buttons, minimize and close.

## Customization (Settings)
- **Toggle column**: choose which columns show in the main list, ability breakdown, target breakdown and last-50-hits window.
- **Style**: size, opacity, global font (Arial by default), and a bar color for each damage type.
- **Minimize toward**: top, bottom, left or right.
- **Breakdown shows** on the left or right, **New segment after** a set idle time, **My character** highlighting, and **Always on top**.
- Window size, position and settings are remembered between runs.

## Logs
- Watches your Champions Online combat log folder (**Log folder...**) and follows new logs automatically.
- **Open file...** analyzes a specific log, even outside the game. If a newer log then appears in your log folder, it switches to that one.

## Auto-update
- On start and every six hours, the app checks this repository for a newer version.
- A popup asks "Yes, update now" or "No, not now". On Yes it downloads, replaces itself and restarts.
- **Check for updates** in Settings checks on demand.

## For maintainers
1. Set `VERSION` in `combat_meter.py`.
2. Build with `build_exe.bat`.
3. Publish a Release containing `CombatMeter.exe`.
4. Update `version.txt` last (the first line is the version number).
