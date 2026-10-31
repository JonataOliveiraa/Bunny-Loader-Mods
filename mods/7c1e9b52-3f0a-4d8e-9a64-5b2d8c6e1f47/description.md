# Menu Media

Every **GIF** (or image) in the mod's `content/Assets/MenuThemes/` folder becomes a **main-menu theme**. If an audio file with the **same name** sits next to it, that audio is the theme's music; with no audio, the game's own menu music plays.

## Adding themes

1. Unzip the mod and put your files in `content/Assets/MenuThemes/`:
   - `beach.gif` + `beach.mp3` → theme **beach**, with its own music;
   - `night.png` → theme **night**, normal game music.
2. Zip it again (`manifest.json` must be at the root of the ZIP) and import it in Bunny Loader.
3. In game: Settings > **Menu Theme** switches between the themes.

Backgrounds: `.gif`, `.png`, `.jpg`. Audio: `.mp3`, `.ogg`, `.wav`, `.m4a`, `.aac`, `.flac`.

## Size, position and GIF speed

In game: **Settings > Mod Configuration > Menu Media** (also in the pause menu, inside a world). Four sliders:

| Option | Default | Range |
|---|---|---|
| Size | `115%` | 50% to 300% |
| Position X | `0 px` | -1000 to 1000 (negative = left) |
| Position Y | `0 px` | -1000 to 1000 (negative = up) |
| GIF speed | `0` | 0 to 60 fps. `0` = the GIF's own timing; any other value shows every kept frame for `1000 / fps` ms. |

Press **Apply** and the menu background updates right away. **Default** resets them. The picture is zoomed around the center of the screen, then moved by X/Y.

The GIF speed slider only changes how fast the kept frames are played. How many frames are kept is set when the GIF is prepared (`maxFps`, 15 by default): to get a smoother result above 15 fps, raise `maxFps` in `config.json` (it uses more memory).

## Video

The game has no video player a mod can use, so the mod **does not open MP4/MKV directly**. Convert it on a computer with `convert-video.sh` (Linux/macOS) or `convert-video.bat` (Windows), which ship with the mod (they need ffmpeg):

```
./convert-video.sh my-video.mp4 10 12 480
```

It writes `my-video.gif` and, **if the video has sound**, `my-video.mp3`. Put both in the themes folder. A silent video becomes a GIF only and the music stays the game's.

## The first time with a GIF

The GIF is decoded inside the game in small slices spread over many game frames (so the menu stays smooth), and saved as PNGs in `cache/` (in the mod's data folder, outside the package). The first time, the background shows up when preparation finishes (the game may stutter a little); after that it opens instantly. `/menumedia` shows the state of every theme.

## config.json (optional, in the themes folder)

| Key | Default | What it does |
|---|---|---|
| `language` | `"auto"` | Language of the `/menumedia` command: `auto`, `en` or `vi`. |
| `fit` | `"cover"` | `cover` fills the screen and crops the excess, `contain` shows it whole with black bars, `stretch` stretches it. |
| `padLeft`, `padRight`, `padTop`, `padBottom` | `0`, `0.12`, `0`, `0` | Extends the drawing area past the screen edges (fraction of the screen). If a strip of the game's own background still shows on one side, raise that side (e.g. `"padRight": 0.2`). |
| `areaScale` | `1` | Advanced: multiplies the screen size used for drawing. |
| `maxSide` | `480` | Longest side of a frame (px). |
| `maxFps` | `15` | Playback fps cap. Faster GIFs lose frames (duration is kept), which makes them much lighter. |
| `maxFrames` | `120` | Frames kept per theme; longer GIFs merge frames but keep their duration. |
| `maxPixels` | `16000000` | Total pixels of a theme's frames (memory). |
| `preloadPerFrame` | `1` | Frames sent to the GPU per work slot. |
| `showStatus` | `true` | Shows a status line at the top-left of the menu while a GIF is preparing, or the error if it fails. |
| `budgetMs` | `8` | Target ms of work per game frame while a GIF is being prepared. Lower = smoother but slower to prepare. |

## Limits

- The frames of the theme in use stay in memory after you enter a world.
- A theme's music only plays while that theme is selected.
