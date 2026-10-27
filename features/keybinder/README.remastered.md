# Keybinder in Wurm HUD Remastered

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

Install and configure this component using the [Remastered guide](../../README.md).
