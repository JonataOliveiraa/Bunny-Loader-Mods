# Shared Inventory

On multiplayer, the player hosting the world is the **source of truth**. The host's
inventory becomes everyone's inventory: whatever a client picks up, drops, crafts or
moves between slots goes to the host and comes back to everyone.

## What is shared

- **Inventory** (all slots, including coins and ammo)
- **Armor and accessories**, and **vanity**
- **Pets and light pets** (the pet/light slots)
- **Dyes** (`dye` and `miscDyes`)
- **Life and mana**: one shared pool. Damage, healing, mana spent and regeneration
  from any player change the same value.

## Joining a host's world

- The items you already had go into the host's empty inventory slots. This happens
  **once per character** (it is marked in the save).
- Your inventory then becomes the shared one.
- Items that do not fit are dropped, and the chat tells you how many did not fit.

## Known limits

- **Extra data on modded items** (anything a mod stores inside the item) does not
  travel: the item arrives with its type, stack and prefix. Vanilla items come through
  whole.
- **Items on the cursor** (held with the mouse or finger, outside a slot) are not synced
  until they go back into a slot.
- **Safes, piggy banks and chests** are not included: they work as they do in the game.
- Two players changing the **same slot at the same instant**: the one the host processes
  last wins, and everyone ends up with that value.
- **Everyone needs the mod and the same content mods** (a Bunny Loader rule).

## How to test

1. Install the mod on the host and on the clients (in `bunny_packs/`, or import the zip).
2. Use test characters. Clients' items go to the host when they join.
3. The host opens the world in multiplayer; the clients join.
4. Pick up, drop and move items, and take damage or spend mana on both sides. Check that
   the inventory and life match everywhere.

Logs: `bl.log` lines appear in the game's log file, starting with `Shared inventory: ...`.
