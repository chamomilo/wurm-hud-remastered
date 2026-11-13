Wurm HUD Remastered 0.6.0

Eight selectable Wurm Unlimited client components in one installation.
No server mod is required. The interface supports English, Brazilian
Portuguese, German and Russian. Player names, item names, enchantments and
verbatim server messages retain the wording supplied by the game/server.

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
   highres-hud, highres-startup, keybinder, wurm-highres and wurm-waypointer.
   Keep predecessor standalone healthbar/selectbar/fighting HUD disabled too.
   Preserve their folders and saved data. Avatar2 stays a separate mod.
3. Extract wurm-hud-remastered-0.6.0.zip into WurmLauncher, merging mods and
   replacing the Remastered descriptor. It selects the new versioned JAR.
4. Start through Client Mod Launcher. Open Main menu > Wurm HUD Remastered.
   Module switches apply after a COMPLETE client restart. Check your existing
   data before deleting any backup or old versioned JAR.

The ZIP contains exactly three files:

    README.txt
    mods/wurm-hud-remastered.properties
    mods/wurm-hud-remastered/wurm-hud-remastered-0.6.0.jar

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
- Startup Screen: the fifteen-screen loading collection and credited artwork.

Settings are on the local shared page; user data retains its legacy paths.
Recent integrated changes also include the startup update progress window,
per-session recipe Back/Ahead history, the recipe Craft action, and the fix
that keeps floor-loom damage separate from its crafting weight.

Enabled Remastered interfaces take priority over overlapping SkloGraphics UI.
Other SkloGraphics interfaces and effects remain available. The shared window
chrome supports reading size changes and opacity without changing game data.

CHECK IN GAME AFTER INSTALLING

1. Right-click a working spirit mailbox: Postbox appears and opens that box.
2. Expand an incoming filled/nested container, inspect a child's enchantments,
   then accept/pay one package. Verify it enters the mailbox and can be taken.
3. Try a mixed incoming list and Accept and pay for all. Check the displayed
   total, bank debit and physical contents. An occupied box blocks another batch.
4. Send one ordinary item, then several items including a filled container and
   COD. Check quote, recipient, prices and receipt on the receiving account.
5. Edit/cancel a quote and change box contents: nothing sends until final Send.
   Check refusal, insufficient funds and unavailable-service messages.
6. Check narrow windows, all four languages, reading controls, ordinary Examine,
   and coexistence with SkloGraphics. Also check recipes, bindings and timers.

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
Need a brew ? (Wolfbane), and Troll King Slayer (Cudlekinz | Sklotopolis).
See the published component guides and embedded notices for original projects.
