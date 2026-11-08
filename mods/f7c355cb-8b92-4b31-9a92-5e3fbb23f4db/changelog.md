# Changelog

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
