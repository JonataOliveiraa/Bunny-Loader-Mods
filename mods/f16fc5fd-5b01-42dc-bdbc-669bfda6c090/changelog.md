# Changelog

## 1.1.1

- Fixed the drawing of many items: spears from mods sit in the hand the right
  way round, and other mods' sprite turns always apply.

## 1.1.0

- New **Turn Sprite** button (and `/wo turn`): turns the held item's sprite in
  90° steps and saves it for that item, for items drawn the wrong way round.
  **Clear Override** removes it.
- Other mods can set it with `Call('RegisterItemSpriteTurn', item, degrees)`.
- Shorter settings labels and titles in every language.

## 1.0.1

- Fixed the drawing of many items: spears use their projectile sprite in the
  right hand and direction in the combat and rest poses, like the original,
  and the item is hidden while sleeping in a bed.
- Settings translated to 12 languages.

## 1.0.0

- Port of *Weapon Out Lite* (tModLoader) to Bunny Loader: all 61 poses, the
  item classifier, the combat poses with the put-away animation, the arrow on
  the bow and item glow.
- Both original configs on one screen; the inventory eye button became the
  `/wo` command and two buttons in the config.
- Per-item overrides are saved in `ItemOverrides.json`.
- The original `Call` API (Register*, HidePlayerHeldItem, RegisterCustom*).
- Synced in multiplayer (visible item, pose and combat timer).
