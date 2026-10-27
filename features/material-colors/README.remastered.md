# Material Colors in Wurm HUD Remastered

Compared with the latest public standalone release: [Material Colors v0.5.3](https://github.com/chamomilo/wurm-material-colors/releases/tag/v0.5.3).

Supported world equipment, held/dropped items, shields, helmets, worn armour,
wooden furniture, containers, parts, piles and vehicles retain material colours.

- The supported SkloGraphics configuration now uses palettes and masks only.
  Keep 14 metal and 26 wood palettes, reviewed world masks, neutral armour and
  plank textures, and worn plate/chain material colouring.
- Remove Material Colors' reflections, glints, cave-light compensation, custom
  shaders and reflection metadata in opacity/player atlases. SkloGraphics owns
  those effects; Wurm keeps its normal shader programs and texture compositor.
- Remove obsolete reflection controls and custom pack selection so old saved
  options cannot reactivate a shader pack. The reviewed bundled masks load from
  the module's embedded resource prefix. Existing custom/stock masks take
  precedence where supported; fabric, leather and painted details are preserved.

Existing palette/mask settings and user data remain in use. Complete client
restart is required to stop hooks left in a previous standalone session.

Install and configure this component using the [Remastered guide](../../README.md).
