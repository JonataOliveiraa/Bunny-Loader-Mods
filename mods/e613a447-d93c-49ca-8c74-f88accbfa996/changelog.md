# Changelog

## 1.1.0

- New **Held Item Class** section in the settings: hold a weapon of a modded
  damage class to see and change its tooltip, damage and crit colors right in
  the menu. **Mod Defaults** brings back the colors the mod registered.
- Settings in 12 languages, with shorter labels.

## 1.0.1

- Colors sent by other mods through `Call('AddDamageType', ...)` always apply,
  even when they arrive late; only the colors you changed take their place.

## 1.0.0

- Port of *Colored Damage Types* (tModLoader) to Bunny Loader.
- The original's four configs on one screen; the Celestial Pillars preset is a
  button.
- Colors of other mods' damage classes are kept in `CrossModDamageTypes.json`.
