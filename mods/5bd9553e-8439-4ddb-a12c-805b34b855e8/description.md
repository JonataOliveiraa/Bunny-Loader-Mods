# Boss Checklist

Keep track of every boss, mini-boss and event in your world. The Boss Log is a
book with your whole progression, how to summon each entry, what it drops and
how well you fought it, laid out like the PC mod and made for touch.

## Opening the Boss Log

- **Touch buttons**: add the **Boss Log** and **Boss Checklist** actions to
  your controls in the game's controls editor (Settings > Controls, a custom
  layout, Edit: the mod actions are at the end of a slot's action list). Each
  button opens and closes its screen.
- Opening the Boss Log or the checklist closes the inventory (and the other
  one). Tap outside the book, or open the inventory, the map or the pause menu
  to close them.

## Touch controls

| Gesture | What it does |
| --- | --- |
| Tap | Opens a page, picks a tab, toggles a filter or pins an item tooltip. |
| Hold your finger | Shows the tooltip of what is under it, and the head icons of a Table of Contents entry. Hold for half a second to read it without tapping. |
| Long-press | The right click of the PC version: marks or unmarks a Table of Contents entry as defeated, compares a record category, hides an entry of the classic checklist, and, with **Reset Options** on, clears marks, hidden entries, items and records. |
| Drag | Scrolls lists and long texts. |
| Swipe left or right | Turns the page. |

## The book

- **Table of Contents**: pre-Hardmode and Hardmode lists with check marks, the
  next entry highlighted and progress bars (tap a bar to switch between entry
  types and mods). The tab on the left opens the filters for bosses,
  mini-bosses and events, and the hidden list where you choose which entries
  are hidden.
- **Indicators** at the top right toggle Bosses Only, the automatic checklist
  and progressive mode.
- **Entry pages**: portrait, head icons and three sub-pages:
  - **Spawn Info**: how to summon it, its spawn items and their recipes with
    ingredients and crafting stations.
  - **Loot & Collectibles**: the treasure bag, relic, pet, trophy, mask, music
    boxes, expert item and every drop. Items you have obtained are checked,
    and master-only, expert-only and locked items are marked.
  - **Records**: previous attempt, first victory, personal best and, in
    multiplayer, world records: fight time, hits taken and kills/deaths.
    Mini-bosses show your kill count, events show their banners.
- **Progressive mode** hides the names and pages of what you have not defeated
  yet, so you can play blind. You are asked about it the first time you open
  the log.
- **Credits** list the original contributors and every mod that registered
  entries.

## Other features

- **Classic checklist**: a compact panel on the right side with the checklist.
  Tap an entry to see how to summon it and **More Info** to open its page in
  the Boss Log; long-press an entry to hide it.
- **Boss radar**: arrows at the screen edges point to bosses that are off
  screen.
- **Map items**: treasure bags and lunar fragments (and, optionally, Shadow
  Scales and Tissue Samples) show on the map.
- **Chat messages** when a boss leaves, when a part like Skeletron's hands or a
  Celestial Pillar is defeated, and when a moon event ends.
- **Respawn sounds** in the last 3 seconds of your respawn timer.
- Everything can be turned on or off in the two mod configs.

## For mod makers

Other mods can add entries with `Call`, using the same messages as the
original mod: `LogBoss`, `LogMiniBoss`, `LogEvent`, `SubmitEntryLoot`,
`SubmitEntryCollectibles`, `SubmitEntrySpawnItems`, `SubmitEventNPCs` and
`GetBossInfoDictionary`. Calls that add data must be sent before
`AddRecipes` (from `PostSetupContent`).

```js
const ref = new Ref();
if (ModLoader.TryGetMod('bosschecklist', ref)) {
    ref.value.Call('LogBoss', bl.mod, 'MyBoss', 5.5, () => MyWorld.downedMyBoss, [ModContent.NPCType(MyBoss)], {
        spawnItems: [ModContent.ItemType(MySummon)],
        collectibles: [ModContent.ItemType(MyTrophy)],
        spawnInfo: 'Use [i:' + ModContent.ItemType(MySummon) + '] at night.',
    });
}
```

`GetEntry` (with an entry key such as `Terraria KingSlime`) and `IsDowned`
return a single entry.
