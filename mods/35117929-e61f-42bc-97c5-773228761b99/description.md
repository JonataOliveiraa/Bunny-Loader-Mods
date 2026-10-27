# Universal Map

In multiplayer, everything the players explore ends up on everyone's map.
Every minute, each player sends the areas they explored since the last sync
and receives the areas the others explored.

## How it works

- Only new areas are sent, so syncs stay small after the first one.
- Shared areas keep the same brightness the other player saw.
- Areas you already explored yourself are never overwritten.
- Players who join later receive the whole shared map a few seconds after
  joining.
- Works on a dedicated server and when a phone hosts the world.
- The work is spread over many frames, so the game keeps running smoothly.

## Settings

| Setting | What it does |
| --- | --- |
| Interval | Minutes between syncs (1 to 10). |
| Notifications | Shows a chat message when your map receives new areas. |
| Share Now | Sends your whole explored map right away. |
