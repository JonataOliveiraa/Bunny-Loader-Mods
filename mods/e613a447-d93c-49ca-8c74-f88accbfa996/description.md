Damage numbers popping out of enemies and the damage line of the tooltip take
the color of the weapon's class, like Colored Damage Types for tModLoader
(PvtFudgepants).

| Class | Damage | Crit |
|---|---|---|
| Melee | [c/AA0000:dark red] | [c/FF0A32:red] |
| Ranged | [c/96E19B:light green] | [c/1ECD5A:green] |
| Magic | [c/78BEFF:light blue] | [c/3782FF:blue] |
| Throwing | [c/A06E3C:brown] | [c/DC8700:orange] |
| Summon | [c/FF73C3:pink] | [c/FA50FA:magenta] |
| Sentry | [c/9673FF:lilac] | [c/7846FF:purple] |

The defense line of armor gets a color too.

> [!TIP]
> Hold a weapon from another mod and open the settings: the **Held Item
> Class** section shows the colors of its damage class, ready to change.

## Settings

- Turn the tooltip and damage colors on or off.
- Hide damage numbers (yours and other players').
- **Condense** hits: the number shows after N hits with the total (good for
  very fast weapons), and optionally on kill.
- Every color, one by one, and the **Pillar Colors** preset.
- Default colors for the damage classes of other mods.

## Modded damage classes

Every damage class from another mod gets colors on its own. A mod can register
its own colors:

```js
const cdt = new Ref();
if (ModLoader.TryGetMod('coloreddamagetypes', cdt)) {
    cdt.value.Call('AddDamageType', ModContent.GetInstance(MyClass), [80, 200, 255], [120, 220, 255], [0, 150, 255]);
}
```

The colors are tooltip, damage and crit. White in the tooltip keeps the game's
color. The player can change them in the menu while holding a weapon of that
class; the mod's colors come back with **Mod Defaults**.

## Multiplayer

Other players' numbers also show their class color (dimmer) when everyone has
the mod.

Available in 12 languages.
