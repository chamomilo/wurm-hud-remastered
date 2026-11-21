# Waypointer in Wurm HUD Remastered

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
