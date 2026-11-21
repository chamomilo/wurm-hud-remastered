Wurm HUD Remastered 0.7.4

Nine selectable Wurm Unlimited client components in one installation.
No server mod is required. The interface supports English, Brazilian
Portuguese, German and Russian. Player names, item names, enchantments and
verbatim server messages retain the wording supplied by the game/server.

ADDED IN 0.7.4

Containers now has Show on map immediately before Add to monitor. Toggle it to
show the loaded containers matching the current filters as blue stars on both
the full map and mini-map. Mobs and Containers can be enabled independently.
Both use the same received catalogue and 250ms filter refresh, without extra
tracking requests, saved waypoint creation or a separate loading radius.
Moving containers retain live coordinates; cave/surface markers stay separated.
Changing the list filters updates its enabled layer. The layer resets on session
teardown, like Mobs.

Route Statistics has three NAV LINE style buttons and a green NAV toggle.
Disable NAV here to pause navigation; enable it again to resume the same target.
Off-road, road and highway speeds start at 8/16/24 km/h. Movement samples learn
actual speeds independently for walking and each vehicle during the session.
Measured speeds update ETA. Stops, teleports and surface/transport transitions
are excluded; an unmeasured surface keeps its default estimate.

The startup collection now contains 17 screens. Silverlake sermons at Revival
event is credited to Opene/Sklotopolis and uses the supplied scene with its
interface removed. The short settings caption keeps the complete title and
credit in the hint. Death retains its ID and Red Leaf/Sklotopolis credit with
new deep, layered abyss artwork conveying a fall into oblivion.

The avatar portrait investigation is deferred as requested; no portrait changes
are included.

FIXED IN 0.7.3

Full-map resizing now survives rendered frames. Native WorldMap.update no longer
resets this custom map to 926x645 after every pointer movement. Use the lower-left
grip to change width and height independently; the top and right edges stay fixed.
Other servers retain their native fixed-size map behavior.

FIXED IN 0.7.2

Includes 579 newly completed world-object icon families from the development
library. The installed catalog now contains 2,020 ready families: 882 item and
1,138 world-object families, with 64/32/16-pixel artwork and reviewed masks.
Unfinished artwork remains excluded.

Drag single items, several selected items or filled containers into Postbox
without the inventory-handler crash. Incoming mail lists and quote forms no
longer act as physical inventory drop targets.

World hover text is restored, including food storage bin names and creature
descriptions. Container weights continue to use the available server data.

Cave-map artwork now loads correctly through the shared game loader, preventing
the repeated HUD rendering error. Hovering dropdowns no longer overflows the
stack. Keybinder waits for the connection before requesting the recipe catalog.

Manual Examine replies remain visible in Events, including drink quality sent
by the server. This also applies with several selected items and pending
background metadata requests.

Both maps refresh from the entire received surface tile buffer once a second,
including terrain edits made by other players and changes in tile state. This
uses existing server data without additional requests. Exact packet coordinates
prevent wrapped buffer slots from appearing at unrelated map locations.
Surface mini-map zoom-out now covers up to 480 tiles per side instead of 160,
so enlarged mini-map windows can show a wider area.
Its contour interval, north/heading orientation, size and zoom are saved locally
in .chamomilo/mod-settings/wurm-waypointer-ui.properties under your user home.
They survive window recreation, reconnects and restarts; saved dimensions fit
the current HUD. Surface and cave zoom ranges remain independent.

The full map has one lower-left resize button, matching the mini-map treatment.
Drag horizontally or vertically to resize those axes independently, down to a
480x360 minimum. The old four-corner resize mechanism has been removed.

The skill tracker's gain heading follows Recent/Session mode immediately.

Model-name decoding no longer modifies shared storage, preventing concurrent
readers from corrupting native resource paths.

Map texture updates preserve the renderer's texture bindings. The corrected
state leak could disrupt the HUD; check the cave map and underground stability
in your game session after updating.

This ZIP includes all previously integrated crafting, Skills, maps, Quick Turn,
loading-screen and reviewed icon updates below.

NEW IN 0.7.1

All 1,441 ready icon families are integrated: 882 item and 559 world-object
families, each at 64/32/16 pixels with approved material masks. This includes
young lemon, orange and willow, and the repaired walnut wood mask. Exact native
metadata selects artwork; ambiguous matches retain the existing icon. Unfinished
masks and source masters remain in the separate development library.

NEW IN 0.7.0

Quick Turn is integrated as a separate component with its own On/Off settings
block. The switch applies after a complete client restart. It preserves the
standalone numeric tuning and vqt console commands; console On/Off is temporary.
Disable the standalone wurm-vehicles-quick-turn.properties before installation.

Both maps use compact terrain artwork. The main map has an outside frame,
one lower-left resize button and a single-row toolbar that scrolls horizontally with
the mouse wheel or dragging. It reopens at its default size. The mini-map has
a lower-left resize grip and lower-right compass switch for north up / heading
up. Terrain, markers, routes and deed borders rotate together; labels stay
horizontal. Following uses continuous player coordinates with smooth easing.

Mobs has a Show on map switch for the current filtered list. Both maps show
peaceful types in green and aggressive types in red, independently of attitude
and Fo effects. Points follow loaded client actors; hover shows the exact name.
No server tracking requests are added. Exact animal and Exact age each have
their own highlight selector, On/Off and color. Waypoints has a left-hand delete
cross, no Copy column, and measured widths before allocating space to Name.

Skills includes Faith, Favor and Alignment with deity-specific guidance,
including Ivan. Religion uses confirmed own-player server messages instead
of the client's unused Atheist default. If initially unknown, pray once to
identify your deity; priest status needs a confirming server message. Opening
any skill card selects Overview. Small maul Parry includes a Venerable troll
sample with an iron QL90 small maul and full assumptions in its hover. Mining's
diagonal image corruption is fixed without changing its source pixels; all
138 skill images have been checked for the same upload-alignment defect.

Build auto-picks tools from nested backpacks, including before choosing metal.
Damaged stored items have a square hammer Repair button. Next QL estimates
expected successful-action base quality, with assumptions in its hover.
Single-stage recipes hide Continue. Required metal is red until selected,
and ingredient requirements stay hidden until then. Container hovers include
weight in inventory and world/Select, using available server data. Unknown
nearby containers may need one bounded metadata request; unknown is not zero.

Recipe-specific precious-metal quantities are preserved. On this Wurm Unlimited
baseline, the precious group is gold, silver and electrum. There is no general
one-tenth multiplier: small anvils require 2 kg for every supported metal;
recipes specifying 100 g precious lumps retain that reduced requirement.

Start Screens adds Death, based on Red Leaf's Sklotopolis screenshot, with
the interface removed and new horror artwork. The collection now has 16 screens.

FIXED IN 0.6.1

Fixed toolbelt icon recursion that could interrupt HUD rendering after login.
Items without a new catalog icon keep their existing icon. Failed or invalid
new textures also fall back to the existing icon.

NEW IN 0.6.0: POSTBOX

Right-click a working mailbox and choose Postbox. It has three views:
Incoming, Send mail and In the mailbox. Mail service availability, prices,
recipient checks and item restrictions remain controlled by the server.

Postbox works with spirit houses, cottages, mansions and castles, including
renamed objects and server variants that actually offer native mail actions.
A matching display name alone does not turn an ordinary container into mail.

Receiving and inspecting mail

1. Open Postbox on the mailbox you intend to use. Its physical inventory must
   finish loading. Empty an occupied mailbox before requesting incoming mail.
2. On Incoming, refresh the list. Expand containers and select any item to see
   the sender, quality, damage, expiry and supplied enchantment names/powers.
   Selecting or inspecting an attachment does not accept it or spend money.
3. Use Accept / pay for the selected package, or Return package to refuse it.
   A container and everything inside it form one package. Selecting a child
   still acts on that whole package. Already-returned mail cannot be returned
   again when the server omits that option.
4. Accept and pay for all covers every package in the CURRENT server list,
   including free items, COD and returned-mail retrieval charges whose exact
   prices were supplied. The list count and aggregate bank charge are shown.
   The action is unavailable if the mailbox is occupied, an operation is in
   progress, the balance is insufficient or a complete price/balance is unknown.
   It never selects only the affordable items or silently pays for unseen pages.
5. Accepted mail goes into the PHYSICAL MAILBOX, not straight into your bags.
   Open In the mailbox, then use Take into inventory or ordinary inventory
   actions. Empty it before refreshing/receiving the next batch. Servers may
   limit one incoming list to 100 top-level packages.

The server sometimes leaves charge cells blank. Postbox shows an unknown
amount instead of inventing free postage. Receiving one such package requires
an explicit warning confirmation authorizing the server-defined charge.

Before receipt, right-click offers Inspect mail manifest. The pending form
has no real world item ID, so ordinary server Examine is unavailable there.
After receipt, and for owned outgoing items, the real inventory retains normal
right-click actions and Examine. Unprovided weight/model/hidden properties
are not fabricated. Expiry and return rules follow the server.

Sending one item, several items or a filled container

1. Choose Send mail. Drag the actual items from your inventory into the mailbox
   using normal inventory transfer. Filled containers and nested contents stay
   together. Inspect them through their normal inventory menus as needed.
2. Use Prepare shipment. Enter one recipient for the whole batch. Each listed
   top-level row has its own COD checkbox and G/S/C/I price fields. The item-name
   column uses one third of its previous width; full names remain in hints.
   Unchecked COD means normal postage paid by the sender. Quality/damage help
   distinguish equal item names. Enter COD prices directly in their item rows.
   Every physical top-level mailbox item is included. Take unwanted items out
   before preparing the shipment, especially previously received mail.
3. Use Calculate postage. The server validates the recipient/items and returns
   its actual quote beside the same rows, retaining your entered prices.
   Use whole G/S/C/I amounts, 0 through 99 in each field.
   The recipient pays your COD price plus postage;
   you receive your price. Normal postage is charged to the sender.
4. Review the recipient, contents, server postage and payment modes. Only the
   final Send shipment button dispatches the goods. Enter, Inspect, editing,
   changing tabs, closing and cancelling do not send a shipment.
5. If the mailbox contents change, prepare a fresh quote. Repeat transaction
   clicks are blocked. Follow the operation status and actual server messages;
   a submitted request is not advertised as successful delivery or acceptance.

Mail sends game items, including supported inscribed paper/papyrus. It does not
add an unsupported email-text composer or delivery/read tracking. The server
can reject coins, unfinished items, locked/unavailable goods and other restricted
contents. One batch has one recipient; use separate batches for other people.

INSTALL OR UPDATE MANUALLY

Requires Wurm Unlimited, Java 8 and Ago's Client Mod Launcher.
Download: https://github.com/chamomilo/wurm-hud-remastered/releases/latest

1. Close the entire game client AND WurmLauncher. Back up bindings, waypoints,
   alarms, camera state and mod settings outside the installation directory.
2. Disable duplicate standalone loader descriptors by renaming .properties to
   .properties.disabled: WU-third_person_view, alarmclock, armor-material-colors,
   highres-hud, highres-startup, keybinder, wurm-highres, wurm-waypointer and
   wurm-vehicles-quick-turn.
   Keep predecessor standalone healthbar/selectbar/fighting HUD disabled too.
   Preserve their folders and saved data. Avatar2 stays a separate mod.
3. Extract wurm-hud-remastered-0.7.4.zip into WurmLauncher, merging mods and
   replacing the Remastered descriptor. It selects the new versioned JAR.
4. Start through Client Mod Launcher. Open Main menu > Wurm HUD Remastered.
   Module switches apply after a COMPLETE client restart. Check your existing
   data before deleting any backup or old versioned JAR.

The ZIP contains exactly three files:

    README.txt
    mods/wurm-hud-remastered.properties
    mods/wurm-hud-remastered/wurm-hud-remastered-0.7.4.jar

One JAR contains all code, enabled modules' resource packs and the pinned
high-res UI SDK. No research, scripts, logs, screenshots, loose assets,
experimental packs or saved player profiles are included.

Moving from standalone Keybinder

Keep mods/keybinder and its keybinds.properties and
keybinds.properties.accounts files. If a custom Keybind file was configured,
back up that file and its .accounts companion instead. Older accounts may not
have the companion. Back up mods/keybinder.properties (or its disabled copy),
mods/keybinder.config and ~/.chamomilo/mod-settings/keybinder.properties too.
Here ~ means your Windows user home directory.

Rename only the standalone loader descriptor; do not delete its data folder.
Remastered reads the old settings and bindings in the same WurmLauncher folder.
No export/import is needed for this migration. If bindings appear empty, check
Keybinder's Keybind file setting against the old path, then restart. A path
change does not move or merge files. Restore matching backup files together
while the client is closed.

THE INCLUDED COMPONENTS

- Keybinder: existing bindings, action queues and account selections.
- Waypointer: waypoints, compass and navigation with preserved saved data.
- High-res HUD: inventory/containers, Chat, Events, Build/recipes, Skills/cards,
  character/equipment, menu, health/select/fighting panels, pins and Postbox.
- Alarm Clock: alarms and timers; HUD Settings > Timers opens Alarm Clock.
- Third Person View: the native-compatible camera controls and saved state.
- High-res Icons: the reviewed integrated item-icon pack.
- Material Colors: the supported material palettes and masks; SkloGraphics
  retains unrelated lighting, shaders and world effects.
- Startup Screen: the seventeen-screen loading collection and credited artwork.
- Quick Turn: responsive cart/wagon visual steering, hitch/rider/particle follow.

Settings are on the local shared page; user data retains its legacy paths.
Recent integrated changes also include the startup update progress window,
per-session recipe Back/Ahead history, the recipe Craft action, and the fix
that keeps floor-loom damage separate from its crafting weight.

Enabled Remastered interfaces take priority over overlapping SkloGraphics UI.
Other SkloGraphics interfaces and effects remain available. The shared window
chrome supports reading size changes and opacity without changing game data.

CHECK IN GAME AFTER INSTALLING

For 0.7.4 and the retained map-resize fix:

1. Resize the full map with its lower-left grip in both axes. Dimensions survive
   movement and rendered frames; top/right anchors stay fixed. Reopen the map.
2. On Containers, filter the list and enable Show on map. Blue stars appear on
   both maps for matching loaded containers, with names on hover. Disable this
   layer while Mobs stays enabled; its animal markers remain visible.
3. Open Route Statistics during navigation. Click all three NAV LINE styles:
   the selected style and route rendering change together. NAV starts green;
   turn it off and on to pause and resume the same target from this window.
4. Travel steadily for several seconds on off-road, road and published highway
   surfaces. The corresponding default 8/16/24 km/h row becomes measured and ETA
   updates. Stopping must not overwrite the travelling speed with zero.
5. Change vehicle or dismount: a new transport starts with its own defaults.
   Return to the previous transport to restore its session measurements.
   Reconnect to verify session cleanup and ordinary map/navigation behavior.
6. Choose Silverlake sermons, restart and inspect its picture/title/credit.
   Repeat with Death: the abyss has visible depth and the original credit.
   Check Random rotation, narrow settings and all four interface languages.

Earlier integrated fixes:

1. Drag one item, several selected items and a filled container into Postbox's
   Send and Mailbox inventory views. The client stays open and the selected
   items move into the physical mailbox with their nested contents retained.
2. Drop over Incoming and a draft/quote form: no transfer occurs. Preparing or
   cancelling a quote never sends mail; only the separate final Send does.
3. Hover a renamed food storage bin, a ground item and a creature. Their names
   and original server descriptions remain visible; known weights still appear.
   Hover dropdowns in server forms: the selected value appears without freezing.
   Examine a drink manually: the server's description and QL reach Events.
4. Enter a cave, enable Cave view, walk and mine. Check received terrain and
   updates with contours on/off. HUD text, icons and windows should stay stable.
5. Leave and re-enter the cave, then reconnect. Repeat the hover and Postbox
   checks and confirm normal inventory transfers and toolbelt actions.

Earlier integrated changes:

1. Disable the standalone Quick Turn descriptor manually. Toggle the integrated
   Quick Turn block and restart: enabled carts/wagons turn promptly with their
   hitch/rider; disabled mode uses native steering. Check boats and ridden horses.
2. Open Mining and other skill cards: images are straight and each opening starts
   on Overview. Inspect Faith/Favor/Alignment, pray to Ivan and check confirmed
   deity. Inspect small maul Parry and its sample assumptions.
3. Choose small anvil: metal is required/red, requirements are hidden until a
   selection, the backpack mallet auto-picks, Continue is absent and Next QL is
   numeric after materials/skills are known. Click Repair on a damaged tool.
4. Hover filled containers in inventory and world/Select: weights appear when
   metadata is known, without counting nested contents twice. Ordinary Open and
   inventory transfers still work.
5. Check terrain artwork on both maps, lower-left resize buttons, scrolling main toolbar,
   default main-map size on reopen and the mini-map compass toggle. Turn/move:
   points, routes and deed borders rotate together; labels remain horizontal.
6. Test Show on map with filtered peaceful/aggressive mobs and exact-name hovers;
   Exact animal/age colors; waypoint delete cross. Select Death at the next start.
   Check narrow windows, four languages, SkloGraphics, bindings, timers and Postbox.

Native parser/serializer, UI/layout, regression and loader checks are automated.
Live server transactions, real GPU rendering and delivery require these manual
in-game checks. No game installation files are changed by the build process.

GUIDES, CREDITS AND LICENCES

Component guides: https://github.com/chamomilo/wurm-hud-remastered
The public repository contains documentation; project source/research stays local.
Original namespaces, saved data and required notices are preserved in the JAR.
The embedded high-res UI SDK is pinned to 0.4.15 and included once.

Startup artwork credits remain on the images. The collection includes
A Day of Climbing (FlpSilva), Avallone Docks (Encode), A Fine Work (Mlemow),
Need a brew ? (Wolfbane), Troll King Slayer (Cudlekinz | Sklotopolis), and
Death (Red Leaf | Sklotopolis), and Silverlake sermons at Revival event
(Opene/Sklotopolis).
Compact terrain artwork comes from the user-supplied Thources Minimap 1.0.0
reference archive. Its executable mod classes are not included.
See the published component guides and embedded notices for original projects.
