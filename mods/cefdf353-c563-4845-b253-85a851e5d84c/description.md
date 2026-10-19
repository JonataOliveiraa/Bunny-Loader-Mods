# Lights And Shadows

A port of **yiyang233's Lights And Shadows** for tModLoader. The sun and the moon cast a warm glow over the sky that changes color through the day, the terrain throws **shadow rays** away from the light, and bright things **bloom**.

The look follows the original step by step: the same color gradients, the same sun path, the same biome and moon phase adjustments, the same 30 shadow samples by day and 20 by night, and the same four-pass Kawase bloom. Everything runs as one effect between the world and the interface, so the hotbar and the buttons stay sharp.

## Rebuilt for phones

The PC version renders the screen several times per frame. This one draws the same image with far less work:

- the sunlight is computed in the final shader instead of being rendered to a full-screen texture;
- the 30 shadow layers are one pass with 30 samples, not 30 full draws;
- the shadow mask and the bloom read the same small copy of the screen;
- the threshold and the first blur pass are one step, and the light and the bloom are added in one final pass;
- underground, where the original light is never visible, only the bloom runs.

## Options

In **Mod Configuration**: lighting on or off, light, moonlight and shadow strength, yellow or white midday light, bloom on or off, bloom strength and passes, and **shadow quality** (High is the original; Medium and Low draw the shadow rays at a lower resolution for weaker phones).

With **Screen Effects** off in Settings, nothing is drawn.

## Credits

Original mod, shaders and color gradients by yiyang233 ([Steam Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=2670628346), [GitHub](https://github.com/AWEoghAwo/Lights)). Polish translation by Gryfu.
