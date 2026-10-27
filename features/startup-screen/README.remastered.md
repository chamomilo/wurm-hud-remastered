# Startup Screen in Wurm HUD Remastered

Compared with the latest public standalone release: [Startup Screen v0.5.2](https://github.com/chamomilo/wurm-highres-startup/releases/tag/v0.5.2).

Illustrated 3840 x 2160 JPEG loading screens retain the native loading text,
progress display and reconnect controls.

- Three credited Sklotopolis scenes extend the collection to thirteen:
  A Day of Climbing (FlpSilva), Avallone Docks (Encode), and A Fine Work (Mlemow),
  whose pinto horse looks into the dug pit. Titles and source credits are on
  the images and preserved with the embedded collection.
- Choose a fixed named screen or Random. Random changes images every five
  seconds without showing any usable image twice in one loading session,
  including the initial screen and loading fallbacks. After the collection is
  exhausted, the last screen stays visible. Reconnect starts a fresh session.
- Images decode asynchronously and load directly from the single Remastered
  JAR. Settings are on the common local page and apply after a full restart.

Existing screen preferences remain compatible. No separate image JAR or loose
startup image directory is needed.

Install and configure this component using the [Remastered guide](../../README.md).
