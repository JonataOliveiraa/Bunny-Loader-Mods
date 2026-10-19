# Mita NPC

The four MiSide town residents from **Mita NPC 0.0.9**, adapted for Terraria Mobile with Bunny Loader.

- **Mita:** Game Cartridge boomerang, Carrot, Travel Ring after all mechanical bosses, and the Psycho Knife during a hardmode Blood Moon.
- **Cappie:** Mita's Cap, a wearable vanity hat.
- **Mila:** Mila's Book and four permanent manuals granting 10% damage to melee, ranged, magic or summon weapons. Each manual can be used once per character.
- **Player (MiSide):** Game Console, Ramen and Alarm Clock. The console summons the glowing Fly pet; the clock summons Broken Mita.

Residents can move in during the day when suitable empty houses are available. Complete Brazilian Portuguese, Spanish, Russian and English text is included, covering item tooltips, dialogue, bestiary entries and happiness. Japanese/Russian Mita voices, textures, shops and prices are included. Player (MiSide) has Russian voices only, as in the original. Voices remain in their original recorded languages.

## Travel Ring on mobile

Equip the ring in an accessory slot. Open **Settings > Controls**, choose a custom layout, select **Edit** and add the **Travel Ring** action. Aim the cursor and tap the button to teleport. The original collision checks and 20-second Chaos State cooldown apply.

## Port details

Town melee combat uses a small client-independent projectile on the host because Bunny Loader does not expose the original town melee callbacks. Broken Mita's ground/flying behavior and the cartridge's return behavior are implemented in JavaScript. Buff and pet icons retain their animation where supported; character preview bobbing is not included.

Original mod and assets by **rzc0d3r**. Bunny Loader port by **Potato**. The original MIT copyright notice is included in `license.md`.

[Original Workshop page](https://steamcommunity.com/sharedfiles/filedetails/?id=3402763063) | [Original source code](https://github.com/rzc00d3r/MitaNPC)
