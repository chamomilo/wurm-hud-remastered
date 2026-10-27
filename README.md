# Wurm HUD Remastered 0.3.29

Eight selectable Wurm Unlimited client components in one installation, with one
local settings page and one product version. This is the first public Remastered
release. The component sections collect changes since each component's latest
public standalone release, verified on 2026-10-28. Intermediate development
versions are deliberately combined into one description per component.

[Download the latest ZIP](https://github.com/chamomilo/wurm-hud-remastered/releases/latest)

## Install or update manually

Requires Wurm Unlimited, Java 8 and Ago's Client Mod Launcher. No server mod is
required. Close the entire game client and WurmLauncher before installation.

1. Back up bindings, waypoints, alarms, camera state and mod settings.
2. Rename old standalone loader descriptors from .properties to
   .properties.disabled: WU-third_person_view, alarmclock, armor-material-colors,
   highres-hud, highres-startup, keybinder, wurm-highres and wurm-waypointer.
   Keep predecessor standalone healthbar/selectbar/fighting HUD disabled too.
   Preserve their folders and user data; renamed descriptor settings are read.
3. Extract wurm-hud-remastered-0.3.29.zip into WurmLauncher, merging mods and
   replacing the Remastered descriptor if present.
4. Start through Client Mod Launcher. For a previous Remastered installation,
   the replaced descriptor selects the new versioned JAR.

The ZIP contains exactly three files:

    README.txt
    mods/wurm-hud-remastered.properties
    mods/wurm-hud-remastered/wurm-hud-remastered-0.3.29.jar

One JAR contains all eight components' code and their bundled resources.
Resource activation follows each component's switch. Existing user files keep
their legacy locations. No saved bindings, waypoints, alarms or overrides are
included. Avatar2 remains a separate mod.

## Common settings and language

Open Main menu > Wurm HUD Remastered or enter remastered settings in the console.
The first row selects English, Brazilian Portuguese, German or Russian. Language
changes apply immediately to the page and capable enabled components when the
HUD is ready. Existing component-specific language coverage is preserved.

Eight module switches follow, then the enabled components' original settings.
All modules default to enabled. Module switches apply after a complete client
restart; a disabled module is not constructed and installs no hooks. Other
settings identify immediate application or restart requirements.

Language is saved in ~/.chamomilo/remastered.properties; a previous shared
language is read on first use without changing its old file. Module overrides
in ~/.chamomilo/mod-settings/wurm-hud-remastered.properties take precedence over
modules.<module-id>.enabled in the descriptor. Feature settings retain their
original files. Here ~ means the user's home directory.

Settings and language are local. Remastered includes no updater, release-check
client or update catalogue. Existing network-backed feature functions, such as
Waypointer's map feeds, remain part of those features.

## Cumulative component guide

### Keybinder

Compared with the latest public standalone release: [Keybinder v1.0.3](https://github.com/chamomilo/wurm-keybinder/releases/tag/v1.0.3).

Create action chains, Quick menus and Multi variants on a key, with tool and
target selection and the existing command catalogues.

- The queue monitor recovers actions already running when a binding starts and
  follows consecutive server timers. Current uses the actual game timer verb,
  including phases of compound and area commands. A brass divider separates it
  from planned actions in both expanded and collapsed views.
- Tool and target details belong to a correlated outgoing single-target command.
  Later tool selections or hover changes cannot rewrite the running row. Area
  phases, missing observations and conflicting or expired matches show unknown
  details. Uncertain matches cannot trigger a remembered queued cancellation;
  clicking Current still explicitly stops the running action.
- Captured menu actions retain their full server menu path, including nested
  area commands. World targets use their display names and exact dispatched IDs.
- The complete action catalogue and spell target declarations were audited.
  Corrected contexts include crafting-window targets, ground equipment, trellis
  sprouts, rift objects, conches, creature Cure spells and Stand up.
- A server prayer charm can have a different action ID from built-in altar Pray.
  Use Capture Action on its actual menu action. Captured Pray keeps that server
  ID and exact target, uses empty hand and hides the irrelevant Tool field.
- Rename executes without consuming a native action-queue slot or adding a
  monitor row, including when the action queue is full.
- Gameplay actions chosen from a catalogue reopen in the same catalogue with
  their action, tool and target selections. This metadata survives duplication
  and export/import. Existing Custom steps stay custom until explicitly changed.

Existing bindings, account data and custom file paths are retained. Mutable
legacy descriptor preferences use mods/keybinder.config, keeping the disabled
standalone loader descriptor from being recreated. The HUD tag is inside the
Remastered JAR.

### Waypointer

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

### High-res HUD

Compared with the latest public standalone release: [High-res HUD v0.8.7](https://github.com/chamomilo/Wurm-HighRes-HUD/releases/tag/v0.8.7).

The unified Inventory, Containers, Character, Chat, Events, Build/recipes,
Healthbar, Select bar and Fighting HUD retain their native gameplay actions.

- Pin any carried inventory or equipment item, including nested bag contents,
  through Pin to HUD in its normal context menu. One left click activates the
  exact item as a tool; a double click opens a container. Right click keeps its
  native actions and adds Unpin from HUD and the 70/44 px size choice.
- Pins can be dragged and retain item IDs, sizes and positions per server and
  character. Unavailable items keep their saved shortcut. The actual active
  tool has a green inner outline, a clockwise travelling bright segment, a lower
  marker and a translucent face; inventory and hotkey changes update it too.
- Repeated Build/Continue clicks and numbered Build queue buttons reserve exact
  item IDs and required masses up to the character's action limit. A numbered
  batch is rejected as a whole if stock or free slots are insufficient. Tools
  remain reusable. Reservations survive intermediate results and appended
  actions, then clear when the queue finishes or is cancelled.
- Auto-pick includes suitable materials inside bags and surplus stock for
  multiple crafts, while preserving manual choices and avoiding duplicates.
  The native hand is added automatically for recipes that need it. Mortar uses
  1 kg each of clay and sand; liquid ingredients reserve only the required mass.
- Glowing server-added metal name prefixes are recognized. Actual temperature,
  mass and the chosen result metal still determine whether material is usable.
- For an unfinished item, select a row in Remaining to finish or a material
  in the store. Continue and queue buttons keep using that component type until
  another is chosen. If it runs out, crafting stops. Reordering the store
  restores automatic selection. An altar can be left needing only its bowl.
- Crafting separates material rarity inheritance from random rarity. Drum Roll
  chance shows the inactive window-opening rate, 1/3600 per second. The random
  outcomes in an active window display Rare 48%, Supreme 4%, Fantastic 0.01%.
  Rare materials do not turn the window-opening trigger into a guaranteed event.
- Recipe catalogue text is 15 px. The selected row's magnifier copies its name
  into name search. Inventory, store and catalogue search fields have a brighter
  orange surface and an amber focus marker. Auto-pick and empty-store help are
  easier to find and support all four interface languages.
- Independent minus/plus controls change window reading text in one-pixel steps
  within +/-2 px. Buttons keep their dimensions. Chat/Events have compact 32 px
  opacity controls. Existing per-window opacity and minimized channel strips
  remain available.

The bundled 2702-recipe catalogue remains a manual Sklotopolis Novus snapshot;
unfinished requirements follow the server. Existing pins, portrait overrides
and combat knowledge paths are preserved. Required default resources load from
the single JAR; no loose portrait profile file is installed.

### Alarm Clock

Compared with the latest public standalone release: [Alarm Clock v0.3.10](https://github.com/chamomilo/wurm-alarm-clock/releases/tag/v0.3.10).

Keep food, water, prayer, meditation, Favor and custom reminders, including
All on / All off, saved preferences, chimes and reminders while the list is closed.

- The alarm window displays actual game time and adds Lock time with separate
  HH:MM fields. ASCII digits, hours 0-23 and minutes 0-59 are validated. The
  initial lock value is 12:00, with locking off. Valid edits apply immediately.
- TimeLock changes the local sky and lighting while the real calendar and alarm
  deadlines continue. Turning it off immediately restores the normal sky.
- The draggable brass HUD clock has 42 px and 84 px size choices, scaled for the
  viewport. Independent hands follow real game time, including fractional hour
  movement, while a time lock is active. Ringing reminders use the same artwork.
- Hover shows actual time, optional locked time, then enabled alarms and their
  countdowns. Food, water and Favor show their condition when no exact countdown
  is available. Time digits and editors use aligned, centred 20 px body text.

New controls and hints support English, Brazilian Portuguese, German and
Russian. Clock and lock preferences are saved beside the existing alarms.

### Third Person View

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

### High-res Icons

Compared with the latest public standalone release: [High-res Icons v0.2.5](https://github.com/chamomilo/wurm-high-res-icons/releases/tag/v0.2.5).

Detailed 32 x 32 runtime item icons retain material colours, animated rarity
highlights and magic shimmer across supported item views.

- The completed old and modern fishing collections add distinct rods, poles,
  lines, hooks, landing net, reel components and assembled reels. Material masks
  preserve cotton line, stone sinkers, leather grips and fixed fittings.
- Finished tools and separate parts have matching artwork: mallet, hammer,
  pickaxe, rake and shovel, with distinct wooden/metal shovel blades. The rake
  uses six widely spaced teeth. Leatherworking knife and blade are separated
  from cutlery; the stone chisel follows the metal stone-cutting tool.
- Training equipment, weapons, ammunition and unfinished parts have additional
  artwork, including different axe/maul sizes and heads. Sickle and blade follow
  the curved game model and wrapped grip. Separate short-bow states are selected
  only when the client supplies a distinguishing name or model marker.
- Shared icons are resolved using confirmed names, models or standard weights.
  Ambiguous renamed items and generic recipe labels keep the existing icon.
- Runtime icons, mappings and masks are embedded under the module's own prefix
  in the sole Remastered JAR. The module switch controls resource activation;
  saved icon, material and effect settings remain compatible.

The newer model-based library of 132 reviewed 64/32/16 px artwork families is
development work. It has not replaced the installed runtime pack. Its catalogue,
masters, source cache and unconfirmed bindings are excluded from this ZIP.

### Material Colors

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

### Startup Screen

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

## Validation and source

The release build checks component regressions, native UI/input/layout probes,
four-language layouts, geometry, resource bytes and activation isolation. It
also runs fourteen fresh packaged shared-loader scenarios and the complete
actual ModLoader lifecycle with all components enabled and all disabled.
The SDK is pinned to high-res UI 0.4.11 and embedded exactly once, retaining
font and component notices. The ZIP whitelist is checked against all three files.

Each component has a README.remastered.md in its features directory with the
same cumulative guide. This public repository contains documentation and the
installation ZIP. Full project sources and development research remain local.
Use this root guide for Remastered installation, settings and package contents.

Sources, research, previews, experimental icon caches and disposable files are
excluded from the installation ZIP. Required licence notices remain in the JAR.
Live GPU rendering and server gameplay require manual verification in the game.
