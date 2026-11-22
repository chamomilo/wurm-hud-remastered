# Wurm HUD Remastered 0.9.4

Ten selectable Wurm Unlimited client components in one installation, with one
local settings page and one product version.

## Changes in 0.9.4

- Inventory and container windows quietly check visible gems and eligible
  items, including tools, for magic. Confirmed rows keep their rarity-colour
  glow and localized hint during the session. Casts, dispels and item updates
  trigger a recheck, and manual Examine still appears in Events.
- Waypointer's surface navigation line stays visible through trees and shrubs
  while terrain and structures still occlude it.
- Hovering Waypointer dropdowns shows the full current choice without a stack overflow.
- Narrow saved chat windows reopen with room for both channel tabs and controls.

## Changes in 0.9.3

- **As much as I can carry, any QL** in Bulk Transfer takes matching items
  from the same storage in descending quality order until the destination
  reaches its limit. The original single-row maximum remains the default.
- The chat rename and private-chat prompts visibly focus the text field as
  soon as they open.
- Inventory names glow in their rarity colour when an enchantment is
  confirmed. Visible gems are checked automatically, and Examine can reveal
  the glow on tools and other items.
- Fighting HUD shows the confirmed stance in auto combat and updates hit
  chances after stance changes. It also shows expected weapon damage before
  armour and compares estimated combat ratings.
- Waypointer removes the automatic meteorite waypoint when the server
  removes the fully mined meteorite.

## Changes in 0.9.2

- Fighting HUD shows the attack figure and a preliminary BEST zone when a
  target is selected. During manual combat BEST ranks server-available zones.
- The damage index uses observations for the equipped loadout, including the
  sickle, and shows a dash until there are hit samples for that loadout.
- Fighting HUD reads the shield from its equipment slot, including renamed
  shields, and shows its equipped status before it has block observations.

## Changes in 0.9.1

- In Waypointer's Creatures Highlight tab, **&** links the exact animal and age
  filters. The switches move together, each list counts matches within the
  other selection, and creatures matching both use the animal outline color.
- Chat channels publish to the HUD by default. Their HUD switches and colors are
  saved locally. The chat window folds on window activation or movement, and the
  pin beside **Clear messages** keeps it open.
- **Rename** and **Default name** in the channel menu manage local display names.
  The private-chat and rename prompts use high-res UI frames and focused text
  fields directly below their labels.

## Changes in 0.9.0

- Chat channels can copy new messages into a transparent HUD area. Right-click
  a channel to enable **Show on HUD** or choose a color. Messages start with the
  channel in brackets, followed by the chat time, sender and message. Personal
  conversations use `[private]`. The chat window's text size also applies to
  the feed. Scroll with the mouse wheel and use **Clear messages** in the chat
  window to clear the HUD history.
- Select **+** after the last chat tab, enter a character's name and press Enter
  to open their private conversation.
- Waypointer's Tiles Highlight tab places Tree Hunter in the right column and
  Meteors immediately below Harvestable areas on the left.

## Changes in 0.8.3

- Launcher synchronization waits for a loaded session before sending `/alts`
  in Local with the native channel/message order. Manual `/alts` stays visible
  and cancels automatic reply suppression.

## Changes in 0.8.2

- Keybinder's Plant, Plant in center and Sow select planting material inside the
  configured container using the server's actual available actions. Seeds,
  flowers, sprouts, seedlings and server-specific materials need no name/icon
  whitelist. Private asynchronous queries preserve native/SkloGraphics popup
  requests. The container stays active and other containers are not searched.

## Changes in 0.8.1

- Go to sleep uses direct YES/NO actions with the original native answer.
- Keybinder's initial container fix supports native sprouts for Plant and
  Plant in center. Version 0.8.2 extends this to server-approved planting
  materials and Sow.

## Changes in 0.8.0

- The full map's title and status text now sit directly on the wooden top/bottom
  frame in the shared ivory text colour, without separate black plates. The
  toolbar also overlays the map without a black strip. Terrain gains 86 pixels
  of height at the same window size.
- Overflowing map controls have fixed left/right arrow buttons. Wheel/drag
  scrolling remains available; increasing the window width returns the strip
  to its first button. Close is fixed to the upper-right frame corner and stays
  reachable independently of toolbar scrolling.
- Title/status full hints and new scroll-arrow hints cover all four languages.
- Tree Hunter's Species list now includes all 10 native bush species alongside
  the existing 15 trees. Bushes use the same age/pruning/harvest/sprout filters;
  saved tree selections retain their IDs and bushes have separate stable IDs.

- Drag the full map by its wooden frame; map-body gestures continue to pan.
- Show on map includes its marker legend: red/green circles for Mobs and a blue
  star for Containers, with measured room for all four localized captions.
- Creature species and age selectors refresh loaded counts on opening. Only
  nonzero counts have a suffix; zero-count options remain selectable. Rule
  captions also omit zero suffixes. Counts ignore outline enable/disable state.
  Exact animal/age each use one ordinary row: switch, narrow dropdown, swatch,
  Color. Their localized names are the empty/default choices, without headings.
- Startup rotation uses persistent presentation history and session/date filters;
  all settings and feature state now share one config with legacy migration.
- Stone-wall continuation retains the trowel as a reusable tool and can fill the
  native action queue without treating the trowel as one consumable component.
- Inventory items can be dropped onto Pin to HUD container shortcuts through
  the original client transfer handler, preserving multiple selection and Shift
  quantity prompts, including nested/equipped containers and compact shortcuts.
- Name sorting in inventory/equipment and container windows ignores the native
  rarity prefix. Full names, rarity colours, grouping and numeric sorts remain
  intact; an ordinary custom name containing the word rare keeps that word.
- The combined release also includes selectable Launcher compatibility and the
  expanded skill research cards, formulas, conditions and localized Overviews.
- Go to sleep uses two direct YES/NO actions instead of radio choices and Send;
  each retains the original native question and answer handling.

## Changes in 0.7.4

- Added Show on map before Add to monitor on Containers. Matching loaded
  containers appear as blue stars on the full map and mini-map. This layer
  uses the same received catalogue and update interval as Mobs, with independent
  toggles and filters, live positions and no tracking requests or saved marks.
- Route Statistics adds three NAV LINE style buttons and a green NAV toggle.
  Separate off-road, road and highway rows start at 8/16/24 km/h and learn actual
  movement speeds for the current vehicle or walking. Measured speeds drive ETA;
  stops, teleports and terrain/transport transitions do not contaminate samples.
- Added Silverlake sermons at Revival event, credited to Opene/Sklotopolis,
  after removing the source screenshot's interface. The startup library now has
  17 screens. Death keeps its existing ID and Red Leaf/Sklotopolis credit, with
  new layered artwork showing a deep abyss and the feeling of falling.

## Changes in 0.7.3

- Fixed full-map resizing being undone by the native fixed-size reset on every
  rendered frame. The lower-left grip keeps independent width/height changes
  and stable top/right anchors; other servers retain their native map behavior.

## Changes in 0.7.2

- Integrated 579 newly completed world-object icon families from the development
  library: 2,020 ready families total, at 64/32/16 pixels with reviewed masks.
- Fixed the crash when dragging items into Postbox. Single items, multiple
  selections and filled containers use the physical mailbox inventory.
- Restored world hover text, including food storage bin names and creature
  descriptions, by fixing an access error in the container-weight hook.
- Fixed shared-loader access to terrain artwork that stopped the cave map and
  repeatedly interrupted the HUD. Dropdown hovers no longer recurse, and
  Keybinder waits for a connection before requesting the creation catalog.
- Manual Examine replies reach Events, including drink quality supplied by the
  server, even when several items are selected or a background probe was pending.
- Once a second, both maps receive the entire surface tile buffer already sent
  by the server. Other players' terrain edits and tile-state changes update too;
  exact receipt coordinates prevent wrapped buffer slots appearing elsewhere.
- Surface mini-map zoom-out now covers up to 480 tiles per side, three times
  the previous limit, for enlarged windows.
- Mini-map contour interval, north/heading orientation, size and zoom persist
  in local settings across window recreation, reconnects and client restarts.
- The full map uses one lower-left resize button with independent width/height
  and a 480x360 minimum. The former four-corner resize mechanism is removed.
- Skill tracker gain headings follow Recent/Session mode immediately, with
  localized full-caption hints in narrow columns.
- Native model-name decoding uses a private copy, preventing concurrent readers
  from corrupting resource paths.
- Map texture updates preserve the renderer's texture bindings. This fixes a
  state leak that could interfere with the HUD; cave-map output and underground
  stability still need verification in the game.
- Includes the previously integrated crafting, Skills, maps, Quick Turn,
  loading-screen and reviewed icon updates described below.

## Changes in 0.7.1

- Integrated all 1,441 ready icon families, including young lemon, orange, willow
  and the repaired walnut wood mask. All three raster sizes and approved material
  masks are embedded in the single JAR. Unfinished masks remain excluded, and
  ambiguous native metadata retains the existing icon.

## Changes in 0.7.0

- Integrated Quick Turn 1.0.1, with its own restart-only On/Off block. It keeps
  cart/wagon, hitch, rider and particle steering behavior and session vqt commands.
  Disable the standalone wurm-vehicles-quick-turn descriptor before installation.
- Both maps use compact terrain artwork. The main map has an outside frame,
  one lower-left resize button, default size on reopening, and a single toolbar row with
  horizontal mouse scrolling. The mini-map adds a resize grip and north/heading
  compass switch; terrain, marks, routes and deed borders rotate while text stays
  horizontal. Center, player arrow and navigation origin use continuous positions.
- Mobs can show their filtered loaded list on both maps: peaceful types are green,
  aggressive types red, independently of attitude/Fo. Exact names appear on hover.
  Updates are bounded and do not request server tracking. Exact animal and Exact
  age each have their own selector, On/Off and color. Waypoints moves Delete to a
  left cross, removes Copy, and fits non-Name columns before allocating Name.
- Added Faith, Favor and Alignment cards with Ivan guidance. Religion uses
  confirmed own-player messages instead of the unused Atheist default. Pray once
  if your deity is initially unknown. Every card opens on Overview. Small maul
  Parry includes a Venerable troll / iron QL90 reference with assumptions on hover.
  Mining's diagonal image corruption is repaired losslessly; all 138 skill images
  have been audited for native upload row alignment.
- Build auto-picks backpack tools before/after metal selection. Damaged store rows
  have a visible animated hammer Repair button, including a missing-texture glyph.
  Next QL estimates expected successful-action base quality. Single-stage recipes
  hide Continue. Required metal is red and requirements wait for its selection.
  Container hovers show available weights in inventory and world/Select.
- Precious-metal requirements were audited per recipe: gold, silver and electrum
  are the WU group. Small anvils correctly require 2 kg; recipes specifying 100 g
  precious components retain those quantities. There is no universal 1/10 rule.
- Added Death to the 16-screen startup collection, based on Red Leaf's Sklotopolis
  screenshot, with the interface removed and new horror artwork. Credits remain.
- New captions and generated hints cover all four languages. Full regression,
  native layout/input, older-SDK, both SkloGraphics hook orders, packaged module
  gates and actual ModLoader lifecycle checks passed. Live GPU/server checks
  remain manual; see the installable README.txt checklist.

## Changes in 0.6.1

- Fixed toolbelt icon recursion that could abort HUD rendering after login.
- Missing, unreadable or invalid new catalog icons retain the existing item icon.
- Added execution checks for native toolbelt icon/size calls, both belt sizes,
  dragging, disabled replacement and incomplete-catalog fallback.

## Changes in 0.6.0

- Postbox adds a client-only mail workspace to native mailbox context menus.
  Incoming, Send and physical-mailbox views use high-res UI and native inventory
  behavior. Expand pending containers and inspect their supplied enchantments
  before accepting anything. Accept/pay or return individual packages, or accept
  and pay for the current list together when its complete cost is known.
- Prepare one item, several items or filled/nested containers for one recipient.
  Set COD and G/S/C/I prices directly in each item row; the name column is one
  third of its former width. Request the authoritative server postage quote
  with those prices retained, then use the separate final Send button. Editing or
  cancelling a quote never sends items. Changing contents invalidates the quote.
- Mail arrives in the physical mailbox. Take it into inventory before receiving
  another batch. Pending manifests have local Inspect; received/outgoing real
  inventory items retain native right-click actions and Examine.
- Postbox captions, hints and status templates support English, Brazilian
  Portuguese, German and Russian. Server messages and item/enchantment names
  retain their original text. See README.txt for the complete mail workflow.
- Includes the recent Timers -> Alarm Clock menu correction, startup update
  progress window, recipe history/Craft action and world-tool crafting fixes.

## Changes retained from 0.5.4

- Troll King Slayer now includes its bottom title and the source credit
  Cudlekinz | Sklotopolis in the collection's gold serif style.

## Changes retained from 0.5.2

- The recipe browser keeps per-session Back/Ahead history, including expanded
  recipes, selection and scroll position; closing clears it.
- Selected craftable recipe rows have a Craft action beside the magnifier.
  New controls and hints are localized in all four interface languages.

## Changes retained from 0.5.1

- Ground crafting updates preserve weight and damage separately. Floor looms and
  other heavy world tools remain usable after crafting batches.

## Changes retained from 0.4.10

- A single completed click in the skill browser opens the selected skill card.
- Child-skill headers show an explicit hierarchy, for example Mauls -> Small maul.
  Item names keep their original wording without a parent-skill prefix.
- Weapon overviews explain the effects on attack speed, damage and parrying.
- The attack summary uses the shorter Damage factor label. Table cells wrap
  without hiding values; text aligns left, numbers right, and cells align at top.
- Parry shows a calculated chance against a Venerable troll for the current
  fighting style. Its hover explains the reference opponent and assumptions:
  a ready weapon, neutral stance, current matching weapon QL or QL 50 if absent.
  The weapon's attempt gate is no longer presented as the final parry chance.
- Small Maul includes all six crushing/universal combat moves for the current
  server-assigned kingdom in Actions and Overview. Other kingdoms are hidden.
  The list shows skill requirements, duration and stamina cost; stance
  requirements are available on hover. A skill above 19 is required to begin.
- Updated text and layouts cover English, Brazilian Portuguese, German and
  Russian, including narrow windows and all five reading-size settings.

## Earlier corrections included in this update

This release also includes compact server forms and automatic scrollbar hiding,
blank skill-card fixes, the Metal altar caption, the compact bulk transfer form,
SkloGraphics expanded cave-buffer support, and the Timers menu mapping to Alarm
Clock. Keybinder, crafting, Waypointer, native camera behavior and the seventeen
startup screens retain the integrated updates described in the sections below.

[Download the latest ZIP](https://github.com/chamomilo/wurm-hud-remastered/releases/latest)

## Install or update manually

Requires Wurm Unlimited, Java 8 and Ago's Client Mod Launcher. No server mod is
required. Close the entire game client and WurmLauncher before installation.

1. Back up bindings, waypoints, alarms, camera state and mod settings.
   For existing Keybinder users, follow the migration instructions below.
2. Rename old standalone loader descriptors from .properties to
   .properties.disabled: WU-third_person_view, alarmclock, armor-material-colors,
   highres-hud, highres-startup, keybinder, wurm-highres, wurm-waypointer and
   wurm-vehicles-quick-turn.
   Keep predecessor standalone healthbar/selectbar/fighting HUD disabled too.
   Preserve their folders and user data; renamed descriptor settings are read.
3. Extract wurm-hud-remastered-0.9.4.zip into WurmLauncher, merging mods and
   replacing the Remastered descriptor if present.
4. Start through Client Mod Launcher. For a previous Remastered installation,
   the replaced descriptor selects the new versioned JAR.

The ZIP contains exactly three files:

    README.txt
    mods/wurm-hud-remastered.properties
    mods/wurm-hud-remastered/wurm-hud-remastered-0.9.4.jar

One JAR contains all ten components' code and their bundled resources.
Resource activation follows each component's switch. Existing user files keep
their legacy locations. No saved bindings, waypoints, alarms or overrides are
included. Avatar2 remains a separate mod.

## Moving from standalone Keybinder

When installing Remastered in the same WurmLauncher folder, existing Keybinder
bindings load automatically from their old location. Older saved formats are
supported; exporting and importing is not needed for this kind of upgrade.
Keep the mods/keybinder folder: it contains your saved bindings.

1. Close the entire game client and WurmLauncher. Make a backup outside the
   installation folder of mods/keybinder and these settings files, if present:
   mods/keybinder.properties (or mods/keybinder.properties.disabled),
   mods/keybinder.config and ~/.chamomilo/mod-settings/keybinder.properties.
   Here ~ means your user home directory, such as C:/Users/YourName on Windows.
2. Check that the backup contains these data files:

       mods/keybinder/keybinds.properties
       mods/keybinder/keybinds.properties.accounts

   The first file stores your binding definitions. The .accounts companion
   stores which bindings are enabled for each account; older installations may
   not have it. If you chose a custom Keybind file, back up that actual file
   and its .accounts companion instead, and note the configured path.
3. Rename only the standalone loader descriptor:
   mods/keybinder.properties -> mods/keybinder.properties.disabled.
   If it is already disabled, leave it disabled. Remastered reads settings from
   the renamed descriptor, including a custom dataFile path. Preserve the
   mods/keybinder folder and the settings files backed up in step 1.
4. Follow the manual installation steps above, merging the ZIP into the same
   WurmLauncher folder. The ZIP contains no saved bindings and does not replace
   your Keybinder data files.
5. Start through Client Mod Launcher. In Main menu > Wurm HUD Remastered, check
   that Keybinder is enabled; if you change its module switch, restart the
   entire client. Log in with your usual account and check the binding list,
   assigned keys and enabled states before deleting any backup.

If the list is empty, check Keybinder's Keybind file setting in the Remastered
settings page against the original file path. A path change takes effect after
a complete client restart and does not move or merge files. Close the client
before copying or restoring data; keep the definitions and .accounts companion
from the same backup together. Retain the original backup if you need to return
to an older standalone version, because newer saves may use a newer format.

For a different game folder or computer, copy the saved definitions and their
.accounts companion, if present, into the corresponding location before
starting the client. Preserve the settings from step 1 and check any custom
path on the destination. Back up destination data before replacing it.

To add old bindings to an existing Remastered collection, use Export all in
the old Keybinder, if available, then Import file in Remastered and select the
exported .keybinder file. Import file expects an exported .keybinder file, not
keybinds.properties. Imported bindings start disabled for review. Check their
keys, tools and targets, resolve key conflicts and enable the bindings you
want to use. Exact item or world-object references may need to be selected
again, especially for a different character or server.

## Common settings and language

Open Main menu > Wurm HUD Remastered or enter remastered settings in the console.
The first row selects English, Brazilian Portuguese, German or Russian. Language
changes apply immediately to the page and capable enabled components when the
HUD is ready. Existing component-specific language coverage is preserved.

Shared client integration delivers server events to observers before display filters. Examine metadata is tied to its outgoing request, exact target and recipient; an unrelated vehicle response cannot modify a selected creature. Managed wheel bindings, camera zoom and map/portrait scrolling have explicit ownership. Module switches still require a full restart.

Module switches, including Launcher compatibility and Quick Turn, precede the
enabled components' settings.
All modules default to enabled. Module switches apply after a complete client
restart; a disabled module is not constructed and installs no hooks. Other
settings identify immediate application or restart requirements.

Settings, language, window state, feature preferences and startup presentation
history share ~/.chamomilo/remastered.properties. Here ~ is the user's home.
Legacy per-module files are imported only when that module has no records in
the common config. Existing common records win; old files remain untouched and
are not written again. Concurrent feature saves preserve other sections, and
runtime saves preserve pending values that require a restart.

Waypoint and keybind data retain their existing separate files and custom paths.
Native client data, binary map caches, diagnostic exports and launcher snapshots
retain their own data formats; they are not additional settings files.

Settings and language are local. Remastered includes no updater, release-check
client or update catalogue. Existing network-backed feature functions, such as
Waypointer's map feeds, remain part of those features.

## Cumulative component guide

### Keybinder

Compared with the standalone baseline: [Keybinder v1.0.3](https://github.com/chamomilo/wurm-keybinder/releases/tag/v1.0.3).

Create action chains, Quick menus and Multi variants on a key, with tool and
target selection and the existing command catalogues.

- The queue monitor recovers actions already running when a binding starts and
  follows consecutive server timers. Current retains the sent command name and
  shows the actual game timer phase in parentheses. A brass divider separates it
  from planned actions in both expanded and collapsed views.
- Tool and target details belong to a correlated outgoing single-target command.
  Later tool selections or hover changes cannot rewrite the running row. Area
  requests keep their sent tool and initial target in Current without a duplicate
  planned row, including old bindings with only an area leaf. Repeated tile timers
  retain that context, labelled Sent. Missing observations and conflicting or
  expired matches show unknown
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

Compared with the standalone baseline: [Waypointer v1.10.11](https://github.com/chamomilo/wurm-waypointer/releases/tag/v1.10.11).

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
- Moving-creature classification reuses fixed parsing data and bounded tracking
  identities to reduce temporary allocations and GC pressure. Existing tracking
  IDs, account/server isolation, modifier rules and saved records are preserved.
- Diagnostics distinguish client ticks, render queues and frame output. A
  background worker can capture the active stack during a long call. Brief black
  flashes or reappearance of older frames still need live verification; this
  release does not claim a confirmed repair of their presentation/GPU cause.

Open Waypointer with its compass. General settings are now in Main menu >
Wurm HUD Remastered. Existing wurm-waypointer-data, configuration, map caches
and explicitly configured data paths remain in use. Network-backed map and deed
features retain their existing behaviour.

### High-res HUD

Compared with the standalone baseline: [High-res HUD v0.8.7](https://github.com/chamomilo/Wurm-HighRes-HUD/releases/tag/v0.8.7).

The unified Inventory, Containers, Character, Chat, Events, Build/recipes,
Healthbar, Select bar and Fighting HUD retain their native gameplay actions.

- K opens the skill browser with cards for all 138 skills, groups and
  characteristics. Double-click a skill or use Build skill help to open its card.
  Cards include Overview, Status, Actions, Skillgain, Titles, Relations and Wiki,
  themed artwork and links to related cards. Action tables compare the current
  value with skill milestones. Skillgain separates gain chance and gain amount,
  and lists current influencing factors. Status identifies calculation inputs.
- Enabled Remastered windows override overlapping SkloGraphics presentation.
  Chat and Events retain native channel models, history, input and saved bounds.
  Compatibility includes an older shared UI SDK loaded by another mod first.
- Native offscreen-buffer cleanup retires each GPU allocation once, including
  when Offscreen and FBO finalizers run in different GC cycles. It preserves
  shared scene-depth textures and the separate texture/renderbuffer namespaces.
  This prevents a late finalizer from deleting newer resources with reused
  numeric handles. The hook applies when High-res HUD is enabled; disappearance
  of the reported world-only black/stale-frame flashes still needs live testing.
- Pin any carried inventory or equipment item, including nested bag contents,
  through Pin to HUD in its normal context menu. One left click activates the
  exact item as a tool; a double click opens a container. Right click keeps its
  native actions and adds Unpin from HUD and the 70/44 px size choice.
- Pins can be dragged and retain item IDs, sizes and positions per server and
  character. Unavailable items keep their saved shortcut. A selected pin has
  a green inner outline, a clockwise travelling bright segment, a lower marker
  and a translucent face. Selecting another world object or inventory row clears
  this state; activating the item again by pin, inventory or hotkey restores it.
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
- Metal recipe variants share one catalogue row. Multiple options use a localized
  metal suffix; a single option shows its metal and is selected immediately.
  Only catalogued metals are offered. Selection switches the concrete recipe,
  requirements and model, including gold/silver altars. Material-neutral
  assemblies inherit their parts' options; alloy inputs keep their own metals.
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

Compared with the standalone baseline: [Alarm Clock v0.3.10](https://github.com/chamomilo/wurm-alarm-clock/releases/tag/v0.3.10).

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

Compared with the standalone baseline: [Third Person View v0.5.0](https://github.com/chamomilo/WU-3rd-person-view/releases/tag/v0.5.0).

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

Compared with the standalone baseline: [High-res Icons v0.2.5](https://github.com/chamomilo/wurm-high-res-icons/releases/tag/v0.2.5).

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

The runtime catalogue includes 1,441 reviewed artwork families (882 item and
559 world-object families), each at 64/32/16 px with approved material masks.
Exact native metadata selects the artwork; ambiguous or unavailable matches
retain the existing icon. New artwork continues in the separate development
library. Masters, source references and unfinished masks are excluded from ZIPs.

### Material Colors

Compared with the standalone baseline: [Material Colors v0.5.3](https://github.com/chamomilo/wurm-material-colors/releases/tag/v0.5.3).

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

Compared with the standalone baseline: [Startup Screen v0.5.2](https://github.com/chamomilo/wurm-highres-startup/releases/tag/v0.5.2).

Illustrated 1920 x 1080 JPEG loading screens retain the native loading text,
progress display and reconnect controls. Legacy 3840 x 2160 custom packs remain supported.

- The seventeen-screen collection includes credited Sklotopolis scenes:
  A Day of Climbing (FlpSilva), Avallone Docks (Encode), and A Fine Work (Mlemow),
  whose pinto horse looks into the dug pit, plus Need a brew ? (Wolfbane),
  showing a copper-still cellar. Troll King Slayer (Cudlekinz) adds an arena
  battle with a gold title and the credit Cudlekinz | Sklotopolis.
  Silverlake sermons at Revival event (Opene/Sklotopolis) preserves the Revival
  congregation after removing the source screenshot's interface. Death
  (Red Leaf | Sklotopolis) uses a deep abyss, layered clouds and falling fragments.
  Titles and source credits are on the images and preserved with the
  embedded collection.
- Choose a fixed named screen or Random. Random starts with a never-shown or
  least-recently-shown usable image. Subsequent five-second slides exclude images
  shown this loading session, then prefer those not shown on today's local date.
  If needed, today's images return; after exhausting the session, its flags reset
  and rotation continues. Reconnect begins a new loading session. The common
  config stores each actual presentation's UTC timestamp and current-session
  flag. Fixed selections are recorded too; discarded prefetch is never recorded.
- Images decode asynchronously and load directly from the single Remastered
  JAR. Settings are on the common local page and apply after a full restart.

Existing screen preferences remain compatible. No separate image JAR or loose
startup image directory is needed.

Compact PNG artwork keeps source alpha and window opacity. The pin is
256 x 234, the clock and compass layers are 256 x 256, and shared
material tiles repeat at 128 x 128. Native frames, buttons and icon
atlas geometry are preserved. Other PNGs use lossless compression;
the seventeen Full HD loading screens retain baseline JPEG encoding.

### Quick Turn

Quick Turn 1.0.1 is integrated with a separate On/Off block in Remastered settings.
The switch requires a complete client restart; disabled modules install no hooks.
Cart/wagon, hitch, rider and particle presentation retain the original behavior.
Native movement, collision, camera and outgoing packets remain under game control.
Boats, ridden creatures, dragged carts and passenger-only seats are excluded.
Legacy numeric tuning is read, while the Remastered switch owns startup enablement.
The existing vqt status/on/off commands remain temporary session controls and are
available in Keybinder with localized captions. Disable the standalone descriptor.

## Validation and source

The release build checks component regressions, native UI/input/layout probes,
four-language layouts, geometry, resource bytes and activation isolation. It
also runs twenty-three fresh packaged shared-loader scenarios and the complete
actual ModLoader lifecycle with all components enabled and all disabled.
The SDK is pinned to high-res UI 0.4.15 and embedded exactly once, retaining
font and component notices. The ZIP whitelist is checked against all three files.

Each component has a README.remastered.md in its features directory with the
same cumulative guide. This public repository contains documentation and the
installation ZIP. Full project sources and development research remain local.
Use this root guide for Remastered installation, settings and package contents.

Sources, research, previews, experimental icon caches and disposable files are
excluded from the installation ZIP. Required licence notices remain in the JAR.
Live GPU rendering and server gameplay require manual verification in the game.


## Interface compatibility

Enabled Remastered interfaces take priority over overlapping SkloGraphics UI.
SkloGraphics remains responsible for other interfaces and world rendering.
Compatibility is checked against the supplied skloGraphics (3).zip in both hook
orders, including an older shared UI SDK loaded first. Native IDs, inventory
models, chat history/input and server form answers are retained.

K and the Skills menu open the Remastered skill browser. Build skill help opens
the corresponding card. Rename forms, Journal entry pages, standalone Character,
Equipment and the native Menu bar use the shared presentation. Mod-owned text
supports English, Brazilian Portuguese, German and Russian. Original server
content, player/item names and external Wiki text retain their original wording.
