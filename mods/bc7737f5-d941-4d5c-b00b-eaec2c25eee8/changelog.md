# 1.2.10

- Edit mode is much smoother. Dragging a part used to rebuild the whole screen layout on every frame; now only the part you are dragging moves while your finger is down, nothing is recalculated when the finger holds still, and the full layout runs once when you let go.

# 1.2.9

- Quick stack and Similar stack are now one button using the game's own icons. Tap it to stack with the current mode; press and hold it to switch between Quick stack (exact matches) and Similar stack (same category too). The icon changes to show the mode, and the status bar says which one you switched to. If the game's own Similar setting can be found, the button follows it and the hold only tells you so.

# 1.2.8

- New recipe slot at the top of the Storage and Crafting tabs, with a faded hammer icon while empty. Hold an item (from storage, your inventory or the recipe list), move it over the slot and lift: the screen jumps to the Crafting tab and lists every recipe that makes that item or uses it. The item itself never leaves where it was. Tap the filled slot to clear it. The slot can be moved in Edit mode like any other part.
- Removed the Tap mode button: tapping a storage item always takes it out now; finding recipes is done with the slot.
- Removed the "Using" chip that showed up next to Craftable only; the slot shows and clears the item filter instead.
- Opening the screen starts with an empty recipe slot.

# 1.2.7

- Hold an item like in Terraria: press and hold a slot for a moment (about a quarter of a second, without sliding) and its stack is picked up. The icon floats above your finger, bobbing up and down with a little shadow, and its slot dims where it came from. Works on the storage grid, the inventory grid and the installed stations list.
- Lift your finger over the other grid to drop it: storage to inventory takes it out, inventory to storage stores it, inventory to the Stations list installs a station or gravestone, and a station dragged to the inventory takes it back. The grid you are over is framed while it can accept the item. Lift anywhere else to put it back; nothing moves until you drop it.
- A quick tap still works exactly as before, and dragging without holding still scrolls.

# 1.2.6

- The storage grid now shows the empty slots of your storage units as dimmed bordered slots after the items, so you can see how much room is left. They are hidden while a search or category filter is active, and they can't be tapped.

# 1.2.5

- Similar stack: the game's Quick Stack button (and the storage screen's Quick stack) can now also store items "similar" to what is already stored, meaning the same item category (Materials with Materials, and so on; Misc is ignored). Exact matches are always stored first.
- The mod follows the game's own Quick Stack / Similar Stack setting when it can find it, and logs which flag it used. If it cannot, a new Similar: On/Off button next to Quick stack sets the mode by hand.

# 1.2.4

- Quick stack from the game's own button now reaches storage as far as vanilla chests: 600 world units (37.5 tiles) from the player, measured in a circle. It used to cover only a 12-tile square, so most nearby storage was skipped. Only every second tile is scanned (all storage blocks except connectors are 2x2), so the wider range stays cheap.
- The log now records when the game's quick stack button triggers the hook and how many networks and items it handled, to help track down problems.

# 1.2.3

- The Deposit all button is replaced by two PNG buttons: Take all (moves everything in storage into your inventory) and Deposit all (moves your inventory into storage), using the chest-and-arrow icons.
- Sort is now a PNG button, using the old Deposit all texture (renamed Sort.png). Tap it to cycle the sort; the status bar shows the current sort. Order keeps its text button.
- Saved positions for Sort, Order and Deposit are reset once because their sizes changed.

# 1.2.1

- Fixed edit mode: dragging a tab button, the search box, Sort or Order no longer makes it fly away. Their position was being added on top of the previous one on every layout update, so they overshot, jittered, and shoved each other when any other part was moved. Every part now follows your finger exactly.
- Sort: Type and Order now sit on the bottom row next to Quick stack, Take and the tap-mode button by default. They were being pushed off the left edge of the panel.
- Fixed the UI size slider: below 100% the whole screen disappeared. Scaling now restarts the draw batch the way the phone expects (same blend/depth/raster states, only the matrix changes) and always puts it back. If scaling still cannot start, the storage screen shows at 100% and says why in the status bar instead of vanishing.
- While the storage screen is open, the game UI is hidden: hotbars, inventory, resource bars, minimap, settings and builder/info bars, chat, NPC dialog and the other listed vanilla layers. They come back when you close it. Any layer with "buff" in its name is hidden too, and the first time you open the screen in a world the chat says which layer that was (or that none exists), so the real name is confirmed in-game.
- Saved positions of the tab buttons, search box, Sort and Order from older versions are reset once, since they were recorded under the bug. Everything else keeps its saved position.

# 1.2.0

- The Config button and its panel are gone from the storage screen. Those settings now live in the game's Mod Configuration screen (pause menu, or Settings in the main menu): Size (25% to 100%), then one section per tab (Storage, Crafting, Stations) with a size slider for each button group that tab has and its own Reset for part positions, plus Reset all.
- Edit mode: parts can no longer be dragged completely off the panel, panels can't be resized past its edge, and the drag no longer jumps when the UI is scaled below 100%.
- Part size sliders now grow a part inward from the nearest panel edge, and moved or resized parts always stay fully on the panel, so buttons like Sort can't end up at the screen edge.
- Edit mode: every button is its own part now (each tab button, Clear, Sort and Order, each action button, Craft x1 and Craft max...), so they move independently. Size sliders still apply to a group of related buttons, scaled together so neighbours don't overlap.
- Changing the Mod Configuration (or pressing Reset) updates an open storage screen right away.
- If UI scaling can't start, the game now says why and retries.
- The Edit button stays: drag a part to move it, drag a panel's corner (grids, details) to resize it. Buttons and bars are sized from the config sliders instead of by pinching.

# 1.1.0

- New PNG buttons for the Storage, Crafting and Stations tabs, Deposit all and search mode.
- Edit button: opens edit mode. Drag a part to move it, drag its corner to resize it. Tap Done to finish.
- Config button: UI size slider from 25% to 100%, an Individual part scaling switch, and Reset layout.
- Storage and recipe grids: drag, flick, grab the scrollbar or use the mouse wheel.
- More room between the tab row and the search bar.

# 1.0.0 (retextured)

- Renamed to Magic Storage Adaptation; new description and credits.
- Crafting now plays the vanilla crafting sound, and taking, storing, quick stacking and depositing items play the vanilla item-grab sound.
- Storage Unit light now shows its state: green when empty, yellow when partly filled, red when full.
- Category filter buttons use the Magic Storage filter icons instead of item icons.
- Replaced all textures with the Magic Storage texture set (by absoluteAquarian & Contributors, MIT).

# 72

- Crafting tab: the recipe's ingredient list scrolls. Recipes with many ingredients (Crucible of the Cosmos and similar) no longer run over the Craft buttons: drag the list up or down; a scrollbar shows when there is more. Short recipes look the same as before, and stations and missing requirements scroll along with the ingredients.

# 1.0.3

- Touching or hovering an item shows the game's item tooltip: in every grid, on the recipe result, and on each ingredient row.
- Category filters stack: tap several category icons to show items from any of them (tap again to turn one off, All clears them). They combine with search, #category tags, Craftable only and the Using filter.
- Green/red recipe tint and the yellow selection frame now follow the slot's rounded corners.
- The tap-mode toggle is an item icon (Piggy Bank = take, Work Bench = show recipes) and the "recipes that use" filter shows the item's icon instead of its name.
- Recipe details now list every ingredient with Required (for the whole batch) and Stored (in the network, plus "(+N)" in your inventory), updating right after each craft.
- Batch crafting: -100 -10 -1 / +1 +10 +100 buttons set how many crafts one tap makes; the middle button resets to x1. Craft button reads "Craft xN"; Craft max is unchanged.
- Item slots (grids, recipe ingredients, result) use the vanilla inventory slot border.
- Category filters are item icons instead of words (Chest = All, Iron Broadsword, Iron Pickaxe, Iron Chainmail, Hermes Boots, Healing Potion, Dirt Block, Wooden Arrow, Iron Bar, Magic Mirror).

# 1.0.2

- Graveyard recipes: tap gravestones or tombstones in your inventory on the Storage Heart screen to install them (7 needed, any mix). They appear in the Stations tab, tap one twice to take it back. With 7 installed, recipes that need the Graveyard can be crafted from storage. Standing in a real Graveyard still works too.

# 1.0.1

- Recipe details show how many of each item a craft uses ("10x Iron Bar") and how many you have.
- Tap a crafting station in your inventory on the Storage Heart screen to install it; the "Install held" button is gone.
- New Stations tab: lists every installed crafting station; tap one to select, tap again to take it back.
- Fixed the search text not showing with the phone keyboard.
- Replaced the near-black boxes behind slots, search field and recipe details with the vanilla blue UI; slot backgrounds are drawn before icons so they cannot cover items.
- Storage blocks can be placed on top of, under or beside each other; they no longer need a floor or table.
- Tapping a Storage Unit also shows the combined slots of all connected units (two basic units = 80 slots).
- The search bar and recipe ingredient panel are outline-only (no filled box), so nothing can sit over their text and icons.
- The game's own Quick Stack to Nearby Chests button now also stacks into storage networks within 12 tiles (items the network already holds, from the main inventory).

# 1.0.0

- First release.
