# Overhealth

Port of **Overhealth** by JADen (tModLoader) for Bunny Loader.

When you receive healing while already near full health, the part that does not fit becomes temporary **Overhealth**:

- It works as an extension of your max life: **damage is taken from overhealth first**.
- It slowly decays. The more you have, the faster it goes (same formula as the original: a constant part plus a part that grows with the amount).
- Natural regeneration never creates overhealth.
- A gold heart, bar and `+N` counter show it on the HUD.

**Options** (Mod Config): enable, maximum overhealth (% of max life), constant / progressive decay and a multiplier, HUD on/off, position, size and opacity, debug log.

**Differences from the PC version**
- The original removes the game's health caps with IL edits, which Bunny Loader cannot do. Here overhealth is its own value kept next to your life, so the game's own health bar is not changed (the gold HUD shows the extra).
- Healing is detected through the game's heal effect, so potions, hearts, lifesteal and similar all count. Poison/burning and other damage that does not go through the game's normal hurt call is not absorbed by overhealth.
- Local player only (other players' overhealth bars in multiplayer are not shown).
