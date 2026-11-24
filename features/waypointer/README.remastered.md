# Waypointer in Wurm HUD Remastered

In 0.10.4, Waypointer reuses unchanged marker lists and updates terrain chunks
affected by incoming tile data. Every second it also checks a 7 × 7 area
around each loaded player and the tile under each loaded creature, including
neighboring tiles needed to render local changes.

## Remastered 0.9.4

Surface navigation lines stay visible through trees and shrubs, with terrain
and structures still hiding the sections behind them.
Hovering a dropdown shows the full selected choice without a stack overflow.

## Remastered 0.9.3

The automatic meteorite waypoint is removed when the server removes the fully
mined meteorite.

## Remastered 0.7.5

Full-map title/status text is drawn directly on the wooden rails in the shared
ivory colour, with no separate black plates. The reclaimed strips add 86 pixels
of terrain height. Overflowing controls have fixed left/right arrow buttons;
wheel and drag scrolling remain available. Widening the window returns the
strip to its first button. Close stays fixed to the upper-right frame corner.
Full caption and scroll hints support all four interface languages.
Tree Hunter adds all ten native bush species to Species, alongside the fifteen
trees. Age/pruning/harvest/sprout filters apply to bushes, including mycelium and
enchanted variants. Tree IDs and saved selections remain compatible.

## Remastered 0.7.4

Containers adds Show on map before Add to monitor. Matching loaded containers
appear as blue stars on both maps with exact-name hover. Containers and Mobs
keep independent filters and toggles, sharing the received catalogue and update
cadence without additional tracking requests or a separate loading radius.

Route Statistics has three NAV LINE style buttons and a green NAV toggle for
pausing/resuming the same target. Vertical off-road, road and highway rows begin
at 8/16/24 km/h. Session-local measurements learn actual movement speeds for
walking and each vehicle, and measured categories update ETA. Stops, teleports
and surface/transport transitions do not contaminate the samples.

The retained 0.7.3 resize fix prevents native WorldMap.update from resetting
the full map's dimensions on every rendered frame. Independent axes and fixed
top/right anchors survive dragging and subsequent frames.

## Remastered 0.7.0

Both maps use compact terrain artwork. The main-map frame has one lower-left
resize button with independent axes; the toolbar scrolls horizontally and reopening resets size.
The mini-map has a resize grip and north/heading compass switch. Geometry rotates,
labels stay horizontal, and continuous player positions keep following smooth.
Mobs Show on map displays the filtered loaded actors with type-based green/red
points and exact-name hover, without additional server tracking. Exact animal and
Exact age each have independent selectors, On/Off and color. Waypoints uses a left
delete cross, removes Copy and fits non-Name values before allocating Name width.
Generated surface/cave hints and controls support all four interface languages.

Compared with the latest public standalone release: [Waypointer v1.10.11](https://github.com/chamomilo/wurm-waypointer/releases/tag/v1.10.11).

Keep waypoints, compass navigation, the full map and minimap, deeds and highways,
tracking, Loot Maps, archaeology, scanners and creature/tile highlights. Large
lists retain viewport-based controls, filtering, sorting and bulk actions.

- Tree Hunter replaces the single Overaged trees rule with a compact framed
  panel, five multi-select filters, a colour picker and one On/Off switch.
  Match age, pruning, harvest, sprouting and species using native tree data
  already received by the client. Chosen filters and colour persist.
- Native modern and legacy render queues skip an indexed draw when its index
  data is unavailable in both GPU and CPU memory. Healthy draws and native
  callbacks continue. This contains the reported shadow-map null-buffer crash;
  it does not identify or repair the producer of missing geometry.
- Coalesced incidents are written by the existing diagnostics worker to
  wurm-waypointer-data/waypointer-diagnostics-*.log, without render-thread file IO.

Open Waypointer with its compass. General settings are now in Main menu >
Wurm HUD Remastered. Existing wurm-waypointer-data, configuration, map caches
and explicitly configured data paths remain in use. Network-backed map and deed
features retain their existing behaviour.

Install and configure this component using the [Remastered guide](../../README.md).
