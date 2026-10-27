# Changelog

## 1.1.2

- Fixed the host getting "Destination array was not long enough" when
  receiving map data: on mobile every received message must fit in 32767
  bytes, and a full map packet was about 48 KB. Packets now stay under 27 KB.

## 1.1.1

- Fixed the explored map not being shared when joining another player's
  world: the mod kept reading the map from before the game rebuilt it, saw
  nothing explored and sent nothing.
- The first three syncs share the whole map, so areas from the map saved for
  this world are sent even if it finishes loading late.
- Nothing is sent before you finish joining the world (the server kicks
  players who do).
- The Bunny log shows how many tiles each sync shared and received.

## 1.1.0

- Shared areas keep the brightness the other player saw instead of being
  fully lit, and the same blocks they saw on their map.
- Reading the map is much faster: each part of the map is read at once
  instead of tile by tile.

## 1.0.2

- Received areas now show up whole on the map instead of in scattered
  patches: when the game's map redraw queue is full, the mod waits for it
  instead of writing tiles the map never draws.
- The Notifications setting works: chat messages use the mobile signature.
- Receiving a map no longer delays your own syncs.

## 1.0.1

- Fixed the map never being shared: the server now listens for the players'
  map data from the start.
- Received areas now show up on the map and minimap right away.
- Empty parts of the map are skipped when reading, so syncs are much lighter.
- A failed read no longer stops future syncs and the Share Now button.

## 1.0.0

- First release: automatic map sharing between all players every minute,
  with the shared map sent to players who join later.
- Settings for the interval, notifications and a Share Now button.
- Text in 12 languages.
