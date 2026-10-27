# High-res HUD in Wurm HUD Remastered

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

Install and configure this component using the [Remastered guide](../../README.md).
