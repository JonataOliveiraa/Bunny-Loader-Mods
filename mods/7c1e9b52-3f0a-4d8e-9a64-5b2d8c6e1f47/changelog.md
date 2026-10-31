# Changelog

## 1.5.0
- New in-game option **GIF speed** (0-60 fps, 0 = the GIF's own timing) in Settings > Mod Configuration > Menu Media.

## 1.4.0
- New in-game options (Settings > Mod Configuration > Menu Media): **Size** (50-300%), **Position X** and **Position Y** (-1000 to 1000 px), with English and Vietnamese labels. They replace `zoom`, `offsetX` and `offsetY` in `config.json`.

## 1.3.2
- Fixes the uncovered strip on the right edge: the drawing area is now the screen plus a 12% margin on the right (`padRight`), and the picture is fitted and zoomed inside that area. New `padLeft`, `padRight`, `padTop`, `padBottom` options (fractions of the screen).

## 1.3.1
- A small status line now appears at the top-left of the menu while a GIF is preparing or loading, or if it fails (with the reason). Turn it off with `"showStatus": false`.
- More log lines (`Menu Media: selected theme ...`) to help find problems.

## 1.3.0
- Much less lag with GIFs: playback is capped at `maxFps` (15 by default, duration kept), and preparation is cut into small slices spread over many game frames (`budgetMs`).
- Pictures are zoomed 1.15x by default, centered (`zoom`, plus `offsetX`/`offsetY` to nudge).
- Old caches are rebuilt once.

## 1.2.0
- English is now the default language, with a Vietnamese translation (description, changelog, `/menumedia`).
- New `language` option in `config.json` (`auto`, `en`, `vi`).

## 1.1.0
- Backgrounds now live INSIDE the mod, in `content/Assets/MenuThemes/`: each GIF/image (plus the audio of the same name) is a menu theme. Add the files, zip and import again.
- Pick the theme in Settings > Menu Theme; only the selected theme is prepared.

## 1.0.0
- First version (external folder).
