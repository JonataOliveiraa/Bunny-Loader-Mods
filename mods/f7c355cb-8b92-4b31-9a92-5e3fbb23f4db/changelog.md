# Changelog

## 1.0.5 - 2026-11-10 - Loading before the title screen

**Fixes**
- The opening screen (the logo before the menu) now waits for Split to finish loading. On slower phones the title screen opened with the mod only half loaded, and entering a world at that point left you without the mod's items, blocks and NPCs. The opening may take longer than before: it is the time the mod needs.
- If someone still enters a world before the mod has finished loading, a red warning shows in game: exit without saving and enter again so you do not lose mod items.

## 1.0.4 - 2026-11-09 - Weapon review

A review of every weapon (and the rest of the mod) against the functions mobile Terraria actually has.

**Fixes**
- Sounds that never played: Ball of Flesh missile explosions, photo album clicks and Basaltite pots breaking (which also dropped no dust or debris).
- Paraffin: the body afterimage (spinning, running and the final cough) threw an error.
- Starshroom: the extra sentry was not created.
- Space Cell Phone: the info displays (watch, compass, depth and the rest) did not work.
- Frostbite Sapling threw an error when trying to grow.
- Boss Checklist: summon items showed without their rarity color.
- The Magician threw an error when leaving at the end of the day (and in multiplayer his departure did not reach other players).
- The Dazzler shot's flash did not follow the shot's own transparency.
- Preventive fix for calls that passed more arguments than mobile expects: running out of ammo with ranged weapons (Balloon Gland, Lava Blaster, Heartmelter, Starstorm, Flamaxe and others), the Crab Heart and several buffs (Heavy Metal, heavy weapon stances, Stargazer, Jelly Bond, the teas, Molten Ring, Gelid Healing, Toxic Rush, Firecaster's Blessing, House Of Evil and some enemy debuffs).

**Performance**
- Two internal caches emptied themselves between frames and now keep what they should: less work per player every frame, mainly in multiplayer.
- Split's ammo weapons made the game run an extra ammo check on every shot, from any weapon. Not anymore.

## 1.0.3 - 2026-11-09 - Fixes and performance

Fixes for the errors reported in 1.0.2, including the crash when summoning vanilla bosses, and more performance.

**Performance**
- Systems that used to run all the time now only run when used: minion and sentry accessories, the Stargazer armor, Flandre, Mana Overload, armor prefixes and the Possessed Armor. Spawning projectiles is lighter in fights with lots of shots.

**Fixes**
- Summoning Plantera, Golem or other vanilla bosses that create parts (hooks, hands, head) crashed the game.
- Frosty Glove and Tearful Scepter threw an error on their first shot.
- Starshroom threw an error with a sentry out.
- After fighting One-Shot, equipment threw an error that kept repeating.
- Near mod crafting stations, an error kept repeating.
- The Collector could throw an error when closing the exchange.
- Red Patch: the extra strike did not trigger with melee weapons.

## 1.0.2 - 2026-11-08 - Fixes and performance

A general pass over the beta: crashes and errors that showed up while playing, weapons out of place, and a lot of performance work, mainly for weaker phones and multiplayer.

**New**
- Boss Checklist support: with the mod installed, the Boss Log lists The Spirit, One-Shot, Menace and Paraffin, plus the mini-bosses Colossus, Breathtaker and Fairyfly, with how to summon them, summon items, despawn message and whether they were defeated.

**Performance**
- Automatic effect quality: when the game drops frames, the amount of Split particles, dust and lights goes down on its own and comes back gradually when the game recovers.
- A per-frame limit on Split dust and lights, following the visual effects intensity option.
- Much lighter multiplayer: each extra player in the world costs far less than before.
- Less work every frame for particle effects, boss relics, The Spirit's projectiles, the Master Spirit pet, Paraffin's bone serpents, Bits of Sky on the ground, touch buttons, and accessories and armors that only need an occasional check.
- Monolith Tome: the aura is lighter in multiplayer.

**Fixes**
- Opening the housing menu with Menace (the spirit chained to the NPC) crashed the game. Split NPCs that are not residents (Menace, Menacing Person, Twilight Walker and the Spirit and Paraffin ones) no longer show up in the housing menu.
- Saving the world could throw an error because of Split NPC banners.
- The Spirit, Menace and Breathtaker now leave when you die (before, they stayed in the world). The Spirit also leaves if you get too far away, as in Split.
- Weapons that floated ahead of the player's hand: Arctic Oscillation, Poison Break, Zircon Spear, Ceremonial Knife, Chikage, Swapper, Weather Rocket, Eye of Belial, Photo Rifle, Razzle-Dazzle, Frostflake Fan and Monolith Tome.
- Starstorm: the shot's flash no longer drifts away. Arachnid Rod: the shell follows the right arc. Racquets follow the player without getting ahead.
- Garlic: can be thrown again and, when thrown in the Corruption or Crimson, summons the Twilight Walker as in Split.
- Mounted Sheep: the body is visible again. The rainbow-wool Sheep no longer throws an error.
- The happiness button of Split NPCs (Twilight Walker, Menace, Magician and others) showed broken text instead of a line.
- Basaltite and Stranded Ship biomes threw errors in some worlds.
- Errors when used or on screen: Ballistick dash, trails of Paraffin and minion projectiles, Hyperboloid (baseball), Overgrowth (secondary attack), Flare Blade, Starstorm and Flamaxe (homing projectiles).
- Errors that kept repeating: Mask of Evil and Avenger Mask (they now raise minion damage and whip speed) and 7th Element during Potion Sickness.
- Moon Rock (Moon Wheel) did not recognize the weapon's class.
- Frostflake Fan did not apply the mana regeneration delay.

## 1.0.0 - 2026-11-01 - Beta: up to Paraffin

The first complete version of the port: all of Split 1.0.11 up to Paraffin, reviewed and optimized for mobile.

**New**
- **Magician**: a hardmode night visitor who arrives near the Guide and leaves in the morning. The original's full shop, with stock that changes every day.
- **Leviathan** and **Schwarzwelt**, the hardmode heavy greatswords: Leviathan grants Agile Stance on hit; Schwarzwelt releases four blood daggers per swing.
- **Sheep**: a Snow critter with 13 wool colors (three of them glow). Catch it with a net and ride it; the One-Shot's sneakers make it run.
- **Photography**: the 12 photos of Split creatures now count in the album, so its pages can be completed.
- 7 hardmode armor prefixes, the Ancient Blast Forge, the Holographic Board and the Heavy Metal buff of heavy weapons.

**Fixes**
- Heavy swings to the left came out mirrored; they now follow the player's side and, on the backswing, the blade flips with the edge facing out.
- A character picked before Split finished loading came without its mod items.
- Paraffin now dies like in the original: she explodes, leaves a Basaltite heart behind and flies off spinning; the loot drops where she died.
- Menace now has the original death animation: she explodes in sparks, falls, hops away saying her last line and gets struck by lightning, dropping the umbrella and her charred body.
- Enemies that died without gore now drop the original pieces: Cave Imp, Crabcannon, Faceless Pirate, Headless Pirate, Husk, Idler, Moonwalker, Muskeleton, Savage, Shutterbug, Toiler and Unfairy.
- The Toiler explodes its pot on death again, with shards and fire; Basaltite pots break into pieces and the common one drops coins instead of a geyser.
- A broken Monster Cage drops a bomb that falls and explodes before releasing the monster; Paraffin's cage breaks with a shake, an explosion and debris.
- One-Shot's Ice Prison sheds ice shards on each crack and when it breaks.
- The Firecaster Scepter totem grants Firecaster's Blessing (+10% damage, +5 defense, life and mana regen) to whoever stands nearby, like the original.
- Poison Break gained Toxic Rush: each debuff on the target makes its swings faster.
- Leftover test items were removed.
- Paraffin's second form entrance has its explosion and camera focus again.
- The boss camera focus (Spirit, One-Shot, Menace, Paraffin) and screen shake barely showed: the game repositioned the screen before drawing.
- Insidious Addiction, the curse from Paraffin turning into the Stalker, had no name or description (Icebreak and Fury Forged too).
- With the Wall of Flesh alive, Paraffin gets scared and runs off to the other side, like in the original.
- The Stranded Ship could be missing from new worlds. Its site now accepts loose cave decorations and, if a world opens without the ship (including worlds made before), it is generated once on entering.
- The Magician and the Schwarzwelt daggers failed to load; the Leviathan blade showed a black square; the Heavy Metal text overflowed its box; the Forest Echo trail threw an error.

**Performance**
- The Paraffin fight, which dropped to 10–20 fps, now stays between 50 and 60 fps most of the time on phones.
- Boss shots, bone serpents and Flandre's waves are updated together, and the most common shots are drawn by the game itself.
- Armor, accessory, buff and potion effects only run while someone uses them, instead of checking every enemy or projectile each frame.
- Minions and homing projectiles use the game's own target search.
- Boss sounds and textures load when entering the world, with no hitches mid-fight, and the game starts up much faster.

## 0.7.63 - Project start (0.6 to 0.7.63)

From scratch up to the version before the beta, Split was brought to Bunny Loader in batches, always from the original Split 1.0.11 code and textures.

- **Bosses**: Spirit, One-Shot, Menace and Paraffin (with all four forms), plus the mini-bosses Colossus, Fairyfly and Breathtaker, and new enemies in every biome.
- **World**: the Stranded Ship in the Underground Snow and the Underworld Domain, with Basaltite, rooms, the Champion Chest and the Blast Forge.
- **Systems**: Photography with the Shutterbug and the album, Mana Overload, heavy swings with stances, the secondary action button and banners.
- **NPCs**: Twilight Walker, Genoshi, Astrologist and Shutterbug, with the original's shops and items in the vanilla NPCs' shops.
- **Items**: hundreds of weapons, armor, combat helmets, accessories, teas and potions, pets, mounts, wings, hooks, furniture, paintings, costumes and music boxes.
