# WorldGen Previewer

Watch your world take shape while it is being generated. The game's own map
fills in as each step runs, and you can pause, step through, repeat, skip or
cancel the generation.

## The screen

| Button | What it does |
|---|---|
| **Steps** | Shows or hides the list of generation steps (the map gets wider). |
| **Previous** | Pauses and runs the last step again. |
| **Play** | Resumes the generation. |
| **Pause** | Pauses after the current step. |
| **Next** | Runs one more step, then pauses. |
| **Structures** | Shows the protected structures (green and red). |
| **Cancel** | Stops the generation. The world is not saved. |

Tap a button to use it, or hold your finger on it to see what it does.

## The map

- The map is updated one whole column at a time, from left to right. The pink
  line marks the column being read right now.
- The map is drawn at full resolution: every block is one pixel, as in the
  in-game map, and the frame fits the shape of the world.
- **Pinch** with two fingers to zoom in and out, and drag to move it while
  zoomed in. While zoomed in, only what is on screen is updated and the steps
  list hides; pinch all the way out to bring it back.
- **Hold** your finger on the map to see the name of the block under it.
- Below the map, the world generation text and progress bars, drawn with the
  game's own bars.
- The world only finishes after one last full pass of the map, so the preview
  shows the final world.

## The steps list

- The steps are shown in the game's language, and each name fits whole in its
  line.
- Drag the list up and down to see every step.
- Tap a step to keep generating and pause right after it.
- Tap the **X** next to a step to skip it (tap again to keep it).
- White: still to run. Gray: will be skipped. Red: done. Yellow: skipped.
  **(x2)** means the step ran twice.

## Config

**Start Paused** pauses after the first step, so you can skip or repeat the
early steps. **Map Preview** turns the live map on or off.

Port of *WorldGen Previewer* by jopojelly (tModLoader).
