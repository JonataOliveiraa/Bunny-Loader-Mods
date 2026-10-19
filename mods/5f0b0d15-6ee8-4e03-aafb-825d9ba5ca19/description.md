# Tooltip Icon

Adds a small icon to the left of each item tooltip line, like Tooltip Icon for
tModLoader (Nil256): damage by class, critical chance, speed, knockback,
defense, pickaxe, axe and hammer power, range, healing, mana, placeables,
ammo, consumables, equipables, buff time, materials, fishing, prefixes
(with + and −), Expert, Master and research lines.

The Expert, Master, research and boss summon icons are the game's own icons,
as in the original.

## Mod.Call

Recommended icon size: 22 × 22 px. Textures can be a `Texture2D`, an asset
(`ModContent.Request`) or a texture path in your mod.

```js
const ti = new Ref();
if (ModLoader.TryGetMod('tooltipicon', ti)) {
    ti.value.Call('AddNormalIcon', 'mymod', 'MyLine', ModContent.Request('Assets/MyIcon'));
    ti.value.Call('AddPrefixIcon', 'mymod', 'MyPrefixLine', 'Assets/MyIcon', false);
    ti.value.Call('AddFramedIcon', 'mymod', 'MyLine2', 'Assets/Sheet', Rectangle.new(0, 0, 22, 22), Vector2.new(0, 0));
    ti.value.Call('AddCustomIcon', 'mymod', 'MyLine3', (item, line, spriteBatch, position, color) => {});
    ti.value.Call('AddDamageClassIcon', MyDamageClass, 'Assets/Damage', 'Assets/Speed', null, null);
    ti.value.Call('AddConsumableIcon', (item, line) => item.type === myType, 'Assets/MyConsumable');
    ti.value.Call('AddEquipableIcon', (item, line) => item.type === myType, 'Assets/MyEquip');
    ti.value.Call('AddBuffTimeIcon', (item, line) => item.type === myType, 'Assets/MyBuffTime');
    ti.value.Call('AddBossSummoningItem', ModContent.ItemType('MySummon'));
}
```

Call it from `PostSetupContent`.
