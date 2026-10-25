# Quality of Bunny

Quality-of-life tweaks for Terraria Mobile, **inspired by Quality of Terraria** (tModLoader, by 局长 and contributors, MIT). Nothing is on by default: open **Mod Configuration** and switch on only what you want. Every option is its own toggle.

## Death and combat
- **Full HP on respawn**
- **Faster respawn**: the respawn timer runs at 2x.
- **Keep buffs on death**
- **No tombstones**
- **No damage variance**: weapons hit for their exact damage.

## Buffs and stations
- **Infinite potions**: carry enough of a potion and its buff never runs out (you choose how many).
- **Infinite stations**: all Campfires, Heart Lantern, Star in a Bottle, Sunflower, Bast Statue, Sharpening Station, Ammo Box, Bewitching Table, Crystal Ball, Slice of Cake, War Table and the candles. Keep one in your inventory and the buff is permanent, with no countdown, exactly as if you stood next to it.
- **Portable crafting**: crafting stations in your inventory count as nearby.

## World
- **No biome spread**: Corruption, Crimson and Hallow stop spreading.
- **Pylons: no NPCs**: pylons work without the town NPC requirement.
- **Infinite angler quests**: turn in a quest and the Angler has the next one right away, no waiting for the next day. Single player or host only.
- **Glowing life crystals and fruits**: life crystals glow red and life fruits glow green. say goodbye to spelunker potions!

## Items
- **Show mod name**: tooltips of modded items say which mod they come from.

## Notes
- Each feature hooks the game on its own. If your game build lacks something a feature needs, that feature is skipped and the log says so (search for `[QoB]`).
- Other mods can add support through `Mod.Call` with the same names as Quality of Terraria: `IgnoreInfItem`, `AddPotion`, `AddStation`, `AddPortableCraftingStation`.
- Options are per device; in multiplayer each player sets their own.
