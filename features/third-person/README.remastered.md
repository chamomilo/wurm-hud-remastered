# Third Person View in Wurm HUD Remastered

Compared with the latest public standalone release: [Third Person View v0.5.0](https://github.com/chamomilo/WU-3rd-person-view/releases/tag/v0.5.0).

The published camera behaviour is preserved: third person, held orbit, flying
freelook, smooth zoom, head animation, collision handling and the existing tp
console commands. Its Keybinder command catalogue remains available when the
camera and Keybinder modules are enabled.

- Camera settings now appear in the common local Remastered page. The camera
  view, zoom, orbit direction, existing overrides and saved state are retained.
- One restart-only module switch controls construction and hook installation.
  Disable it and restart the whole client to omit the camera completely.
- The separate updater is removed from this embedded component. Camera commands
  and user data paths keep their original namespaces and compatibility.

No new camera modes or gameplay changes are introduced beyond the published
camera release. Existing state.properties and custom camera settings stay in use.

Install and configure this component using the [Remastered guide](../../README.md).
